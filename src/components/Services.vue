<template>
  <section id="services" class="py-20 bg-white px-6 font-poppins relative">
    <div class="max-w-5xl mx-auto relative z-10">

      <!-- Header: Super Simpel & Menarik -->
      <div class="mb-16 text-left">
        <div class="flex items-center gap-2 mb-4">
          <span class="w-1.5 h-1.5 rounded-full bg-[#8B5CF6]"></span>
          <h2 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Solusi Tugas Kamu</h2>
        </div>
        <h3 class="text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-tight">
          Tugas Kelar, <span class="text-[#8B5CF6]">Nilai Aman.</span>
        </h3>
        <p class="mt-4 text-[12px] text-zinc-400 font-light max-w-sm">
          Serahkan kodinganmu pada ahlinya. Cepat, rapi, dan siap dipresentasikan di depan dosen.
        </p>
      </div>

      <!-- Services List: Lebih Bersih & Elegan -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">

        <!-- Joki Frontend -->
        <div class="group flex flex-col items-start">
          <div class="text-[#8B5CF6] mb-6 group-hover:scale-110 transition-transform duration-300">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" /></svg>
          </div>
          <h4 class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-3">01. Frontend</h4>
          <h5 class="text-sm font-bold text-[#1A1A1A] mb-3">Tugas Slicing & UI</h5>
          <p class="text-[11px] text-zinc-500 leading-relaxed font-light">Konversi desain ke React/Vue. Pixel perfect dan responsif untuk tugas pemrograman web.</p>
        </div>

        <!-- Joki Fullstack -->
        <div class="group flex flex-col items-start">
          <div class="text-[#8B5CF6] mb-6 group-hover:scale-110 transition-transform duration-300">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4" /></svg>
          </div>
          <h4 class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-3">02. Fullstack</h4>
          <h5 class="text-sm font-bold text-[#1A1A1A] mb-3">Sistem CRUD & UAS</h5>
          <p class="text-[11px] text-zinc-500 leading-relaxed font-light">Pengerjaan sistem informasi lengkap berbasis Laravel atau Supabase. Siap pakai untuk tugas UAS/Akhir.</p>
        </div>

        <!-- Joki Mobile -->
        <div class="group flex flex-col items-start">
          <div class="text-[#8B5CF6] mb-6 group-hover:scale-110 transition-transform duration-300">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" /></svg>
          </div>
          <h4 class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-3">03. Mobile</h4>
          <h5 class="text-sm font-bold text-[#1A1A1A] mb-3">App Mobile Flutter</h5>
          <p class="text-[11px] text-zinc-500 leading-relaxed font-light">Bantu pengerjaan aplikasi mobile untuk tugas akhir. Fitur lengkap, desain modern, dan jaminan lulus.</p>
        </div>

      </div>

      <!-- Minimalist CTA Link -->
      <div class="mt-20 flex justify-start items-center border-t border-zinc-50 pt-10">
        <a href="https://wa.me/6281234567890" target="_blank" class="group flex items-center gap-4 transition-all">
          <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-[#1A1A1A] group-hover:text-[#8B5CF6]">Konsultasi Tugas Sekarang</span>
          <div class="w-8 h-8 rounded-full border border-zinc-100 flex items-center justify-center group-hover:bg-[#8B5CF6] group-hover:border-[#8B5CF6] transition-all">
            <svg class="w-3 h-3 text-black group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" /></svg>
          </div>
        </a>
      </div>

    </div>
  </section>
</template>
