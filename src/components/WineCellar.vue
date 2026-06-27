<template>
  <section class="py-32 relative overflow-hidden bg-rest-dark">
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="flex flex-col lg:flex-row items-center gap-20">
        
        <!-- Text Content -->
        <div class="w-full lg:w-1/2 reveal-left">
          <div class="inline-flex items-center gap-4 mb-8">
            <div class="w-8 h-[1px] bg-rest-gold"></div>
            <span class="text-rest-gold text-xs font-sans font-light tracking-[0.4em] uppercase">
              La Bodega Subterránea
            </span>
          </div>
          <h2 class="text-5xl md:text-7xl font-serif text-white mb-8 leading-[1.1]">
            Néctar de los <br/><span class="text-rest-gold italic font-light">Dioses</span>
          </h2>
          <p class="text-gray-400 font-sans font-light text-lg leading-relaxed mb-8">
            Nuestra cava resguarda más de 1,500 etiquetas celosamente seleccionadas de los viñedos más exclusivos del mundo. Un santuario dedicado al arte del maridaje perfecto.
          </p>
          <div class="grid grid-cols-2 gap-8 mb-12">
            <div>
              <h4 class="text-3xl font-serif text-white mb-2">1.5K+</h4>
              <p class="text-xs font-sans text-rest-gold tracking-[0.2em] uppercase">Etiquetas</p>
            </div>
            <div>
              <h4 class="text-3xl font-serif text-white mb-2">25</h4>
              <p class="text-xs font-sans text-rest-gold tracking-[0.2em] uppercase">Países</p>
            </div>
          </div>
          <a href="#" class="inline-flex items-center gap-4 text-white hover:text-rest-gold transition-colors group">
            <span class="font-sans font-light tracking-[0.2em] uppercase text-sm">Explorar Carta de Vinos</span>
            <div class="w-12 h-[1px] bg-white group-hover:bg-rest-gold transition-colors"></div>
          </a>
        </div>

        <!-- Parallax/Masked Image -->
        <div class="w-full lg:w-1/2 relative group reveal-right delay-200">
          <div class="aspect-[3/4] overflow-hidden rounded-t-full rounded-b-sm relative">
            <!-- Overlay oscuro -->
            <div class="absolute inset-0 bg-rest-dark/40 z-10 mix-blend-multiply group-hover:bg-transparent transition-colors duration-1000"></div>
            <img 
              src="https://images.unsplash.com/photo-1506377247377-2a5b3b417ebb?q=80&w=1000&auto=format&fit=crop" 
              alt="Wine Cellar" 
              class="w-full h-[120%] object-cover object-center -translate-y-10 group-hover:-translate-y-0 transition-transform duration-[2s] ease-out grayscale-[40%] group-hover:grayscale-0"
            />
            <!-- Golden ring decor -->
            <div class="absolute top-4 left-4 right-4 bottom-4 border border-rest-gold/30 rounded-t-full rounded-b-none z-20 pointer-events-none scale-95 group-hover:scale-100 transition-transform duration-1000 opacity-50"></div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
