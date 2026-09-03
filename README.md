<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0" />
  <title>BA'II IMAM ZANAWI — Portfolio Profesional</title>
  <meta name="description" content="Portfolio pribadi BA'II IMAM ZANAWI — karya digital, fotografi, dan profesional branding." />
  <style>
    /* === RESET & VARIABLES === */
    :root {
      --bg: #faf9f7;
      --bg-card: #ffffff;
      --text: #1e1e1f;
      --text-soft: #4b4b4f;
      --border: #e7e5e4;
      --accent: #0f766e;
      --accent-hover: #0d5f58;
      --shadow: 0 6px 18px rgba(0, 0, 0, 0.04);
      --shadow-hover: 0 14px 28px rgba(0, 0, 0, 0.07);
      --radius: 18px;
      --radius-sm: 12px;
      --font: 'Plus Jakarta Sans', 'Inter', system-ui, -apple-system, sans-serif;
      --maxw: 1200px;
      --header-h: 72px;
    }

    .dark {
      --bg: #141416;
      --bg-card: #1e1e21;
      --text: #f1f1f2;
      --text-soft: #b8b8be;
      --border: #2c2c31;
      --accent: #2aa79d;
      --accent-hover: #259b92;
      --shadow: 0 6px 18px rgba(0, 0, 0, 0.25);
      --shadow-hover: 0 16px 32px rgba(0, 0, 0, 0.35);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      font-family: var(--font);
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      transition: background 0.3s ease, color 0.3s ease;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }
    img {
      max-width: 100%;
      display: block;
      border-radius: var(--radius-sm);
    }
    button {
      font-family: inherit;
      cursor: pointer;
      border: none;
      background: none;
      color: inherit;
    }

    .container {
      max-width: var(--maxw);
      margin: 0 auto;
      padding: 0 24px;
    }

    /* === TYPOGRAPHY === */
    h1, h2, h3, h4 {
      font-weight: 700;
      letter-spacing: -0.02em;
      line-height: 1.2;
    }
    .section-title {
      font-size: clamp(1.8rem, 4vw, 2.8rem);
      margin-bottom: 16px;
      color: var(--text);
    }
    .section-sub {
      font-size: 1.1rem;
      color: var(--text-soft);
      margin-bottom: 40px;
      max-width: 650px;
    }

    /* === BUTTONS === */
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 12px 28px;
      border-radius: 40px;
      font-weight: 600;
      font-size: 0.95rem;
      transition: all 0.25s ease;
      border: 1px solid transparent;
      letter-spacing: 0.01em;
    }
    .btn-primary {
      background: var(--accent);
      color: #fff;
      box-shadow: 0 6px 16px rgba(15, 118, 110, 0.25);
    }
    .btn-primary:hover {
      background: var(--accent-hover);
      transform: translateY(-2px);
      box-shadow: 0 12px 24px rgba(15, 118, 110, 0.3);
    }
    .btn-outline {
      border-color: var(--border);
      background: transparent;
      color: var(--text);
    }
    .btn-outline:hover {
      border-color: var(--accent);
      color: var(--accent);
      background: color-mix(in srgb, var(--accent) 6%, transparent);
      transform: translateY(-2px);
    }

    /* === HEADER === */
    .header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: color-mix(in srgb, var(--bg) 82%, transparent);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border);
      height: var(--header-h);
      display: flex;
      align-items: center;
      transition: background 0.3s;
    }
    .nav-wrap {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
    }
    .logo {
      font-weight: 800;
      font-size: 1.5rem;
      letter-spacing: -0.03em;
      color: var(--text);
    }
    .nav-desktop {
      display: flex;
      align-items: center;
      gap: 28px;
    }
    .nav-desktop a {
      font-size: 0.95rem;
      font-weight: 500;
      color: var(--text-soft);
      transition: color 0.2s;
      position: relative;
    }
    .nav-desktop a:hover,
    .nav-desktop a.active {
      color: var(--accent);
    }
    .nav-desktop a.active::after {
      content: '';
      position: absolute;
      bottom: -6px;
      left: 0;
      width: 100%;
      height: 2px;
      background: var(--accent);
      border-radius: 2px;
    }
    .cta-header {
      margin-left: 12px;
    }
    .hamburger {
      display: none;
      flex-direction: column;
      gap: 5px;
      padding: 8px;
      background: transparent;
    }
    .hamburger span {
      width: 26px;
      height: 2px;
      background: var(--text);
      transition: 0.25s;
      border-radius: 2px;
    }
    .mobile-menu {
      position: fixed;
      top: var(--header-h);
      left: 0;
      width: 100%;
      background: var(--bg-card);
      border-bottom: 1px solid var(--border);
      padding: 20px 24px 32px;
      transform: translateY(-110%);
      transition: transform 0.3s cubic-bezier(0.2, 0.9, 0.3, 1);
      z-index: 99;
      box-shadow: var(--shadow);
    }
    .mobile-menu.open {
      transform: translateY(0);
    }
    .mobile-menu a {
      display: block;
      padding: 12px 0;
      font-weight: 500;
      border-bottom: 1px solid var(--border);
      color: var(--text-soft);
    }
    .mobile-menu a:hover {
      color: var(--accent);
    }

    /* === DARK MODE TOGGLE === */
    .theme-toggle {
      background: var(--bg-card);
      border: 1px solid var(--border);
      width: 40px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50%;
      transition: all 0.25s;
      font-size: 1.2rem;
      margin-left: 10px;
    }
    .theme-toggle:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: rotate(15deg);
    }

    /* === HERO === */
    .hero {
      padding: 70px 0 60px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 50px;
      align-items: center;
    }
    .hero-badge {
      display: inline-block;
      background: color-mix(in srgb, var(--accent) 10%, transparent);
      color: var(--accent);
      padding: 6px 16px;
      border-radius: 40px;
      font-size: 0.85rem;
      font-weight: 600;
      margin-bottom: 20px;
    }
    .hero h1 {
      font-size: clamp(2.3rem, 6vw, 4rem);
      margin-bottom: 16px;
    }
    .hero-desc {
      font-size: 1.15rem;
      color: var(--text-soft);
      margin: 20px 0 28px;
      max-width: 500px;
    }
    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin-bottom: 28px;
    }
    .social-row {
      display: flex;
      gap: 18px;
      font-size: 1.3rem;
      color: var(--text-soft);
    }
    .social-row a {
      transition: color 0.2s, transform 0.2s;
    }
    .social-row a:hover {
      color: var(--accent);
      transform: translateY(-3px);
    }
    .hero-img {
      display: flex;
      justify-content: center;
    }
    .hero-img img {
      width: 340px;
      height: 340px;
      object-fit: cover;
      border-radius: 50%;
      border: 4px solid var(--border);
      box-shadow: var(--shadow-hover);
      background: #d9d9d9;
    }

    /* === CARDS & GRID === */
    .grid-2 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 28px;
    }
    .stat-card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 24px;
      text-align: center;
      box-shadow: var(--shadow);
      transition: all 0.25s;
    }
    .stat-card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-hover);
      border-color: var(--accent);
    }
    .stat-number {
      font-size: 2.4rem;
      font-weight: 800;
      color: var(--accent);
    }

    /* === PORTFOLIO === */
    .filter-bar {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 32px;
    }
    .filter-btn {
      padding: 8px 22px;
      border-radius: 30px;
      border: 1px solid var(--border);
      background: var(--bg-card);
      font-size: 0.9rem;
      font-weight: 500;
      transition: all 0.2s;
    }
    .filter-btn.active,
    .filter-btn:hover {
      background: var(--accent);
      color: white;
      border-color: var(--accent);
    }
    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 24px;
    }
    .project-card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: var(--shadow);
      transition: all 0.3s;
      display: flex;
      flex-direction: column;
    }
    .project-card:hover {
      transform: translateY(-6px);
      box-shadow: var(--shadow-hover);
      border-color: var(--accent);
    }
    .project-thumb {
      height: 180px;
      background: #e2e2e2;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #888;
      font-weight: 500;
    }
    .project-body {
      padding: 20px;
    }

    /* === TIMELINE === */
    .timeline {
      border-left: 3px solid var(--border);
      margin-left: 20px;
      padding-left: 28px;
    }
    .timeline-item {
      margin-bottom: 32px;
      position: relative;
    }
    .timeline-item::before {
      content: '';
      position: absolute;
      left: -36px;
      top: 6px;
      width: 12px;
      height: 12px;
      background: var(--accent);
      border-radius: 50%;
      border: 3px solid var(--bg);
    }

    /* === TABS === */
    .tab-buttons {
      display: flex;
      gap: 16px;
      margin-bottom: 32px;
    }
    .tab-btn {
      padding: 10px 24px;
      border-radius: 40px;
      font-weight: 600;
      background: transparent;
      border: 1px solid var(--border);
    }
    .tab-btn.active {
      background: var(--accent);
      color: white;
    }
    .masonry {
      columns: 3;
      column-gap: 20px;
    }
    .masonry img {
      width: 100%;
      margin-bottom: 20px;
      border-radius: var(--radius-sm);
      transition: transform 0.3s;
    }
    .masonry img:hover {
      transform: scale(1.01);
    }

    /* === TESTIMONIAL CAROUSEL === */
    .testimonial-track {
      display: flex;
      gap: 24px;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      padding-bottom: 20px;
    }
    .testimonial-card {
      scroll-snap-align: start;
      min-width: 280px;
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 24px;
      box-shadow: var(--shadow);
    }

    /* === CONTACT FORM === */
    .contact-wrap {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
    }
    .form-input {
      width: 100%;
      padding: 14px 18px;
      margin-bottom: 18px;
      border-radius: var(--radius-sm);
      border: 1px solid var(--border);
      background: var(--bg-card);
      color: var(--text);
      transition: border 0.2s;
      font-family: inherit;
    }
    .form-input:focus {
      outline: 2px solid var(--accent);
      border-color: transparent;
    }

    /* === FOOTER === */
    footer {
      border-top: 1px solid var(--border);
      padding: 40px 0 24px;
      margin-top: 80px;
    }

    .back-to-top {
      position: fixed;
      bottom: 30px;
      right: 24px;
      background: var(--accent);
      color: white;
      width: 46px;
      height: 46px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: var(--shadow-hover);
      transition: all 0.3s;
      z-index: 80;
      opacity: 0;
      pointer-events: none;
      font-size: 1.3rem;
    }
    .back-to-top.show {
      opacity: 1;
      pointer-events: auto;
    }
    .back-to-top:hover {
      background: var(--accent-hover);
      transform: translateY(-4px);
    }

    /* === RESPONSIVE === */
    @media (max-width: 900px) {
      .nav-desktop { display: none; }
      .hamburger { display: flex; }
      .hero { grid-template-columns: 1fr; text-align: center; }
      .hero-img img { width: 220px; height: 220px; }
      .social-row { justify-content: center; }
      .contact-wrap { grid-template-columns: 1fr; }
      .masonry { columns: 2; }
    }
    @media (max-width: 500px) {
      .masonry { columns: 1; }
      .btn { padding: 10px 20px; }
    }
  </style>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet" />
