<script setup lang="ts">
const items = [
  'papas.jpg', 'tomate.jpg', 'carne.jpg','lechuga.jpg','cebolla.jpg','salchicha.jpg','pan.jpg','repollo.jpg', 'frijoles.jpg'
]
</script>

<template>
  <div>
    <UPageHero class="hero-bg">
      <template #title >
        <h1 class="text-[#ffffff]">
          Taquería:
        </h1>
        <h1 class="text-[#ffffff]">
          El Callejón de Dany
        </h1>
      </template>
    </UPageHero>
    
    <hr class="bg-[#309bb5]">

    <UPageSection
      id="features"
      title="CONÓCENOS"
      description="En Taquería 'El Callejón de Dany' nos dedicamos a la preparación de alimentos con un estricto control de higiene. Nuestra especialidad abarca desde los tacos de carne asada y tacos piratas (chicos y grandes), acompañados de nuestros frijoles charros, hasta hamburguesas sencillas preparadas al momento y órdenes de papas con complementos frescos. Ofrecemos un servicio ágil y un entorno limpio para brindar una experiencia gastronómica confiable y de alta calidad a toda la comunidad."
      :features="[{
        icon: 'i-lucide-rocket',
        title: 'Production-ready from day one',
        description: 'Pre-configured with TypeScript, ESLint, Tailwind CSS, and all the best practices. Focus on building features, not setting up tooling.'
      }, {
        icon: 'i-lucide-palette',
        title: 'Beautiful by default',
        description: 'Leveraging Nuxt UI\'s design system with automatic dark mode, consistent spacing, and polished components that look great out of the box.'
      }, {
        icon: 'i-lucide-zap',
        title: 'Lightning fast',
        description: 'Optimized for performance with SSR/SSG support, automatic code splitting, and edge-ready deployment. Your users will love the speed.'
      }, {
        icon: 'i-lucide-blocks',
        title: '100+ components included',
        description: 'Access Nuxt UI\'s comprehensive component library. From forms to navigation, everything is accessible, responsive, and customizable.'
      }]"
    />

    <p class="text-4xl font-bold text-center text-white">
      ¡EXPLORA NUESTRO SABOR!
    </p>

    <UCarousel
      v-slot="{ item }"
      loop
      arrows
      auto-scroll
      :items="items"
      :ui="{ container: 'gap-0', item: 'basis-1/5' }"
    >
      <img
        :src="item"
        class="w-[300px] h-[300px] object-cover rounded-lg my-20"
        loading="lazy"
      >
    </UCarousel>

    <hr class="h-2 bg-[#e52463] my-8">
  </div>
</template>
