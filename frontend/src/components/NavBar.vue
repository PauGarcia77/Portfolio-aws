<template>
  <nav class="sticky top-0 z-50 glass-strong border-b border-white/5">
    <div class="max-w-5xl mx-auto px-6 h-16 flex items-center justify-between">
      <a href="#hero" class="group flex items-center gap-2.5">
        <span class="relative inline-flex h-8 w-8 items-center justify-center rounded-lg bg-white text-black text-sm font-bold transition-transform group-hover:scale-105">
          PG
        </span>
        <span class="font-semibold tracking-tight text-white">Pau Garcia</span>
      </a>
      <div class="hidden md:flex gap-1">
        <a v-for="link in links" :key="link.label" :href="link.href"
          class="relative text-sm text-neutral-400 hover:text-white px-3 py-2 rounded-lg transition-colors duration-200 hover:bg-white/5">
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
