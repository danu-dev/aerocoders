<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  // Animasi Reveal Awal
  gsap.fromTo('.reveal-service',
    { y: 30, autoAlpha: 0 },
    {
      y: 0, autoAlpha: 1, stagger: 0.15, duration: 1, ease: 'expo.out',
      scrollTrigger: { trigger: '#layanan', start: 'top 85%' }
    }
  )

  // Google Scrub Effect (Infinity Scroll & Unscroll)
  gsap.to('.service-content-wrapper', {
    scrollTrigger: {
      trigger: '#layanan',
      start: 'top top',
      end: 'bottom 20%',
      scrub: 1,
    },
    y: -40,
    scale: 0.96,
    autoAlpha: 0,
    ease: 'none'
  })
})
</script>

<template>
  <section id="layanan" class="py-24 px-6 bg-white font-poppins relative overflow-hidden border-t border-zinc-50">
    <div class="service-content-wrapper max-w-5xl mx-auto relative z-10">

      <div class="flex flex-col items-center text-center md:items-start md:text-left mb-24">
        <div class="reveal-service flex items-center gap-3 mb-6">
          <div class="w-8 h-[1px] bg-[#8B5CF6]"></div>
          <span class="text-[9px] font-bold uppercase tracking-[0.4em] text-[#8B5CF6]">Layanan Komprehensif</span>
        </div>
        <h3 class="reveal-service text-3xl md:text-5xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1] mb-8 uppercase">
          Solusi Digital.<br /><span class="text-zinc-300 italic">Order Sekarang.</span>
        </h3>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-16 relative">
        <div v-for="(s, i) in [
          { n: '01', t: 'Frontend', d: 'Slicing UI menggunakan React atau Vue dengan standar industri.' },
          { n: '02', t: 'Fullstack', d: 'Sistem informasi terintegrasi Laravel atau Supabase.' },
          { n: '03', t: 'Mobile', d: 'Aplikasi Flutter untuk tugas akhir & skripsi mahasiswa.' }
        ]" :key="i" class="reveal-service group flex flex-col items-center text-center md:items-start md:text-left pt-10 border-t border-zinc-50">
          <span class="text-[10px] font-mono text-zinc-300 mb-6 tracking-widest group-hover:text-[#8B5CF6] transition-colors italic">/ {{ s.n }}</span>
          <h4 class="text-xs font-bold text-[#1A1A1A] uppercase tracking-widest mb-4">{{ s.t }}</h4>
          <p class="text-[11px] text-zinc-400 leading-relaxed font-light">{{ s.d }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
