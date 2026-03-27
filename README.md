<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Party Kolín | ...s námi to oslavíte</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #8cc63f;
            --text-dark: #1a1a1a;
            --text-gray: #4a4a4a;
            --bg-light: #fdfdfd;
            --border-color: #f0f0f0;
        }

        body {
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 0;
            color: var(--text-dark);
            line-height: 1.5;
            background-color: #fff;
            scroll-behavior: smooth;
            overflow-x: hidden; /* Zabrání vodorovnému posunu */
        }

        /* Navigace */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 5%;
            box-sizing: border-box;
        }

        nav img { height: 35px; }

        .nav-links { display: flex; gap: 12px; }
        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 0.65rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Hero Sekce */
        .hero {
            height: 60vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('uvod.jpg.JPG') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 55px;
            padding: 0 20px;
        }

        .hero h1 { font-size: clamp(1.8rem, 8vw, 4rem); font-weight: 700; margin: 0; }
        .hero h1 span { color: var(--primary-color); }

        /* Kontejner */
        .container { max-width: 1100px; margin: 0 auto; padding: 60px 20px; box-sizing: border-box; }
        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 1.8rem; margin-bottom: 10px; }
        .divider { width: 50px; height: 3px; background: var(--primary-color); margin: 0 auto; }

        /* Grid a Karty - OPRAVENO PRO MOBIL */
        .grid-fixed {
            display: grid;
            grid-template-columns: 1fr; /* Default: jeden sloupec pro mobil */
            gap: 25px;
            width: 100%;
        }

        @media (min-width: 768px) {
            .grid-fixed { grid-template-columns: repeat(2, 1fr); }
        }

        @media (min-width: 1100px) {
            .grid-fixed { grid-template-columns: repeat(3, 1fr); }
        }

        .card {
            background: #fff;
            border-radius: 8px;
            border: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
            overflow: hidden;
            transition: transform 0.3s ease;
            width: 100%;
            box-sizing: border-box;
        }

        .card:hover { transform: translateY(-5px); border-color: var(--primary-color); }
        .card-img { width: 100%; height: 200px; background-size: cover; background-position: center; }
        .card-content { padding: 25px; flex-grow: 1; display: flex; flex-direction: column; }
        
        .card h3 { font-size: 1.2rem; margin: 10px 0; }
        .price { font-size: 1.6rem; font-weight: 700; margin: 15px 0; }
        .price span { font-size: 0.8rem; font-weight: 400; color: var(--text-gray); }

        .card-list { list-style: none; padding: 0; margin: 15px 0; font-size: 0.9rem; flex-grow: 1; }
        .card-list li { margin-bottom: 6px; padding-left: 20px; position: relative; }
        .card-list li::before { content: "✓"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: block;
            background: var(--primary-color);
            color: white;
            padding: 12px;
            text-decoration: none;
            border-radius: 4px;
            font-weight: 600;
            text-align: center;
        }

        footer { background: #fafafa; border-top: 1px solid var(--border-color); padding: 60px 20px; text-align: center; }
        .contact-large { font-size: 1.3rem; font-weight: 700; margin: 15px 0; display: block; text-decoration: none; color: var(--text-dark); }

        /* Mobilní úpravy menu */
        @media (max-width: 600px) {
            nav { flex-direction: column; padding: 10px; height: auto; }
            .nav-links { flex-wrap: wrap; justify-content: center; margin-top: 10px; gap: 8px; }
            .hero { margin-top: 90px; height: 45vh; }
        }
    </style>
</head>
<body>

    <nav>
        <img src="logo.jpg" alt="Party Kolín">
        <div class="nav-links">
            <a href="#sluzby">Služby</a>
            <a href="#vybaveni">Ceník</a>
            <a href="#galerie">Galerie</a>
            <a href="#kontakt">Kontakt</a>
            <a href="#podminky">Podmínky</a>
        </div>
    </nav>

    <header class="hero">
        <h1>...s námi to <span>oslavíte</span>.</h1>
    </header>

    <section id="sluzby" class="container">
        <div class="section-title">
            <h2>Naše Služby</h2>
            <div class="divider"></div>
        </div>
        <p style="text-align: center; max-width: 800px; margin: 0 auto; color: var(--text-gray);">
            Nabízíme pronájem párty stanů a skákacích hradů pro vaše oslavy, svatby či výročí. 
            Rádi vám pomůžeme váš den zastřešit a ochránit hosty před deštěm, sluncem či větrem.
        </p>
    </section>

    <section id="vybaveni" style="background: var(--bg-light); padding: 20px 0 60px 0;">
        <div class="container">
            <div class="section-title">
                <h2>Vybavení & Ceník</h2>
                <div class="divider"></div>
            </div>

            <div class="grid-fixed">
                <div class="card">
                    <div class="card-img" style="background-image: url('image_2.png');"></div>
                    <div class="card-content">
                        <div style="color: var(--primary-color); font-weight:700; font-size:0.7rem; text-transform:uppercase;">Hlavní nabídka</div>
                        <h3>Párty stan 6 x 12 m</h3>
                        <ul class="card-list">
                            <li>Kapacita 50 až 80 osob</li>
                            <li>Výška boční 2m / hřeben 3m</li>
                            <li>Robustní trubková konstrukce</li>
                        </ul>
                        <div class="price">10 890 Kč <span>s DPH</span></div>
                        <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-content">
                        <div style="color: var(--text-gray); font-weight:700; font-size:0.7rem; text-transform:uppercase;">Rychlé řešení</div>
                        <h3>Nůžkový stan 3 x 6 m</h3>
                        <ul class="card-list">
                            <li>Kapacita cca 20 osob</li>
                            <li>Postavení do 5 minut</li>
                            <li>3x bok, 1x otevřená strana</li>
                        </ul>
                        <div class="price">1 900 Kč <span>s DPH</span></div>
                        <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img" style="background-image: url('Pivni set.jpg');"></div>
                    <div class="card-content">
                        <div style="color: var(--text-gray); font-weight:700; font-size:0.7rem; text-transform:uppercase;">Posezení</div>
                        <h3>Pivní set 200 x 50 cm</h3>
                        <ul class="card-list">
                            <li>Sestava: 1x stůl + 2x lavice</li>
                            <li>Kapacita 6 až 8 osob</li>
                            <li>Stabilní dřevěné provedení</li>
                        </ul>
                        <div class="price">330 Kč <span>s DPH</span></div>
                        <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img" style="background-image: url('hrib.jpg');"></div>
                    <div class="card-content">
                        <div style="color: var(--text-gray); font-weight:700; font-size:0.75rem; text-transform:uppercase;">Pohodlí</div>
                        <h3>Vytápění (plynový hřib)</h3>
                        <ul class="card-list">
                            <li>Výkon 10kW, až 13h provozu</li>
                            <li>Bez náplně: <strong>770 Kč</strong></li>
                            <li>S náplní 10kg PB: <strong>1550 Kč</strong></li>
                        </ul>
                        <div class="price" style="margin-top:auto;">od 770 Kč <span>s DPH</span></div>
                        <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="galerie" class="container">
        <div class="section-title">
            <h2>Fotogalerie</h2>
            <div class="divider"></div>
        </div>
        <p style="text-align: center; color: var(--text-gray);">Připravujeme pro vás ukázky našich realizací.</p>
    </section>

    <footer id="kontakt">
        <div class="container" style="padding: 0;">
            <h2 style="font-size:1.4rem;">Chcete rezervovat?</h2>
            <a href="tel:+420723355740" class="contact-large">+420 723 355 740</a>
            <a href="tel:+420605717081" class="contact-large">+420 605 717 081</a>
            <p>Kolín a široké okolí</p>
            <p style="font-size:0.8rem; color:#aaa; margin-top:30px;">&copy; 2026 Party-Kolin.cz</p>
        </div>
    </footer>

</body>
</html>
