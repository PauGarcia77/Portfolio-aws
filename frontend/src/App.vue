<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import ProyectosSection from './components/ProyectosSection.vue'
import CertificacionesSection from './components/CertificacionesSection.vue'
import EducacionSection from './components/EducacionSection.vue'
import ContactoSection from './components/ContactoSection.vue'
</script>

<template>
  <div class="relative min-h-screen overflow-x-hidden bg-white text-neutral-900">
    <!-- Decorative background -->
    <div class="pointer-events-none fixed inset-0 -z-10">
      <div class="absolute inset-0 grid-bg opacity-70"></div>
      <div class="absolute -top-32 -left-32 w-[28rem] h-[28rem] bg-neutral-200/60 rounded-full blur-3xl animate-blob"></div>
      <div class="absolute top-1/3 -right-32 w-[28rem] h-[28rem] bg-neutral-200/60 rounded-full blur-3xl animate-blob delay-200"></div>
      <div class="absolute bottom-0 left-1/3 w-[26rem] h-[26rem] bg-neutral-200/50 rounded-full blur-3xl animate-blob delay-400"></div>
      <div class="absolute inset-0 bg-gradient-to-b from-transparent via-transparent to-white"></div>
    </div>

    <NavBar />

    <main class="relative">
      <HeroSection />
      <ProyectosSection />
      <CertificacionesSection />
      <EducacionSection />
      <ContactoSection />
    </main>

    <footer class="relative border-t border-black/10 py-10 text-center">
      <div class="max-w-4xl mx-auto px-6">
        <p class="text-sm text-neutral-500">
          © {{ new Date().getFullYear() }}
          <span class="text-neutral-900 font-medium">Pau García</span>
          · Portfolio AWS
        </p>
        <p class="mt-2 text-xs text-neutral-400">
          Diseñado y desplegado en la nube ☁
        </p>
      </div>
    </footer>
  </div>
</template>
