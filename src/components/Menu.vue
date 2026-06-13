<script setup>
const menuItems = [
  {
    name: 'Tartar de Res Premium',
    description: 'Corte fino de res wagyu, yema curada, alcaparras crujientes y emulsión de mostaza antigua.',
    price: '$32'
  },
  {
    name: 'Lubina Salvaje',
    description: 'Sellada a la perfección, puré de coliflor ahumada, espárragos de mar y beurre blanc de yuzu.',
    price: '$45'
  },
  {
    name: 'Pato Glaseado',
    description: 'Pechuga de pato madurado, reducción de frutos rojos, texturas de remolacha y pistachos.',
    price: '$42'
  },
  {
    name: 'Esfera de Chocolate',
    description: 'Chocolate oscuro 70%, corazón líquido de maracuyá, polvo de oro y helado de vainilla en vaina.',
    price: '$24'
  }
];
</script>

<template>
  <section id="menu" class="py-32 bg-rest-dark relative border-t border-white/5">
    <div class="max-w-7xl mx-auto px-6">
      
      <div class="text-center mb-24">
        <span class="text-rest-gold font-semibold tracking-widest uppercase text-xs md:text-sm mb-4 block">
          Menú Degustación
        </span>
        <h2 class="font-serif text-4xl md:text-6xl text-white mb-6">Obras Maestras</h2>
        <div class="w-16 h-px bg-rest-gold mx-auto"></div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
        <!-- Imagen -->
        <div class="relative group overflow-hidden">
          <div class="absolute inset-0 bg-rest-accent/20 mix-blend-overlay z-10 group-hover:opacity-0 transition-opacity duration-700"></div>
          <img src="/images/dish.png" alt="Plato Gourmet" class="w-full h-auto object-cover transform group-hover:scale-105 transition-transform duration-1000 grayscale-[30%] group-hover:grayscale-0" />
          <!-- Marco decorativo -->
          <div class="absolute inset-4 border border-white/20 z-20 pointer-events-none"></div>
        </div>

        <!-- Lista de Platillos -->
        <div class="space-y-12">
          <div v-for="(item, index) in menuItems" :key="index" class="group cursor-pointer">
            <div class="flex justify-between items-baseline mb-2">
              <h3 class="font-serif text-2xl text-rest-light group-hover:text-rest-gold transition-colors duration-300">
                {{ item.name }}
              </h3>
              <div class="flex-grow border-b border-dashed border-white/20 mx-4 relative top-[-6px]"></div>
              <span class="font-serif text-xl text-rest-accent">{{ item.price }}</span>
            </div>
            <p class="text-gray-400 font-light text-sm leading-relaxed pr-16 group-hover:text-gray-300 transition-colors duration-300">
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>
