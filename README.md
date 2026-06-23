
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mode & Élégance | Boutique en Ligne</title>
    <style>
        /* --- STYLE GLOBAL & VARIABLE --- */
        :root { --primary: #2c3e50; --accent: #e74c3c; --light: #f8f9fa; --dark: #333; }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', sans-serif; scroll-behavior: smooth; }
        body { color: var(--dark); background: #fff; line-height: 1.6; }
        a { text-decoration: none; color: inherit; }
        
        /* --- NAVIGATION --- */
        header { background: var(--primary); color: white; padding: 15px 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 0; z-index: 100; }
        .logo { font-size: 24px; font-weight: bold; }
        nav a { color: white; font-size: 16px; margin-left: 20px; transition: 0.3s; }
        nav a:hover { color: var(--accent); }
        .cart-link { background: var(--accent); color: white; padding: 5px 15px; border-radius: 5px; font-weight: bold; }
        /* --- STRUCTURE DES SECTIONS --- */
        .section-page { padding: 80px 5% 40px; border-bottom: 1px solid #eee; }
        h1 { text-align: center; margin-bottom: 30px; color: var(--primary); }
        /* --- SECTION ACCUEIL --- */
        .hero { background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1441986300917-64674bd600d8?w=1200') center/cover; height: 60vh; display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center; }
        .hero h2 { font-size: 45px; margin-bottom: 15px; }
        .btn { background: var(--accent); color: white; padding: 12px 30px; border: none; border-radius: 5px; cursor: pointer; font-size: 16px; display: inline-block; text-align: center; }
        .btn:hover { background: #c0392b; }
        .featured { display: flex; justify-content: space-around; margin-top: 40px; flex-wrap: wrap; gap: 20px; }
        .feat-card { width: 45%; height: 250px; position: relative; overflow: hidden; border-radius: 8px; }
        .feat-card img { width: 100%; height: 100%; object-fit: cover; transition: 0.5s; }
        .feat-card:hover img { transform: scale(1.1); }
        .feat-text { position: absolute; bottom: 20px; left: 20px; color: white; text-shadow: 2px 2px 4px rgba(0,0,0,0.8); font-size: 24px; font-weight: bold; }
        /* --- SECTION PRODUITS --- */
        .products-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; margin-top: 20px; }
        .product-card { border: 1px solid #ddd; border-radius: 8px; overflow: hidden; transition: 0.3s; text-align: center; padding-bottom: 15px; background: white; }
        .product-card:hover { box-shadow: 0 5px 15px rgba(0,0,0,0.1); }
        .product-img { width: 100%; height: 350px; object-fit: cover; }
        .product-title { font-size: 18px; margin: 15px 0 5px; }
        .product-price { color: var(--accent); font-weight: bold; margin-bottom: 15px; }
        /* --- SECTION À PROPOS --- */
        .about-container { display: flex; align-items: center; gap: 50px; max-width: 1000px; margin: 0 auto; flex-wrap: wrap; }
        .about-text { flex: 1; min-width: 300px; }
        .about-img { flex: 1; min-width: 300px; border-radius: 8px; max-height: 400px; object-fit: cover; }
        /* --- SECTION OFFRES --- */
        .offers-container { display: flex; justify-content: center; gap: 30px; flex-wrap: wrap; }
        .offer-card { background: var(--light); border: 2px dashed var(--accent); padding: 30px; border-radius: 8px; text-align: center; width: 300px; }
        .offer-code { font-size: 24px; font-weight: bold; color: var(--primary); margin: 15px 0; letter-spacing: 2px; }
        /* --- SECTION CONTACT & PANIER --- */
        .contact-container { max-width: 600px; margin: 0 auto; text-align: center; }
        .contact-buttons { display: flex; flex-direction: column; gap: 15px; margin-top: 30px; }
        .contact-link { display: flex; align-items: center; justify-content: center; gap: 10px; padding: 15px; border-radius: 8px; color: white; font-weight: bold; font-size: 18px; }
        .btn-whatsapp { background: #25D366; }
        .btn-whatsapp:hover { background: #1ebd58; }
        .btn-phone { background: #3498db; }
        .btn-phone:hover { background: #2980b9; }
        /* --- FOOTER --- */
        footer { background: var(--primary); color: white; text-align: center; padding: 20px; margin-top: 50px; }
    </style>
</head>
<body>
    <header>
        <div class="logo">Mode élégance</div>
        <nav>
            <a href="#accueil">Accueil</a>
            <a href="#produits">Produits</a>
            <a href="#apropos">À Propos</a>
            <a href="#offres">Offres</a>
            <a href="#contact">Contact</a>
            <a href="#contact" class="cart-link">🛒 Commander</a>
        </nav>
    </header>
    <div id="accueil" class="section-page">
        <section class="hero">
            <h2>Élégance Masculine & Féminine</h2>
            <p>Découvrez notre nouvelle collection de pantalons et robes tendances</p><br>
            <a href="#produits" class="btn">Acheter Maintenant</a>
        </section>
        <h2 style="text-align:center; margin-top:40px;">Nos Catégories</h2>
        <div class="featured">
            <a href="#produits" class="feat-card">
                <img src="https://images.unsplash.com/photo-1624378439575-d8705ad7ae80?w=500" alt="Pantalons Homme">
                <div class="feat-text">Pantalons Hommes</div>
            </a>
            <a href="#produits" class="feat-card">
                <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=500" alt="Robes Femme">
                <div class="feat-text">Robes Femmes</div>
            </a>
        </div>
    </div>
    <div id="produits" class="section-page">
        <h1>Nos Articles en Ariary</h1>
        <div class="products-grid">
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1542272604-787c3835535d?w=400" alt="Pantalon Chino" class="product-img">
                <h3 class="product-title">Pantalon Chino Ajusté</h3>
                <p class="product-price">45 000 Ar</p>
                <ahref="https://wa.me/261386287680?text=Bonjour,%20je%20souhaite%20commander%20le%20Pantalon%20Chino%20Ajust%C3%A9%20%C3%A0%2045000%20Ar" target="_blank" class="btn">Commander sur WhatsApp</a>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1566174053879-31528523f8ae?w=400" alt="Robe d'été" class="product-img">
                <h3 class="product-title">Robe d'Été Fleurie</h3>
                <p class="product-price">60 000 Ar</p>
                <a href="https://wa.me/261386287680?text=Bonjour,%20je%20souhaite%20commander%20la%20Robe%20d%27%C3%89t%C3%A9%20Fleurie%20%C3%A0%2060000%20Ar" target="_blank" class="btn">Commander sur WhatsApp</a>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1479064555552-3ef4979f8908?w=400" alt="Pantalon Costume" class="product-img">
                <h3 class="product-title">Pantalon de Costume Slim</h3>
                <p class="product-price">65 000 Ar</p>
                <a href="https://wa.me/261386287680?text=Bonjour,%20je%20souhaite%20commander%20le%20Pantalon%20de%20Costume%20Slim%20%C3%A0%2075000%20Ar" target="_blank" class="btn">Commander sur WhatsApp</a>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1572804013309-59a88b7e92f1?w=400" alt="Robe de soirée" class="product-img">
                <h3 class="product-title">Robe de Soirée Élégante</h3>
                <p class="product-price">85 000 Ar</p>
                <a href="https://wa.me/261386287680?text=Bonjour,%20je%20souhaite%20commander%20la%20Robe%20de%20Soir%C3%A9e%20%C3%89l%C3%A9gante%20%C3%A0%2095000%20Ar" target="_blank" class="btn">Commander sur WhatsApp</a>
            </div>
        </div>
    </div>
    <div id="apropos" class="section-page">
        <h1>À Propos de Nous</h1>
        <div class="about-container">
            <div class="about-text">
                <h2>Qualité & Style depuis 2025</h2><br>
                <p>Bienvenue chez Mode élégance, votre destination mode incontournable à Madagascar. Nous sélectionnons avec passion les meilleurs pantalons pour hommes et les plus belles robes pour femmes.</p><br>
                <p>Notre mission est de vous proposer des vêtements confortables, durables et à la pointe de la tendance pour sublimer votre quotidien ou vos événements spéciaux.</p>
            </div>
            <img src="https://images.unsplash.com/photo-1470309864661-68328b2cd0a5?w=500" alt="Boutique" class="about-img">
        </div>
    </div>
    <div id="offres" class="section-page">
        <h1>Nos Offres Spéciales</h1>
        <div class="offers-container">
            <div class="offer-card">
                <h2>Offre de Bienvenue</h2>
                <p>Profitez de 5 000 Ar de réduction sur votre premier achat.</p>
                <div class="offer-code">CHIC05</div>
            </div>
            <div class="offer-card">
                <h2>Look Duo d'Été</h2>
                <p>1 Pantalon + 1 Robe achetés = Livraison Gratuite.</p>
                <div class="offer-code">DUOMADA</div>
            </div>
        </div>
    </div>
    <div id="contact" class="section-page">
        <h1>Contact & Commandes</h1>
        <div class="contact-container">
            <p>Pour valider votre panier, poser une question ou passer une commande personnalisée, contactez-nous directement :</p>
            <div class="contact-buttons">
                <a href="https://wa.me/261386287680?text=Bonjour%20Modeélegance,%20je%20souhaite%20discuter%20pour%20un%20achat" target="_blank" class="contact-link btn-whatsapp">
                    💬 Commander via WhatsApp
                </a>
                <a href="tel:+261386287680" class="contact-link btn-phone">
                    📞 Nous Appeler Directement
                </a>
            </div>
        </div>
    </div>
    <footer>
        <p>&copy; 2026 Mode élégance - Tous droits réservés.</p>
    </footer>
</body>
</html>