</head>
<body>
  <!-- LOADING ANIMATION (ringan) -->
  <div id="loader" style="position: fixed; inset:0; background:var(--bg); display:flex; align-items:center; justify-content:center; z-index:200; transition: opacity 0.5s;">
    <div style="width:32px; height:32px; border-radius:50%; border:3px solid var(--accent); border-top-color:transparent; animation:spin 0.8s linear infinite;"></div>
  </div>
  <style>@keyframes spin { to { transform: rotate(360deg); } }</style>

  <!-- HEADER -->
  <header class="header" id="navbar">
    <div class="container nav-wrap">
      <div class="logo">BA'II IMAM</div>
      <nav class="nav-desktop" id="nav-desktop">
        <a href="#beranda" class="active">Beranda</a>
        <a href="#tentang">Tentang Kami</a>
        <a href="#cv">CV</a>
        <a href="#karya">Hasil Karya</a>
        <a href="#fotoartikel">Foto & Artikel</a>
        <a href="#sosmed">Media Sosial</a>
        <a href="#kontak">Kontak</a>
        <a href="#testimoni">Testimoni</a>
      </nav>
      <div style="display:flex; align-items:center;">
        <a href="#kontak" class="btn btn-primary cta-header" style="padding:10px 22px;">Hubungi Saya</a>
        <button class="theme-toggle" id="themeToggle" aria-label="Ganti tema">🌙</button>
        <button class="hamburger" id="hamburgerBtn" aria-label="Menu">
          <span></span><span></span><span></span>
        </button>
      </div>
    </div>
  </header>
  <!-- MOBILE MENU -->
  <div class="mobile-menu" id="mobileMenu">
    <a href="#beranda">Beranda</a>
    <a href="#tentang">Tentang Kami</a>
    <a href="#cv">CV</a>
    <a href="#karya">Hasil Karya</a>
    <a href="#fotoartikel">Foto & Artikel</a>
    <a href="#sosmed">Media Sosial</a>
    <a href="#kontak">Kontak</a>
    <a href="#testimoni">Testimoni</a>
  </div>

  <main>
    <!-- BERANDA / HERO -->
    <section id="beranda" class="container hero">
      <div>
        <span class="hero-badge">Portfolio Premium</span>
        <h1>Menciptakan Karya Digital yang Bermakna dan Profesional.</h1>
        <p class="hero-desc">Saya BA'II IMAM ZANAWI, desainer & kreator digital dengan pengalaman lebih dari 5 tahun membantu brand bertumbuh melalui desain, fotografi, dan strategi visual.</p>
        <div class="hero-actions">
          <a href="#karya" class="btn btn-primary">Lihat Hasil Karya</a>
          <a href="#kontak" class="btn btn-outline">Hubungi Saya</a>
        </div>
        <div class="social-row">
          <a href="#" aria-label="Instagram">📷</a>
          <a href="#" aria-label="YouTube">▶️</a>
          <a href="#" aria-label="TikTok">🎵</a>
          <a href="#" aria-label="LinkedIn">💼</a>
          <a href="#" aria-label="WhatsApp">💬</a>
        </div>
      </div>
      <div class="hero-img">
        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' fill='%23e2e8f0'/%3E%3Ctext x='25' y='55' font-family='sans-serif' font-size='12' fill='%23555'%3EProfil%3C/text%3E%3C/svg%3E" alt="Foto profil profesional" loading="lazy" />
      </div>
    </section>

    <!-- TENTANG -->
    <section id="tentang" class="container" style="padding:60px 0;">
      <h2 class="section-title">Tentang Kami</h2>
      <p class="section-sub">Visi, misi, dan perjalanan profesional.</p>
      <div style="display:grid; grid-template-columns:1fr 1fr; gap:40px; align-items:center;">
        <div>
          <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='300' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23e2e8f0'/%3E%3Ctext x='35' y='32' font-size='8' fill='%23555'%3ETentang%3C/text%3E%3C/svg%3E" alt="tentang kami" style="width:100%;" loading="lazy">
        </div>
        <div>
          <p style="margin-bottom:24px; color:var(--text-soft);">Berpengalaman dalam membangun identitas visual yang kuat dan strategi konten kreatif untuk berbagai klien.</p>
          <h4>Visi</h4><p style="margin-bottom:12px;">Menjadi mitra kreatif terdepan yang menghasilkan karya berdampak.</p>
          <h4>Misi</h4><p style="margin-bottom:24px;">Memberikan solusi desain yang efektif, estetis, dan profesional.</p>
          <div class="grid-2" style="margin-top:24px;">
            <div class="stat-card"><div class="stat-number">5+</div> Tahun Pengalaman</div>
            <div class="stat-card"><div class="stat-number">100+</div> Proyek</div>
            <div class="stat-card"><div class="stat-number">50+</div> Klien</div>
            <div class="stat-card"><div class="stat-number">20+</div> Penghargaan</div>
          </div>
        </div>
      </div>
    </section>

    <!-- CV -->
    <section id="cv" class="container" style="padding:40px 0;">
      <h2 class="section-title">Curriculum Vitae</h2>
      <div style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap;">
        <p class="section-sub">Pendidikan, pengalaman, dan pencapaian.</p>
        <a href="#" class="btn btn-outline" style="margin-bottom:20px;">⬇ Download CV</a>
      </div>
      <div class="timeline">
        <div class="timeline-item"><strong>Sarjana Desain Komunikasi Visual</strong> — Universitas Indonesia (2015-2019)</div>
        <div class="timeline-item"><strong>Senior Graphic Designer</strong> — Kreativa Studio (2019-2022)</div>
        <div class="timeline-item"><strong>Brand & Content Lead</strong> — DigitalNusantara (2022-Sekarang)</div>
        <div class="timeline-item"><strong>Penghargaan Desain Terbaik</strong> — Indonesian Creative Awards 2023</div>
        <div class="timeline-item"><strong>Sertifikasi UI/UX</strong> — Google (2024)</div>
      </div>
    </section>

    <!-- HASIL KARYA -->
    <section id="karya" class="container" style="padding:60px 0;">
      <h2 class="section-title">Hasil Karya</h2>
      <div class="filter-bar">
        <button class="filter-btn active">Semua</button>
        <button class="filter-btn">Website</button>
        <button class="filter-btn">Desain</button>
        <button class="filter-btn">Fotografi</button>
        <button class="filter-btn">Video</button>
        <button class="filter-btn">Branding</button>
        <button class="filter-btn">Lainnya</button>
      </div>
      <div class="portfolio-grid" id="portfolioGrid">
        <div class="project-card" data-category="website"><div class="project-thumb">Website</div><div class="project-body"><h4>Website Toko Online</h4><p>UI/UX modern</p><button class="btn btn-outline" style="margin-top:10px;">Lihat Detail</button></div></div>
        <div class="project-card" data-category="desain"><div class="project-thumb">Desain</div><div class="project-body"><h4>Poster Event</h4><p>Desain grafis</p></div></div>
        <div class="project-card" data-category="fotografi"><div class="project-thumb">Foto</div><div class="project-body"><h4>Portrait Studio</h4><p>Fotografi profesional</p></div></div>
        <div class="project-card" data-category="branding"><div class="project-thumb">Branding</div><div class="project-body"><h4>Logo Kopi</h4><p>Identitas visual</p></div></div>
        <div class="project-card" data-category="video"><div class="project-thumb">Video</div><div class="project-body"><h4>Company Profile</h4><p>Motion graphics</p></div></div>
      </div>
    </section>

    <!-- FOTO & ARTIKEL -->
    <section id="fotoartikel" class="container" style="padding:40px 0;">
      <h2 class="section-title">Foto & Artikel</h2>
      <div class="tab-buttons">
        <button class="tab-btn active" id="tabFoto">Foto</button>
        <button class="tab-btn" id="tabArtikel">Artikel</button>
      </div>
      <div id="tabFotoContent">
        <div class="masonry">
          <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='200' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23d4d4d4'/%3E%3C/svg%3E" alt="foto1">
          <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='280' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23ccc'/%3E%3C/svg%3E" alt="foto2">
          <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='150' viewBox='0 0 100 60'%3E%3Crect width='100' height='60' fill='%23b0b0b0'/%3E%3C/svg%3E" alt="foto3">
        </div>
      </div>
      <div id="tabArtikelContent" style="display:none;">
        <div style="display:grid; grid-template-columns:repeat(auto-fill,minmax(250px,1fr)); gap:24px;">
          <div class="project-card"><div class="project-thumb">Cover</div><div class="project-body"><h4>Tips Branding 2026</h4><p>12 Feb 2026 • Artikel</p><button class="btn btn-outline">Baca Selengkapnya</button></div></div>
          <div class="project-card"><div class="project-thumb">Cover</div><div class="project-body"><h4>Fotografi Mobile</h4><p>20 Jan 2026 • Tips</p></div></div>
        </div>
      </div>
    </section>

    <!-- MEDIA SOSIAL -->
    <section id="sosmed" class="container" style="padding:60px 0;">
      <h2 class="section-title">Media Sosial</h2>
      <div class="grid-2">
        <div class="stat-card" style="display:flex; align-items:center; gap:16px;">📷 Instagram — @itzzyrr_m4mz <a href="https://www.instagram.com/itzzyrr_m4mz" class="btn btn-outline" style="margin-left:auto;">Kunjungi</a></div>
        <div class="stat-card" style="display:flex; align-items:center; gap:16px;">▶️ YouTube — @baiiimamzanawi <a href="https://youtube.com/@baiiimamzanawi" class="btn btn-outline" style="margin-left:auto;">Kunjungi</a></div>
        <div class="stat-card" style="display:flex; align-items:center; gap:16px;">🎵 TikTok — @immxtyy <a href="https://www.tiktok.com/@immxtyy" class="btn btn-outline" style="margin-left:auto;">Kunjungi</a></div>
        <div class="stat-card" style="display:flex; align-items:center; gap:16px;">💬 WhatsApp — 0882095514943 <a href="https://wa.me/qr/5ET5AHIOKB74D1" class="btn btn-outline" style="margin-left:auto;">Chat</a></div>
      </div>
    </section>

    <!-- KONTAK -->
    <section id="kontak" class="container" style="padding:40px 0;">
      <h2 class="section-title">Kontak</h2>
      <div class="contact-wrap">
        <div>
          <p>📧 baiimamzanawi@gmail.com</p>
          <p>📱 0882095514943</p>
          <p>📍 Ibra Aksesoris</p>
          <p>🕒 06:30 - 15:00 WIB</p>
          <div style="margin-top:20px;">Social media: Instagram, YouTube, TikTok, WhatsApp</div>
        </div>
        <form id="contactForm">
          <input class="form-input" type="text" placeholder="Nama: BA'II IMAM ZANAWI" value="BA'II IMAM ZANAWI" required />
          <input class="form-input" type="email" placeholder="Email: baiimamzanawi@gmail.com" value="baiimamzanawi@gmail.com" required />
          <input class="form-input" type="text" placeholder="Nomor WhatsApp: 088295514943" required />
          <input class="form-input" type="text" placeholder="Subjek" required />
          <textarea class="form-input" rows="4" placeholder="Pesan" required></textarea>
          <button class="btn btn-primary" type="submit">Kirim Pesan</button>
        </form>
      </div>
    </section>

    <!-- TESTIMONI -->
    <section id="testimoni" class="container" style="padding:60px 0;">
      <h2 class="section-title">Testimoni</h2>
      <div class="testimonial-track">
        <div class="testimonial-card">⭐⭐⭐⭐⭐<br/>"Hasil luar biasa, sangat profesional dan cepat."<br/><strong>Rina</strong> — Marketing Manager</div>
        <div class="testimonial-card">⭐⭐⭐⭐⭐<br/>"Desainnya melebihi ekspektasi, recommended!"<br/><strong>Budi</strong> — CEO Startup</div>
        <div class="testimonial-card">⭐⭐⭐⭐⭐<br/>"Kreatif dan komunikatif, project selesai tepat waktu."<br/><strong>Sari</strong> — Brand Owner</div>
        <div class="testimonial-card">⭐⭐⭐⭐⭐<br/>"Sangat membantu dalam rebranding perusahaan."<br/><strong>Andi</strong> — Direktur</div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container" style="display:flex; justify-content:space-between; flex-wrap:wrap; gap:20px;">
      <div>BA'II IMAM ZANAWI<br/>Portfolio pribadi premium</div>
      <div>© 2026 BA'II IMAM ZANAWI. All Rights Reserved.</div>
      <div>Instagram • YouTube • TikTok</div>
    </div>
  </footer>

  <button class="back-to-top" id="backToTop" aria-label="Kembali ke atas">↑</button>

  <script>
    (function() {
      // Loader
      const loader = document.getElementById('loader');
      window.addEventListener('load', () => {
        setTimeout(() => { loader.style.opacity = '0'; setTimeout(() => loader.style.display = 'none', 500); }, 300);
      });

      // Mobile menu
      const hamburger = document.getElementById('hamburgerBtn');
      const mobileMenu = document.getElementById('mobileMenu');
      hamburger.addEventListener('click', () => mobileMenu.classList.toggle('open'));
      document.querySelectorAll('.mobile-menu a').forEach(a => a.addEventListener('click', () => mobileMenu.classList.remove('open')));

      // Smooth scroll & active menu
      const navLinks = document.querySelectorAll('.nav-desktop a');
      const sections = document.querySelectorAll('section[id]');
      window.addEventListener('scroll', () => {
        let current = 'beranda';
        sections.forEach(sec => { if (window.scrollY >= sec.offsetTop - 120) current = sec.id; });
        navLinks.forEach(l => l.classList.remove('active'));
        document.querySelector(`.nav-desktop a[href="#${current}"]`)?.classList.add('active');
      });

      // Back to top
      const backBtn = document.getElementById('backToTop');
      window.addEventListener('scroll', () => { backBtn.classList.toggle('show', window.scrollY > 500); });
      backBtn.addEventListener('click', () => window.scrollTo({ top: 0, behavior: '
