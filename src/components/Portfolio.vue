<script setup>
const projects = [
  {
    id: 1,
    title: 'KosKita',
    category: 'Tugas Akhir / Skripsi',
    tech: ['Laravel 11', 'React 19', 'Tailwind'],
    status: 'Demo Ready',
    description: 'Sistem manajemen kos dengan fitur multi-role dan laporan otomatis.'
  },
  {
    id: 2,
    title: 'LibroModern',
    category: 'Project UAS',
    tech: ['React', 'Google Sheets'],
    status: 'Siap Kumpul',
    description: 'Perpustakaan digital minimalis dengan integrasi database praktis.'
  },
  {
    id: 3,
    title: 'DompetKu AI',
    category: 'Tugas Mata Kuliah',
    tech: ['Vue', 'AI Integration'],
    status: 'Ready to Use',
    description: 'Aplikasi finansial pintar dengan saran otomatis berbasis AI.'
  },
  {
    id: 4,
    title: 'TypeLab Arena',
    category: 'Tugas Pemrograman Web',
    tech: ['React 19', 'Vite'],
    status: 'Full Source Code',
    description: 'Platform latihan typing real-time untuk kebutuhan presentasi kampus.'
  }
]
</script>

<template>
  <section id="portfolio" class="py-20 px-6 bg-white border-t border-zinc-50 font-poppins relative">
    <div class="max-w-5xl mx-auto relative z-10">

      <!-- Header: Samakan dengan gaya Services & About -->
      <div class="mb-16 text-left">
        <div class="flex items-center gap-2 mb-4">
          <span class="w-1.5 h-1.5 rounded-full bg-[#8B5CF6]"></span>
          <h2 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Katalog Hasil Tugas</h2>
        </div>
        <h3 class="text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-tight">
          Project Selesai, <span class="text-[#8B5CF6]">Siap Kamu Miliki.</span>
        </h3>
        <p class="mt-4 text-[12px] text-zinc-400 font-light max-w-sm">
          Lihat berbagai project yang telah kami selesaikan. Kode rapi, standar tinggi, dan jaminan nilai memuaskan.
        </p>
      </div>

      <!-- Portfolio Grid: Simpel & Bersih -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-x-16 gap-y-12">
        <div
          v-for="project in projects"
          :key="project.id"
          class="group flex flex-col items-start"
        >
          <!-- Project Visual Placeholder: Sangat Subtle -->
          <div class="relative w-full aspect-video bg-zinc-50 rounded-2xl border border-zinc-100 mb-6 overflow-hidden transition-all duration-300 group-hover:border-[#8B5CF6]/30">
            <div class="absolute inset-0 bg-gradient-to-br from-[#8B5CF6]/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"></div>
            <div class="absolute top-4 right-4 px-3 py-1 bg-white/80 backdrop-blur-sm rounded-full border border-zinc-50">
              <span class="text-[8px] font-bold uppercase tracking-widest text-[#8B5CF6]">{{ project.status }}</span>
            </div>
          </div>

          <!-- Project Info -->
          <div class="w-full">
            <span class="text-[9px] font-bold text-zinc-300 uppercase tracking-widest mb-2 block">
              {{ project.category }}
            </span>
            <h4 class="text-lg font-bold text-[#1A1A1A] mb-3 tracking-tight group-hover:text-[#8B5CF6] transition-colors">
              {{ project.title }}
            </h4>
            <p class="text-[11px] text-zinc-500 font-light leading-relaxed mb-4">
              {{ project.description }}
            </p>

            <!-- Tech Badges -->
            <div class="flex flex-wrap gap-2">
              <span
                v-for="t in project.tech"
                :key="t"
                class="text-[9px] font-medium text-zinc-400 bg-zinc-50 px-2 py-0.5 rounded border border-zinc-100/50"
              >
                {{ t }}
              </span>
            </div>
          </div>
        </div>
      </div>

      <!-- Minimalist CTA Link: Samakan dengan gaya Services & About -->
      <div class="mt-20 flex justify-start items-center border-t border-zinc-50 pt-10">
        <a href="https://wa.me/6281234567890" target="_blank" class="group flex items-center gap-4 transition-all">
          <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-[#1A1A1A] group-hover:text-[#8B5CF6]">Tanya Project Lainnya</span>
          <div class="w-8 h-8 rounded-full border border-zinc-100 flex items-center justify-center group-hover:bg-[#8B5CF6] group-hover:border-[#8B5CF6] transition-all">
            <svg class="w-3 h-3 text-black group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </div>
        </a>
      </div>

    </div>
  </section>
</template>
