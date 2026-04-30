<template>
  <section id="educacion" class="py-20 bg-gray-50">
    <div class="max-w-4xl mx-auto px-6">
      <h2 class="text-xl font-semibold text-gray-900 mb-10">Educación</h2>
      <div class="flex flex-col gap-4">
        <div v-for="edu in educacion" :key="edu.titulo"
          class="bg-white border border-gray-200 rounded-xl p-6">
          <div class="flex justify-between items-start">
            <div>
              <h3 class="font-semibold text-gray-900">{{ edu.titulo }}</h3>
              <p class="text-sm text-gray-500 mt-1">{{ edu.centro }}</p>
            </div>
            <span class="text-xs text-gray-400 bg-gray-50 border border-gray-200 px-3 py-1 rounded-full">
              {{ edu.periodo }}
            </span>
          </div>
          <p v-if="edu.descripcion" class="text-sm text-gray-400 mt-3 leading-relaxed">
            {{ edu.descripcion }}
          </p>
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