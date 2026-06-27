<template>
  <section id="historia" class="py-32 relative overflow-hidden bg-rest-dark">
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="flex flex-col md:flex-row items-center gap-20">
        <div class="w-full md:w-1/2 relative group reveal-left">
          <div class="absolute inset-0 bg-rest-gold/10 translate-x-4 translate-y-4 rounded-sm group-hover:translate-x-6 group-hover:translate-y-6 transition-transform duration-700 pointer-events-none"></div>
          <img src="https://images.unsplash.com/photo-1577219491135-ce391730fb2c?auto=format&fit=crop&q=80&w=800" alt="Chef preparando platillo" class="relative z-10 rounded-sm w-full h-[600px] object-cover grayscale-[30%] group-hover:grayscale-0 transition-all duration-1000 contrast-125" />
          <!-- Marco decorativo overlay -->
          <div class="absolute inset-8 border border-white/20 z-20 pointer-events-none scale-105 group-hover:scale-100 transition-transform duration-1000 opacity-0 group-hover:opacity-100"></div>
        </div>
        <div class="w-full md:w-1/2 reveal-right delay-200">
          <div class="inline-flex items-center gap-4 mb-8">
            <div class="w-8 h-[1px] bg-rest-gold"></div>
            <span class="text-rest-gold text-xs font-sans font-light tracking-[0.4em] uppercase">
              Tradición y Vanguardia
            </span>
          </div>
          <h2 class="text-5xl md:text-6xl font-serif text-white mb-8 leading-[1.1]">La Esencia de la <br/><span class="text-rest-gold italic font-light">Alta Cocina</span></h2>
          <p class="text-gray-400 font-sans font-light text-lg leading-relaxed mb-6">
            Fundado en el corazón de la ciudad, SAVOIR nació de la visión del Chef Ejecutivo Alexander V., quien tras recorrer los mercados más remotos de Europa y Asia, decidió destilar esa amalgama de sabores en una experiencia sin precedentes.
          </p>
          <p class="text-gray-400 font-sans font-light text-lg leading-relaxed mb-12">
            Nuestra cocina no es solo técnica e ingredientes de proximidad; es el relato íntimo del fuego, el tiempo y la pasión, plasmado en cada emplatado.
          </p>
          <div class="flex items-center gap-6">
            <img src="https://upload.wikimedia.org/wikipedia/commons/f/f6/Signature_of_Alexander_Hamilton.svg" alt="Firma del Chef" class="h-16 opacity-40 invert filter sepia-[0.5] hue-rotate-[10deg]" />
            <div class="border-l border-white/20 pl-6">
              <span class="block text-white font-serif text-xl">Alexander V.</span>
              <span class="text-xs text-rest-gold tracking-[0.3em] uppercase font-light">Chef Ejecutivo</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
