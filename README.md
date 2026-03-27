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
            line-height: 1.5;
            background-color: #fff;
            scroll-behavior: smooth;
        }

        nav {
            position: fixed; top: 0; left: 0; width: 100%;
            background: rgba(255, 255, 255, 0.98);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000; display: flex;
            justify-content: space-between; align-items: center;
            padding: 10px 15px;
        }

        nav img { height: 30px; max-width: 40%; object-fit: contain; }

        .nav-links { display: flex; gap: 10px; }
        .nav-links a {
            text-decoration: none; color: var(--text-dark);
            font-weight: 600; font-size: 0.65rem;
            text-transform: uppercase;
        }

        .hero {
            height: 50vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('uvod.jpg.JPG') no-repeat center center/cover;
            display: flex; flex-direction: column; align-items: center;
            justify-content: center; text-align: center; color: white;
            margin-top: 50px; padding: 20px; width: 100%;
        }

        .hero h1 { font-size: clamp(1.5rem, 7vw, 3.5rem); margin: 0; }
        .hero h1 span { color: var(--primary-color); }

        .container { width: 100%; max-width: 1100px; margin: 0 auto; padding: 40px 15px; }
        .section-title { text-align: center; margin-bottom: 30px; }
        .divider { width: 40px; height: 3px; background: var(--primary-color); margin: 0 auto; }

        .grid-fixed { display: block; width: 100%; }

        .card {
            background: #fff; border-radius: 8px; border: 1px solid var(--border-color);
            margin-bottom: 25px; overflow: hidden; width: 100%;
            display: flex; flex-direction: column;
        }

        .card-img { width: 100%; height: 200px; background-size: cover; background-position: center; }
        .card-content { padding: 20px; flex-grow: 1; display: flex; flex-direction: column; }
        .card h3 { font-size: 1.15rem; margin: 5px 0; color: var(--text-dark); }
        .price { font-size: 1.4rem; font-weight: 700; margin: 15px 0 10px 0; }
        .price span { font-size: 0.8rem; font-weight: 400; color: var(--text-gray); }
        
        .card-list { list-style: none; padding: 0; margin: 10px 0; font-size: 0.85rem; flex-grow: 1; }
        .card-list li { margin-bottom: 5px; padding-left: 20px; position: relative; color: var(--text-gray); }
        .card-list li::before { content: "✓"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: block; background: var(--primary-color); color: white;
            padding: 12px; text-decoration: none; border-radius: 4px;
            font-weight: 600; text-align: center; font-size: 0.9rem; margin-top: 10px;
        }

        @media (min-width: 768px) {
            .grid-fixed { display: grid; grid-template-columns: repeat(2, 1fr); gap: 25px; }
            .card { margin-bottom: 0; }
            .nav-links { gap: 15px; }
            .nav-links a { font-size: 0.75rem; }
        }

        @media (min-width: 1024px) {
            .grid-fixed { grid-template-columns: repeat(3, 1fr); }
        }

        footer { background: #fafafa; padding: 60px 20px; text-align: center; border-top: 1px solid var(--border-color); }
        .contact-large { font-size: 1.3rem; font-weight: 700; display: block; margin: 10px 0; color: var(--text-dark); text-decoration: none; }
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
                <div class="card-img" style="background-image: url('image_2.png');"></div>
                <div class="card-content">
                    <h3>Párty stan 6 x 12 m</h3>
                    <ul class="card-list">
                        <li>Kapacita 50 až 80 osob</li>
                        <li>Robustní trubková konstrukce</li>
                        <li>Doprava do 10km zdarma</li>
                    </ul>
                    <div class="price">10 890 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>

            <div class="card">
                <div class="card-img" style="background-color: #eee; display: flex; align-items: center; justify-content: center; color: #aaa;">Foto připravujeme</div>
                <div class="card-content">
                    <h3>Nůžkový stan 3 x 6 m</h3>
                    <ul class="card-list">
                        <li>Kapacita cca 20 osob</li>
                        <li>Postavení do 5 minut</li>
                        <li>3x bok, 1x otevřená strana</li>
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
                        <li>Sestava: 1x stůl + 2x lavice</li>
                        <li>Kapacita 6 až 8 osob</li>
                        <li>Stabilní dřevěné provedení</li>
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
                        <li>Povlak na 2 lavice a stůl</li>
                        <li><strong>Molitanová výstelka</strong> lavic</li>
                        <li>100% bavlna, půjčujeme od 4ks</li>
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
                        <li>Rozměr: 180x74x75cm</li>
                        <li>Stabilní skládací provedení</li>
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
                        <li>Sklopná deska, stavitelné nohy</li>
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
                        <li>Bez náplně: 770 Kč</li>
                        <li>S náplní 10kg PB: 1550 Kč</li>
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
                        <li>4,55 x 3,30 x 2,65 m</li>
                        <li>Max. 6 dětí najednou</li>
                        <li>Atest TÜV, boční sítě</li>
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
                        <li>5,60 x 2,55 x 1,90 m</li>
                        <li>Max. 4 děti najednou</li>
                        <li>Velká plocha na klouzání</li>
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
                        <li>5,60 x 2,55 x 1,90 m</li>
                        <li>Aktivní herní prvky</li>
                        <li>Pro děti od 3 do 10 let</li>
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
                        <li>2x LED/Halogen reflektor</li>
                        <li>Kabeláž 15m nebo 20m</li>
                        <li><strong>Včetně montáže</strong></li>
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
                        <li>Stan 6x12m: do 10km zdarma</li>
                        <li>Ostatní dle velikosti akce</li>
                        <li>Rozvoz z Kolína</li>
                    </ul>
                    <div class="price">Individuálně</div>
                    <a href="#kontakt" class="btn-main">POPTAT TERMÍN</a>
                </div>
            </div>
        </div>
    </section>

    <footer id="kontakt">
        <h2 style="font-size:1.4rem;">Máte zájem o rezervaci?</h2>
        <a href="tel:+420723355740" class="contact-large">+420 723 355 740</a>
        <a href="tel:+420605717081" class="contact-large">+420 605 717 081</a>
        <p>Kolín a široké okolí</p>
        <p style="font-size:0.8rem; color:#aaa; margin-top:30px;">&copy; 2026 Party-Kolin.cz</p>
    </footer>

</body>
</html>
