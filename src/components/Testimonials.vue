<template>
  <section id="testimonios" class="py-24 relative bg-[#050505]">
    <div class="max-w-6xl mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-playfair text-white mb-4">Críticas de nuestros <span class="text-amber-500 italic">Comensales</span></h2>
        <div class="w-24 h-1 bg-amber-500 mx-auto rounded-full"></div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="(review, idx) in reviews" :key="idx" class="bg-[#111] p-8 rounded-xl border border-white/5 hover:border-amber-500/30 transition-all duration-300">
          <div class="flex items-center gap-1 mb-6 text-amber-500">
            <svg v-for="i in 5" :key="i" class="w-4 h-4 fill-current" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/></svg>
          </div>
          <p class="text-gray-400 font-light italic mb-8 leading-relaxed">"{{ review.text }}"</p>
          <div class="flex items-center gap-4 border-t border-white/5 pt-4">
            <div>
              <h4 class="text-white font-medium">{{ review.author }}</h4>
              <span class="text-xs text-amber-500/70">{{ review.role }}</span>
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
