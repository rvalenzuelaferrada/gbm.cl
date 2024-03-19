
<script setup>
const people = [
  {
    name: 'Piezas en bronce fosfórico',
    company: 'Carozzi',
    description: 'Estas son las piezas solicitadas debido al desgaste en el mecanismo de la máquina envasadora de productos alimenticios de nuestro cliente. Nuestra atención meticulosa a la calidad y la precisión garantiza un rendimiento óptimo y una producción sin problemas en la maquinaria de envasado.',
    imageUrl:
      '/images/proyectos/07_img.jpeg',
    url: '#',
  },
  {
    name: 'Piezas de acero',
    company: 'Carozzi',
    description: 'Estas piezas han sido solicitadas para ajustar los movimientos del brazo robótico en un proyecto destinado a la calibración de puntos de programación del robot. Estas componentes desempeñan un papel crucial en garantizar la precisión y la eficiencia en la ejecución de las tareas programadas por el robot.',
    imageUrl:
      '/images/proyectos/10_img.jpeg',
    url: '#',
  },
  {
    name: 'Piezas en polímero Ertacetal',
    company: 'Carozzi',
    description: 'Estas piezas han sido solicitadas para su uso en la línea de transmisión en un entorno corrosivo. Están fabricadas en polímero de alta resistencia y dureza, diseñadas para soportar las condiciones corrosivas y la degradación, asegurando un funcionamiento fiable y duradero en este ambiente exigente.',
    imageUrl:
      '/images/proyectos/08_img.jpeg',
    url: '#',
  },
  // More people...
]
</script>

<template>
    <div id="proyectos" class="bg-white">
      <div class="mx-auto max-w-7xl py-12 px-6 lg:px-8 lg:py-24">
        <div class="space-y-12">
          <div class="space-y-5 sm:space-y-4 md:max-w-xl lg:max-w-3xl xl:max-w-none">
            <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Proyectos</h2>
            <p class="text-xl text-gray-500">Explora nuestra cartera de proyectos destacados, donde hemos abordado desafíos diversos y entregado soluciones innovadoras. Desde la optimización de robots industriales hasta la fabricación de piezas resistentes en entornos corrosivos.</p>
          </div>
          <ul role="list" class="space-y-12 sm:grid sm:grid-cols-2 sm:gap-x-6 sm:gap-y-12 sm:space-y-0 lg:grid-cols-3 lg:gap-x-8">
            <li v-for="person in people" :key="person.name">
              <div class="space-y-4">
                <div class="aspect-w-3 aspect-h-2">
                  <img class="rounded-lg object-cover shadow-lg" :src="person.imageUrl" alt="" />
                </div>

                <div class="space-y-2">
                  <div class="space-y-1 text-lg font-medium leading-6">
                    <h3>{{ person.name }}</h3>
                    <!--<p class="text-yellow-600">{{ person.company }}</p>-->
                    <p class="mt-4 pt-4 text-base text-gray-500">{{ person.description }}</p>
                  </div>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </template>