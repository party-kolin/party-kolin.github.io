<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    
    <title>Party Kolín | Půjčovna párty stanů, skákacích hradů a vybavení</title>
    <meta name="description" content="Půjčovna vybavení pro vaši oslavu v Kolíně a okolí. Půjčujeme párty stany 6x12m, nůžkové stany, skákací hrady pro děti, pivní sety s potahy a plynové hřiby.">
    <meta name="keywords" content="půjčovna stanů Kolín, párty stan 6x12, nůžkový stan, skákací hrad Kolín, pivní sety, plynový hřib, oslavy Kolín">
    <meta name="author" content="Miloš Hulinko">

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
        html, body { margin: 0; padding: 0; width: 100%; overflow-x: hidden; scroll-behavior: smooth; }
        body { font-family: 'Inter', sans-serif; color: var(--text-dark); line-height: 1.6; background-color: #fff; }

        /* NAVIGACE */
        nav {
            position: fixed; top: 0; left: 0; width: 100%;
            background: rgba(255, 255, 255, 0.98);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000; display: flex;
            justify-content: space-between; align-items: center;
            padding: 10px 5%;
        }
        nav img { height: 50px; width: auto; }
        .nav-links { display: flex; gap: 15px; flex-wrap: wrap; }
        .nav-links a { text-decoration: none; color: var(--text-dark); font-weight: 700; font-size: 0.65rem; text-transform: uppercase; }

        /* HERO */
        .hero {
            height: 60vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('uvod.jpg.JPG') no-repeat center center/cover;
            display: flex; flex-direction: column; align-items: center;
            justify-content: center; text-align: center; color: white;
            margin-top: 60px; padding: 20px;
        }
        .hero h1 { font-size: clamp(2rem, 8vw, 4.5rem); font-weight: 800; }
        .hero h1 span { color: var(--primary-color); }

        /* KONTEJNERY */
        .container { width: 100%; max-width: 1150px; margin: 0 auto; padding: 60px 20px; }
        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 2.2rem; margin-bottom: 10px; font-weight: 800; }
        .divider { width: 60px; height: 5px; background: var(--primary-color); margin: 0 auto; border-radius: 2px; }

        /* CENÍK KARTY */
        .grid-fixed { display: grid; grid-template-columns: 1fr; gap: 30px; }
        .card { background: #fff; border-radius: 12px; border: 1px solid var(--border-color); overflow: hidden; display: flex; flex-direction: column; }
        .card-img { width: 100%; height: 220px; background-size: cover; background-position: center; }
        .card-content { padding: 25px; flex-grow: 1; display: flex; flex-direction: column; }
        .price { font-size: 1.5rem; font-weight: 800; color: var(--text-dark); margin: 10px 0; }
        .card-list { list-style: none; padding: 0; font-size: 0.85rem; }
        .card-list li::before { content: "✓"; color: var(--primary-color); margin-right: 10px; font-weight: bold; }

        /* FILTR GALERIE */
        .filter-container { text-align: center; margin-bottom: 30px; display: flex; justify-content: center; flex-wrap: wrap; gap: 10px; }
        .filter-btn {
            padding: 10px 20px; border: 1px solid var(--primary-color); background: transparent;
            color: var(--text-dark); cursor: pointer; border-radius: 30px; font-weight: 600;
            transition: all 0.3s ease; font-size: 0.8rem;
        }
        .filter-btn.active, .filter-btn:hover { background: var(--primary-color); color: white; }

        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 15px; }
        .gallery-item { border-radius: 8px; overflow: hidden; height: 200px; transition: 0.3s; display: block; }
        .gallery-item img { width: 100%; height: 100%; object-fit: cover; }
        .gallery-item.hide { display: none; }

        /* FAQ & OSTATNÍ */
        .faq-item { margin-bottom: 20px; padding: 20px; border: 1px solid var(--border-color); border-radius: 8px; }
        footer { background: #1a1a1a; color: white; padding: 60px 20px; text-align: center; }
        .btn-main { display: block; background: var(--primary-color); color: white; padding: 12px; text-decoration: none; border-radius: 6px; text-align: center; font-weight: 700; margin-top: auto; }

        @media (min-width: 768px) { .grid-fixed { grid-template-columns: repeat(2, 1fr); } }
        @media (min-width: 1024px) { .grid-fixed { grid-template-columns: repeat(3, 1fr); } }
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

    <section id="sluzby" class="container">
        <div class="section-title">
            <h2>Naše služby</h2>
            <div class="divider"></div>
        </div>
        <p style="text-align: center; max-width: 800px; margin: 0 auto;">Půjčovna párty vybavení v Kolíně. Zajišťujeme kompletní zázemí pro vaše rodinné oslavy, svatby i firemní akce. Odolné stany, zábava pro děti a profesionální posezení.</p>
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
                    <h3>Párty stan 6x12m</h3>
                    <div class="price">10 890 Kč</div>
                    <ul class="card-list">
                        <li>Kapacita až 80 osob</li>
                        <li>V ceně montáž a doprava do 10km</li>
                    </ul>
                    <a href="#kontakt" class="btn-main">POPTAT</a>
                </div>
            </div>
            </div>
    </section>

    <section id="galerie" class="container" style="background: #fafafa; max-width: 100%;">
        <div class="section-title">
            <h2>Galerie našich realizací</h2>
            <div class="divider"></div>
        </div>

        <div class="filter-container">
            <button class="filter-btn active" onclick="filterGallery('all')">Vše</button>
            <button class="filter-btn" onclick="filterGallery('stan6x12')">Stan 6x12m</button>
            <button class="filter-btn" onclick="filterGallery('nuzkovy')">Nůžkový stan</button>
            <button class="filter-btn" onclick="filterGallery('hrady')">Skákací hrady</button>
            <button class="filter-btn" onclick="filterGallery('ostatni')">Ostatní</button>
        </div>

        <div class="gallery-grid" id="gallery">
            <div class="gallery-item stan6x12"><img src="stan-hájenka 1.jpg" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 2.jpg" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 3.jpg" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 4.jpg" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 5.jpg" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hájenka 6.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 7.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hájenka 8.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-hajenka 9.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 1.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 2.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 3.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-khbox 4.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-mlyn 1.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-mlyn 2.JPG" alt="Realizace 6x12"></div>
            <div class="gallery-item stan6x12"><img src="stan-mlyn 3.JPG" alt="Realizace 6x12"></div>

            <div class="gallery-item nuzkovy"><img src="nízký-stan.JPG" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 1.jpg" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 2.jpg" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 3.jpg" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-ostrov 4.jpg" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-park.jpg" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-zahrada 1.JPG" alt="Nůžkový stan"></div>
            <div class="gallery-item nuzkovy"><img src="nuzkovy-stan-zahrada 2.jpg" alt="Nůžkový stan"></div>

            <div class="gallery-item hrady"><img src="hrad-draha 1.jpg" alt="Skákací hrad"></div>
            <div class="gallery-item hrady"><img src="hrad-draha 2.jpg" alt="Skákací hrad"></div>
            <div class="gallery-item hrady"><img src="hrad-draha 3.jpg" alt="Skákací hrad"></div>
            <div class="gallery-item hrady"><img src="hrad-draha 4.jpg" alt="Skákací hrad"></div>
            <div class="gallery-item hrady"><img src="hradní dům 1.JPG" alt="Skákací hrad"></div>
            <div class="gallery-item hrady"><img src="hradní dům 2.JPG" alt="Skákací hrad"></div>
            <div class="gallery-item hrady"><img src="hradní dům 3.JPG" alt="Skákací hrad"></div>
            <div class="gallery-item hrady"><img src="hrad-skluzavka 1.JPG" alt="Skákací hrad"></div>

            <div class="gallery-item ostatni"><img src="pivní sety 1.JPG" alt="Vybavení"></div>
            <div class="gallery-item ostatni"><img src="plynový hřib 1.jpg" alt="Vybavení"></div>
            <div class="gallery-item ostatni"><img src="plynový hřib 2.jpg" alt="Vybavení"></div>
            <div class="gallery-item ostatni"><img src="plynový hřib 3.JPG" alt="Vybavení"></div>
            <div class="gallery-item ostatni"><img src="sada-povlak 1.jpg" alt="Vybavení"></div>
            <div class="gallery-item ostatni"><img src="sada-povlak 2.jpg" alt="Vybavení"></div>
            <div class="gallery-item ostatni"><img src="stul-povlak 1.jpg" alt="Vybavení"></div>
            <div class="gallery-item ostatni"><img src="stul-povlak 2.JPG" alt="Vybavení"></div>
        </div>
    </section>

    <section id="faq" class="container">
        <div class="section-title"><h2>Časté dotazy</h2><div class="divider"></div></div>
        <div class="faq-item"><h4>Jak objednat?</h4><p>Stačí nám napsat email nebo zavolat. Prověříme termín a potvrdíme rezervaci.</p></div>
    </section>

    <section id="podminky" class="container" style="background: #fcfcfc;">
        <div class="section-title"><h2>Podmínky</h2><div class="divider"></div></div>
        <p style="text-align: center;">Vybavení půjčujeme čisté a funkční. Odpovědnost za škody nese nájemce.</p>
    </section>

    <footer id="kontakt">
        <div class="container">
            <h2>Kontaktujte nás</h2>
            <a href="mailto:info@party-kolin.cz" class="contact-large" style="color: white; font-size: 1.5rem; text-decoration: none;">info@party-kolin.cz</a><br><br>
            <a href="tel:+420723355740" class="contact-large" style="color: white; font-size: 1.5rem; text-decoration: none;">+420 723 355 740</a>
            <p>&copy; 2026 Party-Kolin.cz | Miloš Hulinko</p>
        </div>
    </footer>

    <script>
        function filterGallery(category) {
            const items = document.querySelectorAll('.gallery-item');
            const btns = document.querySelectorAll('.filter-btn');
            
            // Aktivní tlačítko
            btns.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
