<template>
  <section id="services" class="py-32 bg-white px-6 font-poppins relative overflow-hidden">
    <div class="max-w-7xl mx-auto relative z-10">

      <!-- Header Section -->
      <div class="mb-20 text-left md:text-center">
        <h2 class="text-[10px] font-bold uppercase tracking-[0.5em] text-[#8B5CF6] mb-4">Layanan & Solusi</h2>
        <h3 class="text-4xl md:text-5xl font-bold tracking-tighter text-[#1A1A1A]">
          Kualitas Industri <br class="hidden md:block" /> Untuk Tugas Akademik.
        </h3>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <!-- Service 01: Frontend -->
        <div class="group p-10 border border-zinc-100 rounded-2xl hover:border-[#8B5CF6]/20 hover:shadow-2xl hover:shadow-purple-500/5 transition-all duration-500 bg-white">
          <div class="w-12 h-12 bg-purple-50 rounded-xl flex items-center justify-center mb-8 group-hover:bg-[#8B5CF6] transition-colors duration-500">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[#8B5CF6] group-hover:text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
          </div>
          <span class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-2 block">01 / Frontend</span>
          <h4 class="text-xl font-bold text-[#1A1A1A] mb-4 tracking-tight">UI & Client-Side</h4>
          <p class="text-sm text-zinc-500 font-light leading-relaxed">Konversi Figma ke React 19 atau Vue 3 dengan presisi pixel. Responsif, interaktif, dan siap dipresentasikan.</p>
        </div>

        <!-- Service 02: Fullstack -->
        <div class="group p-10 border border-zinc-100 rounded-2xl hover:border-[#8B5CF6]/20 hover:shadow-2xl hover:shadow-purple-500/5 transition-all duration-500 bg-white">
          <div class="w-12 h-12 bg-purple-50 rounded-xl flex items-center justify-center mb-8 group-hover:bg-[#8B5CF6] transition-colors duration-500">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[#8B5CF6] group-hover:text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4" />
            </svg>
          </div>
          <span class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-2 block">02 / Fullstack</span>
          <h4 class="text-xl font-bold text-[#1A1A1A] mb-4 tracking-tight">Sistem Informasi</h4>
          <p class="text-sm text-zinc-500 font-light leading-relaxed">Integrasi backend Laravel 11 atau Supabase untuk sistem manajemen kompleks seperti manajemen kos atau perpustakaan.</p>
        </div>

        <!-- Service 03: Mobile -->
        <div class="group p-10 border border-zinc-100 rounded-2xl hover:border-[#8B5CF6]/20 hover:shadow-2xl hover:shadow-purple-500/5 transition-all duration-500 bg-white">
          <div class="w-12 h-12 bg-purple-50 rounded-xl flex items-center justify-center mb-8 group-hover:bg-[#8B5CF6] transition-colors duration-500">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[#8B5CF6] group-hover:text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
            </svg>
          </div>
          <span class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-2 block">03 / Mobile</span>
          <h4 class="text-xl font-bold text-[#1A1A1A] mb-4 tracking-tight">Multi-platform App</h4>
          <p class="text-sm text-zinc-500 font-light leading-relaxed">Aplikasi mobile lintas platform berbasis Flutter dengan UI modern. Solusi tepat untuk tugas akhir yang membutuhkan integrasi mobile.</p>
        </div>
      </div>
    </div>
  </section>
</template>
