<template>
  <Navbar />
  <HeroSection />
  <FeaturesSection />
  <HowItWorks />
  <Testimoni />
  <Footer />
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import HeroSection from './components/HeroSection.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import HowItWorks from './components/HowItWorks.vue'
import Testimoni from './components/Testimoni.vue'
import Footer from './components/Footer.vue'
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', 'Segoe UI', sans-serif;
}

html {
  scroll-behavior: smooth;
}

body {
  background: linear-gradient(135deg, #f0fbf7 0%, #e0f0ea 100%);
  overflow-x: hidden;
}
</style>