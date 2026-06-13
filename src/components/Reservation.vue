<template>
  <section id="reservas" class="py-24 relative overflow-hidden bg-[url('https://images.unsplash.com/photo-1514933651103-005eec06c04b?auto=format&fit=crop&q=80&w=1920')] bg-cover bg-fixed bg-center">
    <div class="absolute inset-0 bg-black/80 backdrop-blur-sm z-0"></div>
    
    <div class="max-w-4xl mx-auto px-6 relative z-10">
      <div class="bg-[#0A0A0A]/90 border border-amber-500/20 p-10 md:p-14 rounded-2xl">
        <div class="text-center mb-10">
          <h2 class="text-3xl md:text-4xl font-playfair text-white mb-4">Asegura tu <span class="text-amber-500 italic">Mesa</span></h2>
          <p class="text-gray-400 font-light">Debido a la alta demanda, sugerimos reservar con al menos 48 horas de anticipación.</p>
        </div>

        <form class="space-y-6">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div>
              <label class="block text-sm text-gray-400 mb-2">Nombre Completo</label>
              <input type="text" class="w-full bg-transparent border-b border-white/20 px-0 py-2 text-white focus:outline-none focus:border-amber-500 transition-colors" placeholder="Ej. Juan Pérez" />
            </div>
            <div>
              <label class="block text-sm text-gray-400 mb-2">Teléfono / WhatsApp</label>
              <input type="tel" class="w-full bg-transparent border-b border-white/20 px-0 py-2 text-white focus:outline-none focus:border-amber-500 transition-colors" placeholder="+1 234 567 8900" />
            </div>
            <div>
              <label class="block text-sm text-gray-400 mb-2">Fecha</label>
              <input type="date" class="w-full bg-transparent border-b border-white/20 px-0 py-2 text-white focus:outline-none focus:border-amber-500 transition-colors" />
            </div>
            <div>
              <label class="block text-sm text-gray-400 mb-2">Hora</label>
              <select class="w-full bg-transparent border-b border-white/20 px-0 py-2 text-white focus:outline-none focus:border-amber-500 transition-colors appearance-none">
                <option class="bg-[#0A0A0A]">19:00</option>
                <option class="bg-[#0A0A0A]">20:00</option>
                <option class="bg-[#0A0A0A]">21:00</option>
                <option class="bg-[#0A0A0A]">22:00</option>
              </select>
            </div>
            <div class="md:col-span-2">
              <label class="block text-sm text-gray-400 mb-2">Número de Personas</label>
              <select class="w-full bg-transparent border-b border-white/20 px-0 py-2 text-white focus:outline-none focus:border-amber-500 transition-colors appearance-none">
                <option class="bg-[#0A0A0A]">2 Personas</option>
                <option class="bg-[#0A0A0A]">3 Personas</option>
                <option class="bg-[#0A0A0A]">4 Personas</option>
                <option class="bg-[#0A0A0A]">Mesa Grande (+5 personas)</option>
              </select>
            </div>
          </div>
          
          <div class="pt-6">
            <button type="button" class="w-full py-4 border border-amber-500 text-amber-500 font-bold tracking-widest uppercase hover:bg-amber-500 hover:text-black transition-colors duration-300">
              Solicitar Reservación
            </button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>
