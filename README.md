<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Studio Lumière — Templates Canva</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --ink:    #0f0f0f;
  --paper:  #f8f5f0;
  --sand:   #e8e0d5;
  --gold:   #b8960c;
  --gold-l: #d4af37;
  --muted:  #7a7268;
  --white:  #ffffff;
}

html { scroll-behavior: smooth; }

body {
  background: var(--paper);
  color: var(--ink);
  font-family: 'Inter', sans-serif;
  font-size: 15px;
  line-height: 1.6;
  overflow-x: hidden;
}

/* ── NAV ── */
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 60px;
  background: rgba(248,245,240,0.92);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(0,0,0,0.06);
}

.nav-logo {
  font-family: 'Cormorant Garamond', serif;
  font-size: 20px;
  font-weight: 600;
  letter-spacing: 0.04em;
  color: var(--ink);
  text-decoration: none;
}

.nav-logo span { color: var(--gold); }

.nav-links {
  display: flex;
  gap: 36px;
  list-style: none;
}

.nav-links a {
  font-size: 12px;
  font-weight: 500;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
  text-decoration: none;
  transition: color .2s;
}
.nav-links a:hover { color: var(--ink); }

.nav-cta {
  background: var(--ink);
  color: var(--white) !important;
  padding: 10px 22px;
  border-radius: 2px;
  transition: background .2s !important;
}
.nav-cta:hover { background: var(--gold) !important; color: var(--white) !important; }

/* ── HERO ── */
.hero {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  padding: 120px 60px 80px;
  gap: 80px;
  position: relative;
  overflow: hidden;
}

.hero::after {
  content: '';
  position: absolute;
  right: -100px; top: 50%;
  transform: translateY(-50%);
  width: 500px; height: 500px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(184,150,12,0.08) 0%, transparent 70%);
  pointer-events: none;
}

.hero-text { position: relative; z-index: 1; }

.hero-eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 28px;
}

.hero-eyebrow::before {
  content: '';
  display: block;
  width: 32px; height: 1px;
  background: var(--gold);
}

h1 {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(52px, 6vw, 80px);
  font-weight: 300;
  line-height: 1.05;
  color: var(--ink);
  margin-bottom: 28px;
}

h1 em {
  font-style: italic;
  font-weight: 300;
  color: var(--gold);
}

.hero-sub {
  font-size: 16px;
  font-weight: 300;
  color: var(--muted);
  max-width: 380px;
  line-height: 1.8;
  margin-bottom: 48px;
}

.hero-actions {
  display: flex;
  align-items: center;
  gap: 24px;
}

.btn-primary {
  background: var(--ink);
  color: var(--white);
  padding: 14px 32px;
  font-size: 12px;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  text-decoration: none;
  border-radius: 2px;
  transition: background .2s;
}
.btn-primary:hover { background: var(--gold); }

.btn-ghost {
  font-size: 12px;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--muted);
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 8px;
  transition: color .2s;
}
.btn-ghost:hover { color: var(--ink); }
.btn-ghost::after { content: '→'; }

.hero-stats {
  display: flex;
  gap: 40px;
  margin-top: 60px;
  padding-top: 40px;
  border-top: 1px solid var(--sand);
}

.stat-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 36px;
  font-weight: 300;
  color: var(--ink);
  line-height: 1;
}

.stat-label {
  font-size: 11px;
  color: var(--muted);
  margin-top: 4px;
  letter-spacing: 0.05em;
}

/* ── HERO PREVIEW CARDS ── */
.hero-preview {
  position: relative;
  height: 560px;
  z-index: 1;
}

.preview-card {
  position: absolute;
  border-radius: 4px;
  overflow: hidden;
  box-shadow: 0 20px 60px rgba(0,0,0,0.15);
  transition: transform .3s;
}

.preview-card:hover { transform: scale(1.02); }

.pc-main {
  width: 260px;
  height: 360px;
  top: 40px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 3;
}

.pc-left {
  width: 180px;
  height: 250px;
  top: 120px;
  left: 0;
  z-index: 2;
  transform: rotate(-4deg);
}

.pc-right {
  width: 180px;
  height: 250px;
  top: 140px;
  right: 0;
  z-index: 2;
  transform: rotate(4deg);
}

/* Inline SVG mini-templates */
.pc-main svg, .pc-left svg, .pc-right svg {
  width: 100%;
  height: 100%;
}

/* ── SECTION SHARED ── */
section { padding: 100px 60px; }

.section-label {
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 16px;
}
.section-label::before {
  content: '';
  width: 28px; height: 1px;
  background: var(--gold);
}

h2 {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(36px, 4vw, 52px);
  font-weight: 300;
  line-height: 1.1;
  margin-bottom: 16px;
}

h2 em { font-style: italic; color: var(--gold); }

.section-intro {
  font-size: 15px;
  color: var(--muted);
  max-width: 480px;
  line-height: 1.8;
  margin-bottom: 64px;
}

/* ── CATEGORIES ── */
#templates { background: var(--white); }

.categories-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 64px;
}

.filter-tabs {
  display: flex;
  gap: 4px;
  background: var(--sand);
  padding: 4px;
  border-radius: 4px;
}

.filter-tab {
  padding: 8px 18px;
  font-size: 12px;
  font-weight: 500;
  color: var(--muted);
  background: none;
  border: none;
  border-radius: 2px;
  cursor: pointer;
  transition: all .2s;
}

.filter-tab.active {
  background: var(--white);
  color: var(--ink);
  box-shadow: 0 1px 4px rgba(0,0,0,0.1);
}

/* ── TEMPLATE GRID ── */
.templates-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

.template-card {
  cursor: pointer;
  transition: transform .2s;
}
.template-card:hover { transform: translateY(-4px); }

