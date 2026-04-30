<template>
  <section id="proyectos" class="relative py-24">
    <div class="max-w-5xl mx-auto px-6">
      <div class="mb-12">
        <p class="text-xs font-semibold uppercase tracking-[0.2em] text-neutral-400">Mi trabajo</p>
        <h2 class="text-3xl md:text-4xl font-bold text-white mt-2">
          Proyectos<span class="text-gradient">.</span>
        </h2>
        <div class="mt-4 h-px w-24 bg-gradient-to-r from-white/60 to-transparent"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <article v-for="p in proyectos" :key="p.titulo"
          class="group relative glass rounded-2xl p-6 overflow-hidden hover:border-white/30 transition-all duration-300 hover:-translate-y-1">
          <div class="flex items-start justify-between gap-4">
            <h3 class="font-semibold text-lg text-white">{{ p.titulo }}</h3>
            <span class="flex-shrink-0 inline-flex items-center justify-center w-9 h-9 rounded-lg bg-white/5 border border-white/10 text-neutral-200 group-hover:bg-white/10 group-hover:rotate-12 transition-all">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M7 17L17 7M17 7H7M17 7V17"/>
              </svg>
            </span>
          </div>

          <p class="text-sm text-neutral-400 mt-3 leading-relaxed">{{ p.descripcion }}</p>

          <div class="flex gap-2 mt-5 flex-wrap">
            <span v-for="tag in p.tags" :key="tag"
              class="bg-white/5 text-neutral-300 text-xs font-medium px-2.5 py-1 rounded-md border border-white/10">
              {{ tag }}
            </span>
          </div>

          <a v-if="p.link" :href="p.link" target="_blank"
            class="inline-flex items-center gap-1.5 mt-5 text-sm font-medium text-white hover:text-neutral-300 transition-colors">
            Ver proyecto
            <svg xmlns="http://www.w3.org/2000/svg" class="w-3.5 h-3.5 transition-transform group-hover:translate-x-1" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M5 12h14M13 5l7 7-7 7"/>
            </svg>
          </a>
        </article>
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
