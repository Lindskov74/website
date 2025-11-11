# website
Min Hjemmeside

<!DOCTYPE html>
<html lang="da">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Meditation</title>
  <meta name="description" content="Stilhed. Nærvær. Et roligt øjeblik." />

  <style>
    /* ===== Baseline ===== */
    :root{
      --bg: #0b0f14;
      --ink: #e8edf2;
      --muted: #b7c2cd;
      --card: #121821;
      --accent: #93c5fd;
      --ring: #2a3441;
      --radius: 16px;
      --maxw: 980px;
    }
    *{ box-sizing: border-box; }
    html,body{ height:100%; }
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial;
      color: var(--ink);
      background: linear-gradient(180deg, #0b0f14 0%, #0f1520 100%);
      line-height:1.6;
    }
    a{ color: inherit; text-decoration: none; }
    img{ max-width:100%; display:block; }

    /* ===== Header ===== */
    header{
      position: sticky; top:0; z-index:10;
      backdrop-filter: blur(10px);
      background: color-mix(in oklab, var(--bg) 75%, transparent);
      border-bottom: 1px solid var(--ring);
    }
    .nav{
      max-width: var(--maxw); margin: 0 auto; padding: 12px 20px;
      display: flex; align-items:center; justify-content: space-between;
    }
    .brand{ font-weight:600; letter-spacing:.4px; }
    .nav a.btn{
      padding:10px 14px; border:1px solid var(--ring); border-radius: 999px;
    }
    .nav a.btn:hover{ border-color: var(--accent); }

    /* ===== Hero ===== */
    .hero{
      position: relative; min-height: 78vh;
      display:grid; place-items:center; text-align:center; overflow:hidden;
      border-bottom: 1px solid var(--ring);
    }
    .hero-media{
      position:absolute; inset:0; pointer-events:none; overflow:hidden;
    }
    .hero-media::before{
      content:"";
      position:absolute; inset:-4rem;
      background:
        radial-gradient(80% 60% at 50% 20%, rgba(147,197,253,.35) 0%, transparent 60%),
        linear-gradient(180deg, rgba(11,15,20,.2), rgba(11,15,20,.75));
      z-index:1;
    }
    .hero-media img{
      width:100%; height:100%; object-fit: cover; filter: saturate(1.05) contrast(1.05) brightness(.9);
      transform: scale(1.02);
    }
    .hero-inner{ position:relative; z-index:2; padding: 80px 20px; }
    .kicker{
      display:inline-block; padding:6px 12px; border:1px solid var(--ring); border-radius: 999px;
      color: var(--muted); font-size: .9rem; letter-spacing:.3px;
      background: color-mix(in oklab, var(--card) 70%, transparent);
    }
    h1{
      margin:18px auto 10px; max-width: 16ch;
      font-size: clamp(34px, 6vw, 52px); line-height:1.1; font-weight:700;
    }
    .sub{
      margin: 0 auto 26px; max-width: 48ch; color: var(--muted);
      font-size: clamp(16px, 2.5vw, 18px);
    }
    .cta{
      display:inline-flex; gap:10px; align-items:center; justify-content:center;
      padding:12px 18px; border-radius: 999px; background: var(--ink); color:#0b0f14;
      font-weight:600;
    }
    .cta:hover{ transform: translateY(-1px); }
    .ghost{
      display:inline-flex; gap:8px; align-items:center; justify-content:center;
      padding:12px 18px; margin-left:8px; border-radius: 999px; border:1px solid var(--ring);
      color: var(--ink);
    }
    .ghost:hover{ border-color: var(--accent); }

    /* ===== Content ===== */
    .section{
      max-width: var(--maxw); margin: 60px auto; padding: 0 20px;
      display:grid; gap: 22px;
    }
    .card{
      background: color-mix(in oklab, var(--card) 90%, transparent);
      border:1px solid var(--ring); border-radius: var(--radius);
      padding: 22px;
    }
    .grid{
      display:grid; gap: 16px;
      grid-template-columns: repeat(12, 1fr);
    }
    .grid > .card{ grid-column: span 12; }
    @media (min-width: 800px){
      .grid > .card.span-4{ grid-column: span 4; }
      .grid > .card.span-8{ grid-column: span 8; }
    }
    .muted{ color: var(--muted); }

    /* ===== Footer ===== */
    footer{
      border-top:1px solid var(--ring); padding: 24px 20px; color: var(--muted);
      text-align:center; margin-top: 60px;
    }
  </style>
</head>
<body>
  <header>
    <nav class="nav" aria-label="Primær">
      <div class="brand">Nærvær</div>
      <a class="btn" href="#kontakt">Kontakt</a>
    </nav>
  </header>

  <main>
    <!-- Hero med meditationsbillede -->
    <section class="hero" aria-label="Forside">
      <div class="hero-media" aria-hidden="true">
        <!-- Læg dit eget billede i repoet som /images/meditation.jpg -->
        <img src="images/meditation.jpg" alt="" />
      </div>
      <div class="hero-inner">
        <span class="kicker">Stilhed i bevægelse</span>
        <h1>Meditation der lander skuldrene</h1>
        <p class="sub">Små guidede pauser, der hjælper dig tilbage i kroppen—enkelt, roligt og uden præstation.</p>
        <a class="cta" href="#sessioner">Prøv en session</a>
        <a class="ghost" href="#om">Læs mere</a>
      </div>
    </section>

    <!-- Indhold -->
    <section id="sessioner" class="section">
      <div class="grid">
        <article class="card span-8">
          <h2>Hvad du kan forvente</h2>
          <p class="muted">Rolige åndedrætsøvelser, blid kropsscanning og korte stilheder. Velegnet til begyndere.</p>
          <ul>
            <li>10–15 min korte pauser</li>
            <li>Afspænding for nakke/skuldre</li>
            <li>Ingen app eller login</li>
          </ul>
        </article>
        <aside class="card span-4">
          <h3>Næste skridt</h3>
          <p class="muted">Start med en gratis prøve-session. Ingen tilmelding.</p>
          <a class="cta" href="#kontakt">Book et kald</a>
        </aside>
      </div>
    </section>

    <section id="om" class="section">
      <div class="card">
        <h2>Om</h2>
        <p class="muted">Et enkelt sted på nettet til pauser, der faktisk føles som pauser. Hold tempoet nede, og vend tilbage når du har brug for det.</p>
      </div>
    </section>

    <section id="kontakt" class="section">
      <div class="card">
        <h2>Kontakt</h2>
        <p class="muted">Skriv en mail til <a href="mailto:kontakt@example.com">kontakt@example.com</a> — eller skift til dit eget kontaktlink.</p>
      </div>
    </section>
  </main>

  <footer>© <span id="y"></span> Nærvær</footer>

  <script>
    // Lidt hygge: opdater årstal automatisk
    document.getElementById("y").textContent = new Date().getFullYear();
  </script>
</body>
</html>

