<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Portfolio from './components/Portfolio.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="min-h-screen selection:bg-black selection:text-white">
    <Navbar />
    <main>
      <Hero />
      <About />
      <Services />
      <Portfolio />
      <Contact />
    </main>
    <Footer />
  </div>
</template>
