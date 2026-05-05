<script setup>
import { ref } from 'vue'
import gsap from 'gsap'

const isMobileMenuOpen = ref(false)

const toggleMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value

  if (isMobileMenuOpen.value) {
    document.body.style.overflow = 'hidden'
    // Animasi Masuk
    gsap.to('.menu-backdrop', { opacity: 1, display: 'block', duration: 0.4 })
    gsap.to('.side-drawer', { x: 0, duration: 0.6, ease: 'expo.out' })
    gsap.fromTo('.nav-link-mobile',
      { x: 20, opacity: 0 },
      { x: 0, opacity: 1, duration: 0.5, stagger: 0.1, delay: 0.2 }
    )
  } else {
    document.body.style.overflow = 'auto'
    // Animasi Keluar
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
      isMobileMenuOpen ? 'bg-white border-slate-100' : 'bg-white/80 backdrop-blur-xl border-slate-50'
    ]"
  >
    <div class="max-w-7xl mx-auto px-8 h-full flex items-center justify-between">
      <!-- Logo: Fokus pada Brand Jasa -->
      <a href="#" class="text-lg font-bold tracking-tighter text-[#1A1A1A] uppercase">
        Aerocode<span class="text-[#8B5CF6]">.</span>
      </a>

      <!-- Desktop Navigation: Bahasa Indonesia -->
      <div class="hidden lg:flex items-center gap-10">
        <div class="flex gap-8 text-[11px] font-medium uppercase tracking-[0.15em] text-slate-400">
          <a href="#home" class="hover:text-black transition-colors font-semibold">Beranda</a>
          <a href="#about" class="hover:text-black transition-colors font-semibold">Tentang</a>
          <a href="#services" class="hover:text-black transition-colors font-semibold">Layanan</a>
          <a href="#portfolio" class="hover:text-black transition-colors font-semibold">Portofolio</a>
        </div>
        <!-- CTA: Fokus Konversi Pelanggan -->
        <a href="https://wa.me/6281234567890" target="_blank" class="px-6 py-2.5 bg-[#1A1A1A] text-white text-[10px] font-bold uppercase tracking-[0.1em] rounded-full hover:bg-[#8B5CF6] transition-all">
          Pesan Sekarang
        </a>
      </div>

      <!-- Mobile Trigger Button -->
      <button
        type="button"
        @click="toggleMenu"
        class="lg:hidden w-10 h-10 flex items-center justify-end focus:outline-none z-[130]"
      >
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 text-black">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5M12 17.25h8.25" />
        </svg>
      </button>
    </div>
  </nav>

  <!-- Mobile Overlay -->
  <div class="menu-backdrop fixed inset-0 bg-slate-900/10 backdrop-blur-md z-[110] hidden opacity-0" @click="toggleMenu"></div>

  <!-- Side Drawer -->
  <div class="side-drawer fixed top-0 right-0 h-dvh w-[300px] bg-white z-[120] border-l border-slate-100 translate-x-full shadow-2xl flex flex-col p-10">

    <!-- Tombol Tutup -->
    <div class="flex justify-between items-center mb-20">
      <span class="text-[9px] font-bold uppercase tracking-[0.3em] text-zinc-300">Navigasi Menu</span>
      <button @click="toggleMenu" class="group flex items-center gap-2 focus:outline-none">
        <div class="w-8 h-8 rounded-full bg-zinc-50 flex items-center justify-center group-hover:bg-zinc-100 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4 text-black">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
          </svg>
        </div>
      </button>
    </div>

    <!-- Links Mobile: Bahasa Indonesia -->
    <div class="flex flex-col gap-6 text-right">
      <a href="#home" @click="toggleMenu" class="nav-link-mobile text-[13px] font-medium uppercase tracking-[0.2em] text-slate-400 hover:text-black transition-colors">Beranda</a>
      <a href="#about" @click="toggleMenu" class="nav-link-mobile text-[13px] font-medium uppercase tracking-[0.2em] text-slate-400 hover:text-black transition-colors">Tentang Jasa</a>
      <a href="#services" @click="toggleMenu" class="nav-link-mobile text-[13px] font-medium uppercase tracking-[0.2em] text-slate-400 hover:text-black transition-colors">Layanan Joki</a>
      <a href="#portfolio" @click="toggleMenu" class="nav-link-mobile text-[13px] font-medium uppercase tracking-[0.2em] text-slate-400 hover:text-black transition-colors">Hasil Project</a>
      <a href="https://wa.me/6281234567890" @click="toggleMenu" class="nav-link-mobile text-[13px] font-bold uppercase tracking-[0.2em] text-[#8B5CF6] border-t border-zinc-50 pt-6">Konsultasi Tugas</a>
    </div>

    <!-- Footer Side Drawer: Fokus ke Menarik Customer -->
    <div class="mt-auto pt-10 border-t border-zinc-50">
      <p class="text-[9px] font-bold uppercase tracking-[0.4em] text-zinc-300 mb-2">Solusi Tugas Akademik</p>
      <p class="text-[9px] text-zinc-400 font-medium uppercase tracking-widest leading-relaxed">
        Jaminan Nilai A • Kode Rapi <br> Pengerjaan Cepat & Aman.
      </p>
    </div>
  </div>
</template>
