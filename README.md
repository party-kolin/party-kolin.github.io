# party-kolin.github.io
<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Party Kolín | ...s námi to oslavíte</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        /* Definice zelené barvy z loga a základní styl */
        :root { --brand-green: #8cc63f; --dark: #222; --light-bg: #f9f9f9; }
        body { font-family: 'Open Sans', sans-serif; margin: 0; color: var(--dark); background-color: white; scroll-behavior: smooth; }
        h1, h2, h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; text-transform: uppercase; }

        /* Hlavní lišta s logem */
        .top-bar { background: white; padding: 10px 20px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); position: fixed; width: 100%; top: 0; z-index: 1000; box-sizing: border-box; display: flex; align-items: center; }
        .logo-img { height: 50px; width: auto; /* Zde se načte vaše logo */ }
        
        /* Úvodní velká fotka (Hero) */
        header { 
            height: 100vh; 
            margin-top: 70px; /* Prostor pro top-bar */
            /* !!! ZDE ZMĚŇTE NAZEV VAŠÍ FOTKY !!! */
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('uvod.jpg') no-repeat center center/cover; 
            display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; padding: 20px;
        }
        h1.hero-title { font-size: 4rem; margin: 0; text-shadow: 2px 2px 15px rgba(0,0,0,0.8); }
        h1.hero-title span { color: var(--brand-green); } /* Zelený akcent */

        /* Sekce dlaždic */
        section#menu-tiles { padding: 60px 20px; background-color: var(--light-bg); text-align: center; }
        
        .tile-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; max-width: 1200px; margin: 40px auto; }
        
        /* Styl jedné dlaždice */
        .tile { 
            background: white; padding: 40px 20px; border-radius: 10px; text-decoration: none; color: var(--dark);
            box-shadow: 0 4px 6px rgba(0,0,0,0.05); transition: all 0.3s ease; border: 2px solid transparent;
            display: flex; flex-direction: column; align-items: center; justify-content: center; height: 180px;
        }
        
        /* Efekt při najetí myší na dlaždici */
        .tile:hover { transform: translateY(-8px); box-shadow: 0 10px 20px rgba(140, 198, 63, 0.2); border-color: var(--brand-green); }
        
        .tile h3 { font-size: 1.3rem; margin: 10px 0 0 0; color: #111; }
        .tile-icon { font-size: 2.5rem; color: var(--brand-green); margin-bottom: 10px; }

        /* Patička s kontaktem */
        footer { background: var(--dark); color: #bbb; text-align: center; padding: 50px 20px; }
        footer h2 { color: white; }
        .contact-info { font-size: 1.2rem; color: white; margin: 20px 0; font-weight: 600; }
        .contact-info a { color: var(--brand-green); text-decoration: none; }

        /* Responsivita pro mobily */
        @media (max-width: 768px) { h1.hero-title { font-size: 2.5rem; } .tile-grid { grid-template-columns: 1fr; } }
    </style>
</head>
<body>

    <div class="top-bar">
        <img src="logo.png" alt="Party Kolín Logo" class="logo-img">
    </div>

    <header>
        <h1 class="hero-title">...s námi to <span>oslavíte</span>.</h1>
    </header>

    <section id="menu-tiles">
        <h2>Vyberte si službu</h2>
        <div class="tile-grid">
            
            <a href="#vybaveni" class="tile">
                <div class="tile-icon">⛺</div> <h3>Vybavení (ceník)</h3>
            </a>

            <a href="#galerie" class="tile">
                <div class="tile-icon">📷</div> <h3>Fotogalerie</h3>
            </a>

            <a href="#faq" class="tile">
                <div class="tile-icon">❓</div> <h3>Časté dotazy</h3>
            </a>

            <a href="#sluzby" class="tile">
                <div class="tile-icon">🤝</div> <h3>Naše služby</h3>
            </a>

            <a href="#podminky" class="tile">
                <div class="tile-icon">📄</div> <h3>Obchodní podmínky</h3>
            </a>

            <a href="#kontakt" class="tile">
                <div class="tile-icon">📞</div> <h3>Kontakty</h3>
            </a>

        </div>
    </section>

    <section id="vybaveni" style="padding:100px 20px; text-align:center;"><h2>Zde bude Ceník Vybavení</h2></section>
    <section id="galerie" style="padding:100px 20px; text-align:center; background:#eee;"><h2>Zde bude Fotogalerie</h2></section>

    <footer id="kontakt">
        <h2>Kontaktujte nás</h2>
        <p>Pro nezávaznou poptávku nám zavolejte nebo napište.</p>
        <div class="contact-info">
            📧 <a href="mailto:info@party-kolin.cz">info@party-kolin.cz</a><br>
            📞 <a href="tel:+420123456789">+420 123 456 789</a>
        </div>
        <p>&copy; 2026 www.party-kolin.cz | Kolín a okolí</p>
    </footer>

</body>
</html>
