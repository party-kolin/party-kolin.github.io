# party-kolin.github.io
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
            line-height: 1.6;
            background-color: #fff;
            scroll-behavior: smooth;
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
            padding: 12px 5%;
            box-sizing: border-box;
        }

        nav img { height: 45px; }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            margin-left: 25px;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: color 0.3s;
        }

        .nav-links a:hover { color: var(--primary-color); }

        /* Hero Sekce */
        .hero {
            height: 75vh;
            background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('uvod.jpg') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 60px;
        }

        .hero h1 {
            font-size: clamp(2rem, 6vw, 4.5rem);
            font-weight: 700;
            margin: 0;
            letter-spacing: -2px;
        }

        .hero h1 span { color: var(--primary-color); }

        /* Kontejner */
        .container {
            max-width: 1140px;
            margin: 0 auto;
            padding: 80px 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.2rem;
            margin-bottom: 15px;
        }

        .section-title .divider {
            width: 60px;
            height: 3px;
            background: var(--primary-color);
            margin: 0 auto;
        }

        /* Grid a Karty */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: #fff;
            padding: 40px;
            border-radius: 6px;
            border: 1px solid var(--border-color);
            text-align: center;
            display: flex;
            flex-direction: column;
            transition: all 0.4s ease;
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.06);
            border-color: var(--primary-color);
        }

        .card h3 { font-size: 1.4rem; margin-bottom: 10px; }
        .card .price { font-size: 1.8rem; font-weight: 700; margin: 20px 0; color: var(--text-dark); }
        .card .price span { font-size: 0.9rem; font-weight: 400; color: var(--text-gray); }

        .card-list {
            list-style: none;
            padding: 0;
            margin: 20px 0;
            text-align: left;
            font-size: 0.95rem;
            flex-grow: 1;
        }

        .card-list li { margin-bottom: 8px; padding-left: 20px; position: relative; }
        .card-list li::before { content: "•"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 14px 28px;
            text-decoration: none;
            border-radius: 4px;
            font-weight: 600;
            transition: background 0.3s;
        }

        .btn-main:hover { background: #7ab332; }

        /* Footer */
        footer {
            background: #fafafa;
            border-top: 1px solid var(--border-color);
            padding: 80px 20px;
            text-align: center;
        }

        .contact-large { font-size: 1.8rem; font-weight: 700; margin: 25px 0; display: block; text-decoration: none; color: var(--text-dark); }
        .contact-large:hover { color: var(--primary-color); }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero h1 { font-size: 2.5rem; }
        }
    </style>
</head>
<body>

    <nav>
        <img src="logo.jpg" alt="Party Kolín">
        <div class="nav-links">
            <a href="#vybaveni">Ceník</a>
            <a href="#sluzby">Služby</a>
            <a href="#faq">Dotazy</a>
            <a href="#kontakt">Kontakt</a>
        </div>
    </nav>

    <header class="hero">
        <h1>...s námi to <span>oslavíte</span>.</h1>
    </header>

    <div class="container" id="vybaveni">
        <div class="section-title">
            <h2>Vybavení & Ceník</h2>
            <div class="divider"></div>
            <p style="margin-top:20px; color: var(--text-gray);">Kvalitní zázemí pro vaše soukromé i firemní akce.</p>
        </div>

        <div class="grid">
            <div class="card">
                <span style="color: var(--primary-color); font-weight:700; font-size:0.75rem; letter-spacing:1px;">PRO VELKÉ OSLAVY</span>
                <h3>Párty stan 6 x 12 m</h3>
                <ul class="card-list">
                    <li>Kapacita 50 až 80 osob</li>
                    <li>Výška boční stěny 2m / hřeben 3m</li>
                    <li>Robustní trubková konstrukce</li>
                    <li>Odolná plachta proti dešti a větru</li>
                </ul>
                <div class="price">10 890 Kč <span>s DPH</span></div>
                <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
            </div>

            <div class="card">
                <span style="color: var(--text-gray); font-weight:700; font-size:0.75rem; letter-spacing:1px;">RYCHLÉ ZASTŘEŠENÍ</span>
                <h3>Nůžkový stan 3 x 6 m</h3>
                <ul class="card-list">
                    <li>Kapacita cca 20 osob</li>
                    <li>Postavení do 5 minut</li>
                    <li>Stabilní konstrukce</li>
                    <li>3x boční stěna, 1x otevřená</li>
                </ul>
                <div class="price">1 900 Kč <span>s DPH</span></div>
                <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
            </div>

            <div class="card">
                <span style="color: var(--text-gray); font-weight:700; font-size:0.75rem; letter-spacing:1px;">POSEZENÍ</span>
                <h3>Pivní set 200 x 50 cm</h3>
                <ul class="card-list">
                    <li>Sestava: 1x stůl + 2x lavice</li>
                    <li>Kapacita 6 až 8 osob na set</li>
                    <li>Stabilní provedení</li>
                    <li>Samostatně od 4ks (nebo se stanem)</li>
                </ul>
                <div class="price">330 Kč <span>s DPH</span></div>
                <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
            </div>
        </div>
    </div>

    <div id="sluzby" style="background: var(--bg-light);">
        <div class="container">
            <div class="section-title">
                <h2>Naše Služby</h2>
                <div class="divider"></div>
            </div>
            <p style="text-align: center; max-width: 800px; margin: 0 auto; color: var(--text-gray);">
                Nabízíme pronájem párty stanů a dětských skákacích hradů pro menší soukromé akce. 
                Rádi Vám pomůžeme Váš slavnostní den zastřešit a ochránit hosty před deštěm, sluncem či větrem.Nabízíme pronájem párty stanů, dětských skákacích hradů pro menší soukromé akce typu svatba, výročí, narozeninová oslava apod.

Počasí je někdy neúprosné a mnohdy dokáže zkazit vysněný a dlouho plánovaný slavnostní den. Rádi Vám pomůžeme Váš slavnostní den zastřešit. Naše párty stany pomohou hosty schovat před deštěm, přímým sluncem či větrem. Nabízíme pronájem stanů 6x12m (trubkový) a 6x3m (nůžkový), posezení (pivní sety), vytápění a také skákací dětské hrady
            </p>
        </div>
    </div>

    <footer id="kontakt">
        <div class="container" style="padding: 0;">
            <h2>Máte dotaz nebo chcete rezervovat?</h2>
            <p>Působíme v Kolíně a širokém okolí.</p>
            <a href="tel:+420 723 355 740" class="contact-large">+420 723 355 740</a>
            <a href="mailto:info@party-kolin.cz" style="color: var(--primary-color); text-decoration: none; font-weight: 600;">info@party-kolin.cz</a>
            <div style="margin-top: 50px; font-size: 0.8rem; color: #aaa;">
                &copy; 2026 Party-Kolin.cz | Kolín
            </div>
        </div>
    </footer>

</body>
</html>>
