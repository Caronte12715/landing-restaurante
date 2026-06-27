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
      'fixed w-full top-0 z-50 transition-all duration-700 border-b',
      isScrolled ? 'bg-rest-dark/80 backdrop-blur-xl py-4 shadow-[0_10px_30px_rgba(0,0,0,0.8)] border-white/10' : 'bg-transparent py-8 border-transparent'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <a href="#" class="text-3xl font-serif font-bold text-rest-light tracking-[0.2em] uppercase flex items-center gap-2 group">
        <span class="w-8 h-8 flex items-center justify-center border border-rest-gold text-rest-gold group-hover:bg-rest-gold group-hover:text-rest-dark transition-all duration-500">S</span>
        AVOIR<span class="text-rest-gold">.</span>
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-12">
        <a href="#menu" class="text-xs font-sans font-medium tracking-[0.3em] uppercase text-gray-400 hover:text-rest-gold transition-colors relative group">
          Menú
          <span class="absolute -bottom-2 left-1/2 -translate-x-1/2 w-0 h-[1px] bg-rest-gold transition-all duration-300 group-hover:w-full"></span>
        </a>
        <a href="#historia" class="text-xs font-sans font-medium tracking-[0.3em] uppercase text-gray-400 hover:text-rest-gold transition-colors relative group">
          Historia
          <span class="absolute -bottom-2 left-1/2 -translate-x-1/2 w-0 h-[1px] bg-rest-gold transition-all duration-300 group-hover:w-full"></span>
        </a>
        <a href="#reservar" class="bg-rest-gold hover:bg-white text-rest-dark px-8 py-3 font-bold text-xs transition-all duration-500 uppercase tracking-[0.3em] shadow-[0_0_15px_rgba(212,175,55,0.4)] hover:shadow-[0_0_25px_rgba(255,255,255,0.5)]">
          Reservar Mesa
        </a>
      </nav>

      <!-- Mobile Toggle -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen" 
        class="md:hidden text-rest-light p-2 focus:outline-none hover:text-rest-gold transition-colors"
      >
        <svg v-if="!isMobileMenuOpen" xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div 
      v-if="isMobileMenuOpen" 
      class="md:hidden absolute top-full left-0 w-full bg-rest-dark/95 backdrop-blur-2xl shadow-2xl border-t border-white/10 flex flex-col"
    >
      <a href="#menu" class="p-8 border-b border-white/5 text-center font-sans font-light tracking-[0.3em] uppercase text-gray-300 hover:text-rest-gold">Menú</a>
      <a href="#historia" class="p-8 border-b border-white/5 text-center font-sans font-light tracking-[0.3em] uppercase text-gray-300 hover:text-rest-gold">Historia</a>
      <a href="#reservar" class="p-8 bg-rest-gold text-rest-dark text-center font-bold uppercase tracking-[0.3em]">Reservar Mesa</a>
    </div>
  </header>
</template>
