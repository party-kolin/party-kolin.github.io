<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
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

        /* KLÍČOVÉ OPRAVY PRO ŠÍŘKU */
        * {
            box-sizing: border-box; /* Všechny okraje se počítají dovnitř šířky */
        }

        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            max-width: 100vw;
            overflow-x: hidden; /* ABSOLUTNÍ ZÁKAZ POSUNU DO STRAN */
            position: relative;
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--text-dark);
            line-height: 1.5;
            background-color: #fff;
            scroll-behavior: smooth;
        }

        /* Navigace - Oprava přetékání na mobilu */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 15px;
        }

        nav img { height: 30px; max-width: 40%; object-fit: contain; }

        .nav-links { display: flex; gap: 8px; }
        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 0.6rem;
            text-transform: uppercase;
        }

        /* Hero - Zmenšení na mobilu */
        .hero {
            height: 50vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('uvod.jpg.JPG') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 50px;
            padding: 20px;
            width: 100%;
        }

        .hero h1 { font-size: clamp(1.5rem, 7vw, 3.5rem); margin: 0; }
        .hero h1 span { color: var(--primary-color); }

        /* Kontejner - Zajištění, že nepřeteče */
        .container { 
            width: 100%;
            max-width: 1100px; 
            margin: 0 auto; 
            padding: 40px 15px; 
        }

        .section-title { text-align: center; margin-bottom: 30px; }
        .divider { width: 40px; height: 3px; background: var(--primary-color); margin: 0 auto; }

        /* Mřížka karet - ČISTÝ JEDEN SLOUPEC NA MOBILU */
        .grid-fixed {
            display: block; /* Na mobilu dáváme blokové uspořádání */
            width: 100%;
        }

        .card {
            background: #fff;
            border-radius: 8px;
            border: 1px solid var(--border-color);
            margin-bottom: 20px; /* Mezera mezi kartami pod sebou */
            overflow: hidden;
            width: 100%;
        }

        .card-img { 
            width: 100%; 
            height: 180px; 
            background-size: cover; 
            background-position: center; 
        }

        .card-content { padding: 20px; }
        .card h3 { font-size: 1.1rem; margin: 5px 0; }
        .price { font-size: 1.4rem; font-weight: 700; margin: 10px 0; }
        
        .card-list { list-style: none; padding: 0; margin: 10px 0; font-size: 0.85rem; }
        .card-list li { margin-bottom: 4px; padding-left: 20px; position: relative; }
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
            font-size: 0.9rem;
        }

        /* DESKTOP ÚPRAVY */
        @media (min-width: 768px) {
            .grid-fixed {
                display: grid;
                grid-template-columns: repeat(2, 1fr);
                gap: 20px;
            }
            .nav-links { gap: 15px; }
            .nav-links a { font-size: 0.75rem; }
        }

        @media (min-width: 1024px) {
            .grid-fixed { grid-template-columns: repeat(3, 1fr); }
        }

        footer { background: #fafafa; padding: 40px 15px; text-align: center; border-top: 1px solid var(--border-color); }
        .contact-large { font-size: 1.1rem; font-weight: 700; display: block; margin: 10px 0; color: var(--text-dark); text-decoration: none; word-break: break-all; }
    </style>
</head>
<body>

    <nav>
        <img src="logo.jpg" alt="Party Kolín">
        <div class="nav-links">
            <a href="#vybaveni">Ceník</a>
            <a href="#galerie">Galerie</a>
            <a href="#kontakt">Kontakt</a>
        </div>
    </nav>

    <header class="hero">
        <h1>...s námi to <span>oslavíte</span>.</h1>
    </header>

    <section id="vybaveni" class="container">
        <div class="section-title">
            <h2>Vybavení & Ceník</h2>
            <div class="divider"></div>
        </div>

        <div class="grid-fixed">
            <div class="card">
                <div class="card-img" style="background-image: url('uvod.JPG');"></div>
                <div class="card-content">
                    <h3 style="color: var(--primary-color)">Párty stan 6 x 12 m</h3>
                    <ul class="card-list">
                        <li>Kapacita 50 až 80 osob</li>
                        <li>Robustní konstrukce</li>
                    </ul>
                    <div class="price">10 890 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
            <div class="card-img" style="background-image: url('nuzkový stan.png');"></div>
                <div class="card-content">
                    <h3>Nůžkový stan 3 x 6 m</h3>
                    <ul class="card-list">
                        <li>Kapacita cca 20 osob</li>
                        <li>Postavení do 5 minut</li>
                    </ul>
                    <div class="price">1 900 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('pivni-set1.png');"></div>
                <div class="card-content">
                    <h3>Pivní set 200 x 50 cm</h3>
                    <ul class="card-list">
                        <li>1x stůl + 2x lavice</li>
                        <li>Pro 6 až 8 osob</li>
                    </ul>
                    <div class="price">330 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrib1.jpg');"></div>
                <div class="card-content">
                    <h3>Plynový hřib (10kW)</h3>
                    <ul class="card-list">
                        <li>Bez náplně: 770 Kč</li>
                        <li>S náplní 10kg PB: 1550 Kč</li>
                    </ul>
                    <div class="price">od 770 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>
        </div>
    </section>

    <footer id="kontakt">
        <h2 style="font-size:1.2rem;">Chcete rezervovat?</h2>
        <a href="tel:+420723355740" class="contact-large">+420 723 355 740</a>
        <a href="tel:+420605717081" class="contact-large">+420 605 717 081</a>
        <p style="font-size: 0.9rem;">Kolín a široké okolí</p>
        <p style="font-size:0.7rem; color:#aaa; margin-top:20px;">&copy; 2026 Party-Kolin.cz</p>
    </footer>

</body>
</html>
