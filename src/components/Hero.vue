<script setup>
</script>

<template>
  <section class="relative h-screen min-h-[700px] flex items-center justify-center overflow-hidden bg-rest-dark">
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img src="/images/hero.png" alt="Alta Cocina" class="w-full h-full object-cover object-center opacity-40 scale-105 animate-slow-zoom" />
      <div class="absolute inset-0 bg-gradient-to-t from-rest-dark via-rest-dark/50 to-transparent"></div>
      <div class="absolute inset-0 bg-gradient-to-r from-rest-dark via-transparent to-rest-dark opacity-80"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 text-center px-4 max-w-5xl mx-auto animate-fade-in-up mt-20">
      <div class="flex items-center justify-center gap-4 mb-8">
        <div class="h-px w-12 bg-rest-gold"></div>
        <span class="text-rest-gold font-semibold tracking-[0.3em] uppercase text-xs md:text-sm">
          Experiencia Culinaria
        </span>
        <div class="h-px w-12 bg-rest-gold"></div>
      </div>
      
      <h1 class="font-serif text-6xl md:text-8xl lg:text-9xl text-white mb-8 leading-none tracking-tight drop-shadow-2xl">
        El Arte del <br/>
        <span class="italic text-rest-light/90 font-light">Sabor</span>
      </h1>
      
      <p class="text-gray-300 text-lg md:text-xl font-light mb-14 max-w-2xl mx-auto drop-shadow leading-relaxed">
        Donde la tradición se encuentra con la innovación. Descubre platos diseñados para despertar tus sentidos en una atmósfera de lujo sin pretensiones.
      </p>
      
      <div class="flex flex-col sm:flex-row items-center justify-center gap-6">
        <a href="#reservar" class="w-full sm:w-auto bg-rest-accent hover:bg-orange-600 text-white px-12 py-4 rounded-sm font-bold text-sm transition-all duration-300 uppercase tracking-widest hover:-translate-y-1 shadow-[0_0_20px_rgba(230,92,0,0.3)] hover:shadow-[0_0_30px_rgba(230,92,0,0.5)]">
          Reservar Ahora
        </a>
        <a href="#menu" class="w-full sm:w-auto bg-transparent border border-white/30 hover:border-white hover:bg-white/5 text-white px-12 py-4 rounded-sm font-bold text-sm transition-all duration-300 uppercase tracking-widest hover:-translate-y-1">
          Ver Menú
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes slowZoom {
  from { transform: scale(1); }
  to { transform: scale(1.1); }
}
.animate-fade-in-up {
  animation: fadeInUp 1.2s cubic-bezier(0.2, 0.8, 0.2, 1) forwards;
}
.animate-slow-zoom {
  animation: slowZoom 20s linear infinite alternate;
}
</style>
