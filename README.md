[quantumcustom_licences_store-2.html](https://github.com/user-attachments/files/34747565/quantumcustom_licences_store-2.html)
<!DOCTYPE html>
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QuantumCustom - Licences Store | Premium Digital Subscriptions</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        gold: {
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706',
                            700: '#b45309',
                            glow: 'rgba(245, 158, 11, 0.35)'
                        },
                        obsidian: {
                            900: '#090a0f',
                            800: '#11131c',
                            700: '#1a1d29',
                            600: '#25293a'
                        },
                        khqr: '#E21A22'
                    },
                    boxShadow: {
                        'gold-glow': '0 0 25px rgba(245, 158, 11, 0.25)',
                        'card-glow': '0 10px 30px -10px rgba(0, 0, 0, 0.5)'
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- QRCode.js Library -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
    <!-- Google Font Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-attachment: fixed;
        }
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #090a0f;
        }
        ::-webkit-scrollbar-thumb {
            background: #25293a;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #f59e0b;
        }
        .gold-gradient-text {
            background: linear-gradient(135deg, #FFF 0%, #fbbf24 50%, #d97706 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-border {
            border-image: linear-gradient(to right, #f59e0b, #d97706, #fbbf24) 1;
        }
        .khqr-card-shadow {
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
        }
    </style>
</head>
<body class="bg-obsidian-900 text-slate-100 dark:bg-obsidian-900 dark:text-slate-100 min-h-screen transition-colors duration-300">

    <!-- Toast Notification Container -->
    <div id="toast-container" class="fixed top-5 right-5 z-50 flex flex-col gap-3 max-w-sm w-full pointer-events-none"></div>

    <!-- MAIN HEADER / NAVBAR -->
    <header class="sticky top-0 z-40 backdrop-blur-md bg-obsidian-900/85 dark:bg-obsidian-900/85 bg-white/90 text-slate-800 dark:text-slate-100 border-b border-amber-500/20 shadow-lg transition-colors">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            
            <!-- Brand Logo & Title -->
            <div class="flex items-center gap-3 cursor-pointer" onclick="scrollToTop()">
                <div id="app-logo-container" class="w-12 h-12 flex items-center justify-center relative">
                    <!-- Default SVG Golden Microchip Logo -->
                    <svg id="default-qc-logo" class="w-12 h-12 drop-shadow-[0_0_10px_rgba(245,158,11,0.5)]" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <defs>
                            <linearGradient id="goldGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#FFE259" />
                                <stop offset="100%" stop-color="#FFA751" />
                            </linearGradient>
                            <linearGradient id="darkGold" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#d97706" />
                                <stop offset="100%" stop-color="#78350f" />
                            </linearGradient>
                        </defs>
                        <!-- Hexagonal Outer Microchip Frame -->
                        <polygon points="50,5 90,27.5 90,72.5 50,95 10,72.5 10,27.5" fill="url(#darkGold)" stroke="url(#goldGrad)" stroke-width="3" />
                        <!-- Inner Chip Grid Lines -->
                        <path d="M50,15 L50,85 M20,32.5 L80,67.5 M20,67.5 L80,32.5" stroke="url(#goldGrad)" stroke-width="1" stroke-opacity="0.4" stroke-dasharray="2 2" />
                        <!-- Center Core Monogram -->
                        <circle cx="50" cy="50" r="28" fill="#090a0f" stroke="url(#goldGrad)" stroke-width="2.5" />
                        <!-- QC Monogram Text -->
                        <text x="50%" y="57%" text-anchor="middle" font-family="'Inter', sans-serif" font-weight="900" font-size="22" fill="url(#goldGrad)" letter-spacing="-1">QC</text>
                        <!-- Corner Node Pins -->
                        <circle cx="50" cy="5" r="3" fill="#FFE259" />
                        <circle cx="90" cy="27.5" r="3" fill="#FFE259" />
                        <circle cx="90" cy="72.5" r="3" fill="#FFE259" />
                        <circle cx="50" cy="95" r="3" fill="#FFE259" />
                        <circle cx="10" cy="72.5" r="3" fill="#FFE259" />
                        <circle cx="10" cy="27.5" r="3" fill="#FFE259" />
                    </svg>
                    <!-- Container for custom image logo if set -->
                    <img id="custom-qc-logo" class="hidden w-12 h-12 object-contain rounded-lg border border-amber-500/40" src="" alt="QuantumCustom Logo">
                </div>

                <div>
                    <div class="flex items-center gap-2">
                        <span class="text-xl sm:text-2xl font-black tracking-wider text-slate-900 dark:text-white">Quantum<span class="gold-gradient-text">Custom</span></span>
                        <span class="text-[10px] font-semibold bg-amber-500/20 text-amber-500 border border-amber-500/40 px-2 py-0.5 rounded-full uppercase tracking-widest hidden sm:inline-block">PRO</span>
                    </div>
                    <p class="text-xs text-amber-500/90 font-medium tracking-wide">Licences Store • Digital Subscriptions</p>
                </div>
            </div>

            <!-- Header Action Controls -->
            <div class="flex items-center gap-2 sm:gap-4">
                
                <!-- Currency Toggle Button -->
                <div class="bg-obsidian-800 border border-amber-500/30 p-1 rounded-xl flex items-center gap-1 shadow-inner">
                    <button id="curr-usd-btn" onclick="setCurrency('USD')" class="px-2.5 py-1 text-xs font-bold rounded-lg transition-all bg-amber-500 text-obsidian-900 shadow">
                        USD ($)
                    </button>
                    <button id="curr-khr-btn" onclick="setCurrency('KHR')" class="px-2.5 py-1 text-xs font-bold rounded-lg transition-all text-slate-400 hover:text-white">
                        KHR (៛)
                    </button>
                </div>

                <!-- Theme Toggle Button -->
                <button onclick="toggleTheme()" class="w-10 h-10 rounded-xl bg-obsidian-800/80 dark:bg-obsidian-800/80 bg-slate-100 border border-amber-500/30 flex items-center justify-center text-amber-400 hover:scale-105 transition-all" title="Toggle Light/Dark Theme">
                    <i id="theme-icon" class="fa-solid fa-moon"></i>
                </button>

                <!-- Telegram Direct Button -->
                <a id="telegram-header-link" href="https://t.me/quantumcustomlicences" target="_blank" class="hidden md:flex items-center gap-2 px-3.5 py-2 rounded-xl bg-sky-500/10 hover:bg-sky-500/20 border border-sky-400/40 text-sky-400 text-xs font-bold transition-all hover:scale-105">
                    <i class="fa-brands fa-telegram text-base"></i>
                    <span>Contact Telegram</span>
                </a>

                <!-- Edit Store Mode Button -->
                <button onclick="openEditStoreModal()" class="px-3 py-2 rounded-xl bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-600 hover:to-amber-700 text-obsidian-900 font-bold text-xs flex items-center gap-2 shadow-gold-glow transition-all hover:scale-105">
                    <i class="fa-solid fa-gear"></i>
                    <span class="hidden sm:inline">Edit Store</span>
                </button>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="relative overflow-hidden py-12 sm:py-16 bg-gradient-to-b from-obsidian-900 via-obsidian-800 to-obsidian-900 border-b border-amber-500/10">
        <!-- Glow Orbs BG -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 w-96 h-96 bg-amber-500/10 blur-[120px] rounded-full pointer-events-none"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
            
            <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-amber-500/10 border border-amber-500/30 text-amber-400 text-xs sm:text-sm font-semibold mb-6 animate-pulse">
                <i class="fa-solid fa-bolt-lightning text-amber-400"></i>
                <span>Instant Digital License Delivery & Guaranteed Warranty</span>
            </div>

            <h1 class="text-3xl sm:text-5xl lg:text-6xl font-black text-white tracking-tight leading-tight max-w-4xl mx-auto">
                Elevate Your Digital Experience with <span class="gold-gradient-text">Quantum Custom</span>
            </h1>
            
            <p class="mt-4 text-slate-400 text-sm sm:text-base max-w-2xl mx-auto leading-relaxed">
                Get premium subscriptions for YouTube, AI tools, Streaming, Music, and Design at unbeatable rates. Pay seamlessly with Cambodia's ABA Pay KHQR.
            </p>

            <!-- Trust Badges -->
            <div class="mt-8 flex flex-wrap items-center justify-center gap-4 sm:gap-8 text-xs sm:text-sm text-slate-300">
                <div class="flex items-center gap-2 bg-obsidian-800/80 px-3.5 py-2 rounded-lg border border-slate-700/50">
                    <i class="fa-solid fa-shield-halved text-emerald-400"></i>
                    <span>100% Guaranteed</span>
                </div>
                <div class="flex items-center gap-2 bg-obsidian-800/80 px-3.5 py-2 rounded-lg border border-slate-700/50">
                    <i class="fa-solid fa-qrcode text-red-500"></i>
                    <span>ABA KHQR Checkout</span>
                </div>
                <div class="flex items-center gap-2 bg-obsidian-800/80 px-3.5 py-2 rounded-lg border border-slate-700/50">
                    <i class="fa-brands fa-telegram text-sky-400"></i>
                    <span>Instant Support</span>
                </div>
            </div>
        </div>
    </section>

    <!-- SEARCH & CATEGORY FILTER TABS -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
        
        <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-8">
            <!-- Category Tabs -->
            <div id="category-tabs-container" class="flex items-center gap-2 overflow-x-auto pb-2 md:pb-0 scrollbar-none">
                <!-- JS will inject category buttons here -->
            </div>

            <!-- Search Bar & Order Lookup Trigger -->
            <div class="flex items-center gap-3 w-full md:w-auto">
                <div class="relative w-full md:w-72">
                    <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-1/2 -translate-y-1/2 text-slate-400 text-sm"></i>
                    <input type="text" id="search-input" oninput="handleSearch()" placeholder="Search subscriptions..." class="w-full pl-10 pr-4 py-2.5 rounded-xl bg-obsidian-800 border border-slate-700/80 text-white placeholder-slate-400 text-sm focus:outline-none focus:border-amber-500 transition-all">
                </div>
                <button onclick="openOrderLookupModal()" class="px-3.5 py-2.5 rounded-xl bg-obsidian-800 border border-slate-700/80 text-slate-300 hover:text-white hover:border-amber-500/50 text-xs font-semibold flex items-center gap-2 whitespace-nowrap transition-all">
                    <i class="fa-solid fa-receipt text-amber-400"></i>
                    <span>My Receipt</span>
                </button>
            </div>
        </div>

        <!-- PRODUCTS GRID -->
        <div id="products-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- JS will inject products here -->
        </div>

        <!-- FAQ & GUARANTEE SECTION -->
        <section class="mt-20 pt-12 border-t border-amber-500/10">
            <div class="text-center mb-10">
                <h2 class="text-2xl sm:text-3xl font-black text-white">Frequently Asked <span class="gold-gradient-text">Questions</span></h2>
                <p class="text-slate-400 text-xs sm:text-sm mt-2">Everything you need to know about purchasing and activating your licenses.</p>
            </div>

            <div class="max-w-3xl mx-auto space-y-4">
                <div class="bg-obsidian-800/80 border border-slate-700/60 rounded-xl p-4 sm:p-5">
                    <h3 class="font-bold text-white text-base flex items-center gap-2">
                        <i class="fa-solid fa-bolt text-amber-400"></i> How long does license activation take?
                    </h3>
                    <p class="text-slate-400 text-xs sm:text-sm mt-2 leading-relaxed">
                        After submitting your ABA KHQR payment proof on Telegram, activation is typically processed within 5 to 15 minutes during business hours (8:00 AM - 11:00 PM UTC+7).
                    </p>
                </div>

                <div class="bg-obsidian-800/80 border border-slate-700/60 rounded-xl p-4 sm:p-5">
                    <h3 class="font-bold text-white text-base flex items-center gap-2">
                        <i class="fa-solid fa-shield-heart text-emerald-400"></i> Is there a warranty for full plan duration?
                    </h3>
                    <p class="text-slate-400 text-xs sm:text-sm mt-2 leading-relaxed">
                        Yes! All subscriptions from QuantumCustom come with a 100% full-term replacement warranty. If you experience any issues, our Telegram support team replaces your access immediately.
                    </p>
                </div>

                <div class="bg-obsidian-800/80 border border-slate-700/60 rounded-xl p-4 sm:p-5">
                    <h3 class="font-bold text-white text-base flex items-center gap-2">
                        <i class="fa-solid fa-envelope-open-text text-sky-400"></i> Do I need to provide my account password?
                    </h3>
                    <p class="text-slate-400 text-xs sm:text-sm mt-2 leading-relaxed">
                        For YouTube Premium, Gemini Pro, Spotify, and Canva Pro, we invite your existing Google/Email account directly via Family or Team links—no password required!
                    </p>
                </div>
            </div>
        </section>
    </main>

    <!-- FOOTER -->
    <footer class="mt-20 border-t border-amber-500/20 bg-obsidian-900 py-10 text-slate-400 text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between gap-6">
            <div class="flex items-center gap-3">
                <span class="font-black text-white text-base">Quantum<span class="gold-gradient-text">Custom</span></span>
                <span class="text-slate-600">|</span>
                <span>© 2026 QuantumCustom Licences Store. All Rights Reserved.</span>
            </div>
            <div class="flex items-center gap-6 text-slate-300">
                <a href="#" onclick="openEditStoreModal(); return false;" class="hover:text-amber-400 transition-colors">Admin Settings</a>
                <a id="telegram-footer-link" href="https://t.me/quantumcustomlicences" target="_blank" class="hover:text-amber-400 transition-colors">Telegram Support</a>
            </div>
        </div>
    </footer>

    <!-- FLOATING TELEGRAM BUTTON -->
    <a id="telegram-float-btn" href="https://t.me/quantumcustomlicences" target="_blank" class="fixed bottom-6 right-6 z-40 bg-sky-500 text-white p-4 rounded-full shadow-2xl hover:bg-sky-400 hover:scale-110 transition-all flex items-center justify-center group" title="Contact Support on Telegram">
        <i class="fa-brands fa-telegram text-2xl"></i>
        <span class="max-w-0 overflow-hidden group-hover:max-w-xs transition-all duration-300 ease-in-out whitespace-nowrap font-bold text-xs group-hover:ml-2">Telegram Support</span>
    </a>

    <!-- CHECKOUT & ABA KHQR PAYMENT MODAL -->
    <div id="checkout-modal" class="fixed inset-0 z-50 hidden flex items-center justify-center p-4 bg-black/80 backdrop-blur-md overflow-y-auto">
        <div class="bg-obsidian-800 border border-amber-500/30 rounded-2xl max-w-xl w-full p-6 shadow-card-glow relative my-8">
            
            <!-- Close Button -->
            <button onclick="closeCheckoutModal()" class="absolute top-4 right-4 text-slate-400 hover:text-white text-lg w-8 h-8 flex items-center justify-center rounded-lg bg-obsidian-700/50">
                <i class="fa-solid fa-xmark"></i>
            </button>

            <!-- Checkout Header -->
            <div class="flex items-center gap-3 mb-6 pb-4 border-b border-slate-700">
                <div id="checkout-product-icon" class="w-12 h-12 rounded-xl bg-amber-500/10 border border-amber-500/30 flex items-center justify-center text-amber-400 text-xl">
                    <!-- Icon injected JS -->
                </div>
                <div>
                    <h3 id="checkout-product-name" class="font-black text-xl text-white">Product Name</h3>
                    <p id="checkout-plan-name" class="text-xs text-amber-400 font-semibold">1 Month Access</p>
                </div>
            </div>

            <!-- Customer Details Inputs -->
            <div class="space-y-4 mb-6">
                <div>
                    <label class="block text-xs font-bold text-slate-300 uppercase tracking-wider mb-1">Your Full Name / Telegram</label>
                    <input type="text" id="cust-name-input" placeholder="e.g. John Doe / @johndoe" class="w-full px-3.5 py-2.5 rounded-xl bg-obsidian-900 border border-slate-700 text-white text-sm focus:outline-none focus:border-amber-500">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-300 uppercase tracking-wider mb-1">Your Email (for license invite delivery)</label>
                    <input type="email" id="cust-email-input" placeholder="e.g. customer@gmail.com" class="w-full px-3.5 py-2.5 rounded-xl bg-obsidian-900 border border-slate-700 text-white text-sm focus:outline-none focus:border-amber-500">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-300 uppercase tracking-wider mb-1">Payment Currency</label>
                    <div class="grid grid-cols-2 gap-2">
                        <button id="checkout-pay-usd-btn" onclick="setCheckoutCurrency('USD')" class="py-2 rounded-xl text-xs font-bold border border-amber-500 bg-amber-500 text-obsidian-900">Pay in USD ($)</button>
                        <button id="checkout-pay-khr-btn" onclick="setCheckoutCurrency('KHR')" class="py-2 rounded-xl text-xs font-bold border border-slate-700 bg-obsidian-900 text-slate-300">Pay in KHR (៛)</button>
                    </div>
                </div>
            </div>

            <!-- AUTHENTIC ABA KHQR CARD CONTAINER -->
            <div id="khqr-card-element" class="bg-white text-slate-900 rounded-2xl overflow-hidden border border-slate-300 shadow-2xl mb-6 text-center relative">
                <!-- Red KHQR Header -->
                <div class="bg-khqr py-3.5 px-4 flex items-center justify-between">
                    <div class="flex items-center gap-2">
                        <span class="bg-white text-khqr font-black text-sm px-2 py-0.5 rounded tracking-tighter italic">KHQR</span>
                        <span class="text-white text-xs font-bold tracking-widest uppercase">Bakong Payment</span>
                    </div>
                    <div class="text-white text-xs font-bold opacity-80" id="khqr-card-currency-tag">USD</div>
                </div>

                <!-- Card Body -->
                <div class="p-6 flex flex-col items-center">
                    <p id="khqr-merchant-name" class="font-extrabold text-slate-800 text-base tracking-wide uppercase">LY MENGHOR</p>
                    <p class="text-xs text-slate-500 font-medium">QuantumCustom Licences Store</p>
                    
                    <div class="my-3 py-1.5 px-6 rounded-full bg-slate-100 border border-slate-200">
                        <span id="khqr-amount-display" class="font-black text-2xl text-slate-900">$2.50</span>
                    </div>

                    <!-- QR Matrix Container (Dynamically rendered via JS or Base64 uploaded Image) -->
                    <div class="relative p-3 bg-white rounded-xl border border-slate-200 shadow-inner flex items-center justify-center my-2">
                        <div id="qr-code-render-target"></div>
                        <img id="custom-khqr-img-target" class="hidden w-56 h-56 object-contain" src="" alt="KHQR Payment Code">
                    </div>

                    <p class="text-[11px] text-slate-400 mt-1 font-mono" id="khqr-order-ref">ORDER REF: QC-8921</p>
                </div>
            </div>

            <!-- Action Buttons for Checkout Modal -->
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                <button onclick="downloadKHQRCard()" class="py-3 px-4 rounded-xl bg-slate-700 hover:bg-slate-600 text-white font-bold text-xs flex items-center justify-center gap-2 transition-all">
                    <i class="fa-solid fa-download text-amber-400"></i>
                    <span>Download KHQR Image</span>
                </button>
                <button onclick="submitTelegramProof()" class="py-3 px-4 rounded-xl bg-sky-500 hover:bg-sky-400 text-white font-bold text-xs flex items-center justify-center gap-2 shadow-lg transition-all">
                    <i class="fa-brands fa-telegram text-base"></i>
                    <span>Send Proof on Telegram</span>
                </button>
            </div>
            
            <p class="text-[11px] text-slate-400 text-center mt-3">
                Scan with any Cambodia Banking App (ABA, ACLEDA, Wing, Sathapana, etc.).
            </p>
        </div>
    </div>

    <!-- EDIT STORE / ADMIN MANAGEMENT MODAL -->
    <div id="edit-store-modal" class="fixed inset-0 z-50 hidden flex items-center justify-center p-4 bg-black/80 backdrop-blur-md overflow-y-auto">
        <div class="bg-obsidian-800 border border-amber-500/40 rounded-2xl max-w-3xl w-full p-6 shadow-2xl relative my-8 text-slate-100">
            
            <button onclick="closeEditStoreModal()" class="absolute top-4 right-4 text-slate-400 hover:text-white text-lg w-8 h-8 flex items-center justify-center rounded-lg bg-obsidian-700/50">
                <i class="fa-solid fa-xmark"></i>
            </button>

            <div class="flex items-center gap-3 mb-6 pb-4 border-b border-slate-700">
                <i class="fa-solid fa-sliders text-amber-400 text-2xl"></i>
                <div>
                    <h3 class="font-black text-xl text-white">Store Management & Settings</h3>
                    <p class="text-xs text-amber-400">Customize products, pricing, merchant credentials & KHQR payload.</p>
                </div>
            </div>

            <!-- Admin Navigation Tabs -->
            <div class="flex gap-2 mb-6 border-b border-slate-700 pb-2">
                <button id="admin-tab-general-btn" onclick="switchAdminTab('general')" class="px-4 py-2 rounded-xl text-xs font-bold bg-amber-500 text-obsidian-900">Merchant Settings</button>
                <button id="admin-tab-products-btn" onclick="switchAdminTab('products')" class="px-4 py-2 rounded-xl text-xs font-bold bg-obsidian-700 text-slate-300">Manage Products</button>
            </div>

            <!-- TAB 1: GENERAL & MERCHANT SETTINGS -->
            <div id="admin-tab-general" class="space-y-5">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold text-slate-300 uppercase mb-1">Merchant Name (Shown on KHQR)</label>
                        <input type="text" id="admin-merchant-name" class="w-full px-3.5 py-2.5 rounded-xl bg-obsidian-900 border border-slate-700 text-white text-sm focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-300 uppercase mb-1">Telegram Link / Username</label>
                        <input type="text" id="admin-telegram-link" class="w-full px-3.5 py-2.5 rounded-xl bg-obsidian-900 border border-slate-700 text-white text-sm focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-300 uppercase mb-1">USD to KHR Exchange Rate (1 USD = ? KHR)</label>
                        <input type="number" id="admin-exchange-rate" class="w-full px-3.5 py-2.5 rounded-xl bg-obsidian-900 border border-slate-700 text-white text-sm focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-300 uppercase mb-1">Store Logo Image (Optional)</label>
                        <input type="file" id="admin-logo-upload" accept="image/*" onchange="handleLogoUpload(event)" class="w-full text-xs text-slate-400 file:mr-3 file:py-2 file:px-4 file:rounded-xl file:border-0 file:text-xs file:font-semibold file:bg-amber-500 file:text-obsidian-900 hover:file:bg-amber-400">
                    </div>
                </div>

                <div class="border-t border-slate-700/60 pt-4">
                    <h4 class="font-bold text-amber-400 text-xs uppercase tracking-wider mb-3">Custom KHQR QR Codes (Upload Images or Paste EMVCo Payloads)</h4>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div class="p-3 bg-obsidian-900 rounded-xl border border-slate-700">
                            <label class="block text-xs font-bold text-slate-300 mb-1">Upload USD KHQR Code Image</label>
                            <input type="file" id="admin-khqr-usd-file" accept="image/*" onchange="handleKHQRImageUpload(event, 'USD')" class="w-full text-xs text-slate-400 file:mr-2 file:py-1.5 file:px-3 file:rounded-lg file:border-0 file:text-xs file:bg-slate-700 file:text-white">
                            <p class="text-[10px] text-slate-500 mt-1">Or paste EMVCo String below:</p>
                            <input type="text" id="admin-khqr-usd-payload" placeholder="000201010212..." class="w-full mt-1 px-3 py-1.5 rounded-lg bg-obsidian-800 border border-slate-700 text-xs font-mono text-white">
                        </div>
                        <div class="p-3 bg-obsidian-900 rounded-xl border border-slate-700">
                            <label class="block text-xs font-bold text-slate-300 mb-1">Upload KHR KHQR Code Image</label>
                            <input type="file" id="admin-khqr-khr-file" accept="image/*" onchange="handleKHQRImageUpload(event, 'KHR')" class="w-full text-xs text-slate-400 file:mr-2 file:py-1.5 file:px-3 file:rounded-lg file:border-0 file:text-xs file:bg-slate-700 file:text-white">
                            <p class="text-[10px] text-slate-500 mt-1">Or paste EMVCo String below:</p>
                            <input type="text" id="admin-khqr-khr-payload" placeholder="000201010212..." class="w-full mt-1 px-3 py-1.5 rounded-lg bg-obsidian-800 border border-slate-700 text-xs font-mono text-white">
                        </div>
                    </div>
                </div>

                <div class="flex flex-wrap items-center justify-between gap-3 pt-4 border-t border-slate-700">
                    <div class="flex gap-2">
                        <button onclick="exportStoreConfig()" class="px-3.5 py-2 rounded-xl bg-slate-700 hover:bg-slate-600 text-xs font-bold text-white"><i class="fa-solid fa-download mr-1"></i> Export JSON</button>
                        <button onclick="triggerImportConfig()" class="px-3.5 py-2 rounded-xl bg-slate-700 hover:bg-slate-600 text-xs font-bold text-white"><i class="fa-solid fa-upload mr-1"></i> Import JSON</button>
                        <input type="file" id="import-json-file" class="hidden" accept=".json" onchange="importStoreConfig(event)">
                    </div>
                    <button onclick="resetStoreToDefault()" class="px-3.5 py-2 rounded-xl bg-rose-500/20 text-rose-400 hover:bg-rose-500/30 text-xs font-bold border border-rose-500/40"><i class="fa-solid fa-rotate-left mr-1"></i> Reset to Defaults</button>
                </div>
            </div>

            <!-- TAB 2: MANAGE PRODUCTS -->
            <div id="admin-tab-products" class="hidden space-y-4">
                <div class="flex justify-between items-center mb-2">
                    <span class="text-xs text-slate-400 font-semibold">Configured Products (<span id="admin-product-count">0</span>)</span>
                    <button onclick="openProductEditForm(null)" class="px-3 py-1.5 rounded-xl bg-amber-500 text-obsidian-900 font-bold text-xs hover:bg-amber-400"><i class="fa-solid fa-plus mr-1"></i> Add New Product</button>
                </div>

                <div id="admin-products-list-container" class="space-y-3 max-h-96 overflow-y-auto pr-1">
                    <!-- JS will render product items with Edit / Delete actions -->
                </div>
            </div>

            <div class="mt-6 pt-4 border-t border-slate-700 flex justify-end">
                <button onclick="saveStoreSettings()" class="px-6 py-2.5 rounded-xl bg-amber-500 text-obsidian-900 font-black text-sm hover:bg-amber-400 shadow-gold-glow transition-all">Save Store Settings</button>
            </div>
        </div>
    </div>

    <!-- PRODUCT ADD / EDIT SUB-MODAL -->
    <div id="product-form-modal" class="fixed inset-0 z-50 hidden flex items-center justify-center p-4 bg-black/85 backdrop-blur-md overflow-y-auto">
        <div class="bg-obsidian-800 border border-amber-500/40 rounded-2xl max-w-xl w-full p-6 shadow-2xl relative my-8 text-white">
            <button onclick="closeProductFormModal()" class="absolute top-4 right-4 text-slate-400 hover:text-white"><i class="fa-solid fa-xmark text-lg"></i></button>
            
            <h3 id="product-form-title" class="font-black text-xl mb-4">Edit Product</h3>
            
            <form id="product-edit-form" onsubmit="handleProductFormSubmit(event)" class="space-y-4">
                <input type="hidden" id="pf-id">
                
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-xs font-bold text-slate-300 mb-1">Product Name</label>
                        <input type="text" id="pf-name" required class="w-full px-3 py-2 rounded-xl bg-obsidian-900 border border-slate-700 text-xs text-white">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-300 mb-1">Category</label>
                        <select id="pf-category" required class="w-full px-3 py-2 rounded-xl bg-obsidian-900 border border-slate-700 text-xs text-white">
                            <option value="Video & Streaming">Video & Streaming</option>
                            <option value="AI Tools">AI Tools</option>
                            <option value="Music & Design">Music & Design</option>
                            <option value="Productivity">Productivity</option>
                        </select>
                    </div>
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-xs font-bold text-slate-300 mb-1">FontAwesome Icon Class</label>
                        <input type="text" id="pf-icon" placeholder="fa-brands fa-youtube" required class="w-full px-3 py-2 rounded-xl bg-obsidian-900 border border-slate-700 text-xs text-white">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-300 mb-1">Badge Text (e.g. Best Seller)</label>
                        <input type="text" id="pf-badge" placeholder="Popular" class="w-full px-3 py-2 rounded-xl bg-obsidian-900 border border-slate-700 text-xs text-white">
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold text-slate-300 mb-1">Short Description</label>
                    <input type="text" id="pf-desc" required class="w-full px-3 py-2 rounded-xl bg-obsidian-900 border border-slate-700 text-xs text-white">
                </div>

                <div>
                    <label class="block text-xs font-bold text-slate-300 mb-1">Features List (Comma Separated)</label>
                    <input type="text" id="pf-features" placeholder="No ads, Background Play, 4K Ultra HD" required class="w-full px-3 py-2 rounded-xl bg-obsidian-900 border border-slate-700 text-xs text-white">
                </div>

                <div>
                    <label class="block text-xs font-bold text-amber-400 mb-1">Subscription Plans & Prices (USD)</label>
                    <div id="pf-plans-container" class="space-y-2">
                        <!-- JS injected plan rows -->
                    </div>
                    <button type="button" onclick="addPlanRow('', 0)" class="mt-2 text-xs text-amber-400 font-bold hover:underline"><i class="fa-solid fa-plus mr-1"></i> Add Plan Option</button>
                </div>

                <div class="flex justify-end gap-2 pt-4 border-t border-slate-700">
                    <button type="button" onclick="closeProductFormModal()" class="px-4 py-2 rounded-xl bg-slate-700 text-xs font-bold">Cancel</button>
                    <button type="submit" class="px-5 py-2 rounded-xl bg-amber-500 text-obsidian-900 text-xs font-bold">Save Product</button>
                </div>
            </form>
        </div>
    </div>

    <!-- ORDER RECEIPT LOOKUP MODAL -->
    <div id="receipt-modal" class="fixed inset-0 z-50 hidden flex items-center justify-center p-4 bg-black/80 backdrop-blur-md">
        <div class="bg-obsidian-800 border border-amber-500/40 rounded-2xl max-w-md w-full p-6 shadow-2xl relative text-slate-100">
            <button onclick="closeReceiptModal()" class="absolute top-4 right-4 text-slate-400 hover:text-white"><i class="fa-solid fa-xmark text-lg"></i></button>

            <h3 class="font-black text-xl mb-4 flex items-center gap-2">
                <i class="fa-solid fa-receipt text-amber-400"></i>
                <span>Order Receipt & Lookup</span>
            </h3>

            <p class="text-xs text-slate-400 mb-4">Enter your Order ID (e.g. QC-8921) to view or regenerate your payment confirmation receipt.</p>

            <div class="flex gap-2 mb-4">
                <input type="text" id="receipt-search-id" placeholder="Enter Order ID" class="w-full px-3.5 py-2 rounded-xl bg-obsidian-900 border border-slate-700 text-white text-xs uppercase font-mono">
                <button onclick="lookupReceipt()" class="px-4 py-2 bg-amber-500 text-obsidian-900 font-bold text-xs rounded-xl hover:bg-amber-400">Search</button>
            </div>

            <div id="receipt-output-card" class="bg-obsidian-900 p-4 rounded-xl border border-slate-700 hidden text-xs font-mono space-y-2">
                <!-- JS injected output -->
            </div>
        </div>
    </div>


    <!-- JAVASCRIPT APPLICATION ENGINE -->
    <script>
        // ==========================================
        // DEFAULT STORE CONFIGURATION & SEED DATA
        // ==========================================
        const DEFAULT_STORE_CONFIG = {
            merchantName: "LY MENGHOR",
            telegramLink: "https://t.me/quantumcustomlicences",
            exchangeRate: 4100, // 1 USD = 4100 KHR
            customLogoBase64: "",
            khqrUsdImageBase64: "",
            khqrKhrImageBase64: "",
            khqrUsdPayload: "00020101021238560016A0000007700000010108ABA0000020102030004LY MENGHOR5204599953038405802KH5910LY MENGHOR6010Phnom Penh63044C81",
            khqrKhrPayload: "00020101021238560016A0000007700000010108ABA0000020102030004LY MENGHOR5204599953031165802KH5910LY MENGHOR6010Phnom Penh63042A19"
        };

        const DEFAULT_PRODUCTS = [
            {
                id: "yt-premium",
                name: "YouTube Premium",
                category: "Video & Streaming",
                icon: "fa-brands fa-youtube",
                iconColor: "text-red-500",
                badge: "Best Seller",
                description: "No ads, background playback, and YouTube Music Premium included.",
                features: ["Zero Ads Playback", "Background Audio Play", "YouTube Music Included", "Upgrade Own Email"],
                plans: [
                    { name: "1 Month", priceUSD: 2.50 },
                    { name: "3 Months", priceUSD: 6.50 },
                    { name: "6 Months", priceUSD: 12.00 },
                    { name: "1 Year", priceUSD: 22.00 }
                ]
            },
            {
                id: "gemini-pro",
                name: "Gemini Advanced / Pro",
                category: "AI Tools",
                icon: "fa-solid fa-brain",
                iconColor: "text-purple-400",
                badge: "2TB Cloud AI",
                description: "Google's most capable AI model + 2TB Google One Cloud storage.",
                features: ["Gemini 1.5 Pro Model", "2TB Google Storage", "Gmail & Docs Integration", "Ultra Fast Response"],
                plans: [
                    { name: "1 Month", priceUSD: 5.00 },
                    { name: "1 Year", priceUSD: 35.00 }
                ]
            },
            {
                id: "chatgpt-plus",
                name: "ChatGPT Plus",
                category: "AI Tools",
                icon: "fa-solid fa-robot",
                iconColor: "text-emerald-400",
                badge: "GPT-4o Access",
                description: "Full access to GPT-4o, DALL-E 3 image generation, and Custom GPTs.",
                features: ["GPT-4o & GPT-4 models", "DALL-E 3 Image Generation", "Advanced Data Analysis", "Voice Mode Access"],
                plans: [
                    { name: "1 Month (Shared)", priceUSD: 4.00 },
                    { name: "1 Month (Private)", priceUSD: 18.00 }
                ]
            },
            {
                id: "netflix-4k",
                name: "Netflix Premium 4K",
                category: "Video & Streaming",
                icon: "fa-solid fa-film",
                iconColor: "text-red-600",
                badge: "4K Ultra HD",
                description: "Ultra HD 4K streaming quality with private pin-locked profile.",
                features: ["Ultra HD 4K + HDR", "Private Screen Profile", "Works on Smart TV/Mobile", "Full Term Warranty"],
                plans: [
                    { name: "1 Month", priceUSD: 3.50 },
                    { name: "3 Months", priceUSD: 9.50 },
                    { name: "1 Year", priceUSD: 32.00 }
                ]
            },
            {
                id: "spotify-premium",
                name: "Spotify Premium",
                category: "Music & Design",
                icon: "fa-brands fa-spotify",
                iconColor: "text-green-500",
                badge: "Offline Audio",
                description: "Ad-free music listening with unlimited skips and offline downloads.",
                features: ["Ad-free Music Play", "Unlimited Song Skips", "Very High Audio Quality", "Offline Songs Download"],
                plans: [
                    { name: "1 Month", priceUSD: 2.00 },
                    { name: "6 Months", priceUSD: 9.00 },
                    { name: "1 Year", priceUSD: 16.00 }
                ]
            },
            {
                id: "canva-pro",
                name: "Canva Pro",
                category: "Music & Design",
                icon: "fa-solid fa-palette",
                iconColor: "text-cyan-400",
                badge: "Magic AI Tools",
                description: "Full brand kit access, Magic Studio AI tools, and 100M+ stock assets.",
                features: ["Magic Studio AI Access", "100M+ Premium Assets", "Unlimited Brand Kits", "Upgrade Own Account"],
                plans: [
                    { name: "1 Year", priceUSD: 6.00 },
                    { name: "Lifetime Access", priceUSD: 15.00 }
                ]
            }
        ];

        // ==========================================
        // STATE MANAGEMENT
        // ==========================================
        let storeConfig = JSON.parse(localStorage.getItem('qc_store_config')) || DEFAULT_STORE_CONFIG;
        let products = JSON.parse(localStorage.getItem('qc_products')) || DEFAULT_PRODUCTS;
        let currentCurrency = localStorage.getItem('qc_currency') || 'USD';
        let currentCategory = 'All';
        let searchQuery = '';

        // Active checkout state
        let activeCheckoutProduct = null;
        let activeCheckoutPlanIndex = 0;
        let activeCheckoutCurrency = 'USD';
        let currentOrderRef = '';

        // ==========================================
        // INITIALIZATION
        // ==========================================
        window.addEventListener('DOMContentLoaded', () => {
            applyThemeFromStorage();
            applyStoreConfigUI();
            renderCategories();
            renderProducts();
        });

        // ==========================================
        // RENDER PRODUCTS & CATEGORIES
        // ==========================================
        function renderCategories() {
            const categories = ['All', 'Video & Streaming', 'AI Tools', 'Music & Design', 'Productivity'];
            const container = document.getElementById('category-tabs-container');
            
            container.innerHTML = categories.map(cat => {
                const isActive = cat === currentCategory;
                const activeClass = isActive 
                    ? 'bg-amber-500 text-obsidian-900 font-extrabold shadow-gold-glow' 
                    : 'bg-obsidian-800 text-slate-400 hover:text-white border border-slate-700/60 font-medium';
                return `<button onclick="setCategory('${cat}')" class="px-4 py-2 rounded-xl text-xs whitespace-nowrap transition-all ${activeClass}">${cat}</button>`;
            }).join('');
        }

        function setCategory(cat) {
            currentCategory = cat;
            renderCategories();
            renderProducts();
        }

        function handleSearch() {
            searchQuery = document.getElementById('search-input').value.toLowerCase();
            renderProducts();
        }

        function setCurrency(curr) {
            currentCurrency = curr;
            localStorage.setItem('qc_currency', curr);
            
            // Toggle header button styles
            const usdBtn = document.getElementById('curr-usd-btn');
            const khrBtn = document.getElementById('curr-khr-btn');
            
            if (curr === 'USD') {
                usdBtn.className = "px-2.5 py-1 text-xs font-bold rounded-lg transition-all bg-amber-500 text-obsidian-900 shadow";
                khrBtn.className = "px-2.5 py-1 text-xs font-bold rounded-lg transition-all text-slate-400 hover:text-white";
            } else {
                khrBtn.className = "px-2.5 py-1 text-xs font-bold rounded-lg transition-all bg-amber-500 text-obsidian-900 shadow";
                usdBtn.className = "px-2.5 py-1 text-xs font-bold rounded-lg transition-all text-slate-400 hover:text-white";
            }
            
            renderProducts();
        }

        function formatPrice(usdAmount) {
            if (currentCurrency === 'KHR') {
                const khrVal = Math.round(usdAmount * storeConfig.exchangeRate);
                return `${khrVal.toLocaleString()} ៛`;
            }
            return `$${usdAmount.toFixed(2)}`;
        }

        function renderProducts() {
            const grid = document.getElementById('products-grid');
            
            const filtered = products.filter(prod => {
                const matchCat = currentCategory === 'All' || prod.category === currentCategory;
                const matchSearch = prod.name.toLowerCase().includes(searchQuery) || prod.description.toLowerCase().includes(searchQuery);
                return matchCat && matchSearch;
            });

            if (filtered.length === 0) {
                grid.innerHTML = `
                    <div class="col-span-full py-16 text-center text-slate-500">
                        <i class="fa-solid fa-box-open text-4xl mb-3 text-slate-600"></i>
                        <p class="font-bold text-base">No subscription licenses found</p>
                        <p class="text-xs">Try adjusting your search query or category filter.</p>
                    </div>
                `;
                return;
            }

            grid.innerHTML = filtered.map(prod => {
                // Default selected plan is index 0
                const selectedPlan = prod.plans[0];
                const priceFormatted = formatPrice(selectedPlan.priceUSD);

                return `
                    <div id="product-card-${prod.id}" class="bg-obsidian-800/90 border border-slate-700/80 hover:border-amber-500/50 rounded-2xl p-5 flex flex-col justify-between transition-all duration-300 hover:-translate-y-1 hover:shadow-gold-glow group">
                        
                        <div>
                            <!-- Header Info -->
                            <div class="flex items-start justify-between mb-4">
                                <div class="w-12 h-12 rounded-2xl bg-obsidian-900 border border-slate-700/80 flex items-center justify-center text-2xl ${prod.iconColor || 'text-amber-400'} group-hover:scale-110 transition-transform">
                                    <i class="${prod.icon}"></i>
                                </div>
                                ${prod.badge ? `<span class="bg-amber-500/15 border border-amber-500/30 text-amber-400 text-[10px] font-extrabold px-2.5 py-1 rounded-full uppercase tracking-wider">${prod.badge}</span>` : ''}
                            </div>

                            <h3 class="font-black text-xl text-white group-hover:text-amber-400 transition-colors">${prod.name}</h3>
                            <p class="text-xs text-slate-400 mt-1 line-clamp-2">${prod.description}</p>

                            <!-- Plan Selector Pills -->
                            <div class="mt-4">
                                <label class="block text-[11px] font-bold text-slate-400 uppercase tracking-wider mb-2">Select Duration Plan:</label>
                                <div class="flex flex-wrap gap-1.5">
                                    ${prod.plans.map((p, idx) => `
                                        <button onclick="selectProductPlan('${prod.id}', ${idx})" id="plan-btn-${prod.id}-${idx}" class="plan-pill-${prod.id} px-2.5 py-1 rounded-lg text-xs font-semibold border transition-all ${idx === 0 ? 'bg-amber-500 text-obsidian-900 border-amber-500' : 'bg-obsidian-900 text-slate-300 border-slate-700 hover:border-slate-500'}">
                                            ${p.name}
                                        </button>
                                    `).join('')}
                                </div>
                            </div>

                            <!-- Bullet Features -->
                            <ul class="mt-4 space-y-2 text-xs text-slate-300 border-t border-slate-700/60 pt-4">
                                ${prod.features.map(feat => `
                                    <li class="flex items-center gap-2">
                                        <i class="fa-solid fa-check text-emerald-400 text-[11px]"></i>
                                        <span>${feat}</span>
                                    </li>
                                `).join('')}
                            </ul>
                        </div>

                        <!-- Price & Buy Button Footer -->
                        <div class="mt-6 pt-4 border-t border-slate-700/60 flex items-center justify-between">
                            <div>
                                <span class="text-[10px] text-slate-400 uppercase block font-semibold">Total Price:</span>
                                <span id="price-display-${prod.id}" class="text-xl font-black text-white gold-gradient-text">${priceFormatted}</span>
                            </div>

                            <button onclick="openCheckoutModal('${prod.id}')" class="px-4 py-2.5 rounded-xl bg-amber-500 hover:bg-amber-400 text-obsidian-900 font-extrabold text-xs flex items-center gap-2 shadow-gold-glow hover:scale-105 transition-all">
                                <i class="fa-solid fa-bolt"></i>
                                <span>Buy Now / KHQR</span>
                            </button>
                        </div>
                    </div>
                `;
            }).join('');
        }

        function selectProductPlan(productId, planIndex) {
            const prod = products.find(p => p.id === productId);
            if (!prod) return;

            // Update UI buttons
            const pills = document.querySelectorAll(`.plan-pill-${productId}`);
            pills.forEach((pill, idx) => {
                if (idx === planIndex) {
                    pill.className = `plan-pill-${productId} px-2.5 py-1 rounded-lg text-xs font-semibold border transition-all bg-amber-500 text-obsidian-900 border-amber-500`;
                } else {
                    pill.className = `plan-pill-${productId} px-2.5 py-1 rounded-lg text-xs font-semibold border transition-all bg-obsidian-900 text-slate-300 border-slate-700 hover:border-slate-500`;
                }
            });

            // Update Price Display on Card
            const plan = prod.plans[planIndex];
            const priceEl = document.getElementById(`price-display-${productId}`);
            if (priceEl) {
                priceEl.innerText = formatPrice(plan.priceUSD);
            }

            // Store active plan index attribute on card
            const card = document.getElementById(`product-card-${productId}`);
            if (card) {
                card.dataset.selectedPlanIndex = planIndex;
            }
        }

        // ==========================================
        // CHECKOUT & ABA KHQR ENGINE
        // ==========================================
        function openCheckoutModal(productId) {
            const card = document.getElementById(`product-card-${productId}`);
            const selectedPlanIndex = card && card.dataset.selectedPlanIndex ? parseInt(card.dataset.selectedPlanIndex) : 0;
            
            const prod = products.find(p => p.id === productId);
            if (!prod) return;

            activeCheckoutProduct = prod;
            activeCheckoutPlanIndex = selectedPlanIndex;
            activeCheckoutCurrency = currentCurrency;

            // Generate Random Order Ref ID
            currentOrderRef = 'QC-' + Math.floor(1000 + Math.random() * 9000);

            // Populate Modal UI
            document.getElementById('checkout-product-name').innerText = prod.name;
            document.getElementById('checkout-plan-name').innerText = prod.plans[selectedPlanIndex].name + " License Access";
            
            const iconContainer = document.getElementById('checkout-product-icon');
            iconContainer.innerHTML = `<i class="${prod.icon}"></i>`;

            setCheckoutCurrency(currentCurrency);

            // Open Modal
            document.getElementById('checkout-modal').classList.remove('hidden');
        }

        function closeCheckoutModal() {
            document.getElementById('checkout-modal').classList.add('hidden');
        }

        function setCheckoutCurrency(curr) {
            activeCheckoutCurrency = curr;

            const payUsdBtn = document.getElementById('checkout-pay-usd-btn');
            const payKhrBtn = document.getElementById('checkout-pay-khr-btn');
            
            if (curr === 'USD') {
                payUsdBtn.className = "py-2 rounded-xl text-xs font-bold border border-amber-500 bg-amber-500 text-obsidian-900";
                payKhrBtn.className = "py-2 rounded-xl text-xs font-bold border border-slate-700 bg-obsidian-900 text-slate-300";
            } else {
                payKhrBtn.className = "py-2 rounded-xl text-xs font-bold border border-amber-500 bg-amber-500 text-obsidian-900";
                payUsdBtn.className = "py-2 rounded-xl text-xs font-bold border border-slate-700 bg-obsidian-900 text-slate-300";
            }

            renderKHQRDisplay();
        }

        function renderKHQRDisplay() {
            if (!activeCheckoutProduct) return;

            const plan = activeCheckoutProduct.plans[activeCheckoutPlanIndex];
            const priceUSD = plan.priceUSD;
            let displayAmount = '';
            let rawPayload = '';
            let customImg = '';

            if (activeCheckoutCurrency === 'KHR') {
                const khrVal = Math.round(priceUSD * storeConfig.exchangeRate);
                displayAmount = `${khrVal.toLocaleString()} ៛`;
                rawPayload = storeConfig.khqrKhrPayload;
                customImg = storeConfig.khqrKhrImageBase64;
                document.getElementById('khqr-card-currency-tag').innerText = 'KHR (៛)';
            } else {
                displayAmount = `$${priceUSD.toFixed(2)}`;
                rawPayload = storeConfig.khqrUsdPayload;
                customImg = storeConfig.khqrUsdImageBase64;
                document.getElementById('khqr-card-currency-tag').innerText = 'USD ($)';
            }

            document.getElementById('khqr-merchant-name').innerText = storeConfig.merchantName || 'LY MENGHOR';
            document.getElementById('khqr-amount-display').innerText = displayAmount;
            document.getElementById('khqr-order-ref').innerText = `ORDER REF: ${currentOrderRef}`;

            const qrTarget = document.getElementById('qr-code-render-target');
            const imgTarget = document.getElementById('custom-khqr-img-target');

            // If store owner uploaded an explicit image for KHQR, show image
            if (customImg && customImg.length > 50) {
                qrTarget.innerHTML = '';
                qrTarget.classList.add('hidden');
                imgTarget.src = customImg;
                imgTarget.classList.remove('hidden');
            } else {
                // Dynamically render QR Matrix using QRCode.js
                imgTarget.classList.add('hidden');
                qrTarget.classList.remove('hidden');
                qrTarget.innerHTML = '';

                new QRCode(qrTarget, {
                    text: rawPayload || "https://t.me/quantumcustomlicences",
                    width: 200,
                    height: 200,
                    colorDark : "#000000",
                    colorLight : "#ffffff",
                    correctLevel : QRCode.CorrectLevel.H
                });
            }
        }

        // ==========================================
        // HIGH-RES KHQR CARD DOWNLOAD CANVAS ENGINE
        // ==========================================
        function downloadKHQRCard() {
            showToast('Generating High-Res KHQR Voucher Card...', 'info');

            const canvas = document.createElement('canvas');
            canvas.width = 750;
            canvas.height = 1000;
            const ctx = canvas.getContext('2d');

            // Background White Voucher Card
            ctx.fillStyle = '#FFFFFF';
            ctx.roundRect(0, 0, 750, 1000, 32);
            ctx.fill();

            // Header Red Bar (KHQR Red)
            ctx.fillStyle = '#E21A22';
            ctx.beginPath();
            ctx.roundRect(0, 0, 750, 140, [32, 32, 0, 0]);
            ctx.fill();

            // KHQR Text Logo inside Header
            ctx.fillStyle = '#FFFFFF';
            ctx.font = '900 38px Inter, sans-serif';
            ctx.fillText('KHQR', 40, 85);

            ctx.font = '600 22px Inter, sans-serif';
            ctx.fillText('BAKONG PAYMENT', 180, 82);

            // Currency Pill Tag
            ctx.fillStyle = 'rgba(255, 255, 255, 0.25)';
            ctx.roundRect(610, 45, 100, 50, 12);
            ctx.fill();
            ctx.fillStyle = '#FFFFFF';
            ctx.font = 'bold 20px Inter, sans-serif';
            ctx.textAlign = 'center';
            ctx.fillText(activeCheckoutCurrency, 660, 77);

            // Merchant Details
            ctx.textAlign = 'center';
            ctx.fillStyle = '#0F172A';
            ctx.font = '900 36px Inter, sans-serif';
            ctx.fillText((storeConfig.merchantName || 'LY MENGHOR').toUpperCase(), 375, 220);

            ctx.fillStyle = '#64748B';
            ctx.font = '500 22px Inter, sans-serif';
            ctx.fillText('QuantumCustom Digital Licences Store', 375, 260);

            // Amount Display Box
            const plan = activeCheckoutProduct.plans[activeCheckoutPlanIndex];
            let amountTxt = activeCheckoutCurrency === 'KHR' 
                ? `${Math.round(plan.priceUSD * storeConfig.exchangeRate).toLocaleString()} ៛`
                : `$${plan.priceUSD.toFixed(2)}`;

            ctx.fillStyle = '#F8FAFC';
            ctx.strokeStyle = '#E2E8F0';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.roundRect(175, 290, 400, 70, 35);
            ctx.fill();
            ctx.stroke();

            ctx.fillStyle = '#0F172A';
            ctx.font = '900 34px Inter, sans-serif';
            ctx.fillText(amountTxt, 375, 338);

            // Draw QR Code Image into Canvas
            const qrTarget = document.getElementById('qr-code-render-target');
            const imgTarget = document.getElementById('custom-khqr-img-target');
            
            let qrSourceImg = null;
            if (!imgTarget.classList.contains('hidden') && imgTarget.src) {
                qrSourceImg = imgTarget;
            } else {
                qrSourceImg = qrTarget.querySelector('img') || qrTarget.querySelector('canvas');
            }

            const drawFooterAndDownload = () => {
                // Product & Order Footer Box
                ctx.fillStyle = '#090A0F';
                ctx.roundRect(40, 830, 670, 130, 20);
                ctx.fill();

                ctx.textAlign = 'left';
                ctx.fillStyle = '#F59E0B';
                ctx.font = 'bold 22px Inter, sans-serif';
                ctx.fillText(`Product: ${activeCheckoutProduct.name}`, 70, 875);

                ctx.fillStyle = '#94A3B8';
                ctx.font = '500 18px Inter, sans-serif';
                ctx.fillText(`Plan: ${plan.name} Access  |  Ref: ${currentOrderRef}`, 70, 915);

                // Download File
                const link = document.createElement('a');
                link.download = `QuantumCustom-KHQR-${currentOrderRef}.png`;
                link.href = canvas.toDataURL('image/png');
                link.click();
                showToast('KHQR Voucher downloaded successfully!', 'success');
            };

            if (qrSourceImg) {
                const tempImage = new Image();
                tempImage.crossOrigin = "anonymous";
                tempImage.onload = () => {
                    ctx.drawImage(tempImage, 187, 390, 375, 375);
                    drawFooterAndDownload();
                };
                tempImage.src = qrSourceImg.tagName === 'CANVAS' ? qrSourceImg.toDataURL() : qrSourceImg.src;
            } else {
                drawFooterAndDownload();
            }
        }

        // ==========================================
        // SUBMIT PROOF ON TELEGRAM
        // ==========================================
        function submitTelegramProof() {
            const custName = document.getElementById('cust-name-input').value.trim() || 'Valued Customer';
            const custEmail = document.getElementById('cust-email-input').value.trim() || 'Not Provided';
            const plan = activeCheckoutProduct.plans[activeCheckoutPlanIndex];

            const priceTxt = activeCheckoutCurrency === 'KHR'
                ? `${Math.round(plan.priceUSD * storeConfig.exchangeRate).toLocaleString()} ៛`
                : `$${plan.priceUSD.toFixed(2)}`;

            const msg = `⚡ *NEW LICENSE ORDER - QUANTUMCUSTOM*\n` +
                        `━━━━━━━━━━━━━━━━━━━━\n` +
                        `🆔 *Order Ref:* \`${currentOrderRef}\` \n` +
                        `📦 *Product:* ${activeCheckoutProduct.name}\n` +
                        `⏳ *Plan:* ${plan.name}\n` +
                        `💰 *Amount Paid:* ${priceTxt}\n` +
                        `👤 *Customer:* ${custName}\n` +
                        `📧 *Delivery Email:* ${custEmail}\n` +
                        `━━━━━━━━━━━━━━━━━━━━\n` +
                        `Please verify my ABA KHQR payment and send my license access!`;

            // Save order to LocalStorage for receipt lookup
            saveOrderReceipt({
                orderRef: currentOrderRef,
                product: activeCheckoutProduct.name,
                plan: plan.name,
                amount: priceTxt,
                customer: custName,
                email: custEmail,
                date: new Date().toLocaleString()
            });

            // Copy pre-formatted message to clipboard
            copyToClipboard(msg);

            showToast('Order details copied! Opening Telegram...', 'success');

            // Open Telegram link
            setTimeout(() => {
                let tgUrl = storeConfig.telegramLink || "https://t.me/quantumcustomlicences";
                window.open(tgUrl, '_blank');
            }, 800);
        }

        function saveOrderReceipt(orderData) {
            let receipts = JSON.parse(localStorage.getItem('qc_orders')) || [];
            receipts.unshift(orderData);
            localStorage.setItem('qc_orders', JSON.stringify(receipts));
        }

        // ==========================================
        // EDIT STORE / ADMIN MANAGEMENT
        // ==========================================
        function openEditStoreModal() {
            // Populate Store Config Fields
            document.getElementById('admin-merchant-name').value = storeConfig.merchantName || '';
            document.getElementById('admin-telegram-link').value = storeConfig.telegramLink || '';
            document.getElementById('admin-exchange-rate').value = storeConfig.exchangeRate || 4100;
            document.getElementById('admin-khqr-usd-payload').value = storeConfig.khqrUsdPayload || '';
            document.getElementById('admin-khqr-khr-payload').value = storeConfig.khqrKhrPayload || '';

            renderAdminProductsList();
            document.getElementById('edit-store-modal').classList.remove('hidden');
        }

        function closeEditStoreModal() {
            document.getElementById('edit-store-modal').classList.add('hidden');
        }

        function switchAdminTab(tab) {
            const genTab = document.getElementById('admin-tab-general');
            const prodTab = document.getElementById('admin-tab-products');
            const genBtn = document.getElementById('admin-tab-general-btn');
            const prodBtn = document.getElementById('admin-tab-products-btn');

            if (tab === 'general') {
                genTab.classList.remove('hidden');
                prodTab.classList.add('hidden');
                genBtn.className = "px-4 py-2 rounded-xl text-xs font-bold bg-amber-500 text-obsidian-900";
                prodBtn.className = "px-4 py-2 rounded-xl text-xs font-bold bg-obsidian-700 text-slate-300";
            } else {
                prodTab.classList.remove('hidden');
                genTab.classList.add('hidden');
                prodBtn.className = "px-4 py-2 rounded-xl text-xs font-bold bg-amber-500 text-obsidian-900";
                genBtn.className = "px-4 py-2 rounded-xl text-xs font-bold bg-obsidian-700 text-slate-300";
            }
        }

        function handleLogoUpload(event) {
            const file = event.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = (e) => {
                storeConfig.customLogoBase64 = e.target.result;
                showToast('Logo image uploaded! Save settings to apply.', 'info');
            };
            reader.readAsDataURL(file);
        }

        function handleKHQRImageUpload(event, type) {
            const file = event.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = (e) => {
                if (type === 'USD') {
                    storeConfig.khqrUsdImageBase64 = e.target.result;
                } else {
                    storeConfig.khqrKhrImageBase64 = e.target.result;
                }
                showToast(`${type} KHQR Image loaded! Save settings to commit.`, 'info');
            };
            reader.readAsDataURL(file);
        }

        function saveStoreSettings() {
            storeConfig.merchantName = document.getElementById('admin-merchant-name').value.trim() || 'LY MENGHOR';
            storeConfig.telegramLink = document.getElementById('admin-telegram-link').value.trim() || 'https://t.me/quantumcustomlicences';
            storeConfig.exchangeRate = parseFloat(document.getElementById('admin-exchange-rate').value) || 4100;
            storeConfig.khqrUsdPayload = document.getElementById('admin-khqr-usd-payload').value.trim();
            storeConfig.khqrKhrPayload = document.getElementById('admin-khqr-khr-payload').value.trim();

            localStorage.setItem('qc_store_config', JSON.stringify(storeConfig));
            localStorage.setItem('qc_products', JSON.stringify(products));

            applyStoreConfigUI();
            renderProducts();
            closeEditStoreModal();
            showToast('Store Configuration & Products Saved!', 'success');
        }

        function applyStoreConfigUI() {
            // Update Telegram Links
            const tgLink = storeConfig.telegramLink || 'https://t.me/quantumcustomlicences';
            document.getElementById('telegram-header-link').href = tgLink;
            document.getElementById('telegram-footer-link').href = tgLink;
            document.getElementById('telegram-float-btn').href = tgLink;

            // Update Logo
            const defaultLogo = document.getElementById('default-qc-logo');
            const customLogo = document.getElementById('custom-qc-logo');
            
            if (storeConfig.customLogoBase64 && storeConfig.customLogoBase64.length > 50) {
                defaultLogo.classList.add('hidden');
                customLogo.src = storeConfig.customLogoBase64;
                customLogo.classList.remove('hidden');
            } else {
                customLogo.classList.add('hidden');
                defaultLogo.classList.remove('hidden');
            }
        }

        // ==========================================
        // ADMIN PRODUCT EDIT & DELETE ENGINE
        // ==========================================
        function renderAdminProductsList() {
            const container = document.getElementById('admin-products-list-container');
            document.getElementById('admin-product-count').innerText = products.length;

            container.innerHTML = products.map((prod, idx) => `
                <div class="bg-obsidian-900 border border-slate-700 p-3 rounded-xl flex items-center justify-between gap-3 text-xs">
                    <div class="flex items-center gap-3">
                        <div class="w-8 h-8 rounded-lg bg-obsidian-800 border border-slate-700 flex items-center justify-center text-amber-400">
                            <i class="${prod.icon}"></i>
                        </div>
                        <div>
                            <p class="font-bold text-white">${prod.name}</p>
                            <p class="text-[10px] text-slate-400">${prod.category} • ${prod.plans.length} Plans</p>
                        </div>
                    </div>

                    <div class="flex items-center gap-2">
                        <button onclick="openProductEditForm('${prod.id}')" class="px-2.5 py-1.5 bg-slate-700 hover:bg-slate-600 text-white font-bold rounded-lg"><i class="fa-solid fa-pen-to-square"></i></button>
                        <button onclick="deleteProduct('${prod.id}')" class="px-2.5 py-1.5 bg-rose-500/20 hover:bg-rose-500/30 text-rose-400 font-bold rounded-lg border border-rose-500/30"><i class="fa-solid fa-trash-can"></i></button>
                    </div>
                </div>
            `).join('');
        }

        function deleteProduct(prodId) {
            products = products.filter(p => p.id !== prodId);
            localStorage.setItem('qc_products', JSON.stringify(products));
            renderAdminProductsList();
            renderProducts();
            showToast('Product removed.', 'info');
        }

        function openProductEditForm(prodId) {
            const container = document.getElementById('pf-plans-container');
            container.innerHTML = '';

            if (prodId) {
                const prod = products.find(p => p.id === prodId);
                if (!prod) return;
                document.getElementById('product-form-title').innerText = "Edit Product";
                document.getElementById('pf-id').value = prod.id;
                document.getElementById('pf-name').value = prod.name;
                document.getElementById('pf-category').value = prod.category;
                document.getElementById('pf-icon').value = prod.icon;
                document.getElementById('pf-badge').value = prod.badge || '';
                document.getElementById('pf-desc').value = prod.description;
                document.getElementById('pf-features').value = prod.features.join(', ');

                prod.plans.forEach(p => addPlanRow(p.name, p.priceUSD));
            } else {
                document.getElementById('product-form-title').innerText = "Add New Product";
                document.getElementById('pf-id').value = '';
                document.getElementById('product-edit-form').reset();
                addPlanRow('1 Month', 5.00);
            }

            document.getElementById('product-form-modal').classList.remove('hidden');
        }

        function closeProductFormModal() {
            document.getElementById('product-form-modal').classList.add('hidden');
        }

        function addPlanRow(name = '', price = 0) {
            const container = document.getElementById('pf-plans-container');
            const div = document.createElement('div');
            div.className = 'flex gap-2 items-center plan-row';
            div.innerHTML = `
                <input type="text" placeholder="Plan Name (e.g. 1 Month)" value="${name}" required class="w-1/2 px-2.5 py-1.5 rounded-lg bg-obsidian-900 border border-slate-700 text-xs text-white">
                <input type="number" step="0.01" placeholder="Price USD ($)" value="${price}" required class="w-1/2 px-2.5 py-1.5 rounded-lg bg-obsidian-900 border border-slate-700 text-xs text-white">
                <button type="button" onclick="this.parentElement.remove()" class="text-rose-400 hover:text-rose-300 p-1"><i class="fa-solid fa-xmark"></i></button>
            `;
            container.appendChild(div);
        }

        function handleProductFormSubmit(e) {
            e.preventDefault();
            const id = document.getElementById('pf-id').value || ('prod-' + Date.now());
            const name = document.getElementById('pf-name').value.trim();
            const category = document.getElementById('pf-category').value;
            const icon = document.getElementById('pf-icon').value.trim() || 'fa-solid fa-cube';
            const badge = document.getElementById('pf-badge').value.trim();
            const description = document.getElementById('pf-desc').value.trim();
            const features = document.getElementById('pf-features').value.split(',').map(s => s.trim()).filter(Boolean);

            const planRows = document.querySelectorAll('.plan-row');
            const plans = [];
            planRows.forEach(row => {
                const inputs = row.querySelectorAll('input');
                if (inputs[0].value && inputs[1].value) {
                    plans.push({
                        name: inputs[0].value.trim(),
                        priceUSD: parseFloat(inputs[1].value) || 0
                    });
                }
            });

            if (plans.length === 0) {
                showToast('Please add at least one subscription plan.', 'error');
                return;
            }

            const newProd = { id, name, category, icon, iconColor: 'text-amber-400', badge, description, features, plans };

            const existingIdx = products.findIndex(p => p.id === id);
            if (existingIdx >= 0) {
                products[existingIdx] = newProd;
            } else {
                products.push(newProd);
            }

            localStorage.setItem('qc_products', JSON.stringify(products));
            renderAdminProductsList();
            renderProducts();
            closeProductFormModal();
            showToast('Product updated successfully!', 'success');
        }

        function exportStoreConfig() {
            const dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify({
                storeConfig,
                products
            }, null, 2));
            const downloadAnchor = document.createElement('a');
            downloadAnchor.setAttribute("href", dataStr);
            downloadAnchor.setAttribute("download", `QuantumCustom_Store_Backup.json`);
            document.body.appendChild(downloadAnchor);
            downloadAnchor.click();
            downloadAnchor.remove();
        }

        function triggerImportConfig() {
            document.getElementById('import-json-file').click();
        }

        function importStoreConfig(e) {
            const file = e.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = (evt) => {
                try {
                    const parsed = JSON.parse(evt.target.result);
                    if (parsed.storeConfig && parsed.products) {
                        storeConfig = parsed.storeConfig;
                        products = parsed.products;
                        localStorage.setItem('qc_store_config', JSON.stringify(storeConfig));
                        localStorage.setItem('qc_products', JSON.stringify(products));
                        applyStoreConfigUI();
                        renderProducts();
                        closeEditStoreModal();
                        showToast('Store config imported successfully!', 'success');
                    }
                } catch(err) {
                    showToast('Invalid JSON file.', 'error');
                }
            };
            reader.readAsText(file);
        }

        function resetStoreToDefault() {
            storeConfig = DEFAULT_STORE_CONFIG;
            products = DEFAULT_PRODUCTS;
            localStorage.removeItem('qc_store_config');
            localStorage.removeItem('qc_products');
            applyStoreConfigUI();
            renderProducts();
            closeEditStoreModal();
            showToast('Store reset to defaults!', 'info');
        }

        // ==========================================
        // RECEIPT & ORDER LOOKUP
        // ==========================================
        function openOrderLookupModal() {
            document.getElementById('receipt-modal').classList.remove('hidden');
        }

        function closeReceiptModal() {
            document.getElementById('receipt-modal').classList.add('hidden');
        }

        function lookupReceipt() {
            const ref = document.getElementById('receipt-search-id').value.trim().toUpperCase();
            const output = document.getElementById('receipt-output-card');
            
            const orders = JSON.parse(localStorage.getItem('qc_orders')) || [];
            const found = orders.find(o => o.orderRef === ref);

            output.classList.remove('hidden');
            if (found) {
                output.innerHTML = `
                    <div class="text-emerald-400 font-bold mb-2">✓ Order Verified</div>
                    <p>Order Ref: <span class="text-white">${found.orderRef}</span></p>
                    <p>Product: <span class="text-white">${found.product} (${found.plan})</span></p>
                    <p>Amount: <span class="text-white">${found.amount}</span></p>
                    <p>Customer: <span class="text-white">${found.customer}</span></p>
                    <p>Date: <span class="text-slate-400">${found.date}</span></p>
                `;
            } else {
                output.innerHTML = `<p class="text-rose-400 font-bold">No receipt found for "${ref}". Please ensure you completed Telegram verification.</p>`;
            }
        }

        // ==========================================
        // UI UTILITIES: THEME, TOAST & CLIPBOARD
        // ==========================================
        function toggleTheme() {
            const html = document.documentElement;
            const themeIcon = document.getElementById('theme-icon');
            if (html.classList.contains('dark')) {
                html.classList.remove('dark');
                localStorage.setItem('qc_theme', 'light');
                themeIcon.className = 'fa-solid fa-sun';
            } else {
                html.classList.add('dark');
                localStorage.setItem('qc_theme', 'dark');
                themeIcon.className = 'fa-solid fa-moon';
            }
        }

        function applyThemeFromStorage() {
            const theme = localStorage.getItem('qc_theme') || 'dark';
            const html = document.documentElement;
            const themeIcon = document.getElementById('theme-icon');
            if (theme === 'light') {
                html.classList.remove('dark');
                themeIcon.className = 'fa-solid fa-sun';
            } else {
                html.classList.add('dark');
                themeIcon.className = 'fa-solid fa-moon';
            }
        }

        function copyToClipboard(text) {
            const dummy = document.createElement("textarea");
            document.body.appendChild(dummy);
            dummy.value = text;
            dummy.select();
            document.execCommand("copy");
            document.body.removeChild(dummy);
        }

        function showToast(message, type = 'info') {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            
            const colorMap = {
                success: 'bg-emerald-500/90 text-white border-emerald-400',
                info: 'bg-obsidian-800 text-amber-400 border-amber-500/50',
                error: 'bg-rose-500/90 text-white border-rose-400'
            };

            const iconMap = {
                success: 'fa-circle-check',
                info: 'fa-circle-info',
                error: 'fa-triangle-exclamation'
            };

            toast.className = `p-3.5 rounded-xl border shadow-xl text-xs font-bold flex items-center gap-3 backdrop-blur-md transition-all duration-300 transform translate-x-10 pointer-events-auto ${colorMap[type] || colorMap.info}`;
            toast.innerHTML = `<i class="fa-solid ${iconMap[type] || iconMap.info} text-base"></i><span>${message}</span>`;
            
            container.appendChild(toast);
            
            requestAnimationFrame(() => {
                toast.classList.remove('translate-x-10');
            });

            setTimeout(() => {
                toast.classList.add('opacity-0', 'translate-x-10');
                setTimeout(() => toast.remove(), 300);
            }, 3500);
        }

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    </script>
</body>
</html>
