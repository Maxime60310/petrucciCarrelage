<script>
  // Tu peux ajouter des variables ou de la logique ici si nécessaire
</script>

<div class="relative min-h-screen w-full flex flex-col justify-between bg-gray-900 text-white overflow-hidden">
  
  <div class="absolute inset-0 z-0">
    <img 
      src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1920&q=80" 
      alt="Salle de bain moderne carrelée" 
      class="w-full h-full object-cover"
    />
    <div class="absolute inset-0 bg-black/60"></div>
  </div>

  <header class="relative z-10 flex items-center justify-between px-6 py-4 max-w-7xl w-full mx-auto">
    <div class="flex items-center space-x-2">
      <div class="border-2 border-indigo-400 px-3 py-1 font-bold tracking-wider rounded text-sm sm:text-base">
        Petrucci Carrelage
      </div>
    </div>

    <div class="flex items-center space-x-6">
      <nav class="hidden md:flex items-center space-x-6 text-sm font-medium">
        <a href="#propos" class="hover:text-blue-400 transition underline underline-offset-4 decoration-blue-500">À propos de nous</a>
        <a href="#realisations" class="hover:text-blue-400 transition">Réalisations</a>
        <a href="#avis" class="hover:text-blue-400 transition">Avis</a>
      </nav>
      
      <a 
        href="#contact" 
        class="bg-slate-900/90 hover:bg-slate-800 border border-slate-700 text-white px-4 py-2 rounded-md text-xs sm:text-sm font-semibold transition"
      >
        Contacter pour un projet !
      </a>
    </div>
  </header>

  <main class="relative z-10 flex-grow flex flex-col items-center justify-center text-center px-4 max-w-4xl mx-auto my-12">
    <span class="text-indigo-300 font-semibold uppercase tracking-wider text-sm sm:text-base mb-3">
      Votre expert carreleur
    </span>
    
    <h1 class="text-3xl sm:text-5xl font-bold tracking-tight leading-tight max-w-3xl mb-8">
      Salles de bains, cuisines, terrasses. <br class="hidden sm:inline" />
      <span class="text-slate-200 font-medium">Qualité & précision.</span>
    </h1>

    <div class="flex flex-col sm:flex-row gap-4 w-full sm:w-auto">
      <a 
        href="#contact" 
        class="bg-slate-900/80 hover:bg-slate-800 border border-slate-700 px-6 py-3 rounded-md font-medium text-sm transition text-center"
      >
        Contacter pour un projet !
      </a>
      <a 
        href="#realisations" 
        class="bg-blue-600 hover:bg-blue-500 px-6 py-3 rounded-md font-medium text-sm transition text-center"
      >
        Voir nos réalisations
      </a>
    </div>
  </main>

  <section class="relative z-10 w-full max-w-6xl mx-auto px-4 translate-y-1/2 mt-auto">
    <div class="bg-slate-950/95 border border-slate-800 rounded-lg p-6 grid grid-cols-2 md:grid-cols-5 gap-6 text-center shadow-2xl backdrop-blur-sm">
      
      <div class="flex flex-col items-center space-y-2">
        <svg class="w-8 h-8 text-blue-500" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path d="M12 15a3 3 0 100-6 3 3 0 000 6z" />
          <path d="M19.4 15a1.65 1.65 0 00.33 1.82l.06.06a2 2 0 11-2.83 2.83l-.06-.06a1.65 1.65 0 00-1.82-.33 1.65 1.65 0 00-1 1.51V21a2 2 0 01-4 0v-.09A1.65 1.65 0 009 19.4a1.65 1.65 0 00-1.82.33l-.06.06a2 2 0 11-2.83-2.83l.06-.06a1.65 1.65 0 00.33-1.82 1.65 1.65 0 00-1.51-1H3a2 2 0 010-4h.09A1.65 1.65 0 005 9a1.65 1.65 0 00-.33-1.82l-.06-.06a2 2 0 112.83-2.83l.06.06a1.65 1.65 0 001.82.33H9a1.65 1.65 0 001-1.51V3a2 2 0 014 0v.09a1.65 1.65 0 001 1.51 1.65 1.65 0 001.82-.33l.06-.06a2 2 0 112.83 2.83l-.06.06a1.65 1.65 0 00-.33 1.82V9a1.65 1.65 0 001.51 1H21a2 2 0 010 4h-.09a1.65 1.65 0 00-1.51 1z" />
        </svg>
        <span class="text-xs sm:text-sm font-semibold text-gray-200">15+ ans d'expérience</span>
      </div>

      <div class="flex flex-col items-center space-y-2">
        <svg class="w-8 h-8 text-blue-500" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
        </svg>
        <span class="text-xs sm:text-sm font-semibold text-gray-200">Devis gratuit</span>
      </div>

      <div class="flex flex-col items-center space-y-2 col-span-2 md:col-span-1">
        <svg class="w-8 h-8 text-blue-500" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z" />
          <path d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
        </svg>
        <span class="text-xs sm:text-sm font-semibold text-gray-200">Expertise de votre projet</span>
      </div>

      <div class="flex flex-col items-center space-y-2">
        <svg class="w-8 h-8 text-blue-500" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
        </svg>
        <span class="text-xs sm:text-sm font-semibold text-gray-200">Respect des délais</span>
      </div>

      <div class="flex flex-col items-center space-y-2">
        <svg class="w-8 h-8 text-blue-500" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path d="M14 10h4.757a1 1 0 011 1v1a4.9 4.9 0 01-4.9 4.9H12v3H9.1a2 2 0 01-1.8-1.2L5 11V3h8a2 2 0 012 2v5z" />
        </svg>
        <span class="text-xs sm:text-sm font-semibold text-gray-200">Satisfaction</span>
      </div>

    </div>
  </section>
  
</div>

<div class="bg-slate-900 pt-24 pb-16 text-center text-gray-400">
  <p>La suite du site commence ici après la barre d'avantages...</p>
</div>