<script setup>
import { ref } from 'vue'
import gsap from 'gsap'

const isMobileMenuOpen = ref(false)

const toggleMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value

  if (isMobileMenuOpen.value) {
    document.body.style.overflow = 'hidden'
    gsap.to('.menu-backdrop', { opacity: 1, display: 'block', duration: 0.4 })
    gsap.to('.side-drawer', { x: 0, duration: 0.6, ease: 'expo.out' })
    gsap.fromTo('.nav-link-mobile',
      { x: 20, opacity: 0 },
      { x: 0, opacity: 1, duration: 0.5, stagger: 0.1, delay: 0.2 }
    )
  } else {
    document.body.style.overflow = 'auto'
    gsap.to('.side-drawer', { x: '100%', duration: 0.5, ease: 'expo.in' })
    gsap.to('.menu-backdrop', {
      opacity: 0,
      duration: 0.4,
      onComplete: () => gsap.set('.menu-backdrop', { display: 'none' })
    })
  }
}
</script>

<template>
  <nav
    :class="[
      'fixed top-0 w-full z-[100] h-[72px] border-b font-poppins transition-colors duration-300',
      isMobileMenuOpen ? 'bg-white border-zinc-100' : 'bg-white/80 backdrop-blur-xl border-zinc-50'
    ]"
  >
    <div class="max-w-7xl mx-auto px-8 h-full flex items-center justify-between">
      <a href="#" class="text-lg font-bold tracking-tighter text-[#1A1A1A] uppercase">
        Aerocode<span class="text-[#8B5CF6]">.</span>
      </a>

      <!-- Navigasi Desktop -->
      <div class="hidden lg:flex items-center gap-10">
        <div class="flex gap-8 text-[10px] font-bold uppercase tracking-[0.15em] text-zinc-400">
          <a href="#" class="hover:text-[#8B5CF6] transition-colors">Beranda</a>
          <a href="#tentang" class="hover:text-[#8B5CF6] transition-colors">Tentang</a>
          <a href="#layanan" class="hover:text-[#8B5CF6] transition-colors">Layanan</a>
          <a href="#how-to-order" class="hover:text-[#8B5CF6] transition-colors">Alur</a>
          <a href="#portfolio" class="hover:text-[#8B5CF6] transition-colors">Portofolio</a>
          <a href="#kontak" class="hover:text-[#8B5CF6] transition-colors">Kontak</a>
        </div>
        <a href="https://wa.me/6283849521229" target="_blank" class="px-6 py-2.5 bg-[#1A1A1A] text-white text-[10px] font-bold uppercase tracking-[0.1em] rounded-full hover:bg-[#8B5CF6] transition-all">
          Pesan Sekarang
        </a>
      </div>

      <button @click="toggleMenu" class="lg:hidden w-10 h-10 flex items-center justify-end focus:outline-none z-[130]">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 text-black">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5M12 17.25h8.25" />
        </svg>
      </button>
    </div>
  </nav>

  <div class="menu-backdrop fixed inset-0 bg-zinc-900/10 backdrop-blur-md z-[110] hidden opacity-0" @click="toggleMenu"></div>

  <div class="side-drawer fixed top-0 right-0 h-dvh w-[300px] bg-white z-[120] border-l border-zinc-100 translate-x-full shadow-2xl flex flex-col p-10">
    <div class="flex justify-between items-center mb-16">
      <span class="text-[9px] font-bold uppercase tracking-[0.3em] text-zinc-300">Menu Navigasi</span>
      <button @click="toggleMenu" class="w-8 h-8 rounded-full bg-zinc-50 flex items-center justify-center">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4 text-black">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <div class="flex flex-col gap-6 text-right">
      <a v-for="link in [['Beranda', '#hero'], ['Tentang', '#tentang'], ['Layanan', '#layanan'], ['Alur Kerja', '#alur'], ['Portofolio', '#portofolio'], ['Hubungi Kami', '#kontak']]"
         :key="link[0]" :href="link[1]" @click="toggleMenu"
         class="nav-link-mobile text-[12px] font-bold uppercase tracking-[0.2em] text-zinc-400 hover:text-[#8B5CF6] transition-colors">
        {{ link[0] }}
      </a>
      <a href="https://wa.me/6283849521229" target="_blank" class="nav-link-mobile text-[12px] font-bold uppercase tracking-[0.2em] text-[#8B5CF6] border-t border-zinc-50 pt-6">Konsultasi Tugas</a>
    </div>

    <div class="mt-auto pt-10 border-t border-zinc-50">
      <p class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-300 mb-2">Solusi Akademik Digital</p>
      <p class="text-[9px] text-zinc-400 font-medium uppercase tracking-widest leading-relaxed">
        Jaminan Nilai A • Kode Rapi <br> Pengerjaan Standar Industri.
      </p>
    </div>
  </div>
</template>
