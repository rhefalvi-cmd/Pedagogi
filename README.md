
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sekolah Biar Dapat Kerja? - Evolusi Tujuan Pendidikan Indonesia</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,700;0,900;1,400;1,600&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        darkgreen: '#263D32',
                        darkgreenlight: '#314e41',
                        beige: '#E8DCC8',
                        beigelight: '#FAF6F0',
                        darkgrey: '#191919',
                        gold: '#B08D57',
                        goldlight: '#D4AF37',
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
        /* High Contrast & Custom Typography Styles */
        body {
            background-color: #191919;
            color: #E8DCC8;
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
            line-height: 1.7;
        }

        /* High Visibility Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #191919;
        }
        ::-webkit-scrollbar-thumb {
            background: #B08D57;
            border-radius: 5px;
            border: 2px solid #191919;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #D4AF37;
        }

        /* High-Contrast Glassmorphism Container */
        .glass-card {
            background: rgba(38, 61, 50, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(176, 141, 87, 0.4);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
        }

        .glass-card-hover {
            transition: all 0.35s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .glass-card-hover:hover {
            border-color: #B08D57;
            transform: translateY(-5px);
            box-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.7), 0 0 15px rgba(176, 141, 87, 0.3);
        }

        /* Timeline connector line styling */
        .timeline-line::before {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            left: 20px;
            width: 3px;
            background: linear-gradient(180deg, #B08D57 0%, #263D32 50%, #B08D57 100%);
        }
        @media (min-width: 768px) {
            .timeline-line::before {
                left: 50%;
                transform: translateX(-50%);
            }
        }

        .gold-border-glow {
            box-shadow: 0 0 25px rgba(176, 141, 87, 0.25);
        }

        /* Text readability enhancers */
        .text-high-contrast {
            color: #FAF6F0 !important;
        }
        .text-muted-gold {
            color: #D4AF37 !important;
        }
    </style>
</head>
<body class="selection:bg-gold selection:text-darkgrey">

    <!-- Reading Progress Indicator -->
    <div id="progress-bar" class="fixed top-0 left-0 h-1 bg-gold z-50 transition-all duration-150" style="width: 0%"></div>

    <!-- Navigation Header -->
    <header class="fixed top-0 w-full z-40 bg-darkgrey/95 backdrop-blur-md border-b border-gold/30 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <a href="#pertanyaan" class="flex items-center gap-3 group">
                    <div class="w-10 h-10 rounded-full bg-darkgreen border-2 border-gold flex items-center justify-center text-gold group-hover:scale-105 transition-transform">
                        <i data-lucide="book-open" class="w-5 h-5"></i>
                    </div>
                    <div>
                        <span class="font-serif font-bold text-xl text-beigelight tracking-wide block leading-none">EVOLUSI PEDAGOGI</span>
                        <span class="text-xs text-gold uppercase tracking-widest font-bold">Pendidikan & Kemanusiaan</span>
                    </div>
                </a>

                <!-- Desktop Navigation Menu -->
                <nav class="hidden md:flex items-center space-x-1 lg:space-x-2 text-sm font-semibold">
                    <a href="#pertanyaan" class="px-3 py-2 rounded-lg text-beigelight hover:text-gold hover:bg-darkgreen/60 transition">Pertanyaan Utama</a>
                    <a href="#sejarah" class="px-3 py-2 rounded-lg text-beigelight hover:text-gold hover:bg-darkgreen/60 transition">Jejak Sejarah</a>
                    <a href="#filsafat" class="px-3 py-2 rounded-lg text-beigelight hover:text-gold hover:bg-darkgreen/60 transition">Filsafat</a>
                    <a href="#poster" class="px-3 py-2 rounded-lg text-beigelight hover:text-gold hover:bg-darkgreen/60 transition">Poster</a>
                    <a href="#refleksi" class="px-3 py-2 rounded-lg text-beigelight hover:text-gold hover:bg-darkgreen/60 transition">Refleksi</a>
                    <a href="#pustaka" class="px-3.5 py-2 rounded-lg text-darkgrey bg-gold hover:bg-goldlight transition font-bold shadow-md">Daftar Pustaka</a>
                </nav>

                <!-- Mobile Menu Button -->
                <button id="mobile-menu-btn" class="md:hidden p-2 rounded-lg text-beigelight hover:text-gold focus:outline-none" aria-label="Toggle Navigation">
                    <i data-lucide="menu" class="w-7 h-7"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu Drawer -->
        <div id="mobile-menu" class="hidden md:hidden bg-darkgrey border-b border-gold/30 px-4 pt-3 pb-6 space-y-3 font-semibold">
            <a href="#pertanyaan" class="block px-3 py-2 rounded-md text-beigelight hover:bg-darkgreen hover:text-gold">Pertanyaan Utama</a>
            <a href="#sejarah" class="block px-3 py-2 rounded-md text-beigelight hover:bg-darkgreen hover:text-gold">Jejak Sejarah</a>
            <a href="#filsafat" class="block px-3 py-2 rounded-md text-beigelight hover:bg-darkgreen hover:text-gold">Filsafat Pendidikan</a>
            <a href="#poster" class="block px-3 py-2 rounded-md text-beigelight hover:bg-darkgreen hover:text-gold">Poster Refleksi</a>
            <a href="#refleksi" class="block px-3 py-2 rounded-md text-beigelight hover:bg-darkgreen hover:text-gold">Refleksi Kemanusiaan</a>
            <a href="#pustaka" class="block px-3 py-2 rounded-md bg-gold text-darkgrey text-center font-bold">Daftar Pustaka</a>
        </div>
    </header>

    <!-- Hero / Pertanyaan Utama Section -->
    <section id="pertanyaan" class="min-h-screen pt-28 pb-20 flex items-center justify-center relative overflow-hidden bg-gradient-to-b from-darkgrey via-darkgreen/40 to-darkgrey">
        <!-- Ambient Decorative Graphics -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] bg-darkgreen/50 rounded-full blur-3xl pointer-events-none"></div>
        <div class="absolute bottom-10 right-10 w-96 h-96 bg-gold/15 rounded-full blur-3xl pointer-events-none"></div>

        <div class="max-w-5xl mx-auto px-4 sm:px-6 text-center relative z-10">
            
            <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-darkgreen border border-gold/50 text-gold text-sm font-bold tracking-wider uppercase mb-8 shadow-lg">
                <i data-lucide="help-circle" class="w-4 h-4"></i> Kajian Kritis & Dekonstruksi Filosofi Pendidikan
            </div>

            <h1 class="font-serif text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight mb-6 leading-tight text-beigelight">
                “SEKOLAH BIAR DAPAT KERJA?”
            </h1>

            <p class="text-lg sm:text-2xl text-beigelight font-normal mb-10 max-w-3xl mx-auto leading-relaxed">
                Menelusuri Evolusi Tujuan Pendidikan Indonesia dari Masa Kolonial hingga Era Digital
            </p>

            <!-- Main Philosophical Question Highlight Box -->
            <div class="glass-card p-8 sm:p-12 rounded-3xl relative border-l-8 border-l-gold shadow-2xl mb-12 text-left">
                <i data-lucide="quote" class="w-16 h-16 text-gold/30 absolute top-4 right-4"></i>
                <span class="text-xs font-bold uppercase tracking-widest text-gold block mb-3">Pertanyaan Kunci Penuntun Logika</span>
                <p class="font-serif text-2xl sm:text-4xl font-semibold text-beigelight leading-snug italic">
                    “Jika pendidikan bukan sekadar untuk mendapatkan pekerjaan, lalu manusia seperti apa yang hendak dibentuk oleh pendidikan?”
                </p>
            </div>

            <!-- Contextual Deep Expansion Paragraphs -->
            <div class="glass-card p-8 rounded-2xl text-left space-y-5 text-beigelight text-base sm:text-lg mb-10 border border-gold/30">
                <h3 class="font-serif text-xl sm:text-2xl font-bold text-gold flex items-center gap-2">
                    <i data-lucide="compass" class="w-6 h-6"></i> Mengapa Pertanyaan Ini Penting Hari Ini?
                </h3>
                <p>
                    Dalam kehidupan masyarakat modern, institusi sekolah sering kali dipersempit fungsinya menjadi sekadar pabrik penyedia tenaga kerja. Siswa dituntut belajar selama belasan tahun hanya demi selembar ijazah yang dapat ditukarkan dengan status pegawai atau gaji bulanan. Fenomena komodifikasi dan pragmatisme pendidikan ini menimbulkan kegelisahan mendalam: <strong>apakah martabat manusia sejajar dengan kapasitas komoditas ekonominya?</strong>
                </p>
                <p>
                    Ketika gelombang otomatisasi, disrupsi teknologi, dan Kecerdasan Buatan (AI) mengancam berbagai bidang pekerjaan formal, manusia yang dilatih <em>hanya</em> untuk bekerja rentan mengalami krisis eksistensial. Oleh karena itu, kita perlu melacak kembali akar sejarah dan tujuan fundamental pedagogi Indonesia agar pendidikan tidak kehilangan ruh kemanusiaannya.
                </p>
            </div>

            <!-- Interactive Perspective Poll -->
            <div class="glass-card p-6 sm:p-8 rounded-2xl border border-gold/40 max-w-3xl mx-auto text-left shadow-xl">
                <h3 class="text-base sm:text-lg font-bold text-gold tracking-wider uppercase mb-2 flex items-center gap-2">
                    <i data-lucide="bar-chart-3" class="w-5 h-5"></i> Menurut Anda, Apa Tujuan Utama Sekolah Saat Ini?
                </h3>
                <p class="text-sm text-beigelight/90 mb-5">Pilih salah satu sudut pandang untuk melihat gambaran dinamika persepsi publik:</p>
                
                <div id="poll-options" class="space-y-3">
                    <button onclick="votePoll(0)" class="w-full text-left p-4 rounded-xl bg-darkgrey/90 border border-gold/30 hover:border-gold transition flex justify-between items-center group">
                        <span class="text-sm sm:text-base text-beigelight font-semibold group-hover:text-gold transition">1. Jaminan ijazah, status sosial, dan kepastian kerja yang layak</span>
                        <span id="poll-count-0" class="text-xs sm:text-sm bg-darkgreen px-3 py-1.5 rounded-lg text-gold font-bold">42%</span>
                    </button>
                    <button onclick="votePoll(1)" class="w-full text-left p-4 rounded-xl bg-darkgrey/90 border border-gold/30 hover:border-gold transition flex justify-between items-center group">
                        <span class="text-sm sm:text-base text-beigelight font-semibold group-hover:text-gold transition">2. Pembentukan karakter, kemampuan bernalar, dan kemandirian</span>
                        <span id="poll-count-1" class="text-xs sm:text-sm bg-darkgreen px-3 py-1.5 rounded-lg text-gold font-bold">31%</span>
                    </button>
                    <button onclick="votePoll(2)" class="w-full text-left p-4 rounded-xl bg-darkgrey/90 border border-gold/30 hover:border-gold transition flex justify-between items-center group">
                        <span class="text-sm sm:text-base text-beigelight font-semibold group-hover:text-gold transition">3. Proses pembebasan nalar kritis dan memanusiakan manusia</span>
                        <span id="poll-count-2" class="text-xs sm:text-sm bg-darkgreen px-3 py-1.5 rounded-lg text-gold font-bold">27%</span>
                    </button>
                </div>
                <div id="poll-feedback" class="mt-4 p-3 bg-darkgreen/80 rounded-lg text-sm text-gold font-medium hidden text-center border border-gold/40">
                    ✓ Terima kasih atas partisipasi Anda! Pilihan Anda mencerminkan perdebatan nyata antara paradigma instrumentalistis dan humanistis.
                </div>
            </div>

            <div class="mt-12">
                <a href="#sejarah" class="inline-flex items-center gap-2 text-base text-gold hover:text-beigelight transition tracking-wide font-bold bg-darkgreen/60 px-6 py-3 rounded-full border border-gold/40">
                    Mulai Menelusuri Rekam Sejarah <i data-lucide="arrow-down" class="w-5 h-5 animate-bounce"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- Sejarah Section -->
    <section id="sejarah" class="py-24 bg-darkgrey relative border-t border-gold/20">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-gold text-xs sm:text-sm font-bold tracking-widest uppercase mb-2 block">Analisis Dialektika Historis</span>
                <h2 class="font-serif text-3xl sm:text-5xl font-extrabold text-beigelight mb-4">Evolusi Tujuan Pendidikan Indonesia</h2>
                <p class="text-beigelight text-base sm:text-lg leading-relaxed">
                    Setiap periode zaman membawa kepentingan politik, ekonomi, dan sosial yang secara langsung mendikte orientasi serta output dari persekolahan di Nusantara.
                </p>
            </div>

            <!-- Vertical Timeline Wrapper -->
            <div class="relative timeline-line space-y-16">
                
                <!-- 1. Pendidikan Kolonial -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-12 h-12 rounded-full bg-darkgreen border-2 border-gold text-gold font-extrabold text-base z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2 shadow-lg">
                        1
                    </div>
                    <div class="w-full md:w-1/2 md:pr-12 md:text-right">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl border-t-4 border-t-gold">
                            <span class="text-xs font-bold text-gold tracking-widest uppercase block mb-1">Abad ke-19 hingga Pertengahan Abad ke-20</span>
                            <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight mb-3">Pendidikan Kolonial Hindia Belanda</h3>
                            <p class="text-sm sm:text-base text-beigelight leading-relaxed mb-4">
                                Didesain khusus melalui kebijakan <strong>Politik Etis (1901)</strong> bukan untuk mencerdaskan kehidupan rakyat secara utuh, melainkan untuk memenuhi kebutuhan tenaga kerja birokrasi dan perkebunan kolonial yang murah (<em>ambtenaar</em>).
                            </p>
                            <div class="space-y-2 text-xs sm:text-sm text-beigelight bg-darkgrey/80 p-4 rounded-xl border border-gold/20 text-left mb-4">
                                <p class="font-semibold text-gold">Karakteristik Utama:</p>
                                <ul class="list-disc pl-4 space-y-1">
                                    <li>Diskriminatif & Stratifikasi Sosial (ELS untuk Eropa, HIS untuk Bumiputera, Schakel School).</li>
                                    <li>Menekankan kepatuhan hierarkis, kemampuan berhitung praktis, dan literasi dasar birokrasi.</li>
                                    <li>Mencegah lahirnya kesadaran politik kritis kaum pribumi.</li>
                                </ul>
                            </div>
                            <div class="inline-flex items-center gap-2 text-xs sm:text-sm font-semibold text-gold bg-darkgreen px-3.5 py-2 rounded-lg border border-gold/30">
                                <i data-lucide="target" class="w-4 h-4"></i> Muara: Efisiensi Eksploitasi & Kepatuhan Birokrasi
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                </div>

                <!-- 2. Pendidikan Nasional & Ki Hadjar Dewantara -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-12 h-12 rounded-full bg-gold border-2 border-darkgreen text-darkgrey font-extrabold text-base z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2 shadow-lg">
                        2
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                    <div class="w-full md:w-1/2 md:pl-12">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl border-l-4 border-l-gold">
                            <span class="text-xs font-bold text-gold tracking-widest uppercase block mb-1">Tahun 1922 (Pergerakan Nasional)</span>
                            <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight mb-3">Pendidikan Nasional & Ki Hadjar Dewantara</h3>
                            <p class="text-sm sm:text-base text-beigelight leading-relaxed mb-4">
                                Lahir sebagai tandingan (<em>counter-hegemony</em>) terhadap sekolah kolonial. Melalui pengesahan <strong>Perguruan Taman Siswa (3 Juli 1922)</strong>, Ki Hadjar Dewantara merumuskan gagasan pendidikan berbasis kebudayaan nasional dan kemerdekaan jiwa.
                            </p>
                            <div class="p-4 bg-darkgreen/90 rounded-xl border border-gold/30 text-xs sm:text-sm text-beigelight italic mb-4">
                                “Pendidikan adalah tuntunan dalam hidup tumbuhnya anak-anak. Maksud pendidikan yaitu menuntun segala kodrat yang ada pada anak-anak itu, agar mereka sebagai manusia dan anggota masyarakat dapat mencapai keselamatan dan kebahagiaan yang setinggi-tingginya.”
                            </div>
                            <div class="space-y-2 text-xs sm:text-sm text-beigelight bg-darkgrey/80 p-4 rounded-xl border border-gold/20 mb-4">
                                <p class="font-semibold text-gold">Sistem Among & Tri-Kon:</p>
                                <ul class="list-disc pl-4 space-y-1">
                                    <li><strong>Ing Ngarsa Sung Tulada, Ing Madya Mangun Karsa, Tut Wuri Handayani.</strong></li>
                                    <li>Pendidikan selaras dengan <em>Kodrat Alam</em> dan <em>Kodrat Zaman</em>.</li>
                                    <li>Pendidikan sebagai proses humanisasi dan pembentukan karakter merdeka.</li>
                                </ul>
                            </div>
                            <div class="inline-flex items-center gap-2 text-xs sm:text-sm font-semibold text-gold bg-darkgreen px-3.5 py-2 rounded-lg border border-gold/30">
                                <i data-lucide="compass" class="w-4 h-4"></i> Muara: Manusia Merdeka & Kesadaran Kebangsaan
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 3. Pendidikan Pascakemerdekaan -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-12 h-12 rounded-full bg-darkgreen border-2 border-gold text-gold font-extrabold text-base z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2 shadow-lg">
                        3
                    </div>
                    <div class="w-full md:w-1/2 md:pr-12 md:text-right">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl border-t-4 border-t-gold">
                            <span class="text-xs font-bold text-gold tracking-widest uppercase block mb-1">Pasca 1945 hingga Era Orde Baru</span>
                            <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight mb-3">Pendidikan Pascakemerdekaan & Konsolidasi Negara</h3>
                            <p class="text-sm sm:text-base text-beigelight leading-relaxed mb-4">
                                Era pasca-kemerdekaan difokuskan pada dekolonisasi mental, unifikasi kebudayaan, dan pementasan gerakan pencerahan rakyat secara masif (seperti pementasan buta huruf).
                            </p>
                            <div class="space-y-2 text-xs sm:text-sm text-beigelight bg-darkgrey/80 p-4 rounded-xl border border-gold/20 text-left mb-4">
                                <p class="font-semibold text-gold">Pergeseran Orde Lama ke Orde Baru:</p>
                                <ul class="list-disc pl-4 space-y-1">
                                    <li><strong>Orde Lama:</strong> Pendidikan difungsikan untuk menggelorakan karakter 'Nation and Character Building' serta anti-imperialisme.</li>
                                    <li><strong>Orde Baru:</strong> Penyeragaman kurikulum nasional, doktrinasi Pancasila, pembentukan stabilitas nasional, dan pemerataan Sekolah Dasar Inpres.</li>
                                </ul>
                            </div>
                            <div class="inline-flex items-center gap-2 text-xs sm:text-sm font-semibold text-gold bg-darkgreen px-3.5 py-2 rounded-lg border border-gold/30">
                                <i data-lucide="shield" class="w-4 h-4"></i> Muara: Unifikasi Identitas Nasional & Stabilitas
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                </div>

                <!-- 4. Pendidikan Era Industri -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-12 h-12 rounded-full bg-darkgreen border-2 border-gold text-gold font-extrabold text-base z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2 shadow-lg">
                        4
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                    <div class="w-full md:w-1/2 md:pl-12">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl border-t-4 border-t-gold">
                            <span class="text-xs font-bold text-gold tracking-widest uppercase block mb-1">Akhir Abad ke-20 hingga Awal Abad ke-21</span>
                            <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight mb-3">Pendidikan Era Industri & Link and Match</h3>
                            <p class="text-sm sm:text-base text-beigelight leading-relaxed mb-4">
                                Masuknya kapitalisme global menggeser paradigma pendidikan menuju <strong>teknokrasi</strong>. Slogan populer <em>Link and Match</em> (keterikatan dan kesepadanan) diperkenalkan untuk memastikan institusi pendidikan tunduk pada pasar kerja.
                            </p>
                            <div class="space-y-2 text-xs sm:text-sm text-beigelight bg-darkgrey/80 p-4 rounded-xl border border-gold/20 mb-4">
                                <p class="font-semibold text-gold">Dampak Teknokratisasi:</p>
                                <ul class="list-disc pl-4 space-y-1">
                                    <li>Siswa dan mahasiswa dipandang sebagai "Sumber Daya Manusia" (SDM) / bahan baku ekonomi.</li>
                                    <li>Indikator keberhasilan disempitkan pada statistik daya serap industri dan tingginya angka kelulusan formal.</li>
                                    <li>Standardisasi ujian nasional (UN) masif yang mengenyampingkan keunikan potensi lokal.</li>
                                </ul>
                            </div>
                            <div class="inline-flex items-center gap-2 text-xs sm:text-sm font-semibold text-gold bg-darkgreen px-3.5 py-2 rounded-lg border border-gold/30">
                                <i data-lucide="briefcase" class="w-4 h-4"></i> Muara: Efisiensi Pasar Kerja & Kapitalisasi SDM
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 5. Pendidikan Era Digital -->
                <div class="relative flex flex-col md:flex-row items-center group">
                    <div class="flex items-center justify-center w-12 h-12 rounded-full bg-gold border-2 border-darkgreen text-darkgrey font-extrabold text-base z-10 mb-4 md:mb-0 md:absolute md:left-1/2 md:-translate-x-1/2 shadow-lg">
                        5
                    </div>
                    <div class="w-full md:w-1/2 md:pr-12 md:text-right">
                        <div class="glass-card glass-card-hover p-6 sm:p-8 rounded-2xl border-r-4 border-r-gold">
                            <span class="text-xs font-bold text-gold tracking-widest uppercase block mb-1">Masa Kini & Masa Depan AI</span>
                            <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight mb-3">Pendidikan Era Digital & Kurikulum Merdeka</h3>
                            <p class="text-sm sm:text-base text-beigelight leading-relaxed mb-4">
                                Di era disrupsi teknologi dan Kecerdasan Buatan (AI), lanskap pendidikan menghadapi dilema ganda: apakah teknologi memperluas kebebasan bernalar atau justru melanggengkan alienasi digital?
                            </p>
                            <div class="space-y-2 text-xs sm:text-sm text-beigelight bg-darkgrey/80 p-4 rounded-xl border border-gold/20 text-left mb-4">
                                <p class="font-semibold text-gold">Dinamika Kurikulum Merdeka:</p>
                                <ul class="list-disc pl-4 space-y-1">
                                    <li>Mencoba menghidupkan kembali spirit Ki Hadjar Dewantara melalui <strong>Profil Pelajar Pancasila</strong>.</li>
                                    <li>Pengembangan diferensiasi belajar dan keterampilan abad 21 (Critical Thinking, Communication, Collaboration, Creativity).</li>
                                    <li>Tantangan komodifikasi platform digital dan ancaman hilangnya empati mendalam akibat interaksi teknologis.</li>
                                </ul>
                            </div>
                            <div class="inline-flex items-center gap-2 text-xs sm:text-sm font-semibold text-gold bg-darkgreen px-3.5 py-2 rounded-lg border border-gold/30">
                                <i data-lucide="cpu" class="w-4 h-4"></i> Muara: Adaptabilitas Digital & Rekonsiliasi Humanisme
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block md:w-1/2"></div>
                </div>

            </div>
        </div>
    </section>

    <!-- Filsafat Section -->
    <section id="filsafat" class="py-24 bg-darkgreen/30 relative border-t border-gold/20">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-gold text-xs sm:text-sm font-bold tracking-widest uppercase mb-2 block">Analisis Kerangka Filsafat</span>
                <h2 class="font-serif text-3xl sm:text-5xl font-extrabold text-beigelight mb-4">Dimensi Ontologi & Aksiologi</h2>
                <p class="text-beigelight text-base sm:text-lg">
                    Membedah esensi pendidikan menggunakan pisau analisis filosofis: dari hakikat keberadaan manusia hingga susunan nilai luhur yang hendak diwujudkan.
                </p>
            </div>

            <!-- Tab Navigation Buttons -->
            <div class="flex justify-center mb-10">
                <div class="bg-darkgrey p-2 rounded-2xl border border-gold/40 inline-flex space-x-2 shadow-2xl">
                    <button id="btn-ontologi" onclick="switchPhilosophicalTab('ontologi')" class="px-6 py-3 rounded-xl text-sm sm:text-base font-bold transition bg-gold text-darkgrey shadow-md">
                        <i data-lucide="user-check" class="w-5 h-5 inline-block mr-2"></i> Ontologi: Hakikat Manusia
                    </button>
                    <button id="btn-aksiologi" onclick="switchPhilosophicalTab('aksiologi')" class="px-6 py-3 rounded-xl text-sm sm:text-base font-bold transition text-beigelight hover:text-gold">
                        <i data-lucide="heart-handshake" class="w-5 h-5 inline-block mr-2"></i> Aksiologi: Nilai Kebajikan
                    </button>
                </div>
            </div>

            <!-- Tab Content Display -->
            <div id="tab-content-container">
                <!-- Ontologi Content -->
                <div id="content-ontologi" class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <div class="glass-card p-8 rounded-2xl border-t-4 border-t-gold space-y-4">
                        <div class="w-14 h-14 rounded-2xl bg-darkgreen flex items-center justify-center text-gold border border-gold/40 shadow-inner">
                            <i data-lucide="sparkles" class="w-7 h-7"></i>
                        </div>
                        <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight">1. Manusia Utuh Berbudi Pekerti (Ki Hadjar Dewantara)</h3>
                        <p class="text-sm sm:text-base text-beigelight leading-relaxed">
                            Secara ontologis, manusia bukanlah sekadar sekumpulan urat saraf dan otot mekanis yang disiapkan untuk menggerakkan mesin industri. Manusia adalah makhluk spiritual dan sosial yang memiliki kecerdasan <strong>Cipta (Nalar)</strong>, <strong>Rasa (Emosi & Empati)</strong>, dan <strong>Karsa (Kemauan/Tindakan)</strong>.
                        </p>
                        <div class="p-4 bg-darkgrey/90 rounded-xl border border-gold/20 space-y-2 text-xs sm:text-sm text-beigelight">
                            <p class="font-bold text-gold">Tujuan Pembentukan Manusia:</p>
                            <p>• Memiliki kebebasan internal (bebas dari rasa takut dan ketergantungan mental).</p>
                            <p>• Mampu berdiri di atas kaki sendiri (<em>mandiri</em>) dalam menjaga kehormatan diri dan masyarakatnya.</p>
                        </div>
                    </div>

                    <div class="glass-card p-8 rounded-2xl border-t-4 border-t-gold space-y-4">
                        <div class="w-14 h-14 rounded-2xl bg-darkgreen flex items-center justify-center text-gold border border-gold/40 shadow-inner">
                            <i data-lucide="shield-alert" class="w-7 h-7"></i>
                        </div>
                        <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight">2. Proses Humanisasi Kritis (Paulo Freire)</h3>
                        <p class="text-sm sm:text-base text-beigelight leading-relaxed">
                            Dalam karya kuncinya <em>Pedagogy of the Oppressed</em>, Freire menegaskan bahwa ontologi manusia adalah <strong>Humanisasi</strong> (proses menjadi manusia seutuhnya). Ketika sekolah hanya mengajarkan kepatuhan pasif tanpa nalar kritis, terjadi proses <strong>Dehumanisasi</strong>—di mana manusia direduksi menjadi objek penurut (<em>banking education</em>).
                        </p>
                        <div class="p-4 bg-darkgrey/90 rounded-xl border border-gold/20 space-y-2 text-xs sm:text-sm text-beigelight">
                            <p class="font-bold text-gold">Langkah Transformatif Freire:</p>
                            <p>• Mengubah <em>Kesadaran Magis/Naif</em> (pasrah pada nasib) menjadi <em>Kesadaran Kritis</em>.</p>
                            <p>• Melakukan dialog interaktif antara guru dan siswa sebagai sesama subjek pembelajar.</p>
                        </div>
                    </div>
                </div>

                <!-- Aksiologi Content (Hidden by default) -->
                <div id="content-aksiologi" class="grid grid-cols-1 md:grid-cols-2 gap-8 hidden">
                    <div class="glass-card p-8 rounded-2xl border-t-4 border-t-gold space-y-4">
                        <div class="w-14 h-14 rounded-2xl bg-darkgreen flex items-center justify-center text-gold border border-gold/40 shadow-inner">
                            <i data-lucide="compass" class="w-7 h-7"></i>
                        </div>
                        <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight">1. Etika Social & Keadilan Kemanusiaan</h3>
                        <p class="text-sm sm:text-base text-beigelight leading-relaxed">
                            Aksiologi mempertanyakan: <em>untuk apa ilmu tersebut digunakan?</em> Jika nilai tertinggi pendidikan hanya diletakkan pada besarnya penghasilan finansial pribadi, maka ilmu pengetahuan rentan disalahgunakan untuk mengeksploitasi sesama. Nilai sejati ilmu terletak pada pengabdian sosial (<em>bonum commune</em>).
                        </p>
                        <div class="p-4 bg-darkgrey/90 rounded-xl border border-gold/20 space-y-2 text-xs sm:text-sm text-beigelight">
                            <p class="font-bold text-gold">Nilai-Nilai Utama:</p>
                            <p>• Keberpihakan pada keadilan sosial dan penghapusan penindasan.</p>
                            <p>• Solider terhadap penderitaan sesama dan kelestarian ekologi alam.</p>
                        </div>
                    </div>

                    <div class="glass-card p-8 rounded-2xl border-t-4 border-t-gold space-y-4">
                        <div class="w-14 h-14 rounded-2xl bg-darkgreen flex items-center justify-center text-gold border border-gold/40 shadow-inner">
                            <i data-lucide="scale" class="w-7 h-7"></i>
                        </div>
                        <h3 class="font-serif text-2xl sm:text-3xl font-bold text-beigelight">2. Keseimbangan Antara Bekerja & Kemanusiaan</h3>
                        <p class="text-sm sm:text-base text-beigelight leading-relaxed">
                            Keterampilan vokasional untuk bekerja merupakan <em>Nilai Instrumental</em> (alat mempertahankan hidup fisik). Namun nilai tersebut tidak boleh mengorbankan <em>Nilai Intrinsik</em> manusia (martabat, kejujuran, dan kebebasan berpikir).
                        </p>
                        <div class="p-4 bg-darkgrey/90 rounded-xl border border-gold/20 space-y-2 text-xs sm:text-sm text-beigelight">
                            <p class="font-bold text-gold">Aksiologi Terintegrasi:</p>
                            <p>• Pekerjaan dipandang sebagai sarana mengaktualisasikan kebaikan dan karya seni kehidupan.</p>
                            <p>• Mencegah keterasingan (<em>alienasi</em>) manusia dari hasil karyanya sendiri.</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Conceptual Comparison Matrix -->
            <div class="mt-14 glass-card p-6 sm:p-10 rounded-3xl border border-gold/40 shadow-2xl">
                <h3 class="font-serif text-2xl sm:text-3xl font-bold text-gold mb-6 text-center">Tabel Perbandingan Paradigma Pendidikan</h3>
                <div class="overflow-x-auto">
                    <table class="w-full text-sm sm:text-base text-left text-beigelight">
                        <thead class="text-xs sm:text-sm uppercase bg-darkgrey text-gold border-b-2 border-gold/30">
                            <tr>
                                <th class="py-4 px-4 font-bold">Dimensi Analisis</th>
                                <th class="py-4 px-4 font-bold">Paradigma Teknokratis (Pasar Kerja)</th>
                                <th class="py-4 px-4 font-bold">Paradigma Humanistik (KHD & Freire)</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-gold/20">
                            <tr class="hover:bg-darkgreen/40 transition">
                                <td class="py-4 px-4 font-bold text-gold">Orientasi Utama</td>
                                <td class="py-4 px-4">Efisiensi ekonomi, utilitas industri, komodifikasi modal.</td>
                                <td class="py-4 px-4">Memanusiakan manusia, kemerdekaan jiwa, dan keadilan sosial.</td>
                            </tr>
                            <tr class="hover:bg-darkgreen/40 transition">
                                <td class="py-4 px-4 font-bold text-gold">Posisi Siswa</td>
                                <td class="py-4 px-4">Objek penerima informasi, calon angkatan kerja pabrik.</td>
                                <td class="py-4 px-4">Subjek unik pembelajar yang dituntun sesuai potensi alamiahnya.</td>
                            </tr>
                            <tr class="hover:bg-darkgreen/40 transition">
                                <td class="py-4 px-4 font-bold text-gold">Peran Guru</td>
                                <td class="py-4 px-4">Instruktur kurikulum baku, pengawas standar tes.</td>
                                <td class="py-4 px-4">Fasilitator, pamong yang menuntun (*Sistem Among*), dan mitra dialog.</td>
                            </tr>
                            <tr class="hover:bg-darkgreen/40 transition">
                                <td class="py-4 px-4 font-bold text-gold">Indikator Sukses</td>
                                <td class="py-4 px-4">Ijazah, IPK, besaran gaji, serapan pasar kerja cepat.</td>
                                <td class="py-4 px-4">Kebijaksanaan budi pekerti, kesadaran kritis, kebermanfaatan hidup.</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

        </div>
    </section>

    <!-- Poster Utama Section -->
    <section id="poster" class="py-24 bg-darkgrey border-t-2 border-b-2 border-gold/30 relative overflow-hidden">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 text-center">

            <!-- Poster Frame Design -->
            <div class="relative bg-gradient-to-b from-darkgreen via-darkgreenlight to-darkgrey p-8 sm:p-16 rounded-3xl border-4 border-gold shadow-2xl gold-border-glow max-w-3xl mx-auto text-center overflow-hidden">
                
                <!-- Corner Accents -->
                <div class="absolute top-0 left-0 w-full h-3 bg-gradient-to-r from-gold via-beigelight to-gold"></div>
                <div class="absolute top-4 left-4 w-6 h-6 border-t-2 border-l-2 border-gold"></div>
                <div class="absolute top-4 right-4 w-6 h-6 border-t-2 border-r-2 border-gold"></div>
                <div class="absolute bottom-4 left-4 w-6 h-6 border-b-2 border-l-2 border-gold"></div>
                <div class="absolute bottom-4 right-4 w-6 h-6 border-b-2 border-r-2 border-gold"></div>

                <span class="inline-block px-4 py-1.5 rounded-full bg-darkgrey border border-gold text-gold text-xs uppercase tracking-widest font-extrabold mb-8 shadow-md">
                    POSTER REFLEKSI FILOSOFIS
                </span>

                <!-- Prominent Hook Statement -->
                <h2 class="font-serif text-3xl sm:text-5xl lg:text-6xl font-black text-beigelight leading-snug sm:leading-tight tracking-tight mb-8 drop-shadow-lg">
                    “Apakah sekolah kita sedang mempersiapkan manusia untuk hidup, atau hanya tenaga kerja untuk bekerja?”
                </h2>

                <div class="w-32 h-1.5 bg-gold mx-auto rounded-full mb-6"></div>

                <p class="text-sm sm:text-base text-beigelight/90 italic font-serif">
                    — Menelusuri Kembali Akar Kemanusiaan dalam Pendidikan Indonesia —
                </p>
            </div>

        </div>
    </section>

    <!-- Refleksi Section -->
    <section id="refleksi" class="py-24 bg-darkgrey relative">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 text-center">
            
            <div class="w-20 h-20 rounded-full bg-gold/10 border-2 border-gold flex items-center justify-center text-gold mx-auto mb-6 shadow-xl">
                <i data-lucide="brain-circuit" class="w-10 h-10"></i>
            </div>

            <span class="text-gold text-xs sm:text-sm font-bold tracking-widest uppercase mb-2 block">Sintesis Dialektika</span>
            <h2 class="font-serif text-3xl sm:text-5xl font-extrabold text-beigelight mb-10">Refleksi Kemanusiaan & Masa Depan</h2>

            <!-- Expanded Critical Reflection Content -->
            <div class="glass-card p-8 sm:p-14 rounded-3xl border border-gold/40 text-left mb-12 shadow-2xl relative space-y-6 text-beigelight text-base sm:text-lg leading-relaxed font-normal">
                
                <h3 class="font-serif text-2xl sm:text-3xl font-bold text-gold border-b border-gold/30 pb-3">
                    Bekerja untuk Hidup, Bukan Hidup untuk Bekerja
                </h3>

                <p>
                    Ketika sistem persekolahan bertekuk lutut sepenuhnya pada tuntutan efisiensi pasar modal, peserta didik pelan-pelan kehilangan daya reflektifnya. Mereka dilatih untuk menjawab soal pilihan ganda, menghafal formula kaku, serta tunduk pada perintah hirarki tanpa pernah diajak mempertanyakan: <em>Mengapa dunia ini tidak adil? Apa arti kebahagiaan sejati? Bagaimana cara saya berkontribusi bagi kemanusiaan?</em>
                </p>

                <p>
                    Akibatnya, ketika lulus sekolah atau kuliah, lahirlah generasi yang rapuh secara mental, mudah terasing (<em>alienated</em>), serta rentan mengalami krisis identitas ketika kehilangan pekerjaan. <strong>Bekerja adalah hak dan kebutuhan hidup fisik manusia, namun pekerjaan bukanlah satu-satunya takdir eksistensi manusia.</strong>
                </p>

                <div class="p-6 bg-darkgreen/80 rounded-2xl border-l-4 border-l-gold text-beigelight space-y-3 font-serif italic text-lg sm:text-xl my-6">
                    “Anak-anak hidup dan tumbuh sesuai kodratnya sendiri. Pendidik hanya dapat menuntun tumbuhnya kodrat itu.”
                    <span class="block text-xs font-sans not-italic text-gold font-bold uppercase tracking-wider mt-2">— Ki Hadjar Dewantara</span>
                </div>

                <p>
                    Kecerdasan buatan (AI) hari ini dengan sangat cepat mengambil alih tugas-tugas teknis, kognitif rutin, dan komputasi data. Jika persekolahan kita masih ngotot mencetak manusia yang sekadar pandai menjalankan rutinitas teknis mekanis, maka manusia akan kalah bersaing dengan mesin buatannya sendiri. <strong>Inilah momentum sejarah bagi pendidikan untuk kembali ke khittahnya: mengasah empati, nurani, kearifan lokal, daya cipta seni, dan kedalaman spiritual.</strong>
                </p>
            </div>

            <!-- Grand Synthesis / Final Conclusion Quote Card -->
            <div class="p-8 sm:p-14 rounded-3xl bg-gradient-to-br from-darkgreen via-darkgreenlight to-darkgrey border-4 border-gold shadow-2xl relative overflow-hidden text-center gold-border-glow">
                <i data-lucide="quote" class="w-20 h-20 text-gold/20 mx-auto mb-4"></i>
                
                <span class="text-xs uppercase tracking-widest text-gold font-bold mb-4 block">Gagasan Penutup Paling Mendasar</span>
                
                <blockquote class="font-serif text-2xl sm:text-4xl lg:text-5xl font-bold text-beigelight leading-snug tracking-tight mb-8">
                    “Mungkin tujuan pendidikan bukan memilih antara menjadi manusia atau menjadi pekerja. Mungkin pendidikan seharusnya membuat kita mampu bekerja tanpa kehilangan kemanusiaan.”
                </blockquote>

                <div class="inline-flex items-center gap-2 text-xs sm:text-sm text-beigelight bg-darkgrey/90 px-5 py-2.5 rounded-full border border-gold">
                    <i data-lucide="feather" class="w-4 h-4 text-gold"></i> Renungan Reflektif Pendidikan Indonesia
                </div>
            </div>

        </div>
    </section>

    <!-- Daftar Pustaka Section -->
    <section id="pustaka" class="py-20 bg-darkgrey border-t border-gold/30">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-center justify-between mb-10 pb-4 border-b border-gold/30 gap-4">
                <div>
                    <span class="text-gold text-xs font-bold tracking-widest uppercase block mb-1">Rujukan Literatur Kunci</span>
                    <h2 class="font-serif text-3xl font-extrabold text-beigelight">Daftar Pustaka Lengkap</h2>
                </div>
                
                <!-- Interactive Search Filter -->
                <div class="relative w-full md:w-80">
                    <input type="text" id="bib-search" onkeyup="filterBibliography()" placeholder="Cari nama penulis / judul..." class="w-full bg-darkgreen/60 border border-gold/50 rounded-xl px-4 py-2.5 text-sm text-beigelight placeholder-beigelight/50 focus:outline-none focus:border-gold shadow-inner">
                    <i data-lucide="search" class="w-4 h-4 text-gold absolute right-3.5 top-3.5"></i>
                </div>
            </div>

            <!-- List of 8 References with High Contrast & Complete Details -->
            <div id="bib-list" class="space-y-4 text-sm sm:text-base">
                
                <!-- 1 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Dewantara, K. H.</strong> (2013). <em>Ki Hadjar Dewantara: Bagian pertama pendidikan</em>. Yogyakarta: Majelis Luhur Persatuan Tamansiswa.
                    </p>
                </div>

                <!-- 2 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Fadhlurrahman.</strong> (2025). Educational journey: From the Roman era, the Dutch colonial period, to Muhammadiyah in Indonesia. <em>Humanika: Kajian Ilmiah Mata Kuliah Umum</em>, 25(1).
                    </p>
                    <a href="https://doi.org/10.21831/hum.v25i1.79883" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/50 px-3.5 py-1.5 rounded-lg hover:bg-gold hover:text-darkgrey transition font-bold flex items-center gap-1 w-fit">
                        DOI Link <i data-lucide="external-link" class="w-3.5 h-3.5"></i>
                    </a>
                </div>

                <!-- 3 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Freire, P.</strong> (1970). <em>Pedagogy of the oppressed</em>. Herder and Herder.
                    </p>
                </div>

                <!-- 4 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Kementerian Pendidikan, Kebudayaan, Riset, dan Teknologi.</strong> (2024). <em>Kurikulum Merdeka: Landasan filosofis dan tujuan Kurikulum Merdeka</em>. Kementerian Pendidikan, Kebudayaan, Riset, dan Teknologi.
                    </p>
                </div>

                <!-- 5 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Rhamadani, A., & Triaristina, A.</strong> (2023). Peran Taman Siswa dalam pembentukan rasa nasionalisme pada masa pergerakan nasional. <em>ISTORIA: Jurnal Pendidikan dan Ilmu Sejarah</em>, 19(1).
                    </p>
                    <a href="https://doi.org/10.21831/istoria.v19i1.53750" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/50 px-3.5 py-1.5 rounded-lg hover:bg-gold hover:text-darkgrey transition font-bold flex items-center gap-1 w-fit">
                        DOI Link <i data-lucide="external-link" class="w-3.5 h-3.5"></i>
                    </a>
                </div>

                <!-- 6 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Riberu, K., & Rosvita, L. A.</strong> (2020). Education foundation: History (history as the basis of education). <em>Jurnal Pembangunan Pendidikan: Fondasi dan Aplikasi</em>, 8(1).
                    </p>
                    <a href="https://doi.org/10.21831/jppfa.v8i1.35988" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/50 px-3.5 py-1.5 rounded-lg hover:bg-gold hover:text-darkgrey transition font-bold flex items-center gap-1 w-fit">
                        DOI Link <i data-lucide="external-link" class="w-3.5 h-3.5"></i>
                    </a>
                </div>

                <!-- 7 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Riski, M. A., Haq, M. A., & Daristin, P. E.</strong> (2026). Pendidikan sebagai proses humanisasi: Analisis pemikiran Paulo Freire. <em>Education: Jurnal Sosial Humaniora dan Pendidikan</em>, 6(2).
                    </p>
                    <a href="https://doi.org/10.51903/maedx172" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/50 px-3.5 py-1.5 rounded-lg hover:bg-gold hover:text-darkgrey transition font-bold flex items-center gap-1 w-fit">
                        DOI Link <i data-lucide="external-link" class="w-3.5 h-3.5"></i>
                    </a>
                </div>

                <!-- 8 -->
                <div class="bib-item glass-card p-5 rounded-xl border border-gold/30 hover:border-gold transition flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                    <p class="text-beigelight leading-relaxed">
                        <strong class="text-gold font-bold">Thaariq, Z. Z. A., & Karima, U.</strong> (2023). Menelisik pemikiran Ki Hadjar Dewantara dalam konteks pembelajaran abad 21: Sebuah renungan dan inspirasi. <em>FOUNDASIA</em>, 14(2).
                    </p>
                    <a href="https://doi.org/10.21831/foundasia.v14i2.63740" target="_blank" rel="noopener noreferrer" class="shrink-0 text-xs text-gold border border-gold/50 px-3.5 py-1.5 rounded-lg hover:bg-gold hover:text-darkgrey transition font-bold flex items-center gap-1 w-fit">
                        DOI Link <i data-lucide="external-link" class="w-3.5 h-3.5"></i>
                    </a>
                </div>

            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-darkgrey border-t border-gold/20 py-10 text-center text-xs sm:text-sm text-beigelight/80">
        <div class="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-4">
            <p>© Kajian Historis & Filosofis Pendidikan Indonesia.</p>
            <p class="text-gold font-medium">Palet Warna: Dark Green (#263D32) • Beige (#E8DCC8) • Hitam (#191919) • Gold (#B08D57)</p>
        </div>
    </footer>

    <!-- Interactive Client Scripts -->
    <script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Reading Scroll Progress Indicator
        window.addEventListener('scroll', () => {
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            document.getElementById('progress-bar').style.width = scrolled + '%';
        });

        // Mobile Menu Controls
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Poll Voting Mechanics
        let pollVoted = false;
        function votePoll(index) {
            if(pollVoted) return;
            pollVoted = true;

            const feedback = document.getElementById('poll-feedback');
            feedback.classList.remove('hidden');

            const counts = ['43%', '32%', '28%'];
            document.getElementById(`poll-count-${index}`).innerText = counts[index] + ' (Pilihan Anda)';
            document.getElementById(`poll-count-${index}`).className = 'text-xs sm:text-sm bg-gold text-darkgrey font-extrabold px-3 py-1.5 rounded-lg shadow';
        }

        // Philosophical Tab Switcher Function
        function switchPhilosophicalTab(tab) {
            const btnOntologi = document.getElementById('btn-ontologi');
            const btnAksiologi = document.getElementById('btn-aksiologi');
            const contentOntologi = document.getElementById('content-ontologi');
            const contentAksiologi = document.getElementById('content-aksiologi');

            if (tab === 'ontologi') {
                btnOntologi.className = "px-6 py-3 rounded-xl text-sm sm:text-base font-bold transition bg-gold text-darkgrey shadow-md";
                btnAksiologi.className = "px-6 py-3 rounded-xl text-sm sm:text-base font-bold transition text-beigelight hover:text-gold";
                contentOntologi.classList.remove('hidden');
                contentAksiologi.classList.add('hidden');
            } else {
                btnAksiologi.className = "px-6 py-3 rounded-xl text-sm sm:text-base font-bold transition bg-gold text-darkgrey shadow-md";
                btnOntologi.className = "px-6 py-3 rounded-xl text-sm sm:text-base font-bold transition text-beigelight hover:text-gold";
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
