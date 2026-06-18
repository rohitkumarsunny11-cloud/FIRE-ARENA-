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
                <p c
