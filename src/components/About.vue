<template>
  <section id="about" class="py-20 px-6 bg-white border-t border-zinc-50 font-poppins relative">
    <div class="max-w-5xl mx-auto relative z-10">

      <!-- Header: Samakan dengan gaya Services -->
      <div class="mb-16 text-left">
        <div class="flex items-center gap-2 mb-4">
          <span class="w-1.5 h-1.5 rounded-full bg-[#8B5CF6]"></span>
          <h2 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Kenapa Harus Kami?</h2>
        </div>
        <h3 class="text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-tight">
          Pengerjaan Rapih, <span class="text-[#8B5CF6]">Hasil Pasti A.</span>
        </h3>
        <p class="mt-4 text-[12px] text-zinc-400 font-light max-w-sm">
          Kami bantu mahasiswa dan siswa menyelesaikan tugas coding dengan standar industri. Kode bersih, aman, dan siap dikumpulkan.
        </p>
      </div>

      <!-- Feature Grid: Simpel & Airy -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-x-16 gap-y-12">

        <!-- Poin 01 -->
        <div class="group flex flex-col items-start">
          <h4 class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-3">01 / Kualitas Kode</h4>
          <h5 class="text-sm font-bold text-[#1A1A1A] mb-3 uppercase tracking-wider">Clean Code Standar Industri</h5>
          <p class="text-[11px] text-zinc-500 leading-relaxed font-light">
            Bukan sekedar asal jalan. Kami menggunakan struktur kode yang rapi agar kamu bisa menjelaskan alur program dengan lancar saat presentasi di depan dosen.
          </p>
        </div>

        <!-- Poin 02 -->
        <div class="group flex flex-col items-start">
          <h4 class="text-[10px] font-bold text-zinc-300 uppercase tracking-widest mb-3">02 / Keamanan</h4>
          <h5 class="text-sm font-bold text-[#1A1A1A] mb-3 uppercase tracking-wider">Bebas Plagiasi & Privasi</h5>
          <p class="text-[11px] text-zinc-500 leading-relaxed font-light">
            Setiap proyek dikerjakan secara eksklusif dan dari nol. Kami menjamin rahasia klien tetap aman dan hasil pekerjaan terhindar dari plagiarisme.
          </p>
        </div>

      </div>

      <!-- Minimalist CTA Link: Samakan dengan gaya Services -->
      <div class="mt-20 flex justify-start items-center border-t border-zinc-50 pt-10">
        <a href="https://wa.me/6281234567890" target="_blank" class="group flex items-center gap-4 transition-all">
          <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-[#1A1A1A] group-hover:text-[#8B5CF6]">Siap Amankan Nilaimu Sekarang</span>
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
