<template>
  <section class="relative h-[120vh] bg-rest-dark overflow-hidden flex items-center justify-center">
    <!-- Texto gigante de fondo fijo -->
    <div class="absolute inset-0 flex items-center justify-center opacity-5 pointer-events-none overflow-hidden">
      <h2 class="text-[25vw] font-serif text-white whitespace-nowrap leading-none tracking-tighter">
        FILOSOFÍA
      </h2>
    </div>

    <div class="relative z-10 max-w-5xl mx-auto px-6 text-center reveal-up">
      <div class="mb-12">
        <svg class="w-16 h-16 mx-auto text-rest-gold opacity-50" fill="currentColor" viewBox="0 0 24 24">
          <path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h3.983v10h-9.983z" />
        </svg>
      </div>
      
      <h3 class="font-serif text-4xl md:text-6xl lg:text-7xl text-white mb-12 leading-[1.2] tracking-wide">
        No cocinamos para alimentar el cuerpo, <br/>
        <span class="italic text-rest-gold font-light">cocinamos para incendiar el alma.</span>
      </h3>
      
      <div class="flex items-center justify-center gap-6">
        <div class="w-12 h-[1px] bg-rest-gold"></div>
        <p class="font-sans font-light tracking-[0.3em] uppercase text-gray-400 text-sm">El Manifiesto Savoir</p>
        <div class="w-12 h-[1px] bg-rest-gold"></div>
      </div>
    </div>
  </section>
</template>
