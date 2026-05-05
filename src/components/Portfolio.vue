<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Autoplay } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';

const modules = [Navigation, Autoplay];

const projects = [
  {
    id: 1,
    title: 'KosKita',
    category: 'Tugas Akhir / Skripsi',
    tech: ['Laravel 11', 'React 19'],
    status: 'Ready to Present',
    description: 'Sistem manajemen kos dengan fitur multi-role dan laporan otomatis. Full source code.'
  },
  {
    id: 2,
    title: 'LibroModern',
    category: 'Project UAS',
    tech: ['React', 'Supabase'],
    status: 'Siap Kumpul',
    description: 'Perpustakaan digital minimalis dengan integrasi database praktis dan responsif.'
  },
  {
    id: 3,
    title: 'DompetKu AI',
    category: 'Tugas Mata Kuliah',
    tech: ['Vue', 'AI Integration'],
    status: 'Anti-Plagiasi',
    description: 'Aplikasi finansial pintar dengan saran otomatis berbasis AI. Kode bersih & unik.'
  },
  {
    id: 4,
    title: 'TypeLab Arena',
    category: 'Tugas Pemrograman Web',
    tech: ['React 19', 'Vite'],
    status: 'High Quality',
    description: 'Platform latihan typing real-time untuk kebutuhan presentasi di depan dosen.'
  }
]
</script>

<template>
  <section id="portfolio" class="py-24 px-6 bg-white border-t border-zinc-50 font-poppins relative overflow-hidden selection:bg-[#8B5CF6] selection:text-white">

    <!-- PATTERN: Micro-Dot Grid -->
    <div class="absolute inset-0 opacity-[0.03] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 24px 24px;">
    </div>

    <div class="max-w-5xl mx-auto relative z-10">

      <!-- Header: Fokus ke Joki Tugas -->
      <div class="mb-16 flex flex-col md:flex-row md:items-end justify-between gap-8 relative">
        <div class="relative">
          <!-- ELEMENT: Corner Bracket -->
          <div class="absolute -top-6 -left-6 w-4 h-4 border-t border-l border-zinc-200"></div>

          <div class="flex items-center gap-2 mb-4">
            <span class="flex h-1.5 w-1.5 rounded-full bg-[#8B5CF6] animate-pulse"></span>
            <h2 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Katalog Hasil Pengerjaan</h2>
          </div>
          <h3 class="text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-tight">
            Tugas Selesai, <br /><span class="text-[#8B5CF6]">Kualitas Standar Industri.</span>
          </h3>
        </div>

        <!-- Custom Navigation -->
        <div class="flex gap-3">
          <button class="swiper-prev-port w-10 h-10 rounded-full border border-zinc-100 flex items-center justify-center hover:bg-[#8B5CF6] hover:border-[#8B5CF6] hover:text-white transition-all duration-300">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M15 19l-7-7 7-7" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </button>
          <button class="swiper-next-port w-10 h-10 rounded-full border border-zinc-100 flex items-center justify-center hover:bg-[#8B5CF6] hover:border-[#8B5CF6] hover:text-white transition-all duration-300">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M9 5l7 7-7 7" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </button>
        </div>
      </div>

      <!-- Slider Area -->
      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="30"
        :loop="true"
        :autoplay="{ delay: 4000, disableOnInteraction: false }"
        :navigation="{ prevEl: '.swiper-prev-port', nextEl: '.swiper-next-port' }"
        :breakpoints="{ '768': { slidesPerView: 2, spaceBetween: 40 } }"
        class="portfolio-swiper"
      >
        <swiper-slide v-for="project in projects" :key="project.id">
          <div class="group flex flex-col items-start transition-all">
            <div class="relative w-full aspect-video bg-zinc-50 rounded-2xl border border-zinc-100 mb-8 overflow-hidden group-hover:border-[#8B5CF6]/30 transition-all duration-500">
              <div class="absolute inset-0 bg-gradient-to-br from-[#8B5CF6]/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"></div>

              <div class="absolute top-2 left-2 w-2 h-2 border-t border-l border-zinc-200 group-hover:border-[#8B5CF6]/40"></div>
              <div class="absolute bottom-2 right-2 w-2 h-2 border-b border-r border-zinc-200 group-hover:border-[#8B5CF6]/40"></div>

              <div class="absolute top-4 right-4 px-3 py-1 bg-white/80 backdrop-blur-sm rounded-full border border-zinc-50 shadow-sm">
                <span class="text-[8px] font-bold uppercase tracking-widest text-[#8B5CF6]">{{ project.status }}</span>
              </div>
            </div>

            <div class="w-full relative">
              <div class="flex items-center gap-4 mb-3">
                 <span class="text-[9px] font-bold text-zinc-300 uppercase tracking-[0.2em]">{{ project.category }}</span>
                 <div class="h-px flex-1 bg-zinc-50 group-hover:bg-[#8B5CF6]/10 transition-colors"></div>
              </div>

              <h4 class="text-lg font-bold text-[#1A1A1A] mb-3 tracking-tight group-hover:text-[#8B5CF6] transition-colors uppercase">
                {{ project.title }}
              </h4>
              <p class="text-[11px] text-zinc-500 font-light leading-relaxed mb-6">
                {{ project.description }}
              </p>

              <div class="flex flex-wrap gap-2">
                <span v-for="t in project.tech" :key="t" class="text-[8px] font-bold text-zinc-400 bg-zinc-50 px-2 py-0.5 rounded border border-zinc-100/50 uppercase tracking-tighter">
                  {{ t }}
                </span>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>

      <!-- CTA -->
      <!-- <div class="mt-24 flex justify-start items-center border-t border-zinc-50 pt-12 relative">
        <div class="absolute bottom-0 right-0 w-4 h-4 border-b border-r border-zinc-200"></div>

        <a href="https://wa.me/6281234567890" target="_blank" class="group flex items-center gap-4 transition-all">
          <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-[#1A1A1A] group-hover:text-[#8B5CF6]">Amankan Nilai A Milikmu Sekarang</span>
          <div class="w-9 h-9 rounded-full border border-zinc-100 flex items-center justify-center group-hover:bg-[#8B5CF6] group-hover:border-[#8B5CF6] transition-all duration-300">
            <svg class="w-3.5 h-3.5 text-black group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </div>
        </a>
      </div> -->

    </div>
  </section>
</template>
