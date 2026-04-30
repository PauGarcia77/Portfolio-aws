<template>
  <section id="educacion" class="relative py-24">
    <div class="max-w-5xl mx-auto px-6">
      <div class="mb-12">
        <p class="text-xs font-semibold uppercase tracking-[0.2em] text-neutral-500">Formación</p>
        <h2 class="text-3xl md:text-4xl font-bold text-neutral-900 mt-2">
          Educación<span class="text-gradient">.</span>
        </h2>
        <div class="mt-4 h-px w-24 bg-gradient-to-r from-black/60 to-transparent"></div>
      </div>

      <div class="relative">
        <!-- Vertical timeline line -->
        <div class="absolute left-4 top-2 bottom-2 w-px bg-gradient-to-b from-black/40 via-black/20 to-transparent"></div>

        <div class="flex flex-col gap-6">
          <div v-for="edu in educacion" :key="edu.titulo"
            class="relative pl-12">
            <!-- Timeline dot -->
            <span class="absolute left-2 top-6 w-5 h-5 rounded-full bg-black ring-4 ring-white"></span>

            <div class="glass rounded-2xl p-6 hover:border-black/30 transition-colors duration-300">
              <div class="flex justify-between items-start gap-4 flex-wrap">
                <div>
                  <h3 class="font-semibold text-lg text-neutral-900">{{ edu.titulo }}</h3>
                  <p class="text-sm text-neutral-700 mt-1">{{ edu.centro }}</p>
                </div>
                <span class="text-xs font-medium text-neutral-700 bg-black/5 border border-black/10 px-3 py-1 rounded-full whitespace-nowrap">
                  {{ edu.periodo }}
                </span>
              </div>
              <p v-if="edu.descripcion" class="text-sm text-neutral-600 mt-4 leading-relaxed">
                {{ edu.descripcion }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const educacion = [
  {
    titulo: 'FP Superior DAM',
    centro: 'El Cide',
    periodo: '2024-2026',
    descripcion: 'Técnico Superior en Desarrollo de Aplicaciones Multiplataforma (DAM) — Formación Profesional de Grado Superior. Especialización en el desarrollo de software para entornos de escritorio, móvil y web, con sólida base en programación orientada a objetos, bases de datos y despliegue de aplicaciones.'
  }
]
</script>
