<template>
  <section id="galeria" class="py-32 bg-rest-dark relative border-t border-white/5">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-20 reveal-up">
        <span class="text-rest-gold font-sans font-light tracking-[0.4em] uppercase text-xs md:text-sm mb-4 block">
          Portafolio Culinario
        </span>
        <h2 class="text-5xl md:text-6xl font-serif text-white mb-6">Experiencia <span class="italic text-rest-gold font-light">Visual</span></h2>
        <div class="w-16 h-[1px] bg-rest-gold mx-auto opacity-50"></div>
      </div>

      <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
        <div 
          v-for="(img, idx) in gallery" 
          :key="idx" 
          :class="['relative overflow-hidden group cursor-pointer reveal-scale', img.span ? 'col-span-2 row-span-2' : '', `delay-${(idx % 4 + 1) * 100}`]"
        >
          <div class="absolute inset-0 bg-rest-dark/70 group-hover:bg-rest-dark/10 transition-colors duration-700 z-10 mix-blend-multiply"></div>
          <img :src="img.src" :alt="img.alt" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-[1.5s] ease-out grayscale-[50%] group-hover:grayscale-0" />
          
          <!-- Efecto Marco Interno Hover -->
          <div class="absolute inset-4 border border-rest-gold/0 group-hover:border-rest-gold/40 transition-all duration-700 z-20 pointer-events-none scale-110 group-hover:scale-100"></div>

          <div class="absolute inset-0 flex flex-col justify-end p-8 z-30 opacity-0 group-hover:opacity-100 transition-opacity duration-700 bg-gradient-to-t from-rest-dark via-rest-dark/50 to-transparent translate-y-4 group-hover:translate-y-0">
            <div class="w-8 h-[1px] bg-rest-gold mb-3 transform origin-left scale-x-0 group-hover:scale-x-100 transition-transform duration-700 delay-300"></div>
            <h3 class="text-white font-serif text-2xl md:text-3xl tracking-wide">{{ img.alt }}</h3>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const gallery = [
  { src: 'https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&q=80&w=800', alt: 'Corte Premium', span: true },
  { src: 'https://images.unsplash.com/photo-1559339352-11d035aa65de?auto=format&fit=crop&q=80&w=400', alt: 'Postre Exclusivo', span: false },
  { src: 'https://images.unsplash.com/photo-1550966871-3ed3cdb5ed0c?auto=format&fit=crop&q=80&w=400', alt: 'Ambiente Íntimo', span: false },
  { src: 'https://images.unsplash.com/photo-1514362545857-3bc16c4c7d1b?auto=format&fit=crop&q=80&w=400', alt: 'Coctelería de Autor', span: false },
  { src: 'https://images.unsplash.com/photo-1546069901-ba9599a7e63c?auto=format&fit=crop&q=80&w=400', alt: 'Ensalada Orgánica', span: false }
];
</script>
