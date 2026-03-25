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
        }

        /* Navigace - Responzivní */
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

        nav img { height: 35px; } /* Trochu menší logo pro víc místa */

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            margin-left: 15px;
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Hero Sekce - Lepší pro mobil */
        .hero {
            height: 60vh; /* Menší na mobilu */
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('uvod.jpg') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 55px;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: clamp(1.8rem, 8vw, 4rem);
            font-weight: 700;
            margin: 0;
            line-height: 1.1;
        }

        .hero h1 span { color: var(--primary-color); }

        /* Kontejner */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 40px 15px; /* Menší padding na mobilu */
        }

        .section-title {
            text-align: center;
            margin-bottom: 30px;
        }

        .section-title h2 {
            font-size: clamp(1.5rem, 5vw, 2.2rem);
            margin-bottom: 10px;
        }

        .section-title .divider {
            width: 50px;
            height: 3px;
            background: var(--primary-color);
            margin: 0 auto;
        }

        /* Grid a Karty - Optimalizováno */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .card {
            background: #fff;
            padding: 25px; /* Menší padding na mobilu */
            border-radius: 8px;
            border: 1px solid var(--border-color);
            text-align: center;
            display: flex;
            flex-direction: column;
            transition: transform 0.3s ease;
        }

        .card:hover {
            border-color: var(--primary-color);
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
        }

        .card h3 { font-size: 1.2rem; margin: 10px 0; }
        .card .price { font-size: 1.6rem; font-weight: 700; margin: 15px 0; color: var(--text-dark); }
        .card .price span { font-size: 0.85rem; font-weight: 400; color: var(--text-gray); }

        .card-list {
            list-style: none;
            padding: 0;
            margin: 15px 0;
            text-align: left;
            font-size: 0.9rem;
            flex-grow: 1;
        }

        .card-list li { margin-bottom: 6px; padding-left: 20px; position: relative; }
        .card-list li::before { content: "✓"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 12px 20px;
            text-decoration: none;
            border-radius: 4px;
            font-weight: 600;
            font-size: 0.9rem;
        }

        /* Footer */
        footer {
            background: #fafafa;
            border-top: 1px solid var(--border-color);
            padding: 40px 20px;
            text-align: center;
        }

        .contact-large { font-size: 1.4rem; font-weight: 700; margin: 15px 0; display: block; text-decoration: none; color: var(--text-dark); }

        /* Skrytí navigace na velmi malých mobilech pro čistotu */
        @media (max-width: 400px) {
            .nav-links { display: none; }
            nav { justify-content: center; }
        }

        /* Úprava pro desktop */
        @media (min-width: 768px) {
            .container { padding: 80px 20px; }
            .hero { height: 75vh; }
            .nav-links a { font-size: 0.85rem; margin-left: 25px; }
            .card { padding: 40px; }
        }
    </style>
</head>
<body>

    <nav>
        <img src="logo.png" alt="Party Kolín">
        <div class="nav-links">
            <a href="#vybaveni">Ceník</a>
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
        </div>

        <div class="grid">
            <div class="card">
                <div style="color: var(--primary-color); font-weight:700; font-size:0.7rem; text-transform:uppercase;">Hlavní nabídka</div>
                <h3>Párty stan 6 x 12 m</h3>
                <ul class="card-list">
                    <li>Kapacita 50 až 80 osob</li>
                    <li>Výška boční 2m / hřeben 3m</li>
                    <li>Robustní konstrukce</li>
                    <li>Odolná plachta</li>
                </ul>
                <div class="price">10 890 Kč <span>s DPH</span></div>
                <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
            </div>

            <div class="card">
                <div style="color: var(--text-gray); font-weight:700; font-size:0.7rem; text-transform:uppercase;">Rychlé řešení</div>
                <h3>Nůžkový stan 3 x 6 m</h3>
                <ul class="card-list">
                    <li>Kapacita cca 20 osob</li>
                    <li>Postavení do 5 minut</li>
                    <li>Stabilní konstrukce</li>
                    <li>3x bok, 1x otevřená strana</li>
                </ul>
                <div class="price">1 900 Kč <span>s DPH</span></div>
                <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
            </div>

            <div class="card">
                <div style="color: var(--text-gray); font-weight:700; font-size:0.7rem; text-transform:uppercase;">Doplňky</div>
                <h3>Pivní set 200 x 50 cm</h3>
                <ul class="card-list">
                    <li>Sestava: 1x stůl + 2x lavice</li>
                    <li>Kapacita 6 až 8 osob</li>
                    <li>Samostatně od 4ks</li>
                    <li>Nebo v setu se stanem</li>
                </ul>
                <div class="price">330 Kč <span>s DPH</span></div>
                <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
            </div>
        </div>
    </div>

    <div id="sluzby" style="background: var(--bg-light); padding: 60px 0;">
        <div class="container" style="text-align:center;">
            <h2>Naše Služby</h2>
            <div class="divider" style="margin-bottom:20px;"></div>
            <p style="max-width: 700px; margin: 0 auto; color: var(--text-gray); font-size: 0.95rem;">
                Nabízíme pronájem stanů a dětských skákacích hradů pro soukromé akce. 
                Rádi Vám pomůžeme Váš den zastřešit před deštěm i sluncem.
            </p>
        </div>
    </div>

    <footer id="kontakt">
        <div class="container" style="padding: 0;">
            <h2 style="font-size:1.4rem;">Chcete rezervovat?</h2>
            <a href="tel:+420123456789" class="contact-large">+420 123 456 789</a>
            <p>Kolín a široké okolí</p>
            <p style="font-size:0.8rem; color:#aaa; margin-top:30px;">&copy; 2026 Party-Kolin.cz</p>
        </div>
    </footer>

</body>
</html>
