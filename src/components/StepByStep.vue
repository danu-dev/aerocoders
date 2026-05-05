<template>
  <!-- Seksi Alur Kerja (Workflow) -->
  <section id="alur" class="py-24 md:py-36 px-6 bg-white font-poppins relative overflow-hidden border-t border-zinc-100 selection:bg-[#8B5CF6] selection:text-white">

    <!-- Pattern: Radial Dots (Konsisten dengan Hero) -->
    <div class="absolute inset-0 opacity-[0.015] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 30px 30px;">
    </div>

    <div class="flow-content-wrapper max-w-5xl mx-auto relative z-10 w-full">
      <div class="grid lg:grid-cols-12 gap-16">

        <!-- Header: Full Left Aligned -->
        <div class="lg:col-span-5 flex flex-col items-start text-left lg:sticky lg:top-32 h-fit">
          <div class="flex items-center gap-4 mb-8">
            <span class="text-[10px] font-bold uppercase tracking-[0.5em] text-[#8B5CF6]">Protokol Order</span>
            <div class="w-12 h-px bg-zinc-200"></div>
          </div>
          <h3 class="text-4xl md:text-5xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1] mb-10 uppercase">
            SISTEMATIS.<br />
            <span class="text-zinc-200 italic">TERIMA BERES.</span>
          </h3>
          <p class="text-[12px] text-zinc-400 font-light leading-relaxed max-w-xs uppercase tracking-wider border-l border-zinc-100 pl-6">
            Alur pengerjaan terstruktur untuk memastikan setiap detail teknis terselesaikan sesuai spesifikasi Anda.
          </p>
        </div>

        <!-- Steps List: Technical Style -->
        <div class="lg:col-span-7 space-y-16 relative">
          <div v-for="(step, index) in [
            { n: '01', t: 'Order Brief', d: 'Kirim detail fitur, bahasa pemrograman, dan deadline via WhatsApp.' },
            { n: '02', t: 'Fixing & DP', d: 'Penentuan harga transparan. Pembayaran uang muka untuk mengamankan slot.' },
            { n: '03', t: 'Live Demo', d: 'Review kualitas melalui video demo atau link akses sebelum handover final.' },
            { n: '04', t: 'Handover File', d: 'Pelunasan dan pengiriman source code lengkap beserta dokumentasi.' }
          ]" :key="index" class="group flex flex-col items-start text-left">
            <div class="flex items-center gap-3 mb-4">
              <span class="text-[11px] font-mono text-[#8B5CF6] italic">[ STEP_{{ step.n }} ]</span>
              <div class="h-px w-8 bg-zinc-100 group-hover:w-16 group-hover:bg-[#8B5CF6]"></div>
            </div>
            <h4 class="text-sm font-bold text-[#1A1A1A] mb-4 uppercase tracking-[0.2em]">{{ step.t }}</h4>
            <p class="text-[11px] text-zinc-500 font-light leading-relaxed max-w-sm">{{ step.d }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Seksi Jaminan Kualitas (Guarantee) -->
  <section id="jaminan" class="py-24 md:py-36 px-6 bg-white font-poppins relative overflow-hidden border-t border-zinc-100 selection:bg-[#8B5CF6] selection:text-white">
    <div class="guarantee-content-wrapper max-w-5xl mx-auto relative z-10">
      <div class="grid lg:grid-cols-12 gap-16 items-start">

        <!-- Header -->
        <div class="lg:col-span-5 flex flex-col items-start text-left">
          <div class="flex items-center gap-4 mb-8">
            <span class="text-[10px] font-bold uppercase tracking-[0.5em] text-[#8B5CF6]">Proteksi Data</span>
            <div class="w-12 h-px bg-zinc-200"></div>
          </div>
          <h3 class="text-4xl md:text-5xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1] mb-10 uppercase">
            PRIVASI AMAN.<br />
            <span class="text-zinc-200 italic">HASIL ORIGINAL.</span>
          </h3>
          <p class="text-[12px] text-zinc-400 font-light leading-relaxed max-w-xs border-l border-zinc-100 pl-6 uppercase tracking-wider">
            Prioritas kami adalah keamanan identitas Anda dan orisinalitas setiap baris kode yang kami buat.
          </p>
        </div>

        <!-- Rules List: Boxed Technical Style -->
        <div class="lg:col-span-7 grid grid-cols-1 sm:grid-cols-2 gap-px bg-zinc-100 border border-zinc-100">
          <div v-for="(rule, index) in [
            { t: 'Garansi Revisi', d: 'Dukungan revisi penuh sampai proyek siap dikumpulkan.' },
            { t: 'Anonimitas Total', d: 'Identitas dan detail proyek dijaga kerahasiaannya 100%.' },
            { t: 'Zero Plagiarism', d: 'Kode ditulis dari nol, unik, dan lolos cek standar industri.' },
            { t: 'Edukasi Logika', d: 'Penjelasan alur program agar Anda percaya diri saat demo.' }
          ]" :key="index" class="bg-white p-8 group hover:bg-zinc-50/50">
            <span class="text-[9px] font-mono text-zinc-200 group-hover:text-[#8B5CF6] mb-4 block italic">// RULE_0{{ index + 1 }}</span>
            <h5 class="text-[11px] font-bold text-[#1A1A1A] uppercase tracking-widest mb-4">
              {{ rule.t }}
            </h5>
            <p class="text-[11px] text-zinc-500 leading-relaxed font-light">
              {{ rule.d }}
            </p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>
