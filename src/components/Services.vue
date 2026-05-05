<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  const tl = gsap.timeline({
    scrollTrigger: {
      trigger: '#layanan',
      start: 'top 85%',
      toggleActions: 'play none none reverse'
    },
    defaults: { ease: 'expo.out', duration: 1.2 }
  })

  tl.fromTo('.reveal-service-text', { y: 30, autoAlpha: 0 }, { y: 0, autoAlpha: 1, stagger: 0.15 })
    .fromTo('.service-line-draw', { scaleX: 0 }, { scaleX: 1, duration: 1.5, stagger: 0.2 }, '-=1')
})
</script>

<template>
  <section id="layanan" class="py-20 md:py-32 px-6 bg-white font-poppins relative selection:bg-[#8B5CF6] selection:text-white overflow-hidden border-t border-zinc-50">

    <!-- Pattern: Subtle Dot Grid -->
    <div class="absolute inset-0 opacity-[0.02] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 30px 30px;">
    </div>

    <div class="max-w-5xl mx-auto relative z-10">

      <!-- Header: Centered on Mobile -->
      <div class="flex flex-col items-center text-center md:items-start md:text-left mb-24">
        <div class="reveal-service-text flex items-center gap-3 mb-6">
          <div class="w-8 h-[1px] bg-[#8B5CF6]"></div>
          <span class="text-[9px] font-bold uppercase tracking-[0.4em] text-[#8B5CF6]">Layanan Komprehensif</span>
        </div>

        <h3 class="reveal-service-text text-3xl md:text-5xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1] mb-8">
          Solusi Digital.<br />
          <span class="text-zinc-300 italic">Presisi & Bergaransi.</span>
        </h3>

        <p class="reveal-service-text max-w-lg text-[12px] md:text-[13px] text-zinc-500 font-light leading-relaxed">
          Menyediakan layanan pengembangan perangkat lunak dengan standar industri untuk kebutuhan akademik. Fokus pada kode yang bersih, terdokumentasi, dan siap dipresentasikan.
        </p>
      </div>

      <!-- Services Grid -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-16 md:gap-12 relative">

        <!-- Item 01: Frontend -->
        <div class="reveal-service-text group flex flex-col items-center text-center md:items-start md:text-left pt-10 relative">
          <div class="service-line-draw absolute top-0 left-0 w-full h-[1px] bg-zinc-100 origin-left"></div>
          <span class="text-[10px] font-mono text-zinc-300 mb-6 tracking-widest transition-colors group-hover:text-[#8B5CF6]">01 / FRONTEND</span>
          <h4 class="text-xs font-bold text-[#1A1A1A] uppercase tracking-widest mb-4">Slicing UI & Responsif</h4>
          <p class="text-[11px] text-zinc-400 leading-relaxed font-light">
            Konversi desain ke React atau Vue dengan tingkat presisi tinggi. Optimal untuk tugas pemrograman web modern.
          </p>
        </div>

        <!-- Item 02: Fullstack -->
        <div class="reveal-service-text group flex flex-col items-center text-center md:items-start md:text-left pt-10 relative">
          <div class="service-line-draw absolute top-0 left-0 w-full h-[1px] bg-zinc-100 origin-left"></div>
          <span class="text-[10px] font-mono text-zinc-300 mb-6 tracking-widest transition-colors group-hover:text-[#8B5CF6]">02 / FULLSTACK</span>
          <h4 class="text-xs font-bold text-[#1A1A1A] uppercase tracking-widest mb-4">Sistem CRUD & UAS</h4>
          <p class="text-[11px] text-zinc-400 leading-relaxed font-light">
            Pengembangan sistem informasi terintegrasi menggunakan Laravel atau Supabase. Siap pakai untuk project UAS.
          </p>
        </div>

        <!-- Item 03: Mobile -->
        <div class="reveal-service-text group flex flex-col items-center text-center md:items-start md:text-left pt-10 relative">
          <div class="service-line-draw absolute top-0 left-0 w-full h-[1px] bg-zinc-100 origin-left"></div>
          <span class="text-[10px] font-mono text-zinc-300 mb-6 tracking-widest transition-colors group-hover:text-[#8B5CF6]">03 / MOBILE</span>
          <h4 class="text-xs font-bold text-[#1A1A1A] uppercase tracking-widest mb-4">Aplikasi Flutter</h4>
          <p class="text-[11px] text-zinc-400 leading-relaxed font-light">
            Pembuatan aplikasi mobile lintas platform dengan fitur lengkap dan original untuk tugas akhir atau skripsi.
          </p>
        </div>
      </div>

      <!-- Simplified CTA -->
      <!-- <div class="reveal-service-text mt-24 flex justify-center md:justify-start">
        <a href="https://wa.me/6283849521229" target="_blank" class="group flex items-center gap-6">
          <div class="relative">
            <div class="w-12 h-12 rounded-full border border-zinc-100 flex items-center justify-center group-hover:border-[#8B5CF6] transition-all duration-500">
              <svg class="w-4 h-4 text-zinc-400 group-hover:text-[#8B5CF6] transition-colors" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 8l4 4m0 0l-4 4m4-4H3" />
              </svg>
            </div>
          </div>
          <div class="flex flex-col items-start text-left">
            <span class="text-[9px] font-bold uppercase tracking-[0.3em] text-zinc-300 group-hover:text-[#8B5CF6] transition-colors italic">Bimbingan Teknis Tersedia</span>
            <span class="text-[11px] font-bold text-[#1A1A1A] uppercase tracking-widest border-b border-zinc-100 group-hover:border-[#8B5CF6] transition-all">Konsultasi Tugas Sekarang</span>
          </div>
        </a>
      </div> -->

    </div>
  </section>
</template>
