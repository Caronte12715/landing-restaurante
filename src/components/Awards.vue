<template>
  <section class="py-24 bg-rest-gold relative overflow-hidden flex flex-col justify-center border-t border-b border-rest-dark">
    <!-- Static intro text -->
    <div class="max-w-7xl mx-auto px-6 w-full mb-12 text-center reveal-up">
      <span class="text-rest-dark font-sans font-bold tracking-[0.4em] uppercase text-xs">
        Reconocimiento Internacional
      </span>
    </div>

    <!-- Infinite Marquee -->
    <div class="w-full relative overflow-hidden flex whitespace-nowrap">
      <div class="animate-marquee flex items-center gap-16 md:gap-32 px-8">
        <!-- Michelin -->
        <div class="flex items-center gap-6">
          <svg class="w-12 h-12 text-rest-dark" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z" />
          </svg>
          <span class="font-serif text-3xl md:text-5xl text-rest-dark tracking-wide">3 Estrellas Michelin</span>
        </div>
        
        <div class="w-2 h-2 rounded-full bg-rest-dark opacity-30"></div>

        <!-- Repsol -->
        <div class="flex items-center gap-6">
          <svg class="w-12 h-12 text-rest-dark" viewBox="0 0 24 24" fill="currentColor">
            <circle cx="12" cy="12" r="10" />
          </svg>
          <span class="font-serif text-3xl md:text-5xl text-rest-dark tracking-wide">3 Soles Repsol</span>
        </div>

        <div class="w-2 h-2 rounded-full bg-rest-dark opacity-30"></div>

        <!-- 50 Best -->
        <div class="flex items-center gap-6">
          <span class="font-sans font-bold text-4xl text-rest-dark">Nº 14</span>
          <span class="font-serif text-3xl md:text-5xl text-rest-dark tracking-wide">The World's 50 Best</span>
        </div>
        
        <div class="w-2 h-2 rounded-full bg-rest-dark opacity-30"></div>
      </div>
      
      <!-- Duplicated for seamless loop -->
      <div class="animate-marquee flex items-center gap-16 md:gap-32 px-8" aria-hidden="true">
        <!-- Michelin -->
        <div class="flex items-center gap-6">
          <svg class="w-12 h-12 text-rest-dark" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z" />
          </svg>
          <span class="font-serif text-3xl md:text-5xl text-rest-dark tracking-wide">3 Estrellas Michelin</span>
        </div>
        
        <div class="w-2 h-2 rounded-full bg-rest-dark opacity-30"></div>

        <!-- Repsol -->
        <div class="flex items-center gap-6">
          <svg class="w-12 h-12 text-rest-dark" viewBox="0 0 24 24" fill="currentColor">
            <circle cx="12" cy="12" r="10" />
          </svg>
          <span class="font-serif text-3xl md:text-5xl text-rest-dark tracking-wide">3 Soles Repsol</span>
        </div>

        <div class="w-2 h-2 rounded-full bg-rest-dark opacity-30"></div>

        <!-- 50 Best -->
        <div class="flex items-center gap-6">
          <span class="font-sans font-bold text-4xl text-rest-dark">Nº 14</span>
          <span class="font-serif text-3xl md:text-5xl text-rest-dark tracking-wide">The World's 50 Best</span>
        </div>
        
        <div class="w-2 h-2 rounded-full bg-rest-dark opacity-30"></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes marquee {
  0% { transform: translateX(0%); }
  100% { transform: translateX(-100%); }
}
.animate-marquee {
  animation: marquee 25s linear infinite;
}
</style>
