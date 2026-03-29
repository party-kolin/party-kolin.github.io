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

        /* GALERIE STYLY */
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

        /* FAQ & OSTATNÍ */
        .faq-item, .policy-item { margin-bottom: 25px; padding: 20px; background: #fff; border: 1px solid var(--border-color); border-radius: 8px; }
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
            <a href="#podminky">Podmínky</a>
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

                <div style="text-align: center; margin-top: 50px; padding: 30px; border-top: 1px dashed #ddd;">
                    <h3 style="margin-bottom: 15px;">Proč jít do toho s námi?</h3>
                    <p style="font-style: italic; color: var(--text-gray);">
                        "Protože nás to baví. Zakládáme si na tom, že naše vybavení je vždy čisté, funkční a že domluva s námi prostě platí. Vaši radost ze srazu s blízkými nenecháme zmoknout."
                    </p>
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
                <div class="card-img" style="background-image: url('povlak.jpg');"></div>
                <div class="card-content">
                    <h3>Povlak na pivní set 200x50</h3>
                    <ul class="card-list">
                        <li>Povlak na 2 lavice a stůl</li>
                        <li>Molitanová výstelka lavic</li>
                        <li>Luxusní měkké posezení</li>
                        <li>Půjčujeme od 4ks</li>
                    </ul>
                    <div class="price">390 Kč <span>s DPH</span></div>
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
                        <li>Samostatně po domluvě</li>
                    </ul>
                    <div class="price">770 Kč <span>/ bez náplně</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('rautovy-stul.JPG');"></div>
                <div class="card-content">
                    <h3>Rautový stůl 180 cm</h3>
                    <ul class="card-list">
                        <li>Rozměr: 180 x 74 x 75 cm</li>
                        <li>Vnitřní i venkovní použití</li>
                        <li>Možnost potahu (+180 Kč s DPH)</li>
                        <li>Půjčujeme pouze se stany</li>
                    </ul>
                    <div class="price">245 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('stul-povlak 2.JPG');"></div>
                <div class="card-content">
                    <h3>Barový kulatý stůl</h3>
                    <ul class="card-list">
                        <li>ø 60 cm, výška 110 cm</li>
                        <li>Sklopná deska, stavitelné nohy</li>
                        <li>Možnost potahu (+150 Kč)</li>
                        <li>Samostatně po domluvě</li>
                    </ul>
                    <div class="price">245 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
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
                        <li>Atest TÜV, boční sítě</li>
                        <li>Věk dětí 3 až 10 let</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <div class="note">Hmotnost jednotlivce max 45kg</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad skluzavka.JPG');"></div>
                <div class="card-content">
                    <h3>Hrad Obří skluzavka</h3>
                    <ul class="card-list">
                        <li>5,60 x 2,55 x 1,90 m</li>
                        <li>Max. 4 děti, nosnost 180kg</li>
                        <li>Atest TÜV, fukar v ceně</li>
                        <li>Věk dětí 3 až 10 let</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <div class="note">Hmotnost jednotlivce max 45kg</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad-draha 2.jpg');"></div>
                <div class="card-content">
                    <h3>Hrad Překážková dráha</h3>
                    <ul class="card-list">
                        <li>5,60 x 2,55 x 1,90 m</li>
                        <li>Max. 4 děti, nosnost 180kg</li>
                        <li>Atest TÜV, váha 30kg</li>
                        <li>Věk dětí 3 až 10 let</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <div class="note">Hmotnost jednotlivce max 45kg</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>
          
      <div class="card">
                <div class="card-img" style="background-image: url('hrad-draha 2.jpg');"></div>
                <div class="card-content">
                    <h3>Hrad Překážková dráha</h3>
                    <ul class="card-list">
                        <li>5,60 x 2,55 x 1,90 m</li>
                        <li>Max. 4 děti, nosnost 180kg</li>
                        <li>Atest TÜV, váha 30kg</li>
                        <li>Věk dětí 3 až 10 let</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <div class="note">Hmotnost jednotlivce max 45kg</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('image2.jpg');"></div>
                <div class="card-content">
                    <h3>Osvětlení stanu</h3>
                    <ul class="card-list">
                        <li>2x halogenový nebo LED reflektor</li>
                        <li>Světelný výkon ekv. 3200lm</li>
                        <li>Kabel 15m nebo 20m (dle stanu)</li>
                        <li>Půjčujeme pouze se stany</li>
                    </ul>
                    <div class="price">390 Kč <span>/ 1 až 2 dny</span></div>
                    <div class="note">Cena včetně montáže a demontáže</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('doprava.jpg');"></div>
                <div class="card-content">
                    <h3>Doprava a závoz</h3>
                    <ul class="card-list">
                        <li><strong>Stan 6x12m: do 10km ZDARMA</strong></li>
                        <li>Ostatní: individuální kalkulace</li>
                        <li>Dle velikosti zakázky a vzdálenosti</li>
                        <li>Závoz v rámci Kolína a okolí</li>
                    </ul>
                    <div class="price">Individuálně <span>/ dle cesty</span></div>
                    <div class="note">Cenu vám upřesníme v nabídce</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

        </div> </section> <section id="galerie" class="container" style="background: #fafafa; max-width: 100%;">

    <section id="galerie" class="container" style="background: #fafafa; max-width: 100%;">
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
            <div class="gallery-item stan6x12"><img src="stan-hajenka 1.jpg" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 2.jpg" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 3.jpg" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 4.jpg" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 5.jpg" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 6.JPG" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 7.JPG" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 8.JPG" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 9.JPG" alt="Párty stan Hájenka"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 1.JPG" alt="Párty stan Kolín"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 2.JPG" alt="Párty stan Kolín"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 3.JPG" alt="Párty stan Kolín"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 4.JPG" alt="Párty stan Kolín"></div>
            <div class="gallery-item stan6x12"><img src="stan-mlyn 1.JPG" alt="Párty stan u mlýna"></div>
            <div class="gallery-item stan6x12"><img src="stan-mlyn 2.JPG" alt="Párty stan u mlýna"></div>
            <div class="gallery-item stan6x12"><img src="stan-mlyn 3.JPG" alt="Párty stan u mlýna"></div>

            <div class="gallery-item nuzkovy"><img src="nizkovy-stan.JPG" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 1.jpg" alt="Nůžkový stan Ostrov"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 2.jpg" alt="Nůžkový stan Ostrov"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 3.jpg" alt="Nůžkový stan Ostrov"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 4.jpg" alt="Nůžkový stan Ostrov"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-park.jpg" alt="Nůžkový stan v parku"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-zahrada 1.JPG" alt="Nůžkový stan na zahradě"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-zahrada 2.jpg" alt="Nůžkový stan na zahradě"></div>

            <div class="gallery-item hrady"><img src="hrad-draha 1.jpg" alt="Překážková dráha"></div>
            <div class="gallery-item hrady"><img src="hrad-draha 2.jpg" alt="Překážková dráha"></div>
            <div class="gallery-item hrady"><img src="hrad-draha 3.jpg" alt="Překážková dráha"></div>
            <div class="gallery-item hrady"><img src="hrad-draha 4.jpg" alt="Překážková dráha"></div>
            <div class="gallery-item hrady"><img src="hrad-house 1.JPG" alt="Hradní dům"></div>
            <div class="gallery-item hrady"><img src="hrad-house 2.JPG" alt="Hradní dům"></div>
            <div class="gallery-item hrady"><img src="hrad-house 3.JPG" alt="Hradní dům"></div>
            <div class="gallery-item hrady"><img src="hrad-skluzavka 1.JPG" alt="Obří skluzavka"></div>

            <div class="gallery-item ostatni"><img src="pivni-sety 1.JPG" alt="Pivní sety"></div>
            <div class="gallery-item ostatni"><img src="plynovy-hrib 1.jpg" alt="Plynový hřib"></div>
            <div class="gallery-item ostatni"><img src="plynovy-hrib 2.jpg" alt="Plynový hřib"></div>
            <div class="gallery-item ostatni"><img src="plynovy-hrib 3.JPG" alt="Plynový hřib"></div>
            <div class="gallery-item ostatni"><img src="set-povlak 1.jpg" alt="Povlaky na pivní sety"></div>
            <div class="gallery-item ostatni"><img src="set-povlak 2.jpg" alt="Povlaky na pivní sety"></div>
            <div class="gallery-item ostatni"><img src="stul-povlak 1.jpg" alt="Rautový stůl s povlakem"></div>
            <div class="gallery-item ostatni"><img src="stul-povlak 2.JPG" alt="Barový stůl s povlakem"></div>
        </div>
    </section>

   <section id="faq" class="container" style="background: #fff;">
        <div class="section-title">
            <h2>Časté dotazy</h2>
            <div class="divider"></div>
        </div>

        <div style="max-width: 900px; margin: 0 auto;">
            
            <div style="margin-bottom: 40px;">
                <h3 style="color: var(--primary-color); border-bottom: 2px solid var(--border-color); padding-bottom: 10px; margin-bottom: 20px;">📌 Obecné informace</h3>
                
                <div class="faq-item">
                    <h4>Jak objednat zápůjčku (pronájem)?</h4>
                    <p>Kontaktujte nás přes email nebo kontaktní formulář a sdělte nám, co byste z výčtu vybavení potřebovali zapůjčit a také na jaké období. V odpovědi Vám potvrdíme dostupnost vybavení. V ten moment nepřijmeme další požadavek od jiných zájemců, dokud u Vás nebudeme mít jasno, zda máte zájem či nikoliv. V dalších krocích komunikace přejdeme od nabídky až po případné potvrzení Vaší objednávky.</p>
                </div>

                <div class="faq-item">
                    <h4>Jak vzniká obchodní vztah (smlouva o pronájmu)?</h4>
                    <p>1) Potvrzením nabídky zájemcem elektronicky (závazná objednávka), kde zároveň zájemce souhlasí s Obchodními podmínkami.<br>
                       2) Podpisem papírové Smlouvy o pronájmu při předání předmětu nájmu.</p>
                </div>

                <div class="faq-item">
                    <h4>Kde je možné zápůjčku vyzvednout?</h4>
                    <p>Jelikož nemáme žádné oficiální výdejní místo, stany a další vybavení Vám <strong>přivezeme na místo určení</strong>, kde Vám stan(y) rovnou postavíme. Dětský skákací hrad Vám buď také přivezeme, nebo se domluvíme na místě předání.</p>
                </div>
            </div>

            <div style="margin-bottom: 40px;">
                <h3 style="color: var(--primary-color); border-bottom: 2px solid var(--border-color); padding-bottom: 10px; margin-bottom: 20px;">⛺ Párty stany</h3>
                
                <div class="faq-item">
                    <h4>Mohu si párty stan + příslušenství postavit sám/sama?</h4>
                    <p>Bohužel to není možné. Stany půjčujeme <strong>pouze se stavbou od nás</strong>, z důvodů kontroly stavu při navrácení a také proto, že stavba velkého stanu vyžaduje zkušenosti a přesný postup.</p>
                </div>

                <div class="faq-item">
                    <h4>Jak velké místo budu pro stan či hrad potřebovat?</h4>
                    <p>Pro párty stan je třeba počítat s <strong>3 m navíc</strong> oproti psaným rozměrům na každou stranu stanu. Na výšku stan potřebuje cca 3 m prostoru. Skákací hrad potřebuje rovněž min. 3 m odstup na každou stranu.</p>
                </div>

                <div class="faq-item">
                    <h4>Na jakém místě lze párty stan postavit?</h4>
                    <p>Je třeba <strong>měkký podklad (tráva, hlína)</strong>, aby stan bylo možno řádně ukotvit, popř. podklad, do kterého lze navrtat kotvící turbo šrouby. Stavba na jiný podklad (beton, dlažba) je možná pouze po předchozí domluvě.</p>
                </div>
            </div>

            <div style="margin-bottom: 40px;">
                <h3 style="color: var(--primary-color); border-bottom: 2px solid var(--border-color); padding-bottom: 10px; margin-bottom: 20px;">🏰 Dětské skákací hrady</h3>
                
                <div class="faq-item">
                    <h4>Zvládnu hrad rozbalit a nafouknout sám?</h4>
                    <p>Ano, hrad postavíte během pár minut. Stačí zkontrolovat plochu (bez ostrých nečistot), rozložit podkladovou plachtu a na ní hrad roztáhnout. Poté nasadíte rukáv hradu na kompresor, zajistíte suchým zipem a zapojíte do sítě. Hrad se do minut
