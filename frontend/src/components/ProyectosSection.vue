<template>
  <section id="proyectos" class="py-20 bg-gray-50">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="text-xl font-semibold text-gray-900 mb-10">Proyectos</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div v-for="p in proyectos" :key="p.titulo"
          class="bg-white border border-gray-200 rounded-xl p-6 hover:border-sky-300 transition-colors">
          <h3 class="font-semibold text-gray-900">{{ p.titulo }}</h3>
          <p class="text-sm text-gray-500 mt-2 leading-relaxed">{{ p.descripcion }}</p>
          <div class="flex gap-2 mt-4 flex-wrap">
            <span v-for="tag in p.tags" :key="tag"
              class="bg-blue-50 text-blue-700 text-xs px-2 py-1 rounded">
              {{ tag }}
            </span>
          </div>
          <a v-if="p.link" :href="p.link" target="_blank"
            class="inline-block mt-4 text-xs text-sky-500 hover:underline">
            Ver proyecto →
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const proyectos = [
  {
    titulo: 'Portfolio AWS',
    descripcion: 'Web estática desplegada con S3, CloudFront, ACM y Route 53. CI/CD con GitHub Actions.',
    tags: ['S3', 'CloudFront', 'Route 53', 'ACM', 'GitHub Actions'],
    link: 'https://github.com/PauGarcia77/Portfolio-aws'
  }
]
</script>