.template-thumb {
  width: 100%;
  aspect-ratio: 3/4;
  border-radius: 4px;
  overflow: hidden;
  margin-bottom: 16px;
  position: relative;
}

.template-thumb svg {
  width: 100%;
  height: 100%;
}

.template-overlay {
  position: absolute;
  inset: 0;
  background: rgba(15,15,15,0.0);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background .2s;
}

.template-card:hover .template-overlay {
  background: rgba(15,15,15,0.45);
}

.template-overlay-btn {
  background: var(--white);
  color: var(--ink);
  padding: 10px 22px;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  border-radius: 2px;
  opacity: 0;
  transform: translateY(6px);
  transition: opacity .2s, transform .2s;
}

.template-card:hover .template-overlay-btn {
  opacity: 1;
  transform: translateY(0);
}

.template-name {
  font-size: 14px;
  font-weight: 500;
  color: var(--ink);
  margin-bottom: 4px;
}

.template-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.template-cat {
  font-size: 11px;
  color: var(--muted);
  letter-spacing: 0.05em;
}

.template-price {
  font-family: 'Cormorant Garamond', serif;
  font-size: 18px;
  font-weight: 600;
  color: var(--gold);
}

/* ── PROCESS ── */
#process { background: var(--paper); }

.process-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 40px;
  margin-top: 64px;
}

.process-step {
  padding: 32px;
  background: var(--white);
  border-radius: 4px;
  border: 1px solid var(--sand);
  position: relative;
}

.step-num {
  font-family: 'Cormorant Garamond', serif;
  font-size: 64px;
  font-weight: 300;
  color: var(--sand);
  line-height: 1;
  margin-bottom: 16px;
}

.step-title {
  font-size: 15px;
  font-weight: 600;
  color: var(--ink);
  margin-bottom: 8px;
}

.step-desc {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.7;
}

/* ── TESTIMONIALS ── */
#avis { background: var(--ink); }

#avis .section-label { color: var(--gold-l); }
#avis .section-label::before { background: var(--gold-l); }
#avis h2 { color: var(--white); }
#avis h2 em { color: var(--gold-l); }

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.testimonial {
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 4px;
  padding: 36px;
}

.stars {
  color: var(--gold-l);
  font-size: 14px;
  margin-bottom: 20px;
  letter-spacing: 2px;
}

.testimonial-text {
  font-family: 'Cormorant Garamond', serif;
  font-size: 18px;
  font-style: italic;
  font-weight: 300;
  color: rgba(255,255,255,0.85);
  line-height: 1.7;
  margin-bottom: 28px;
}

.testimonial-author {
  display: flex;
  align-items: center;
  gap: 12px;
}

.author-avatar {
  width: 40px; height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
  font-weight: 600;
  color: var(--white);
  flex-shrink: 0;
}

.author-name {
  font-size: 14px;
  font-weight: 500;
  color: var(--white);
}

.author-role {
  font-size: 12px;
  color: rgba(255,255,255,0.4);
}

