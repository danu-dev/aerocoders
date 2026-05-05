<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  // Animasi Alur Kerja
  const flowTl = gsap.timeline({
    scrollTrigger: {
      trigger: '#alur',
      start: 'top 85%',
      toggleActions: 'play none none reverse'
    },
    defaults: { ease: 'expo.out', duration: 1.2 }
  })

  flowTl.fromTo('.reveal-step', { y: 30, autoAlpha: 0 }, { y: 0, autoAlpha: 1, stagger: 0.15 })
    .fromTo('.step-line', { scaleY: 0 }, { scaleY: 1, duration: 1.5 }, '-=1')

  // Animasi Jaminan
  gsap.fromTo('.reveal-rule',
    { y: 20, autoAlpha: 0 },
    {
      y: 0,
      autoAlpha: 1,
      stagger: 0.1,
      scrollTrigger: {
        trigger: '#jaminan',
        start: 'top 85%'
      }
    }
  )
})
</script>

<template>
  <!-- Seksi Alur Kerja -->
  <section id="alur" class="py-20 md:py-32 px-6 bg-white font-poppins relative selection:bg-[#8B5CF6] selection:text-white overflow-hidden border-t border-zinc-50">
    <div class="max-w-5xl mx-auto relative z-10">
      <div class="grid lg:grid-cols-12 gap-16 lg:gap-24">

        <!-- Header: Centered on Mobile -->
        <div class="lg:col-span-5 flex flex-col items-center text-center md:items-start md:text-left lg:sticky lg:top-32 h-fit">
          <div class="reveal-step flex items-center gap-3 mb-6">
            <div class="w-8 h-[1px] bg-[#8B5CF6]"></div>
            <span class="text-[9px] font-bold uppercase tracking-[0.4em] text-[#8B5CF6]">Alur Kerja</span>
          </div>
          <h3 class="reveal-step text-2xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-tight mb-8">
            Proses Mudah, <br /><span class="text-zinc-300 italic">Terima Beres.</span>
          </h3>
          <p class="reveal-step text-[11px] text-zinc-400 font-light leading-relaxed max-w-xs">
            Kami merancang sistem pengerjaan yang praktis agar Anda dapat fokus pada hal lain sementara proyek diselesaikan dengan presisi standar industri.
          </p>
        </div>

        <!-- Steps List -->
        <div class="lg:col-span-7 space-y-12 relative">
          <div class="step-line absolute left-0 md:left-4 top-0 w-[1px] h-full bg-zinc-50 origin-top hidden md:block"></div>

          <div v-for="(step, index) in [
            { n: '01', t: 'Konsultasi Brief', d: 'Diskusi detail tugas, fitur, dan deadline via WhatsApp.' },
            { n: '02', t: 'Booking Slot', d: 'Estimasi biaya transparan dan pembayaran DP untuk amankan jadwal.' },
            { n: '03', t: 'Review & Demo', d: 'Cek kualitas melalui video demo sebelum penyerahan final.' },
            { n: '04', t: 'Handover File', d: 'Pelunasan dan pengiriman seluruh source code langsung ke Anda.' }
          ]" :key="index" class="reveal-step group relative md:pl-16 flex flex-col items-center text-center md:items-start md:text-left">
            <span class="text-[10px] font-mono text-zinc-300 mb-2 tracking-widest group-hover:text-[#8B5CF6] transition-colors italic">/ Step {{ step.n }}</span>
            <h4 class="text-xs font-bold text-[#1A1A1A] mb-3 uppercase tracking-widest">{{ step.t }}</h4>
            <p class="text-[11px] text-zinc-500 font-light leading-relaxed max-w-sm">{{ step.d }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Seksi Jaminan Kualitas -->
  <section id="jaminan" class="py-20 md:py-32 px-6 bg-white font-poppins relative selection:bg-[#8B5CF6] selection:text-white border-t border-zinc-50 overflow-hidden">
    <div class="max-w-5xl mx-auto relative z-10">
      <div class="grid lg:grid-cols-12 gap-16 items-start">

        <div class="lg:col-span-5 flex flex-col items-center text-center md:items-start md:text-left">
          <div class="reveal-rule flex items-center gap-3 mb-6">
            <div class="w-8 h-[1px] bg-[#8B5CF6]"></div>
            <span class="text-[9px] font-bold uppercase tracking-[0.4em] text-[#8B5CF6]">Proteksi</span>
          </div>
          <h3 class="reveal-rule text-2xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1] mb-8">
            Privasi Aman.<br />
            <span class="text-zinc-300 italic">Nilai Terjamin.</span>
          </h3>
          <p class="reveal-rule text-[11px] text-zinc-400 font-light leading-relaxed max-w-xs">
            Komitmen kami adalah memberikan keamanan data dan kualitas kode orisinal untuk kepuasan akademik Anda.
          </p>
        </div>

        <div class="lg:col-span-7 divide-y divide-zinc-50">
          <div v-for="(rule, index) in [
            { t: 'Garansi Revisi', d: 'Dukungan revisi penuh sampai proyek siap dikumpulkan.' },
            { t: 'Anonimitas', d: 'Identitas dan detail proyek dijaga kerahasiaannya 100%.' },
            { t: 'Zero Plagiarism', d: 'Kode ditulis dari nol, unik, dan lolos cek standar industri.' },
            { t: 'Edukasi Logika', d: 'Penjelasan alur program agar Anda percaya diri saat demo.' }
          ]" :key="index" class="reveal-rule py-8 first:pt-0 last:pb-0 group">
            <div class="flex flex-col sm:flex-row sm:items-baseline justify-between gap-4 text-center sm:text-left">
              <h5 class="text-[10px] font-bold text-[#1A1A1A] uppercase tracking-widest group-hover:text-[#8B5CF6] transition-colors italic">
                // {{ rule.t }}
              </h5>
              <p class="text-[11px] text-zinc-500 leading-relaxed font-light max-w-sm">
                {{ rule.d }}
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Simplified CTA -->
      <!-- <div class="reveal-rule mt-24 flex justify-center md:justify-start">
        <a href="https://wa.me/6283849521229" target="_blank" class="group flex items-center gap-6">
          <div class="w-10 h-10 rounded-full border border-zinc-100 flex items-center justify-center group-hover:border-[#8B5CF6] transition-all duration-500">
            <svg class="w-3.5 h-3.5 text-zinc-400 group-hover:text-[#8B5CF6] transition-colors" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </div>
          <div class="flex flex-col items-start text-left">
            <span class="text-[8px] font-bold uppercase tracking-[0.3em] text-zinc-300 group-hover:text-[#8B5CF6] transition-colors italic">Konsultasi Gratis</span>
            <span class="text-[10px] font-bold text-[#1A1A1A] uppercase tracking-widest border-b border-zinc-100 group-hover:border-[#8B5CF6] transition-all">Amankan Nilaimu Sekarang</span>
          </div>
        </a>
      </div> -->
    </div>
  </section>
</template>
