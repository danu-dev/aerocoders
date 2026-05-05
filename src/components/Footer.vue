<script setup>
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="bg-black text-white pt-24 pb-8 px-6 font-poppins selection:bg-[#8B5CF6] selection:text-white overflow-hidden">
    <div class="max-w-6xl mx-auto">
      <div class="grid md:grid-cols-2 gap-12 mb-20">

        <!-- Joki Narrative & Branding -->
        <div class="border-l border-zinc-800 pl-6">
          <h3 class="text-lg font-bold tracking-tighter mb-4 flex items-center gap-2">
            AEROCODE<span class="text-[#8B5CF6]">.</span>
          </h3>
          <p class="max-w-xs text-[11px] text-zinc-500 font-normal leading-relaxed mb-6">
            Penyedia solusi digital dengan standar industri untuk kebutuhan akademik. Fokus pada pengerjaan tugas coding yang presisi, kode bersih, dan jaminan kualitas untuk mahasiswa/siswa.
          </p>
          <div class="flex items-center gap-3">
             <span class="text-[9px] font-bold text-zinc-700 uppercase tracking-widest px-2 py-1 border border-zinc-800 rounded">Industrial Standards</span>
             <span class="text-[9px] font-bold text-zinc-700 uppercase tracking-widest px-2 py-1 border border-zinc-800 rounded">Academic Support</span>
          </div>
        </div>

        <!-- Sitemap & Social: Small Text -->
        <div class="grid grid-cols-2 gap-8 md:justify-end">
          <div class="flex flex-col gap-3">
            <h4 class="text-[9px] font-bold uppercase tracking-[0.3em] text-zinc-600 mb-2">Explore</h4>
            <a href="#services" class="text-[11px] font-normal text-zinc-400 hover:text-[#8B5CF6] transition-colors">Layanan Joki</a>
            <a href="#portfolio" class="text-[11px] font-normal text-zinc-400 hover:text-[#8B5CF6] transition-colors">Katalog Tugas</a>
            <a href="#about" class="text-[11px] font-normal text-zinc-400 hover:text-[#8B5CF6] transition-colors">Tentang Saya</a>
          </div>
          <div class="flex flex-col gap-3">
            <h4 class="text-[9px] font-bold uppercase tracking-[0.3em] text-zinc-600 mb-2">Connect</h4>
            <a href="https://github.com/DanzSukaRgb" target="_blank" rel="noopener noreferrer" class="text-[11px] font-normal text-zinc-400 hover:text-[#8B5CF6] transition-colors">GitHub</a>
            <a href="mailto:halo@danu.dev" class="text-[11px] font-normal text-zinc-400 hover:text-[#8B5CF6] transition-colors">Email</a>
            <a href="https://wa.me/6281234567890" class="text-[11px] font-normal text-zinc-400 hover:text-[#8B5CF6] transition-colors">WhatsApp</a>
          </div>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div class="border-t border-zinc-900 pt-10">
        <!-- Minimalist Impact Text -->
        <div class="relative group cursor-default mb-10 overflow-hidden">
          <h2 class="text-[10vw] font-bold tracking-tighter text-zinc-900 leading-none select-none transition-all duration-700 group-hover:text-white/5">
            A+ PROJECTS READY
          </h2>
        </div>

        <div class="flex flex-col md:flex-row justify-between items-center gap-6">
          <!-- Small Info Bar -->
          <div class="flex items-center gap-4 text-[9px] text-zinc-600 font-bold uppercase tracking-[0.4em]">
            <span>&copy; {{ currentYear }} AEROCODE</span>
            <span class="w-1 h-1 bg-zinc-800 rounded-full"></span>
            <span>Finalis Nasional JHIC 2025</span>
          </div>

          <!-- Industrial Badge -->
          <div class="text-[9px] text-zinc-700 font-medium">
            REKAYASA PERANGKAT LUNAK DENGAN PRESISI TINGGI.
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
