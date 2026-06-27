<template>
  <section class="py-40 bg-rest-dark relative overflow-hidden border-t border-white/5">
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      
      <!-- Titulo Asimetrico -->
      <div class="flex flex-col lg:flex-row gap-12 mb-24 items-end">
        <h2 class="text-6xl md:text-8xl font-serif text-white leading-[0.9] reveal-left flex-1">
          Eventos <br/><span class="italic text-rest-gold font-light pl-12 md:pl-24">Privados</span>
        </h2>
        <div class="w-full lg:w-1/3 reveal-right">
          <p class="text-gray-400 font-sans font-light text-lg">
            Celebre sus momentos más importantes en nuestros salones exclusivos. Diseño íntimo, menús personalizados y servicio impecable, aislados del bullicio.
          </p>
        </div>
      </div>

      <!-- Layout Asimetrico Editorial -->
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 lg:gap-12 relative">
        <!-- Imagen Principal (Larga) -->
        <div class="lg:col-span-7 relative group reveal-up">
          <div class="aspect-[4/5] overflow-hidden relative">
            <div class="absolute inset-0 bg-rest-dark/20 z-10 group-hover:bg-transparent transition-colors duration-1000"></div>
            <img src="https://images.unsplash.com/photo-1551632436-cbf8dd35adfa?q=80&w=1200&auto=format&fit=crop" alt="Salón Privado Principal" class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-[2s] filter contrast-125" />
          </div>
          <div class="absolute bottom-8 left-8 right-8 z-20">
            <h3 class="font-serif text-4xl text-white mb-2 drop-shadow-xl">El Salón Ámbar</h3>
            <div class="flex items-center gap-4">
              <span class="text-rest-gold font-sans font-bold text-xs uppercase tracking-[0.2em]">Capacidad: 12 Personas</span>
            </div>
          </div>
        </div>

        <!-- Columna Secundaria (Desfasada) -->
        <div class="lg:col-span-5 flex flex-col justify-center gap-12 mt-12 lg:mt-32">
          
          <div class="relative group reveal-up delay-200">
            <div class="aspect-square overflow-hidden relative w-3/4 ml-auto">
              <div class="absolute inset-0 bg-rest-dark/20 z-10 group-hover:bg-transparent transition-colors duration-1000"></div>
              <img src="https://images.unsplash.com/photo-1549488344-c60317e3be97?q=80&w=800&auto=format&fit=crop" alt="Mesa de Eventos" class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-[2s] filter grayscale-[40%] group-hover:grayscale-0" />
            </div>
            <div class="mt-6 text-right w-3/4 ml-auto">
              <h3 class="font-serif text-3xl text-white mb-2">Salón Vantablack</h3>
              <p class="text-gray-400 font-sans font-light text-sm">Privacidad absoluta tras puertas ocultas, ideal para juntas directivas y compromisos.</p>
            </div>
          </div>

          <div class="reveal-up delay-400 p-8 border border-rest-gold/20 hover:border-rest-gold/50 transition-colors duration-500 bg-rest-dark/50 backdrop-blur-sm">
            <h4 class="font-sans font-light text-rest-gold tracking-[0.3em] uppercase text-xs mb-4">Cotizar Evento</h4>
            <p class="text-gray-300 font-serif text-xl mb-6 leading-relaxed">Póngase en contacto con nuestro Concierge para diseñar un menú a la medida de su celebración.</p>
            <a href="#reservar" class="inline-block text-white border-b border-rest-gold pb-1 font-sans font-bold uppercase tracking-widest text-xs hover:text-rest-gold transition-colors">Hablar con Concierge</a>
          </div>
          
        </div>
      </div>
      
    </div>
  </section>
</template>
