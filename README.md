<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abubakr Yernazarov — Neurologist & Founder of NeyroYo'l</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0d1117;
    --paper: #f7f4ef;
    --accent: #1a6b4a;
    --accent-light: #e8f4ef;
    --muted: #6b7280;
    --border: #e2ddd6;
    --white: #ffffff;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--paper);
    color: var(--ink);
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.2rem 3rem;
    background: rgba(247,244,239,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    font-family: 'DM Serif Display', serif;
    font-size: 1.1rem;
    color: var(--ink);
    text-decoration: none;
    letter-spacing: -0.02em;
  }

  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .nav-links a {
    text-decoration: none;
    color: var(--muted);
    font-size: 0.875rem;
    font-weight: 500;
    letter-spacing: 0.03em;
    text-transform: uppercase;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--accent); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding-top: 80px;
  }

  .hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 5rem 3rem 5rem 3rem;
    border-right: 1px solid var(--border);
  }

  .hero-tag {
    display: inline-block;
    background: var(--accent-light);
    color: var(--accent);
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 0.35rem 0.85rem;
    border-radius: 2rem;
    margin-bottom: 1.5rem;
    width: fit-content;
  }

  .hero-title {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2.5rem, 4vw, 4rem);
    line-height: 1.1;
    letter-spacing: -0.03em;
    margin-bottom: 1rem;
  }

  .hero-title em {
    font-style: italic;
    color: var(--accent);
  }

  .hero-subtitle {
    font-size: 1rem;
    color: var(--muted);
    font-weight: 300;
    margin-bottom: 2rem;
    max-width: 400px;
    line-height: 1.7;
  }

  .hero-cta {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--ink);
    color: var(--white);
    padding: 0.85rem 1.75rem;
    border-radius: 0.5rem;
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 500;
    width: fit-content;
    transition: background 0.2s, transform 0.2s;
  }

  .hero-cta:hover { background: var(--accent); transform: translateY(-1px); }

  .hero-right {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 5rem 3rem;
    background: var(--white);
  }

  .stat-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
  }

  .stat-card {
    padding: 1.5rem;
    border: 1px solid var(--border);
    border-radius: 0.75rem;
    background: var(--paper);
    transition: border-color 0.2s, transform 0.2s;
  }

  .stat-card:hover { border-color: var(--accent); transform: translateY(-2px); }

  .stat-number {
    font-family: 'DM Serif Display', serif;
    font-size: 2.5rem;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 0.35rem;
  }

  .stat-label {
    font-size: 0.8rem;
    color: var(--muted);
    font-weight: 500;
    line-height: 1.4;
  }

  /* ── SECTION ── */
  section {
    padding: 5rem 3rem;
    border-bottom: 1px solid var(--border);
    max-width: 1100px;
    margin: 0 auto;
  }

  .section-label {
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 0.75rem;
  }

  .section-title {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.5rem);
    letter-spacing: -0.02em;
    line-height: 1.15;
    margin-bottom: 1.5rem;
  }

  .section-body {
    font-size: 1rem;
    color: #374151;
    line-height: 1.8;
    max-width: 680px;
  }

  /* ── WHAT I DO ── */
  .services {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    margin-top: 2.5rem;
  }

  .service-card {
    padding: 2rem 1.5rem;
    border: 1px solid var(--border);
    border-radius: 0.75rem;
    background: var(--white);
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
  }

  .service-card:hover { border-color: var(--accent); transform: translateY(-3px); }

  .service-icon {
    font-size: 1.75rem;
    margin-bottom: 1rem;
  }

  .service-title {
    font-family: 'DM Serif Display', serif;
    font-size: 1.15rem;
    margin-bottom: 0.5rem;
  }

  .service-desc {
    font-size: 0.875rem;
    color: var(--muted);
    line-height: 1.6;
  }

  /* ── DIFFERENCE ── */
  .diff-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0;
    margin-top: 2.5rem;
    border: 1px solid var(--border);
    border-radius: 0.75rem;
    overflow: hidden;
  }

  .diff-col { padding: 2rem; }
  .diff-col:first-child { border-right: 1px solid var(--border); background: #fafafa; }
  .diff-col:last-child { background: var(--white); }

  .diff-col-title {
    font-size: 0.75rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 1.25rem;
    padding-bottom: 0.75rem;
    border-bottom: 1px solid var(--border);
  }

  .diff-col:first-child .diff-col-title { color: var(--muted); }
  .diff-col:last-child .diff-col-title { color: var(--accent); }

  .diff-item {
    display: flex;
    align-items: flex-start;
    gap: 0.65rem;
    margin-bottom: 0.85rem;
    font-size: 0.9rem;
    line-height: 1.5;
  }

  .diff-item .icon { flex-shrink: 0; margin-top: 0.1rem; }

  /* ── PUBLICATIONS ── */
  .pub-list { margin-top: 2rem; display: flex; flex-direction: column; gap: 1rem; }

  .pub-card {
    padding: 1.5rem;
    border: 1px solid var(--border);
    border-radius: 0.75rem;
    background: var(--white);
    display: flex;
    gap: 1.25rem;
    align-items: flex-start;
    transition: border-color 0.2s;
  }

  .pub-card:hover { border-color: var(--accent); }

  .pub-year {
    font-family: 'DM Serif Display', serif;
    font-size: 1.5rem;
    color: var(--accent);
    flex-shrink: 0;
    line-height: 1;
    padding-top: 0.15rem;
  }

  .pub-title {
    font-weight: 500;
    font-size: 0.95rem;
    margin-bottom: 0.35rem;
    line-height: 1.4;
  }

  .pub-meta {
    font-size: 0.8rem;
    color: var(--muted);
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 3rem;
    align-items: start;
    margin-top: 2rem;
  }

  .about-text { font-size: 1rem; color: #374151; line-height: 1.8; }
  .about-text p { margin-bottom: 1rem; }

  .about-sidebar { display: flex; flex-direction: column; gap: 1rem; }

  .sidebar-item {
    padding: 1.25rem;
    border: 1px solid var(--border);
    border-radius: 0.75rem;
    background: var(--white);
  }

  .sidebar-item-label {
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 0.35rem;
  }

  .sidebar-item-value {
    font-size: 0.9rem;
    font-weight: 500;
  }

  /* ── CONTACT ── */
  .contact-section {
    background: var(--ink);
    color: var(--white);
    padding: 5rem 3rem;
    text-align: center;
  }

  .contact-section .section-label { color: var(--accent-light); }

  .contact-title {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 3.5vw, 3rem);
    margin-bottom: 1rem;
    letter-spacing: -0.02em;
  }

  .contact-sub {
    color: #9ca3af;
    font-size: 1rem;
    margin-bottom: 2rem;
  }

  .contact-email {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--accent);
    color: var(--white);
    padding: 0.9rem 2rem;
    border-radius: 0.5rem;
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95rem;
    transition: opacity 0.2s, transform 0.2s;
  }

  .contact-email:hover { opacity: 0.9; transform: translateY(-1px); }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .fade-up { animation: fadeUp 0.6s ease forwards; }
  .delay-1 { animation-delay: 0.1s; opacity: 0; }
  .delay-2 { animation-delay: 0.2s; opacity: 0; }
  .delay-3 { animation-delay: 0.3s; opacity: 0; }
  .delay-4 { animation-delay: 0.4s; opacity: 0; }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; }
    .hero-left { border-right: none; border-bottom: 1px solid var(--border); padding: 3rem 1.5rem; }
    .hero-right { padding: 3rem 1.5rem; }
    section { padding: 3rem 1.5rem; }
    .services { grid-template-columns: 1fr; }
    .diff-grid { grid-template-columns: 1fr; }
    .diff-col:first-child { border-right: none; border-bottom: 1px solid var(--border); }
    .about-grid { grid-template-columns: 1fr; }
    .contact-section { padding: 3rem 1.5rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">NeyroYo'l</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#difference">Why Us</a></li>
    <li><a href="#publications">Research</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-left">
    <span class="hero-tag fade-up">Tashkent, Uzbekistan</span>
    <h1 class="hero-title fade-up delay-1">
      Neurological care<br>that comes <em>to you</em>
    </h1>
    <p class="hero-subtitle fade-up delay-2">
      NeyroYo'l brings professional EEG diagnostics and neurological consultation directly to patients who cannot access standard clinical settings — children with autism, cerebral palsy, epilepsy, and critically ill patients in hospitals without equipment.
    </p>
    <a href="#contact" class="hero-cta fade-up delay-3">
      Get in touch →
    </a>
  </div>

  <div class="hero-right">
    <div class="stat-grid fade-up delay-2">
      <div class="stat-card">
        <div class="stat-number">150+</div>
        <div class="stat-label">EEG sessions completed in first year</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">24/7</div>
        <div class="stat-label">Including nights, weekends & holidays</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">2</div>
        <div class="stat-label">Peer-reviewed publications in neurology</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">$0</div>
        <div class="stat-label">Charged when families cannot afford care</div>
      </div>
    </div>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">Who I am</div>
  <h2 class="section-title">Neurologist, researcher,<br>and founder</h2>
  <div class="about-grid">
    <div class="about-text">
      <p>
        My name is Abubakr Yernazarov. I am a practicing neurologist and third-year master's student in the Department of Neurology in Tashkent, Uzbekistan. I also live with a disability — which means I understand inaccessibility not as a policy problem, but as something I navigate personally every day.
      </p>
      <p>
        In 2024, I founded NeyroYo'l (Uzbek for "neuro path") — a mobile neurodiagnostics service built around a simple principle: if the patient cannot come to the clinic, the clinic must come to the patient.
      </p>
      <p>
        Unlike standard mobile EEG providers who send technicians, I perform every session myself as a licensed neurologist. I interpret results on the spot, explain the diagnosis and its clinical implications to families in plain language, and connect patients with the right specialists — neuropsychologists, speech therapists, rehabilitation teams. One visit. Complete care.
      </p>
    </div>
    <div class="about-sidebar">
      <div class="sidebar-item">
        <div class="sidebar-item-label">Location</div>
        <div class="sidebar-item-value">Tashkent & Tashkent Region, Uzbekistan</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-item-label">Specialty</div>
        <div class="sidebar-item-value">Neurology — Pediatric & Adult</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-item-label">Education</div>
        <div class="sidebar-item-value">Master's in Neurology (Year 3)</div>
      </div>
      <div class="sidebar-item">
        <div class="sidebar-item-label">Languages</div>
        <div class="sidebar-item-value">Uzbek, Russian, English</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="section-label">What we do</div>
  <h2 class="section-title">Full neurological care,<br>wherever you are</h2>
  <p class="section-body">
    NeyroYo'l operates across Tashkent city and the Tashkent region — visiting family homes, and traveling to hospital wards that lack diagnostic equipment.
  </p>
  <div class="services">
    <div class="service-card">
      <div class="service-icon">🧠</div>
      <div class="service-title">Home-Visit EEG</div>
      <div class="service-desc">Portable EEG for children with autism, cerebral palsy, and epilepsy in the comfort and safety of their own home — where they can actually cooperate.</div>
    </div>
    <div class="service-card">
      <div class="service-icon">🏥</div>
      <div class="service-title">Bedside EEG</div>
      <div class="service-desc">EEG for comatose and critically ill patients in public and private hospitals that have no EEG device on-site. Available at any hour.</div>
    </div>
    <div class="service-card">
      <div class="service-icon">💬</div>
      <div class="service-title">On-Site Consultation</div>
      <div class="service-desc">Every session includes a full neurological consultation — diagnosis interpretation, pathogenesis explained in plain language, and referrals to the right specialists.</div>
    </div>
  </div>
</section>

<!-- DIFFERENCE -->
<section id="difference">
  <div class="section-label">Why NeyroYo'l</div>
  <h2 class="section-title">Not just faster —<br>fundamentally different</h2>
  <p class="section-body">
    Other mobile EEG services exist. Here is what makes NeyroYo'l different.
  </p>
  <div class="diff-grid">
    <div class="diff-col">
      <div class="diff-col-title">Standard mobile EEG</div>
      <div class="diff-item"><span class="icon">✗</span><span>Student or technician performs the procedure</span></div>
      <div class="diff-item"><span class="icon">✗</span><span>No consultation — results sent later</span></div>
      <div class="diff-item"><span class="icon">✗</span><span>Travel costs charged separately</span></div>
      <div class="diff-item"><span class="icon">✗</span><span>No specialist referrals provided</span></div>
      <div class="diff-item"><span class="icon">✗</span><span>Often unavailable on weekends</span></div>
      <div class="diff-item"><span class="icon">✗</span><span>Fixed pricing regardless of family income</span></div>
    </div>
    <div class="diff-col">
      <div class="diff-col-title">NeyroYo'l</div>
      <div class="diff-item"><span class="icon" style="color:var(--accent)">✓</span><span>Licensed neurologist performs every session</span></div>
      <div class="diff-item"><span class="icon" style="color:var(--accent)">✓</span><span>Full consultation on the spot — diagnosis explained to family</span></div>
      <div class="diff-item"><span class="icon" style="color:var(--accent)">✓</span><span>All-inclusive pricing, no hidden travel costs</span></div>
      <div class="diff-item"><span class="icon" style="color:var(--accent)">✓</span><span>Referrals to neuropsychologists, speech therapists & more</span></div>
      <div class="diff-item"><span class="icon" style="color:var(--accent)">✓</span><span>24/7 including nights, weekends & holidays</span></div>
      <div class="diff-item"><span class="icon" style="color:var(--accent)">✓</span><span>Free for families who cannot pay</span></div>
    </div>
  </div>
</section>

<!-- PUBLICATIONS -->
<section id="publications">
  <div class="section-label">Research</div>
  <h2 class="section-title">Peer-reviewed publications</h2>
  <div class="pub-list">
    <div class="pub-card">
      <div class="pub-year">2025</div>
      <div>
        <div class="pub-title">Information and Communication Technologies in the Diagnosis and Treatment of Patients with Chronic Cerebral Ischemia</div>
        <div class="pub-meta">Review article · Journal of Neurology and Neurosurgical Research, Vol. 6, No. 1 · Co-authors: Maksudova Khurshida Nabievna (PhD, Associate Professor), Rajapov Amirbek Azatbaevich</div>
      </div>
    </div>
    <div class="pub-card">
      <div class="pub-year">2026</div>
      <div>
        <div class="pub-title">Information and Communication Technologies in the Diagnosis and Treatment of Patients with Chronic Cerebral Ischemia</div>
        <div class="pub-meta">Scientific-practical article · NEVROLOGIYA Journal, Issue 1 · Co-authors: Maksudova Khurshida Nabievna (PhD, Associate Professor), Rajapov Amirbek Azatbaevich</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<div class="contact-section" id="contact">
  <div class="section-label">Get in touch</div>
  <h2 class="contact-title">Ready to help your patient</h2>
  <p class="contact-sub">Serving Tashkent city and Tashkent region · Available 24/7</p>
  <a href="mailto:abubakr-ernazarov@mail.ru" class="contact-email">
    abubakr-ernazarov@mail.ru →
  </a>
</div>

</body>
</html>