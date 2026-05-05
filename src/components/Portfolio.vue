<script setup>
import { onMounted } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Autoplay } from 'swiper/modules';
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';

import 'swiper/css';

gsap.registerPlugin(ScrollTrigger);

const modules = [Navigation, Autoplay];

const waNumber = "6283849521229"
const waMessage = encodeURIComponent("Halo Aerocode, saya mau order pengerjaan tugas website.")

const projects = [
  { id: 1, title: 'KosKita Ecosystem', cat: 'Fullstack', img: './porto/kos.png', tech: 'Laravel + React' },
  { id: 2, title: 'LibroModern Lib', cat: 'Frontend', img: './porto/lib.png', tech: 'React + Supabase' },
  { id: 3, title: 'DompetKu AI', cat: 'AI System', img: './porto/dompet.png', tech: 'Vue + Gemini' },
  { id: 4, title: 'TypeLab Arena', cat: 'Web App', img: './porto/type.png', tech: 'React 19' }
]

onMounted(() => {
  // Reveal Awal
  gsap.fromTo('.reveal-p', { y: 20, autoAlpha: 0 }, {
    y: 0, autoAlpha: 1, stagger: 0.1, duration: 0.8, ease: 'power3.out',
    scrollTrigger: { trigger: '#portfolio', start: 'top 85%' }
  });

  // Google Scrub Effect
  gsap.to('.p-wrapper', {
    scrollTrigger: {
      trigger: '#portfolio',
      start: 'top top',
      end: 'bottom 15%',
      scrub: 1,
    },
    y: -40,
    scale: 0.97,
    autoAlpha: 0,
    ease: 'none'
  });
})
</script>

<template>
  <section id="portfolio" class="py-20 md:py-32 px-6 bg-white font-poppins relative overflow-hidden border-t border-zinc-50 selection:bg-[#8B5CF6] selection:text-white">

    <!-- Pattern: Super Minimalist Dot -->
    <div class="absolute inset-0 opacity-[0.015] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 30px 30px;">
    </div>

    <div class="p-wrapper max-w-5xl mx-auto relative z-10 w-full">

      <!-- Header: Simple & Sharp -->
      <div class="flex flex-col items-start text-left mb-16 md:mb-24">
        <div class="reveal-p flex items-center gap-3 mb-6">
          <div class="w-8 h-[1px] bg-[#8B5CF6]"></div>
          <span class="text-[9px] font-bold uppercase tracking-[0.4em] text-[#8B5CF6]">Selected Works</span>
        </div>

        <h3 class="reveal-p text-3xl md:text-5xl font-bold tracking-tighter text-[#1A1A1A] leading-tight uppercase">
          Katalog Project.<br />
          <span class="text-zinc-300 italic font-medium">Standar Industri.</span>
        </h3>
      </div>

      <!-- Slider Area -->
      <div class="reveal-p">
        <swiper
          :modules="modules"
          :slides-per-view="1"
          :space-between="20"
          :loop="true"
          :autoplay="{ delay: 4000 }"
          :navigation="{ prevEl: '.prev-p', nextEl: '.next-p' }"
          :breakpoints="{ '768': { slidesPerView: 2, spaceBetween: 30 } }"
          class="pb-10"
        >
          <swiper-slide v-for="p in projects" :key="p.id">
            <div class="group relative flex flex-col border border-zinc-100 rounded-sm bg-white overflow-hidden transition-all duration-500 hover:border-[#8B5CF6]/40 hover:shadow-xl hover:shadow-zinc-200/50">

              <!-- Visual -->
              <div class="aspect-video bg-zinc-50 overflow-hidden">
                <img :src="p.img" :alt="p.title" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105" />
              </div>

              <!-- Content -->
              <div class="p-6 md:p-8">
                <div class="flex justify-between items-start mb-4">
                  <span class="text-[9px] font-mono text-zinc-300 uppercase tracking-widest">{{ p.cat }}</span>
                  <span class="text-[8px] font-bold text-[#8B5CF6] uppercase tracking-widest border border-[#8B5CF6]/20 px-2 py-0.5 rounded-full">Active</span>
                </div>

                <h4 class="text-base md:text-lg font-bold text-[#1A1A1A] mb-2 group-hover:text-[#8B5CF6] transition-colors uppercase tracking-tight">
                  {{ p.title }}
                </h4>
                <p class="text-[10px] md:text-[11px] text-zinc-400 font-light mb-6 uppercase tracking-wider">
                  Tech: {{ p.tech }}
                </p>

                <!-- Micro Link -->
                <div class="flex items-center gap-2 text-[9px] font-bold uppercase tracking-widest text-zinc-300 group-hover:text-[#1A1A1A] transition-all">
                  <span>View Details</span>
                  <div class="w-4 h-[1px] bg-zinc-200 group-hover:w-8 group-hover:bg-[#8B5CF6] transition-all"></div>
                </div>
              </div>
            </div>
          </swiper-slide>
        </swiper>

        <!-- Minimalist Nav -->
        <div class="flex gap-4 mt-8 md:mt-12">
          <button class="prev-p w-10 h-10 rounded-full border border-zinc-100 flex items-center justify-center hover:bg-[#1A1A1A] hover:text-white transition-all group">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M15 19l-7-7 7-7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </button>
          <button class="next-p w-10 h-10 rounded-full border border-zinc-100 flex items-center justify-center hover:bg-[#1A1A1A] hover:text-white transition-all group">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M9 5l7 7-7 7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </button>
        </div>
      </div>

      <!-- Footer CTA -->
      <div class="reveal-p mt-20 pt-10 border-t border-zinc-50 flex flex-col md:flex-row justify-between items-start md:items-end gap-10">
        <a :href="`https://wa.me/${waNumber}?text=${waMessage}`"
           target="_blank"
           class="group flex items-center gap-6">
          <div class="w-12 h-12 rounded-full border border-zinc-200 flex items-center justify-center group-hover:bg-[#8B5CF6] group-hover:border-[#8B5CF6] transition-all duration-500">
            <svg class="w-4 h-4 text-zinc-400 group-hover:text-white transition-colors" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </div>
          <div class="flex flex-col items-start">
            <span class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-300 italic group-hover:text-[#8B5CF6]">Direct Access</span>
            <span class="text-[11px] font-bold text-[#1A1A1A] uppercase tracking-widest border-b border-zinc-100 group-hover:border-[#8B5CF6]">Order via WhatsApp</span>
          </div>
        </a>

        <div class="text-[8px] font-mono text-zinc-300 tracking-[0.5em] uppercase">
          Aerocode Systems // © 2026
        </div>
      </div>

    </div>
  </section>
</template>
