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
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('uvod.jpg.JPG') no-repeat center center/cover;
            display: flex; flex-direction: column; align-items: center;
            justify-content: center; text-align: center; color: white;
            margin-top: 60px; padding: 20px;
        }
        .hero h1 { font-size: clamp(2rem, 8vw, 4.5rem); font-weight: 800; margin: 0; text-shadow: 2px 2px 10px rgba(0,0,0,0.3); }
        .hero h1 span { color: var(--primary-color); }

        /* SEKCE O NÁS / SLUŽBY */
        .services-intro { background: #fcfcfc; border-bottom: 1px solid var(--border-color); }
        .services-text { max-width: 800px; margin: 0 auto; text-align: center; }
        .services-text p { margin-bottom: 20px; color: var(--text-gray); font-size: 1.05rem; }
        .services-grid { 
            display: grid; grid-template-columns: 1fr; gap: 30px; margin-top: 40px; text-align: left;
        }

        /* KONTEJNERY */
        .container { width: 100%; max-width: 1150px; margin: 0 auto; padding: 60px 20px; }
        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 2.2rem; margin-bottom: 10px; font-weight: 800; }
        .divider { width: 60px; height: 5px; background: var(--primary-color); margin: 0 auto; border-radius: 2px; }

        /* MŘÍŽKA KARET */
        .grid-fixed { display: grid; grid-template-columns: 1fr; gap: 30px; }

        .card {
            background: #fff; border-radius: 12px; border: 1px solid var(--border-color);
            overflow: hidden; display: flex; flex-direction: column;
            transition: all 0.3s ease;
        }
        .card:hover { transform: translateY(-5px); border-color: var(--primary-color); box-shadow: 0 10px 20px rgba(0,0,0,0.05); }

        .card-img { width: 100%; height: 220px; background-size: cover; background-position: center; }
        .card-content { padding: 25px; flex-grow: 1; display: flex; flex-direction: column; }
        .card h3 { font-size: 1.3rem; margin: 5px 0; font-weight: 700; }
        
        .price { font-size: 1.6rem; font-weight: 800; margin: 15px 0 10px 0; }
        .price span { font-size: 0.85rem; font-weight: 400; color: var(--text-gray); }
        
        .card-list { list-style: none; padding: 0; margin: 15px 0; font-size: 0.9rem; flex-grow: 1; }
        .card-list li { margin-bottom: 8px; padding-left: 25px; position: relative; color: var(--text-gray); }
        .card-list li::before { content: "✓"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: block; background: var(--primary-color); color: white;
            padding: 14px; text-decoration: none; border-radius: 6px;
            font-weight: 700; text-align: center; font-size: 1rem;
        }

        /* FAQ STYLE */
        .faq-item { margin-bottom: 25px; padding: 20px; background: #fff; border: 1px solid var(--border-color); border-radius: 8px; }
        .faq-item h4 { margin: 0 0 10px 0; color: var(--text-dark); border-bottom: 1px solid var(--primary-color); display: inline-block; }
        .faq-category { margin-top: 40px; margin-bottom: 20px; text-transform: uppercase; letter-spacing: 1px; color: var(--primary-color); font-weight: 800; }

        /* PATIČKA */
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

        @media (min-width: 768px) {
            .grid-fixed { grid-template-columns: repeat(2, 1fr); }
            .services-grid { grid-template-columns: 1fr 1fr; }
        }

        @media (min-width: 1024px) {
            .grid-fixed { grid-template-columns: repeat(3, 1fr); }
        }
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

    <section id="sluzby" class="services-intro">
        <div class="container">
            <div class="section-title">
                <h2>Nenechte počasí diktovat pravidla vaší párty!</h2>
                <div class="divider"></div>
            </div>
            <div class="services-text">
                <p>Plánujete svatbu, rodinné výročí nebo tu nejlepší narozeninovou oslavu pod širým nebem? Máte vybrané jídlo, pozvané hosty a vyladěný každý detail, ale jedna věc vás straší – počasí. My v <strong>Párty Kolín</strong> jsme tu od toho, abychom tuhle nejistotu vymazali z vašeho seznamu starostí.</p>
                <p>Jsme dva bratranci, kteří věří, že každá oslava si zaslouží být perfektní, ať už venku praží slunce, fouká vítr nebo padají trakaře. K našemu vybavení přidáváme lidský přístup a spolehlivost, na kterou se můžete v ten důležitý den stoprocentně spolehnout.</p>
                
                <div class="services-grid">
                    <div>
                        <h4 style="color:var(--primary-color)">Párty stany pro každou příležitost</h4>
                        <p style="font-size: 0.95rem;">Pro větší události (svatby, firemní akce) máme prostorný stan <strong>6x12 m</strong>. Pro komornější setkání nabízíme rychlý nůžkový stan <strong>3x6 m</strong>, který stojí za pár minut.</p>
                    </div>
                    <div>
                        <h4 style="color:var(--primary-color)">Komfort, teplo a zábava</h4>
                        <p style="font-size: 0.95rem;">Zajistíme pivní sety pro pohodlné sezení a vytápění pro chladné večery. Pro děti máme <strong>skákací hrady</strong>, které je zabaví na celé hodiny.</p>
                    </div>
                </div>

                <div style="margin-top: 40px; padding: 25px; background: #fff; border: 1px solid var(--border-color); border-radius: 12px;">
                    <h3 style="margin-top:0">Proč jít do toho s námi?</h3>
                    <p>Protože nejsme anonymní půjčovna. Jsme kluci z Kolína, které to baví. Zakládáme si na tom, že naše vybavení je <strong>čisté, funkční a že domluva s námi platí</strong>. Vaši radost ze srazu s blízkými prostě nenecháme zmoknout.</p>
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
                <div class="card-img" style="background-image: url('image_2.png');"></div>
                <div class="card-content">
                    <h3>Párty stan 6 x 12 m</h3>
                    <ul class="card-list">
                        <li>Kapacita 50 až 80 osob</li>
                        <li>Doprava do 10km zdarma</li>
                    </ul>
                    <div class="price">10 890 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-color: #f5f5f5; display: flex; align-items: center; justify-content: center; color: #bbb;">Foto připravujeme</div>
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
                <div class="card-img" style="background-image: url('Pivni set.jpg');"></div>
                <div class="card-content">
                    <h3>Pivní set 200 x 50 cm</h3>
                    <ul class="card-list">
                        <li>1x stůl + 2x lavice</li>
                        <li>Stabilní dřevo</li>
                    </ul>
                    <div class="price">330 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('povlak.jpg');"></div>
                <div class="card-content">
                    <h3>Povlak na pivní set</h3>
                    <ul class="card-list">
                        <li>Bílá bavlna, molitan</li>
                        <li>Set na stůl a lavice</li>
                    </ul>
                    <div class="price">390 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('rautovy-stul.jpg');"></div>
                <div class="card-content">
                    <h3>Rautový stůl 180 cm</h3>
                    <ul class="card-list">
                        <li>Skládací, stabilní</li>
                        <li>Možnost potahu (+ 180 Kč)</li>
                    </ul>
                    <div class="price">245 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('barovy stul.jpg');"></div>
                <div class="card-content">
                    <h3>Barový kulatý stůl</h3>
                    <ul class="card-list">
                        <li>ø 60 cm, výška 110 cm</li>
                        <li>Možnost potahu (+ 150 Kč)</li>
                    </ul>
                    <div class="price">245 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrib.jpg');"></div>
                <div class="card-content">
                    <h3>Plynový hřib (10kW)</h3>
                    <ul class="card-list">
                        <li>Až 13 hodin provozu</li>
                        <li>Cena od 770 Kč</li>
                    </ul>
                    <div class="price">od 770 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad 3v1.jpg');"></div>
                <div class="card-content">
                    <h3>Hrad House 3 v 1</h3>
                    <ul class="card-list">
                        <li>Atest TÜV, max 6 dětí</li>
                        <li>Postavení do 5 minut</li>
                    </ul>
                    <div class="price">1 500 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad skluzavka.jpg');"></div>
                <div class="card-content">
                    <h3>Obří skluzavka</h3>
                    <ul class="card-list">
                        <li>Atest TÜV, max 4 děti</li>
                        <li>Extra dlouhá plocha</li>
                    </ul>
                    <div class="price">1 500 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad prekazkova draha.jpg');"></div>
                <div class="card-content">
                    <h3>Překážková dráha</h3>
                    <ul class="card-list">
                        <li>Atest TÜV</li>
                        <li>Aktivní prvky uvnitř</li>
                    </ul>
                    <div class="price">1 500 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('osvetleni.jpg');"></div>
                <div class="card-content">
                    <h3>Osvětlení stanu</h3>
                    <ul class="card-list">
                        <li>2x LED reflektor</li>
                        <li>Včetně odborné montáže</li>
                    </ul>
                    <div class="price">390 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('doprava.jpg');"></div>
                <div class="card-content">
                    <h3>Doprava a závoz</h3>
                    <ul class="card-list">
                        <li>Stan 6x12: do 10km zdarma</li>
                        <li>Individuální rozvoz</li>
                    </ul>
                    <div class="price">Dle domluvy</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>
        </div>
    </section>

    <section id="galerie" class="container" style="background: #fafafa; max-width: 100%;">
        <div class="section-title">
            <h2>Fotogalerie</h2>
            <div class="divider"></div>
        </div>
        <p style="text-align: center; color: #888;">Připravujeme pro vás fotky z našich realizací...</p>
    </section>

    <section id="faq" class="container">
        <div class="section-title">
            <h2>Časté dotazy</h2>
            <div class="divider"></div>
        </div>
        <div style="max-width: 900px; margin: 0 auto;">
            
            <div class="faq-category">Obecné informace</div>
            <div class="faq-item">
                <h4>Jak objednat zápůjčku?</h4>
                <p>Kontaktujte nás přes email nebo kontaktní formulář a sdělte nám, co byste z výčtu vybavení potřebovali zapůjčit a také na jaké období. V odpovědi Vám potvrdíme dostupnost vybavení. V ten moment nepřijmeme další požadavek od jiných zájemců, dokud u Vás nebudeme mít jasno.</p>
            </div>
            <div class="faq-item">
                <h4>Jak vzniká smlouva o pronájmu?</h4>
                <p>1) Potvrzením nabídky zájemcem elektronicky (závazná objednávka), kde souhlasíte s Obchodními podmínkami.<br>2) Podpisem papírové Smlouvy o pronájmu při předání předmětu nájmu.</p>
            </div>
            <div class="faq-item">
                <h4>Kde je možné zápůjčku vyzvednout?</h4>
                <p>Jelikož nemáme oficiální výdejní místo, stany a vybavení Vám přivezeme na místo určení, kde Vám stan(y) rovnou postavíme. Dětský hrad Vám také přivezeme nebo se domluvíme na místě předání.</p>
            </div>

            <div class="faq-category">Párty stany</div>
            <div class="faq-item">
                <h4>Mohu si párty stan postavit sám?</h4>
                <p>Bohužel to není možné. Stany půjčujeme pouze se stavbou od nás z důvodu kontroly stavu při navrácení a náročnosti samotné stavby.</p>
            </div>
            <div class="faq-item">
                <h4>Jak velké místo budu potřebovat?</h4>
                <p>Pro párty stan je třeba počítat s 3 m navíc oproti rozměrům na každou stranu. Na výšku stan potřebuje cca 3 m prostoru. Skákací hrad potřebuje také min. 3 m na každou stranu navíc.</p>
            </div>
            <div class="faq-item">
                <h4>Na jakém místě lze stan postavit?</h4>
                <p>Je třeba měkký podklad (tráva, hlína) pro řádné ukotvení, popř. podklad, do kterého lze navrtat turbo šrouby. Stavba na jiný podklad je možná pouze po předchozí domluvě.</p>
            </div>

            <div class="faq-category">Skákací hrady</div>
            <div class="faq-item">
                <h4>Zvládnu hrad rozbalit a nafouknout sám?</h4>
                <p>Ano, zvládnete to během pár minut. Stačí zkontrolovat plochu bez nečistot, rozložit podkladovou plachtu (součástí vybavení), připojit kompresor a zapojit do sítě. Hrad se do minuty nafoukne. Poté ho zafixujete kolíky do země.</p>
            </div>
            <div class="faq-item">
                <h4>Co dělat když hrad poškodím?</h4>
                <p>Ihned nás kontaktujte. I v případě malého propíchnutí hrad normálně funguje dál, protože kompresor je velmi výkonný.</p>
            </div>
            <div class="faq-item">
                <h4>Může na hrad pršet?</h4>
                <p>V žádném případě! Hrozí úraz proudem od kompresoru. Pokud začne pršet, ihned ho odpojte. Pokud atrakce zmokne, je třeba ji později rozbalit a nechat dokonale vyschnout.</p>
            </div>
        </div>
    </section>

    <section id="podminky" class="container" style="background: #f9f9f9; max-width: 100%;">
        <div class="section-title">
            <h2>Obchodní podmínky</h2>
            <div class="divider"></div>
        </div>
        <div style="max-width: 900px; margin: 0 auto; font-size: 0.85rem; color: var(--text-gray); line-height: 1.4; text-align: justify;">
            <h3>1. Výklad pojmů</h3>
            <p>1.1. Pronajímatel - Miloš Hulinko, Tylova 184, 281 01, Velim, IČ: 76282431.<br>
            1.2. Nájemce - osoba, která uzavřela smlouvu o pronájmu.<br>
            1.3. Smlouva - písemná nebo elektronická (emailem).<br>
            1.4. Předmět nájmu - párty vybavení (stany, lavice, stoly, hrad atd.).</p>

            <h3>2. Platnost VOP</h3>
            <p>2.1. Tyto VOP platí pro všechny smlouvy, ve kterých vystupuje Miloš Hulinko jako pronajímatel dle § 1751 odst. 1 občanského zákoníku.</p>

            <h3>3. Obecné zásady</h3>
            <p>3.1. K uzavření vztahu dochází podpisem smlouvy nebo závaznou objednávkou emailem.</p>

            <h3>4. Předmět nájmu</h3>
            <p>4.1. U stanů je součástí plnění také montáž, demontáž a doprava dle ceníku v sekci "VYBAVENÍ".</p>

            <h3>5. Místo nájmu a montáž</h3>
            <p>5.2. Nájemce zajistí povolení užívat prostranství. 5.3. Nájemce zajistí rovný podklad a informuje pronajímatele o druhu podkladu (tráva, beton atd.). 5.6. Změna místa po zahájení montáže může být zpoplatněna sazbou 250 Kč/hod na osobu.</p>

            <h3>6. Trvání nájmu</h3>
            <p>6.2. Nedostavení se nájemce k montáži (nad 30 min) dává pronajímateli právo odstoupit se sankcí 30 % ceny. 6.3. O předání a vrácení se sepisuje předávací protokol.</p>

            <h3>7. Nájemné a platba</h3>
            <p>7.1. Nájemné se platí hotově při předání předmětu nájmu. 7.5. Případné vícenáklady jsou splatné do 7 dnů. 7.8. Úrok z prodlení činí 1 % z dlužné částky za každý den.</p>

            <h3>9. Odpovědnost a meteorologické podmínky</h3>
            <p>9.1. Nájemce odpovídá za ztrátu a poškození. 9.5. Stan nelze užívat při větru nad 72 km/h, teplotách pod -30°C/+40°C nebo při sněhové pokrývce na plachtě. 9.6. Zákaz otevřeného ohně v blízkosti vybavení.</p>

            <h3>10. Odstupné</h3>
            <p>10.1. Rezervační záloha je vratná při zrušení 90 a více dnů předem, nebo z důvodu nepříznivého počasí.</p>

            <h3>12. Závěrečná ustanovení</h3>
            <p>12.2. Tyto VOP nabývají účinnosti dnem 1.4.2026.</p>
        </div>
    </section>

    <footer id="kontakt">
        <div class="container" style="padding: 0;">
            <h2 style="font-size:2rem; margin-bottom: 10px;">Máte zájem o rezervaci?</h2>
            <p style="color: #aaa; margin-bottom: 40px; font-size: 1.1rem;">Napište nám nebo zavolejte, rádi vám poradíme.</p>
            
            <div style="margin-bottom: 30px;">
                <span class="contact-label">E-mail</span>
                <a href="mailto:info@party-kolin.cz" class="contact-large">info@party-kolin.cz</a>
            </div>

            <div style="margin-bottom: 30px;">
                <span class="contact-label">Telefon</span>
                <a href="tel:+420723355740" class="contact-large">+420 723 355 740</a>
                <a href="tel:+420605717081" class="contact-large">+420 605 717 081</a>
            </div>

            <p style="font-weight: 700; font-size: 1.2rem; color: var(--primary-color);">Kolín a široké okolí</p>
            
            <div class="footer-bottom">
                &copy; 2026 Party-Kolin.cz | Miloš Hulinko | Bratranci z Kolína
            </div>
        </div>
    </footer>

</body>
</html>
