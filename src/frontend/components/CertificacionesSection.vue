<template>
  <section id="certificaciones" class="py-20 bg-white">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="text-xl font-semibold text-gray-900 mb-10">Certificaciones</h2>
      <div class="flex flex-col gap-4">
        <div v-for="cert in certificaciones" :key="cert.nombre"
          class="flex items-center gap-5 border border-gray-200 rounded-xl p-5 hover:border-sky-300 transition-colors">
          <img :src="cert.imagen" :alt="cert.nombre" class="w-14 h-14 object-contain rounded-lg" />
          <div>
            <p class="font-medium text-gray-900">{{ cert.nombre }}</p>
            <p class="text-sm text-gray-400 mt-1">{{ cert.emisor }} · {{ cert.año }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const certificaciones = [
  {
    nombre: 'AWS Solutions Architect Associate',
    emisor: 'Amazon Web Services',
    año: '2024',
    imagen: '/projects/comptia-security-plus.webp'
  },
  {
    nombre: 'CompTIA Security+',
    emisor: 'CompTIA',
    año: '2024',
    imagen: '/projects/comptia-security-plus.webp'
  }
]
</script>