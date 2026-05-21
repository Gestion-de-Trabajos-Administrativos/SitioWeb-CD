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
        icon: 'i-lucide-award',
        title: 'Compromiso',
        description: 'Nos distingue el compromiso diario por mantener la frescura de nuestros productos.'
      }, {
        icon: 'i-lucide-zap',
        title: 'Calidad',
        description: 'La comodidad y la calidad del servicio ofrecido a nuestros clientes es nuestra prioridad.'
      }, {
        icon: 'i-lucide-badge-dollar-sign',
        title: 'Servicio',
        description: 'Aceptamos las siguientes formas de pago: Efectivo, Tarjeta y Transferencia bancaria.'
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
