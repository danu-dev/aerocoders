<template>
  <section id="layanan" class="py-24 md:py-40 px-6 bg-white font-poppins relative overflow-hidden border-t border-zinc-100 selection:bg-[#8B5CF6] selection:text-white">

    <!-- Pattern: Radial Dots (Konsisten dengan Hero) -->
    <div class="absolute inset-0 opacity-[0.015] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 30px 30px;">
    </div>

    <div class="service-wrapper max-w-5xl mx-auto relative z-10 w-full">

      <!-- Header Section: Full Left Aligned -->
      <div class="flex flex-col items-start text-left mb-24 md:mb-32">
        <!-- Badge (Konsisten dengan Hero) -->
        <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full border border-purple-100 bg-purple-50/50 mb-8">
          <span class="relative flex h-1.5 w-1.5">
            <span class="relative inline-flex rounded-full h-1.5 w-1.5 bg-[#8B5CF6]"></span>
          </span>
          <span class="text-[9px] font-bold uppercase tracking-[0.3em] text-[#8B5CF6]">Katalog Layanan & Order</span>
        </div>

        <h3 class="text-4xl md:text-6xl font-bold tracking-tighter text-[#1A1A1A] leading-[1] mb-10 uppercase">
          EKSEKUSI DIGITAL.<br />
          <span class="text-zinc-200 italic">HASIL PRESISI.</span>
        </h3>

        <!-- Technical Metadata Box -->
        <div class="flex flex-col md:flex-row gap-8 items-start md:items-center border-l border-zinc-100 pl-8">
            <p class="max-w-xs text-[11px] md:text-[12px] text-zinc-400 font-light leading-relaxed uppercase tracking-widest">
              Layanan pengembangan perangkat lunak khusus akademik dengan jaminan kode bersih dan orisinalitas 100%.
            </p>
            <div class="hidden md:block h-12 w-px bg-zinc-100"></div>
            <div class="text-[9px] font-mono text-zinc-300 space-y-1 uppercase tracking-tighter">
                <p>Status: Operational</p>
                <p>Standard: Industrial_Grade</p>
                <p>Security: No_Plagiarism</p>
            </div>
        </div>
      </div>

      <!-- Services Grid: Technical Blueprint Style -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-0 relative border-t border-l border-zinc-100">
        <div v-for="(s, i) in [
          { n: '01', t: 'Frontend Architecture', d: 'Slicing UI presisi tinggi menggunakan React atau Vue. Responsif dan siap dipresentasikan.' },
          { n: '02', t: 'System Integration', d: 'Manajemen basis data dan sistem CRUD terintegrasi Laravel atau Supabase untuk project UAS.' },
          { n: '03', t: 'Mobile Engineering', d: 'Pembuatan aplikasi mobile lintas platform dengan Flutter. Fitur lengkap dan kode original.' }
        ]" :key="i" class="group relative flex flex-col items-start text-left p-10 border-r border-b border-zinc-100 hover:bg-zinc-50/30">

          <!-- Corner Bracket on Hover -->
          <div class="absolute top-0 right-0 w-3 h-3 border-t border-r border-[#8B5CF6] opacity-0 group-hover:opacity-100"></div>

          <span class="text-[10px] font-mono text-zinc-200 group-hover:text-[#8B5CF6] mb-8 block uppercase tracking-widest">
            [ ID: 0x0{{ i + 1 }} ]
          </span>
          <h4 class="text-sm font-bold text-[#1A1A1A] uppercase tracking-widest mb-6">
            {{ s.t }}
          </h4>
          <p class="text-[11px] text-zinc-400 leading-relaxed font-light">
            {{ s.d }}
          </p>
        </div>
      </div>

    </div>
  </section>
</template>
