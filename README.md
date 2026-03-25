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
            --primary-color: #8cc63f; /* Vaše zelená z loga */
            --text-dark: #1a1a1a;
            --text-gray: #4a4a4a;
            --bg-light: #ffffff;
            --border-color: #f0f0f0;
        }

        body {
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 0;
            color: var(--text-dark);
            line-height: 1.6;
            background-color: #fff;
        }

        /* Navigace ve stylu Ringel */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 5%;
            box-sizing: border-box;
        }

        nav img { height: 45px; }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            margin-left: 25px;
            font-size: 0.9rem;
            transition: color 0.3s;
        }

        .nav-links a:hover { color: var(--primary-color); }

        /* Hero Sekce */
        .hero {
            height: 80vh;
            background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('uvod.jpg') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 65px;
        }

        .hero h1 {
            font-size: clamp(2rem, 5vw, 4rem);
            font-weight: 700;
            letter-spacing: -1px;
        }

        /* Sekce a Dlaždice (Styl čistých karet) */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 80px 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2rem;
            font-weight: 700;
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 3px;
            background-color: var(--primary-color);
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: #fff;
            padding: 40px;
            border-radius: 4px;
            border: 1px solid var(--border-color);
            text-decoration: none;
            color: inherit;
            transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
            text-align: center;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.05);
            border-color: var(--primary-color);
        }

        .card h3 {
            font-size: 1.25rem;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .card p {
            color: var(--text-gray);
            font-size: 0.95rem;
        }

        /* Footer */
        footer {
            background: #fafafa;
            border-top: 1px solid var(--border-color);
            padding: 60px 20px;
            text-align: center;
        }

        .footer-content { max-width: 600px; margin: 0 auto; }
        .footer-content p { margin: 10px 0; color: var(--text-gray); }
        .footer-contact { font-weight: 700; font-size: 1.2rem; margin: 20px 0; }

        @media (max-width: 768px) {
            .nav-links { display: none; } /* Na mobilu schováme menu pro jednoduchost */
            .grid { grid-template-columns: 1fr; }
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
        </div>
    </nav>

    <header class="hero">
        <h1>...s námi to <strong>oslavíte</strong>.</h1>
    </header>

    <div class="container" id="sluzby">
        <div class="section-title">
            <h2>Naše nabídka</h2>
        </div>

        <div class="grid">
            <a href="#vybaveni" class="card">
                <h3>Vybavení & Ceník</h3>
                <p>Párty stany, pivní sety a vytápění pro vaši akci.</p>
                <section id="vybaveni" class="container">
    <div class="section-title">
        <h2>Vybavení & Ceník</h2>
        <p>Kvalitní zázemí pro vaše soukromé i firemní akce.</p>
    </div>

    <div class="grid">
        <div class="card" style="border-top: 5px solid var(--primary-color);">
            <div style="font-size: 0.8rem; color: var(--primary-color); font-weight: 700; margin-bottom: 10px;">NEJOBLÍBENĚJŠÍ</div>
            <h3>Párty stan 6 x 12 m</h3>
            <p>Prostorný trubkový stan ideální pro větší oslavy a svatby.</p>
            
            <ul style="list-style: none; padding: 0; margin: 20px 0; text-align: left; font-size: 0.9rem;">
                <li>📏 <strong>Rozměry:</strong> 6 x 12 m</li>
                <li>↕️ <strong>Výška:</strong> boční 2m / hřeben 3m</li>
                <li>👥 <strong>Kapacita:</strong> 50 až 80 osob</li>
                <li>🛡️ <strong>Ochrana:</strong> UV záření, déšť i vítr</li>
            </ul>

            <div style="font-size: 1.5rem; font-weight: 700; color: var(--text-dark); margin: 20px 0;">
                10 890 Kč <span style="font-size: 0.9rem; font-weight: 400;">s DPH</span>
            </div>
            <p style="font-size: 0.8rem; font-style: italic;">Cena platí pro pronájem na 1 až 2 dny.</p>
            
            <a href="#kontakt" class="btn" style="display: inline-block; margin-top: 15px; background: var(--primary-color); color: white; padding: 10px 20px; text-decoration: none; border-radius: 4px; font-weight: 600;">POPTAT TERMÍN</a>
        </div>

        </div>
</section>
            </a>
            <a href="#galerie" class="card">
                <h3>Fotogalerie</h3>
                <p>Prohlédněte si naše realizace a skákací hrady.</p>
            </a>
            <a href="#faq" class="card">
                <h3>Časté dotazy</h3>
                <p>Vše, co potřebujete vědět o pronájmu a montáži.</p>
            </a>
            <a href="#sluzby-detail" class="card">
                <h3>Naše služby</h3>
                <p>Zajistíme dopravu, stavbu i demontáž vybavení.</p>
            </a>
            <a href="#podminky" class="card">
                <h3>Obchodní podmínky</h3>
                <p>Jasná pravidla pro bezproblémový průběh akce.</p>
            </a>
            <a href="#kontakt" class="card">
                <h3>Kontakty</h3>
                <p>Jsme tu pro vás v Kolíně a širokém okolí.</p>
            </a>
        </div>
    </div>

    <footer id="kontakt">
        <div class="footer-content">
            <h2>Party-Kolin.cz</h2>
            <p>Rádi Vám pomůžeme Váš slavnostní den zastřešit.</p>
            <div class="footer-contact">
                <a href="tel:+420123456789" style="text-decoration:none; color:inherit;">+420 123 456 789</a><br>
                <a href="mailto:info@party-kolin.cz" style="text-decoration:none; color:var(--primary-color);">info@party-kolin.cz</a>
            </div>
            <p>&copy; 2026 Všechna práva vyhrazena.</p>
        </div>
    </footer>

</body>
</html>
</body>
</html>
