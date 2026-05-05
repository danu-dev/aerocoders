<template>
  <section id="tentang" class="py-16 sm:py-24 px-5 sm:px-6 bg-white border-t border-zinc-50 font-poppins relative selection:bg-[#8B5CF6] selection:text-white overflow-hidden">
    <div class="absolute inset-0 opacity-[0.03] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 24px 24px;">
    </div>

    <div class="absolute top-0 right-0 w-px h-full bg-gradient-to-b from-transparent via-zinc-100 to-transparent hidden lg:block"></div>

    <div class="max-w-5xl mx-auto relative z-10">
      <div class="flex flex-col md:flex-row md:items-end justify-between mb-16 sm:mb-24 gap-8">
        <div class="max-w-xl relative">
          <div class="absolute -top-4 -left-4 sm:-top-6 sm:-left-6 w-4 h-4 border-t border-l border-zinc-200"></div>

          <div class="flex items-center gap-2 mb-4 sm:mb-6">
            <span class="flex h-1.5 w-1.5 rounded-full bg-[#8B5CF6] animate-pulse"></span>
            <h2 class="text-[8px] sm:text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Filosofi Kerja</h2>
          </div>
          <h3 class="text-2xl sm:text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1]">
            Standar Industri.<br />
            <span class="text-[#8B5CF6]">Pengerjaan Presisi.</span>
          </h3>
        </div>

        <div class="relative">
          <p class="max-w-[200px] sm:max-w-[240px] text-[9px] sm:text-[10px] text-zinc-400 font-bold leading-relaxed uppercase tracking-[0.2em] border-l border-[#8B5CF6]/20 pl-4 sm:pl-6">
            Membantu mahasiswa meraih hasil maksimal dengan kode yang bersih dan terstruktur.
          </p>
        </div>
      </div>

      <div class="grid md:grid-cols-2 gap-10 sm:gap-12 lg:gap-24 items-start relative">
        <div class="group relative transition-all">
          <div class="flex flex-col gap-4 sm:gap-5">
            <div class="flex items-center gap-4">
               <span class="text-[9px] sm:text-[10px] font-bold text-zinc-300 group-hover:text-[#8B5CF6] transition-colors tracking-[0.3em] uppercase italic">01. Quality</span>
               <div class="h-px flex-1 bg-zinc-50"></div>
            </div>
            <h4 class="text-xs sm:text-sm font-bold text-[#1A1A1A] uppercase tracking-wider">Clean Code Standar Industri</h4>
            <p class="text-[10px] sm:text-[11px] text-zinc-500 leading-relaxed font-light max-w-sm">
              Setiap baris kode dikelola dengan standar industri untuk memastikan Anda dapat menjelaskan alur program dengan lancar saat presentasi akademik.
            </p>
          </div>
        </div>

        <div class="group md:mt-24 lg:mt-32 relative transition-all">
          <div class="flex flex-col gap-4 sm:gap-5">
            <div class="flex items-center gap-4">
               <span class="text-[9px] sm:text-[10px] font-bold text-zinc-300 group-hover:text-[#8B5CF6] transition-colors tracking-[0.3em] uppercase italic">02. Ethics</span>
               <div class="h-px flex-1 bg-zinc-50"></div>
            </div>
            <h4 class="text-xs sm:text-sm font-bold text-[#1A1A1A] uppercase tracking-wider">Bebas Plagiasi & Privasi Aman</h4>
            <p class="text-[10px] sm:text-[11px] text-zinc-500 leading-relaxed font-light max-w-sm">
              Proyek dikerjakan secara eksklusif dari nol. Kami menjamin kerahasiaan data pribadi Anda dan memastikan hasil pekerjaan bersih dari unsur plagiarisme.
            </p>
          </div>
          <div class="absolute -right-2 -bottom-8 sm:-right-4 sm:-bottom-10 text-6xl sm:text-8xl md:text-9xl font-bold text-zinc-50/50 pointer-events-none select-none">02</div>
        </div>
      </div>

      <div class="mt-16 sm:mt-20 flex justify-start items-center border-t border-zinc-50 pt-8 sm:pt-10 relative">
        <div class="absolute bottom-0 right-0 w-4 h-4 border-b border-r border-zinc-200"></div>

        <a href="https://wa.me/6281234567890" target="_blank" class="group flex items-center gap-4 transition-all">
          <span class="text-[9px] sm:text-[10px] font-bold uppercase tracking-[0.2em] text-[#1A1A1A] group-hover:text-[#8B5CF6]">Siap Amankan Nilaimu Sekarang</span>
          <div class="w-8 h-8 sm:w-9 sm:h-9 rounded-full border border-zinc-100 flex items-center justify-center group-hover:bg-[#8B5CF6] group-hover:border-[#8B5CF6] transition-all duration-300">
            <svg class="w-3 sm:w-3.5 h-3 sm:h-3.5 text-black group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>
