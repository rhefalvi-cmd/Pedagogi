
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sekolah Biar Dapat Kerja? - Evolusi Tujuan Pendidikan Indonesia</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        darkgreen: '#263D32',
                        darkgreenlight: '#345244',
                        beige: '#E8DCC8',
                        beigelight: '#F4ECE1',
                        darkgrey: '#191919',
                        gold: '#B08D57',
                        goldlight: '#C9A773',
                    },
                    fontFamily: {
                        serif: ['Playfair Display', 'Georgia', 'serif'],
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    
    <!-- Lucide Icons CDN -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
        body {
            background-color: #191919;
            color: #E8DCC8;
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #191919;
        }
        ::-webkit-scrollbar-thumb {
            background: #B08D57;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #C9A773;
        }

        /* Glassmorphism elements */
        .glass-card {
            background: rgba(38, 61, 50, 0.45);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(176, 141, 87, 0.25);
        }

        .glass-card-hover {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .glass-card-hover:hover {
            border-color: rgba(176, 141, 87, 0.6);
            transform: translateY(-4px);
            box-shadow: 0 12px 30px -10px rgba(0, 0, 0, 0.5);
        }

        /* Timeline connector line styling */
        .timeline-line::before {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            left: 20px;
            width: 2px;
            background: linear-gradient(180deg, #B08D57 0%, #263D32 50%, #B08D57 100%);
        }
        @media (min-width: 768px) {
            .timeline-line::before {
                left: 50%;
                transform: translateX(-50%);
            }
        }

        .gold-gradient-text {
            background: linear-gradient(135deg, #E8DCC8 20%, #B08D57 80%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .gold-border-glow {
            box-shadow: 0 0 15px rgba(176, 141, 87, 0.2);
        }
    </style>
</head>
<body class="selection:bg-gold selection:text-darkgrey">

    <!-- Reading Progress Bar -->
    <div id="progress-bar" class="fixed top-0 left-0 h-1 bg-gold z-50 transition-all duration-150" style="width: 0%"></div>

    <!-- Navigation Header -->
    <header class="fixed top-0 w-full z-40 bg-darkgrey/90 backdrop-blur-md border-b border-gold/20 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <a href="#hero" class="flex items-center gap-3 group">
                    <div class="w-10 h-10 rounded-full bg-darkgreen border border-gold flex items-center justify-center text-gold group-hover:scale-105 transition-transform">
                        <i data-lucide="book-open" class="w-5 h-5"></i>
                    </div>
                    <div>
                        <span class="font-serif font-bold text-lg text-beige tracking-wide block leading-none">PEDAGOGI</span>
                        <span class="text-[10px] text-gold uppercase tracking-widest font-semibold">Humanisme & Realita</span>
                    </div>
                </a>

                <!-- Desktop Navigation Menu -->
                <nav class="hidden md:flex items-center space-x-1 lg:space-x-2 text-sm font-medium">
                    <a href="#pertanyaan" class="px-3 py-2 rounded-lg text-beige hover:text-gold hover:bg-darkgreen/40 transition">Pertanyaan</a>
                    <a href="#sejarah" class="px-3 py-2 rounded-lg text-beige hover:text-gold hover:bg-darkgreen/40 transition">Sejarah</a>
                    <a href="#filsafat" class="px-3 py-2 rounded-lg text-beige hover:text-gold hover:bg-darkgreen/40 transition">Filsafat</a>
                    <a href="#refleksi" class="px-3 py-2 rounded-lg text-beige hover:text-gold hover:bg-darkgreen/40 transition">Refleksi</a>
                    <a href="#pustaka" class="px-3 py-2 rounded-lg text-gold border border-gold/40 hover:bg-gold hover:text-darkgrey transition font-semibold">Daftar Pustaka</a>
                </nav>

                <!-- Mobile Menu Button -->
                <button id="mobile-menu-btn" class="md:hidden p-2 rounded-lg text-beige hover:text-gold focus:outline-none" aria-label="Toggle Navigation">
                    <i data-lucide="menu" class="w-6 h-6"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu Drawer -->
        <div id="mobile-menu" class="hidden md:hidden bg-darkgrey/98 border-b border-gold/20 px-4 pt-2 pb-6 space-y-3">
            <a href="#pertanyaan" class="block px-3 py-2 rounded-md text-beige hover:bg-darkgreen/50 hover:text-gold">Pertanyaan</a>
            <a href="#sejarah" class="block px-3 py-2 rounded-md text-beige hover:bg-darkgreen/50 hover:text-gold">Sejarah Evolusi</a>
            <a href="#filsafat" class="block px-3 py-2 rounded-md text-beige hover:bg-darkgreen/50 hover:text-gold">Filsafat Pendidikan</a>
            <a href="#refleksi" class="block px-3 py-2 rounded-md text-beige hover:bg-darkgreen/50 hover:text-gold">Refleksi Kemanusiaan</a>
            <a href="#pustaka" class="block px-3 py-2 rounded-md text-gold border border-gold/40 text-center hover:bg-gold hover:text-darkgrey">Daftar Pustaka</a>
        </div>
    </header>

    <!-- Hero / Pertanyaan Section -->
    <section id="pertanyaan" class="min-h-screen pt-28 pb-16 flex items-center justify-center relative overflow-hidden bg-gradient-to-b from-darkgrey via-darkgreen/30 to-darkgrey">
        <!-- Decorative Ambient Background Elements -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-darkgreen/30 rounded-full blur-3xl pointer-events-none"></div>
        <div class="absolute bottom-10 right-10 w-80 h-80 bg-gold/10 rounded-full blur-3xl pointer-events-none"></div>

        <div class="max-w-4xl mx-auto px-4 sm:px-6 text-center relative z-10">
            <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-darkgreen/80 border border-gold/30 text-gold text-xs font-semibold tracking-wider uppercase mb-6">
                <i data-lucide="help-circle" class="w-4 h-4"></i> Kajian Kritis Pendidikan Indonesia
            </div>

            <h1 class="font-serif text-4xl sm:text-6xl lg:text-7xl font-bold tracking-tight mb-6 leading-tight">
                “SEKOLAH BIAR DAPAT KERJA?”
            </h1>

            <p class="text-lg sm:text-xl text-beige/80 font-light mb-10 max-w-2xl mx-auto leading-relaxed">
                Menelusuri Evolusi Tujuan Pendidikan Indonesia dari Masa Kolonial hingga Era Digital
            </p>

            <!-- Main Philosophical Question Highlight Box -->
            <div class="glass-card p-8 sm:p-10 rounded-2xl relative border-l-4 border-l-gold shadow-2xl mb-12 text-left">
                <i data-lucide="quote" class="w-12 h-12 text-gold/20 absolute top-4 right-4"></i>
                <span class="text-xs font-semibold uppercase tracking-widest text-gold block mb-2">Pertanyaan Utama</span>
                <p class="font-serif text-2xl sm:text-3xl font-medium text-beige leading-snug italic">
                    “Jika pendidikan bukan sekadar untuk mendapatkan pekerjaan, lalu manusia seperti apa yang hendak dibentuk oleh pendidikan?”
                </p>
            </div>

            <!-- Interactive Perspective Poll -->
            <div class="glass-card p-6 rounded-2xl border border-gold/20 max-w-2xl mx-auto text-left">
                <h3 class="text-sm font-semibold text-gold tracking-wider uppercase mb-3 flex items-center gap-2">
                    <i data-lucide="bar-chart-2" class="w-4 h-4"></i> Menurut Anda, Apa Tujuan Utama Sekolah Hari Ini?
                </h3>
                <p class="text-xs text-beige/70 mb-4">Pilih sudut pandang Anda untuk melihat bagaimana persepsi masyarakat terbentuk:</p>
                
                <div id="poll-options" class="space-y-3">
                    <button onclick="votePoll(0)" class="w-full text-left p-3 rounded-lg bg-darkgrey/60 border border-beige/10 hover:border-gold/50 transition flex justify-between items-center group">
                        <span class="text-sm text-beige font-medium group-hover:text-gold transition">Mendapatkan sertifikat & garansi pekerjaan layak</span>
                        <span id="poll-count-0" class="text-xs bg-darkgreen px-2.5 py-1 rounded text-gold font-semibold">42%</span>
                    </button>
                    <button onclick="votePoll(1)" class="w-full text-left p-3 rounded-lg bg-darkgrey/60 border border-beige/10 hover:border-gold/50 transition flex justify-between items-center group">
                        <span class="text-sm text-beige font-medium group-hover:text-gold transition">Mengembangkan kecerdasan nalar & karakter emosional</span>
                        <span id="poll-count-1" class="text-xs bg-darkgreen px-2.5 py-1 rounded text-gold font-semibold">31%</span>
                    </button>
                    <button onclick="votePoll(2)" class="w-full text-left p-3 rounded-lg bg-darkgrey/60 border border-beige/10 hover:border-gold/50 transition flex justify-between items-center group">
                        <span class="text-sm text-beige font-medium group-hover:text-gold transition">Proses pembebasan nalar dan memanusiakan manusia</span>
                        <span id="poll-count-2" class="text-xs bg-darkgreen px-2.5 py-1 rounded text-gold font-semibold">27%</span>
                    </button>
                </div>
                <div id="poll-feedback" class="mt-3 text-xs text-gold italic hidden text-center">
                    ✓ Terima kasih! Pilihan Anda mencerminkan dialektika antara fungsi ekonomis dan pembebasan jiwa.
                </div>
            </div>

            <div class="mt-12">
                <a href="#sejarah" class="inline-flex items-center gap-2 text-sm text-gold hover:text-beige transition tracking-wide font-medium">
                    Jelajahi Rekam Sejarah <i data-lucide="arrow-down" class="w-4 h-4 animate-bounce"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- Sejarah Section -->
    <section id="sejarah" class="py-24 bg-darkgrey relative border-t border-gold/10">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-gold text-xs font-semibold tracking-widest uppercase mb-2 block">Rekam Jejak Historis</span>
                <h2 class="font-serif text-3xl sm:text-5xl font-bold text-beige mb-4">Evolusi Tujuan Pendidikan Indonesia</h2>
                <p class="text-beige/70 text-sm sm:text-base leading-relaxed">
                    Bagaimana fungsi sekolah bergeser dari alat kolonialisme, wadah pergerakan kemerdekaan, pembentukan identitas nasional, hingga pencetak tenaga kerja industri dan digital.
                </p>
            </div>

            <!-- Vertical Timeline Wrapper -->
            <div class="relative timeline-line space-y-12">
                
                <!-- 1. Pendidikan Kolonial -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-10 h-10 rounded-full bg-darkgreen border-2 border-gold text-gold font-bold text-sm z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2">
                        1
                    </div>
                    <div class="w-full md:w-1/2 md:pr-12 md:text-right">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl">
                            <span class="text-xs font-semibold text-gold tracking-wider uppercase block mb-1">Masa Hindia Belanda</span>
                            <h3 class="font-serif text-2xl font-bold text-beige mb-3">Pendidikan Kolonial</h3>
                            <p class="text-sm text-beige/80 leading-relaxed mb-4">
                                Berfokus pada penciptaan juru tulis dan tenaga administratif murah untuk memenuhi efisiensi birokrasi serta perkebunan pemerintah kolonial (Politik Etis). Sekolah melatih kepatuhan teknis tanpa ruang kritis.
                            </p>
                            <div class="inline-flex items-center gap-2 text-xs text-gold/80 bg-darkgrey/60 px-3 py-1.5 rounded-md border border-gold/20">
                                <i data-lucide="target" class="w-3.5 h-3.5"></i> Fokus: Kepatuhan & Efisiensi Birokrasi Kolonial
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                </div>

                <!-- 2. Pendidikan Nasional & Ki Hadjar Dewantara -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-10 h-10 rounded-full bg-gold border-2 border-darkgreen text-darkgrey font-bold text-sm z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2">
                        2
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                    <div class="w-full md:w-1/2 md:pl-12">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl border-l-4 border-l-gold">
                            <span class="text-xs font-semibold text-gold tracking-wider uppercase block mb-1">Awal Abad ke-20 & Taman Siswa</span>
                            <h3 class="font-serif text-2xl font-bold text-beige mb-3">Pendidikan Nasional & Ki Hadjar Dewantara</h3>
                            <p class="text-sm text-beige/80 leading-relaxed mb-4">
                                Muncul sebagai reaksi perlawanan. Ki Hadjar Dewantara mendirikan Taman Siswa (1922) dengan *Sistem Among*: menuntun kodrat anak agar mencapai kesadaran nasional, kemerdekaan lahir dan batin, serta rasa kebangsaan.
                            </p>
                            <div class="p-3 bg-darkgreen/60 rounded-lg border border-gold/20 text-xs text-beige/90 italic mb-3">
                                “Pendidikan adalah tempat persemaian benih-benih kebudayaan dalam masyarakat.” — Ki Hadjar Dewantara
                            </div>
                            <div class="inline-flex items-center gap-2 text-xs text-gold/80 bg-darkgrey/60 px-3 py-1.5 rounded-md border border-gold/20">
                                <i data-lucide="compass" class="w-3.5 h-3.5"></i> Fokus: Humanisasi & Kesadaran Nasional
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 3. Pendidikan Pascakemerdekaan -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-10 h-10 rounded-full bg-darkgreen border-2 border-gold text-gold font-bold text-sm z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2">
                        3
                    </div>
                    <div class="w-full md:w-1/2 md:pr-12 md:text-right">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl">
                            <span class="text-xs font-semibold text-gold tracking-wider uppercase block mb-1">Era Orde Lama & Orde Baru</span>
                            <h3 class="font-serif text-2xl font-bold text-beige mb-3">Pendidikan Pascakemerdekaan</h3>
                            <p class="text-sm text-beige/80 leading-relaxed mb-4">
                                Peralihan menuju unifikasi identitas bangsa, pemberantasan buta huruf, serta konsolidasi ideologi Pancasila. Sekolah difungsikan sebagai instrumen integrator bangsa pasca-kolonial.
                            </p>
                            <div class="inline-flex items-center gap-2 text-xs text-gold/80 bg-darkgrey/60 px-3 py-1.5 rounded-md border border-gold/20">
                                <i data-lucide="shield" class="w-3.5 h-3.5"></i> Fokus: Karakter Bangsa & Unifikasi Ideologi
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                </div>

                <!-- 4. Pendidikan Era Industri -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-10 h-10 rounded-full bg-darkgreen border-2 border-gold text-gold font-bold text-sm z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2">
                        4
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                    <div class="w-full md:w-1/2 md:pl-12">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl">
                            <span class="text-xs font-semibold text-gold tracking-wider uppercase block mb-1">Akhir Abad ke-20 (Kapitalisme Modern)</span>
                            <h3 class="font-serif text-2xl font-bold text-beige mb-3">Pendidikan Era Industri</h3>
                            <p class="text-sm text-beige/80 leading-relaxed mb-4">
                                Tuntutan modernisasi dan industrialisasi mengubah kurikulum menjadi berorientasi pada pencetakan "Sumber Daya Manusia" (SDM). Sekolah kerap diibaratkan pabrik, dengan standar kelulusan massal yang terukur untuk pasar kerja.
                            </p>
                            <div class="inline-flex items-center gap-2 text-xs text-gold/80 bg-darkgrey/60 px-3 py-1.5 rounded-md border border-gold/20">
                                <i data-lucide="briefcase" class="w-3.5 h-3.5"></i> Fokus: Link and Match dengan Industri
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 5. Pendidikan Era Digital & Kurikulum Merdeka -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-10 h-10 rounded-full bg-gold border-2 border-darkgreen text-darkgrey font-bold text-sm z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2">
                        5
                    </div>
                    <div class="w-full md:w-1/2 md:pr-12 md:text-right">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl border-r-4 border-r-gold">
                            <span class="text-xs font-semibold text-gold tracking-wider uppercase block mb-1">Abad ke-21 & Disrupsi Teknologi</span>
                            <h3 class="font-serif text-2xl font-bold text-beige mb-3">Pendidikan Era Digital</h3>
                            <p class="text-sm text-beige/80 leading-relaxed mb-4">
                                Menghadapi disrupsi AI dan kecerdasan buatan. Melalui spirit Kurikulum Merdeka, tantangan baru muncul: apakah teknologi akan makin mereduksi manusia menjadi sekadar operator data, atau membebaskan potensi nalar kritis manusia?
                            </p>
                            <div class="inline-flex items-center gap-2 text-xs text-gold/80 bg-darkgrey/60 px-3 py-1.5 rounded-md border border-gold/20">
                                <i data-lucide="cpu" class="w-3.5 h-3.5"></i> Fokus: Adaptabilitas, Keterampilan 21st Century & Kemandirian
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                </div>

            </div>
        </div>
    </section>

    <!-- Filsafat Section -->
    <section id="filsafat" class="py-24 bg-darkgreen/20 relative">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-gold text-xs font-semibold tracking-widest uppercase mb-2 block">Pisau Analisis Filosofis</span>
                <h2 class="font-serif text-3xl sm:text-5xl font-bold text-beige mb-4">Dimensi Ontologi & Aksiologi</h2>
                <p class="text-beige/70 text-sm sm:text-base">
                    Membedah esensi mendasar pendidikan dengan mempertanyakan hakikat manusia dan nilai luhur yang dituju.
                </p>
            </div>

            <!-- Tab Navigation for Philosophical Views -->
            <div class="flex justify-center mb-8">
                <div class="bg-darkgrey/80 p-1.5 rounded-xl border border-gold/30 inline-flex space-x-2">
                    <button id="btn-ontologi" onclick="switchPhilosophicalTab('ontologi')" class="px-6 py-2.5 rounded-lg text-sm font-semibold transition bg-gold text-darkgrey shadow">
                        <i data-lucide="user-check" class="w-4 h-4 inline-block mr-1.5"></i> Ontologi (Manusia Seperti Apa?)
                    </button>
                    <button id="btn-aksiologi" onclick="switchPhilosophicalTab('aksiologi')" class="px-6 py-2.5 rounded-lg text-sm font-semibold transition text-beige hover:text-gold">
                        <i data-lucide="heart-handshake" class="w-4 h-4 inline-block mr-1.5"></i> Aksiologi (Nilai Apa yang Diberikan?)
                    </button>
                </div>
            </div>

            <!-- Tab Content Display -->
            <div id="tab-content-container">
                <!-- Ontologi Content -->
                <div id="content-ontologi" class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <div class="glass-card p-8 rounded-2xl border-t-2 border-t-gold">
                        <div class="w-12 h-12 rounded-xl bg-darkgreen flex items-center justify-center text-gold mb-6 border border-gold/30">
                            <i data-lucide="sparkles" class="w-6 h-6"></i>
                        </div>
                        <h3 class="font-serif text-2xl font-bold text-beige mb-3">Manusia Merdeka & Utuh</h3>
                        <p class="text-sm text-beige/80 leading-relaxed mb-4">
                            Dalam tinjauan ontologis Ki Hadjar Dewantara, manusia yang hendak dibentuk bukanlah sosok penurut pasif, melainkan manusia merdeka secara lahir dan batin. Manusia yang tidak bergantung pada orang lain, melainkan bersandar pada kekuatan sendiri untuk mengatur kehidupannya secara bermartabat.
                        </p>
                        <ul class="space-y-2 text-xs text-beige/90">
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Kesadaran akan kodrat alam dan kodrat zaman</li>
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Keseimbangan olah rasa, olah karsa, dan olah raga</li>
                        </ul>
                    </div>

                    <div class="glass-card p-8 rounded-2xl border-t-2 border-t-gold">
                        <div class="w-12 h-12 rounded-xl bg-darkgreen flex items-center justify-center text-gold mb-6 border border-gold/30">
                            <i data-lucide="shield-alert" class="w-6 h-6"></i>
                        </div>
                        <h3 class="font-serif text-2xl font-bold text-beige mb-3">Kritik Humanisasi (Paulo Freire)</h3>
                        <p class="text-sm text-beige/80 leading-relaxed mb-4">
                            Paulo Freire menegaskan bahwa tujuan hakiki pendidikan adalah humanisasi (proses memanusiakan manusia). Pendidikan bertugas membongkar "pendidikan gaya bank" (banking concept of education) yang memperlakukan peserta didik sebagai wadah kosong penampung dogma demi kepentingan akumulasi modal semata.
                        </p>
                        <ul class="space-y-2 text-xs text-beige/90">
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Penolakan terhadap dehumanisasi pekerja</li>
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Pemikiran kritis-transformatif atas realitas sosial</li>
                        </ul>
                    </div>
                </div>

                <!-- Aksiologi Content (Hidden by default) -->
                <div id="content-aksiologi" class="grid grid-cols-1 md:grid-cols-2 gap-8 hidden">
                    <div class="glass-card p-8 rounded-2xl border-t-2 border-t-gold">
                        <div class="w-12 h-12 rounded-xl bg-darkgreen flex items-center justify-center text-gold mb-6 border border-gold/30">
                            <i data-lucide="compass" class="w-6 h-6"></i>
                        </div>
                        <h3 class="font-serif text-2xl font-bold text-beige mb-3">Nilai Budi Pekerti & Etika Sosial</h3>
                        <p class="text-sm text-beige/80 leading-relaxed mb-4">
                            Secara aksiologis, nilai terbesar pendidikan bukan semata-mata diukur dari angka indeks IPK atau tingginya gaji bulanan, melainkan pada pembentukan **Budi Pekerti** (kebijaksanaan watak dan kesadaran etis terhadap sesama).
                        </p>
                        <ul class="space-y-2 text-xs text-beige/90">
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Emphaty, keadilan sosial, dan solidaritas antarmanusia</li>
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Integritas pribadi di tengah kompetisi materialistis</li>
                        </ul>
                    </div>

                    <div class="glass-card p-8 rounded-2xl border-t-2 border-t-gold">
                        <div class="w-12 h-12 rounded-xl bg-darkgreen flex items-center justify-center text-gold mb-6 border border-gold/30">
                            <i data-lucide="scale" class="w-6 h-6"></i>
                        </div>
                        <h3 class="font-serif text-2xl font-bold text-beige mb-3">Keseimbangan Nalar Keterampilan & Kemanusiaan</h3>
                        <p class="text-sm text-beige/80 leading-relaxed mb-4">
                            Keterampilan teknis untuk bekerja memang penting demi kelangsungan hidup fisik, namun nilai instrumental tersebut harus dinaungi oleh **Nilai Kemanusiaan**. Tanpa nilai ini, pendidikan hanya menghasilkan robot pekerja bernyawa.
                        </p>
                        <ul class="space-y-2 text-xs text-beige/90">
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Pengetahuannya melayani kebaikan bersama (*bonum commune*)</li>
                            <li class="flex items-center gap-2"><i data-lucide="check-circle-2" class="w-4 h-4 text-gold"></i> Kemampuan berpikir independen dan tidak mudah dimanipulasi</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Conceptual Comparison Matrix -->
            <div class="mt-12 glass-card p-6 sm:p-8 rounded-2xl">
                <h4 class="font-serif text-xl font-bold text-gold mb-4 text-center">Dialektika Dua Paradigma Pendidikan</h4>
                <div class="overflow-x-auto">
                    <table class="w-full text-sm text-left text-beige/80">
                        <thead class="text-xs uppercase bg-darkgrey/80 text-gold border-b border-gold/20">
                            <tr>
                                <th class="py-3 px-4">Aspek</th>
                                <th class="py-3 px-4">Paradigma Teknokratis (Pasar Kerja)</th>
                                <th class="py-3 px-4">Paradigma Humanistik (Ki Hadjar Dewantara / Freire)</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-gold/10">
                            <tr>
                                <td class="py-3 px-4 font-semibold text-gold">Tujuan Utama</td>
                                <td class="py-3 px-4">Menciptakan tenaga kerja efisien untuk industri</td>
                                <td class="py-3 px-4">Membentuk manusia merdeka, berakal budi, dan berdampak</td>
                            </tr>
                            <tr>
                                <td class="py-3 px-4 font-semibold text-gold">Posisi Murid</td>
                                <td class="py-3 px-4">Komoditas / Objek penerima materi (*banking system*)</td>
                                <td class="py-3 px-4">Subjek aktif pembelajar yang dituntun sesuai kodratnya</td>
                            </tr>
                            <tr>
                                <td class="py-3 px-4 font-semibold text-gold">Ukuran Keberhasilan</td>
                                <td class="py-3 px-4">Gaji, serapan pasar kerja, Ijazah & Gelar formal</td>
                                <td class="py-3 px-4">Kebijaksanaan, kebebasan berpikir, berkontribusi pada masyarakat</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

        </div>
    </section>

    <!-- Poster Digital & Hook Utama Section -->
    <section id="poster" class="py-20 bg-darkgrey border-t border-b border-gold/20 relative overflow-hidden">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 text-center">

            <!-- Poster Frame -->
            <div class="relative bg-gradient-to-b from-darkgreen via-darkgreenlight to-darkgrey p-8 sm:p-14 rounded-3xl border-2 border-gold shadow-2xl gold-border-glow max-w-2xl mx-auto text-center overflow-hidden">
                <div class="absolute top-0 left-0 w-full h-2 bg-gradient-to-r from-gold via-beige to-gold"></div>
                <div class="absolute -top-16 -left-16 w-36 h-36 bg-gold/15 rounded-full blur-2xl pointer-events-none"></div>
                <div class="absolute -bottom-16 -right-16 w-36 h-36 bg-gold/10 rounded-full blur-2xl pointer-events-none"></div>

                <span class="inline-block px-3.5 py-1 rounded-full bg-darkgrey/70 border border-gold/40 text-gold text-[11px] uppercase tracking-widest font-semibold mb-8">
                    EVOLUSI TUJUAN PENDIDIKAN INDONESIA
                </span>

                <!-- Main Hook Statement in Large Font -->
                <h3 class="font-serif text-3xl sm:text-5xl font-extrabold text-beige leading-snug sm:leading-tight tracking-tight mb-8 drop-shadow-md">
                    “Apakah sekolah kita sedang mempersiapkan manusia untuk hidup, atau hanya tenaga kerja untuk bekerja?”
                </h3>

                <div class="w-24 h-1 bg-gold/60 mx-auto rounded-full mb-6"></div>

                <p class="text-xs text-beige/60 italic">
                    Diadaptasi dari gagasan filosofis Ki Hadjar Dewantara & Paulo Freire
                </p>
            </div>

        </div>
    </section>

    <!-- Refleksi Section -->
    <section id="refleksi" class="py-24 bg-darkgrey relative">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 text-center">
            
            <div class="w-16 h-16 rounded-full bg-gold/10 border border-gold flex items-center justify-center text-gold mx-auto mb-6">
                <i data-lucide="brain-circuit" class="w-8 h-8"></i>
            </div>

            <span class="text-gold text-xs font-semibold tracking-widest uppercase mb-2 block">Muara Pemikiran</span>
            <h2 class="font-serif text-3xl sm:text-5xl font-bold text-beige mb-8">Refleksi Kemanusiaan</h2>

            <!-- Big Reflective Card -->
            <div class="glass-card p-8 sm:p-12 rounded-3xl border border-gold/30 text-left mb-12 shadow-2xl relative">
                <div class="space-y-6 text-base sm:text-lg text-beige/90 leading-relaxed font-light">
                    <p class="font-serif italic text-xl sm:text-2xl text-gold border-l-2 border-gold pl-4 mb-6">
                        “Apakah pendidikan kita hari ini sedang mempersiapkan manusia untuk hidup, atau sekadar mempersiapkan tenaga kerja untuk bekerja?”
                    </p>
                    <p>
                        Jika tujuan pendidikan dipersempit menjadi sekadar pabrik pencetak kuli berdasi, maka saat pekerjaan tersebut terdisrupsi oleh otomatisasi kecerdasan buatan (AI), manusia akan kehilangan orientasi keberadaannya.
                    </p>
                    <p>
                        Bekerja adalah bagian dari cara manusia mempertahankan hidup dan berkarya. Namun, bekerja hanyalah salah satu instrumen—bukan muara akhir dari eksistensi manusia. Pendidikan sejati memampukan seseorang untuk memiliki profesi tanpa membiarkan profesinya mengikis kompas moral dan jiwanya.
                    </p>
                </div>
            </div>

            <!-- Synthesis & Final Quote Highlight Box -->
            <div class="p-8 sm:p-12 rounded-3xl bg-gradient-to-br from-darkgreen via-darkgreenlight to-darkgrey border-2 border-gold shadow-2xl relative overflow-hidden text-center gold-border-glow">
                <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-gold/10 rounded-full blur-2xl"></div>
                <i data-lucide="quote" class="w-16 h-16 text-gold/20 mx-auto mb-4"></i>
                
                <h3 class="text-xs uppercase tracking-widest text-gold font-bold mb-4">Sintesis Akhir</h3>
                <blockquote class="font-serif text-2xl sm:text-4xl font-semibold text-beige leading-snug tracking-tight mb-6">
                    “Mungkin tujuan pendidikan bukan memilih antara menjadi manusia atau menjadi pekerja. Mungkin pendidikan seharusnya membuat kita mampu bekerja tanpa kehilangan kemanusiaan.”
                </blockquote>

                <div class="inline-flex items-center gap-2 text-xs text-beige/70 bg-darkgrey/70 px-4 py-2 rounded-full border border-gold/30">
                    <i data-lucide="feather" class="w-4 h-4 text-gold"></i> Sebuah Perenungan Filosofi Pendidikan Indonesia
                </div>
            </div>

        </div>
    </section>

    <!-- Daftar Pustaka Section -->
    <section id="pustaka" class="py-20 bg-darkgrey/90 border-t border-gold/20">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-center justify-between mb-10 pb-4 border-b border-gold/20 gap-4">
                <div>
                    <span class="text-gold text-xs font-semibold tracking-widest uppercase block mb-1">Referensi Akademik</span>
                    <h2 class="font-serif text-2xl sm:text-3xl font-bold text-beige">Daftar Pustaka</h2>
                </div>
                
                <!-- Search Filter in Citations -->
                <div class="relative w-full md:w-72">
                    <input type="text" id="bib-search" onkeyup="filterBibliography()" placeholder="Cari penulis / kata kunci..." class="w-full bg-darkgreen/40 border border-gold/30 rounded-lg px-4 py-2 text-xs text-beige placeholder-beige/40 focus:outline-none focus:border-gold">
                    <i data-lucide="search" class="w-4 h-4 text-gold absolute right-3 top-2.5"></i>
                </div>
            </div>

            <!-- List of References -->
            <div id="bib-list" class="space-y-4 text-sm">
                
                <!-- 1 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Dewantara, K. H.</strong> (2013). <em>Ki Hadjar Dewantara: Bagian pertama pendidikan</em>. Yogyakarta: Majelis Luhur Persatuan Tamansiswa.
                    </p>
                </div>

                <!-- 2 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition flex flex-col sm:flex-row sm:items-center justify-between gap-2">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Fadhlurrahman.</strong> (2025). Educational journey: From the Roman era, the Dutch colonial period, to Muhammadiyah in Indonesia. <em>Humanika: Kajian Ilmiah Mata Kuliah Umum</em>, 25(1).
                    </p>
                    <a href="https://doi.org/10.21831/hum.v25i1.79883" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/30 px-3 py-1 rounded hover:bg-gold hover:text-darkgrey transition flex items-center gap-1 w-fit">
                        DOI <i data-lucide="external-link" class="w-3 h-3"></i>
                    </a>
                </div>

                <!-- 3 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Freire, P.</strong> (1970). <em>Pedagogy of the oppressed</em>. Herder and Herder.
                    </p>
                </div>

                <!-- 4 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Kementerian Pendidikan, Kebudayaan, Riset, dan Teknologi.</strong> (2024). <em>Kurikulum Merdeka: Landasan filosofis dan tujuan Kurikulum Merdeka</em>. Kementerian Pendidikan, Kebudayaan, Riset, dan Teknologi.
                    </p>
                </div>

                <!-- 5 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition flex flex-col sm:flex-row sm:items-center justify-between gap-2">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Rhamadani, A., & Triaristina, A.</strong> (2023). Peran Taman Siswa dalam pembentukan rasa nasionalisme pada masa pergerakan nasional. <em>ISTORIA: Jurnal Pendidikan dan Ilmu Sejarah</em>, 19(1).
                    </p>
                    <a href="https://doi.org/10.21831/istoria.v19i1.53750" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/30 px-3 py-1 rounded hover:bg-gold hover:text-darkgrey transition flex items-center gap-1 w-fit">
                        DOI <i data-lucide="external-link" class="w-3 h-3"></i>
                    </a>
                </div>

                <!-- 6 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition flex flex-col sm:flex-row sm:items-center justify-between gap-2">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Riberu, K., & Rosvita, L. A.</strong> (2020). Education foundation: History (history as the basis of education). <em>Jurnal Pembangunan Pendidikan: Fondasi dan Aplikasi</em>, 8(1).
                    </p>
                    <a href="https://doi.org/10.21831/jppfa.v8i1.35988" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/30 px-3 py-1 rounded hover:bg-gold hover:text-darkgrey transition flex items-center gap-1 w-fit">
                        DOI <i data-lucide="external-link" class="w-3 h-3"></i>
                    </a>
                </div>

                <!-- 7 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition flex flex-col sm:flex-row sm:items-center justify-between gap-2">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Riski, M. A., Haq, M. A., & Daristin, P. E.</strong> (2026). Pendidikan sebagai proses humanisasi: Analisis pemikiran Paulo Freire. <em>Education: Jurnal Sosial Humaniora dan Pendidikan</em>, 6(2).
                    </p>
                    <a href="https://doi.org/10.51903/maedx172" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/30 px-3 py-1 rounded hover:bg-gold hover:text-darkgrey transition flex items-center gap-1 w-fit">
                        DOI <i data-lucide="external-link" class="w-3 h-3"></i>
                    </a>
                </div>

                <!-- 8 -->
                <div class="bib-item glass-card p-4 rounded-xl border border-gold/10 hover:border-gold/40 transition flex flex-col sm:flex-row sm:items-center justify-between gap-2">
                    <p class="text-beige/90 leading-relaxed">
                        <strong class="text-gold">Thaariq, Z. Z. A., & Karima, U.</strong> (2023). Menelisik pemikiran Ki Hadjar Dewantara dalam konteks pembelajaran abad 21: Sebuah renungan dan inspirasi. <em>FOUNDASIA</em>, 14(2).
                    </p>
                    <a href="https://doi.org/10.21831/foundasia.v14i2.63740" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/30 px-3 py-1 rounded hover:bg-gold hover:text-darkgrey transition flex items-center gap-1 w-fit">
                        DOI <i data-lucide="external-link" class="w-3 h-3"></i>
                    </a>
                </div>

            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-darkgrey border-t border-gold/10 py-8 text-center text-xs text-beige/50">
        <div class="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-4">
            <p>© Kajian Filosofi & Evolusi Pendidikan Indonesia.</p>
            <p class="text-gold/80">Kombinasi Warna: Dark Green (#263D32) • Beige (#E8DCC8) • Hitam (#191919) • Muted Gold (#B08D57)</p>
        </div>
    </footer>

    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Scroll Progress Bar calculation
        window.addEventListener('scroll', () => {
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            document.getElementById('progress-bar').style.width = scrolled + '%';
        });

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Close mobile menu on clicking links
        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Interactive Poll Function
        let pollVoted = false;
        function votePoll(index) {
            if(pollVoted) return;
            pollVoted = true;

            const feedback = document.getElementById('poll-feedback');
            feedback.classList.remove('hidden');

            const counts = ['43%', '32%', '28%'];
            document.getElementById(`poll-count-${index}`).innerText = counts[index] + ' (Anda)';
            document.getElementById(`poll-count-${index}`).classList.add('bg-gold', 'text-darkgrey');
        }

        // Philosophical Tab Switcher
        function switchPhilosophicalTab(tab) {
            const btnOntologi = document.getElementById('btn-ontologi');
            const btnAksiologi = document.getElementById('btn-aksiologi');
            const contentOntologi = document.getElementById('content-ontologi');
            const contentAksiologi = document.getElementById('content-aksiologi');

            if (tab === 'ontologi') {
                btnOntologi.className = "px-6 py-2.5 rounded-lg text-sm font-semibold transition bg-gold text-darkgrey shadow";
                btnAksiologi.className = "px-6 py-2.5 rounded-lg text-sm font-semibold transition text-beige hover:text-gold";
                contentOntologi.classList.remove('hidden');
                contentAksiologi.classList.add('hidden');
            } else {
                btnAksiologi.className = "px-6 py-2.5 rounded-lg text-sm font-semibold transition bg-gold text-darkgrey shadow";
                btnOntologi.className = "px-6 py-2.5 rounded-lg text-sm font-semibold transition text-beige hover:text-gold";
                contentAksiologi.classList.remove('hidden');
                contentOntologi.classList.add('hidden');
            }
        }

        // Bibliography Search Filter
        function filterBibliography() {
            const input = document.getElementById('bib-search').value.toLowerCase();
            const items = document.querySelectorAll('.bib-item');

            items.forEach(item => {
                const text = item.textContent.toLowerCase();
                if(text.includes(input)) {
                    item.style.display = "flex";
                } else {
                    item.style.display = "none";
                }
            });
        }
    </script>
</body>
</html>
