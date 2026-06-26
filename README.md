# ```html
<!DOCTYPE html>
<html lang="fr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FIFO.CAREER — Plateforme Premium d'Accès aux Carrières en Australie</title>
    
    <!-- Polices Officielles V3 : Sora (Titres) & Inter (Texte) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@100..900&family=Sora:wght@400;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS pour un Design System Robuste -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- GSAP (GreenSock) & ScrollTrigger pour des animations d'une fluidité absolue -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <!-- Configuration du Design System Premium V3 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        fifoBg: '#0F1115',
                        fifoSurface: '#171A21',
                        fifoCard: '#1D212B',
                        fifoBorder: '#242A36',
                        fifoPrimary: {
                            DEFAULT: '#0F766E',
                            hover: '#115E59'
                        },
                        fifoAccent: {
                            DEFAULT: '#D97706',
                            hover: '#B45309'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        title: ['Sora', 'sans-serif']
                    },
                    borderRadius: {
                        '3xl': '1.5rem',
                        '4xl': '2rem'
                    }
                }
            }
        }
    </script>

    <style type="text/css">
        body {
            background-color: #0F1115;
            color: #F4F5F7;
            font-family: 'Inter', sans-serif;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4, .font-title {
            font-family: 'Sora', sans-serif;
        }

        /* Effet soft border glow type Magic UI / Aceternity UI */
        .premium-glow {
            position: relative;
        }
        .premium-glow::before {
            content: '';
            position: absolute;
            inset: 0;
            border-radius: 1.5rem;
            padding: 1px;
            background: linear-gradient(to bottom, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.01));
            -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: xor;
            mask-composite: exclude;
            pointer-events: none;
            z-index: 2;
        }

        /* Lueur d'arrière-plan immersive */
        .glow-radial {
            background: radial-gradient(circle at 50% 50%, rgba(15, 118, 110, 0.12) 0%, rgba(15, 11, 21, 0) 70%);
        }

        /* Glassmorphism haute définition */
        .glassmorphism {
            background: rgba(23, 26, 33, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.03);
        }

        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0F1115;
        }
        ::-webkit-scrollbar-thumb {
            background: #242A36;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #0F766E;
        }

        /* Animation d'impulsion pour le bouton flottant */
        @keyframes pulse-whatsapp {
            0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.4); }
            70% { box-shadow: 0 0 0 15px rgba(37, 211, 102, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }
        .animate-pulse-wa {
            animation: pulse-whatsapp 2s infinite;
        }

        /* Custom Video controls hover overlays */
        .video-container:hover .play-btn-overlay {
            opacity: 1;
            transform: translate(-55%, -55%) scale(1.05);
        }
    </style>
</head>
<body class="antialiased selection:bg-teal-700 selection:text-white">

    <!-- LUMIÈRE RADIALE D'AMBIANCE HAUT DE GAMME -->
    <div class="fixed top-0 left-1/2 -translate-x-1/2 w-[1100px] h-[700px] glow-radial pointer-events-none z-0"></div>

    <!-- NAVIGATION PREMIUM INTERACTIVE -->
    <header class="sticky top-0 z-50 glassmorphism transition-all duration-300">
        <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <span class="text-2xl font-extrabold tracking-tight text-white font-title">FIFO<span class="text-fifoAccent">.</span>CAREER</span>
                <span class="text-[9px] uppercase tracking-widest bg-white/5 border border-white/10 px-2.5 py-1 rounded-full text-zinc-400 font-semibold">V3 Institutional</span>
            </div>
            <nav class="hidden md:flex items-center gap-8 text-sm font-medium text-zinc-400">
                <a href="#chiffres" class="hover:text-white transition-colors duration-300">Indicateurs</a>
                <a href="#pourquoi" class="hover:text-white transition-colors duration-300">Perspectives</a>
                <a href="#vie" class="hover:text-white transition-colors duration-300">Vie sur Site</a>
                <a href="#temoignages" class="hover:text-white transition-colors duration-300">Témoignages</a>
                <a href="#faq" class="hover:text-white transition-colors duration-300">FAQ</a>
            </nav>
            <div>
                <button onclick="openModal()" class="inline-flex items-center justify-center bg-fifoPrimary text-white text-sm font-semibold h-11 px-6 rounded-full hover:bg-fifoPrimary-hover transition-all duration-300 shadow-lg shadow-fifoPrimary/15 hover:shadow-fifoPrimary/30 transform hover:-translate-y-0.5">
                    Accéder à la plateforme
                </button>
            </div>
        </div>
    </header>

    <!-- HERO SECTION (VIDÉO PLEIN ÉCRAN & UNIQUE CTA) -->
    <section class="relative min-h-[calc(100vh-80px)] flex items-center justify-center overflow-hidden py-16 md:py-24 z-10">
        <!-- Arrière-plan vidéo hautement immersif et asymétrique -->
        <div class="absolute inset-0 z-0">
            <video class="w-full h-full object-cover opacity-20 filter brightness-50 contrast-125" autoplay loop muted playsinline poster="1000608677.jpg">
                <source src="VID_20260618_114353_169.mp4" type="video/mp4">
            </video>
            <div class="absolute inset-0 bg-gradient-to-t from-fifoBg via-fifoBg/70 to-transparent"></div>
            <div class="absolute inset-0 bg-gradient-to-r from-fifoBg/95 via-transparent to-fifoBg/40"></div>
        </div>

        <div class="relative z-10 max-w-5xl mx-auto px-6 text-center" id="hero-content">
            <div class="inline-flex items-center gap-2 bg-fifoSurface border border-white/10 px-4 py-1.5 rounded-full text-xs font-semibold text-fifoAccent mb-8 shadow-2xl">
                <span class="w-1.5 h-1.5 rounded-full bg-fifoAccent animate-pulse"></span>
                Campagne d'intégration Hub Australie 2026
            </div>
            
            <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-extrabold text-white tracking-tight leading-[1.12] mb-8 font-title">
                Déployez votre expertise sur les plus grands <span class="text-transparent bg-clip-text bg-gradient-to-r from-teal-400 to-amber-500">projets industriels</span> d'Australie.
            </h1>
            
            <p class="text-base sm:text-lg md:text-xl text-zinc-400 max-w-3xl mx-auto mb-12 font-light leading-relaxed">
                Accédez de manière sécurisée et encadrée aux opportunités de carrières techniques en formule FIFO. Rémunérations d'excellence, logistique résidentielle entièrement prise en charge et ingénierie de visa intégrale.
            </p>

            <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                <button onclick="openModal()" class="w-full sm:w-auto inline-flex items-center justify-center bg-fifoPrimary text-white font-semibold h-14 px-8 rounded-full hover:bg-fifoPrimary-hover transition-all duration-300 text-base shadow-xl shadow-fifoPrimary/20 transform hover:-translate-y-0.5 group">
                    Initier mon évaluation de profil
                    <i data-lucide="arrow-right" class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300"></i>
                </button>
            </div>
        </div>
        
        <!-- Indicateur de scroll minimaliste -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 z-10 animate-bounce opacity-40">
            <i data-lucide="chevron-down" class="w-6 h-6 text-white"></i>
        </div>
    </section>

    <!-- SECTION CHIFFRES CLÉS (BENTO GRID STYLE SHADCN) -->
    <section id="chiffres" class="py-24 md:py-32 border-y border-white/5 bg-fifoSurface/30 relative z-10">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6" id="chiffres-grid">
                
                <div class="premium-glow bg-fifoCard p-8 rounded-3xl border border-white/[0.02] flex flex-col justify-between min-h-[220px] transition-all duration-500 hover:border-white/10 hover:translate-y-[-4px]">
                    <div>
                        <div class="p-3 rounded-2xl bg-fifoPrimary/10 text-fifoPrimary inline-block mb-4">
                            <i data-lucide="banknote" class="w-6 h-6"></i>
                        </div>
                        <p class="text-xs font-semibold text-zinc-400 uppercase tracking-widest font-title">Barème Opérationnel</p>
                    </div>
                    <div class="mt-4">
                        <span class="text-3xl font-bold text-white tracking-tight">35$ à 65$+ / h</span>
                        <p class="text-xs text-zinc-500 mt-1">Taux ajustés selon vos qualifications et certifications</p>
                    </div>
                </div>

                <div class="premium-glow bg-fifoCard p-8 rounded-3xl border border-white/[0.02] flex flex-col justify-between min-h-[220px] transition-all duration-500 hover:border-white/10 hover:translate-y-[-4px]">
                    <div>
                        <div class="p-3 rounded-2xl bg-amber-500/10 text-fifoAccent inline-block mb-4">
                            <i data-lucide="clock" class="w-6 h-6"></i>
                        </div>
                        <p class="text-xs font-semibold text-zinc-400 uppercase tracking-widest font-title">Volume d'Engagement</p>
                    </div>
                    <div class="mt-4">
                        <span class="text-3xl font-bold text-white tracking-tight">Jusqu'à 12h / jour</span>
                        <p class="text-xs text-zinc-500 mt-1">Planification des heures optimisée pour maximiser l'épargne</p>
                    </div>
                </div>

                <div class="premium-glow bg-fifoCard p-8 rounded-3xl border border-white/[0.02] flex flex-col justify-between min-h-[220px] transition-all duration-500 hover:border-white/10 hover:translate-y-[-4px]">
                    <div>
                        <div class="p-3 rounded-2xl bg-emerald-500/10 text-emerald-400 inline-block mb-4">
                            <i data-lucide="shield-check" class="w-6 h-6"></i>
                        </div>
                        <p class="text-xs font-semibold text-zinc-400 uppercase tracking-widest font-title">Logistique sur Site</p>
                    </div>
                    <div class="mt-4">
                        <span class="text-3xl font-bold text-white tracking-tight">100% Pris en Charge</span>
                        <p class="text-xs text-zinc-500 mt-1">Hébergement en village privé, restauration et navettes</p>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- POURQUOI L'AUSTRALIE (VALEURS & TRANSPARENCE) -->
    <section id="pourquoi" class="py-24 md:py-32 relative z-10">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-16 items-center">
                <div class="lg:col-span-5 space-y-6" id="pourquoi-left">
                    <span class="text-xs font-bold text-fifoPrimary uppercase tracking-widest block font-title">Perspectives</span>
                    <h2 class="text-3xl sm:text-4xl font-bold text-white tracking-tight leading-tight font-title">Un écosystème industriel d'envergure mondiale.</h2>
                    <p class="text-zinc-400 font-light leading-relaxed">
                        Le modèle industriel du Fly-In Fly-Out (FIFO) en Australie offre un cadre rigoureux, sécurisé et extrêmement gratifiant. Notre plateforme collabore exclusivement avec des acteurs majeurs engagés pour la sécurité et la valorisation des compétences internationales.
                    </p>
                    <div class="space-y-4 pt-2">
                        <div class="flex items-start gap-3">
                            <div class="mt-1 p-1 rounded-md bg-fifoPrimary/10 text-fifoPrimary">
                                <i data-lucide="check" class="w-4 h-4"></i>
                            </div>
                            <p class="text-sm text-zinc-300 font-medium">Reconnaissance et passerelles pour vos compétences métiers.</p>
                        </div>
                        <div class="flex items-start gap-3">
                            <div class="mt-1 p-1 rounded-md bg-fifoPrimary/10 text-fifoPrimary">
                                <i data-lucide="check" class="w-4 h-4"></i>
                            </div>
                            <p class="text-sm text-zinc-300 font-medium">Protocoles HSE stricts alignés sur les plus hauts standards mondiaux.</p>
                        </div>
                    </div>
                </div>
                
                <div class="lg:col-span-7 grid grid-cols-1 sm:grid-cols-2 gap-6" id="pourquoi-right">
                    <div class="premium-glow bg-fifoSurface p-8 rounded-3xl border border-white/5 transition-all duration-300 hover:border-white/10">
                        <h3 class="text-lg font-semibold text-white mb-3 font-title">Épargne Optimisée</h3>
                        <p class="text-sm text-zinc-400 font-light leading-relaxed">Puisque l'intégralité des coûts de vie sur place est couverte, vos revenus se transforment directement en capacité d'épargne nette.</p>
                    </div>
                    <div class="premium-glow bg-fifoSurface p-8 rounded-3xl border border-white/5 transition-all duration-300 hover:border-white/10">
                        <h3 class="text-lg font-semibold text-white mb-3 font-title">Sponsorship & Accès</h3>
                        <p class="text-sm text-zinc-400 font-light leading-relaxed">Nous vous guidons à travers les dispositifs légaux d'immigration pour sécuriser votre statut de travailleur en toute conformité.</p>
                    </div>
                    <div class="premium-glow bg-fifoSurface p-8 rounded-3xl border border-white/5 relative overflow-hidden sm:col-span-2 group">
                        <img src="1000608676.jpg" alt="Équipes de terrain en Australie" class="absolute inset-0 w-full h-full object-cover opacity-10 group-hover:scale-102 transition-transform duration-700 pointer-events-none">
                        <div class="relative z-10">
                            <h3 class="text-lg font-semibold text-white mb-3 font-title">Rythme de Rotation (Rosters)</h3>
                            <p class="text-sm text-zinc-400 font-light leading-relaxed">Les structures de roulement vous permettent d'alterner efficacement phases opérationnelles intenses et périodes de récupération complètes pour découvrir l'Australie.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- VIE SUR SITE (GALERIE PREMIUM MEDIAS LOCAUX) -->
    <section id="vie" class="py-24 md:py-32 bg-fifoSurface/20 border-t border-white/5 relative z-10">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-16 gap-6" id="vie-head">
                <div>
                    <span class="text-xs font-bold text-fifoAccent uppercase tracking-widest block mb-3 font-title">Immersion</span>
                    <h2 class="text-3xl sm:text-4xl font-bold text-white tracking-tight font-title">Infrastructures des Villages Résidentiels</h2>
                </div>
                <p class="text-zinc-400 font-light max-w-md text-sm md:text-base">
                    Découvrez la réalité des espaces de vie modernes mis à disposition durant vos périodes de mission.
                </p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6" id="vie-grid">
                
                <div class="group relative overflow-hidden rounded-3xl bg-fifoCard border border-white/5 aspect-[3/4] transition-all duration-500 hover:translate-y-[-4px]">
                    <img src="1000608675.jpg" alt="Village résidentiel" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy">
                    <div class="absolute inset-0 bg-gradient-to-t from-fifoBg via-fifoBg/30 to-transparent flex flex-col justify-end p-6">
                        <span class="text-xs font-semibold text-fifoAccent mb-1">Hébergement</span>
                        <h4 class="text-base font-bold text-white font-title">Complexes Modernes</h4>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-3xl bg-fifoCard border border-white/5 aspect-[3/4] transition-all duration-500 hover:translate-y-[-4px]">
                    <img src="1000608678.jpg" alt="Restauration commune" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy">
                    <div class="absolute inset-0 bg-gradient-to-t from-fifoBg via-fifoBg/30 to-transparent flex flex-col justify-end p-6">
                        <span class="text-xs font-semibold text-fifoAccent mb-1">Restauration</span>
                        <h4 class="text-base font-bold text-white font-title">Services Nutritifs</h4>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-3xl bg-fifoCard border border-white/5 aspect-[3/4] transition-all duration-500 hover:translate-y-[-4px]">
                    <img src="1000608679.jpg" alt="Personnel technique" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy">
                    <div class="absolute inset-0 bg-gradient-to-t from-fifoBg via-fifoBg/30 to-transparent flex flex-col justify-end p-6">
                        <span class="text-xs font-semibold text-fifoAccent mb-1">Équipes</span>
                        <h4 class="text-base font-bold text-white font-title">Synergies Métiers</h4>
                    </div>
                </div>

                <div class="group relative overflow-hidden rounded-3xl bg-fifoCard border border-white/5 aspect-[3/4] transition-all du