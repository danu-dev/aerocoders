<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
import RotatingText from './ui/RotatingText.vue'

onMounted(() => {
  const timeline = gsap.timeline({ defaults: { ease: 'power3.out' } })

  timeline
    .fromTo('.hero-badge', { y: 14, autoAlpha: 0 }, { y: 0, autoAlpha: 1, duration: 0.45 })
    .fromTo('.hero-title', { y: 24, autoAlpha: 0 }, { y: 0, autoAlpha: 1, duration: 0.6 }, '-=0.15')
    .fromTo('.hero-subtitle', { y: 20, autoAlpha: 0 }, { y: 0, autoAlpha: 1, duration: 0.55 }, '-=0.2')
    .fromTo(
      '.hero-cta',
      { y: 16, autoAlpha: 0 },
      { y: 0, autoAlpha: 1, duration: 0.5, stagger: 0.1, clearProps: 'opacity,transform,visibility' },
      '-=0.25'
    )
})
</script>

<template>
  <section id="home" class="relative min-h-[calc(100dvh-72px)] md:min-h-[100dvh] flex flex-col items-center justify-center pt-[90px] sm:pt-24 px-5 sm:px-6 pb-14 sm:pb-20 overflow-hidden bg-white font-poppins">
    <div class="absolute inset-0 opacity-[0.03] pointer-events-none" style="background-image: radial-gradient(#8B5CF6 0.5px, transparent 0.5px); background-size: 30px 30px;"></div>

    <div class="max-w-5xl mx-auto w-full mt-1 sm:mt-4 md:mt-0 flex flex-col items-center text-center relative z-10">
      <!-- Trust Signal -->
      <div class="hero-badge inline-flex items-center gap-2 px-2.5 sm:px-3 py-1 sm:py-1.5 rounded-full border border-purple-100 bg-purple-50/50 mb-5 sm:mb-10">
        <span class="relative flex h-2 w-2">
          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-[#8B5CF6] opacity-75"></span>
          <span class="relative inline-flex rounded-full h-2 w-2 bg-[#8B5CF6]"></span>
        </span>
        <span class="text-[9px] sm:text-[10px] font-bold uppercase tracking-[0.22em] sm:tracking-[0.3em] text-[#8B5CF6]">Terpercaya • 100+ Proyek Selesai</span>
      </div>

      <!-- Heading -->
      <h1 class="hero-title text-[1.9rem] sm:text-5xl md:text-7xl font-bold leading-[1.08] sm:leading-[1.1] tracking-tight sm:tracking-tighter text-[#1A1A1A] mb-5 sm:mb-8">
        Tugas Website-mu Beres,
        <span class="block mt-1">
          Dijamin
          <RotatingText
            :texts="['LULUS.', 'RAPI.', 'ON TIME.']"
            main-class-name="inline-flex ml-1.5 px-2 sm:px-2 md:px-3 bg-[#8B5CF6] text-white overflow-hidden py-0.5 sm:py-1 md:py-2 rounded-md sm:rounded-lg align-middle"
            stagger-from="last"
            :initial="{ y: '100%' }"
            :animate="{ y: 0 }"
            :exit="{ y: '-120%' }"
            :stagger-duration="0.025"
            split-level-class-name="overflow-hidden pb-0.5 sm:pb-1 md:pb-1"
            :transition="{ type: 'spring', damping: 30, stiffness: 400 }"
            :rotation-interval="2000"
          />
        </span>
      </h1>

      <!-- Subtext -->
      <p class="hero-subtitle text-[14px] sm:text-base md:text-xl font-light text-[#525252] mb-7 sm:mb-12 leading-relaxed max-w-2xl px-2 sm:px-0">
        Jasa pembuatan website profesional untuk tugas sekolah & kampus. Kami kerjakan sesuai brief dosen agar Anda bisa fokus pada hal lainnya.
      </p>

      <!-- CTA Group (FIXED) -->
      <div class="flex flex-col sm:flex-row gap-3 sm:gap-5 w-full sm:w-auto max-w-sm sm:max-w-none mt-1 mb-5 sm:mb-0 relative z-20">
        <button class="hero-cta inline-flex items-center justify-center w-full sm:w-auto px-8 sm:px-10 py-3.5 sm:py-4 bg-[#1A1A1A] text-white text-[11px] sm:text-xs font-bold uppercase tracking-[0.2em] sm:tracking-widest hover:bg-[#8B5CF6] transition-all duration-300 rounded-sm shadow-xl shadow-purple-500/10">
          Konsultasi Gratis
        </button>
        <button class="hero-cta inline-flex items-center justify-center w-full sm:w-auto px-8 sm:px-10 py-3.5 sm:py-4 border border-zinc-300 text-[#1A1A1A] bg-white text-[11px] sm:text-xs font-bold uppercase tracking-[0.2em] sm:tracking-widest hover:border-[#8B5CF6] hover:text-[#8B5CF6] transition-all duration-300 rounded-sm">
          Lihat Portofolio
        </button>
      </div>
    </div>

    <!-- Credibility Footer -->
    <div class="hidden sm:block absolute bottom-10 left-1/2 -translate-x-1/2 w-full text-center opacity-40">
      <p class="text-[9px] font-bold uppercase tracking-[0.4em] text-slate-400">Finalis Nasional JHIC 2025</p>
    </div>
  </section>
</template>
