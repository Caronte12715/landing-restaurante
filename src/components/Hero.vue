<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const heroRef = ref(null);
const mouseX = ref(50);
const mouseY = ref(50);

const handleMouseMove = (e) => {
  if (!heroRef.value) return;
  const rect = heroRef.value.getBoundingClientRect();
  const x = ((e.clientX - rect.left) / rect.width) * 100;
  const y = ((e.clientY - rect.top) / rect.height) * 100;
  mouseX.value = x;
  mouseY.value = y;
};

onMounted(() => {
  if (heroRef.value) {
    heroRef.value.addEventListener('mousemove', handleMouseMove);
  }
});

onUnmounted(() => {
  if (heroRef.value) {
    heroRef.value.removeEventListener('mousemove', handleMouseMove);
  }
});
</script>

<template>
  <section 
    ref="heroRef"
    class="relative h-[110vh] min-h-[900px] flex items-center overflow-hidden bg-rest-dark cursor-crosshair"
    :style="{ '--mouse-x': `${mouseX}%`, '--mouse-y': `${mouseY}%` }"
  >
    <!-- Asymmetric Background layout -->
    <div class="absolute inset-0 z-0 flex">
      <div class="w-full lg:w-2/3 h-full relative">
        <div class="absolute inset-0 opacity-40 transition-opacity duration-300 mix-blend-screen pointer-events-none z-20"
             style="background: radial-gradient(circle 600px at var(--mouse-x) var(--mouse-y), rgba(212, 175, 55, 0.2), transparent 80%);">
        </div>
        <!-- High-end Video Background simulation (using an Unsplash luxury cooking gif or high-quality image) -->
        <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=2000&auto=format&fit=crop" class="w-full h-full object-cover object-center filter grayscale-[60%] contrast-125 opacity-40 animate-slow-zoom" />
        <div class="absolute inset-0 bg-gradient-to-r from-rest-dark via-rest-dark/80 to-transparent z-10"></div>
        <div class="absolute inset-0 bg-gradient-to-t from-rest-dark via-transparent to-transparent z-10"></div>
      </div>
      <div class="hidden lg:block w-1/3 h-full bg-rest-dark"></div>
    </div>

    <!-- Editorial Content -->
    <div class="relative z-10 w-full px-6 max-w-[1400px] mx-auto flex flex-col justify-center animate-fade-in-up mt-20">
      
      <div class="flex items-center gap-6 mb-12 reveal-up">
        <div class="h-[1px] w-24 bg-rest-gold"></div>
        <span class="text-rest-gold font-sans font-bold tracking-[0.5em] uppercase text-xs">
          Haute Cuisine
        </span>
      </div>
      
      <!-- Titulo Gigante Asimetrico cortando la pantalla -->
      <h1 class="font-serif text-[12vw] text-rest-light mb-8 leading-[0.85] tracking-tighter drop-shadow-2xl reveal-up delay-100 relative left-[-1vw]">
        El Arte <br/>
        <span class="italic text-rest-gold font-light pr-4 relative z-10">Sensorial.</span>
      </h1>
      
      <div class="flex flex-col lg:flex-row gap-12 mt-12 w-full lg:w-2/3 items-start lg:items-center reveal-up delay-200">
        <p class="text-gray-400 text-lg lg:text-xl font-sans font-light leading-relaxed flex-1">
          Una rebelión contra lo ordinario. Ingredientes excepcionales, fuego vivo y una atmósfera diseñada para desafiar las expectativas gastronómicas más exigentes.
        </p>
        
        <div class="flex flex-col gap-6 w-full sm:w-auto">
          <a href="#reservar" class="group relative w-full sm:w-auto bg-transparent border border-rest-gold/50 text-rest-gold px-10 py-5 text-xs font-bold transition-all duration-500 uppercase tracking-[0.3em] overflow-hidden text-center">
            <span class="relative z-10 group-hover:text-rest-dark transition-colors duration-500">Reservar Mesa</span>
            <div class="absolute inset-0 bg-rest-gold transform scale-y-0 group-hover:scale-y-100 transition-transform duration-500 origin-bottom"></div>
          </a>
          <a href="#menu" class="text-rest-light hover:text-rest-gold text-xs font-bold transition-colors duration-300 uppercase tracking-[0.3em] text-center flex items-center justify-center gap-3 group">
            Ver el Menú
            <span class="w-8 h-[1px] bg-rest-light group-hover:bg-rest-gold transition-colors"></span>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(60px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes slowZoom {
  from { transform: scale(1); }
  to { transform: scale(1.15); }
}
.animate-fade-in-up {
  animation: fadeInUp 1.5s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}
.animate-slow-zoom {
  animation: slowZoom 40s linear infinite alternate;
}
</style>
