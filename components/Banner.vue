<script setup>
import { MegaphoneIcon, XMarkIcon } from '@heroicons/vue/24/outline'

  const dismissBanner = () => {
      document.getElementById('banner').style.display = 'none'
  }
</script>

<template>
    <div id="banner" class="fixed inset-x-0 bottom-0 pb-2 sm:pb-5 z-10">
      <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
        <div class="rounded-lg bg-yellow-600 p-2 shadow-lg sm:p-3">
          <div class="flex flex-wrap items-center justify-between">
            <div class="flex w-0 flex-1 items-center">
              <span class="flex rounded-lg bg-yellow-800 p-2">
                <MegaphoneIcon class="h-6 w-6 text-white" aria-hidden="true" />
              </span>
              <p class="ml-3 truncate font-medium text-white">
                <span class="md:hidden">¡Hablemos, estamos aquí!</span>
                <span class="hidden md:inline">¿Listo para comenzar? ¡Contáctanos ahora y hablemos sobre tu proyecto!</span>
              </p>
            </div>
            <div class="order-3 mt-2 w-full flex-shrink-0 sm:order-2 sm:mt-0 sm:w-auto">
              <a href="#contacto" class="flex items-center justify-center rounded-md border border-transparent bg-white px-4 py-2 text-sm font-medium text-yellow-600 shadow-sm hover:bg-yellow-50">Contacto</a>
            </div>
            <div class="order-2 flex-shrink-0 sm:order-3 sm:ml-2">
              <button @click="dismissBanner" type="button" class="-mr-1 flex rounded-md p-2 hover:bg-yellow-500 focus:outline-none focus:ring-2 focus:ring-white">
                <span class="sr-only">Dismiss</span>
                <XMarkIcon class="h-6 w-6 text-white" aria-hidden="true" />
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>