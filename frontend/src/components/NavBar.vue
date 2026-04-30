<template>
  <nav class="sticky top-0 z-50 bg-white border-b border-gray-200">
    <div class="max-w-4xl mx-auto px-6 h-14 flex items-center justify-between">
      <span class="font-semibold text-gray-900">Pau Garcia</span>
      <div class="hidden md:flex gap-6">
        <a v-for="link in links" :key="link.label" :href="link.href"
          class="text-sm text-gray-500 hover:text-sky-500 transition-colors">
          {{ link.label }}
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
const links = [
  { label: 'Sobre mí',        href: '#hero' },
  { label: 'Proyectos',       href: '#proyectos' },
  { label: 'Certificaciones', href: '#certificaciones' },
  { label: 'Educación',       href: '#educacion' },
  { label: 'Contacto',        href: '#contacto' },
]
</script>