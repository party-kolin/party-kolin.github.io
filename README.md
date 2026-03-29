<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    
    <title>Party Kolín | Půjčovna párty stanů, skákacích hradů a vybavení</title>
    <meta name="description" content="Půjčovna vybavení pro vaši oslavu v Kolíně a okolí. Nabízíme párty stany 6x12m a 3x6m, skákací hrady, pivní sety s luxusními povlaky, plynové hřiby, rautové a barové stoly. Kompletní servis včetně montáže a dopravy.">
    <meta name="keywords" content="půjčovna stanů Kolín, párty stan 6x12, nůžkový stan, skákací hrad Kolín, pivní sety, plynový hřib, rautové stoly, barové stolky, oslavy Kolín, svatba venku">
    <meta name="author" content="Miloš Hulinko">

    <meta property="og:title" content="Party Kolín | ...s námi to oslavíte">
    <meta property="og:description" content="Vše pro vaši párty na jednom místě. Stany, hrady, posezení i topení v Kolíně a okolí.">
    <meta property="og:image" content="logo.jpg">
    <meta property="og:type" content="website">

    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #8cc63f;
            --text-dark: #1a1a1a;
            --text-gray: #4a4a4a;
            --bg-light: #fdfdfd;
            --border-color: #f0f0f0;
        }

        * { box-sizing: border-box; }

        html, body {
            margin: 0; padding: 0; width: 100%; max-width: 100vw;
            overflow-x: hidden; position: relative;
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--text-dark);
            line-height: 1.6;
            background-color: #fff;
            scroll-behavior: smooth;
        }

        /* NAVIGACE */
        nav {
            position: fixed; top: 0; left: 0; width: 100%;
            background: rgba(255, 255, 255, 0.98);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000; display: flex;
            justify-content: space-between; align-items: center;
            padding: 10px 5%;
        }

        nav img { height: 50px; width: auto; max-width: 180px; object-fit: contain; }

        .nav-links { display: flex; gap: 15px; flex-wrap: wrap; justify-content: flex-end; }
        .nav-links a {
            text-decoration: none; color: var(--text-dark);
            font-weight: 700; font-size: 0.65rem;
            text-transform: uppercase; letter-spacing: 0.5px;
        }

        /* HERO */
        .hero {
            height: 60vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('stan-khbox 1.JPG') no-repeat center center/cover;
            display: flex; flex-direction: column; align-items: center;
            justify-content: center; text-align: center; color: white;
            margin-top: 60px; padding: 20px;
        }
        .hero h1 { font-size: clamp(2rem, 8vw, 4.5rem); font-weight: 800; margin: 0; text-shadow: 2px 2px 10px rgba(0,0,0,0.3); }
        .hero h1 span { color: var(--primary-color); }

        /* KONTEJNERY */
        .container { width: 100%; max-width: 1150px; margin: 0 auto; padding: 60px 20px; }
        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 2.2rem; margin-bottom: 10px; font-weight: 800; }
        .divider { width: 60px; height: 5px; background: var(--primary-color); margin: 0 auto; border-radius: 2px; }

        /* KARTY CENÍKU */
        .grid-fixed { display: grid; grid-template-columns: 1fr; gap: 30px; }
        .card {
            background: #fff; border-radius: 12px; border: 1px solid var(--border-color);
            overflow: hidden; display: flex; flex-direction: column;
            transition: all 0.3s ease;
        }
        .card:hover { transform: translateY(-5px); border-color: var(--primary-color); box-shadow: 0 10px 20px rgba(0,0,0,0.05); }
        .card-img { width: 100%; height: 220px; background-size: cover; background-position: center; }
        .card-content { padding: 25px; flex-grow: 1; display: flex; flex-direction: column; }
        .card h3 { font-size: 1.25rem; margin: 5px 0; font-weight: 700; min-height: 3rem; display: flex; align-items: center; }
        
        .price { font-size: 1.5rem; font-weight: 800; margin: 15px 0 5px 0; color: var(--text-dark); }
        .price span { font-size: 0.8rem; font-weight: 400; color: var(--text-gray); }
        .note { font-size: 0.75rem; color: #888; margin-bottom: 15px; line-height: 1.3; }
        
        .card-list { list-style: none; padding: 0; margin: 10px 0; font-size: 0.85rem; flex-grow: 1; }
        .card-list li { margin-bottom: 6px; padding-left: 22px; position: relative; color: var(--text-gray); border-bottom: 1px solid #fcfcfc; padding-bottom: 3px; }
        .card-list li::before { content: "✓"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: block; background: var(--primary-color); color: white;
            padding: 12px; text-decoration: none; border-radius: 6px;
            font-weight: 700; text-align: center; font-size: 0.9rem;
        }

        /* GALERIE */
        .filter-container { text-align: center; margin-bottom: 30px; display: flex; justify-content: center; flex-wrap: wrap; gap: 10px; }
        .filter-btn {
            padding: 10px 20px; border: 1px solid var(--primary-color); background: transparent;
            color: var(--text-dark); cursor: pointer; border-radius: 30px; font-weight: 600;
            transition: all 0.3s ease; font-size: 0.8rem;
        }
        .filter-btn.active, .filter-btn:hover { background: var(--primary-color); color: white; }

        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 15px; }
        .gallery-item { border-radius: 8px; overflow: hidden; height: 200px; transition: 0.3s; }
        .gallery-item img { width: 100%; height: 100%; object-fit: cover; display: block; }
        .gallery-item.hide { display: none; }

        /* FAQ */
        .faq-item { margin-bottom: 25px; padding: 20px; background: #fff; border: 1px solid var(--border-color); border-radius: 8px; }
        .faq-item h4 { margin: 0 0 10px 0; color: var(--text-dark); border-bottom: 1px solid var(--primary-color); display: inline-block; }

        footer { background: #1a1a1a; color: white; padding: 80px 20px 40px; text-align: center; }
        .contact-label { color: var(--primary-color); font-weight: 700; text-transform: uppercase; font-size: 0.8rem; letter-spacing: 1px; }
        .contact-large { font-size: 1.5rem; font-weight: 700; display: block; margin: 10px 0 30px; color: white; text-decoration: none; }
        .footer-bottom { margin-top: 60px; padding-top: 20px; border-top: 1px solid #333; font-size: 0.8rem; color: #777; }

        @media (max-width: 768px) {
            nav { padding: 15px; }
            .nav-links { gap: 8px; justify-content: center; margin-top: 10px; }
            .hero { height: 50vh; margin-top: 110px; }
            .section-title h2 { font-size: 1.8rem; }
        }
        @media (min-width: 768px) { .grid-fixed { grid-template-columns: repeat(2, 1fr); } }
        @media (min-width: 1024px) { .grid-fixed { grid-template-columns: repeat(3, 1fr); } }
    </style>
</head>
<body>

    <nav>
        <img src="logo.jpg" alt="Party Kolín">
        <div class="nav-links">
            <a href="#sluzby">Naše služby</a>
            <a href="#vybaveni">Ceník</a>
            <a href="#galerie">Galerie</a>
            <a href="#faq">Časté dotazy</a>
            <a href="#kontakt">Kontakt</a>
        </div>
    </nav>

    <header class="hero">
        <h1>...s námi to <span>oslavíte</span>.</h1>
    </header>

   <section id="sluzby" style="background: #fcfcfc; padding: 80px 0;">
        <div class="container">
            <div class="section-title">
                <span style="color: var(--primary-color); font-weight: 700; text-transform: uppercase; letter-spacing: 2px; font-size: 0.8rem;">Půjčovna s lidským přístupem</span>
                <h2 style="margin-top: 10px;">...s námi to oslavíte v klidu</h2>
                <div class="divider"></div>
            </div>

            <div style="max-width: 900px; margin: 0 auto;">
                <div style="text-align: center; margin-bottom: 50px;">
                    <p style="font-size: 1.15rem; color: var(--text-dark); font-weight: 600; line-height: 1.6; margin-bottom: 20px;">
                        Nenechte počasí diktovat pravidla vaší párty!
                    </p>
                    <p style="color: var(--text-gray); font-size: 1.05rem;">
                        Plánujete svatbu, rodinné výročí nebo tu nejlepší narozeninovou oslavu pod širým nebem? Máte vybrané jídlo, pozvané hosty a vyladěný každý detail, ale jedna věc vás straší – počasí. My v <strong>Párty Kolín</strong> jsme tu od toho, abychom tuhle nejistotu vymazali z vašeho seznamu starostí.
                    </p>
                </div>

                <div style="background: white; border: 1px solid var(--border-color); border-radius: 15px; padding: 30px; margin-bottom: 50px; display: flex; align-items: center; gap: 20px; flex-wrap: wrap;">
                    <div style="flex: 1; min-width: 280px;">
                        <h3 style="color: var(--primary-color); margin-top: 0;">Kdo jsme?</h3>
                        <p style="margin-bottom: 0;">Jsme dva bratranci z Kolína, kteří věří, že každá oslava si zaslouží být perfektní, ať už venku praží slunce, fouká vítr nebo padají trakaře. Nejsme anonymní půjčovna – zakládáme si na lidském přístupu a 100% spolehlivosti.</p>
                    </div>
                </div>

                <h3 style="text-align: center; margin-bottom: 30px; font-size: 1.6rem;">Co pro vás máme připraveno?</h3>
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px;">
                    <div style="padding: 20px; border-left: 4px solid var(--primary-color); background: #fff; box-shadow: 0 4px 10px rgba(0,0,0,0.02);">
                        <h4 style="margin: 0 0 10px 0; color: var(--text-dark);">⛺ Párty stany</h4>
                        <p style="font-size: 0.9rem; margin: 0; color: var(--text-gray);">
                            Pro velké události (svatby, firemní akce) máme prostorný <strong>trubkový stan 6x12 m</strong>. Pro menší setkání nabízíme <strong>rychlý nůžkový stan 6x3 m</strong>, který stojí doslova za pár minut.
                        </p>
                    </div>
                    <div style="padding: 20px; border-left: 4px solid var(--primary-color); background: #fff; box-shadow: 0 4px 10px rgba(0,0,0,0.02);">
                        <h4 style="margin: 0 0 10px 0; color: var(--text-dark);">☕ Komfort a teplo</h4>
                        <p style="font-size: 0.9rem; margin: 0; color: var(--text-gray);">
                            Zajistíme klasické pivní sety pro pohodlné sezení. A pokud se oslava protáhne do chladného večera? Naše <strong>plynové vytápění</strong> zajistí, že nikdo nebude muset sahat po dece.
                        </p>
                    </div>
                    <div style="padding: 20px; border-left: 4px solid var(--primary-color); background: #fff; box-shadow: 0 4px 10px rgba(0,0,0,0.02);">
                        <h4 style="margin: 0 0 10px 0; color: var(--text-dark);">🏰 Dětský ráj</h4>
                        <p style="font-size: 0.9rem; margin: 0; color: var(--text-gray);">
                            Naše <strong>skákací hrady</strong> zabaví ty nejmenší na dlouhé hodiny, zatímco vy si můžete v klidu užít kávu nebo drink. Bezpečná zábava, která k rodinné akci patří.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
 
    <section id="vybaveni" class="container">
        <div class="section-title">
            <h2>Vybavení & Ceník</h2>
            <div class="divider"></div>
        </div>

        <div class="grid-fixed">
            <div class="card">
                <div class="card-img" style="background-image: url('stan-khbox 1.JPG');"></div>
                <div class="card-content">
                    <h3>Párty stan 6 x 12 m</h3>
                    <ul class="card-list">
                        <li>Kapacita 50 až 80 osob</li>
                        <li>Výška boční stěny 2m / střechy 3m</li>
                        <li>Stabilní PVC plachta a konstrukce</li>
                        <li>V ceně montáž a doprava do 10km</li>
                    </ul>
                    <div class="price">10 890 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('nuzkovy-stan-ostrov 1.jpg');"></div>
                <div class="card-content">
                    <h3>Nůžkový stan 3 x 6 m</h3>
                    <ul class="card-list">
                        <li>Pro cca 20 osob (3 pivní sety)</li>
                        <li>3x bok, 1 strana otevřená</li>
                        <li>Postavení do 5 minut</li>
                        <li>Stabilní konstrukce</li>
                    </ul>
                    <div class="price">1 900 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('pivni-set1.png');"></div>
                <div class="card-content">
                    <h3>Pivní set (2x lavice + stůl)</h3>
                    <ul class="card-list">
                        <li>Pro 6 až 8 osob, stabilní provedení</li>
                        <li>Samostatně od 4ks</li>
                        <li>Jinak pouze ke stanům</li>
                    </ul>
                    <div class="price">330 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('plynový hřib 3.JPG');"></div>
                <div class="card-content">
                    <h3>Vytápění (plynový hřib)</h3>
                    <ul class="card-list">
                        <li>Výkon 10kW (provoz až 13h)</li>
                        <li>Vytápění stanu nebo okolí</li>
                        <li>Cena s 10kg PB: 1550 Kč s DPH</li>
                    </ul>
                    <div class="price">770 Kč <span>/ bez náplně</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad 3v1.JPG');"></div>
                <div class="card-content">
                    <h3>Hrad House 3v1</h3>
                    <ul class="card-list">
                        <li>4,55 x 3,30 x 2,65 m</li>
                        <li>Max. 6 dětí, nosnost 180kg</li>
                        <li>Věk dětí 3 až 10 let</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>
        </div>
    </section>

    <section id="galerie" style="background: #fafafa; padding: 60px 0;">
        <div class="container">
            <div class="section-title">
                <h2>Galerie našich realizací</h2>
                <div class="divider"></div>
            </div>

            <div class="filter-container">
                <button class="filter-btn active" data-filter="all">Vše</button>
                <button class="filter-btn" data-filter="stan6x12">Stan 6x12m</button>
                <button class="filter-btn" data-filter="nuzkovy">Nůžkový stan</button>
                <button class="filter-btn" data-filter="hrady">Skákací hrady</button>
                <button class="filter-btn" data-filter="ostatni">Ostatní</button>
            </div>

            <div class="gallery-grid" id="gallery">
                <div class="gallery-item stan6x12"><img src="stan-hajenka 1.jpg" alt="Párty stan"></div>
                <div class="gallery-item stan6x12"><img src="stan-hajenka 2.jpg" alt="Párty stan"></div>
                <div class="gallery-item stan6x12"><img src="stan-khbox 1.JPG" alt="Párty stan"></div>
                <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 1.jpg" alt="Nůžkový stan"></div>
                <div class="gallery-item hrady"><img src="hrad-draha 1.jpg" alt="Skákací hrad"></div>
                <div class="gallery-item hrady"><img src="hrad-house 1.JPG" alt="Skákací hrad"></div>
                <div class="gallery-item ostatni"><img src="plynovy-hrib 1.jpg" alt="Topení"></div>
                <div class="gallery-item ostatni"><img src="stul-povlak 1.jpg" alt="Rautový stůl"></div>
            </div>
        </div>
    </section>

    <section id="faq" class="container">
        <div class="section-title">
            <h2>Časté dotazy</h2>
            <div class="divider"></div>
        </div>

        <div style="max-width: 900px; margin: 0 auto;">
            <div class="faq-item">
                <h4>Jak objednat zápůjčku?</h4>
                <p>Kontaktujte nás přes email nebo kontaktní formulář a sdělte nám, co byste potřebovali zapůjčit a na jaké období. V odpovědi Vám potvrdíme dostupnost.</p>
            </div>
            <div class="faq-item">
                <h4>Zvládnu hrad rozbalit a nafouknout sám?</h4>
                <p>Ano, hrad postavíte během pár minut. Stačí zkontrolovat plochu, rozložit podkladovou plachtu, nasadit rukáv na kompresor a zapojit do sítě. Hrad se do minuty sám nafoukne.</p>
            </div>
        </div>
    </section>

    <footer id="kontakt">
        <div class="container">
            <span class="contact-label">Miloš Hulinko & Bratranec</span>
            <a href="mailto:info@partykolin.cz" class="contact-large">info@partykolin.cz</a>
            <p>Půjčovna vybavení pro oslavy v Kolíně a okolí.</p>
            <div class="footer-bottom">
                &copy; 2024 Party Kolín | Všechna práva vyhrazena
            </div>
        </div>
    </footer>

    <script>
        // Funkce pro filtrování galerie
        const filterBtns = document.querySelectorAll('.filter-btn');
        const galleryItems = document.querySelectorAll('.gallery-item');

        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                filterBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');

                const filter = btn.getAttribute('data-filter');

                galleryItems.forEach(item => {
                    if (filter === 'all' || item.classList.contains(filter)) {
                        item.classList.remove('hide');
                    } else {
                        item.classList.add('hide');
                    }
                });
            });
        });
    </script>
</body>
</html>
