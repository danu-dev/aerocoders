<script setup>
const currentYear = new Date().getFullYear();
const buildVersion = "v3.1.1";
</script>

<template>
  <footer class="bg-black text-white pt-24 pb-12 px-6 font-poppins selection:bg-[#8B5CF6] selection:text-white relative overflow-hidden">

    <!-- PATTERN: High-Density Micro-Dot Grid -->
    <div class="absolute inset-0 opacity-[0.05] pointer-events-none"
         style="background-image: radial-gradient(#ffffff 0.5px, transparent 0.5px); background-size: 24px 24px;">
    </div>

    <div class="max-w-5xl mx-auto relative z-10">
      <div class="grid md:grid-cols-12 gap-16 mb-24">

        <!-- Branding Section -->
        <div class="md:col-span-6 relative">
          <div class="absolute -top-6 -left-6 w-4 h-4 border-t border-l border-zinc-800"></div>

          <div class="flex items-center gap-3 mb-6">
            <h3 class="text-xl font-bold tracking-tighter">
              AEROCODE<span class="text-[#8B5CF6]">.</span>
            </h3>
            <span class="text-[7px] font-mono text-zinc-700 border border-zinc-800 px-1.5 py-0.5 rounded uppercase tracking-widest">
              {{ buildVersion }}
            </span>
          </div>

          <p class="max-w-sm text-[11px] text-zinc-500 font-light leading-relaxed mb-8">
            Penyedia solusi digital dengan fokus pada rekayasa perangkat lunak standar industri.
            Kami menjamin setiap baris kode bersih, aman, dan siap untuk dipresentasikan.
          </p>
        </div>

        <!-- Sitemap -->
        <div class="md:col-span-3">
          <h4 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-700 mb-6 italic">/ Navigasi</h4>
          <ul class="space-y-3">
            <li v-for="link in [['Layanan', '#layanan'], ['Portofolio', '#portofolio'], ['Tentang', '#tentang'], ['Kontak', '#kontak']]" :key="link[0]">
              <a :href="link[1]" class="text-[10px] text-zinc-500 hover:text-white uppercase tracking-widest block">
                {{ link[0] }}
              </a>
            </li>
          </ul>
        </div>

        <!-- Connection -->
        <div class="md:col-span-3">
          <h4 class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-700 mb-6 italic">/ Hubungi</h4>
          <ul class="space-y-3 text-[10px] font-light text-zinc-500">
            <li><a href="https://github.com/danu-dev" target="_blank" class="hover:text-white block">GitHub</a></li>
            <li><a href="mailto:halo@danu.dev" class="hover:text-white block">mohammadafdanu@gmail.com</a></li>
            <li><a href="https://wa.me/6281234567890" class="hover:text-white block">+62 838 4952 1229</a></li>
          </ul>
        </div>
      </div>

      <!-- Footer Bottom Area -->
      <div class="border-t border-zinc-900 pt-16 relative">
        <div class="absolute bottom-0 right-0 w-4 h-4 border-b border-r border-zinc-800"></div>

        <!-- Impact Text: Skala Lebih Kecil & Center -->
        <div class="mb-16 overflow-hidden pointer-events-none select-none relative">
          <h2 class="text-5xl md:text-7xl font-bold tracking-[0.2em] text-center leading-none uppercase text-stroke opacity-90">
            KODE BERSIH.
          </h2>
        </div>

        <div class="flex flex-col md:flex-row justify-between items-center gap-8">
          <!-- Info Hak Cipta -->
          <div class="flex items-center gap-4 text-[9px] text-zinc-600 font-bold uppercase tracking-[0.4em]">
            <span>&copy; {{ currentYear }} AEROCODE</span>
            <span class="w-1 h-1 bg-zinc-800 rounded-full"></span>
            <span>PRESISI TINGGI</span>
          </div>

          <!-- Tech Stack -->
          <div class="flex gap-6 text-[8px] text-zinc-700 font-bold uppercase tracking-widest">
            <span>Tailwind</span>
            <span>Laravel</span>
            <span>Supabase</span>
            <span>Vercel</span>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.text-stroke {
  color: transparent;
  -webkit-text-stroke: 1px #27272a; /* Zinc-800 */
}
</style>
