<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Diplomarbeit – TGM Wien × Technologen Verband</title>
  <meta name="description" content="OnePager zur Diplomarbeit: Aufgabenstellung, Team, Fortschritt und Kontakt." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --blue-700:#0B63B6; 
      --blue-600:#1273D1;
      --blue-500:#1A88F0;
      --gray-950:#0b0f14;
      --gray-900:#121721;
      --gray-800:#1b2230;
      --gray-700:#2a3446;
      --gray-400:#94a3b8;
      --gray-200:#e2e8f0;
      --gray-100:#f1f5f9;
      --white:#ffffff;
      --accent:#00D1C7; 
      --radius-2xl: 1.25rem;
      --shadow-soft: 0 10px 30px rgba(0,0,0,.15);
    }
    html{scroll-behavior:smooth}
    body{
      margin:0; font-family:Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji";
      color:var(--gray-100); background:linear-gradient(180deg, var(--gray-900), var(--gray-800));
    }
    a{color:inherit; text-decoration:none}
    .container{width:min(1100px, 92vw); margin-inline:auto}

    /* ====== NAVBAR ====== */
    header{
      position:sticky; top:0; z-index:50; backdrop-filter:saturate(1.2) blur(10px);
      background:rgba(18,23,33,.6); border-bottom:1px solid rgba(255,255,255,.06);
    }
    .nav{display:flex; align-items:center; justify-content:space-between; padding:.9rem 0}
    .brand{display:flex; gap:.65rem; align-items:center; font-weight:800; letter-spacing:.3px}
    .brand .dot{width:10px;height:10px;border-radius:999px;background:var(--accent);display:inline-block}
    nav ul{display:flex; gap:1rem; list-style:none; padding:0; margin:0}
    nav a{padding:.6rem .85rem; border-radius:.6rem; color:var(--gray-200); font-weight:600}
    nav a:hover{background:rgba(255,255,255,.06); color:var(--white)}
    .menu-btn{display:none; background:none; border:0; color:var(--white); font-size:1.2rem}

    /* ====== HERO ====== */
    .hero{position:relative; overflow:hidden}
    .hero .wrap{display:grid; grid-template-columns:1.2fr .8fr; gap:2rem; padding:4.2rem 0 3rem}
    .badge{display:inline-flex; align-items:center; gap:.5rem; padding:.35rem .6rem; border-radius:999px; background:rgba(26,136,240,.15); color:#cfe7ff; font-weight:700; font-size:.78rem; border:1px solid rgba(26,136,240,.25)}
    .title{font-size:clamp(2rem, 4vw, 3rem); line-height:1.1; font-weight:800; margin:.8rem 0}
    .subtitle{color:var(--gray-200); font-size:1.1rem; max-width:60ch}
    .cta-row{display:flex; gap:.8rem; margin-top:1.4rem}
    .btn{display:inline-flex; align-items:center; gap:.5rem; padding:.85rem 1.1rem; border-radius:.9rem; border:1px solid rgba(255,255,255,.08); font-weight:700}
    .btn.primary{background:linear-gradient(135deg, var(--blue-600), var(--blue-500)); box-shadow:0 8px 24px rgba(26,136,240,.35)}
    .btn.primary:hover{filter:brightness(1.1)}
    .btn.ghost:hover{background:rgba(255,255,255,.06)}

    .card{background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03)); border:1px solid rgba(255,255,255,.08); border-radius:var(--radius-2xl); box-shadow:var(--shadow-soft)}
    .hero .visual{min-height:260px; background:
      radial-gradient(800px 300px at -20% -30%, rgba(26,136,240,.35), transparent),
      radial-gradient(600px 240px at 120% 120%, rgba(0,209,199,.25), transparent),
      linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      border:1px solid rgba(255,255,255,.08);
      border-radius:var(--radius-2xl);
      position:relative; display:flex; align-items:center; justify-content:center;
    }
    .visual .logo{display:grid; place-items:center; width:min(420px, 80%); aspect-ratio:16/9; border-radius:1rem; border:1px dashed rgba(255,255,255,.14)}
    .visual .logo span{font-weight:800; letter-spacing:.6px; text-align:center}

    /* ====== SECTIONS ====== */
    section{padding:3.5rem 0}
    .section-head{display:flex; align-items:baseline; justify-content:space-between; margin-bottom:1.2rem}
    .section-head h2{margin:0; font-size:1.8rem}
    .section-head p{margin:0; color:var(--gray-400)}

    /* Aufgabenstellung */
    .aufgabe{display:grid; grid-template-columns:1.1fr .9fr; gap:1.8rem}
    .aufgabe .box{padding:1.2rem 1.2rem}

    /* Team */
    .team-grid{display:grid; grid-template-columns:repeat(3, 1fr); gap:1rem}
    .member{padding:1rem}
    .avatar{width:84px; height:84px; border-radius:50%; background:linear-gradient(180deg,#1f2937,#111827); border:2px solid rgba(255,255,255,.14);object-fit: cover;object-position: center;}
    .member h3{margin:.8rem 0 .2rem}
    .role{color:var(--gray-400); font-size:.95rem}
    .chip{display:inline-block; margin-top:.6rem; font-size:.8rem; padding:.25rem .5rem; border-radius:.6rem; border:1px solid rgba(255,255,255,.12); color:#cfe7ff}

    /* Fortschritt */
    .progress-wrap{display:grid; grid-template-columns:1fr 1fr; gap:1.2rem}
    .meter{height:12px; background:rgba(255,255,255,.08); border-radius:999px; overflow:hidden; border:1px solid rgba(255,255,255,.08)}
    .meter > span{display:block; height:100%; width:40%; background:linear-gradient(90deg, var(--blue-600), var(--blue-500));}
    .timeline{display:grid; gap:.8rem}
    .milestone{display:flex; gap:.8rem; align-items:flex-start; padding:.8rem; border-radius:.9rem; border:1px solid rgba(255,255,255,.08); background:rgba(255,255,255,.03)}
    .milestone .dot{width:10px; height:10px; border-radius:999px; background:var(--accent); margin-top:.35rem}
    .milestone small{color:var(--gray-400)}

    /* Kontakt */
    .contact-card{display:grid; grid-template-columns:1.2fr .8fr; gap:1rem; padding:1.2rem}
    .contact-card a.mail{display:inline-flex; align-items:center; gap:.6rem; padding:.7rem 1rem; border-radius:.8rem; background:rgba(26,136,240,.12); border:1px solid rgba(26,136,240,.25); font-weight:700; color:#cfe7ff}
    .contact-card a.mail:hover{background:rgba(26,136,240,.18)}

    footer{padding:2rem 0; color:var(--gray-400); text-align:center; border-top:1px solid rgba(255,255,255,.06)}

    /* ====== RESPONSIVE ====== */
    @media (max-width: 900px){
      .hero .wrap{grid-template-columns:1fr; padding:3rem 0 1.8rem}
      .aufgabe{grid-template-columns:1fr}
      .team-grid{grid-template-columns:1fr 1fr}
      .progress-wrap{grid-template-columns:1fr}
      .contact-card{grid-template-columns:1fr}
      .menu-btn{display:inline-block}
      nav ul{position:fixed; right:1rem; top:64px; background:rgba(18,23,33,.96); border:1px solid rgba(255,255,255,.08); border-radius:1rem; padding:.6rem; display:none; flex-direction:column; box-shadow:var(--shadow-soft)}
      nav ul.open{display:flex}
    }
  </style>
</head>
<body>
  <!-- ====== NAVBAR ====== -->
  <header>
    <div class="container nav">
      <div class="brand" aria-label="Logo und Projekt">
        <span class="dot" aria-hidden="true"></span>
        <span>TGM Wien × Technologen Verband | TV-Website</span>
      </div>
      <nav aria-label="Hauptnavigation">
        <button class="menu-btn" aria-expanded="false" aria-controls="menu">☰</button>
        <ul id="menu">
          <li><a href="#aufgabe">Aufgabenstellung</a></li>
          <li><a href="#team">Team</a></li>
          <li><a href="#fortschritt">Fortschritt</a></li>
          <li><a href="#kontakt">Kontakt</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- ====== HERO ====== -->
  <section class="hero">
    <div class="container wrap">
      <div>
        <span class="badge">Diplomarbeit • TV-Website</span>
        <h1 class="title">Projekt-TV-Website: <span style="color:#cfe7ff">Neugestalltung der TV Website</span></h1>
        <p class="subtitle">Die Website des "Verband der Technologen" am TGM ist mittlerweile schon in die Jahre gekommen, nun sollen wir als Projektteam diese Website wieder auf den neusten technischen und optischen Stand bringen.</p>
        <div class="cta-row">
          <a class="btn primary" href="#aufgabe">Los geht’s</a>
          <a class="btn ghost" href="#kontakt">Kontakt</a>
        </div>
      </div>
      <div class="visual card" aria-hidden="true">
        <div class="logo"><span>TGM × TV<br/>Projektlogo/Platzhalter</span></div>
      </div>
    </div>
  </section>

  <!-- ====== AUFGABENSTELLUNG ====== -->
  <section id="aufgabe">
    <div class="container">
      <div class="section-head">
        <h2>Beschreibung der Aufgabenstellung</h2>
        <p>Worum geht’s in der Arbeit?</p>
      </div>
      <div class="aufgabe">
        <article class="card box">
          <h3>Zielsetzung</h3>
          <p>
          Das Ziel ist die Neugestaltung der Website des Technologenverbands mit modernem, barrierefreiem Design, einfacher Navigation und flexibler Erweiterbarkeit. Geplant sind ein Webshop und ein anpassbares Anmeldeformular. Wichtig dabei ist eine kosteneffiziente, leicht wartbare WordPress-Lösung mit Elementor Pro. Darüber hinaus soll sie modular aufgebaut und flexibel erweiterbar sein.
          </p>
          <h3>Umfang</h3>
          <ul>
            <li>Designsystem (Farben, Typografie, Komponenten)</li>
            <li>Informationsarchitektur & Navigation</li>
            <li>Prototyping & Implementierung</li>
            <li>Webshop-Integration (z. B. WooCommerce)</li>
            <li>Datenbank-Integration</li>
            <li>Testing & Dokumentation</li>
          </ul>
        </article>
        <aside class="card box">
          <h3>Rahmen & Erfolgskriterien</h3>
          <ul>
            <li>Lighthouse Performance ≥ 90</li>
            <li>Modernes ansperchendes Layout/Design</li>
            <li>Konsistentes CI (Blau/ Grau/ Schwarz/ Weiß)</li>
            <li>Responsives Layout (Mobil → Desktop)</li>
            <li>Nachvollziehbare Fortschrittsdokumentation</li>
          </ul>
          <p style="margin-top:.8rem; color:var(--gray-400)">Letzte Aktualisierung: <span id="last-updated">–</span></p>
        </aside>
      </div>
    </div>
  </section>

  <!-- ====== TEAM ====== -->
  <section id="team">
    <div class="container">
      <div class="section-head">
        <h2>Teamvorstellung</h2>
        <p>Wer macht was?</p>
      </div>
      <div class="team-grid">
        <!-- Teammitglied 1 -->
        <div class="member card">
          <div style="display:flex; gap:1rem; align-items:center">
            <img class="avatar" src="Bilder/matteo.jpeg" alt="Avatar Matteo"/>
            <div>
              <h3>Matteo Mayer</h3>
              <div class="role">Frontend • Webshop</div>
              <span class="chip">#UI/UX</span>
            </div>
          </div>
        </div>
        <!-- Teammitglied 2 -->
        <div class="member card">
          <div style="display:flex; gap:1rem; align-items:center">
            <img class="avatar" src="Bilder/julian.jpeg" alt="Avatar Julian"/>
            <div>
              <h3>Julian Stoll</h3>
              <div class="role">Projektleitung • Datenbank</div>
              <span class="chip">#DB</span>
            </div>
          </div>
        </div>
        <!-- Teammitglied 3 -->
        <div class="member card">
          <div style="display:flex; gap:1rem; align-items:center">
            <img class="avatar" src="Bilder/jakob.jpeg" alt="Avatar Jakob"/>
            <div>
              <h3>Jakob Jeindl</h3>
              <div class="role">UI-Testing • Frontend</div>
              <span class="chip">#UI</span>
            </div>
          </div>
        </div>
        <!-- Teammitglied 4 -->
        <div class="member card">
          <div style="display:flex; gap:1rem; align-items:center">
            <img class="avatar" src="Bilder/georg.jpeg" alt="Avatar Georg"/>
            <div>
              <h3>Georg Sinakijevic</h3>
              <div class="role">UI/UX • Wireframing</div>
              <span class="chip">#UI/UX</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ====== FORTSCHRITT ====== -->
  <section id="fortschritt">
    <div class="container">
      <div class="section-head">
        <h2>Fortschrittsdokumentation</h2>
        <p>Status & Meilensteine</p>
      </div>
      <h3 style="margin:.6rem 0 1rem">Meilensteine</h3>
      <div class="milestones">
        <div class="milestone"><span class="ms-date">26.09.2025</span><div class="ms-title">Analyse der bestehenden Website & Anforderungen abgeschlossen</div></div>
        <div class="milestone"><span class="ms-date">08.10.2025</span><div class="ms-title">Machbarkeitsstudie abgeschlossen</div></div>
        <div class="milestone"><span class="ms-date">17.10.2025</span><div class="ms-title">Neues Designkonzept von Kooperationspartner abgenommen</div></div>
        <div class="milestone"><span class="ms-date">05.11.2025</span><div class="ms-title">Datenbank-Setup & technisches Grundgerüst eingerichtet</div></div>
        <div class="milestone"><span class="ms-date">26.11.2025</span><div class="ms-title">Usability Testing abgeschlossen & Feedback eingebunden</div></div>
        <div class="milestone"><span class="ms-date">17.12.2025</span><div class="ms-title">Designkonzept auf Wordpress umgesetzt</div></div>
        <div class="milestone"><span class="ms-date">09.01.2026</span><div class="ms-title">Webshop-Plugin & Career-Day Formular mit DB eingebunden</div></div>
        <div class="milestone"><span class="ms-date">24.01.2026</span><div class="ms-title">Inhalte überarbeitet & integriert</div></div>
        <div class="milestone"><span class="ms-date">13.02.2026</span><div class="ms-title">Technische Optimierung & Finalisierung der Website abgeschlossen</div></div>
        <div class="milestone"><span class="ms-date">07.04.2026</span><div class="ms-title">Diplomarbeitsabgabe / Übergabe Projekt</div></div>
      </div>
    </div>
  </section>

  <!-- ====== KONTAKT ====== -->
  <section id="kontakt">
    <div class="container">
      <div class="section-head">
        <h2>Kontakt</h2>
        <p>Schuladresse & Mail</p>
      </div>
      <div class="contact-card card">
        <div>
          <h3>Technologen Verband × TGM Wien</h3>
          <p style="color:var(--gray-200)">Ansprechperson: Julian Stoll</p>
          <p style="color:var(--gray-400)">Wexstraße 19–23, 1200 Wien (TGM)</p>
          <a class="mail" id="mail-link" href="mailto:jstoll@student.tgm.ac.at">✉ jstoll@student.tgm.ac.at</a>
        </div>
        
      </div>
    </div>
  </section>

  <footer>
    <div class="container">© <span id="year"></span> TGM Wien × Technologen Verband — Diplomarbeit</div>
  </footer>

  <script>
    // Mobile-Menü Toggle
    const btn = document.querySelector('.menu-btn');
    const menu = document.getElementById('menu');
    if(btn){
      btn.addEventListener('click', () => {
        const open = menu.classList.toggle('open');
        btn.setAttribute('aria-expanded', open ? 'true' : 'false');
      });
    }

    // Letzte Aktualisierung & Jahr
    const d = new Date();
    document.getElementById('last-updated').textContent = d.toLocaleDateString('de-AT');
    document.getElementById('year').textContent = d.getFullYear();

    // Fortschritt dynamisch setzen (optional):
    // Ändern Sie die Prozentzahl hier, um die Anzeige zu aktualisieren.
    const PROGRESS = 40; // TODO: Prozentwert anpassen
    const bar = document.getElementById('progress-bar');
    const label = document.getElementById('progress-label');
    if(bar && label){
      const val = Math.max(0, Math.min(100, PROGRESS));
      bar.style.width = val + '%';
      label.textContent = val + '%';
    }

    // Kontakt-Mail bequem ändern (einheitlich an einer Stelle):
    const MAIL = 'vorname.nachname@tgm.ac.at'; // TODO: ersetzen
    const mailLink = document.getElementById('mail-link');
    if(mailLink){
      mailLink.href = 'mailto:' + "jstoll@stuent.tgm.ac.at";
      mailLink.textContent = '✉ ' + "jstoll@student.tgm.ac.at";
    }
  </script>
</body>
</html>
