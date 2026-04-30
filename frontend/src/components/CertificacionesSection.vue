<template>
  <section id="certificaciones" class="relative py-24">
    <div class="max-w-5xl mx-auto px-6">
      <div class="mb-12">
        <p class="text-xs font-semibold uppercase tracking-[0.2em] text-neutral-400">Logros</p>
        <h2 class="text-3xl md:text-4xl font-bold text-white mt-2">
          Certificaciones<span class="text-gradient">.</span>
        </h2>
        <div class="mt-4 h-px w-24 bg-gradient-to-r from-white/60 to-transparent"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <div v-for="cert in certificaciones" :key="cert.nombre"
          class="group relative flex items-center gap-5 glass rounded-2xl p-5 hover:border-white/30 transition-all duration-300 hover:-translate-y-0.5">
          <div class="relative flex-shrink-0">
            <div class="relative w-16 h-16 rounded-xl bg-white/5 border border-white/10 flex items-center justify-center p-2">
              <img :src="cert.imagen" :alt="cert.nombre" class="w-full h-full object-contain" />
            </div>
          </div>
          <div class="flex-1 min-w-0">
            <p class="font-semibold text-white truncate">{{ cert.nombre }}</p>
            <p class="text-sm text-neutral-400 mt-1">{{ cert.emisor }}</p>
            <span class="inline-block mt-2 text-[11px] font-medium text-neutral-200 bg-white/5 border border-white/10 px-2 py-0.5 rounded-full">
              {{ cert.año }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const certificaciones = [
  {
    nombre: 'AWS Cloud Practioner',
    emisor: 'Amazon Web Services',
    año: '2024',
    imagen: '/projects/comptia-security-plus.webp'
  }
]
</script>
