<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import RotatingText from './ui/RotatingText.vue'

gsap.registerPlugin(ScrollTrigger)

const waNumber = "6283849521229"
const waMessage = encodeURIComponent("Halo Aerocode, saya mau order pengerjaan tugas website. Mohon info detailnya.")

onMounted(() => {
  const introTl = gsap.timeline({ defaults: { ease: 'power4.out' } })

  // 1. Animasi Masuk Awal (Intro)
  introTl
    .fromTo('.hero-badge', { y: 14, autoAlpha: 0 }, { y: 0, autoAlpha: 1, duration: 0.5 })
    .fromTo('.hero-title', { y: 24, autoAlpha: 0 }, { y: 0, autoAlpha: 1, duration: 0.65 }, '-=0.2')
    .fromTo('.hero-subtitle', { y: 20, autoAlpha: 0 }, { y: 0, autoAlpha: 1, duration: 0.6 }, '-=0.25')
    .fromTo('.hero-cta', { y: 16, autoAlpha: 0 }, { y: 0, autoAlpha: 1, duration: 0.55, stagger: 0.1 }, '-=0.3')

  // 2. Animasi Scroll Out & In (Google Style)
  // Menghilang saat scroll ke bawah, muncul kembali saat scroll ke atas
  gsap.to('.hero-content-wrapper', {
    scrollTrigger: {
      trigger: '#home',
      start: 'top top',
      end: 'bottom 20%',
      scrub: 1, // Memberikan efek transisi halus mengikuti scroll
    },
    y: -50,
    scale: 0.95,
    autoAlpha: 0,
    ease: 'none'
  })

  // Animasi khusus untuk pattern background agar terasa parallax
  gsap.to('.hero-bg-pattern', {
    scrollTrigger: {
      trigger: '#home',
      start: 'top top',
      end: 'bottom top',
      scrub: true
    },
    y: 100,
    ease: 'none'
  })
})
</script>

<template>
  <section id="home" class="relative min-h-screen flex flex-col items-center justify-center pt-20 px-6 overflow-hidden bg-white font-poppins selection:bg-[#8B5CF6] selection:text-white">

    <!-- Background Pattern dengan Parallax -->
    <div class="hero-bg-pattern absolute inset-0 opacity-[0.015] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 30px 30px;">
    </div>

    <div class="hero-content-wrapper max-w-4xl mx-auto w-full flex flex-col items-center text-center relative z-10">

      <div class="hero-badge inline-flex items-center gap-2 px-3 py-1.5 rounded-full border border-purple-100 bg-purple-50/50 mb-8">
        <span class="relative flex h-1.5 w-1.5">
          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-[#8B5CF6] opacity-75"></span>
          <span class="relative inline-flex rounded-full h-1.5 w-1.5 bg-[#8B5CF6]"></span>
        </span>
        <span class="text-[9px] sm:text-[10px] font-bold uppercase tracking-[0.3em] text-[#8B5CF6]">Pengerjaan Cepat • Bergaransi</span>
      </div>

      <h1 class="hero-title text-[1.6rem] sm:text-4xl md:text-5xl font-bold leading-[1.2] tracking-tighter text-[#1A1A1A] mb-8 px-2 uppercase">
        Tugas Website Beres,
        <span class="block mt-1">
          Hasil Pasti
          <RotatingText
            :texts="['MEMUASKAN.', 'RAPI.', 'AMAN.']"
            main-class-name="inline-flex ml-1.5 px-2 sm:px-3 bg-[#8B5CF6] text-white overflow-hidden py-0.5 sm:py-1 rounded-md align-middle shadow-lg shadow-purple-500/20"
            stagger-from="last"
            :initial="{ y: '100%' }"
            :animate="{ y: 0 }"
            :exit="{ y: '-120%' }"
            :stagger-duration="0.025"
            split-level-class-name="overflow-hidden pb-0.5 sm:pb-1"
            :transition="{ type: 'spring', damping: 30, stiffness: 400 }"
            :rotation-interval="2200"
          />
        </span>
      </h1>

      <p class="hero-subtitle text-[12px] sm:text-[13px] md:text-base font-light text-[#525252] mb-12 leading-relaxed max-w-xl px-4">
        Solusi joki website profesional untuk tugas sekolah, UTS, hingga skripsi. Kode rapi standar industri, bebas plagiasi, dan siap dikumpulkan tepat waktu.
      </p>

      <div class="flex flex-col sm:flex-row gap-3 sm:gap-4 w-full sm:w-auto max-w-xs sm:max-w-none relative z-20">
        <a :href="`https://wa.me/${waNumber}?text=${waMessage}`"
           target="_blank"
           rel="noopener noreferrer"
           class="hero-cta group relative inline-flex items-center justify-center px-10 py-3.5 bg-[#1A1A1A] text-white text-[10px] font-bold uppercase tracking-[0.2em] overflow-hidden transition-all duration-300 rounded-sm shadow-xl shadow-zinc-200">
          <span class="relative z-10">Order via WhatsApp</span>
          <div class="absolute inset-0 bg-[#8B5CF6] translate-y-full group-hover:translate-y-0 transition-transform duration-300"></div>
        </a>
        <a href="#portfolio"
           class="hero-cta inline-flex items-center justify-center px-10 py-3.5 border border-zinc-200 text-[#1A1A1A] bg-white text-[10px] font-bold uppercase tracking-[0.2em] hover:border-[#8B5CF6] hover:text-[#8B5CF6] transition-all duration-300 rounded-sm">
          Katalog Project
        </a>
      </div>
    </div>

    <!-- Info Penutup: Menggunakan detail profesional standar industri -->
    <div class="hidden sm:block absolute bottom-10 left-1/2 -translate-x-1/2 w-full text-center opacity-40">
      <p class="text-[8px] font-bold uppercase tracking-[0.4em] text-zinc-400 italic">/ Kode Bersih • Tanpa Plagiasi • Pengerjaan Presisi /</p>
    </div>
  </section>
</template>
