<script setup>
import { Cog6ToothIcon, BoltIcon, Square3Stack3DIcon } from '@heroicons/vue/24/outline'

const supportLinks = [
  {
    name: 'Mecanizado de Piezas y Diseño 3D',
    href: '#contacto',
    description:
      'Nuestro servicio de mecanizado de piezas es altamente versátil. Ya sea que tengas un diseño en mente, una muestra existente o necesites que creemos un diseño en 3D personalizado, estamos aquí para satisfacer tus necesidades de fabricación de piezas. Especializados en materiales polímeros, materiales no ferrosos y aceros especiales, ofrecemos soluciones de alta calidad y precisión para tu proyecto.',
    icon: Square3Stack3DIcon,
  },
  {
    name: 'Automatización de Maquinaria y Control CNC',
    href: '#contacto',
    description:
      'Transforma tu proceso de producción con nuestra experiencia en automatización de maquinaria. Diseñamos e implementamos sistemas de control CNC avanzados que optimizan la eficiencia y la precisión en tu línea de producción. Además, ofrecemos servicios de mecanizado en máquinas y herramientas, incluyendo máquinas CNC, para mantener tu equipo en condiciones de trabajo óptimas.',
    icon: Cog6ToothIcon,
  },
  {
    name: 'Fabricación de Piezas por Corte Laser y Doblado',
    href: '#contacto',
    description:
      'Nuestra tecnología de corte láser de vanguardia nos permite crear piezas precisas y personalizadas de acuerdo a tus especificaciones. Combinado con nuestro servicio de doblado, ofrecemos soluciones de fabricación eficientes y de alta calidad. Ya sea para prototipos o producción a gran escala, estamos preparados para cumplir con tus requerimientos.',
    icon: BoltIcon,
  },
]
</script>

<template>
    <div id="servicios" class="bg-white">
      <!-- Header -->
      <div class="relative bg-gray-800 pb-32">
        <div class="absolute inset-0">
          <img class="h-full w-full object-cover" src="/images/service-bg.jpg" alt="" />
          <div class="absolute inset-0 bg-yellow-800 mix-blend-multiply" aria-hidden="true" />
        </div>
        <div class="relative mx-auto max-w-7xl py-24 px-6 sm:py-32 lg:px-8">
          <h1 class="text-4xl font-bold tracking-tight text-white md:text-5xl lg:text-6xl">Servicios</h1>
          <p class="mt-6 max-w-3xl text-xl text-gray-300">Descubre nuestra gama de servicios especializados en mecanizado, automatización y fabricación de piezas. Además, ofrecemos servicios de mantenimiento y reparación para garantizar que tus equipos y maquinaria funcionen de manera óptima. Tu satisfacción es nuestra prioridad.</p>
        </div>
      </div>

      <!-- Overlapping cards -->
      <section class="relative z-10 mx-auto -mt-32 max-w-7xl px-6 lg:px-8" aria-labelledby="contact-heading">
        <h2 class="sr-only" id="contact-heading">Contact us</h2>
        <div class="grid grid-cols-1 gap-y-20 lg:grid-cols-3 lg:gap-y-0 lg:gap-x-8">
          <div v-for="link in supportLinks" :key="link.name" class="flex flex-col rounded-2xl bg-white shadow-xl">
            <div class="relative flex-1 px-6 pt-16 pb-8 md:px-8">
              <div class="absolute top-0 inline-block -translate-y-1/2 transform rounded-xl bg-yellow-600 p-5 shadow-lg">
                <component :is="link.icon" class="h-6 w-6 text-white" aria-hidden="true" />
              </div>
              <h3 class="text-xl font-medium text-gray-900">{{ link.name }}</h3>
              <p class="mt-4 text-base text-gray-500">{{ link.description }}</p>
            </div>
            <div class="rounded-bl-2xl rounded-br-2xl bg-gray-50 p-6 md:px-8">
              <a :href="link.href" class="text-base font-medium text-yellow-700 hover:text-yellow-600">Hablemos<span aria-hidden="true"> &rarr;</span></a>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>