<template>
  <section id="layanan" class="py-16 sm:py-24 px-5 sm:px-6 bg-white border-t border-zinc-50 font-poppins relative selection:bg-[#8B5CF6] selection:text-white overflow-hidden">
    <div class="absolute inset-0 opacity-[0.03] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 24px 24px;">
    </div>

    <div class="max-w-5xl mx-auto relative z-10">
      <div class="mb-16 sm:mb-24 text-left relative">
        <div class="absolute -top-4 -left-4 sm:-top-6 sm:-left-6 w-4 h-4 border-t border-l border-zinc-200"></div>

        <div class="flex items-center gap-2 mb-4 sm:mb-6">
          <span class="w-1.5 h-1.5 rounded-full bg-[#8B5CF6]"></span>
          <h2 class="text-[8px] sm:text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Solusi Digital</h2>
        </div>
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-tight">
          Tugas Kelar, <span class="text-[#8B5CF6]">Nilai Aman.</span>
        </h3>
        <p class="mt-4 text-[10px] sm:text-[11px] text-zinc-400 font-light max-w-sm border-l border-[#8B5CF6]/20 pl-4 sm:pl-6">
          Serahkan kodinganmu pada ahlinya. Cepat, rapi, dan siap dipresentasikan dengan standar industri.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-10 sm:gap-12 lg:gap-16">
        <div class="group flex flex-col items-start transition-all">
          <div class="text-[#8B5CF6] mb-5 sm:mb-6 group-hover:scale-110 transition-transform duration-300">
            <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" /></svg>
          </div>
          <div class="flex items-center gap-3 mb-3 w-full">
            <h4 class="text-[9px] sm:text-[10px] font-bold text-zinc-300 group-hover:text-[#8B5CF6] transition-colors uppercase tracking-widest">01. Frontend</h4>
            <div class="h-px flex-1 bg-zinc-50"></div>
          </div>
          <h5 class="text-xs sm:text-sm font-bold text-[#1A1A1A] mb-3 uppercase tracking-wider">Slicing UI & Responsif</h5>
          <p class="text-[10px] sm:text-[11px] text-zinc-500 leading-relaxed font-light">Konversi desain ke React atau Vue. Pixel perfect untuk kebutuhan tugas pemrograman web.</p>
        </div>

        <div class="group flex flex-col items-start transition-all">
          <div class="text-[#8B5CF6] mb-5 sm:mb-6 group-hover:scale-110 transition-transform duration-300">
            <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4" /></svg>
          </div>
          <div class="flex items-center gap-3 mb-3 w-full">
            <h4 class="text-[9px] sm:text-[10px] font-bold text-zinc-300 group-hover:text-[#8B5CF6] transition-colors uppercase tracking-widest">02. Fullstack</h4>
            <div class="h-px flex-1 bg-zinc-50"></div>
          </div>
          <h5 class="text-xs sm:text-sm font-bold text-[#1A1A1A] mb-3 uppercase tracking-wider">Sistem CRUD & UAS</h5>
          <p class="text-[10px] sm:text-[11px] text-zinc-500 leading-relaxed font-light">Sistem informasi terintegrasi Laravel atau Supabase. Siap pakai untuk tugas akhir atau UAS.</p>
        </div>

        <div class="group flex flex-col items-start transition-all">
          <div class="text-[#8B5CF6] mb-5 sm:mb-6 group-hover:scale-110 transition-transform duration-300">
            <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" /></svg>
          </div>
          <div class="flex items-center gap-3 mb-3 w-full">
            <h4 class="text-[9px] sm:text-[10px] font-bold text-zinc-300 group-hover:text-[#8B5CF6] transition-colors uppercase tracking-widest">03. Mobile</h4>
            <div class="h-px flex-1 bg-zinc-50"></div>
          </div>
          <h5 class="text-xs sm:text-sm font-bold text-[#1A1A1A] mb-3 uppercase tracking-wider">Aplikasi Flutter</h5>
          <p class="text-[10px] sm:text-[11px] text-zinc-500 leading-relaxed font-light">Pengembangan aplikasi mobile modern untuk tugas kuliah dengan fitur lengkap dan original.</p>
        </div>
      </div>

      <div class="mt-16 sm:mt-20 flex justify-start items-center border-t border-zinc-50 pt-8 sm:pt-10 relative">
        <div class="absolute bottom-0 right-0 w-4 h-4 border-b border-r border-zinc-200"></div>
        <a href="https://wa.me/6281234567890" target="_blank" class="group flex items-center gap-4 transition-all">
          <span class="text-[9px] sm:text-[10px] font-bold uppercase tracking-[0.2em] text-[#1A1A1A] group-hover:text-[#8B5CF6]">Konsultasi Tugas Sekarang</span>
          <div class="w-8 h-8 sm:w-9 sm:h-9 rounded-full border border-zinc-100 flex items-center justify-center group-hover:bg-[#8B5CF6] group-hover:border-[#8B5CF6] transition-all duration-300">
            <svg class="w-3 sm:w-3.5 h-3 sm:h-3.5 text-black group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" /></svg>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>
