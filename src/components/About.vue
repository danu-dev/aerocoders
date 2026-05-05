<template>
  <section id="tentang" class="relative py-24 md:py-40 px-6 bg-white font-poppins overflow-hidden border-t border-zinc-100 selection:bg-[#8B5CF6] selection:text-white">

    <!-- BACKGROUND: Blueprint Grid Lines (Lebih teknis dari dot) -->
    <div class="absolute inset-0 opacity-[0.03] pointer-events-none"
         style="background-image: linear-gradient(#1A1A1A 1px, transparent 1px), linear-gradient(90deg, #1A1A1A 1px, transparent 1px); background-size: 60px 60px;">
    </div>

    <!-- Wrapper Utama Animasi Scrub -->
    <div class="about-main-wrapper max-w-6xl mx-auto relative z-10">

      <!-- GRID LAYOUT: Asimetris -->
      <div class="grid lg:grid-cols-12 gap-12 lg:gap-0 items-start">

        <!-- SISI KIRI: Pesan Utama (40%) -->
        <div class="lg:col-span-5 pr-0 lg:pr-20">
          <div class="flex items-center gap-4 mb-8">
            <span class="text-[10px] font-bold uppercase tracking-[0.5em] text-[#8B5CF6]">Filosofi Kerja</span>
            <div class="h-px w-12 bg-zinc-200"></div>
          </div>

          <h3 class="text-4xl md:text-6xl font-bold tracking-tighter text-[#1A1A1A] leading-[1] mb-10 uppercase">
            REKAYASA<br />KODE <span class="text-zinc-200 italic">MURNI.</span>
          </h3>

          <p class="text-[13px] text-zinc-500 font-light leading-relaxed max-w-sm mb-12 uppercase tracking-wide">
            Kami tidak hanya mengerjakan tugas, kami membangun pondasi digital yang bersih dan siap dipresentasikan dengan bangga.
          </p>

          <div class="pt-8 border-t border-zinc-100 flex gap-12">
            <div v-for="stat in [{l:'Uptime', v:'24/7'}, {l:'Standard', v:'Industrial'}]" :key="stat.l">
               <p class="text-[8px] font-bold text-zinc-300 uppercase tracking-widest mb-1">{{ stat.l }}</p>
               <p class="text-xs font-mono font-bold text-[#1A1A1A]">{{ stat.v }}</p>
            </div>
          </div>
        </div>

        <!-- SISI KANAN: Poin Teknis (60% / Berbingkai Garis) -->
        <div class="lg:col-span-7 relative">
          <div class="absolute top-0 left-0 w-full h-px bg-zinc-100 origin-left"></div>
          <div class="absolute bottom-0 left-0 w-full h-px bg-zinc-100 origin-left"></div>

          <div class="grid md:grid-cols-2 divide-y md:divide-y-0 md:divide-x divide-zinc-100">
            <!-- Poin 01 -->
            <div class="p-8 md:p-12 group hover:bg-zinc-50/50">
              <span class="text-[10px] font-mono text-zinc-200 group-hover:text-[#8B5CF6] mb-6 block">/ 0x01</span>
              <h4 class="text-sm font-bold text-[#1A1A1A] uppercase tracking-widest mb-6">Clean Architecture</h4>
              <p class="text-[11px] text-zinc-400 leading-relaxed font-light">
                Struktur folder dan penamaan variabel yang logis. Memudahkan Anda memahami isi program saat demo di depan dosen.
              </p>
            </div>

            <!-- Poin 02 -->
            <div class="p-8 md:p-12 group hover:bg-zinc-50/50">
              <span class="text-[10px] font-mono text-zinc-200 group-hover:text-[#8B5CF6] mb-6 block">/ 0x02</span>
              <h4 class="text-sm font-bold text-[#1A1A1A] uppercase tracking-widest mb-6">Ethical Coding</h4>
              <p class="text-[11px] text-zinc-400 leading-relaxed font-light">
                Jaminan orisinalitas tinggi. Kami menjaga privasi identitas Anda seerat mungkin sebagai prioritas utama layanan.
              </p>
            </div>
          </div>
        </div>

      </div>

      <!-- Footer Seksi: Technical Metadata -->
      <div class="mt-24 flex flex-col md:flex-row justify-between items-start md:items-center gap-6 opacity-30">
        <div class="flex items-center gap-4">
          <span class="text-[8px] font-mono font-bold uppercase tracking-[0.5em] text-zinc-400">Core_Solutions_v2.0.6</span>
          <div class="w-1 h-1 bg-zinc-300 rounded-full"></div>
          <span class="text-[8px] font-mono font-bold uppercase tracking-[0.5em] text-zinc-400">Jakarta, IDN</span>
        </div>
        <span class="text-[8px] font-bold uppercase tracking-[0.6em] text-zinc-400">© 2026 Aerocode Digital Engineering</span>
      </div>

    </div>
  </section>
</template>
