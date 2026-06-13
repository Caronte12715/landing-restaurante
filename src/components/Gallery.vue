<template>
  <section id="galeria" class="py-24 bg-black relative">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-playfair text-white mb-4">Experiencia <span class="text-amber-500 italic">Visual</span></h2>
        <p class="text-gray-400 font-light max-w-2xl mx-auto">Un vistazo a nuestros platillos exclusivos y el ambiente inigualable de nuestras instalaciones.</p>
      </div>

      <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
        <div v-for="(img, idx) in gallery" :key="idx" :class="['relative overflow-hidden group cursor-pointer', img.span ? 'col-span-2 row-span-2' : '']">
          <div class="absolute inset-0 bg-black/60 group-hover:bg-transparent transition-colors duration-500 z-10"></div>
          <img :src="img.src" :alt="img.alt" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700 ease-out" />
          <div class="absolute inset-0 flex flex-col justify-end p-6 z-20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 bg-gradient-to-t from-black/90 to-transparent">
            <h3 class="text-white font-playfair text-xl">{{ img.alt }}</h3>
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
