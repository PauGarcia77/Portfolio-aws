<template>
  <section id="hero" class="relative py-24 md:py-32">
    <div class="max-w-5xl mx-auto px-6">
      <div class="flex flex-col md:flex-row items-center gap-12">
        <!-- Avatar -->
        <div class="relative flex-shrink-0 animate-fade-up">
          <div class="absolute inset-0 bg-white/10 rounded-full blur-2xl animate-float"></div>
          <div class="relative w-32 h-32 md:w-36 md:h-36 rounded-full bg-gradient-to-br from-white via-neutral-300 to-neutral-600 p-[2px]">
            <div class="w-full h-full rounded-full bg-black flex items-center justify-center">
              <span class="text-4xl font-bold text-gradient">PG</span>
            </div>
          </div>
        </div>

        <!-- Texto -->
        <div class="text-center md:text-left">
          <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight text-white animate-fade-up">
            Hola, soy <span class="text-gradient">Pau García</span>
          </h1>
          <p class="text-neutral-400 mt-3 text-lg md:text-xl font-medium animate-fade-up delay-100">
            Cloud Engineer · DevSecOps · AWS
          </p>
          <p class="text-neutral-400 mt-5 max-w-xl text-sm md:text-base leading-relaxed animate-fade-up delay-200">
            Apasionado del desarrollo de software, terminando mi FP Superior en DAM y adentrándome en el mundo cloud.
            Aprendiendo AWS, DevOps y todo lo que rodea a la ingeniería en la nube con ganas de crecer y construir cosas que escalen.
          </p>
          <div class="flex gap-2 mt-6 flex-wrap justify-center md:justify-start animate-fade-up delay-300">
            <span v-for="tag in tags" :key="tag"
              class="glass text-neutral-200 text-xs font-medium px-3 py-1.5 rounded-full hover:border-white/30 hover:text-white transition-colors">
              {{ tag }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const tags = ['AWS Cloud', 'DevSecOps', 'Vue.js', 'CI/CD']
</script>
