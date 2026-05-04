<template>
  <section id="about" class="py-24 md:py-32 px-6 bg-white border-t border-slate-100 rounded-t-[40px] md:rounded-t-[80px] relative overflow-hidden font-poppins">
    <!-- Clean Background Element -->
    <div class="absolute top-0 left-1/2 -translate-x-1/2 w-full h-full opacity-[0.03] pointer-events-none">
      <div class="absolute inset-0" style="background-image: linear-gradient(#8B5CF6 1px, transparent 1px), linear-gradient(90deg, #8B5CF6 1px, transparent 1px); background-size: 40px 40px;"></div>
    </div>

    <div class="max-w-6xl mx-auto relative z-10">
      <div class="flex flex-col lg:flex-row gap-16 lg:gap-24">

        <!-- Left: Branding & Heading -->
        <div class="w-full lg:w-1/3 lg:sticky lg:top-32 h-fit">
          <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-50 border border-slate-100 mb-8">
            <span class="w-2 h-2 rounded-full bg-[#8B5CF6]"></span>
            <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-slate-500">Expert Partner</span>
          </div>

          <h2 class="text-4xl md:text-5xl font-bold tracking-tight text-[#1A1A1A] leading-[1.1] mb-6">
            Digital Solution <span class="text-[#8B5CF6]">Simplified.</span>
          </h2>
          <p class="text-slate-400 font-light text-sm tracking-wide uppercase">Est. 2025 • High Standards</p>
        </div>

        <!-- Right: Content & Cards -->
        <div class="w-full lg:w-2/3">
          <p class="text-xl md:text-2xl font-normal text-[#1A1A1A] leading-relaxed mb-12">
            Kami membantu siswa dan mahasiswa menyelesaikan tantangan digital dengan <span class="text-[#8B5CF6] font-semibold underline underline-offset-8 decoration-slate-200">kode yang bersih</span> dan penyelesaian yang presisi.
          </p>

          <!-- Feature Grid -->
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-12">
            <div class="group p-8 border border-slate-100 bg-slate-50/30 rounded-3xl hover:bg-white hover:border-[#8B5CF6]/30 hover:shadow-xl hover:shadow-purple-500/5 transition-all duration-500">
              <div class="w-10 h-10 bg-white rounded-xl shadow-sm flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                <svg class="w-5 h-5 text-[#8B5CF6]" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" /></svg>
              </div>
              <h4 class="text-lg font-bold text-[#1A1A1A] mb-3">Tugas Sekolah</h4>
              <p class="text-sm text-slate-500 leading-relaxed font-light">Eksplorasi visual dengan Landing Page statis dan layout responsif yang modern.</p>
            </div>

            <div class="group p-8 border border-slate-100 bg-slate-50/30 rounded-3xl hover:bg-white hover:border-[#8B5CF6]/30 hover:shadow-xl hover:shadow-purple-500/5 transition-all duration-500">
              <div class="w-10 h-10 bg-white rounded-xl shadow-sm flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                <svg class="w-5 h-5 text-[#8B5CF6]" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" /></svg>
              </div>
              <h4 class="text-lg font-bold text-[#1A1A1A] mb-3">Tugas Kampus</h4>
              <p class="text-sm text-slate-500 leading-relaxed font-light">Pengembangan sistem CRUD, integrasi database, hingga arsitektur Laravel yang kompleks.</p>
            </div>
          </div>

          <!-- Trust Bar -->
          <div class="flex flex-wrap items-center justify-between gap-8 p-8 border border-slate-100 rounded-[2.5rem] bg-white">
            <div>
              <div class="flex items-center gap-1 mb-1">
                <span class="text-2xl font-bold text-[#1A1A1A]">100+</span>
                <span class="text-[#8B5CF6] font-bold leading-none">↗</span>
              </div>
              <p class="text-[11px] text-slate-400 uppercase tracking-widest font-medium">Proyek Selesai</p>
            </div>
            <div class="h-10 w-px bg-slate-100 hidden md:block"></div>
            <div class="flex-1 min-w-[200px]">
              <p class="text-xs text-slate-500 italic leading-relaxed">
                "Finalis Nasional JHIC 2025 — Komitmen kami adalah kualitas standar industri untuk tugas akademik."
              </p>
            </div>
            <button class="w-full md:w-auto px-8 py-4 bg-[#1A1A1A] text-white text-[11px] font-bold uppercase tracking-widest rounded-2xl hover:bg-[#8B5CF6] transition-all duration-300 shadow-lg shadow-slate-200">
              Mulai Diskusi
            </button>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>
