[Loa Papas Médici.html](https://github.com/user-attachments/files/29642579/Loa.Papas.Medici.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La Era de los Papas Médici: Poder, Arte e Innovación</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700;900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Alpine.js -->
    <script defer src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js"></script>
    <!-- Tailwind Configuration for Custom Fonts and Colors -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        serif: ['Cinzel', 'serif'],
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                    },
                    colors: {
                        vatican: {
                            50: '#fdfcf9',
                            100: '#faf5eb',
                            200: '#f0e3cc',
                            300: '#e1ca9e',
                            400: '#cfa96c',
                            500: '#bd8b42', // Gold
                            600: '#a37133',
                            700: '#835427',
                            800: '#541d13', // Deep Crimson/Burgundy
                            900: '#380c07',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .custom-scrollbar::-webkit-scrollbar {
            width: 6px;
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #faf5eb;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #bd8b42;
            border-radius: 3px;
        }
    </style>
</head>
<body class="bg-vatican-100 text-vatican-900 font-sans selection:bg-vatican-500 selection:text-white leading-relaxed">

    <!-- Header / Hero Section -->
    <header class="relative overflow-hidden bg-vatican-900 text-vatican-100 py-16 px-6 border-b-4 border-vatican-500">
        <!-- Background Pattern Deco -->
        <div class="absolute inset-0 opacity-10 pointer-events-none bg-[radial-gradient(#bd8b42_1px,transparent_1px)] [background-size:16px_16px]"></div>
        
        <div class="max-w-6xl mx-auto text-center relative z-10">
            <span class="text-vatican-400 font-serif tracking-widest text-sm uppercase block mb-3">Renacimiento y Revolución Científica</span>
            <h1 class="font-serif text-4xl md:text-6xl font-black mb-4 text-vatican-200 tracking-tight">LOS PAPAS MÉDICI</h1>
            <p class="text-vatican-300 font-serif text-lg md:text-xl max-w-2xl mx-auto italic mb-8">
                "Mecenazgo, agitación religiosa y las chispas de la ciencia moderna (1513 — 1605)"
            </p>
            <div class="h-[1px] w-40 bg-vatican-500 mx-auto mb-6"></div>
            <p class="text-sm md:text-base max-w-3xl mx-auto text-vatican-300/90 leading-relaxed font-light">
                La dinastía de los Médici no solo gobernó Florencia, sino que escaló al trono de San Pedro en cuatro ocasiones. Bajo sus pontificados, Europa experimentó el quiebre de la Reforma Protestante, pero también un asombroso florecimiento de innovaciones en imprenta, cartografía, arquitectura militar y los primeros indicios del sistema heliocéntrico.
            </p>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 py-12" x-data="{ activeFilter: 'all', selectedPope: 'todos' }">
        
        <!-- SECTION 1: The Medici Popes Grid -->
        <section class="mb-16">
            <h2 class="font-serif text-2xl md:text-3xl text-center text-vatican-800 mb-2">Los Cuatro Pontífices Médici</h2>
            <p class="text-center text-gray-600 text-sm md:text-base max-w-xl mx-auto mb-10">Haz clic en cada uno para filtrar la línea de tiempo y ver qué sucedió bajo su mandato político y espiritual.</p>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Pope 1: León X -->
                <div 
                    @click="selectedPope = (selectedPope === 'leon_x' ? 'todos' : 'leon_x')" 
                    :class="selectedPope === 'leon_x' ? 'ring-4 ring-vatican-500 bg-vatican-200/50' : 'bg-white hover:shadow-xl'"
                    class="p-6 rounded-xl shadow-md border border-vatican-200 transition-all duration-300 cursor-pointer group flex flex-col justify-between"
                >
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-bold uppercase tracking-wider text-vatican-600 px-2.5 py-1 bg-vatican-100 rounded-full">1513 — 1521</span>
                            <span class="text-vatican-500 font-serif font-bold group-hover:translate-x-1 transition-transform">→</span>
                        </div>
                        <h3 class="font-serif text-xl font-bold text-vatican-800 group-hover:text-vatican-500 transition-colors">León X</h3>
                        <p class="text-xs text-gray-500 italic mb-3">Giovanni de' Medici</p>
                        <p class="text-sm text-gray-600 font-light mb-4">
                            El gran mecenas del Alto Renacimiento. Financió a Rafael Sanzio, reestructuró la Universidad de Roma y enfrentó el estallido de la Reforma de Martín Lutero.
                        </p>
                    </div>
                    <div class="border-t border-vatican-100 pt-3 mt-4 text-xs font-semibold text-vatican-700 flex justify-between items-center">
                        <span>Foco: Arte y Humanismo</span>
                        <span class="bg-vatican-800 text-white px-2 py-0.5 rounded text-[10px]" x-show="selectedPope === 'leon_x'">Filtrado</span>
                    </div>
                </div>

                <!-- Pope 2: Clemente VII -->
                <div 
                    @click="selectedPope = (selectedPope === 'clemente_vii' ? 'todos' : 'clemente_vii')" 
                    :class="selectedPope === 'clemente_vii' ? 'ring-4 ring-vatican-500 bg-vatican-200/50' : 'bg-white hover:shadow-xl'"
                    class="p-6 rounded-xl shadow-md border border-vatican-200 transition-all duration-300 cursor-pointer group flex flex-col justify-between"
                >
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-bold uppercase tracking-wider text-vatican-600 px-2.5 py-1 bg-vatican-100 rounded-full">1523 — 1534</span>
                            <span class="text-vatican-500 font-serif font-bold group-hover:translate-x-1 transition-transform">→</span>
                        </div>
                        <h3 class="font-serif text-xl font-bold text-vatican-800 group-hover:text-vatican-500 transition-colors">Clemente VII</h3>
                        <p class="text-xs text-gray-500 italic mb-3">Giulio de' Medici</p>
                        <p class="text-sm text-gray-600 font-light mb-4">
                            Vivió el traumático Saqueo de Roma (1527) y la ruptura de Enrique VIII de Inglaterra. Apoyó decididamente las ciencias y escuchó complacido los postulados de Copérnico.
                        </p>
                    </div>
                    <div class="border-t border-vatican-100 pt-3 mt-4 text-xs font-semibold text-vatican-700 flex justify-between items-center">
                        <span>Foco: Ciencia y Crisis Política</span>
                        <span class="bg-vatican-800 text-white px-2 py-0.5 rounded text-[10px]" x-show="selectedPope === 'clemente_vii'">Filtrado</span>
                    </div>
                </div>

                <!-- Pope 3: Pío IV -->
                <div 
                    @click="selectedPope = (selectedPope === 'pio_iv' ? 'todos' : 'pio_iv')" 
                    :class="selectedPope === 'pio_iv' ? 'ring-4 ring-vatican-500 bg-vatican-200/50' : 'bg-white hover:shadow-xl'"
                    class="p-6 rounded-xl shadow-md border border-vatican-200 transition-all duration-300 cursor-pointer group flex flex-col justify-between"
                >
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-bold uppercase tracking-wider text-vatican-600 px-2.5 py-1 bg-vatican-100 rounded-full">1559 — 1565</span>
                            <span class="text-vatican-500 font-serif font-bold group-hover:translate-x-1 transition-transform">→</span>
                        </div>
                        <h3 class="font-serif text-xl font-bold text-vatican-800 group-hover:text-vatican-500 transition-colors">Pío IV</h3>
                        <p class="text-xs text-gray-500 italic mb-3">Giovanni Angelo Medici</p>
                        <p class="text-sm text-gray-600 font-light mb-4">
                            De la rama milanesa de los Médici. Logró concluir con éxito el Concilio de Trento, fomentó grandes obras públicas en Roma diseñadas por Michelangelo y auspició la reforma del calendario.
                        </p>
                    </div>
                    <div class="border-t border-vatican-100 pt-3 mt-4 text-xs font-semibold text-vatican-700 flex justify-between items-center">
                        <span>Foco: Contrarreforma y Urbanismo</span>
                        <span class="bg-vatican-800 text-white px-2 py-0.5 rounded text-[10px]" x-show="selectedPope === 'pio_iv'">Filtrado</span>
                    </div>
                </div>

                <!-- Pope 4: León XI -->
                <div 
                    @click="selectedPope = (selectedPope === 'leon_xi' ? 'todos' : 'leon_xi')" 
                    :class="selectedPope === 'leon_xi' ? 'ring-4 ring-vatican-500 bg-vatican-200/50' : 'bg-white hover:shadow-xl'"
                    class="p-6 rounded-xl shadow-md border border-vatican-200 transition-all duration-300 cursor-pointer group flex flex-col justify-between"
                >
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-xs font-bold uppercase tracking-wider text-vatican-600 px-2.5 py-1 bg-vatican-100 rounded-full">1605 (26 Días)</span>
                            <span class="text-vatican-500 font-serif font-bold group-hover:translate-x-1 transition-transform">→</span>
                        </div>
                        <h3 class="font-serif text-xl font-bold text-vatican-800 group-hover:text-vatican-500 transition-colors">León XI</h3>
                        <p class="text-xs text-gray-500 italic mb-3">Alessandro Ottaviano de' Medici</p>
                        <p class="text-sm text-gray-600 font-light mb-4">
                            Su pontificado duró menos de un mes, pero representa la consolidación final de la influencia Médici en la Iglesia en los albores del telescopio de Galileo y la revolución científica moderna.
                        </p>
                    </div>
                    <div class="border-t border-vatican-100 pt-3 mt-4 text-xs font-semibold text-vatican-700 flex justify-between items-center">
                        <span>Foco: Transición Científica</span>
                        <span class="bg-vatican-800 text-white px-2 py-0.5 rounded text-[10px]" x-show="selectedPope === 'leon_xi'">Filtrado</span>
                    </div>
                </div>
            </div>

            <!-- Clear Filter Button -->
            <div class="text-center mt-6" x-show="selectedPope !== 'todos'">
                <button @click="selectedPope = 'todos'" class="px-4 py-2 bg-vatican-800 hover:bg-vatican-700 text-vatican-100 rounded-lg text-sm transition-colors shadow font-medium">
                    ← Mostrar todos los papas
                </button>
            </div>
        </section>

        <!-- SECTION 2: Timeline Container -->
        <section class="mb-16">
            <div class="bg-white rounded-2xl shadow-xl p-6 md:p-10 border border-vatican-200">
                <div class="flex flex-col md:flex-row justify-between items-start md:items-center border-b border-vatican-200 pb-6 mb-8 gap-4">
                    <div>
                        <h2 class="font-serif text-2xl md:text-3xl text-vatican-800">Línea de Tiempo Interactiva</h2>
                        <p class="text-gray-500 text-sm mt-1">Sucesos históricos combinados con las innovaciones científicas del periodo Médici.</p>
                    </div>
                    
                    <!-- Filters -->
                    <div class="flex flex-wrap gap-2">
                        <button 
                            @click="activeFilter = 'all'" 
                            :class="activeFilter === 'all' ? 'bg-vatican-800 text-white' : 'bg-vatican-100 text-vatican-700 hover:bg-vatican-200'"
                            class="px-3.5 py-1.5 rounded-full text-xs font-semibold transition-all"
                        >
                            Ver Todo
                        </button>
                        <button 
                            @click="activeFilter = 'hitos'" 
                            :class="activeFilter === 'hitos' ? 'bg-amber-600 text-white' : 'bg-amber-50 text-amber-800 hover:bg-amber-100'"
                            class="px-3.5 py-1.5 rounded-full text-xs font-semibold transition-all"
                        >
                            👑 Hitos Políticos
                        </button>
                        <button 
                            @click="activeFilter = 'innovaciones'" 
                            :class="activeFilter === 'innovaciones' ? 'bg-teal-600 text-white' : 'bg-teal-50 text-teal-800 hover:bg-teal-100'"
                            class="px-3.5 py-1.5 rounded-full text-xs font-semibold transition-all"
                        >
                            ⚙️ Innovación y Ciencia
                        </button>
                    </div>
                </div>

                <!-- Vertical Timeline Graphic -->
                <div class="relative pl-6 md:pl-32 border-l-2 border-vatican-300/60 ml-4 md:ml-0 space-y-12">
                    
                    <!-- Timeline Node Data Object Definition inside Alpine -->
                    <!-- Node 1: 1513 -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'hitos') && (selectedPope === 'todos' || selectedPope === 'leon_x')"
                        class="relative group transition-all"
                    >
                        <!-- Year Tag on Left (Hidden on Mobile, nice layout on Desktop) -->
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1513</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">León X</span>
                        </div>
                        <!-- Icon Node on Line -->
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-amber-500 border-4 border-white shadow ring-2 ring-amber-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1513</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">León X</span>
                            </div>
                            <span class="text-xs font-bold text-amber-700 bg-amber-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">👑 Hito Histórico</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Ascenso de León X e Impulso Cultural en Roma</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Giovanni de' Medici es elegido Papa. De inmediato transforma a Roma en el centro intelectual de Europa Occidental, reviviendo la Universidad de Roma (*La Sapienza*) y creando cátedras de griego clásico y lenguas orientales.
                            </p>
                        </div>
                    </div>

                    <!-- Node 2: 1515 - Imprenta -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'innovaciones') && (selectedPope === 'todos' || selectedPope === 'leon_x')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1515</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">León X</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-teal-500 border-4 border-white shadow ring-2 ring-teal-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1515</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">León X</span>
                            </div>
                            <span class="text-xs font-bold text-teal-700 bg-teal-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">⚙️ Innovación y Ciencia</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">El Auge del Tipo Móvil Griego y Calco en Roma</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light text-justify">
                                Bajo el auspicio de León X, se establece una imprenta griega especializada en Roma liderada por el erudito Janus Lascaris. La tecnología tipográfica avanza con nuevos punzones de metal que permitieron la difusión precisa de manuscritos científicos clásicos en su idioma original por primera vez.
                            </p>
                        </div>
                    </div>

                    <!-- Node 3: 1517 - 95 Tesis -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'hitos') && (selectedPope === 'todos' || selectedPope === 'leon_x')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1517</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">León X</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-amber-500 border-4 border-white shadow ring-2 ring-amber-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1517</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">León X</span>
                            </div>
                            <span class="text-xs font-bold text-amber-700 bg-amber-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">👑 Hito Histórico</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Inicio de la Reforma Protestante (95 Tesis de Lutero)</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Martín Lutero clava sus 95 Tesis en Wittenberg como respuesta directa a la venta de indulgencias promovida por León X para financiar la reconstrucción de la Basílica de San Pedro. Se desata un cisma teológico sin precedentes históricos.
                            </p>
                        </div>
                    </div>

                    <!-- Node 4: 1519 - Leonardo da Vinci y Anatomía -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'innovaciones') && (selectedPope === 'todos' || selectedPope === 'leon_x')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1519</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">León X</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-teal-500 border-4 border-white shadow ring-2 ring-teal-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1519</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">León X</span>
                            </div>
                            <span class="text-xs font-bold text-teal-700 bg-teal-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">⚙️ Innovación y Ciencia</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">El Legado de Leonardo da Vinci y la Óptica Geométrica</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Muere Leonardo da Vinci (quien había vivido en el Vaticano bajo el patrocinio directo del hermano del Papa, Giuliano de' Médici). Sus códices de anatomía, mecánica e ingeniería civil influyen decididamente en los intelectuales romanos, impulsando los estudios de la perspectiva y la física óptica del siglo XVI.
                            </p>
                        </div>
                    </div>

                    <!-- Node 5: 1523 - Elección Clemente VII -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'hitos') && (selectedPope === 'todos' || selectedPope === 'clemente_vii')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1523</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">Clemente VII</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-amber-500 border-4 border-white shadow ring-2 ring-amber-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1523</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">Clemente VII</span>
                            </div>
                            <span class="text-xs font-bold text-amber-700 bg-amber-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">👑 Hito Histórico</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Inicio del Pontificado de Clemente VII</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Giulio de' Medici toma el nombre de Clemente VII. Recibe una Iglesia sumida en profundos conflictos geopolíticos entre Carlos V de España y Francisco I de Francia.
                            </p>
                        </div>
                    </div>

                    <!-- Node 6: 1527 - Saqueo de Roma e Ingeniería Militar -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'innovaciones') && (selectedPope === 'todos' || selectedPope === 'clemente_vii')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1527</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">Clemente VII</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-teal-500 border-4 border-white shadow ring-2 ring-teal-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1527</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">Clemente VII</span>
                            </div>
                            <span class="text-xs font-bold text-teal-700 bg-teal-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">⚙️ Innovación y Ciencia</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Innovación en Metalurgia y Fortificaciones (La Traza Italiana)</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Tras el asedio y saqueo de Roma por los Lansquenetes, surge una revolución táctica defensiva. Arquitectos papales como Antonio da Sangallo el Joven diseñan la **Traza Italiana** o fortificación de estrella, optimizando ángulos contra la artillería de pólvora. Benvenuto Cellini revoluciona técnicas de fundición de cañones desde el Castillo de Sant'Angelo.
                            </p>
                        </div>
                    </div>

                    <!-- Node 7: 1533 - Copérnico en el Vaticano -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'innovaciones') && (selectedPope === 'todos' || selectedPope === 'clemente_vii')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1533</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">Clemente VII</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-teal-500 border-4 border-white shadow ring-2 ring-teal-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1533</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">Clemente VII</span>
                            </div>
                            <span class="text-xs font-bold text-teal-700 bg-teal-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">⚙️ Innovación y Ciencia</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Heliocentrismo: Exposición formal ante Clemente VII</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                En los jardines del Vaticano, el secretario papal Johann Albrecht Widmanstetter dicta una conferencia sobre el innovador modelo heliocéntrico de **Nicolás Copérnico** ante el mismísimo Clemente VII. El Papa queda tan asombrado e impresionado que le regala un valioso manuscrito de agradecimiento e impulsa indirectamente la publicación final de la obra de Copérnico.
                            </p>
                        </div>
                    </div>

                    <!-- Node 8: 1559 - Pío IV y Academias -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'hitos') && (selectedPope === 'todos' || selectedPope === 'pio_iv')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1559</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">Pío IV</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-amber-500 border-4 border-white shadow ring-2 ring-amber-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1559</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">Pío IV</span>
                            </div>
                            <span class="text-xs font-bold text-amber-700 bg-amber-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">👑 Hito Histórico</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Pío IV asume el Pontificado de la Estabilización</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Giovanni Angelo de' Medici es elegido. Su enfoque es pragmático: suaviza la inquisición y orienta el dinero papal a reorganizar las defensas urbanas, la medicina pública y el desarrollo urbanístico.
                            </p>
                        </div>
                    </div>

                    <!-- Node 9: 1560 - Primeras Sociedades Científicas -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'innovaciones') && (selectedPope === 'todos' || selectedPope === 'pio_iv')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1560</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">Pío IV</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-teal-500 border-4 border-white shadow ring-2 ring-teal-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1560</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">Pío IV</span>
                            </div>
                            <span class="text-xs font-bold text-teal-700 bg-teal-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">⚙️ Innovación y Ciencia</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Establecimiento de la "Academia Secretorum Naturae"</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Giambattista della Porta funda en Nápoles la que es considerada la primera sociedad científica de la historia, la *Academia de los Secretos de la Naturaleza*. Pío IV apoya a varios de sus eruditos en Roma para sistematizar inventos empíricos ópticos y mecánicos de la época, sentando los precedentes de las lentes telescópicas.
                            </p>
                        </div>
                    </div>

                    <!-- Node 10: 1563 - Fin de Trento y Bases del Calendario -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'hitos') && (selectedPope === 'todos' || selectedPope === 'pio_iv')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1563</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">Pío IV</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-amber-500 border-4 border-white shadow ring-2 ring-amber-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1563</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">Pío IV</span>
                            </div>
                            <span class="text-xs font-bold text-amber-700 bg-amber-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">👑 Hito Histórico</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Conclusión del Concilio de Trento</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Pío IV clausura formalmente el concilio. Este evento reorganiza las estructuras eclesiásticas y establece las bases conceptuales que requerirán una profunda reforma astronómica del calendario civil (el futuro calendario gregoriano de 1582, ideado en parte en este periodo por matemáticos apoyados por Pío IV).
                            </p>
                        </div>
                    </div>

                    <!-- Node 11: 1605 - León XI -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'hitos') && (selectedPope === 'todos' || selectedPope === 'leon_xi')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1605</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">León XI</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-amber-500 border-4 border-white shadow ring-2 ring-amber-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1605</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">León XI</span>
                            </div>
                            <span class="text-xs font-bold text-amber-700 bg-amber-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">👑 Hito Histórico</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">León XI: El "Papa Relámpago" de los Médici</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                Alessandro Ottaviano de' Medici es coronado Papa, pero enferma y fallece a los 26 días de su elección. Marca el final definitivo de la dominación dinástica directa de los Médici sobre el solio pontificio romano.
                            </p>
                        </div>
                    </div>

                    <!-- Node 12: 1605 - Galileo y el Preludio del Telescopio -->
                    <div 
                        x-show="(activeFilter === 'all' || activeFilter === 'innovaciones') && (selectedPope === 'todos' || selectedPope === 'leon_xi')"
                        class="relative group transition-all"
                    >
                        <div class="hidden md:block absolute -left-44 top-1.5 text-right w-32">
                            <span class="font-serif text-2xl font-black text-vatican-800">1605</span>
                            <span class="block text-[10px] text-vatican-500 font-bold tracking-widest uppercase">León XI</span>
                        </div>
                        <div class="absolute -left-[31px] md:-left-[39px] top-1.5 w-4 h-4 rounded-full bg-teal-500 border-4 border-white shadow ring-2 ring-teal-400 group-hover:scale-125 transition-transform"></div>
                        
                        <div class="bg-vatican-50/50 hover:bg-white p-5 rounded-xl border border-vatican-200/60 shadow-sm transition-all duration-300">
                            <div class="md:hidden flex items-center justify-between mb-2">
                                <span class="font-serif text-lg font-bold text-vatican-800">1605</span>
                                <span class="text-xs bg-vatican-200 px-2 py-0.5 rounded text-vatican-700">León XI</span>
                            </div>
                            <span class="text-xs font-bold text-teal-700 bg-teal-50 px-2.5 py-1 rounded-md uppercase tracking-wider mb-2 inline-block">⚙️ Innovación y Ciencia</span>
                            <h4 class="font-serif text-lg font-bold text-vatican-800 mt-1">Física de Caída Libre e Instrumentación Óptica Pre-Telescópica</h4>
                            <p class="text-gray-600 text-sm mt-2 font-light">
                                En este mismo año de 1605, Galileo Galilei (quien contaba con el patronazgo de la corte Médici de Toscana) comienza a refinar sus experimentos sobre planos inclinados y caída libre, así como la fabricación de lupas y binoculares primitivos que le llevarían en 1609 a la construcción de su famoso telescopio astronómico.
                            </p>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- SECTION 3: Deep Dive into Scientific Innovations of the Medici Era -->
        <section class="mb-12">
            <h2 class="font-serif text-2xl md:text-3xl text-center text-vatican-800 mb-2">Las Innovaciones Tecnológicas más Relevantes de este Periodo</h2>
            <p class="text-center text-gray-600 text-sm md:text-base max-w-xl mx-auto mb-10">Análisis pormenorizado del salto tecnológico bajo el mecenazgo de los Papas Médici.</p>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Card 1 -->
                <div class="bg-white p-6 rounded-xl shadow-md border-t-4 border-teal-500">
                    <div class="w-12 h-12 rounded-lg bg-teal-50 flex items-center justify-center text-teal-600 text-2xl font-bold mb-4">☀️</div>
                    <h3 class="font-serif text-lg font-bold text-vatican-800 mb-2">Heliocentrismo Vaticano</h3>
                    <p class="text-sm text-gray-600 leading-relaxed font-light">
                        Lejos del posterior conflicto con Galileo, la teoría heliocéntrica original de Copérnico fue presentada en el Vaticano en 1533 con el apoyo del Papa Clemente VII. Este beneplácito preliminar motivó a científicos como el cardenal Schönberg a escribir a Copérnico instándolo formalmente a divulgar libremente su trabajo.
                    </p>
                </div>

                <!-- Card 2 -->
                <div class="bg-white p-6 rounded-xl shadow-md border-t-4 border-amber-500">
                    <div class="w-12 h-12 rounded-lg bg-amber-50 flex items-center justify-center text-amber-600 text-2xl font-bold mb-4">🛡️</div>
                    <h3 class="font-serif text-lg font-bold text-vatican-800 mb-2">Ingeniería Balística y "Traza Italiana"</h3>
                    <p class="text-sm text-gray-600 leading-relaxed font-light">
                        A medida que las piezas de artillería de pólvora se volvían más potentes durante los reinados de León X y Clemente VII, la arquitectura defensiva cambió para siempre. La transición a murallas inclinadas y baluartes poligonales (fortalezas estrelladas) requirió geometría aplicada de altísima precisión.
                    </p>
                </div>

                <!-- Card 3 -->
                <div class="bg-white p-6 rounded-xl shadow-md border-t-4 border-vatican-500">
                    <div class="w-12 h-12 rounded-lg bg-vatican-50 flex items-center justify-center text-vatican-500 text-2xl font-bold mb-4">📖</div>
                    <h3 class="font-serif text-lg font-bold text-vatican-800 mb-2">Imprenta Científica de Tipos</h3>
                    <p class="text-sm text-gray-600 leading-relaxed font-light">
                        El apoyo incondicional de León X al establecimiento de imprentas multilingües (griego clásico, árabe, hebreo) posibilitó la estandarización y reproducción fiel de textos de geografía (como la Geografía de Ptolomeo) y de medicina anatómica helénica, sirviendo de base directa para la revolución del método científico.
                    </p>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-vatican-900 text-vatican-300 py-12 px-6 text-center border-t border-vatican-800">
        <div class="max-w-4xl mx-auto">
            <h2 class="font-serif text-lg text-vatican-200 mb-3">La Alianza entre el Trono de Pedro y el Intelecto del Renacimiento</h2>
            <p class="text-xs md:text-sm text-vatican-400 font-light max-w-2xl mx-auto mb-6">
                El periodo de los papas Médici es testigo de una de las mayores encrucijadas de la humanidad: donde las viejas estructuras místicas medievales coincidieron con los descubrimientos modernos de la astronomía, física e imprenta.
            </p>
            <div class="h-[1px] w-20 bg-vatican-500 mx-auto mb-6"></div>
            <p class="text-xs text-vatican-500">© 2026 — Infografía Histórica Interactiva. Diseñado con rigor histórico.</p>
        </div>
    </footer>

</body>
</html>
