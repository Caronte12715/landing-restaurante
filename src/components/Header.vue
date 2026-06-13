<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
  <header 
    :class="[
      'fixed w-full top-0 z-50 transition-all duration-500 border-b border-white/5',
      isScrolled ? 'bg-rest-dark/95 backdrop-blur-md py-4 shadow-lg' : 'bg-transparent py-8'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <a href="#" class="text-3xl font-serif font-bold text-rest-light tracking-widest uppercase">
        Savoir<span class="text-rest-accent">.</span>
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-10">
        <a href="#menu" class="text-sm font-semibold tracking-widest uppercase text-rest-light hover:text-rest-gold transition-colors">Menú</a>
        <a href="#historia" class="text-sm font-semibold tracking-widest uppercase text-rest-light hover:text-rest-gold transition-colors">Historia</a>
        <a href="#reservar" class="bg-rest-accent hover:bg-orange-600 text-white px-8 py-3 rounded-sm font-semibold text-xs transition-all duration-300 uppercase tracking-widest border border-rest-accent hover:border-orange-600">
          Reservar Mesa
        </a>
      </nav>

      <!-- Mobile Toggle -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen" 
        class="md:hidden text-rest-light p-2 focus:outline-none"
      >
        <svg v-if="!isMobileMenuOpen" xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div 
      v-if="isMobileMenuOpen" 
      class="md:hidden absolute top-full left-0 w-full bg-rest-dark shadow-2xl border-t border-white/10 flex flex-col"
    >
      <a href="#menu" class="p-6 border-b border-white/5 text-center font-semibold tracking-widest uppercase text-rest-light">Menú</a>
      <a href="#historia" class="p-6 border-b border-white/5 text-center font-semibold tracking-widest uppercase text-rest-light">Historia</a>
      <a href="#reservar" class="p-6 bg-rest-accent text-white text-center font-bold uppercase tracking-widest">Reservar Mesa</a>
    </div>
  </header>
</template>
