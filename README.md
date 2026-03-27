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

        /* SEKCE O NÁS */
        .services-intro { background: #fcfcfc; border-bottom: 1px solid var(--border-color); }
        .services-text { max-width: 800px; margin: 0 auto; text-align: center; }
        .services-text p { margin-bottom: 20px; color: var(--text-gray); font-size: 1.05rem; }

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
        .card h3 { font-size: 1.25rem; margin: 5px 0; font-weight: 700; min-height: 3rem; display: flex; align-items: center; }
        
        .price { font-size: 1.5rem; font-weight: 800; margin: 15px 0 5px 0; color: var(--text-dark); }
        .price span { font-size: 0.8rem; font-weight: 400; color: var(--text-gray); }
        .note { font-size: 0.75rem; color: #888; margin-bottom: 15px; line-height: 1.2; }
        
        .card-list { list-style: none; padding: 0; margin: 10px 0; font-size: 0.85rem; flex-grow: 1; }
        .card-list li { margin-bottom: 6px; padding-left: 22px; position: relative; color: var(--text-gray); border-bottom: 1px solid #fcfcfc; padding-bottom: 3px; }
        .card-list li::before { content: "✓"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: block; background: var(--primary-color); color: white;
            padding: 12px; text-decoration: none; border-radius: 6px;
            font-weight: 700; text-align: center; font-size: 0.9rem;
            transition: background 0.2s;
        }
        .btn-main:hover { background: #7ab334; }

        /* FAQ & OSTATNÍ */
        .faq-item { margin-bottom: 25px; padding: 20px; background: #fff; border: 1px solid var(--border-color); border-radius: 8px; }
        .faq-item h4 { margin: 0 0 10px 0; color: var(--text-dark); border-bottom: 1px solid var(--primary-color); display: inline-block; }
        .faq-category { margin-top: 40px; margin-bottom: 20px; text-transform: uppercase; letter-spacing: 1px; color: var(--primary-color); font-weight: 800; }

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
            <a href="#sluzby">Služby</a>
            <a href="#vybaveni">Ceník</a>
            <a href="#galerie">Galerie</a>
            <a href="#faq">Dotazy</a>
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
                <h2>Nenechte počasí diktovat pravidla</h2>
                <div class="divider"></div>
            </div>
            <div class="services-text">
                <p>Plánujete svatbu, výročí nebo narozeninovou oslavu pod širým nebem? My v <strong>Párty Kolín</strong> zajistíme, aby vaši radost nepřekazil déšť ani ostré slunce. Jsme dva bratranci z Kolína a zakládáme si na spolehlivosti a čistotě našeho vybavení.</p>
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
                        <li>Výška boční stěny 2m / střechy 3m</li>
                        <li>V ceně montáž a doprava do 10km</li>
                        <li>Odolná konstrukce i plachta</li>
                    </ul>
                    <div class="price">10 890 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('nuzkový stan.png');"></div>
                <div class="card-content">
                    <h3>Nůžkový stan 3 x 6 m</h3>
                    <ul class="card-list">
                        <li>Kapacita cca 20 osob (3 pivní sety)</li>
                        <li>3x bok, 1 strana otevřená</li>
                        <li>Stabilní konstrukce, stavba do 5 min</li>
                        <li>Kompaktní a rychlé řešení</li>
                    </ul>
                    <div class="price">1 900 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('Pivni set.jpg');"></div>
                <div class="card-content">
                    <h3>Pivní set (2x lavice + stůl)</h3>
                    <ul class="card-list">
                        <li>Kapacita 6 až 8 osob</li>
                        <li>Stabilní a prověřené provedení</li>
                        <li>Samostatně půjčujeme od 4ks</li>
                        <li>Jinak pouze k zapůjčeným stanům</li>
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
                        <li>Luxusní bílé a měkké posezení</li>
                        <li>Povlak na 2 lavice a 1 stůl</li>
                        <li>Molitanová výstelka lavic</li>
                        <li>Půjčujeme v sadě od 4ks</li>
                    </ul>
                    <div class="price">390 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrib.jpg');"></div>
                <div class="card-content">
                    <h3>Vytápění (plynový hřib)</h3>
                    <ul class="card-list">
                        <li>Výkon 10kW (provoz až 13h)</li>
                        <li>Pro stan i venkovní okolí</li>
                        <li>S 10kg PB náplní: 1 550 Kč</li>
                        <li>Samostatně dle domluvy</li>
                    </ul>
                    <div class="price">770 Kč <span>/ bez náplně</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('rautovy-stul.jpg');"></div>
                <div class="card-content">
                    <h3>Rautový stůl 180 cm</h3>
                    <ul class="card-list">
                        <li>Rozměr: 180 x 74 x 75 cm</li>
                        <li>Vnitřní i venkovní použití</li>
                        <li>Možnost bílého potahu (+180 Kč)</li>
                        <li>Pouze k zapůjčeným stanům</li>
                    </ul>
                    <div class="price">245 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('barovy stul.jpg');"></div>
                <div class="card-content">
                    <h3>Barový kulatý stůl</h3>
                    <ul class="card-list">
                        <li>Rozměr: ø 60 cm, výška 110 cm</li>
                        <li>Sklopná deska a stavitelné nohy</li>
                        <li>Možnost bílého potahu (+150 Kč)</li>
                        <li>Samostatně dle domluvy</li>
                    </ul>
                    <div class="price">245 Kč <span>s DPH</span></div>
                    <div class="note">Cena za 1 až 2 dny zapůjčení</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad 3v1.jpg');"></div>
                <div class="card-content">
                    <h3>Skákací hrad House 3v1</h3>
                    <ul class="card-list">
                        <li>4,55 x 3,30 x 2,65 m</li>
                        <li>Pro max. 6 dětí (3-10 let)</li>
                        <li>Atest TÜV, postavení do 5 min</li>
                        <li>Sluneční clona a boční sítě</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <div class="note">Max. nosnost 180 kg</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad skluzavka.jpg');"></div>
                <div class="card-content">
                    <h3>Hrad Obří skluzavka</h3>
                    <ul class="card-list">
                        <li>5,60 x 2,55 x 1,90 m</li>
                        <li>Pro max. 4 děti (3-10 let)</li>
                        <li>Celková hmotnost jen 30 kg</li>
                        <li>Bezpečná zábava s atestem TÜV</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <div class="note">Max. nosnost 180 kg</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-image: url('hrad prekazkova draha.jpg');"></div>
                <div class="card-content">
                    <h3>Hrad Překážková dráha</h3>
                    <ul class="card-list">
                        <li>5,60 x 2,55 x 1,90 m</li>
                        <li>Pro max. 4 děti (3-10 let)</li>
                        <li>Včetně fukaru a příslušenství</li>
                        <li>Atest TÜV, rychlá instalace</li>
                    </ul>
                    <div class="price">1 500 Kč <span>/ 24 hod.</span></div>
                    <div class="note">Max. nosnost 180 kg</div>
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
        <p style="text-align: center; color: #888;">Fotografie našich realizací připravujeme.</p>
    </section>

    <section id="faq" class="container">
        <div class="section-title">
            <h2>Časté dotazy</h2>
            <div class="divider"></div>
        </div>
        <div style="max-width: 900px; margin: 0 auto;">
            <div class="faq-item">
                <h4>Jak objednat?</h4>
                <p>Napište nám na e-mail nebo zavolejte. Prověříme dostupnost a pošleme vám potvrzení.</p>
            </div>
            <div class="faq-item">
                <h4>Stavíte stany vy?</h4>
                <p>Ano, velké párty stany stavíme vždy my, abychom zaručili správné ukotvení a bezpečnost.</p>
            </div>
        </div>
    </section>

    <footer id="kontakt">
        <div class="container" style="padding: 0;">
            <h2 style="margin-bottom: 40px;">Rezervujte si svůj termín</h2>
            <span class="contact-label">E-mail</span>
            <a href="mailto:info@party-kolin.cz" class="contact-large">info@party-kolin.cz</a>
            
            <span class="contact-label">Telefon</span>
            <a href="tel:+420723355740" class="contact-large">+420 723 355 740</a>
            
            <p style="font-weight: 700; color: var(--primary-color);">Kolín a okolí</p>
            <div class="footer-bottom">
                &copy; 2026 Party-Kolin.cz | Miloš Hulinko
            </div>
        </div>
    </footer>

</body>
</html>
