<script setup>
import { computed, nextTick, onBeforeUnmount, onMounted, ref, watch } from 'vue'
import gsap from 'gsap'

const props = defineProps({
  texts: { type: Array, default: () => [] },
  rotationInterval: { type: Number, default: 2000 },
  initial: { type: Object, default: () => ({ y: '100%', opacity: 0 }) },
  animate: { type: Object, default: () => ({ y: 0, opacity: 1 }) },
  exit: { type: Object, default: () => ({ y: '-120%', opacity: 0 }) },
  animatePresenceMode: { type: String, default: 'wait' },
  animatePresenceInitial: { type: Boolean, default: false },
  staggerDuration: { type: Number, default: 0 },
  staggerFrom: { type: [String, Number], default: 'first' },
  transition: { type: Object, default: () => ({ type: 'spring', damping: 25, stiffness: 300 }) },
  loop: { type: Boolean, default: true },
  auto: { type: Boolean, default: true },
  splitBy: { type: String, default: 'characters' },
  onNext: { type: Function, default: undefined },
  mainClassName: { type: String, default: '' },
  splitLevelClassName: { type: String, default: '' },
  elementLevelClassName: { type: String, default: '' }
})

const currentTextIndex = ref(0)
const splitRootRef = ref(null)
const isAnimating = ref(false)
let intervalId = null

const cn = (...classes) => classes.filter(Boolean).join(' ')

const currentText = computed(() => {
  if (!props.texts.length) return ''
  return props.texts[currentTextIndex.value] ?? ''
})

const splitIntoCharacters = text => {
  if (typeof Intl !== 'undefined' && Intl.Segmenter) {
    const segmenter = new Intl.Segmenter('en', { granularity: 'grapheme' })
    return Array.from(segmenter.segment(text), segment => segment.segment)
  }
  return Array.from(text)
}

const elements = computed(() => {
  const text = currentText.value
  if (!text) return []

  if (props.splitBy === 'characters') {
    const words = text.split(' ')
    return words.map((word, index) => ({
      characters: splitIntoCharacters(word),
      needsSpace: index !== words.length - 1
    }))
  }

  if (props.splitBy === 'words') {
    const words = text.split(' ')
    return words.map((word, index) => ({
      characters: [word],
      needsSpace: index !== words.length - 1
    }))
  }

  if (props.splitBy === 'lines') {
    const lines = text.split('\n')
    return lines.map((line, index) => ({
      characters: [line],
      needsSpace: index !== lines.length - 1
    }))
  }

  const parts = text.split(props.splitBy)
  return parts.map((part, index) => ({
    characters: [part],
    needsSpace: index !== parts.length - 1
  }))
})

const toGsapStaggerFrom = value => {
  if (value === 'first') return 'start'
  if (value === 'last') return 'end'
  if (value === 'center') return 'center'
  if (value === 'random') return 'random'
  if (typeof value === 'number') return value
  return 'start'
}

const getMotionNodes = () => {
  if (!splitRootRef.value) return []
  return Array.from(splitRootRef.value.querySelectorAll('.rt-element'))
}

const getDuration = fallback => {
  if (typeof props.transition?.duration === 'number') return props.transition.duration
  return fallback
}

const getEase = fallback => {
  if (typeof props.transition?.ease === 'string') return props.transition.ease
  if (props.transition?.type === 'spring') return 'back.out(1.7)'
  return fallback
}

const animateIn = async () => {
  await nextTick()
  const nodes = getMotionNodes()
  if (!nodes.length) return

  gsap.fromTo(
    nodes,
    { ...props.initial },
    {
      ...props.animate,
      duration: getDuration(0.55),
      ease: getEase('power3.out'),
      stagger: {
        each: props.staggerDuration,
        from: toGsapStaggerFrom(props.staggerFrom)
      }
    }
  )
}

const changeIndex = newIndex => {
  currentTextIndex.value = newIndex
  if (props.onNext) props.onNext(newIndex)
}

const next = async () => {
  if (isAnimating.value || props.texts.length <= 1) return

  const atLast = currentTextIndex.value === props.texts.length - 1
  const nextIndex = atLast ? (props.loop ? 0 : currentTextIndex.value) : currentTextIndex.value + 1
  if (nextIndex === currentTextIndex.value) return

  const nodes = getMotionNodes()
  if (!nodes.length) {
    changeIndex(nextIndex)
    await animateIn()
    return
  }

  isAnimating.value = true
  gsap.to(nodes, {
    ...props.exit,
    duration: getDuration(0.4),
    ease: getEase('power2.in'),
    stagger: {
      each: props.staggerDuration,
      from: toGsapStaggerFrom(props.staggerFrom)
    },
    onComplete: async () => {
      changeIndex(nextIndex)
      await animateIn()
      isAnimating.value = false
    }
  })
}

const previous = async () => {
  if (isAnimating.value || props.texts.length <= 1) return
  const atFirst = currentTextIndex.value === 0
  const prevIndex = atFirst ? (props.loop ? props.texts.length - 1 : currentTextIndex.value) : currentTextIndex.value - 1
  if (prevIndex === currentTextIndex.value) return
  changeIndex(prevIndex)
  await animateIn()
}

const jumpTo = async index => {
  const target = Math.max(0, Math.min(index, props.texts.length - 1))
  if (target === currentTextIndex.value) return
  changeIndex(target)
  await animateIn()
}

const reset = async () => {
  if (currentTextIndex.value === 0) return
  changeIndex(0)
  await animateIn()
}

const startAutoRotation = () => {
  if (intervalId) clearInterval(intervalId)
  if (!props.auto || props.texts.length <= 1) return
  intervalId = setInterval(() => {
    next()
  }, props.rotationInterval)
}

defineExpose({ next, previous, jumpTo, reset })

watch(
  () => [props.auto, props.rotationInterval, props.texts.length],
  () => {
    startAutoRotation()
  }
)

onMounted(async () => {
  if (props.animatePresenceInitial) {
    await animateIn()
  } else {
    await nextTick()
    const nodes = getMotionNodes()
    if (nodes.length) gsap.set(nodes, { ...props.animate })
  }
  startAutoRotation()
})

onBeforeUnmount(() => {
  if (intervalId) clearInterval(intervalId)
})
</script>

<template>
  <span :class="cn('inline-flex flex-wrap whitespace-pre-wrap relative', mainClassName)">
    <span class="sr-only">{{ currentText }}</span>
    <span
      ref="splitRootRef"
      :class="cn(splitBy === 'lines' ? 'flex flex-col w-full' : 'flex flex-wrap whitespace-pre-wrap relative')"
      aria-hidden="true"
    >
      <span
        v-for="(wordObj, wordIndex) in elements"
        :key="`word-${wordIndex}-${currentTextIndex}`"
        :class="cn('inline-flex', splitLevelClassName)"
      >
        <span
          v-for="(char, charIndex) in wordObj.characters"
          :key="`char-${wordIndex}-${charIndex}-${currentTextIndex}`"
          :class="cn('rt-element inline-block', elementLevelClassName)"
        >
          {{ char }}
        </span>
        <span v-if="wordObj.needsSpace" class="whitespace-pre"> </span>
      </span>
    </span>
  </span>
</template>
