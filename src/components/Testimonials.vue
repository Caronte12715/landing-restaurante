<template>
  <section id="testimonios" class="py-32 relative bg-rest-dark">
    <!-- Ambient Blur -->
    <div class="absolute left-0 top-1/2 -translate-y-1/2 w-[500px] h-[500px] bg-rest-gold/5 rounded-full blur-[150px] pointer-events-none"></div>

    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="text-center mb-24 reveal-up">
        <span class="text-rest-gold font-sans font-light tracking-[0.4em] uppercase text-xs md:text-sm mb-4 block">
          Crítica Gastronómica
        </span>
        <h2 class="text-5xl md:text-6xl font-serif text-white mb-6">La Voz de los <span class="italic text-rest-gold font-light">Comensales</span></h2>
        <div class="w-16 h-[1px] bg-rest-gold mx-auto opacity-50"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
        <div 
          v-for="(review, idx) in reviews" 
          :key="idx" 
          class="bg-rest-dark p-10 rounded-sm border border-white/10 hover:border-rest-gold/40 transition-all duration-700 group relative reveal-up"
          :class="`delay-${(idx + 1) * 100}`"
        >
          <!-- Cita decorativa -->
          <div class="absolute top-6 right-8 text-6xl font-serif text-rest-gold/10 group-hover:text-rest-gold/20 transition-colors duration-700">"</div>
          
          <div class="flex items-center gap-1 mb-8 text-rest-gold opacity-80 group-hover:opacity-100 transition-opacity duration-300">
            <svg v-for="i in 5" :key="i" class="w-4 h-4 fill-current" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/></svg>
          </div>
          <p class="text-gray-400 font-sans font-light italic mb-10 leading-relaxed group-hover:text-gray-300 transition-colors duration-300">"{{ review.text }}"</p>
          <div class="flex items-center gap-4 pt-6 relative">
            <div class="absolute top-0 left-0 w-12 h-[1px] bg-white/20 group-hover:bg-rest-gold/50 transition-colors duration-300"></div>
            <div>
              <h4 class="text-white font-serif text-xl tracking-wide">{{ review.author }}</h4>
              <span class="text-xs font-sans font-light text-rest-gold tracking-widest uppercase">{{ review.role }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const reviews = [
  { text: 'Una experiencia sublime de principio a fin. El trato del personal es excepcional y la calidad de la materia prima se nota en cada bocado. Simplemente perfecto.', author: 'Roberto G.', role: 'Crítico Gastronómico' },
  { text: 'Elegimos Savoir para celebrar nuestro aniversario y superó todas las expectativas. El postre de chocolate amargo es una obra de arte.', author: 'Marina S.', role: 'Cliente Frecuente' },
  { text: 'La carta de vinos es espectacular y el maridaje sugerido por el sommelier elevó los sabores de la cena a otro nivel. Muy recomendable.', author: 'Carlos V.', role: 'Guía Local' }
];
</script>
