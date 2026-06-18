<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>FIRE ARENA - India's Ultimate Esports Tournament Arena</title>
    <!-- Google Fonts Poppins -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Bootstrap CSS CDN -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <!-- Bootstrap Icons CDN -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css" rel="stylesheet">
    
    <!-- Swiper.js CSS CDN -->
    <link href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" rel="stylesheet">

    <style>
      /* Base Theme Colors & Variables */
      :root {
        --primary-bg: #0F172A;
        --secondary-bg: #1E293B;
        --text-primary: #E2E8F0;
        --text-secondary: #94A3B8;
        --accent-color: #FACC15;
        --border-color: #334155;
        --glow-color: rgba(250, 204, 21, 0.4);
      }

      body {
        background-color: var(--primary-bg);
        color: var(--text-primary);
        font-family: 'Poppins', sans-serif;
        overflow-x: hidden;
        padding-bottom: 72px; /* For mobile sticky bar */
      }
      
      @media (min-width: 768px) {
        body {
          padding-bottom: 0;
        }
      }

      /* Custom Accent Styles */
      .text-accent {
        color: var(--accent-color) !important;
      }
      
      /* Navigation Bar Styling */
      .navbar-custom {
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        background: rgba(15, 23, 42, 0.82);
        border-bottom: 1px solid var(--border-color);
        transition: all 0.3s ease;
      }
      
      .logo-frame {
        width: 44px;
        height: 44px;
        border-radius: 50%;
        border: 2px solid var(--accent-color);
        padding: 2px;
        background-color: var(--secondary-bg);
        display: flex;
        align-items: center;
        justify-content: center;
        box-shadow: 0 0 10px var(--glow-color);
      }

      .logo-frame img {
        width: 100%;
        height: 100%;
        object-fit: contain;
        border-radius: 50%;
      }

      .nav-link {
        color: var(--text-primary) !important;
        font-weight: 500;
        transition: color 0.2s ease;
      }

      .nav-link:hover, .nav-link:focus {
        color: var(--accent-color) !important;
      }

      /* Buttons & Badges Styling */
      .btn-accent {
        background-color: var(--accent-color);
        color: #000000 !important;
        font-weight: 700;
        border: none;
        border-radius: 8px;
        transition: all 0.3s ease;
        box-shadow: 0 4px 15px rgba(250, 204, 21, 0.3);
      }

      .btn-accent:hover {
        background-color: #eab308;
        transform: translateY(-2px);
        box-shadow: 0 6px 20px rgba(250, 204, 21, 0.5);
      }

      .btn-outline-accent {
        background: transparent;
        color: var(--accent-color) !important;
        border: 2px solid var(--accent-color);
        font-weight: 600;
        transition: all 0.3s ease;
      }

      .btn-outline-accent:hover {
        background: var(--accent-color);
        color: #000000 !important;
        transform: translateY(-2px);
      }

      /* Hero Section Elements */
      .hero-section {
        position: relative;
        padding: 140px 0 80px 0;
        z-index: 10;
      }

      .hero-title {
        font-size: 2.8rem;
        font-weight: 800;
        line-height: 1.2;
        letter-spacing: -0.02em;
      }

      @media (min-width: 768px) {
        .hero-title {
          font-size: 4.2rem;
        }
      }

      .hero-subtitle {
        color: var(--text-secondary);
        font-size: 1.1rem;
        max-width: 700px;
        margin: 0 auto;
        line-height: 1.6;
      }

      .hero-logo-container {
        position: relative;
        display: inline-block;
        margin-top: 50px;
      }

      .hero-logo-img {
        width: 250px;
        height: 250px;
        object-fit: contain;
        animation: float 4s ease-in-out infinite;
        filter: drop-shadow(0 0 25px rgba(250, 204, 21, 0.4));
      }

      @media (min-width: 768px) {
        .hero-logo-img {
          width: 320px;
          height: 320px;
        }
      }
      
      /* Game Slider Section */
      .game-slider-section {
        background-color: var(--secondary-bg);
        border-top: 1px solid var(--border-color);
        border-bottom: 1px solid var(--border-color);
        padding: 80px 0;
        position: relative;
      }

      .game-swiper {
        padding: 20px 0 50px 0;
      }

      .game-swiper .swiper-slide {
        width: 280px;
        opacity: 0.5;
        transition: opacity 0.3s ease, transform 0.3s ease;
      }

      .game-swiper .swiper-slide-active {
        opacity: 1;
        transform: scale(1.05);
      }

      .game-card {
        background: #1e293b;
        background: linear-gradient(145deg, #1e293b 0%, #111827 100%);
        border: 1px solid var(--border-color);
        border-radius: 16px;
        padding: 24px;
        text-align: center;
        box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        transition: all 0.3s ease;
      }

      .game-card:hover {
        border-color: var(--accent-color);
        box-shadow: 0 10px 30px rgba(250, 204, 21, 0.2);
      }

      .game-card img {
        height: 140px;
        object-fit: contain;
        margin-bottom: 15px;
        filter: drop-shadow(0 8px 12px rgba(0,0,0,0.4));
        transition: transform 0.3s ease;
      }

      .game-card:hover img {
        transform: translateY(-5px);
      }

      /* How it Works Section */
      .how-it-works-section {
        padding: 80px 0;
      }

      .step-card {
        background-color: var(--secondary-bg);
        border: 1px solid var(--border-color);
        border-radius: 16px;
        padding: 40px 30px;
        position: relative;
        overflow: hidden;
        height: 100%;
        transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        z-index: 1;
      }

      .step-card:hover {
        transform: translateY(-8px);
        border-color: var(--accent-color);
        box-shadow: 0 15px 35px rgba(250, 204, 21, 0.12);
      }

      .step-number {
        position: absolute;
        right: 15px;
        bottom: -15px;
        font-size: 6rem;
        font-weight: 800;
        color: var(--accent-color);
        opacity: 0.04;
        transition: opacity 0.3s ease;
        line-height: 1;
        user-select: none;
        z-index: -1;
      }

      .step-card:hover .step-number {
        opacity: 0.08;
      }

      .step-icon-wrapper {
        width: 65px;
        height: 65px;
        background-color: rgba(250, 204, 21, 0.1);
        border: 1px solid rgba(250, 204, 21, 0.2);
        border-radius: 14px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.8rem;
        color: var(--accent-color);
        margin-bottom: 24px;
      }

      /* Features Grid */
      .features-section {
        background-color: var(--secondary-bg);
        border-top: 1px solid var(--border-color);
        border-bottom: 1px solid var(--border-color);
        padding: 80px 0;
      }

      .feature-item {
        background-color: rgba(15, 23, 42, 0.4);
        border: 1px solid var(--border-color);
        border-radius: 16px;
        padding: 30px;
        height: 100%;
        transition: border-color 0.3s ease;
      }

      .feature-item:hover {
        border-color: var(--accent-color);
      }

      .feature-icon-wrapper {
        font-size: 2.2rem;
        color: var(--accent-color);
        margin-bottom: 20px;
      }

      /* FAQ Accordion */
      .faq-section {
        padding: 80px 0;
      }

      .accordion-item {
        background-color: var(--secondary-bg) !important;
        border: 1px solid var(--border-color) !important;
        margin-bottom: 15px;
        border-radius: 12px !important;
        overflow: hidden;
      }

      .accordion-button {
        background-color: var(--secondary-bg) !important;
        color: var(--text-primary) !important;
        font-weight: 600;
        border: none !important;
        padding: 20px;
        box-shadow: none !important;
      }

      .accordion-button:not(.collapsed) {
        color: var(--accent-color) !important;
        border-bottom: 1px solid var(--border-color) !important;
      }

      .accordion-button::after {
        filter: invert(1);
      }

      .accordion-body {
        color: var(--text-secondary);
        background-color: rgba(15, 23, 42, 0.3);
        line-height: 1.7;
      }

      /* Policy Modals */
      .modal-content {
        background-color: var(--secondary-bg) !important;
        border: 1px solid var(--border-color) !important;
        color: var(--text-primary) !important;
      }
      
      .modal-header {
        border-bottom: 1px solid var(--border-color) !important;
      }

      .modal-footer {
        border-top: 1px solid var(--border-color) !important;
      }

      .modal-body {
        font-size: 0.95rem;
        line-height: 1.7;
        color: var(--text-secondary);
        max-height: 480px;
        overflow-y: auto;
      }

      .modal-body h5, .modal-body h6 {
        color: var(--text-primary);
        margin-top: 20px;
        font-weight: 600;
      }

      /* Footer */
      footer {
        background-color: #080D1A;
        border-top: 1px solid var(--border-color);
        padding: 40px 0;
      }

      /* Sticky Mobile Bar */
      .mobile-sticky-bar {
        background: rgba(15, 23, 42, 0.9);
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        border-top: 1px solid var(--border-color);
        z-index: 1050;
      }

      /* Animations */
      @keyframes float {
        0% { transform: translateY(0px) rotate(0deg); }
        50% { transform: translateY(-15px) rotate(2deg); }
        100% { transform: translateY(0px) rotate(0deg); }
      }

      @keyframes pulse {
        0%, 100% { opacity: 1; transform: scale(1); }
        50% { opacity: 0.85; transform: scale(1.02); }
      }

      .animate-pulse {
        animation: pulse 2.5s infinite;
      }

      /* Scroll Animation Classes */
      .animate-on-scroll {
        opacity: 0;
        transform: translateY(30px);
        transition: opacity 0.8s ease-out, transform 0.8s ease-out;
      }

      .animate-on-scroll.visible {
        opacity: 1;
        transform: translateY(0);
      }

      /* Swiper customizations */
      .swiper-pagination-bullet {
        background: var(--text-secondary) !important;
      }
      
      .swiper-pagination-bullet-active {
        background: var(--accent-color) !important;
        width: 18px;
        border-radius: 4px;
        transition: width 0.3s ease;
      }

      /* Glow background shapes */
      .bg-glow {
        position: absolute;
        width: 500px;
        height: 500px;
        border-radius: 50%;
        background: radial-gradient(circle, rgba(250, 204, 21, 0.05) 0%, rgba(15, 23, 42, 0) 70%);
        pointer-events: none;
        z-index: 1;
      }
      
      .bg-glow-1 {
        top: -50px;
        left: -100px;
      }
      
      .bg-glow-2 {
        bottom: 20%;
        right: -100px;
      }
    </style>
  </head>
  <body>

    <!-- Background Ambient Glows -->
    <div class="bg-glow bg-glow-1"></div>
    <div class="bg-glow bg-glow-2"></div>

    <!-- Navigation Header -->
    <nav class="navbar navbar-expand-lg navbar-dark sticky-top navbar-custom py-3">
      <div class="container">
        <!-- Logo and App Name -->
        <a class="navbar-brand d-flex align-items-center gap-2" href="#">
          <div class="logo-frame">
            <img src="https://iili.io/C24aVdQ.png" alt="FIRE ARENA Logo">
          </div>
          <span class="fw-extrabold tracking-tight fs-4 text-white">FIRE ARENA</span>
        </a>
        
        <!-- Toggle Menu for Mobile -->
        <button class="navbar-toggler border-0 shadow-none text-white" type="button" data-bs-toggle="collapse" data-bs-target="#mainNavbar" aria-controls="mainNavbar" aria-expanded="false" aria-label="Toggle navigation">
          <i class="bi bi-list fs-1 text-accent"></i>
        </button>
        
        <!-- Navbar collapse menu -->
        <div class="collapse navbar-collapse" id="mainNavbar">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0 align-items-lg-center gap-lg-3">
            <li class="nav-item">
              <a class="nav-link" href="#home">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#how-to-play">How to Play</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#features">Features</a>
            </li>
            
            <!-- More Dropdown -->
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle d-flex align-items-center gap-1" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                More
              </a>
              <ul class="dropdown-menu dropdown-menu-dark bg-dark border-secondary p-2 shadow-lg">
                <li><a class="dropdown-item py-2 text-white" href="#faq">FAQ</a></li>
                <li><hr class="dropdown-divider border-secondary"></li>
                <li><a class="dropdown-item py-2 text-white-50 hover-accent" href="#" data-bs-toggle="modal" data-bs-target="#privacyModal">Privacy Policy</a></li>
                <li><a class="dropdown-item py-2 text-white-50 hover-accent" href="#" data-bs-toggle="modal" data-bs-target="#termsModal">Terms & Conditions</a></li>
                <li><a class="dropdown-item py-2 text-white-50 hover-accent" href="#" data-bs-toggle="modal" data-bs-target="#fairplayModal">Fair Play Policy</a></li>
                <li><a class="dropdown-item py-2 text-white-50 hover-accent" href="#" data-bs-toggle="modal" data-bs-target="#refundModal">Refund & Cancellation</a></li>
              </ul>
            </li>
            
            <!-- CTA Button Dropdown -->
            <li class="nav-item dropdown ms-lg-2 mt-3 mt-lg-0">
              <button class="btn btn-accent px-4 py-2 d-inline-flex align-items-center gap-2 dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                <i class="bi bi-download"></i> Download App
              </button>
              <ul class="dropdown-menu dropdown-menu-dark bg-dark border-secondary p-2 shadow-lg dropdown-menu-end">
                <li>
                  <a href="https://www.mediafire.com/file/znot1lj4otz0g9h/FIRE_ARENA.apk/file" target="_blank" class="dropdown-item py-2 text-white d-flex align-items-center gap-2">
                    <i class="bi bi-rocket-takeoff-fill text-accent"></i> FIRE ARENA (Stable APK)
                  </a>
                </li>
                <li>
                  <a href="https://www.mediafire.com/file/nmvsd071j99gfcw/ASTUTE+BETA+OB53.apk/file?dkey=5qul4ipdidt&r=130" target="_blank" class="dropdown-item py-2 text-white d-flex align-items-center gap-2">
                    <i class="bi bi-cpu-fill text-accent"></i> ASTUTE BETA OB53 APK
                  </a>
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-section text-center">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-10 animate-on-scroll">
            
            <!-- App Name Spark Badge -->
            <div class="d-inline-flex align-items-center gap-2 bg-secondary-bg border border-secondary px-3 py-1.5 rounded-pill mb-4 shadow-sm animate-pulse">
              <i class="bi bi-shield-lock-fill text-accent"></i>
              <span class="text-white-50 fs-7 fw-medium">💯 Safe & Play-Store Audited Esports Platform</span>
            </div>
            
            <!-- Main Title -->
            <h1 class="hero-title mb-4 text-white">
              India's Ultimate <span class="text-accent">Esports Arena</span> is Here
            </h1>
            
            <!-- description paragraph -->
            <p class="hero-subtitle mb-5">
              Turn your gaming prowess into cold cash. Battle against top-tier squads in professional BGMI, Free Fire Max, and PUBG lobbies. Join daily live room events, earn real prizes, and showcase your skills!
            </p>
            
            <!-- Button Actions -->
            <div class="d-flex flex-column flex-md-row justify-content-center align-items-center gap-3 mb-4">
              <a href="https://www.mediafire.com/file/znot1lj4otz0g9h/FIRE_ARENA.apk/file" target="_blank" class="btn btn-accent btn-lg px-4 py-3 fs-6 d-inline-flex align-items-center gap-2">
                <i class="bi bi-download"></i> Download FIRE ARENA (Stable)
              </a>
              <a href="https://www.mediafire.com/file/nmvsd071j99gfcw/ASTUTE+BETA+OB53.apk/file?dkey=5qul4ipdidt&r=130" target="_blank" class="btn btn-outline-accent btn-lg px-4 py-3 fs-6 d-inline-flex align-items-center gap-2">
                <i class="bi bi-cloud-arrow-down-fill"></i> Download ASTUTE BETA (OB53)
              </a>
            </div>
            
            <div class="mb-5">
              <a href="#how-to-play" class="btn btn-outline-accent btn-md px-4 py-2 rounded-pill d-inline-flex align-items-center gap-2 w-auto">
                <i class="bi bi-gift-fill fs-5"></i> Get ₹10 FREE on Signup!
              </a>
            </div>
            
            <!-- App Logo Visual -->
            <div class="hero-logo-container">
              <div class="bg-glow" style="top: 10%; left: 10%; background: radial-gradient(circle, rgba(250, 204, 21, 0.15) 0%, rgba(15, 23, 42, 0) 75%);"></div>
              <img src="https://iili.io/C24aVdQ.png" alt="FIRE ARENA App Logo" class="hero-logo-img">
            </div>
            
          </div>
        </div>
      </div>
    </section>

    <!-- Game Slider Section -->
    <section class="game-slider-section">
      <div class="container">
        <div class="row justify-content-center text-center mb-5 animate-on-scroll">
          <div class="col-lg-8">
            <h2 class="fw-bold tracking-tight text-white mb-3">Tournaments for Your Favorite Games</h2>
            <p class="text-secondary">Explore esports lobbies happening 24/7. Pick your battlefield and claim victory.</p>
          </div>
        </div>
        
        <!-- Swiper container -->
        <div class="swiper game-swiper animate-on-scroll">
          <div class="swiper-wrapper">
            <!-- BGMI Slide -->
            <div class="swiper-slide">
              <div class="game-card">
                <img src="https://www.gamerji.com/img/games/BGMI.png" alt="BGMI logo" class="img-fluid">
                <h4 class="fw-bold text-white mb-2">BGMI</h4>
                <p class="text-secondary fs-7 mb-3">Solo & Squad daily battles with massive winning structures.</p>
                <a href="https://www.mediafire.com/file/znot1lj4otz0g9h/FIRE_ARENA.apk/file" target="_blank" class="btn btn-outline-accent btn-sm py-2 px-4 w-100">Battle Now</a>
              </div>
            </div>
            <!-- FFM Slide -->
            <div class="swiper-slide">
              <div class="game-card">
                <img src="https://www.gamerji.com/img/games/FFM.png" alt="Free Fire Max logo" class="img-fluid">
                <h4 class="fw-bold text-white mb-2">Free Fire Max</h4>
                <p class="text-secondary fs-7 mb-3">Survival skirmishes with ultra fast-paced lobbies and rewards.</p>
                <a href="https://www.mediafire.com/file/znot1lj4otz0g9h/FIRE_ARENA.apk/file" target="_blank" class="btn btn-outline-accent btn-sm py-2 px-4 w-100">Play Now</a>
              </div>
            </div>
            <!-- PUBG Slide -->
            <div class="swiper-slide">
              <div class="game-card">
                <img src="https://www.gamerji.com/img/games/Pubg_New_State.png" alt="Pubg New State logo" class="img-fluid">
                <h4 class="fw-bold text-white mb-2">PUBG New State</h4>
                <p class="text-secondary fs-7 mb-3">Next-gen futuristic arena competition with global esports veterans.</p>
                <a href="https://www.mediafire.com/file/znot1lj4otz0g9h/FIRE_ARENA.apk/file" target="_blank" class="btn btn-outline-accent btn-sm py-2 px-4 w-100">Enter Arena</a>
              </div>
            </div>
          </div>
          <!-- Pagination -->
          <div class="swiper-pagination mt-4 position-relative"></div>
        </div>
      </div>
    </section>

    <!-- How It Works Section -->
    <section id="how-to-play" class="how-it-works-section">
      <div class="container">
        <div class="row justify-content-center text-center mb-5 animate-on-scroll">
          <div class="col-lg-8">
            <span class="badge bg-warning-subtle text-warning border border-warning px-3 py-1.5 rounded-pill mb-3 fw-bold">Simple 3-Step Setup</span>
            <h2 class="fw-bold tracking-tight text-white">How It Works</h2>
            <p class="text-secondary">Becoming an esports champion on our tournament app is straightforward. Follow these steps to win cash prizes.</p>
          </div>
        </div>
        
        <div class="row g-4 justify-content-center">
          <!-- Step 1 -->
          <div class="col-md-4 animate-on-scroll">
            <div class="step-card">
              <div class="step-number">01</div>
              <div class="step-icon-wrapper">
                <i class="bi bi-cloud-arrow-down-fill"></i>
              </div>
              <h4 class="fw-bold text-white mb-3">1. Download & Register</h4>
              <p class="text-secondary mb-0">Get the off-store verified APK link. Install safely, create your unique user account in seconds, and secure your ₹10 signup bonus directly into your app wallet.</p>
            </div>
          </div>
          <!-- Step 2 -->
          <div class="col-md-4 animate-on-scroll" style="transition-delay: 0.15s;">
            <div class="step-card">
              <div class="step-number">02</div>
              <div class="step-icon-wrapper">
                <i class="bi bi-trophy-fill"></i>
              </div>
              <h4 class="fw-bold text-white mb-3">2. Join a Tournament</h4>
              <p class="text-secondary mb-0">Browse through hundreds of scheduled high-multiplier contests for BGMI and Free Fire. Enter with your preferred squad size and level using your starting wallet bonus!</p>
            </div>
          </div>
          <!-- Step 3 -->
          <div class="col-md-4 animate-on-scroll" style="transition-delay: 0.3s;">
            <div class="step-card">
              <div class="step-number">03</div>
              <div class="step-icon-wrapper">
                <i class="bi bi-cash-coin"></i>
              </div>
              <h4 class="fw-bold text-white mb-3">3. Play, Win & Withdraw</h4>
              <p class="text-secondary mb-0">Hop onto the customized live match, play responsibly by rules, rack up high kill records, and withdraw your prize money instantly via UPI/Paytm with bank verification.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features-section">
      <div class="container">
        <div class="row justify-content-center text-center mb-5 animate-on-scroll">
          <div class="col-lg-8">
            <span class="badge bg-warning-subtle text-warning border border-warning px-3 py-1.5 rounded-pill mb-3 fw-bold">Why Tournament Players Choose Us</span>
            <h2 class="fw-bold tracking-tight text-white text-md-center">Empowering India's Mobile Competitors</h2>
            <p class="text-secondary">We build high-octane esports tech supporting honest competitive fair play, safe server environments, and rapid withdraw support.</p>
          </div>
        </div>
        
        <div class="row g-4">
          <!-- Feature 1 -->
          <div class="col-md-6 animate-on-scroll">
            <div class="feature-item">
              <div class="feature-icon-wrapper">
                <i class="bi bi-shield-fill-check"></i>
              </div>
              <h4 class="fw-bold text-white mb-3">100% Secure & Fair Play</h4>
              <p class="text-secondary mb-0">Advanced custom anticheat algorithms filter emulators and aim hacks. Dedicated referees audit lobbies live to assure zero compromise on tactical battle fairness.</p>
            </div>
          </div>
          <!-- Feature 2 -->
          <div class="col-md-6 animate-on-scroll" style="transition-delay: 0.15s;">
            <div class="feature-item">
              <div class="feature-icon-wrapper">
                <i class="bi bi-lightning-fill"></i>
              </div>
              <h4 class="fw-bold text-white mb-3">Instant Withdrawals</h4>
              <p class="text-secondary mb-0">Never wait for your winnings. Easily bind your UPI id, Paytm Wallet, or Bank account, and transfer funds instantly to cash out whenever you hit the threshold.</p>
            </div>
          </div>
          <!-- Feature 3 -->
          <div class="col-md-6 animate-on-scroll">
            <div class="feature-item">
              <div class="feature-icon-wrapper">
                <i class="bi bi-people-fill"></i>
              </div>
              <h4 class="fw-bold text-white mb-3">Generous Referral Program</h4>
              <p class="text-secondary mb-0">Invite your friends to squad up. Share your custom app referral link and earn commissions on their entry ticket deposits, giving you extra credits to play cash matches.</p>
            </div>
          </div>
          <!-- Feature 4 -->
          <div class="col-md-6 animate-on-scroll" style="transition-delay: 0.15s;">
            <div class="feature-item">
              <div class="feature-icon-wrapper">
                <i class="bi bi-headset"></i>
              </div>
              <h4 class="fw-bold text-white mb-3">24/7 Customer Support</h4>
              <p class="text-secondary mb-0">Direct in-app ticket system and WhatsApp support access. Our specialized agents verify matches, lobby results, and transaction glitches in less than 15 minutes.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq" class="faq-section">
      <div class="container">
        <div class="row justify-content-center text-center mb-5 animate-on-scroll">
          <div class="col-lg-8">
            <h2 class="fw-bold tracking-tight text-white mb-3">Frequently Asked Questions</h2>
            <p class="text-secondary">Have queries regarding lobbies, payouts, or fairness? We got you sorted.</p>
          </div>
        </div>
        
        <div class="row justify-content-center animate-on-scroll">
          <div class="col-lg-9">
            <div class="accordion" id="faqAccordion">
              
              <!-- Question 1 -->
              <div class="accordion-item">
                <h2 class="accordion-header">
                  <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#panel1" aria-expanded="true" aria-controls="panel1">
                    Is playing on FIRE ARENA legal in India?
                  </button>
                </h2>
                <div id="panel1" class="accordion-collapse collapse show" data-bs-parent="#faqAccordion">
                  <div class="accordion-body">
                    Yes, playing mobile esports tournaments falls strictly under "Games of Skill." High legal courts in India protect skill-based gaming as a legitimate commerce activity. However, in accordance with local regulations, users from states restricting play (Assam, Odisha, Telangana, Andhra Pradesh, Sikkim, and Nagaland) cannot entry real-money structures.
                  </div>
                </div>
              </div>
              
              <!-- Question 2 -->
              <div class="accordion-item">
                <h2 class="accordion-header">
                  <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#panel2" aria-expanded="false" aria-controls="panel2">
                    How do I receive my prize withdrawals?
                  </button>
                </h2>
                <div id="panel2" class="accordion-collapse collapse" data-bs-parent="#faqAccordion">
                  <div class="accordion-body">
                    Withdrawal is fast and secure. Go to 'Profile' > 'Withdrawal Wallet,' select your mode (UPI, Netbanking, or Paytm), enter the amount, and initiate. Lobbies winnings are scrutinized instantly and transfer requests are completed mostly in 2 minutes. Standard identity KYC verification might apply for high prize amounts.
                  </div>
                </div>
              </div>
              
              <!-- Question 3 -->
              <div class="accordion-item">
                <h2 class="accordion-header">
                  <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#panel3" aria-expanded="false" aria-controls="panel3">
                    Are there daily free match entries?
                  </button>
                </h2>
                <div id="panel3" class="accordion-collapse collapse" data-bs-parent="#faqAccordion">
                  <div class="accordion-body">
                    We host daily Free Entry (Practice) battles where players can earn cash rewards, testing team play and layout tactics. Use these free entries to gauge lobby skill limits without risking any entry tickets!
                  </div>
                </div>
              </div>

            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer Segment -->
    <footer class="text-center text-white-50">
      <div class="container text-center">
        <div class="d-flex align-items-center justify-content-center gap-2 mb-4">
          <div class="logo-frame" style="width: 32px; height: 32px;">
            <img src="https://iili.io/C24aVdQ.png" alt="Logo">
          </div>
          <span class="text-white fw-bold">FIRE ARENA</span>
        </div>
        
        <!-- App policy links -->
        <div class="d-flex flex-wrap justify-content-center gap-4 mb-4 fs-7">
          <a href="#" class="text-white-50 text-decoration-none hover-accent" data-bs-toggle="modal" data-bs-target="#privacyModal">Privacy Policy</a>
          <a href="#" class="text-white-50 text-decoration-none hover-accent" data-bs-toggle="modal" data-bs-target="#termsModal">Terms & Conditions</a>
          <a href="#" class="text-white-50 text-decoration-none hover-accent" data-bs-toggle="modal" data-bs-target="#fairplayModal">Fair Play Policy</a>
          <a href="#" class="text-white-50 text-decoration-none hover-accent" data-bs-toggle="modal" data-bs-target="#refundModal">Refund Policy</a>
        </div>
        
        <!-- Gaming Disclaimer and copyright notice -->
        <div class="row justify-content-center">
          <div class="col-lg-8 mb-3">
            <p class="fs-8 text-secondary lh-lg mb-0">
              Disclaimer: Real-money esports games on this platform can be addictive and carry financial risk. Play responsibly and at your own discretion. Access is strictly age-restricted to 18+ years of age. Operational jurisdictions exclude states with regulatory restricts on game monetization.
            </p>
          </div>
        </div>
        
        <p class="fs-8 text-secondary mb-0">&copy; 2026 FIRE ARENA. All Rights Reserved.</p>
      </div>
    </footer>

    <!-- STICKY DOWNLOAD BAR (Mobile Only) -->
    <div class="d-block d-md-none position-fixed bottom-0 start-0 w-100 p-2 mobile-sticky-bar text-center">
      <div class="row g-2">
        <div class="col-6">
          <a href="https://www.mediafire.com/file/znot1lj4otz0g9h/FIRE_ARENA.apk/file" target="_blank" class="btn btn-accent w-100 py-2.5 fs-7 d-flex align-items-center justify-content-center gap-1 shadow">
            <i class="bi bi-download"></i> Stable APK
          </a>
        </div>
        <div class="col-6">
          <a href="https://www.mediafire.com/file/nmvsd071j99gfcw/ASTUTE+BETA+OB53.apk/file?dkey=5qul4ipdidt&r=130" target="_blank" class="btn btn-outline-accent w-100 py-2.5 fs-7 d-flex align-items-center justify-content-center gap-1 shadow">
            <i class="bi bi-cloud-arrow-down-fill"></i> Astute Beta
          </a>
        </div>
      </div>
    </div>

    <!-- POLICY MODALS -->

    <!-- Privacy Policy Modal -->
    <div class="modal fade" id="privacyModal" tabindex="-1" aria-labelledby="privacyModalLabel" aria-hidden="true" data-bs-theme="dark">
      <div class="modal-dialog modal-dialog-centered modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title text-accent" id="privacyModalLabel">Privacy Policy</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <p>Welcome to <span class="text-accent fw-bold">FIRE ARENA</span>. We value the privacy of our competitors and users. This Privacy Policy outlines what data we compile, encrypt, and secure when playing on <span class="text-accent fw-bold">FIRE ARENA</span>.</p>
            
            <h5>1. Information We Collect</h5>
            <p>To enable clean tournament play and match management, <span class="text-accent fw-bold">FIRE ARENA</span> processes basic details including user-created handles, email ids, mobile verifications, and regional GPS location coordinates. Location checks help us filter compliance for regulatory laws across Indian states.</p>
            
            <h5>2. Device and In-App Security Data</h5>
            <p>To prevent cheating, we audit device specifics including operating system platforms, memory hashes, and client integrity values. Rest assured, <span class="text-accent fw-bold">FIRE ARENA</span> strictly isolates system safety data for anticheat matches auditing only.</p>
            
            <h5>3. Wallet and Bank Lobbies Integrations</h5>
            <p>All deposits and instant withdrawals on <span class="text-accent fw-bold">FIRE ARENA</span> are handled by certified UPI and regional PCI-complied payment aggregators. <span class="text-accent fw-bold">FIRE ARENA</span> does not log raw bank passwords or sensitive UPI credentials on our central server.</p>
            
            <h5>4. Contact Us</h5>
            <p>For any queries about your stored player accounts profile, contact support on help@<span class="text-accent fw-bold">FIRE ARENA</span>.com.</p>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-accent btn-sm" data-bs-dismiss="modal">I Understand</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Terms & Conditions Modal -->
    <div class="modal fade" id="termsModal" tabindex="-1" aria-labelledby="termsModalLabel" aria-hidden="true" data-bs-theme="dark">
      <div class="modal-dialog modal-dialog-centered modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title text-accent" id="termsModalLabel">Terms & Conditions</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <p>These terms govern your subscription and gameplay on the <span class="text-accent fw-bold">FIRE ARENA</span> tournament network. Please read these agreements thoroughly.</p>
            
            <h5>1. Account Eligibility</h5>
            <p>Competitors on <span class="text-accent fw-bold">FIRE ARENA</span> must declare they are 18 years or older. Our platform serves purely as a skills-based forum. Lobbies involving monetary prizes are strictly inaccessible to players operating from restricted gaming states: Assam, Andhra Pradesh, Odisha, Sikkim, Telangana, and Nagaland.</p>
            
            <h5>2. Game Lobbies Integrity</h5>
            <p>Competiotors must strictly register their authentic game accounts (BGMI/FFM characters ids) inside <span class="text-accent fw-bold">FIRE ARENA</span> app module. Entering brackets using unregistered characters results in direct lobby expulsion with zero tickets claim.</p>
            
            <h5>3. Commission Fees & Rewards Pools</h5>
            <p><span class="text-accent fw-bold">FIRE ARENA</span> reserves the right to capture nominal platforms organizer handling fees from user entries prior to distributing structured winning wallets pools.</p>
            
            <h5>4. Account Suspension Terminals</h5>
            <p>We lock accounts permanently if users practice toxic verbal, malicious hacking, or collusion with opponents on <span class="text-accent fw-bold">FIRE ARENA</span> lobbies.</p>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-accent btn-sm" data-bs-dismiss="modal">Accept Terms</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Fair Play Policy Modal -->
    <div class="modal fade" id="fairplayModal" tabindex="-1" aria-labelledby="fairplayModalLabel" aria-hidden="true" data-bs-theme="dark">
      <div class="modal-dialog modal-dialog-centered modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title text-accent" id="fairplayModalLabel">Fair Play Policy</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <p>At <span class="text-accent fw-bold">FIRE ARENA</span>, maintaining transparent esports sportsmanship holds top priority. Every participant must abide by this strict outline.</p>
            
            <h5>1. Prohibited Hack Utilities</h5>
            <p>Employing third-party aimbots, wallhacks, movement triggers, or emulator mods on standard mobile brackets of <span class="text-accent fw-bold">FIRE ARENA</span> is strictly illegal. All lobbies are inspected by anticheat drivers.</p>
            
            <h5>2. Collusion and Unfair Teaming</h5>
            <p>Working in agreement with other lobbies squads to throw matches or trade kills leads to direct disqualification and forfeiture of wallet records across all implicated accounts on <span class="text-accent fw-bold">FIRE ARENA</span>.</p>
            
            <h5>3. Emulator Restriction</h5>
            <p>Unless a lobby explicitly specifies "Emulator Supported," players must join using physical smartphones only. Emulator play on regular matches is monitored and automatically banned on <span class="text-accent fw-bold">FIRE ARENA</span>.</p>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-accent btn-sm" data-bs-dismiss="modal">Accept Policy</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Refund Policy Modal -->
    <div class="modal fade" id="refundModal" tabindex="-1" aria-labelledby="refundModalLabel" aria-hidden="true" data-bs-theme="dark">
      <div class="modal-dialog modal-dialog-centered modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title text-accent" id="refundModalLabel">Refund & Cancellation Policy</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <p>This document details our stance on transactional balances deposits, tournament cancellation, and handling issues on <span class="text-accent fw-bold">FIRE ARENA</span>.</p>
            
            <h5>1. Tournament Cancellations</h5>
            <p>If a tournament on <span class="text-accent fw-bold">FIRE ARENA</span> gets canceled by admins due to server glitches, patch updates, or low lobby subscriptions, the entire entry fee will reflect back in the player's core wallet within 24 hours.</p>
            
            <h5>2. Player Absence & Connectivity Troubles</h5>
            <p>Once a bracket lobby begins, no entry ticket fee refunds are processed for players who fail to join due to local device issues, low in-match pings, or internet failures. It is your sole responsibility to be online in <span class="text-accent fw-bold">FIRE ARENA</span> rooms.</p>
            
            <h5>3. Failed Transactions</h5>
            <p>In cases where money got debited but wallet deposit hasn't updated on <span class="text-accent fw-bold">FIRE ARENA</span>, payment aggregators typically clear balances in 3-5 bank business days.</p>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-accent btn-sm" data-bs-dismiss="modal">I Agree</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Bootstrap & Swiper JS Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>

    <script>
      // Initialize Swiper Game Slider
      document.addEventListener("DOMContentLoaded", function() {
        new Swiper('.game-swiper', {
          slidesPerView: 'auto',
          centeredSlides: true,
          spaceBetween: 24,
          loop: true,
          autoplay: {
            delay: 3500,
            disableOnInteraction: false,
          },
          pagination: {
            el: '.swiper-pagination',
            clickable: true,
          }
        });

        // Intersection Observer Scroll Animations
        const animatedElements = document.querySelectorAll('.animate-on-scroll');
        const observer = new IntersectionObserver((entries) => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              entry.target.classList.add('visible');
            }
          });
        }, { 
          threshold: 0.15,
          rootMargin: "0px 0px -50px 0px"
        });

        animatedElements.forEach(el => {
          observer.observe(el);
        });
      });
    </script>
  </body>
</html>