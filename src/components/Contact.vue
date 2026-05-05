<template>
  <!-- Seksi Kontak: Industrial Tech-Minimalism -->
  <section id="kontak" class="py-24 px-6 bg-white border-t border-zinc-50 font-poppins relative overflow-hidden selection:bg-[#8B5CF6] selection:text-white">

    <!-- PATTERN: Micro-Dot Grid -->
    <div class="absolute inset-0 opacity-[0.03] pointer-events-none"
         style="background-image: radial-gradient(#1A1A1A 0.5px, transparent 0.5px); background-size: 24px 24px;">
    </div>

    <div class="max-w-5xl mx-auto relative z-10">

      <!-- Header: Editorial Style -->
      <div class="mb-20 text-left relative">
        <div class="absolute -top-6 -left-6 w-4 h-4 border-t border-l border-zinc-200"></div>

        <div class="flex items-center gap-2 mb-6">
          <span class="flex h-1.5 w-1.5 rounded-full bg-[#8B5CF6]"></span>
          <h2 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-400">
            Solusi Akademik Premium
          </h2>
        </div>
        <h3 class="text-3xl md:text-4xl font-bold tracking-tighter text-[#1A1A1A] leading-[1.1] mb-8">
          Konsultasi Project,<br />
          <span class="text-[#8B5CF6]">Raih Nilai Maksimal.</span>
        </h3>
      </div>

      <!-- Main Layout Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-16 lg:gap-20 items-start">

        <!-- Sisi Kiri: Kontak Langsung -->
        <div class="lg:col-span-5 space-y-12">

          <!-- WhatsApp -->
          <a href="https://wa.me/6283849521229" target="_blank" class="group block">
            <span class="text-[9px] font-bold text-zinc-300 uppercase tracking-[0.3em] mb-4 block group-hover:text-[#8B5CF6] italic">/ Respon Cepat</span>
            <span class="text-2xl md:text-3xl font-bold text-[#1A1A1A] border-b border-zinc-50 pb-2 group-hover:border-[#8B5CF6]">
              +62 838 4952 1229
            </span>
          </a>

          <!-- Email: Penyesuaian untuk email panjang -->
          <a href="mailto:mohammadafdanu@gmail.com" class="group block">
            <span class="text-[9px] font-bold text-zinc-300 uppercase tracking-[0.3em] mb-4 block group-hover:text-[#8B5CF6] italic">/ Email Resmi</span>
            <!-- text-lg pada mobile agar tidak overflow, md:text-2xl/3xl pada desktop -->
            <span class="text-lg sm:text-xl md:text-2xl lg:text-[1.6rem] font-bold text-[#1A1A1A] border-b border-zinc-50 pb-2 group-hover:border-[#8B5CF6] break-all sm:break-normal leading-tight">
              mohammadafdanu@gmail.com
            </span>
          </a>
        </div>

        <!-- Sisi Kanan: Scope of Work -->
        <div class="lg:col-span-7">
          <div class="flex items-center gap-4 mb-10">
            <h4 class="text-[10px] font-bold text-[#1A1A1A] uppercase tracking-[0.4em]">Cakupan Kerja</h4>
            <div class="h-px flex-1 bg-zinc-50"></div>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-x-12 gap-y-8">
            <div v-for="(service, index) in [
              'Pemrograman UAS', 'Proyek Akhir',
              'Slicing React & Vue', 'Sistem Laravel',
              'Aplikasi Mobile', 'Arsitektur Basis Data'
            ]" :key="index" class="group">
              <div class="flex flex-col gap-1.5">
                <span class="text-[10px] font-bold text-zinc-200 group-hover:text-[#8B5CF6] tracking-widest">
                  0{{ index + 1 }} —
                </span>
                <span class="text-[11px] font-bold text-zinc-500 group-hover:text-black uppercase tracking-wider leading-relaxed">
                  {{ service }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Footer Branding -->
      <div class="mt-24 pt-10 border-t border-zinc-50 flex flex-col md:flex-row justify-between items-center gap-6">
        <p class="text-[9px] text-zinc-400 font-bold uppercase tracking-[0.4em]">
          Kode Bersih • Standar Industri • No Plagiarism
        </p>
        <div class="flex gap-8">
          <a href="https://www.instagram.com/dannuu________" class="text-[9px] font-bold text-zinc-300 hover:text-black uppercase tracking-[0.2em]">Instagram</a>
          <a href="https://github.com/danu-dev" target="_blank" class="text-[9px] font-bold text-zinc-300 hover:text-black uppercase tracking-[0.2em]">GitHub</a>
        </div>
      </div>

    </div>
  </section>
</template>
