<script setup>
import NavBar from './frontend/components/NavBar.vue'
import HeroSection from './frontend/components/HeroSection.vue'
import ProyectosSection from './frontend/components/ProyectosSection.vue'
import CertificacionesSection from './frontend/components/CertificacionesSection.vue'
import EducacionSection from './frontend/components/EducacionSection.vue'
import ContactoSection from './frontend/components/ContactoSection.vue'
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