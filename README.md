## Hi there 👋

<!--
**mOOnMeridian/mOOnMeridian** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>mOOnMeridian // Chandan Kumar - Portfolio</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;800;900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        onyx: '#090b10',
                        deepSpace: '#0d111a',
                        cyberCyan: '#00f0ff',
                        electricPurple: '#a855f7',
                        amberGold: '#f59e0b',
                        surfaceCard: '#131926'
                    },
                    fontFamily: {
                        orbitron: ['Orbitron', 'sans-serif'],
                        sans: ['Plus Jakarta Sans', 'sans-serif']
                    },
                    boxShadow: {
                        cyanGlow: '0 0 25px rgba(0, 240, 255, 0.35)',
                        purpleGlow: '0 0 25px rgba(168, 85, 247, 0.35)',
                        amberGlow: '0 0 25px rgba(245, 158, 11, 0.35)'
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Custom Scrollbar & Futuristic Effects */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #090b10;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #00f0ff;
        }

        .glow-text-cyan {
            text-shadow: 0 0 12px rgba(0, 240, 255, 0.6);
        }
        .glow-text-purple {
            text-shadow: 0 0 12px rgba(168, 85, 247, 0.6);
        }

        .glass-panel {
            background: rgba(19, 25, 38, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .glass-card {
            background: rgba(22, 30, 46, 0.6);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(0, 240, 255, 0.12);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .glass-card:hover {
            border-color: rgba(0, 240, 255, 0.5);
            box-shadow: 0 10px 30px -10px rgba(0, 240, 255, 0.25);
            transform: translateY(-4px);
        }

        /* Pulse Orbit Effect */
        @keyframes orbitPulse {
            0%, 100% { transform: rotate(0deg) scale(1); opacity: 0.8; }
            50% { transform: rotate(180deg) scale(1.1); opacity: 1; }
        }

        .orbit-ring {
            animation: orbitPulse 12s linear infinite;
        }

        /* Scanline animation overlay for cinematic feel */
        .scanlines {
            background: linear-gradient(
                rgba(18, 16, 16, 0) 50%, 
                rgba(0, 0, 0, 0.25) 50%
            ), linear-gradient(
                90deg,
                rgba(255, 0, 0, 0.03),
                rgba(0, 255, 0, 0.01),
                rgba(0, 0, 255, 0.03)
            );
            background-size: 100% 4px, 6px 100%;
            pointer-events: none;
        }
    </style>
</head>
<body class="bg-onyx text-slate-200 font-sans selection:bg-cyberCyan selection:text-black overflow-x-hidden relative">

    <!-- Interactive Canvas Background -->
    <canvas id="starfield" class="fixed top-0 left-0 w-full h-full pointer-events-none z-0"></canvas>
    
    <!-- Retro Scanline Overlay for Hollywood Cyber Vibe -->
    <div class="fixed inset-0 scanlines z-10 opacity-40 pointer-events-none"></div>

    <!-- MAIN CONTAINER -->
    <div class="relative z-20 flex flex-col min-h-screen">

        <!-- ================= 1. HEADER / NAVIGATION ================= -->
        <header class="sticky top-0 z-50 glass-panel border-b border-slate-800/80">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
                
                <!-- Brand Logo -->
                <a href="#" class="flex items-center gap-3 group">
                    <div class="relative w-10 h-10 flex items-center justify-center">
                        <div class="absolute inset-0 rounded-full border border-cyberCyan/50 orbit-ring"></div>
                        <div class="absolute inset-1 rounded-full border border-electricPurple/60 border-dashed"></div>
                        <i class="fa-solid fa-moon text-cyberCyan text-lg group-hover:scale-110 transition-transform"></i>
                    </div>
                    <div>
                        <span class="font-orbitron font-extrabold text-xl tracking-wider text-white">mOOn<span class="text-cyberCyan">Meridian</span></span>
                        <span class="block text-[10px] font-mono tracking-widest text-slate-400 uppercase">Chandan Kumar</span>
                    </div>
                </a>

                <!-- Desktop Quick Nav -->
                <nav class="hidden md:flex items-center space-x-8 font-medium text-sm tracking-wide">
                    <a href="#intro" class="text-slate-300 hover:text-cyberCyan transition-colors">Intro</a>
                    <a href="#skills" class="text-slate-300 hover:text-cyberCyan transition-colors">Core Matrix</a>
                    <a href="#analytics" class="text-slate-300 hover:text-cyberCyan transition-colors">Impact Analytics</a>
                    <a href="#experience" class="text-slate-300 hover:text-cyberCyan transition-colors">Experience</a>
                    <a href="#contact" class="text-slate-300 hover:text-cyberCyan transition-colors">Contact</a>
                </nav>

                <!-- Header Actions -->
                <div class="flex items-center gap-4">
                    <a href="#contact" class="hidden sm:inline-flex items-center gap-2 px-5 py-2.5 rounded-full text-xs font-orbitron font-semibold tracking-wider text-black bg-cyberCyan hover:bg-white transition-all shadow-cyanGlow transform hover:-translate-y-0.5">
                        <i class="fa-solid fa-bolt"></i> CONNECT LIVE
                    </a>

                    <!-- Mobile Menu Toggle Button -->
                    <button id="mobileMenuBtn" class="md:hidden text-slate-300 hover:text-white p-2">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>

            <!-- Mobile Dropdown Menu -->
            <div id="mobileMenu" class="hidden md:hidden glass-panel border-b border-slate-800 px-6 py-4 flex-col space-y-3">
                <a href="#intro" class="text-slate-200 hover:text-cyberCyan py-1">Intro</a>
                <a href="#skills" class="text-slate-200 hover:text-cyberCyan py-1">Core Matrix</a>
                <a href="#analytics" class="text-slate-200 hover:text-cyberCyan py-1">Impact Analytics</a>
                <a href="#experience" class="text-slate-200 hover:text-cyberCyan py-1">Experience</a>
                <a href="#contact" class="text-slate-200 hover:text-cyberCyan py-1">Contact</a>
                <a href="#contact" class="inline-block text-center mt-2 px-5 py-2 rounded-full text-xs font-orbitron font-semibold text-black bg-cyberCyan">CONNECT LIVE</a>
            </div>
        </header>

        <main class="flex-grow">

            <!-- ================= 2. HERO SECTION ================= -->
            <section id="intro" class="relative min-h-[90vh] flex items-center justify-center py-20 px-4 sm:px-6 lg:px-8 overflow-hidden">
                <!-- Ambient Glow Background Spheres -->
                <div class="absolute top-1/4 left-1/2 -translate-x-1/2 w-96 h-96 bg-cyberCyan/10 rounded-full blur-3xl pointer-events-none"></div>
                <div class="absolute bottom-10 right-10 w-80 h-80 bg-electricPurple/10 rounded-full blur-3xl pointer-events-none"></div>

                <div class="max-w-5xl mx-auto text-center relative z-10">
                    
                    <!-- Subhead Badge -->
                    <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-cyberCyan/30 bg-cyberCyan/10 text-cyberCyan text-xs font-mono tracking-widest uppercase mb-8 shadow-cyanGlow">
                        <span class="w-2 h-2 rounded-full bg-cyberCyan animate-ping"></span>
                        Digital Account Management & Client Success Specialist
                    </div>

                    <!-- Main Headline -->
                    <h1 class="text-4xl sm:text-6xl md:text-7xl font-orbitron font-black text-white tracking-tight leading-none mb-6">
                        CHANDAN KUMAR
                        <span class="block text-transparent bg-clip-text bg-gradient-to-r from-cyberCyan via-electricPurple to-amberGold mt-2">
                            // mOOnMeridian
                        </span>
                    </h1>

                    <!-- Tagline -->
                    <p class="text-lg sm:text-xl text-slate-300 max-w-3xl mx-auto font-light leading-relaxed mb-12">
                        Account Manager & Client Relationship Architect with <span class="text-cyberCyan font-semibold">3.8+ years</span> driving strategic retention, service upselling, and executing high-impact digital personal branding campaigns.
                    </p>

                    <!-- Dynamic Metrics Counter Cards (Hollywood Blockbuster Style) -->
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-12">
                        <div class="glass-card p-5 rounded-2xl text-center">
                            <div class="font-orbitron font-bold text-3xl sm:text-4xl text-cyberCyan glow-text-cyan count-up" data-target="50">0</div>
                            <div class="text-xs font-mono text-slate-400 uppercase mt-2">Enterprise Accounts</div>
                        </div>

                        <div class="glass-card p-5 rounded-2xl text-center">
                            <div class="font-orbitron font-bold text-3xl sm:text-4xl text-electricPurple glow-text-purple"><span class="count-up" data-target="80">0</span>%</div>
                            <div class="text-xs font-mono text-slate-400 uppercase mt-2">LinkedIn Visibility Uplift</div>
                        </div>

                        <div class="glass-card p-5 rounded-2xl text-center">
                            <div class="font-orbitron font-bold text-3xl sm:text-4xl text-amberGold"><span class="count-up" data-target="96">0</span>%</div>
                            <div class="text-xs font-mono text-slate-400 uppercase mt-2">SLA Issue Resolution</div>
                        </div>

                        <div class="glass-card p-5 rounded-2xl text-center">
                            <div class="font-orbitron font-bold text-3xl sm:text-4xl text-white"><span class="count-up" data-target="3">0</span>.8+</div>
                            <div class="text-xs font-mono text-slate-400 uppercase mt-2">Years Strategic Impact</div>
                        </div>
                    </div>

                    <!-- CTA Group -->
                    <div class="flex flex-wrap items-center justify-center gap-4">
                        <a href="#skills" class="px-8 py-4 rounded-xl font-orbitron font-bold text-sm tracking-wider text-black bg-cyberCyan hover:bg-white transition-all shadow-cyanGlow flex items-center gap-3">
                            EXPLORE STRATEGY MATRIX <i class="fa-solid fa-arrow-right"></i>
                        </a>
                        <a href="#contact" class="px-8 py-4 rounded-xl font-orbitron font-bold text-sm tracking-wider text-white glass-panel hover:bg-slate-800 border border-slate-700 transition-all flex items-center gap-3">
                            <i class="fa-solid fa-paper-plane text-electricPurple"></i> INITIATE CONTACT
                        </a>
                    </div>
                </div>
            </section>

            <!-- ================= 3. CORE MATRIX / SKILLS RADAR ================= -->
            <section id="skills" class="py-24 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-xs font-mono tracking-widest text-cyberCyan uppercase mb-2">// CAPABILITY INFRASTRUCTURE</h2>
                    <h3 class="text-3xl sm:text-4xl font-orbitron font-bold text-white">CORE SKILLS MATRIX</h3>
                </div>

                <!-- Skill Filter Tabs -->
                <div class="flex flex-wrap justify-center gap-3 mb-12" id="skillTabs">
                    <button data-category="all" class="skill-tab active px-5 py-2.5 rounded-full text-xs font-orbitron font-semibold tracking-wider bg-cyberCyan text-black shadow-cyanGlow transition-all">
                        ALL CAPABILITIES
                    </button>
                    <button data-category="management" class="skill-tab px-5 py-2.5 rounded-full text-xs font-orbitron font-semibold tracking-wider glass-panel text-slate-300 hover:text-white border border-slate-700 transition-all">
                        CLIENT & STAKEHOLDER MANAGEMENT
                    </button>
                    <button data-category="renewals" class="skill-tab px-5 py-2.5 rounded-full text-xs font-orbitron font-semibold tracking-wider glass-panel text-slate-300 hover:text-white border border-slate-700 transition-all">
                        RENEWALS & GROWTH
                    </button>
                    <button data-category="digital" class="skill-tab px-5 py-2.5 rounded-full text-xs font-orbitron font-semibold tracking-wider glass-panel text-slate-300 hover:text-white border border-slate-700 transition-all">
                        DIGITAL MEDIA & LINKEDIN SEO
                    </button>
                    <button data-category="tools" class="skill-tab px-5 py-2.5 rounded-full text-xs font-orbitron font-semibold tracking-wider glass-panel text-slate-300 hover:text-white border border-slate-700 transition-all">
                        TOOLS & PLATFORMS
                    </button>
                </div>

                <!-- Skill Cards Grid -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6" id="skillsGrid">
                    
                    <!-- Card 1 -->
                    <div class="glass-card p-6 rounded-2xl skill-item" data-category="management">
                        <div class="w-12 h-12 rounded-xl bg-cyberCyan/10 border border-cyberCyan/30 flex items-center justify-center text-cyberCyan mb-4 text-xl">
                            <i class="fa-solid fa-users-gear"></i>
                        </div>
                        <h4 class="font-orbitron font-semibold text-lg text-white mb-2">Account Ownership</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Serving as the primary strategic point of contact for 50+ enterprise client accounts, maintaining seamless lifecycle engagement.
                        </p>
                    </div>

                    <!-- Card 2 -->
                    <div class="glass-card p-6 rounded-2xl skill-item" data-category="digital">
                        <div class="w-12 h-12 rounded-xl bg-electricPurple/10 border border-electricPurple/30 flex items-center justify-center text-electricPurple mb-4 text-xl">
                            <i class="fa-brands fa-linkedin"></i>
                        </div>
                        <h4 class="font-orbitron font-semibold text-lg text-white mb-2">LinkedIn Visibility & SEO</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Crafting tailored content strategies, keyword optimization, and networking pushes that yield an 80% spike in search impressions.
                        </p>
                    </div>

                    <!-- Card 3 -->
                    <div class="glass-card p-6 rounded-2xl skill-item" data-category="renewals">
                        <div class="w-12 h-12 rounded-xl bg-amberGold/10 border border-amberGold/30 flex items-center justify-center text-amberGold mb-4 text-xl">
                            <i class="fa-solid fa-chart-line"></i>
                        </div>
                        <h4 class="font-orbitron font-semibold text-lg text-white mb-2">Renewals & Upselling</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Consultative needs assessment to identify expansion opportunities, driving client retention and upsell conversions.
                        </p>
                    </div>

                    <!-- Card 4 -->
                    <div class="glass-card p-6 rounded-2xl skill-item" data-category="management">
                        <div class="w-12 h-12 rounded-xl bg-cyberCyan/10 border border-cyberCyan/30 flex items-center justify-center text-cyberCyan mb-4 text-xl">
                            <i class="fa-solid fa-headset"></i>
                        </div>
                        <h4 class="font-orbitron font-semibold text-lg text-white mb-2">SLA & Issue Escalation</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Cross-functional issue resolution maintaining a 96% success rate within 24 to 72 business hours.
                        </p>
                    </div>

                    <!-- Card 5 -->
                    <div class="glass-card p-6 rounded-2xl skill-item" data-category="digital">
                        <div class="w-12 h-12 rounded-xl bg-electricPurple/10 border border-electricPurple/30 flex items-center justify-center text-electricPurple mb-4 text-xl">
                            <i class="fa-solid fa-briefcase"></i>
                        </div>
                        <h4 class="font-orbitron font-semibold text-lg text-white mb-2">Job Board Management</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Optimization and management across key career portals including Naukri, Foundit, Shine, and international job engines.
                        </p>
                    </div>

                    <!-- Card 6 -->
                    <div class="glass-card p-6 rounded-2xl skill-item" data-category="tools">
                        <div class="w-12 h-12 rounded-xl bg-amberGold/10 border border-amberGold/30 flex items-center justify-center text-amberGold mb-4 text-xl">
                            <i class="fa-solid fa-file-excel"></i>
                        </div>
                        <h4 class="font-orbitron font-semibold text-lg text-white mb-2">Analytics & Reporting</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Advanced performance tracking via MS Excel, Google Sheets, PowerPoint EOD updates, and activity dashboards.
                        </p>
                    </div>

                </div>
            </section>

            <!-- ================= 4. INTERACTIVE IMPACT ANALYTICS SIMULATOR ================= -->
            <section id="analytics" class="py-20 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
                <div class="glass-panel rounded-3xl p-6 sm:p-10 border border-cyberCyan/30 relative overflow-hidden">
                    <div class="flex flex-col lg:flex-row items-start lg:items-center justify-between gap-6 mb-8">
                        <div>
                            <span class="text-xs font-mono text-cyberCyan uppercase tracking-widest">// LIVE ANALYTICS ENGINE</span>
                            <h3 class="text-2xl sm:text-3xl font-orbitron font-bold text-white mt-1">CLIENT IMPACT SIMULATOR</h3>
                        </div>
                        <div class="flex items-center gap-3">
                            <button id="simToggle" class="px-4 py-2 rounded-lg bg-cyberCyan/20 hover:bg-cyberCyan/30 text-cyberCyan text-xs font-mono border border-cyberCyan/40 transition-all flex items-center gap-2">
                                <i class="fa-solid fa-rotate-right"></i> RE-SIMULATE CAMPAIGN
                            </button>
                        </div>
                    </div>

                    <!-- Simulator Controls & Output -->
                    <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                        
                        <!-- Control Panel -->
                        <div class="space-y-6">
                            <div>
                                <label class="block text-xs font-mono text-slate-300 mb-2">CLIENT ACCOUNTS SCALE: <span id="accountVal" class="text-cyberCyan font-bold">50</span></label>
                                <input type="range" id="accountSlider" min="10" max="100" value="50" class="w-full accent-cyberCyan bg-slate-800 rounded-lg cursor-pointer">
                            </div>

                            <div>
                                <label class="block text-xs font-mono text-slate-300 mb-2">CAMPAIGN INTENSITY: <span id="intensityVal" class="text-electricPurple font-bold">High (80% Uplift)</span></label>
                                <select id="intensitySelect" class="w-full bg-slate-900 border border-slate-700 rounded-lg px-3 py-2 text-sm text-slate-200 focus:border-cyberCyan focus:outline-none">
                                    <option value="0.5">Standard Optimization (+50% Views)</option>
                                    <option value="0.8" selected>Aggressive Campaign (+80% Views)</option>
                                    <option value="1.2">Enterprise Surge (+120% Views)</option>
                                </select>
                            </div>

                            <div class="p-4 rounded-xl bg-slate-900/80 border border-slate-800 text-xs font-mono text-slate-400">
                                <div class="text-slate-200 font-bold mb-1"><i class="fa-solid fa-shield-halved text-cyberCyan"></i> Resolution Guarantee</div>
                                <p>SLA resolution rate consistently maintained at <span class="text-amberGold font-bold">96%</span> within 24–72 hours.</p>
                            </div>
                        </div>

                        <!-- Live Visualizing Metric Bars -->
                        <div class="lg:col-span-2 flex flex-col justify-center space-y-6 bg-slate-900/60 p-6 rounded-2xl border border-slate-800">
                            
                            <!-- Metric 1 -->
                            <div>
                                <div class="flex justify-between text-xs font-mono mb-2">
                                    <span class="text-slate-300">ESTIMATED MONTHLY PROFILE IMPRESSIONS</span>
                                    <span id="metricImpressions" class="text-cyberCyan font-bold">42,500</span>
                                </div>
                                <div class="w-full bg-slate-800 h-3 rounded-full overflow-hidden">
                                    <div id="barImpressions" class="bg-gradient-to-r from-cyberCyan to-blue-600 h-full rounded-full transition-all duration-700" style="width: 75%;"></div>
                                </div>
                            </div>

                            <!-- Metric 2 -->
                            <div>
                                <div class="flex justify-between text-xs font-mono mb-2">
                                    <span class="text-slate-300">CLIENT RETENTION INDEX</span>
                                    <span id="metricRetention" class="text-electricPurple font-bold">94%</span>
                                </div>
                                <div class="w-full bg-slate-800 h-3 rounded-full overflow-hidden">
                                    <div id="barRetention" class="bg-gradient-to-r from-electricPurple to-pink-600 h-full rounded-full transition-all duration-700" style="width: 94%;"></div>
                                </div>
                            </div>

                            <!-- Metric 3 -->
                            <div>
                                <div class="flex justify-between text-xs font-mono mb-2">
                                    <span class="text-slate-300">SLA RESOLUTION SPEED (HOURS)</span>
                                    <span id="metricSpeed" class="text-amberGold font-bold">&lt; 36 HRS AVG</span>
                                </div>
                                <div class="w-full bg-slate-800 h-3 rounded-full overflow-hidden">
                                    <div id="barSpeed" class="bg-gradient-to-r from-amberGold to-orange-600 h-full rounded-full transition-all duration-700" style="width: 88%;"></div>
                                </div>
                            </div>

                        </div>
                    </div>
                </div>
            </section>

            <!-- ================= 5. EXPERIENCE ODYSSEY (TIMELINE) ================= -->
            <section id="experience" class="py-24 px-4 sm:px-6 lg:px-8 max-w-5xl mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-xs font-mono tracking-widest text-electricPurple uppercase mb-2">// CAREER TRAJECTORY</h2>
                    <h3 class="text-3xl sm:text-4xl font-orbitron font-bold text-white">EXPERIENCE ODYSSEY</h3>
                </div>

                <div class="relative border-l-2 border-slate-800 space-y-12 pl-6 sm:pl-10 ml-4 sm:ml-8">

                    <!-- Role 1 -->
                    <div class="relative group">
                        <!-- Timeline Node -->
                        <div class="absolute -left-[31px] sm:-left-[47px] top-1 w-6 h-6 rounded-full bg-onyx border-2 border-cyberCyan flex items-center justify-center group-hover:scale-125 transition-transform shadow-cyanGlow">
                            <div class="w-2 h-2 rounded-full bg-cyberCyan"></div>
                        </div>

                        <div class="glass-card p-6 sm:p-8 rounded-2xl">
                            <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                                <span class="px-3 py-1 rounded-full bg-cyberCyan/10 border border-cyberCyan/30 text-cyberCyan text-xs font-mono">Sep 2025 – Present</span>
                                <span class="text-xs font-mono text-slate-400"><i class="fa-solid fa-location-dot"></i> Gurugram, Haryana, India</span>
                            </div>
                            <h4 class="text-xl font-orbitron font-bold text-white">Human Resources Consultant</h4>
                            <h5 class="text-sm font-semibold text-slate-300 mb-4">Avilox Jobs Gateway (OPC) Private Limited</h5>
                            <ul class="space-y-2.5 text-sm text-slate-300 font-light">
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-angle-right text-cyberCyan mt-1"></i>
                                    Partner with corporate stakeholders to align HR strategies with long-term organizational objectives.
                                </li>
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-angle-right text-cyberCyan mt-1"></i>
                                    Provide strategic consulting for high-performing team engagement and workplace optimization.
                                </li>
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-angle-right text-cyberCyan mt-1"></i>
                                    Support end-to-end talent acquisition and contract recruitment drives.
                                </li>
                            </ul>
                        </div>
                    </div>

                    <!-- Role 2 -->
                    <div class="relative group">
                        <!-- Timeline Node -->
                        <div class="absolute -left-[31px] sm:-left-[47px] top-1 w-6 h-6 rounded-full bg-onyx border-2 border-electricPurple flex items-center justify-center group-hover:scale-125 transition-transform shadow-purpleGlow">
                            <div class="w-2 h-2 rounded-full bg-electricPurple"></div>
                        </div>

                        <div class="glass-card p-6 sm:p-8 rounded-2xl">
                            <div class="flex flex-wrap items-center justify-between gap-2 mb-3">
                                <span class="px-3 py-1 rounded-full bg-electricPurple/10 border border-electricPurple/30 text-electricPurple text-xs font-mono">Jan 2025 – Present</span>
                                <span class="text-xs font-mono text-slate-400"><i class="fa-solid fa-location-dot"></i> Gurugram, Haryana, India</span>
                            </div>
                            <h4 class="text-xl font-orbitron font-bold text-white">Account Manager</h4>
                            <h5 class="text-sm font-semibold text-slate-300 mb-4">OutSpark</h5>
                            <ul class="space-y-2.5 text-sm text-slate-300 font-light">
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-angle-right text-electricPurple mt-1"></i>
                                    Directly manage 50+ client accounts across onboarding, service delivery, renewals, and retention.
                                </li>
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-angle-right text-electricPurple mt-1"></i>
                                    Execute LinkedIn visibility campaigns driving an average <span class="text-cyberCyan font-semibold">80% boost</span> in profile views & post impressions.
                                </li>
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-angle-right text-electricPurple mt-1"></i>
                                    Maintain a <span class="text-amberGold font-semibold">96% resolution rate</span> for client issues within 24 to 72 hours via End-of-Day (EOD) tracking.
                                </li>
                                <li class="flex items-start gap-2">
                                    <i class="fa-solid fa-angle-right text-electricPurple mt-1"></i>
                                    Coordinate setup across top job portals (Naukri, Foundit, Shine) to accelerate client job placements.
                                </li>
                            </ul>
                        </div>
                    </div>

                </div>
            </section>

            <!-- ================= 6. DIRECT LINE / CONTACT PORTAL ================= -->
            <section id="contact" class="py-24 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-xs font-mono tracking-widest text-cyberCyan uppercase mb-2">// DIRECT ACCESS</h2>
                    <h3 class="text-3xl sm:text-4xl font-orbitron font-bold text-white">INITIATE CONTACT</h3>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                    
                    <!-- Direct Contact Card -->
                    <div class="glass-panel p-8 rounded-3xl flex flex-col justify-between">
                        <div>
                            <h4 class="font-orbitron font-bold text-2xl text-white mb-4">Chandan Kumar</h4>
                            <p class="text-slate-400 text-sm leading-relaxed mb-8">
                                Available for strategic Account Management, Client Success Leadership, and HR Consulting opportunities.
                            </p>

                            <div class="space-y-6">
                                <div class="flex items-center gap-4">
                                    <div class="w-12 h-12 rounded-2xl bg-cyberCyan/10 border border-cyberCyan/30 flex items-center justify-center text-cyberCyan text-lg">
                                        <i class="fa-solid fa-phone"></i>
                                    </div>
                                    <div>
                                        <div class="text-xs font-mono text-slate-400 uppercase">Direct Line</div>
                                        <a href="tel:+917533077538" class="text-slate-200 font-semibold hover:text-cyberCyan transition-colors">+91 75330 77538</a>
                                    </div>
                                </div>

                                <div class="flex items-center gap-4">
                                    <div class="w-12 h-12 rounded-2xl bg-electricPurple/10 border border-electricPurple/30 flex items-center justify-center text-electricPurple text-lg">
                                        <i class="fa-solid fa-envelope"></i>
                                    </div>
                                    <div>
                                        <div class="text-xs font-mono text-slate-400 uppercase">Email Dispatch</div>
                                        <a href="mailto:okchandankumar3251@gmail.com" class="text-slate-200 font-semibold hover:text-electricPurple transition-colors">okchandankumar3251@gmail.com</a>
                                    </div>
                                </div>

                                <div class="flex items-center gap-4">
                                    <div class="w-12 h-12 rounded-2xl bg-amberGold/10 border border-amberGold/30 flex items-center justify-center text-amberGold text-lg">
                                        <i class="fa-brands fa-linkedin-in"></i>
                                    </div>
                                    <div>
                                        <div class="text-xs font-mono text-slate-400 uppercase">LinkedIn Profile</div>
                                        <a href="https://linkedin.com/in/chandan-kumar-hrconsultant" target="_blank" class="text-slate-200 font-semibold hover:text-amberGold transition-colors">linkedin.com/in/chandan-kumar-hrconsultant</a>
                                    </div>
                                </div>

                                <div class="flex items-center gap-4">
                                    <div class="w-12 h-12 rounded-2xl bg-slate-800 border border-slate-700 flex items-center justify-center text-slate-300 text-lg">
                                        <i class="fa-solid fa-location-dot"></i>
                                    </div>
                                    <div>
                                        <div class="text-xs font-mono text-slate-400 uppercase">Primary Base</div>
                                        <div class="text-slate-200 font-semibold">South West Delhi / Gurugram, India</div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Brand Footer Tag -->
                        <div class="mt-8 pt-6 border-t border-slate-800 text-xs font-mono text-slate-500">
                            BRAND IDENTIFIER: <span class="text-cyberCyan">mOOnMeridian.com</span>
                        </div>
                    </div>

                    <!-- Interactive Live Message Form -->
                    <div class="glass-card p-8 rounded-3xl">
                        <form id="contactForm" onsubmit="handleFormSubmit(event)">
                            <h4 class="font-orbitron font-semibold text-xl text-white mb-6">Send Direct Transmission</h4>
                            
                            <div class="space-y-4">
                                <div>
                                    <label class="block text-xs font-mono text-slate-400 mb-1">YOUR NAME</label>
                                    <input type="text" required placeholder="e.g. Sarah Jenkins" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-slate-200 focus:border-cyberCyan focus:outline-none transition-colors">
                                </div>

                                <div>
                                    <label class="block text-xs font-mono text-slate-400 mb-1">EMAIL ADDRESS</label>
                                    <input type="email" required placeholder="name@company.com" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-slate-200 focus:border-cyberCyan focus:outline-none transition-colors">
                                </div>

                                <div>
                                    <label class="block text-xs font-mono text-slate-400 mb-1">SUBJECT / TOPIC</label>
                                    <input type="text" placeholder="Account Strategy / Opportunity" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-slate-200 focus:border-cyberCyan focus:outline-none transition-colors">
                                </div>

                                <div>
                                    <label class="block text-xs font-mono text-slate-400 mb-1">MESSAGE TRANSMISSION</label>
                                    <textarea rows="4" required placeholder="Write your query or project scope..." class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-slate-200 focus:border-cyberCyan focus:outline-none transition-colors"></textarea>
                                </div>

                                <button type="submit" id="submitBtn" class="w-full py-4 rounded-xl font-orbitron font-bold text-sm tracking-wider text-black bg-cyberCyan hover:bg-white transition-all shadow-cyanGlow flex items-center justify-center gap-2">
                                    <i class="fa-solid fa-paper-plane"></i> TRANSMIT MESSAGE
                                </button>
                            </div>
                        </form>

                        <!-- Success Message Alert -->
                        <div id="formStatus" class="hidden mt-4 p-4 rounded-xl bg-cyberCyan/10 border border-cyberCyan/40 text-cyberCyan text-sm font-mono text-center">
                            <i class="fa-solid fa-circle-check"></i> Transmission Sent! Chandan Kumar will respond shortly.
                        </div>
                    </div>

                </div>
            </section>

        </main>

        <!-- ================= 7. EDUCATION & CERTIFICATION FOOTER ================= -->
        <footer class="glass-panel border-t border-slate-800 py-10 px-4 sm:px-6 lg:px-8 mt-12">
            <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6 text-xs font-mono text-slate-400">
                
                <div>
                    <span class="text-slate-200 font-bold">Bachelor of Commerce (B.Com)</span> — Delhi University (2021 – 2025)
                    <span class="mx-2 text-slate-600">|</span> 
                    Languages: <span class="text-cyberCyan">English (Proficient)</span>, <span class="text-electricPurple">Hindi (Proficient)</span>
                </div>

                <div class="text-center md:text-right">
                    © 2026 <a href="https://mOOnMeridian.com" class="text-cyberCyan hover:underline">mOOnMeridian.com</a> — Designed for Chandan Kumar.
                </div>
            </div>
        </footer>

    </div>

    <!-- SCRIPT SECTION -->
    <script>
        // 1. STARFIELD CANVAS ANIMATION
        const canvas = document.getElementById('starfield');
        const ctx = canvas.getContext('2d');

        let stars = [];
        const numStars = 120;

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }

        function initStars() {
            stars = [];
            for (let i = 0; i < numStars; i++) {
                stars.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    radius: Math.random() * 1.5,
                    alpha: Math.random(),
                    speed: Math.random() * 0.4 + 0.1
                });
            }
        }

        function animateStars() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            stars.forEach(star => {
                star.y -= star.speed;
                if (star.y < 0) star.y = canvas.height;

                ctx.beginPath();
                ctx.arc(star.x, star.y, star.radius, 0, Math.PI * 2);
                ctx.fillStyle = `rgba(0, 240, 255, ${star.alpha})`;
                ctx.fill();
            });

            requestAnimationFrame(animateStars);
        }

        window.addEventListener('resize', () => {
            resizeCanvas();
            initStars();
        });

        resizeCanvas();
        initStars();
        animateStars();

        // 2. MOBILE MENU TOGGLE
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
            mobileMenu.classList.toggle('flex');
        });

        // 3. SKILLS CATEGORY FILTERING
        const skillTabs = document.querySelectorAll('.skill-tab');
        const skillItems = document.querySelectorAll('.skill-item');

        skillTabs.forEach(tab => {
            tab.addEventListener('click', () => {
                skillTabs.forEach(t => {
                    t.classList.remove('bg-cyberCyan', 'text-black', 'shadow-cyanGlow');
                    t.classList.add('glass-panel', 'text-slate-300');
                });

                tab.classList.remove('glass-panel', 'text-slate-300');
                tab.classList.add('bg-cyberCyan', 'text-black', 'shadow-cyanGlow');

                const category = tab.getAttribute('data-category');

                skillItems.forEach(item => {
                    if (category === 'all' || item.getAttribute('data-category') === category) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });

        // 4. INTERACTIVE ANALYTICS SIMULATOR
        const accountSlider = document.getElementById('accountSlider');
        const accountVal = document.getElementById('accountVal');
        const intensitySelect = document.getElementById('intensitySelect');
        const intensityVal = document.getElementById('intensityVal');
        const metricImpressions = document.getElementById('metricImpressions');
        const barImpressions = document.getElementById('barImpressions');
        const simToggle = document.getElementById('simToggle');

        function updateSimulation() {
            const accounts = parseInt(accountSlider.value);
            const intensity = parseFloat(intensitySelect.value);

            accountVal.textContent = accounts;
            
            if (intensity === 0.5) intensityVal.textContent = "Standard (+50% Views)";
            else if (intensity === 0.8) intensityVal.textContent = "Aggressive (+80% Views)";
            else intensityVal.textContent = "Enterprise Surge (+120% Views)";

            const totalImpressions = Math.round(accounts * 850 * intensity);
            metricImpressions.textContent = totalImpressions.toLocaleString();

            const barWidth = Math.min(100, Math.round((totalImpressions / 100000) * 100));
            barImpressions.style.width = barWidth + '%';
        }

        accountSlider.addEventListener('input', updateSimulation);
        intensitySelect.addEventListener('change', updateSimulation);
        simToggle.addEventListener('click', updateSimulation);

        // 5. ANIMATED NUMERIC COUNTERS
        const counters = document.querySelectorAll('.count-up');
        let counterTriggered = false;

        function runCounters() {
            counters.forEach(counter => {
                const target = parseInt(counter.getAttribute('data-target'));
                let current = 0;
                const increment = Math.ceil(target / 40);

                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        counter.textContent = target;
                        clearInterval(timer);
                    } else {
                        counter.textContent = current;
                    }
                }, 30);
            });
        }

        window.addEventListener('scroll', () => {
            const introSection = document.getElementById('intro');
            const rect = introSection.getBoundingClientRect();
            if (rect.top < window.innerHeight && !counterTriggered) {
                counterTriggered = true;
                runCounters();
            }
        });

        // Initial Counter Execution
        runCounters();

        // 6. FORM TRANSMISSION SIMULATION
        function handleFormSubmit(event) {
            event.preventDefault();
            const submitBtn = document.getElementById('submitBtn');
            const formStatus = document.getElementById('formStatus');

            submitBtn.disabled = true;
            submitBtn.innerHTML = '<i class="fa-solid fa-spinner animate-spin"></i> TRANSMITTING...';

            setTimeout(() => {
                submitBtn.disabled = false;
                submitBtn.innerHTML = '<i class="fa-solid fa-paper-plane"></i> TRANSMIT MESSAGE';
                formStatus.classList.remove('hidden');
                document.getElementById('contactForm').reset();

                setTimeout(() => {
                    formStatus.classList.add('hidden');
                }, 6000);
            }, 1200);
        }
    </script>
</body>
</html>
