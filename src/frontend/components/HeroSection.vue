<template>
  <section id="hero" class="bg-white border-b border-gray-200 py-20">
    <div class="max-w-4xl mx-auto px-6">
      <div class="flex flex-col md:flex-row items-center gap-10">
        <div class="w-28 h-28 rounded-full bg-sky-100 flex items-center justify-center text-sky-700 text-3xl font-bold flex-shrink-0">
          IP
        </div>
        <div class="text-center md:text-left">
          <h1 class="text-3xl font-bold text-gray-900">Pau Garcia</h1>
          <p class="text-gray-500 mt-2 text-lg">Cloud Engineer · DevSecOps · AWS</p>
          <p class="text-gray-400 mt-3 max-w-lg text-sm leading-relaxed">
            Especializado en infraestructura cloud con AWS, automatización DevSecOps
            y desarrollo seguro de software...
          </p>
          <div class="flex gap-2 mt-5 flex-wrap justify-center md:justify-start">
            <span v-for="tag in tags" :key="tag"
              class="bg-sky-50 text-sky-700 text-xs px-3 py-1 rounded-full border border-sky-100">
              {{ tag }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const tags = ['AWS Cloud', 'DevSecOps', 'Security+', 'Vue.js', 'CI/CD']
</script>