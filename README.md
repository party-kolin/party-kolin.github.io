# party-kolin.github.io
<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Party Kolín | Pronájem stanů a skákacích hradů</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root { --primary: #007bff; --accent: #ff8800; --dark: #333; --light: #f4f7f6; }
        body { font-family: 'Open Sans', sans-serif; margin: 0; color: var(--dark); background-color: white; scroll-behavior: smooth; }
        h1, h2, h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; }

        /* Hero sekce s textem od vás */
        header { 
            height: 80vh; 
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1533174072545-7a4b6ad7a6c3?auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover; 
            display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px;
        }
        h1 { font-size: 3.5rem; margin: 0; text-transform: uppercase; }
        .hero-text { max-width: 800px; font-size: 1.2rem; margin: 20px 0; }

        .btn { padding: 15px 35px; background: var(--accent); color: white; text-decoration: none; font-weight: bold; border-radius: 5px; transition: 0.3s; font-size: 1.1rem; }
        .btn:hover { background: #e67a00; transform: translateY(-3px); box-shadow: 0 5px 15px rgba(0,0,0,0.3); }

        /* Sekce Vybavení */
        section { padding: 80px 20px; max-width: 1100px; margin: auto; }
        .section-title { text-align: center; margin-bottom: 50px; }
        .section-title h2 { font-size: 2.5rem; color: var(--primary); }

        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .card { background: var(--light); padding: 30px; border-radius: 10px; text-align: center; border-bottom: 5px solid var(--primary); transition: 0.3s; }
        .card:hover { transform: translateY(-10px); background: #fff; box-shadow: 0 10px 30px rgba(0,0,0,0.1); }
        .card h3 { color: var(--primary); margin-top: 0; }
        .card ul { list-style: none; padding: 0; text-align: left; }
        .card li::before { content: "✓ "; color: var(--accent); font-weight: bold; }

        /* O nás sekce (Váš text) */
        .about-box { background: var(--primary); color: white; padding: 50px; border-radius: 20px; text-align: center; margin-top: 50px; }

        footer { background: #222; color: #ccc; text-align: center; padding: 50px 20px; margin-top: 50px; }
        .contact-info { font-size: 1.2rem; color: white; margin: 20px 0; }
    </style>
</head>
<body>

    <header>
        <h1>PARTY KOLÍN</h1>
        <p class="hero-text">Zajistíme, aby váš slavnostní den nic nepokazilo. Nabízíme pronájem párty stanů a skákacích hradů pro vaše nezapomenutelné oslavy.</p>
        <a href="#kontakt" class="btn">POPTAT TERMÍN ZDARMA</a>
    </header>

    <section id="vybaveni">
        <div class="section-title">
            <h2>Naše Vybavení</h2>
            <p>Vše pro vaši svatbu, výročí nebo narozeninovou oslavu.</p>
        </div>
        
        <div class="grid">
            <div class="card">
                <h3>Párty Stany</h3>
                <ul>
                    <li><strong>6x12m</strong> – Robustní trubkový stan</li>
                    <li><strong>6x3m</strong> – Rychlý nůžkový stan</li>
                    <li>Ochrana před deštěm, sluncem i větrem</li>
                </ul>
            </div>
            <div class="card">
                <h3>Zábava pro děti</h3>
                <ul>
                    <li><strong>Skákací hrady</strong></li>
                    <li>Ideální pro rodinné oslavy</li>
                    <li>Bezpečný a prověřený materiál</li>
                </ul>
            </div>
            <div class="card">
                <h3>Doplňky</h3>
                <ul>
                    <li>Pivní sety (posezení)</li>
                    <li>Výkonné vytápění stanů</li>
                    <li>Kompletní zastřešení akce</li>
                </ul>
            </div>
        </div>
    </section>

    <section>
        <div class="about-box">
            <h2>Proč my?</h2>
            <p>"Počasí je někdy neúprosné a mnohdy dokáže zkazit vysněný a dlouho plánovaný slavnostní den. Rádi Vám pomůžeme Váš slavnostní den zastřešit."</p>
        </div>
    </section>

    <footer id="kontakt">
        <h2>Kontaktujte nás</h2>
        <div class="contact-info">
            📧 info@party-kolin.cz | 📞 +420 123 456 789
        </div>
        <p>Působíme v Kolíně a širokém okolí.</p>
        <hr style="width: 50px; border: 1px solid var(--accent); margin: 30px auto;">
        <p>&copy; 2026 www.party-kolin.cz | Vytvořeno zdarma s AI</p>
    </footer>

</body>
</html>
