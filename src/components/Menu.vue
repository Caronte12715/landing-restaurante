<script setup>
import { ref } from 'vue';

const menuItems = [
  {
    name: 'Tartar de Res Premium',
    description: 'Corte fino de res wagyu, yema curada, alcaparras crujientes y emulsión de mostaza antigua.',
    price: '$32',
    image: 'https://images.unsplash.com/photo-1544025162-d76694265947?q=80&w=1000&auto=format&fit=crop'
  },
  {
    name: 'Lubina Salvaje',
    description: 'Sellada a la perfección, puré de coliflor ahumada, espárragos de mar y beurre blanc de yuzu.',
    price: '$45',
    image: 'https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000&auto=format&fit=crop'
  },
  {
    name: 'Pato Glaseado',
    description: 'Pechuga de pato madurado, reducción de frutos rojos, texturas de remolacha y pistachos.',
    price: '$42',
    image: 'https://images.unsplash.com/photo-1553621042-f6e147245754?q=80&w=1000&auto=format&fit=crop'
  },
  {
    name: 'Esfera de Chocolate',
    description: 'Chocolate oscuro 70%, corazón líquido de maracuyá, polvo de oro y helado de vainilla en vaina.',
    price: '$24',
    image: 'https://images.unsplash.com/photo-1563805042-7684c8e9e5cb?q=80&w=1000&auto=format&fit=crop'
  }
];

const activeImage = ref(menuItems[0].image);

const setActiveImage = (img) => {
  activeImage.value = img;
};
</script>

<template>
  <section id="menu" class="py-40 bg-rest-dark relative overflow-hidden">
    <!-- Huge background letter -->
    <div class="absolute left-[-10%] top-1/2 -translate-y-1/2 text-[40vw] font-serif text-white/5 pointer-events-none select-none leading-none">
      M
    </div>

    <div class="max-w-[1400px] mx-auto px-6 relative z-10">
      
      <div class="flex flex-col md:flex-row justify-between items-end mb-32 reveal-up">
        <div>
          <span class="text-rest-gold font-sans font-light tracking-[0.4em] uppercase text-xs md:text-sm mb-6 block">
            Degustación
          </span>
          <h2 class="font-serif text-[8vw] md:text-7xl lg:text-[7rem] text-rest-light leading-[0.85] tracking-tighter">Obras <br/>Maestras</h2>
        </div>
        <div class="hidden md:block w-32 h-[1px] bg-rest-gold opacity-50 mb-8"></div>
      </div>

      <div class="flex flex-col lg:flex-row gap-20">
        <!-- Interactive Image Panel (Left) -->
        <div class="w-full lg:w-5/12 relative hidden lg:block reveal-left">
          <div class="sticky top-40 h-[700px] overflow-hidden group">
            <transition name="fade" mode="out-in">
              <img :key="activeImage" :src="activeImage" alt="Plato Gourmet" class="absolute inset-0 w-full h-full object-cover filter grayscale-[20%] contrast-125 transform scale-105 transition-transform duration-[2s] group-hover:scale-100" />
            </transition>
            <!-- Vignette -->
            <div class="absolute inset-0 bg-gradient-to-t from-rest-dark via-transparent to-transparent opacity-60"></div>
          </div>
        </div>

        <!-- Menu List (Right) -->
        <div class="w-full lg:w-7/12 space-y-16 lg:mt-32">
          <div 
            v-for="(item, index) in menuItems" 
            :key="index" 
            class="group cursor-pointer relative reveal-right"
            :class="`delay-${(index + 1) * 100}`"
            @mouseenter="setActiveImage(item.image)"
          >
            <div class="flex flex-col mb-4">
              <div class="flex justify-between items-end border-b border-white/10 pb-6 group-hover:border-rest-gold/50 transition-colors duration-500">
                <h3 class="font-serif text-4xl md:text-5xl lg:text-6xl text-rest-light group-hover:text-rest-gold transition-colors duration-500 leading-none">
                  {{ item.name }}
                </h3>
                <span class="font-sans font-light text-2xl text-rest-gold tracking-wider">{{ item.price }}</span>
              </div>
            </div>
            <p class="text-gray-400 font-sans font-light text-lg leading-relaxed max-w-lg mt-6 group-hover:text-gray-300 transition-colors duration-300">
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.8s ease, transform 0.8s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: scale(1.05);
}
.fade-enter-to,
.fade-leave-from {
  opacity: 1;
  transform: scale(1);
}
</style>
