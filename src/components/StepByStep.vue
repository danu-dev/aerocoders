<template>
  <section id="how-to-order" class="py-24 px-6 bg-white border-t border-zinc-50 font-poppins relative selection:bg-[#8B5CF6] selection:text-white">
    <div class="max-w-5xl mx-auto relative z-10">

      <div class="grid lg:grid-cols-12 gap-16">
        <!-- Header: Sticky Side (Memberikan kesan modern & dinamis) -->
        <div class="lg:col-span-5 lg:sticky lg:top-32 h-fit">
          <div class="flex items-center gap-2 mb-6">
            <span class="w-1.5 h-1.5 rounded-full bg-[#8B5CF6]"></span>
            <h2 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Langkah Pemesanan</h2>
          </div>
          <h3 class="text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-tight mb-6">
            Proses Mudah, <br /><span class="text-[#8B5CF6]">Terima Beres.</span>
          </h3>
          <p class="text-[12px] text-zinc-400 font-light leading-relaxed max-w-xs">
            Kami merancang alur yang praktis agar kamu bisa tetap fokus pada aktivitas lain sementara tugasmu kami selesaikan dengan presisi.
          </p>
        </div>

        <!-- Vertical Progress: Menjelaskan perjalanan pelanggan -->
        <div class="lg:col-span-7 space-y-12">
          <div v-for="(step, index) in [
            { n: '01', t: 'Konsultasi & Briefing', d: 'Hubungi kami via WhatsApp untuk diskusi detail tugas, fitur yang diinginkan, dan deadline pengumpulan.' },
            { n: '02', t: 'Penawaran & Booking', d: 'Dapatkan estimasi biaya transparan. Cukup bayar DP untuk mengamankan slot pengerjaan di jadwal kami.' },
            { n: '03', t: 'Review & Demo Proyek', d: 'Kami berikan video demo atau link akses untuk kamu cek kualitasnya sebelum tugas benar-benar diserahkan.' },
            { n: '04', t: 'Pelunasan & Handover', d: 'Setelah pelunasan, seluruh file source code dan dokumen pendukung langsung dikirimkan ke kontak kamu.' }
          ]" :key="index" class="group relative pl-12 border-l border-zinc-100 pb-4">
            <!-- Indikator Titik Halus -->
            <div class="absolute -left-[5px] top-0 w-[9px] h-[9px] rounded-full bg-zinc-100 group-hover:bg-[#8B5CF6] transition-all duration-500"></div>

            <span class="text-[10px] font-bold text-zinc-300 group-hover:text-[#8B5CF6] transition-colors mb-2 block tracking-widest uppercase italic">Langkah {{ step.n }}</span>
            <h4 class="text-sm font-bold text-[#1A1A1A] mb-3 uppercase tracking-wider">{{ step.t }}</h4>
            <p class="text-[11px] text-zinc-500 font-light leading-relaxed max-w-md">{{ step.d }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>

 <!-- Seksi Jaminan: Ultra-Minimalist & Airy -->
  <section id="terms" class="py-20 px-6 bg-white border-t border-zinc-50 font-poppins relative selection:bg-[#8B5CF6] selection:text-white">
    <div class="max-w-5xl mx-auto relative z-10">

      <div class="grid lg:grid-cols-12 gap-16 items-start">
        <!-- Sisi Kiri: Janji Layanan -->
        <div class="lg:col-span-5">
          <div class="flex items-center gap-2 mb-6">
            <span class="w-1.5 h-1.5 rounded-full bg-[#8B5CF6]"></span>
            <h2 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">Proteksi & Kualitas</h2>
          </div>
          <h3 class="text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1] mb-8">
            Privasi Aman.<br />
            <span class="text-zinc-300 font-medium">Nilai Terjamin.</span>
          </h3>
          <p class="text-[12px] text-zinc-400 font-light leading-relaxed max-w-xs">
            Kami memberikan perlindungan penuh pada setiap aspek pengerjaan digital untuk memastikan kepuasan akademik Anda.
          </p>
        </div>

        <!-- Sisi Rerata: Revisi Teks Jaminan -->
        <div class="lg:col-span-7 divide-y divide-zinc-50">
          <div v-for="(rule, index) in [
            { t: 'Garansi ACC', d: 'Fokus kami adalah kepuasan penguji Anda. Kami berikan dukungan revisi penuh sampai tugas benar-benar siap dikumpulkan.' },
            { t: 'Anonimitas Total', d: 'Kerahasiaan identitas dan detail proyek Anda adalah prioritas mutlak. Data tidak akan pernah kami publikasikan.' },
            { t: 'Zero Plagiarism', d: 'Setiap baris kode ditulis dari nol. Hasil unik, original, dan lolos pengecekan standar industri yang presisi.' },
            { t: 'Edukasi & Demo', d: 'Kami bekali Anda dengan penjelasan logika agar Anda tampil percaya diri dan paham sepenuhnya saat demo di depan dosen.' }
          ]" :key="index" class="py-8 first:pt-0 last:pb-0 group">
            <div class="flex flex-col sm:flex-row sm:items-baseline justify-between gap-4">
              <h5 class="text-[11px] font-bold text-[#1A1A1A] uppercase tracking-widest group-hover:text-[#8B5CF6] transition-colors">
                {{ rule.t }}
              </h5>
              <p class="text-[11px] text-zinc-500 leading-relaxed font-light max-w-sm">
                {{ rule.d }}
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Minimalist CTA Link -->
      <div class="mt-20 flex justify-start items-center border-t border-zinc-50 pt-10">
        <a href="https://wa.me/6281234567890" target="_blank" class="group flex items-center gap-4 transition-all">
          <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-[#1A1A1A] group-hover:text-[#8B5CF6]">Amankan Nilai Anda Sekarang</span>
          <div class="w-8 h-8 rounded-full border border-zinc-100 flex items-center justify-center group-hover:bg-[#8B5CF6] group-hover:border-[#8B5CF6] transition-all duration-300">
            <svg class="w-3 h-3 text-black group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </div>
        </a>
      </div>

    </div>
  </section>
</template>
