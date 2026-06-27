<template>
  <section id="reservar" class="py-32 relative overflow-hidden bg-[url('https://images.unsplash.com/photo-1514933651103-005eec06c04b?auto=format&fit=crop&q=80&w=1920')] bg-cover bg-fixed bg-center border-t border-white/5">
    <div class="absolute inset-0 bg-rest-dark/80 backdrop-blur-md z-0"></div>
    
    <div class="max-w-4xl mx-auto px-6 relative z-10">
      <div class="bg-rest-dark/70 backdrop-blur-xl border border-rest-gold/30 p-10 md:p-16 relative reveal-up">
        
        <!-- Esquinas decorativas -->
        <div class="absolute top-0 left-0 w-8 h-8 border-t border-l border-rest-gold/60"></div>
        <div class="absolute top-0 right-0 w-8 h-8 border-t border-r border-rest-gold/60"></div>
        <div class="absolute bottom-0 left-0 w-8 h-8 border-b border-l border-rest-gold/60"></div>
        <div class="absolute bottom-0 right-0 w-8 h-8 border-b border-r border-rest-gold/60"></div>

        <div class="text-center mb-16">
          <span class="text-rest-gold font-sans font-light tracking-[0.4em] uppercase text-xs md:text-sm mb-4 block">
            Invitación Exclusiva
          </span>
          <h2 class="text-4xl md:text-5xl font-serif text-white mb-6">Asegure su <span class="italic text-rest-gold font-light">Mesa</span></h2>
          <div class="w-16 h-[1px] bg-rest-gold mx-auto opacity-50 mb-6"></div>
          <p class="text-gray-400 font-sans font-light">Debido a la exclusividad de nuestro menú degustación, requerimos reservación con 48 horas de anticipación.</p>
        </div>

        <form class="space-y-10">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
            <div class="group relative">
              <label class="block text-xs font-sans text-rest-gold tracking-[0.2em] uppercase mb-2">Nombre Completo</label>
              <input type="text" class="w-full bg-transparent border-b border-white/20 px-0 py-3 text-white focus:outline-none focus:border-rest-gold transition-colors font-serif text-xl" placeholder="Ej. Juan Pérez" />
            </div>
            <div class="group relative">
              <label class="block text-xs font-sans text-rest-gold tracking-[0.2em] uppercase mb-2">Teléfono / WhatsApp</label>
              <input type="tel" class="w-full bg-transparent border-b border-white/20 px-0 py-3 text-white focus:outline-none focus:border-rest-gold transition-colors font-serif text-xl" placeholder="+1 234 567 8900" />
            </div>
            <div class="group relative">
              <label class="block text-xs font-sans text-rest-gold tracking-[0.2em] uppercase mb-2">Fecha</label>
              <input type="date" class="w-full bg-transparent border-b border-white/20 px-0 py-3 text-gray-400 focus:text-white focus:outline-none focus:border-rest-gold transition-colors font-serif text-xl" />
            </div>
            <div class="group relative">
              <label class="block text-xs font-sans text-rest-gold tracking-[0.2em] uppercase mb-2">Hora</label>
              <select class="w-full bg-transparent border-b border-white/20 px-0 py-3 text-gray-400 focus:text-white focus:outline-none focus:border-rest-gold transition-colors font-serif text-xl appearance-none">
                <option class="bg-rest-dark text-white">19:00</option>
                <option class="bg-rest-dark text-white">20:00</option>
                <option class="bg-rest-dark text-white">21:00</option>
                <option class="bg-rest-dark text-white">22:00</option>
              </select>
            </div>
            <div class="md:col-span-2 group relative">
              <label class="block text-xs font-sans text-rest-gold tracking-[0.2em] uppercase mb-2">Número de Personas</label>
              <select class="w-full bg-transparent border-b border-white/20 px-0 py-3 text-gray-400 focus:text-white focus:outline-none focus:border-rest-gold transition-colors font-serif text-xl appearance-none">
                <option class="bg-rest-dark text-white">Mesa Íntima (2 Personas)</option>
                <option class="bg-rest-dark text-white">3 Personas</option>
                <option class="bg-rest-dark text-white">4 Personas</option>
                <option class="bg-rest-dark text-white">Mesa Privada (+5 personas)</option>
              </select>
            </div>
          </div>
          
          <div class="pt-8">
            <button type="button" class="group relative w-full py-5 border border-rest-gold/50 text-rest-gold font-sans font-light tracking-[0.3em] uppercase transition-all duration-500 overflow-hidden bg-transparent">
              <span class="relative z-10 group-hover:text-rest-dark transition-colors duration-500">Confirmar Reservación</span>
              <div class="absolute inset-0 bg-rest-gold transform scale-y-0 group-hover:scale-y-100 transition-transform duration-500 origin-bottom"></div>
            </button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>
