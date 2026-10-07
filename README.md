<!DOCTYPE html>
<html lang="zh-TW" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>政儒 & 怡靜 婚禮邀請函</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Cormorant Garamond & Noto Serif TC -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Noto+Serif+TC:wght@300;400;500;600&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        morandi: {
                            sand: '#d4a373',
                            sage: '#8da399',
                            cream: '#fefae0',
                            dark: '#3a3a3a',
                            lightbg: '#f9f8f6',
                            cardbg: '#ffffff',
                            muted: '#a3b18b'
                        }
                    },
                    fontFamily: {
                        serif: ['"Noto Serif TC"', '"Cormorant Garamond"', 'serif'],
                        en: ['"Cormorant Garamond"', 'serif']
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Noto Serif TC', serif;
            background-color: #f9f8f6;
            color: #3a3a3a;
            overflow-x: hidden;
        }
        .en-font {
            font-family: 'Cormorant Garamond', serif;
        }
        .glass-nav {
            background: rgba(254, 250, 224, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
        }
        .nowrap-text {
            white-space: nowrap;
        }
        /* 隱藏捲軸但保持滾動功能 */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="bg-morandi-lightbg text-morandi-dark antialiased">

    <!-- 1. 固定的毛玻璃質感導航列 -->
    <header class="fixed top-0 left-0 right-0 z-50 glass-nav border-b border-morandi-sand/20 transition-all duration-300">
        <div class="max-w-6xl mx-auto px-6 h-20 flex items-center justify-between">
            <a href="#hero" class="en-font text-2xl md:text-3xl tracking-wider font-semibold text-morandi-dark hover:opacity-80 transition">
                Zheng-Ru & Yi-Jing
            </a>
            <nav class="hidden md:flex items-center space-x-10 text-sm tracking-widest font-medium">
                <a href="#about" class="hover:text-morandi-sand transition">關於我們 / ABOUT</a>
                <a href="#details" class="hover:text-morandi-sand transition">婚禮詳情 / DETAILS</a>
                <a href="#rsvp" class="hover:text-morandi-sand transition">出席回函 / RSVP</a>
            </nav>
            <!-- 手機版漢堡選單按鈕 -->
            <button id="menu-btn" class="md:hidden text-morandi-dark focus:outline-none p-2" aria-label="選單">
                <i class="fa-solid fa-bars text-xl"></i>
            </button>
        </div>
        <!-- 手機版下拉選單 -->
        <div id="mobile-menu" class="hidden md:hidden glass-nav border-b border-morandi-sand/20 px-6 py-4 flex flex-col space-y-3 text-sm tracking-wider">
            <a href="#about" class="mobile-link py-2 hover:text-morandi-sand transition">關於我們 / ABOUT</a>
            <a href="#details" class="mobile-link py-2 hover:text-morandi-sand transition">婚禮詳情 / DETAILS</a>
            <a href="#rsvp" class="mobile-link py-2 hover:text-morandi-sand transition">出席回函 / RSVP</a>
        </div>
    </header>

    <!-- 3. 首頁全螢幕封面背景 -->
    <section id="hero" class="relative h-screen w-full flex items-center justify-center overflow-hidden">
        <!-- 背景圖片與柔和遮罩 -->
        <div class="absolute inset-0 z-0">
            <img src="https://i.postimg.cc/tgMnz6H1/0J7A8207.jpg" alt="政儒與怡靜婚紗照" class="w-full h-full object-cover object-center scale-105 animate-pulse duration-1000" style="animation-duration: 8s;" onerror="this.src='https://placehold.co/1920x1080/d4a373/ffffff?text=Wedding'">
            <div class="absolute inset-0 bg-gradient-to-b from-black/40 via-black/20 to-black/50"></div>
        </div>
        
        <!-- 首頁文案內容 -->
        <div class="relative z-10 text-center px-4 max-w-4xl mx-auto mt-12 text-white">
            <p class="en-font text-xl md:text-2xl tracking-[0.3em] mb-4 text-morandi-cream font-light uppercase">The Wedding Invitation</p>
            <h1 class="text-4xl md:text-7xl font-serif tracking-widest mb-6 font-normal drop-shadow-md">
                政儒 <span class="en-font text-3xl md:text-5xl text-morandi-sand font-light">&amp;</span> 怡靜
            </h1>
            <p class="text-lg md:text-xl font-light tracking-[0.2em] mb-8 text-morandi-cream/90">
                我們的婚禮邀請
            </p>
            <div class="w-16 h-[1px] bg-morandi-sand mx-auto mb-8"></div>
            <p class="en-font text-lg md:text-2xl tracking-widest text-morandi-cream">
                2027.03.06 <span class="text-morandi-sand mx-2">|</span> Wedding Day
            </p>
        </div>

        <!-- 向下滾動提示 -->
        <a href="#about" class="absolute bottom-8 left-1/2 transform -translate-x-1/2 z-10 text-white/80 hover:text-white transition animate-bounce">
            <i class="fa-solid fa-chevron-down text-xl"></i>
        </a>
    </section>

    <!-- 2. 藝術感倒數計時器視覺 (極重要) -->
    <section class="py-20 bg-morandi-cream/60 border-b border-morandi-sand/10">
        <div class="max-w-4xl mx-auto px-6 text-center">
            <h2 class="text-2xl md:text-3xl font-serif tracking-widest mb-2 text-morandi-dark">距離幸福時刻</h2>
            <p class="en-font text-sm text-morandi-sand uppercase tracking-[0.2em] mb-10">Countdown to Our Special Day</p>
            
            <div id="countdown-container" class="grid grid-cols-2 md:grid-cols-4 gap-4 md:gap-6 justify-center items-center max-w-3xl mx-auto">
                <!-- 天數 -->
                <div class="bg-white rounded-2xl p-6 shadow-[0_10px_30px_rgba(212,163,115,0.12)] border border-morandi-sand/20 flex flex-col items-center relative">
                    <span id="days" class="en-font text-4xl md:text-6xl font-semibold text-morandi-dark mb-1">--</span>
                    <span class="text-xs md:text-sm tracking-widest text-morandi-dark/60 uppercase">Days / 天</span>
                </div>
                <!-- 時數 -->
                <div class="bg-white rounded-2xl p-6 shadow-[0_10px_30px_rgba(212,163,115,0.12)] border border-morandi-sand/20 flex flex-col items-center relative">
                    <span id="hours" class="en-font text-4xl md:text-6xl font-semibold text-morandi-dark mb-1">--</span>
                    <span class="text-xs md:text-sm tracking-widest text-morandi-dark/60 uppercase">Hours / 時</span>
                </div>
                <!-- 分鐘 -->
                <div class="bg-white rounded-2xl p-6 shadow-[0_10px_30px_rgba(212,163,115,0.12)] border border-morandi-sand/20 flex flex-col items-center relative">
                    <span id="minutes" class="en-font text-4xl md:text-6xl font-semibold text-morandi-dark mb-1">--</span>
                    <span class="text-xs md:text-sm tracking-widest text-morandi-dark/60 uppercase">Minutes / 分</span>
                </div>
                <!-- 秒數 -->
                <div class="bg-white rounded-2xl p-6 shadow-[0_10px_30px_rgba(212,163,115,0.12)] border border-morandi-sand/20 flex flex-col items-center relative">
                    <span id="seconds" class="en-font text-4xl md:text-6xl font-semibold text-morandi-dark mb-1">--</span>
                    <span class="text-xs md:text-sm tracking-widest text-morandi-dark/60 uppercase">Seconds / 秒</span>
                </div>
            </div>
        </div>
    </section>

    <!-- 關於我們與相片藝廊 -->
    <section id="about" class="py-24 px-6 max-w-5xl mx-auto">
        <div class="text-center mb-16">
            <span class="en-font text-morandi-sand uppercase tracking-[0.3em] text-sm block mb-2">Our Story</span>
            <h2 class="text-3xl md:text-4xl font-serif tracking-widest text-morandi-dark">關於我們</h2>
            <div class="w-12 h-[1px] bg-morandi-sand mx-auto mt-4"></div>
        </div>

        <div class="grid md:grid-cols-2 gap-12 items-center mb-20">
            <div class="space-y-6 text-morandi-dark/80 leading-relaxed font-light text-justify md:text-left">
                <p class="text-lg font-serif text-morandi-dark italic">「在對的時間遇見對的人，是一生最美的幸運。」</p>
                <p>我們相知相惜走過了許多美好的歲月，在彼此的陪伴中看見了未來的模樣。懷著感恩與喜悅的心情，我們決定攜手邁向人生的下一個階段。</p>
                <p>誠摯地邀請您一同來見證我們的幸福時刻，分享我們的喜悅，您的祝福將為我們的婚禮增添最美的光彩。</p>
                <div class="pt-4">
                    <span class="en-font text-2xl text-morandi-sand block">Zheng-Ru &amp; Yi-Jing</span>
                </div>
            </div>
            <div class="grid grid-cols-2 gap-4">
                <div class="space-y-4">
                    <div class="overflow-hidden rounded-xl shadow-md aspect-[3/4]">
                        <img src="https://i.postimg.cc/9FY4nKhq/0J7A8218.jpg" alt="婚紗照 1" class="w-full h-full object-cover hover:scale-105 transition duration-500" onerror="this.src='https://placehold.co/600x800/d4a373/ffffff?text=Photo+1'">
                    </div>
                </div>
                <div class="space-y-4 pt-8">
                    <div class="overflow-hidden rounded-xl shadow-md aspect-[3/4]">
                        <img src="https://i.postimg.cc/2SjqRGkn/0J7A8225.jpg" alt="婚紗照 2" class="w-full h-full object-cover hover:scale-105 transition duration-500" onerror
