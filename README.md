<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tu Energía Habla · Jeanett Romero</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">

<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --forest: #1c3a28;
    --moss: #2e5c3e;
    --sage: #5a8a6a;
    --mist: #a8c4aa;
    --cream: #f6f0e4;
    --ivory: #fdfaf4;
    --gold: #b8956a;
    --gold-light: #d4b88a;
    --warm-dark: #2a1f14;
    --body-text: #3a3228;
    --muted: #7a6e62;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--ivory);
    color: var(--body-text);
    font-size: 16px;
    line-height: 1.7;
  }

  h1, h2, h3, h4 {
    font-family: 'Cormorant Garamond', serif;
    line-height: 1.2;
  }

  /* ─── NAV ─── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 1rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(253, 250, 244, 0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(184, 149, 106, 0.2);
  }

  .nav-brand {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem;
    font-weight: 500;
    color: var(--forest);
    letter-spacing: 0.04em;
  }

  .nav-cta {
    font-size: 0.85rem;
    font-weight: 500;
    color: var(--forest);
    border: 1.5px solid var(--gold);
    padding: 0.5rem 1.25rem;
    border-radius: 2rem;
    text-decoration: none;
    letter-spacing: 0.05em;
    transition: all 0.3s ease;
  }
  .nav-cta:hover { background: var(--gold); color: var(--ivory); }

  /* ─── HERO ─── */
  .hero {
    min-height: 100vh;
    background: linear-gradient(160deg, var(--forest) 0%, var(--moss) 50%, #3d6e50 100%);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 8rem 2rem 5rem;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.025'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
  }

  .hero-eyebrow {
    font-size: 0.8rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold-light);
    margin-bottom: 1.5rem;
    font-weight: 500;
  }

  .hero-subtitle-top {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(1rem, 2vw, 1.3rem);
    color: var(--mist);
    margin-bottom: 1rem;
    letter-spacing: 0.05em;
  }

  .hero h1 {
    font-size: clamp(3.5rem, 8vw, 7rem);
    font-weight: 300;
    color: var(--ivory);
    margin-bottom: 0.5rem;
    letter-spacing: -0.01em;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--gold-light);
  }

  .hero-tagline {
    font-size: clamp(1rem, 2vw, 1.25rem);
    color: rgba(246,240,228,0.75);
    margin: 1.5rem auto 0;
    max-width: 560px;
    font-weight: 300;
  }

  .hero-instructor {
    margin-top: 2rem;
    font-size: 0.9rem;
    color: var(--mist);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    font-weight: 400;
  }

  .hero-stats {
    display: flex;
    gap: 2.5rem;
    margin-top: 3.5rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .stat {
    text-align: center;
    color: var(--ivory);
  }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.8rem;
    font-weight: 300;
    color: var(--gold-light);
    display: block;
    line-height: 1;
  }
  .stat-label {
    font-size: 0.75rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--mist);
    margin-top: 0.3rem;
    display: block;
  }

  .hero-cta {
    margin-top: 3rem;
    display: inline-block;
    background: var(--gold);
    color: var(--warm-dark);
    padding: 1rem 2.5rem;
    border-radius: 3rem;
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95rem;
    letter-spacing: 0.06em;
    transition: all 0.3s ease;
    border: 2px solid var(--gold);
  }
  .hero-cta:hover {
    background: transparent;
    color: var(--gold-light);
    border-color: var(--gold-light);
  }

  .scroll-hint {
    position: absolute;
    bottom: 2rem;
    left: 50%;
    transform: translateX(-50%);
    color: rgba(246,240,228,0.4);
    font-size: 0.75rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
  }
  .scroll-hint::after {
    content: '';
    width: 1px;
    height: 40px;
    background: linear-gradient(to bottom, rgba(184,149,106,0.6), transparent);
    animation: pulse-line 2s ease-in-out infinite;
  }
  @keyframes pulse-line {
    0%,100%{opacity:0.4;} 50%{opacity:1;}
  }

  /* ─── SECTIONS ─── */
  section { padding: 6rem 2rem; }

  .container {
    max-width: 900px;
    margin: 0 auto;
  }

  .section-label {
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  .section-label::before, .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--gold);
    opacity: 0.3;
  }
  .section-label.left::after { display: none; }
  .section-label.left::before { display: none; }

  .section-title {
    font-size: clamp(2.2rem, 4vw, 3.5rem);
    font-weight: 300;
    color: var(--forest);
    margin-bottom: 1.5rem;
  }
  .section-title em { font-style: italic; color: var(--sage); }

  /* ─── ABOUT ─── */
  .about-section { background: var(--cream); }

  .about-inner {
    display: grid;
    grid-template-columns: 1fr 1.8fr;
    gap: 4rem;
    align-items: center;
  }

  .about-visual {
    aspect-ratio: 3/4;
    background: linear-gradient(145deg, var(--moss), var(--forest));
    border-radius: 40% 60% 55% 45% / 45% 40% 60% 55%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: 4rem;
    color: rgba(246,240,228,0.3);
    font-style: italic;
    position: relative;
    overflow: hidden;
  }
  .about-visual::after {
    content: '✦';
    position: absolute;
    font-size: 8rem;
    opacity: 0.08;
    color: var(--gold-light);
  }

  .about-initials {
    font-family: 'Cormorant Garamond', serif;
    font-size: 3.5rem;
    font-weight: 300;
    color: rgba(246,240,228,0.6);
    z-index: 1;
  }

  .about-text p {
    color: var(--muted);
    font-size: 1.05rem;
    margin-bottom: 1.25rem;
  }
  .about-text p:first-of-type {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.4rem;
    font-style: italic;
    color: var(--body-text);
    line-height: 1.5;
  }

  /* ─── WHAT IS ─── */
  .whatis-section { background: var(--ivory); }

  .quote-block {
    background: linear-gradient(135deg, var(--forest), var(--moss));
    border-radius: 1.5rem;
    padding: 3rem 3.5rem;
    margin: 3rem 0;
    position: relative;
    overflow: hidden;
  }
  .quote-block::before {
    content: '"';
    position: absolute;
    top: -1rem;
    left: 1.5rem;
    font-family: 'Cormorant Garamond', serif;
    font-size: 10rem;
    color: rgba(255,255,255,0.07);
    line-height: 1;
  }
  .quote-block p {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.2rem, 2.5vw, 1.6rem);
    color: var(--ivory);
    font-style: italic;
    line-height: 1.6;
    position: relative;
    z-index: 1;
  }
  .quote-block .quote-note {
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    color: var(--mist);
    font-style: normal;
    margin-top: 1rem;
    font-style: italic;
  }

  /* ─── MODULES ─── */
  .modules-section { background: var(--cream); }

  .modules-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    margin-top: 3rem;
  }

  .module-card {
    border-radius: 1.25rem;
    padding: 2.5rem;
    position: relative;
    overflow: hidden;
  }
  .module-card.basic {
    background: var(--forest);
    color: var(--ivory);
  }
  .module-card.advanced {
    background: var(--warm-dark);
    color: var(--ivory);
  }
  .module-card::before {
    content: attr(data-num);
    position: absolute;
    right: 1.5rem;
    bottom: -1rem;
    font-family: 'Cormorant Garamond', serif;
    font-size: 8rem;
    font-weight: 600;
    opacity: 0.07;
    color: var(--gold-light);
    line-height: 1;
  }

  .module-badge {
    display: inline-block;
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold-light);
    border: 1px solid rgba(184,149,106,0.4);
    padding: 0.3rem 0.8rem;
    border-radius: 2rem;
    margin-bottom: 1.5rem;
  }

  .module-card h3 {
    font-size: 1.8rem;
    font-weight: 300;
    margin-bottom: 0.5rem;
    color: var(--ivory);
  }

  .module-card .module-sub {
    font-size: 0.85rem;
    color: var(--mist);
    margin-bottom: 1.5rem;
  }

  .module-features {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
  }
  .module-features li {
    font-size: 0.9rem;
    color: rgba(246,240,228,0.8);
    display: flex;
    align-items: flex-start;
    gap: 0.6rem;
  }
  .module-features li::before {
    content: '◆';
    color: var(--gold);
    font-size: 0.5rem;
    margin-top: 0.55rem;
    flex-shrink: 0;
  }

  /* ─── SESSION MAP ─── */
  .sessions-section { background: var(--ivory); }

  .sessions-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.25rem;
    margin-top: 3rem;
  }

  .session-card {
    border: 1px solid rgba(90,138,106,0.2);
    border-radius: 1rem;
    padding: 1.75rem 2rem;
    background: var(--ivory);
    transition: all 0.3s ease;
    position: relative;
  }
  .session-card:hover {
    border-color: var(--sage);
    background: var(--cream);
    transform: translateY(-2px);
  }

  .session-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.8rem;
    letter-spacing: 0.15em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 0.5rem;
  }

  .session-card h4 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem;
    font-weight: 500;
    color: var(--forest);
    margin-bottom: 0.6rem;
  }

  .session-card p {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.6;
  }

  .session-module-tag {
    position: absolute;
    top: 1rem;
    right: 1rem;
    font-size: 0.65rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 0.2rem 0.6rem;
    border-radius: 2rem;
  }
  .tag-basic {
    background: rgba(44,92,62,0.1);
    color: var(--moss);
  }
  .tag-advanced {
    background: rgba(184,149,106,0.15);
    color: var(--gold);
  }

  /* ─── OUTCOMES ─── */
  .outcomes-section { background: var(--cream); }

  .outcomes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.25rem;
    margin-top: 2.5rem;
  }

  .outcome-item {
    display: flex;
    align-items: flex-start;
    gap: 1rem;
    padding: 1.25rem 1.5rem;
    background: var(--ivory);
    border-radius: 1rem;
    border-left: 3px solid var(--sage);
  }

  .outcome-icon {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: var(--sage);
    flex-shrink: 0;
    margin-top: 0.55rem;
  }

  .outcome-item p {
    font-size: 0.92rem;
    color: var(--body-text);
    line-height: 1.5;
  }

  .outcome-quote {
    text-align: center;
    margin-top: 3rem;
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.3rem, 2.5vw, 1.7rem);
    font-style: italic;
    color: var(--forest);
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
    padding: 2rem 0;
    border-top: 1px solid rgba(90,138,106,0.2);
    border-bottom: 1px solid rgba(90,138,106,0.2);
  }

  /* ─── WHY DIFFERENT ─── */
  .why-section { background: var(--forest); }

  .why-section .section-title { color: var(--ivory); }
  .why-section .section-title em { color: var(--gold-light); }

  .why-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
    margin-top: 3rem;
  }

  .why-item {
    padding: 2rem;
    border-radius: 1rem;
    border: 1px solid rgba(255,255,255,0.1);
    background: rgba(255,255,255,0.04);
    transition: all 0.3s ease;
  }
  .why-item:hover {
    background: rgba(255,255,255,0.08);
    border-color: rgba(184,149,106,0.3);
  }

  .why-item h4 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem;
    color: var(--gold-light);
    margin-bottom: 0.75rem;
    font-weight: 400;
  }

  .why-item p {
    font-size: 0.88rem;
    color: rgba(246,240,228,0.65);
    line-height: 1.6;
  }

  /* ─── FOR WHOM ─── */
  .forwhom-section { background: var(--ivory); }

  .forwhom-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2.5rem;
    margin-top: 3rem;
  }

  .forwhom-col h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.6rem;
    color: var(--forest);
    margin-bottom: 1.5rem;
    font-weight: 400;
    padding-bottom: 0.75rem;
    border-bottom: 1px solid rgba(90,138,106,0.2);
  }

  .forwhom-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.9rem;
  }
  .forwhom-list li {
    font-size: 0.92rem;
    color: var(--muted);
    display: flex;
    align-items: flex-start;
    gap: 0.75rem;
    line-height: 1.5;
  }
  .forwhom-list li span.check {
    color: var(--sage);
    font-size: 0.8rem;
    font-weight: 600;
    flex-shrink: 0;
    margin-top: 0.1rem;
  }
  .forwhom-note {
    margin-top: 1.5rem;
    padding: 1rem 1.25rem;
    background: var(--cream);
    border-radius: 0.75rem;
    font-style: italic;
    font-size: 0.88rem;
    color: var(--muted);
  }

  /* ─── INCLUDES ─── */
  .includes-section { background: var(--cream); }

  .includes-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    margin-top: 3rem;
  }

  .includes-card {
    background: var(--ivory);
    border-radius: 1.25rem;
    padding: 2.25rem;
    border: 1px solid rgba(90,138,106,0.15);
  }

  .includes-card.featured {
    background: var(--forest);
    border-color: transparent;
  }

  .includes-card h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem;
    color: var(--forest);
    margin-bottom: 1.5rem;
    font-weight: 400;
  }
  .includes-card.featured h3 { color: var(--gold-light); }

  .includes-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.7rem;
  }
  .includes-list li {
    font-size: 0.88rem;
    color: var(--muted);
    display: flex;
    align-items: flex-start;
    gap: 0.7rem;
    line-height: 1.5;
  }
  .includes-list li::before {
    content: '✓';
    color: var(--sage);
    font-weight: 600;
    flex-shrink: 0;
  }
  .includes-card.featured .includes-list li {
    color: rgba(246,240,228,0.7);
  }
  .includes-card.featured .includes-list li::before {
    color: var(--gold-light);
  }

  /* ─── FORMAT ─── */
  .format-section { background: var(--ivory); }

  .format-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 2.5rem;
  }

  .format-pill {
    display: flex;
    flex-direction: column;
    gap: 0.25rem;
    padding: 1rem 1.5rem;
    background: var(--cream);
    border-radius: 0.75rem;
    border: 1px solid rgba(90,138,106,0.15);
    flex: 1;
    min-width: 150px;
  }

  .pill-label {
    font-size: 0.7rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
  }
  .pill-value {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.15rem;
    color: var(--forest);
    font-weight: 500;
  }

  /* ─── CTA ─── */
  .cta-section {
    background: linear-gradient(145deg, var(--warm-dark) 0%, #1a3020 100%);
    text-align: center;
    padding: 7rem 2rem;
    position: relative;
    overflow: hidden;
  }

  .cta-section::before {
    content: '✦';
    position: absolute;
    font-size: 30rem;
    color: rgba(184,149,106,0.03);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-family: 'Cormorant Garamond', serif;
  }

  .cta-section h2 {
    font-size: clamp(2.5rem, 5vw, 4.5rem);
    font-weight: 300;
    color: var(--ivory);
    margin-bottom: 1rem;
  }
  .cta-section h2 em { color: var(--gold-light); font-style: italic; }

  .cta-section p {
    font-size: 1.05rem;
    color: rgba(246,240,228,0.6);
    max-width: 480px;
    margin: 0 auto 2.5rem;
    font-weight: 300;
  }

  .cta-btn {
    display: inline-flex;
    align-items: center;
    gap: 0.75rem;
    background: var(--gold);
    color: var(--warm-dark);
    padding: 1.1rem 2.75rem;
    border-radius: 3rem;
    text-decoration: none;
    font-weight: 500;
    font-size: 1rem;
    letter-spacing: 0.04em;
    transition: all 0.35s ease;
    border: 2px solid var(--gold);
    position: relative;
    z-index: 1;
  }
  .cta-btn:hover {
    background: transparent;
    color: var(--gold-light);
    border-color: var(--gold-light);
    transform: translateY(-3px);
  }

  .cta-note {
    margin-top: 1.5rem;
    font-size: 0.82rem;
    color: rgba(246,240,228,0.35);
    position: relative;
    z-index: 1;
  }

  /* ─── FOOTER ─── */
  footer {
    background: var(--warm-dark);
    padding: 2rem;
    text-align: center;
    border-top: 1px solid rgba(184,149,106,0.15);
  }
  footer p {
    font-size: 0.82rem;
    color: rgba(246,240,228,0.3);
  }
  footer strong {
    color: rgba(246,240,228,0.5);
    font-weight: 400;
  }

  /* ─── REVEAL ANIMATIONS ─── */
  .reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 700px) {
    .about-inner,
    .modules-grid,
    .sessions-grid,
    .forwhom-grid,
    .includes-grid { grid-template-columns: 1fr; }
    .hero-stats { gap: 1.5rem; }
    nav { padding: 0.75rem 1rem; }
    section { padding: 4rem 1.25rem; }
    .quote-block { padding: 2rem 1.75rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <span class="nav-brand">✦ Tu Energía Habla</span>
  <a href="#contacto" class="nav-cta">Consultar Inscripción</a>
</nav>

<!-- HERO -->
<section class="hero">
  <p class="hero-eyebrow">Exploración Bioenergética con Radiestesia Pendular</p>
  <p class="hero-subtitle-top">Taller Teórico-Práctico Online · 8 Sesiones en Vivo</p>
  <h1>Tu <em>Energía</em><br>Habla</h1>
  <p class="hero-tagline">Aprende a conectar con tu campo energético, limpiar bloqueos y explorar tu alma con un sistema propio de 33 gráficos.</p>
  <p class="hero-instructor">Con Jeanett Romero · Terapeuta Biointegral</p>
  <div class="hero-stats">
    <div class="stat"><span class="stat-num">8</span><span class="stat-label">Sesiones en vivo</span></div>
    <div class="stat"><span class="stat-num">33</span><span class="stat-label">Gráficos propios</span></div>
    <div class="stat"><span class="stat-num">4h</span><span class="stat-label">Por sesión</span></div>
    <div class="stat"><span class="stat-num">6+</span><span class="stat-label">Años de práctica</span></div>
  </div>
  <a href="#contacto" class="hero-cta">Quiero Inscribirme →</a>
  <div class="scroll-hint">Descubre más</div>
</section>

<!-- ABOUT -->
<section class="about-section">
  <div class="container">
    <div class="about-inner">
      <div class="about-visual">
        <span class="about-initials">JR</span>
      </div>
      <div class="about-text">
        <div class="section-label left">Sobre mí</div>
        <h2 class="section-title" style="margin-bottom:1.25rem;">Hola, me alegra<br>que estés <em>aquí</em> 💚</h2>
        <p>Soy Jeanett Romero, terapeuta biointegral con más de 6 años acompañando procesos de autoconocimiento y sanación energética.</p>
        <p>En 2016 tomé un péndulo por primera vez. Lo que empezó como una consulta se convirtió en un camino que transformó completamente mi forma de conectarme conmigo, con mis guías, el alma y la sanación.</p>
        <p>Desde entonces no he parado de aprender, practicar y diseñar herramientas. Y con el tiempo, esos gráficos y ese sistema se fueron convirtiendo en algo propio — en un mapa vivo que hoy quiero compartir contigo.</p>
      </div>
    </div>
  </div>
</section>

<!-- WHAT IS -->
<section class="whatis-section reveal">
  <div class="container">
    <div class="section-label">¿Qué es?</div>
    <h2 class="section-title">Una experiencia<br>vivencial de <em>8 semanas</em></h2>
    <div class="quote-block">
      <p>"Tu Energía Habla" es una experiencia vivencial donde aprenderás a explorar, limpiar y reequilibrar tu campo energético usando un sistema propio de 33 gráficos y el péndulo como herramienta de conexión interior.</p>
      <p class="quote-note">No necesitas experiencia previa. Solo apertura, curiosidad y disposición para encontrarte contigo mismo/a.</p>
    </div>
  </div>
</section>

<!-- MODULES -->
<section class="modules-section reveal">
  <div class="container">
    <div class="section-label">El programa</div>
    <h2 class="section-title">Dos <em>módulos</em>,<br>un sistema completo</h2>
    <div class="modules-grid">
      <div class="module-card basic" data-num="13">
        <span class="module-badge">🌑 Módulo Básico</span>
        <h3>El Campo<br>Emocional</h3>
        <p class="module-sub">Sesiones 1 a 4 · 4 horas cada una</p>
        <ul class="module-features">
          <li>4 sesiones en vivo de 4 horas</li>
          <li>13 gráficos — el campo emocional completo</li>
          <li>Calibración, neutralidad y protocolo personal</li>
          <li>Primera sesión completa al finalizar</li>
        </ul>
      </div>
      <div class="module-card advanced" data-num="20">
        <span class="module-badge">🌟 Módulo Avanzado</span>
        <h3>Las Raíces<br>del Alma</h3>
        <p class="module-sub">Sesiones 5 a 8 · 4 horas cada una</p>
        <ul class="module-features">
          <li>4 sesiones adicionales en vivo</li>
          <li>20 gráficos nuevos — raíces del alma</li>
          <li>Programas, votos, arquetipos, sombras</li>
          <li>Sistema completo de 33 gráficos integrado</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- SESSIONS -->
<section class="sessions-section reveal">
  <div class="container">
    <div class="section-label">Recorrido sesión por sesión</div>
    <h2 class="section-title">8 encuentros que<br><em>transforman</em></h2>
    <div class="sessions-grid">
      <div class="session-card">
        <span class="session-module-tag tag-basic">Básico</span>
        <p class="session-num">Sesión 1</p>
        <h4>El Umbral</h4>
        <p>Qué somos energéticamente, de dónde viene esta herramienta y cómo hablar con el péndulo. Primer contacto y calibración personal.</p>
      </div>
      <div class="session-card">
        <span class="session-module-tag tag-basic">Básico</span>
        <p class="session-num">Sesión 2</p>
        <h4>El Canal</h4>
        <p>Presencia, neutralidad y el arte de preguntar. Lo que ningún sistema puede enseñarte desde afuera: confiar en tu propio campo.</p>
      </div>
      <div class="session-card">
        <span class="session-module-tag tag-basic">Básico</span>
        <p class="session-num">Sesión 3</p>
        <h4>El Mapa</h4>
        <p>Las capas del ser y el campo emocional completo: emociones activas, miedos, pensamientos limitantes y heridas que condicionan el presente.</p>
      </div>
      <div class="session-card">
        <span class="session-module-tag tag-basic">Básico</span>
        <p class="session-num">Sesión 4</p>
        <h4>El Sistema</h4>
        <p>Los recursos del alma, las energías de activación y el cierre en equilibrio. Primera sesión completa de principio a fin, solo/a.</p>
      </div>
      <div class="session-card">
        <span class="session-module-tag tag-advanced">Avanzado</span>
        <p class="session-num">Sesión 5</p>
        <h4>Las Estructuras del Alma</h4>
        <p>El mapa completo de los cuerpos sutiles, la asistencia espiritual, las virtudes que el alma vino a desarrollar y sus aprendizajes.</p>
      </div>
      <div class="session-card">
        <span class="session-module-tag tag-advanced">Avanzado</span>
        <p class="session-num">Sesión 6</p>
        <h4>Las Raíces</h4>
        <p>Los programas que se arrastran de vida en vida, los compromisos olvidados, el propósito del alma y los personajes internos que nos conducen.</p>
      </div>
      <div class="session-card">
        <span class="session-module-tag tag-advanced">Avanzado</span>
        <p class="session-num">Sesión 7</p>
        <h4>Las Sombras</h4>
        <p>Las energías que interfieren, los bloqueos en capas profundas del campo y los programas de los cuerpos superiores. La sesión que más libera.</p>
      </div>
      <div class="session-card">
        <span class="session-module-tag tag-advanced">Avanzado</span>
        <p class="session-num">Sesión 8</p>
        <h4>El Sistema Completo</h4>
        <p>Los gráficos que sanan y armonizan. Primera sesión con el sistema entero de 33 gráficos integrado. Clausura y protocolo de vida.</p>
      </div>
    </div>
  </div>
</section>

<!-- OUTCOMES -->
<section class="outcomes-section reveal">
  <div class="container">
    <div class="section-label">Al finalizar</div>
    <h2 class="section-title">Lo que vas a poder<br><em>hacer</em></h2>
    <div class="outcomes-grid">
      <div class="outcome-item"><div class="outcome-icon"></div><p>Usar el péndulo con confianza y neutralidad, sin dudas sobre si "lo estás haciendo bien"</p></div>
      <div class="outcome-item"><div class="outcome-icon"></div><p>Navegar el sistema de 33 gráficos para investigar tu campo con claridad y profundidad</p></div>
      <div class="outcome-item"><div class="outcome-icon"></div><p>Identificar heridas emocionales, programas limitantes y patrones repetitivos en tu campo</p></div>
      <div class="outcome-item"><div class="outcome-icon"></div><p>Trabajar con miedos, creencias, votos de vidas pasadas y energías que te estancan</p></div>
      <div class="outcome-item"><div class="outcome-icon"></div><p>Entender tu estructura energética: cuerpos sutiles, arquetipos y programas del alma</p></div>
      <div class="outcome-item"><div class="outcome-icon"></div><p>Hacer limpiezas completas y cerrar sesiones con armonización real</p></div>
      <div class="outcome-item"><div class="outcome-icon"></div><p>Tener un sistema de autoexploración continua que puedes usar solo/a cuando quieras</p></div>
      <div class="outcome-item"><div class="outcome-icon"></div><p>Sentar las bases para acompañar a otros en su propio proceso energético</p></div>
    </div>
    <p class="outcome-quote">"Aprenderás no solo a usar un péndulo... aprenderás a escuchar a tu alma."</p>
  </div>
</section>

<!-- WHY DIFFERENT -->
<section class="why-section reveal">
  <div class="container">
    <div class="section-label" style="color:var(--gold);"><span></span>Por qué es diferente<span></span></div>
    <h2 class="section-title">Un sistema que<br><em>te queda</em> para siempre</h2>
    <div class="why-grid">
      <div class="why-item">
        <h4>Sistema propio de 33 gráficos</h4>
        <p>Creados y perfeccionados en práctica real durante más de 6 años de trabajo continuo.</p>
      </div>
      <div class="why-item">
        <h4>Aprendizaje con corazón</h4>
        <p>No es solo teoría: es conocimiento vivido, practicado y comprobado en sesiones reales.</p>
      </div>
      <div class="why-item">
        <h4>Gráficos intuitivos</h4>
        <p>Diseñados para que cualquier persona, sin experiencia previa, pueda usarlos con confianza.</p>
      </div>
      <div class="why-item">
        <h4>Autoexploración primero</h4>
        <p>Trabajas contigo antes de aprender a acompañar a otros. Lo interno siempre primero.</p>
      </div>
      <div class="why-item">
        <h4>Protocolo personal completo</h4>
        <p>Al terminar tienes un sistema que puedes usar toda la vida, sin depender de nadie más.</p>
      </div>
      <div class="why-item">
        <h4>Acompañamiento real</h4>
        <p>No eres un número. Tienes soporte durante todo el proceso por WhatsApp o Telegram.</p>
      </div>
    </div>
  </div>
</section>

<!-- FOR WHOM -->
<section class="forwhom-section reveal">
  <div class="container">
    <div class="section-label">¿Para quién es?</div>
    <h2 class="section-title">Este taller es<br>para <em>ti</em> si...</h2>
    <div class="forwhom-grid">
      <div class="forwhom-col">
        <h3>Este programa es para ti</h3>
        <ul class="forwhom-list">
          <li><span class="check">💚</span> Sientes que hay algo más en ti que quiere sanar</li>
          <li><span class="check">💚</span> Tienes patrones que se repiten y no entiendes por qué</li>
          <li><span class="check">💚</span> Quieres herramientas reales para limpiar bloqueos propios</li>
          <li><span class="check">💚</span> Estás listo/a para conectar con tu sabiduría interior</li>
          <li><span class="check">💚</span> Sueñas con poder acompañar a otros desde un lugar auténtico</li>
          <li><span class="check">💚</span> Eres terapeuta y quieres ampliar tus herramientas</li>
        </ul>
      </div>
      <div class="forwhom-col">
        <h3>No es necesario que tengas...</h3>
        <ul class="forwhom-list">
          <li><span class="check">✓</span> Experiencia previa con péndulo o radiestesia</li>
          <li><span class="check">✓</span> Conocimientos de energía o metafísica</li>
          <li><span class="check">✓</span> Haber tomado ningún curso antes</li>
          <li><span class="check">✓</span> Ser terapeuta o trabajar en el área de salud</li>
        </ul>
        <div class="forwhom-note">
          Solo necesitas apertura y disposición a encontrarte.
        </div>
      </div>
    </div>
  </div>
</section>

<!-- INCLUDES -->
<section class="includes-section reveal">
  <div class="container">
    <div class="section-label">¿Qué incluye?</div>
    <h2 class="section-title">Todo lo que<br><em>recibes</em></h2>
    <div class="includes-grid">
      <div class="includes-card">
        <h3>🌑 Módulo Básico</h3>
        <ul class="includes-list">
          <li>4 sesiones en vivo de 4 horas</li>
          <li>Acceso a grabación de cada sesión</li>
          <li>Manual del alumno — Módulo Básico</li>
          <li>Cuaderno de trabajo digital</li>
          <li>Glosario completo del sistema</li>
          <li>Gráficos del sistema en formato digital</li>
          <li>Protocolo personal de referencia</li>
          <li>Acompañamiento por WhatsApp durante el módulo</li>
          <li>Certificado digital al completar</li>
          <li>Encuentros mensuales de seguimiento (1 × 2 meses)</li>
        </ul>
      </div>
      <div class="includes-card featured">
        <h3>⭐ Curso Completo</h3>
        <ul class="includes-list">
          <li>Todo lo del Módulo Básico</li>
          <li>4 sesiones adicionales en vivo</li>
          <li>Manual del alumno — Módulo Avanzado</li>
          <li>Cuaderno de trabajo completo (8 sesiones)</li>
          <li>Sistema completo de 33 gráficos</li>
          <li>Protocolo de los 33 gráficos integrado</li>
          <li>Acompañamiento por WhatsApp todo el programa</li>
          <li>Certificado digital del sistema completo</li>
          <li>Encuentros mensuales de seguimiento (1 × 2 meses)</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- FORMAT -->
<section class="format-section reveal">
  <div class="container">
    <div class="section-label">Formato del programa</div>
    <h2 class="section-title">Todo lo que necesitas<br>saber sobre la <em>logística</em></h2>
    <div class="format-pills">
      <div class="format-pill">
        <span class="pill-label">Modalidad</span>
        <span class="pill-value">Online en vivo</span>
      </div>
      <div class="format-pill">
        <span class="pill-label">Plataforma</span>
        <span class="pill-value">Zoom</span>
      </div>
      <div class="format-pill">
        <span class="pill-label">Duración</span>
        <span class="pill-value">8 semanas</span>
      </div>
      <div class="format-pill">
        <span class="pill-label">Por sesión</span>
        <span class="pill-value">4 horas</span>
      </div>
      <div class="format-pill">
        <span class="pill-label">Horario</span>
        <span class="pill-value">9AM – 1PM VE</span>
      </div>
      <div class="format-pill">
        <span class="pill-label">Grabaciones</span>
        <span class="pill-value">30 días de acceso</span>
      </div>
      <div class="format-pill">
        <span class="pill-label">Soporte</span>
        <span class="pill-value">WhatsApp · Telegram</span>
      </div>
    </div>
  </div>
</section>

<!-- CTA -->
<section class="cta-section" id="contacto">
  <h2>¿Lista/o para escuchar<br>a tu <em>alma</em>?</h2>
  <p>Escríbeme y con gusto te comparto todos los detalles, opciones de módulos y formas de pago.</p>
  <!-- 🔧 REEMPLAZA el número de WhatsApp abajo: -->
  <a href="https://wa.me/TUNUMERODEWHATSAPP?text=Hola%20Jeanett%2C%20me%20interesa%20el%20taller%20Tu%20Energ%C3%ADa%20Habla%20%F0%9F%8C%BF" class="cta-btn" target="_blank" rel="noopener">
    <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
    Consultar por WhatsApp
  </a>
  <p class="cta-note">También puedes preguntar por correo electrónico o redes sociales</p>
</section>

<!-- FOOTER -->
<footer>
  <p><strong>Tu Energía Habla</strong> · Jeanett Romero, Terapeuta Biointegral · Taller Online</p>
  <p style="margin-top:0.5rem;">Hecho con amor y práctica real ✦</p>
</footer>

<script>
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.1 });
  reveals.forEach(r => observer.observe(r));
</script>
</body>
</html>
