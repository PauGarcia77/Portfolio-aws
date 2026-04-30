<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import ProyectosSection from './components/ProyectosSection.vue'
import CertificacionesSection from './components/CertificacionesSection.vue'
import EducacionSection from './components/EducacionSection.vue'
import ContactoSection from './components/ContactoSection.vue'
</script>

<template>
  <div class="min-h-screen bg-gray-50">
    <NavBar />

    <main>
      <HeroSection />

      <ProyectosSection />

      <CertificacionesSection />

      <EducacionSection />

      <ContactoSection />
    </main>

    <footer class="py-8 text-center text-gray-500 border-t">
      <p>© {{ new Date().getFullYear() }} Pau García - Portfolio AWS</p>
    </footer>
  </div>
</template>

<style>
/* Estilos globales si los necesitas */
html {
  scroll-behavior: smooth;
}
</style>