<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/Logo.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'Taquería: El Callejón de Dany'
const description = '¡Ven y descubre la variedad de sabores en La Taquería El Callejón de Dany!'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/Logo.ico',
  twitterCard: 'summary_large_image'
})

const items = ref<NavigationMenuItem[][]>([
  [
    {
      label: 'INICIO',
      icon: 'i-lucide-house',
      to: '/'
    },
    {
      label: 'MENÚ',
      icon: 'i-lucide-menu',
      to: '/menu'
    },
    {
      label: 'SOBRE NOSOTROS',
      icon: 'i-lucide-user',
      to: '/nosotros',
      active: true
    }
  ]
])
</script>

<template>
  <UApp>
    <UHeader class="bg-[#e52463] text-[#ffffff]  flex items-center justify-between px-4">
      <template #left>
    <div class="flex items-center gap-2">
      <img
        src="/Logo.png"
        alt="Logo"
        class="max-w-[80px] h-auto object-contain"
      />
      <span class="font-bold text-base">
        TAQUERÍA: EL CALLEJÓN DE DANY
      </span>
    </div>
  </template>
      
      <template #right>
        <UNavigationMenu color="primary" :items="items" />
      </template>
    </UHeader>

    <UMain class="bg-gradient-to-b from-[#fac51c] via-[#fac51c] to-[#fa9221]"
    >
      <NuxtPage />
    </UMain>

    <UFooter class="my-10">
      <template #left>
        <p class="text-lg text-muted">
          Taquería: El Callejón de Dany • © {{ new Date().getFullYear() }}
        </p>
      </template>

      <template #right>
        <p class="text-lg text-muted">
          ¡Sígue nuestra cuenta de Facebook Oficial!
        </p>
        <UButton
          to="https://www.facebook.com/callejondefierritos"
          target="_blank"
          icon="i-simple-icons-facebook"
          aria-label="Facebook"
          color="neutral"
          variant="ghost"
        />
      </template>
    </UFooter>
  </UApp>
</template>