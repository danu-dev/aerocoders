<script setup>
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="bg-black text-white pt-32 pb-8 px-6 font-poppins selection:bg-[#8B5CF6] selection:text-white">
    <div class="max-w-7xl mx-auto">
      <div class="grid md:grid-cols-2 gap-16 mb-24">

        <!-- Brand Narrative -->
        <div>
          <h3 class="text-2xl font-bold tracking-tighter mb-6 flex items-center gap-2">
            NEXACODE<span class="text-[#8B5CF6]">.</span>
          </h3>
          <p class="max-w-sm text-zinc-400 font-light leading-relaxed">
            Arsitektur digital dengan standar industri untuk kebutuhan akademik dan bisnis. Berfokus pada presisi rekayasa dan performa tinggi.
          </p>
        </div>

        <!-- Sitemap & Social -->
        <div class="grid grid-cols-2 gap-8 md:justify-end">
          <div class="flex flex-col gap-4">
            <h4 class="text-[10px] font-bold uppercase tracking-[0.3em] text-zinc-500 mb-2">Explore</h4>
            <a href="#services" class="text-sm font-light hover:text-[#8B5CF6] transition-colors">Layanan</a>
            <a href="#portfolio" class="text-sm font-light hover:text-[#8B5CF6] transition-colors">Portofolio</a>
            <a href="#about" class="text-sm font-light hover:text-[#8B5CF6] transition-colors">Tentang Saya</a>
          </div>
          <div class="flex flex-col gap-4">
            <h4 class="text-[10px] font-bold uppercase tracking-[0.3em] text-zinc-500 mb-2">Connect</h4>
            <a href="https://github.com/DanzSukaRgb" target="_blank" rel="noopener noreferrer" class="text-sm font-light hover:text-[#8B5CF6] transition-colors">GitHub</a>
            <a href="mailto:halo@danu.dev" class="text-sm font-light hover:text-[#8B5CF6] transition-colors">Email</a>
            <a href="https://wa.me/6281234567890" class="text-sm font-light hover:text-[#8B5CF6] transition-colors">WhatsApp</a>
          </div>
        </div>
      </div>

      <!-- Mega Text Impact -->
      <div class="border-t border-zinc-900 pt-12 flex flex-col items-center">
        <h2 class="text-[12vw] font-bold tracking-tighter  text-center leading-none text-zinc-900 select-none mb-12 hover:text-white transition-all duration-700 cursor-default">
          CODE THE FUTURE
        </h2>

        <div class="w-full flex flex-col md:flex-row justify-between items-center text-[10px] text-zinc-600 font-bold uppercase tracking-[0.3em] gap-6">
          <div class="flex items-center gap-4">
            <span>&copy; {{ currentYear }} NEXACODE</span>
            <span class="w-1 h-1 bg-zinc-800 rounded-full"></span>
            <span>Finalis JHIC 2025</span>
          </div>
          <div class="text-zinc-500 font-light italic">
            Built with Arch Linux & CachyOS
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