/* ── CTA BANNER ── */
.cta-banner {
  background: linear-gradient(135deg, var(--gold) 0%, #8B6914 100%);
  padding: 80px 60px;
  text-align: center;
}

.cta-banner h2 {
  color: var(--white);
  margin-bottom: 16px;
}
.cta-banner h2 em { color: rgba(255,255,255,0.7); }

.cta-banner p {
  color: rgba(255,255,255,0.8);
  margin-bottom: 40px;
  font-size: 16px;
}

.btn-white {
  background: var(--white);
  color: var(--gold);
  padding: 16px 40px;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  text-decoration: none;
  border-radius: 2px;
  display: inline-block;
  transition: transform .2s;
}
.btn-white:hover { transform: translateY(-2px); }

/* ── FOOTER ── */
footer {
  background: #0a0a0a;
  color: rgba(255,255,255,0.4);
  padding: 48px 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 12px;
}

.footer-logo {
  font-family: 'Cormorant Garamond', serif;
  font-size: 18px;
  color: rgba(255,255,255,0.7);
}

.footer-logo span { color: var(--gold-l); }

/* ── SCROLL ANIMATIONS ── */
.fade-up {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity .6s ease, transform .6s ease;
}
.fade-up.visible {
  opacity: 1;
  transform: translateY(0);
}

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
  nav { padding: 16px 24px; }
  .nav-links { display: none; }
  .hero { grid-template-columns: 1fr; padding: 100px 24px 60px; }
  .hero-preview { height: 300px; }
  section { padding: 60px 24px; }
  .templates-grid { grid-template-columns: repeat(2, 1fr); gap: 20px; }
  .process-grid { grid-template-columns: repeat(2, 1fr); }
  .testimonials-grid { grid-template-columns: 1fr; }
  .categories-header { flex-direction: column; align-items: flex-start; gap: 20px; }
  footer { flex-direction: column; gap: 16px; text-align: center; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Studio <span>Lumière</span></a>
  <ul class="nav-links">
    <li><a href="#templates">Templates</a></li>
    <li><a href="#process">Comment ça marche</a></li>
    <li><a href="#avis">Avis</a></li>
    <li><a href="#contact" class="nav-cta">Voir la boutique</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-text">
    <div class="hero-eyebrow">Templates Canva Premium</div>
    <h1>Des designs qui<br>font <em>sentir</em><br>quelque chose.</h1>
    <p class="hero-sub">Cartes, invitations, affiches — chaque template est conçu à la main avec une intention précise. Pas de lorem ipsum, pas de remplissage.</p>
    <div class="hero-actions">
      <a href="#templates" class="btn-primary">Voir les templates</a>
      <a href="#process" class="btn-ghost">Comment ça marche</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">84</div>
        <div class="stat-label">Templates disponibles</div>
      </div>
      <div>
        <div class="stat-num">4.9★</div>
        <div class="stat-label">Note moyenne</div>
      </div>
      <div>
        <div class="stat-num">2 k+</div>
        <div class="stat-label">Clients satisfaits</div>
      </div>
    </div>
  </div>

  <!-- Hero preview cards -->
  <div class="hero-preview">

    <!-- Main card: Birthday -->
    <div class="preview-card pc-main">
      <svg viewBox="0 0 260 360" xmlns="http://www.w3.org/2000/svg">
        <rect width="260" height="360" fill="#fdf6ec"/>
        <!-- dots -->
        <circle cx="20" cy="30" r="3" fill="#e8b86d" opacity=".2"/>
        <circle cx="240" cy="60" r="2" fill="#c0392b" opacity=".2"/>
        <circle cx="30" cy="320" r="4" fill="#2c7873" opacity=".15"/>
        <!-- top band -->
        <rect x="0" y="0" width="87" height="7" fill="#c0392b"/>
        <rect x="87" y="0" width="86" height="7" fill="#e8b86d"/>
        <rect x="173" y="0" width="87" height="7" fill="#2c7873"/>
        <!-- text -->
        <text x="26" y="42" font-family="Georgia,serif" font-size="9" fill="#c0392b" letter-spacing="2">UNE JOURNÉE SPÉCIALE</text>
        <text x="26" y="72" font-family="Georgia,serif" font-size="30" font-weight="bold" fill="#1a1007">Joyeux</text>
        <text x="26" y="104" font-family="Georgia,serif" font-size="30" font-style="italic" fill="#c0392b">Anniversaire</text>
        <!-- divider -->
        <line x1="26" y1="118" x2="108" y2="118" stroke="#1a1007" stroke-opacity=".15" stroke-width=".5"/>
        <text x="128" y="122" font-family="Georgia,serif" font-size="7" fill="#1a1007" opacity=".3" text-anchor="middle">✦</text>
        <line x1="148" y1="118" x2="234" y2="118" stroke="#1a1007" stroke-opacity=".15" stroke-width=".5"/>
        <!-- cake -->
        <ellipse cx="130" cy="236" rx="50" ry="7" fill="#e0d0b8"/>
        <rect x="80" y="198" width="100" height="34" rx="4" fill="#e8b86d"/>
        <rect x="80" y="198" width="100" height="9" rx="4" fill="#d4a247"/>
        <rect x="96" y="174" width="68" height="28" rx="4" fill="#c0392b"/>
        <rect x="96" y="174" width="68" height="8" rx="4" fill="#a93226"/>
        <!-- candles -->
        <rect x="114" y="156" width="5" height="18" rx="1.5" fill="#2c7873"/>
        <rect x="127" y="152" width="5" height="22" rx="1.5" fill="#e8b86d"/>
        <rect x="140" y="156" width="5" height="18" rx="1.5" fill="#c0392b"/>
        <!-- flames -->
        <ellipse cx="116.5" cy="153" rx="3" ry="5" fill="#f39c12" opacity=".9"/>
        <ellipse cx="129.5" cy="149" rx="3" ry="5" fill="#f39c12" opacity=".9"/>
        <ellipse cx="142.5" cy="153" rx="3" ry="5" fill="#f39c12" opacity=".9"/>
        <!-- message -->
        <text x="130" y="268" font-family="Georgia,serif" font-size="8" font-style="italic" fill="#3a2e1e" text-anchor="middle">"Que cette nouvelle année t'apporte</text>
        <text x="130" y="280" font-family="Georgia,serif" font-size="8" font-style="italic" fill="#3a2e1e" text-anchor="middle">tout ce que tu mérites."</text>
        <!-- name -->
        <text x="26" y="310" font-family="sans-serif" font-size="7" fill="#aaa" letter-spacing="1.5">POUR</text>
        <text x="26" y="328" font-family="Georgia,serif" font-size="20" font-weight="bold" fill="#1a1007">Sophie</text>
        <!-- badge -->
        <circle cx="222" cy="320" r="22" fill="#c0392b"/>
        <text x="222" y="325" font-family="Georgia,serif" font-size="16" font-weight="bold" fill="white" text-anchor="middle">30</text>
        <!-- bottom band -->
        <rect x="0" y="353" width="87" height="7" fill="#2c7873"/>
        <rect x="87" y="353" width="86" height="7" fill="#e8b86d"/>
        <rect x="173" y="353" width="87" height="7" fill="#c0392b"/>
      </svg>
    </div>

    <!-- Left card: Wedding -->
    <div class="preview-card pc-left">
      <svg viewBox="0 0 180 250" xmlns="http://www.w3.org/2000/svg">
        <rect width="180" height="250" fill="#1a1a2a"/>
        <rect x="12" y="12" width="156" height="226" fill="none" stroke="#d4af37" stroke-width=".8" opacity=".5"/>
        <rect x="18" y="18" width="144" height="214" fill="none" stroke="#d4af37" stroke-width=".3" opacity=".3"/>
        <text x="90" y="60" font-family="Georgia,serif" font-size="9" fill="#d4af37" opacity=".7" text-anchor="middle" letter-spacing="3">MARIAGE</text>
        <text x="90" y="95" font-family="Georgia,serif" font-size="22" font-style="italic" fill="white" text-anchor="middle">Camille</text>
        <text x="90" y="112" font-family="Georgia,serif" font-size="11" fill="#d4af37" text-anchor="middle">&amp;</text>
        <text x="90" y="133" font-family="Georgia,serif" font-size="22" font-style="italic" fill="white" text-anchor="middle">Antoine</text>
        <line x1="50" y1="148" x2="130" y2="148" stroke="#d4af37" stroke-width=".5" opacity=".5"/>
        <text x="90" y="168" font-family="sans-serif" font-size="8" fill="#d4af37" opacity=".7" text-anchor="middle" letter-spacing="1">14 SEPTEMBRE 2026</text>
        <text x="90" y="184" font-family="sans-serif" font-size="7" fill="white" opacity=".4" text-anchor="middle">Château de Vaux-le-Vicomte</text>
        <!-- ring -->
        <circle cx="90" cy="215" r="14" fill="none" stroke="#d4af37" stroke-width="1.5" opacity=".6"/>
        <circle cx="90" cy="215" r="10" fill="none" stroke="#d4af37" stroke-width=".5" opacity=".3"/>
      </svg>
    </div>

    <!-- Right card: Business card -->
    <div class="preview-card pc-right">
      <svg viewBox="0 0 180 250" xmlns="http://www.w3.org/2000/svg">
        <rect width="180" height="250" fill="#f0ede8"/>
        <!-- geometric accent -->
        <rect x="0" y="0" width="6" height="250" fill="#0f0f0f"/>
        <rect x="0" y="0" width="180" height="6" fill="#0f0f0f"/>
        <!-- grid dots -->
        <circle cx="40" cy="40" r="1.5" fill="#0f0f0f" opacity=".15"/>
        <circle cx="80" cy="40" r="1.5" fill="#0f0f0f" opacity=".15"/>
        <circle cx="120" cy="40" r="1.5" fill="#0f0f0f" opacity=".15"/>
        <circle cx="160" cy="40" r="1.5" fill="#0f0f0f" opacity=".15"/>
        <circle cx="40" cy="80" r="1.5" fill="#0f0f0f" opacity=".15"/>
        <circle cx="80" cy="80" r="1.5" fill="#0f0f0f" opacity=".15"/>
        <circle cx="40" cy="120" r="1.5" fill="#0f0f0f" opacity=".15"/>
        <!-- content -->
        <text x="26" y="90" font-family="Georgia,serif" font-size="10" fill="#0f0f0f" opacity=".4" letter-spacing="2">STUDIO</text>
        <text x="26" y="118" font-family="Georgia,serif" font-size="24" font-weight="bold" fill="#0f0f0f">Léa</text>
        <text x="26" y="140" font-family="Georgia,serif" font-size="24" font-weight="bold" fill="#0f0f0f">Martin</text>
        <line x1="26" y1="155" x2="80" y2="155" stroke="#0f0f0f" stroke-width=".8"/>
        <text x="26" y="172" font-family="sans-serif" font-size="7.5" fill="#555" letter-spacing=".5">Photographe &amp; Directrice créative</text>
        <text x="26" y="210" font-family="sans-serif" font-size="7" fill="#888">lea@studio-lumiere.fr</text>
        <text x="26" y="225" font-family="sans-serif" font-size="7" fill="#888">+33 6 12 34 56 78</text>
        <!-- gold dot accent -->
        <circle cx="155" cy="220" r="12" fill="#b8960c" opacity=".15"/>
        <circle cx="155" cy="220" r="6" fill="#b8960c" opacity=".3"/>
      </svg>
    </div>

  </div>
</section>

<!-- TEMPLATES -->
<section id="templates">
  <div class="categories-header fade-up">
    <div>
      <div class="section-label">Collection</div>
      <h2>Templates <em>prêts</em> à personnaliser</h2>
    </div>
    <div class="filter-tabs">
      <button class="filter-tab active">Tout</button>
      <button class="filter-tab">Cartes</button>
      <button class="filter-tab">Business</button>
      <button class="filter-tab">Events</button>
    </div>
  </div>

  <div class="templates-grid">

    <!-- 1. Birthday -->
    <div class="template-card fade-up">
      <div class="template-thumb">
        <svg viewBox="0 0 300 400" xmlns="http://www.w3.org/2000/svg">
          <rect width="300" height="400" fill="#fdf6ec"/>
          <circle cx="40" cy="50" r="5" fill="#e8b86d" opacity=".2"/>
          <circle cx="260" cy="80" r="3" fill="#c0392b" opacity=".2"/>
          <circle cx="30" cy="350" r="6" fill="#2c7873" opacity=".15"/>
          <rect x="0" y="0" width="100" height="8" fill="#c0392b"/>
          <rect x="100" y="0" width="100" height="8" fill="#e8b86d"/>
          <rect x="200" y="0" width="100" height="8" fill="#2c7873"/>
          <text x="30" y="48" font-family="Georgia,serif" font-size="9" fill="#c0392b" letter-spacing="2">UNE JOURNÉE SPÉCIALE</text>
          <text x="30" y="85" font-family="Georgia,serif" font-size="38" font-weight="bold" fill="#1a1007">Joyeux</text>
          <text x="30" y="125" font-family="Georgia,serif" font-size="38" font-style="italic" fill="#c0392b">Anniversaire</text>
          <line x1="30" y1="142" x2="130" y2="142" stroke="#1a1007" stroke-opacity=".12" stroke-width=".5"/>
          <text x="150" y="146" font-family="Georgia,serif" font-size="8" fill="#1a1007" opacity=".3" text-anchor="middle">✦</text>
          <line x1="170" y1="142" x2="270" y2="142" stroke="#1a1007" stroke-opacity=".12" stroke-width=".5"/>
          <!-- cake -->
          <ellipse cx="150" cy="272" rx="62" ry="9" fill="#e0d0b8"/>
          <rect x="88" y="230" width="124" height="42" rx="5" fill="#e8b86d"/>
          <rect x="88" y="230" width="124" height="12" rx="5" fill="#d4a247"/>
          <rect x="110" y="202" width="80" height="32" rx="4" fill="#c0392b"/>
          <rect x="110" y="202" width="80" height="10" rx="4" fill="#a93226"/>
          <rect x="131" y="180" width="7" height="24" rx="2" fill="#2c7873"/>
          <rect x="146" y="174" width="7" height="30" rx="2" fill="#e8b86d"/>
          <rect x="161" y="180" width="7" height="24" rx="2" fill="#c0392b"/>
          <ellipse cx="134.5" cy="177" rx="4" ry="6" fill="#f39c12"/>
          <ellipse cx="149.5" cy="171" rx="4" ry="6" fill="#f39c12"/>
          <ellipse cx="164.5" cy="177" rx="4" ry="6" fill="#f39c12"/>
          <text x="150" y="316" font-family="Georgia,serif" font-size="9.5" font-style="italic" fill="#3a2e1e" text-anchor="middle">"Que cette nouvelle année t'apporte</text>
          <text x="150" y="330" font-family="Georgia,serif" font-size="9.5" font-style="italic" fill="#3a2e1e" text-anchor="middle">tout ce que tu mérites."</text>
          <text x="30" y="358" font-family="sans-serif" font-size="8" fill="#aaa" letter-spacing="1.5">POUR</text>
          <text x="30" y="378" font-family="Georgia,serif" font-size="24" font-weight="bold" fill="#1a1007">Sophie</text>
          <circle cx="260" cy="368" r="26" fill="#c0392b"/>
          <text x="260" y="373" font-family="Georgia,serif" font-size="18" font-weight="bold" fill="white" text-anchor="middle">30</text>
          <rect x="0" y="392" width="100" height="8" fill="#2c7873"/>
          <rect x="100" y="392" width="100" height="8" fill="#e8b86d"/>
          <rect x="200" y="392" width="100" height="8" fill="#c0392b"/>
        </svg>
        <div class="template-overlay"><div class="template-overlay-btn">Aperçu</div></div>
      </div>
      <div class="template-name">Carte Anniversaire Élégante</div>
      <div class="template-meta">
        <span class="template-cat">Carte · Anniversaire</span>
        <span class="template-price">7 €</span>
      </div>
    </div>

    <!-- 2. Wedding -->
    <div class="template-card fade-up">
      <div class="template-thumb">
        <svg viewBox="0 0 300 400" xmlns="http://www.w3.org/2000/svg">
          <rect width="300" height="400" fill="#1a1a2a"/>
          <rect x="16" y="16" width="268" height="368" fill="none" stroke="#d4af37" stroke-width="1" opacity=".45"/>
          <rect x="24" y="24" width="252" height="352" fill="none" stroke="#d4af37" stroke-width=".4" opacity=".2"/>
          <!-- corner ornaments -->
          <text x="22" y="38" font-family="serif" font-size="14" fill="#d4af37" opacity=".4">✦</text>
          <text x="262" y="38" font-family="serif" font-size="14" fill="#d4af37" opacity=".4" text-anchor="end">✦</text>
          <text x="22" y="392" font-family="serif" font-size="14" fill="#d4af37" opacity=".4">✦</text>
          <text x="262" y="392" font-family="serif" font-size="14" fill="#d4af37" opacity=".4" text-anchor="end">✦</text>
          <text x="150" y="68" font-family="Georgia,serif" font-size="10" fill="#d4af37" opacity=".6" text-anchor="middle" letter-spacing="4">INVITATION AU MARIAGE</text>
          <line x1="60" y1="78" x2="240" y2="78" stroke="#d4af37" stroke-width=".4" opacity=".3"/>
          <text x="150" y="130" font-family="Georgia,serif" font-size="34" font-style="italic" fill="white" text-anchor="middle">Camille</text>
          <text x="150" y="162" font-family="Georgia,serif" font-size="16" fill="#d4af37" text-anchor="middle">&amp;</text>
          <text x="150" y="200" font-family="Georgia,serif" font-size="34" font-style="italic" fill="white" text-anchor="middle">Antoine</text>
          <line x1="80" y1="218" x2="220" y2="218" stroke="#d4af37" stroke-width=".6" opacity=".4"/>
          <!-- ring illustration -->
          <circle cx="150" cy="278" r="32" fill="none" stroke="#d4af37" stroke-width="2" opacity=".5"/>
          <circle cx="150" cy="278" r="24" fill="none" stroke="#d4af37" stroke-width=".5" opacity=".25"/>
          <ellipse cx="150" cy="278" rx="8" ry="12" fill="#d4af37" opacity=".2"/>
          <text x="150" y="338" font-family="sans-serif" font-size="9" fill="#d4af37" opacity=".65" text-anchor="middle" letter-spacing="2">14 SEPTEMBRE 2026</text>
          <text x="150" y="356" font-family="sans-serif" font-size="8" fill="white" opacity=".35" text-anchor="middle">Château de Vaux-le-Vicomte</text>
          <text x="150" y="372" font-family="sans-serif" font-size="7.5" fill="white" opacity=".25" text-anchor="middle">Maincy, France</text>
        </svg>
        <div class="template-overlay"><div class="template-overlay-btn">Aperçu</div></div>
      </div>
      <div class="template-name">Faire-Part Mariage Nuit Dorée</div>
      <div class="template-meta">
        <span class="template-cat">Carte · Mariage</span>
        <span class="template-price">12 €</span>
      </div>
    </div>

    <!-- 3. Business -->
    <div class="template-card fade-up">
      <div class="template-thumb">
        <svg viewBox="0 0 300 400" xmlns="http://www.w3.org/2000/svg">
          <rect width="300" height="400" fill="#f0ede8"/>
          <rect x="0" y="0" width="8" height="400" fill="#0f0f0f"/>
          <rect x="0" y="0" width="300" height="8" fill="#0f0f0f"/>
          <!-- grid -->
          <circle cx="60" cy="60" r="2" fill="#0f0f0f" opacity=".1"/>
          <circle cx="120" cy="60" r="2" fill="#0f0f0f" opacity=".1"/>
          <circle cx="180" cy="60" r="2" fill="#0f0f0f" opacity=".1"/>
          <circle cx="240" cy="60" r="2" fill="#0f0f0f" opacity=".1"/>
          <circle cx="60" cy="120" r="2" fill="#0f0f0f" opacity=".1"/>
          <circle cx="120" cy="120" r="2" fill="#0f0f0f" opacity=".1"/>
          <circle cx="60" cy="180" r="2" fill="#0f0f0f" opacity=".1"/>
          <!-- big letter -->
          <text x="200" y="220" font-family="Georgia,serif" font-size="180" font-weight="bold" fill="#0f0f0f" opacity=".04">L</text>
          <text x="32" y="120" font-family="Georgia,serif" font-size="11" fill="#0f0f0f" opacity=".35" letter-spacing="3">STUDIO</text>
          <text x="32" y="172" font-family="Georgia,serif" font-size="42" font-weight="bold" fill="#0f0f0f">Léa</text>
          <text x="32" y="214" font-family="Georgia,serif" font-size="42" font-weight="bold" fill="#0f0f0f">Martin</text>
          <line x1="32" y1="230" x2="130" y2="230" stroke="#0f0f0f" stroke-width="1"/>
          <text x="32" y="252" font-family="sans-serif" font-size="9" fill="#555" letter-spacing=".5">Photographe &amp; Directrice créative</text>
          <text x="32" y="310" font-family="sans-serif" font-size="8.5" fill="#777">lea@studio-lumiere.fr</text>
          <text x="32" y="328" font-family="sans-serif" font-size="8.5" fill="#777">+33 6 12 34 56 78</text>
          <text x="32" y="346" font-family="sans-serif" font-size="8.5" fill="#777">studio-lumiere.fr</text>
          <circle cx="250" cy="330" r="30" fill="#b8960c" opacity=".12"/>
          <circle cx="250" cy="330" r="18" fill="#b8960c" opacity=".18"/>
          <circle cx="250" cy="330" r="8" fill="#b8960c" opacity=".3"/>
        </svg>
        <div class="template-overlay"><div class="template-overlay-btn">Aperçu</div></div>
      </div>
      <div class="template-name">Carte de Visite Architecturale</div>
      <div class="template-meta">
        <span class="template-cat">Business · Carte</span>
        <span class="template-price">6 €</span>
      </div>
    </div>

    <!-- 4. Baby shower -->
    <div class="template-card fade-up">
      <div class="template-thumb">
        <svg viewBox="0 0 300 400" xmlns="http://www.w3.org/2000/svg">
          <rect width="300" height="400" fill="#f9f0f5"/>
          <!-- soft circles bg -->
          <circle cx="30" cy="50" r="40" fill="#e8c4d8" opacity=".2"/>
          <circle cx="270" cy="80" r="60" fill="#c9e4f0" opacity=".15"/>
          <circle cx="40" cy="380" r="50" fill="#e8c4d8" opacity=".15"/>
          <circle cx="260" cy="370" r="35" fill="#c9e4f0" opacity=".12"/>
          <!-- banner top -->
          <path d="M0,0 Q150,30 300,0 L300,50 Q150,20 0,50 Z" fill="#d4a8c7" opacity=".3"/>
          <text x="150" y="32" font-family="Georgia,serif" font-size="11" fill="#8b4578" opacity=".7" text-anchor="middle" letter-spacing="3">BABY SHOWER</text>
          <!-- bunny -->
          <circle cx="150" cy="160" r="38" fill="#f7e8f2"/>
          <ellipse cx="132" cy="118" rx="10" ry="22" fill="#f7e8f2"/>
          <ellipse cx="168" cy="118" rx="10" ry="22" fill="#f7e8f2"/>
          <ellipse cx="132" cy="118" rx="5" ry="16" fill="#e8c4d8" opacity=".7"/>
          <ellipse cx="168" cy="118" rx="5" ry="16" fill="#e8c4d8" opacity=".7"/>
          <circle cx="141" cy="155" r="3" fill="#d4a8c7"/>
          <circle cx="159" cy="155" r="3" fill="#d4a8c7"/>
          <ellipse cx="150" cy="168" rx="6" ry="4" fill="#e8c4d8"/>
          <!-- whiskers -->
          <line x1="120" y1="162" x2="144" y2="165" stroke="#c9a0b8" stroke-width=".8" opacity=".6"/>
          <line x1="120" y1="168" x2="144" y2="168" stroke="#c9a0b8" stroke-width=".8" opacity=".6"/>
          <line x1="156" y1="165" x2="180" y2="162" stroke="#c9a0b8" stroke-width=".8" opacity=".6"/>
          <line x1="156" y1="168" x2="180" y2="168" stroke="#c9a0b8" stroke-width=".8" opacity=".6"/>
          <text x="150" y="228" font-family="Georgia,serif" font-size="11" fill="#8b4578" opacity=".6" text-anchor="middle" letter-spacing="2">BIENVENUE PETIT(E)</text>
          <text x="150" y="270" font-family="Georgia,serif" font-size="38" font-style="italic" fill="#8b4578" text-anchor="middle">Chloé</text>
          <line x1="70" y1="285" x2="230" y2="285" stroke="#d4a8c7" stroke-width=".6"/>
          <text x="150" y="308" font-family="sans-serif" font-size="9" fill="#b085a0" text-anchor="middle" letter-spacing="1">15 JUILLET 2026 · 15H00</text>
          <text x="150" y="326" font-family="sans-serif" font-size="8.5" fill="#c0a0b0" text-anchor="middle">Chez Marie &amp; Paul</text>
          <!-- dots bottom -->
          <circle cx="90" cy="366" r="5" fill="#d4a8c7" opacity=".4"/>
          <circle cx="110" cy="372" r="3" fill="#c9e4f0" opacity=".5"/>
          <circle cx="150" cy="362" r="4" fill="#d4a8c7" opacity=".35"/>
          <circle cx="190" cy="372" r="3" fill="#c9e4f0" opacity=".45"/>
          <circle cx="210" cy="364" r="5" fill="#d4a8c7" opacity=".3"/>
        </svg>
        <div class="template-overlay"><div class="template-overlay-btn">Aperçu</div></div>
      </div>
      <div class="template-name">Invitation Baby Shower Doux</div>
      <div class="template-meta">
        <span class="template-cat">Carte · Naissance</span>
        <span class="template-price">8 €</span>
      </div>
    </div>

    <!-- 5. Instagram post -->
    <div class="template-card fade-up">
      <div class="template-thumb">
        <svg viewBox="0 0 300 300" xmlns="http://www.w3.org/2000/svg">
          <rect width="300" height="300" fill="#0d0d0d"/>
          <!-- gradient overlay top -->
          <defs>
            <radialGradient id="glow1" cx="30%" cy="30%" r="70%">
              <stop offset="0%" stop-color="#6c3bbf" stop-opacity="0.4"/>
              <stop offset="100%" stop-color="#0d0d0d" stop-opacity="0"/>
            </radialGradient>
            <radialGradient id="glow2" cx="70%" cy="70%" r="60%">
              <stop offset="0%" stop-color="#e8485a" stop-opacity="0.3"/>
              <stop offset="100%" stop-color="#0d0d0d" stop-opacity="0"/>
            </radialGradient>
          </defs>
          <rect width="300" height="300" fill="url(#glow1)"/>
          <rect width="300" height="300" fill="url(#glow2)"/>
          <!-- grid lines -->
          <line x1="0" y1="100" x2="300" y2="100" stroke="white" stroke-opacity=".04"/>
          <line x1="0" y1="200" x2="300" y2="200" stroke="white" stroke-opacity=".04"/>
          <line x1="100" y1="0" x2="100" y2="300" stroke="white" stroke-opacity=".04"/>
          <line x1="200" y1="0" x2="200" y2="300" stroke="white" stroke-opacity=".04"/>
          <!-- tag -->
          <rect x="20" y="20" width="80" height="22" rx="2" fill="white" fill-opacity=".08"/>
          <text x="60" y="34" font-family="sans-serif" font-size="8" fill="white" opacity=".5" text-anchor="middle" letter-spacing="1.5">BRANDING</text>
          <!-- main text -->
          <text x="22" y="120" font-family="Georgia,serif" font-size="36" font-weight="bold" fill="white">Faites-vous</text>
          <text x="22" y="158" font-family="Georgia,serif" font-size="36" font-weight="bold" fill="white">remarquer</text>
          <text x="22" y="190" font-family="Georgia,serif" font-size="36" font-style="italic" fill="#a78bfa">enfin.</text>
          <line x1="22" y1="208" x2="100" y2="208" stroke="white" stroke-opacity=".2" stroke-width=".8"/>
          <text x="22" y="228" font-family="sans-serif" font-size="9" fill="white" opacity=".4" letter-spacing=".5">Identité visuelle · Canva templates</text>
          <!-- logo area -->
          <circle cx="258" cy="264" r="24" fill="white" fill-opacity=".06"/>
          <text x="258" y="270" font-family="Georgia,serif" font-size="10" fill="white" opacity=".5" text-anchor="middle">SL</text>
        </svg>
        <div class="template-overlay"><div class="template-overlay-btn">Aperçu</div></div>
      </div>
      <div class="template-name">Post Instagram Branding Nuit</div>
      <div class="template-meta">
        <span class="template-cat">Réseaux · Instagram</span>
        <span class="template-price">5 €</span>
      </div>
    </div>

    <!-- 6. Thank you card -->
    <div class="template-card fade-up">
      <div class="template-thumb">
        <svg viewBox="0 0 300 400" xmlns="http://www.w3.org/2000/svg">
          <rect width="300" height="400" fill="#f5f2ed"/>
          <!-- botanical lines top-left -->
          <line x1="0" y1="60" x2="60" y2="0" stroke="#2d5a3d" stroke-width=".8" opacity=".25"/>
          <line x1="0" y1="90" x2="90" y2="0" stroke="#2d5a3d" stroke-width=".5" opacity=".15"/>
          <line x1="0" y1="40" x2="40" y2="0" stroke="#2d5a3d" stroke-width=".4" opacity=".1"/>
          <!-- leaf cluster top-left -->
          <ellipse cx="18" cy="42" rx="12" ry="20" fill="#2d5a3d" opacity=".18" transform="rotate(-30 18 42)"/>
          <ellipse cx="34" cy="28" rx="9" ry="16" fill="#4a8c5c" opacity=".14" transform="rotate(15 34 28)"/>
          <ellipse cx="8" cy="28" rx="7" ry="14" fill="#2d5a3d" opacity=".12" transform="rotate(-50 8 28)"/>
          <!-- leaf cluster bottom-right -->
          <ellipse cx="282" cy="358" rx="12" ry="20" fill="#2d5a3d" opacity=".18" transform="rotate(150 282 358)"/>
          <ellipse cx="266" cy="372" rx="9" ry="16" fill="#4a8c5c" opacity=".14" transform="rotate(195 266 372)"/>
          <ellipse cx="292" cy="372" rx="7" ry="14" fill="#2d5a3d" opacity=".12" transform="rotate(130 292 372)"/>
          <!-- center content -->
          <text x="150" y="148" font-family="Georgia,serif" font-size="10" fill="#2d5a3d" opacity=".55" text-anchor="middle" letter-spacing="3">UN GRAND</text>
          <text x="150" y="210" font-family="Georgia,serif" font-size="68" font-style="italic" fill="#1c2b1f" text-anchor="middle">Merci</text>
          <line x1="80" y1="224" x2="220" y2="224" stroke="#2d5a3d" stroke-width=".5" opacity=".3"/>
          <text x="150" y="258" font-family="Georgia,serif" font-size="10.5" font-style="italic" fill="#4a6b52" text-anchor="middle">Votre soutien compte infiniment.</text>
          <text x="150" y="276" font-family="Georgia,serif" font-size="10.5" font-style="italic" fill="#4a6b52" text-anchor="middle">Merci du fond du cœur.</text>
          <!-- small leaf divider -->
          <text x="150" y="310" font-family="serif" font-size="16" fill="#2d5a3d" opacity=".3" text-anchor="middle">❧</text>
          <text x="150" y="346" font-family="Georgia,serif" font-size="20" fill="#1c2b1f" text-anchor="middle">Marie &amp; Thomas</text>
        </svg>
        <div class="template-overlay"><div class="template-overlay-btn">Aperçu</div></div>
      </div>
      <div class="template-name">Carte Remerciements Botanique</div>
      <div class="template-meta">
        <span class="template-cat">Carte · Remerciements</span>
        <span class="template-price">6 €</span>
      </div>
    </div>

  </div>
</section>

<!-- PROCESS -->
<section id="process">
  <div class="section-label fade-up">Comment ça marche</div>
  <h2 class="fade-up">Simple comme <em>bonjour.</em></h2>
  <p class="section-intro fade-up">Pas besoin d'être designer. Chaque template est conçu pour que tu puisses le personnaliser en moins de 10 minutes.</p>

  <div class="process-grid">
    <div class="process-step fade-up">
      <div class="step-num">01</div>
      <div class="step-title">Tu choisis ton template</div>
      <p class="step-desc">Parcours la collection et trouve le design qui correspond à ton occasion et ton style.</p>
    </div>
    <div class="process-step fade-up">
      <div class="step-num">02</div>
      <div class="step-title">Tu reçois le lien Canva</div>
      <p class="step-desc">Après l'achat, un lien direct vers le template Canva t'est envoyé instantanément.</p>
    </div>
    <div class="process-step fade-up">
      <div class="step-num">03</div>
      <div class="step-title">Tu personnalises</div>
      <p class="step-desc">Texte, couleurs, photos — tout est modifiable. Canva est gratuit et ne demande aucune installation.</p>
    </div>
    <div class="process-step fade-up">
      <div class="step-num">04</div>
      <div class="step-title">Tu télécharges & utilises</div>
      <p class="step-desc">Exporte en PDF ou PNG en haute résolution. Prêt à imprimer ou envoyer en numérique.</p>
    </div>
  </div>
</section>

<!-- AVIS -->
<section id="avis">
  <div class="section-label fade-up">Avis clients</div>
  <h2 class="fade-up">Ils ont aimé, ils <em>reviennent.</em></h2>
  <p class="section-intro fade-up" style="color:rgba(255,255,255,0.45)">Plus de 2 000 clients depuis l'ouverture de la boutique.</p>

  <div class="testimonials-grid">
    <div class="testimonial fade-up">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">"Le faire-part mariage a fait l'unanimité. Tout le monde nous a demandé qui l'avait créé. Incroyable pour un template !"</p>
      <div class="testimonial-author">
        <div class="author-avatar" style="background:#8b4578;">C</div>
        <div>
          <div class="author-name">Camille R.</div>
          <div class="author-role">Future mariée · Paris</div>
        </div>
      </div>
    </div>
    <div class="testimonial fade-up">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">"J'ai personnalisé la carte d'anniversaire en 5 minutes chrono. Résultat bluffant, ma mère a cru que c'était fait par un pro."</p>
      <div class="testimonial-author">
        <div class="author-avatar" style="background:#2c7873;">J</div>
        <div>
          <div class="author-name">Julien M.</div>
          <div class="author-role">Client fidèle · Lyon</div>
        </div>
      </div>
    </div>
    <div class="testimonial fade-up">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">"Carte de visite livrée en 2 jours après achat du template. Design unique, propre, moderne. Je recommande les yeux fermés."</p>
      <div class="testimonial-author">
        <div class="author-avatar" style="background:#b8960c;">S</div>
        <div>
          <div class="author-name">Sophie T.</div>
          <div class="author-role">Graphiste freelance · Bordeaux</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA -->
<div class="cta-banner">
  <h2>Prêt(e) à créer <em>quelque chose de beau ?</em></h2>
  <p>Tous les templates sont modifiables, téléchargeables et utilisables à vie.</p>
  <a href="#templates" class="btn-white">Voir toute la collection →</a>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Studio <span>Lumière</span></div>
  <div>Templates Canva Premium · Fait avec soin en France</div>
  <div>© 2026 Studio Lumière</div>
</footer>

<script>
// Scroll animations
const observer = new IntersectionObserver((entries) => {
  entries.forEach((entry, i) => {
    if (entry.isIntersecting) {
      setTimeout(() => entry.target.classList.add('visible'), i * 80);
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

// Filter tabs (UI only)
document.querySelectorAll('.filter-tab').forEach(tab => {
  tab.addEventListener('click', () => {
    document.querySelectorAll('.filter-tab').forEach(t => t.classList.remove('active'));
    tab.classList.add('active');
  });
});
</script>
</body>
</html>
