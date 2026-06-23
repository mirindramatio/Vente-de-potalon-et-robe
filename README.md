
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mode Élégance · Pantalons & Robes</title>
    <!-- Font Awesome pour les icônes -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* ----- RESET & BASE ----- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
        }

        body {
            background: #faf8f6;
            color: #1e1e2a;
            line-height: 1.5;
        }

        /* ----- HEADER / NAV ----- */
        header {
            background: #1e1e2a;
            color: #fff;
            padding: 1rem 2rem;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
        }

        .logo {
            font-size: 1.6rem;
            font-weight: 600;
            letter-spacing: 1px;
        }
        .logo i {
            color: #e8b4b8;
            margin-right: 6px;
        }

        nav {
            display: flex;
            flex-wrap: wrap;
            gap: 0.2rem 1rem;
        }

        nav a {
            color: #f0ece6;
            text-decoration: none;
            font-weight: 500;
            padding: 0.4rem 0.8rem;
            border-radius: 40px;
            transition: all 0.2s;
            font-size: 0.95rem;
        }

        nav a:hover {
            background: #e8b4b8;
            color: #1e1e2a;
        }

        /* ----- LIEN ACTIF (statique, pour l'exemple) ----- */
        nav a.active {
            background: #e8b4b8;
            color: #1e1e2a;
        }

        .cart-icon {
            background: #2d2d3f;
            padding: 0.4rem 1rem;
            border-radius: 40px;
            display: flex;
            align-items: center;
            gap: 8px;
            border: 1px solid #3e3e54;
            cursor: default;
        }
        .cart-icon i {
            font-size: 1.2rem;
            color: #e8b4b8;
        }
        .cart-badge {
            background: #e8b4b8;
            color: #1e1e2a;
            border-radius: 40px;
            padding: 0 10px;
            font-weight: 700;
            font-size: 0.8rem;
            line-height: 1.6;
        }

        /* ----- PAGES ----- */
        .page {
            display: none;
            padding: 2rem 2rem 3rem;
            max-width: 1300px;
            margin: 0 auto;
        }

        /* Page active (par défaut : accueil) */
        #page-accueil {
            display: block;
        }

        h1 {
            font-size: 2.2rem;
            font-weight: 300;
            letter-spacing: -0.5px;
            margin-bottom: 0.5rem;
        }
        h1 span {
            font-weight: 600;
            color: #1e1e2a;
        }
        .subhead {
            color: #4a4a5a;
            margin-bottom: 2rem;
            border-left: 4px solid #e8b4b8;
            padding-left: 1rem;
        }

        /* ----- GRILLE PRODUITS ----- */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }

        .product-card {
            background: white;
            border-radius: 20px;
            padding: 1.2rem 1rem 1.5rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.02);
            transition: 0.25s ease;
            border: 1px solid #f0ede8;
            text-align: center;
        }
        .product-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 16px 30px rgba(0,0,0,0.04);
            border-color: #e8b4b8;
        }

        .product-card img {
            width: 100%;
            aspect-ratio: 1/1.1;
            object-fit: cover;
            border-radius: 14px;
            background: #f1ede8;
            margin-bottom: 0.8rem;
        }

        .product-card h3 {
            font-size: 1.1rem;
            font-weight: 600;
        }
        .product-card .price {
            font-size: 1.3rem;
            font-weight: 600;
            color: #1e1e2a;
            margin: 0.3rem 0;
        }
        .product-card .price small {
            font-weight: 300;
            font-size: 0.8rem;
            color: #5a5a6a;
        }
        .product-card .desc {
            font-size: 0.9rem;
            color: #5a5a6a;
            margin-bottom: 0.8rem;
        }

        .btn {
            background: #1e1e2a;
            border: none;
            color: white;
            padding: 0.5rem 1.4rem;
            border-radius: 60px;
            font-weight: 600;
            font-size: 0.9rem;
            cursor: default;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: 0.2s;
        }
        .btn:hover {
            background: #e8b4b8;
            color: #1e1e2a;
        }
        .btn-outline {
            background: transparent;
            border: 1.5px solid #1e1e2a;
            color: #1e1e2a;
        }
        .btn-outline:hover {
            background: #1e1e2a;
            color: white;
        }

        /* ----- OFFRE ----- */
        .offre-banner {
            background: #1e1e2a;
            color: #f0ece6;
            padding: 2.5rem;
            border-radius: 40px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            margin: 2rem 0;
        }
        .offre-banner h2 {
            font-size: 2rem;
            font-weight: 400;
        }
        .offre-banner .big {
            font-size: 2.5rem;
            font-weight: 700;
            color: #e8b4b8;
        }

        /* ----- CONTACT ----- */
        .contact-card {
            background: white;
            border-radius: 32px;
            padding: 2rem 2.5rem;
            border: 1px solid #e8e2da;
            max-width: 600px;
            margin: 2rem 0;
        }
        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            font-size: 1.2rem;
            padding: 0.8rem 0;
            border-bottom: 1px solid #eeeae4;
        }
        .contact-item i {
            width: 2rem;
            color: #e8b4b8;
            font-size: 1.6rem;
        }
        .contact-item a {
            color: #1e1e2a;
            text-decoration: none;
            font-weight: 500;
        }
        .contact-item a:hover {
            color: #e8b4b8;
        }

        /* ----- PANIER (sidebar statique) ----- */
        .cart-sidebar {
            position: fixed;
            top: 0;
            right: 0;
            width: 380px;
            height: 100vh;
            background: white;
            box-shadow: -8px 0 30px rgba(0,0,0,0.08);
            padding: 2rem 1.5rem;
            z-index: 999;
            overflow-y: auto;
            border-left: 1px solid #e8e2da;
            pointer-events: none; /* désactivé : pas de JS */
            opacity: 0.95;
        }
        .cart-sidebar h2 {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid #f0ede8;
            padding-bottom: 1rem;
        }
        .cart-sidebar .close-cart {
            background: none;
            border: none;
            font-size: 1.8rem;
            cursor: default;
            color: #4a4a5a;
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            padding: 0.8rem 0;
            border-bottom: 1px solid #f0ede8;
        }
        .cart-total {
            font-weight: 700;
            font-size: 1.4rem;
            margin: 1.5rem 0;
        }
        .cart-empty {
            color: #7a7a8a;
            text-align: center;
            padding: 2rem 0;
        }

        /* ----- FOOTER ----- */
        footer {
            text-align: center;
            border-top: 1px solid #e8e2da;
            padding: 1.8rem;
            color: #5a5a6a;
            font-size: 0.9rem;
            margin-top: 2rem;
        }

        /* ----- RESPONSIVE ----- */
        @media (max-width: 700px) {
            header { flex-direction: column; gap: 0.8rem; align-items: stretch; }
            nav { justify-content: center; }
            .cart-icon { align-self: center; }
            .page { padding: 1rem; }
            .offre-banner { flex-direction: column; gap: 1rem; text-align: center; }
            .contact-card { padding: 1.5rem; }
            .cart-sidebar { width: 100%; right: 0; position: relative; height: auto; pointer-events: auto; margin-top: 2rem; border-left: none; border-top: 1px solid #e8e2da; }
        }

        /* petites retouches */
        .page#page-offre .product-card {
            border: 2px dashed #d6cec4;
        }
        .page#page-offre .product-card .price {
            color: #b33a4a;
        }
    </style>
</head>
<body>

<!-- ===== HEADER ===== -->
<header>
    <div class="logo"><i class="fas fa-tshirt"></i> Mode·Élégance</div>
    <nav>
        <a href="#page-accueil" class="active"><i class="fas fa-home"></i> Accueil</a>
        <a href="#page-produits"><i class="fas fa-archive"></i> Produits</a>
        <a href="#page-offre"><i class="fas fa-tags"></i> Offres</a>
        <a href="#page-contact"><i class="fas fa-envelope"></i> Contact</a>
        <a href="#page-a-propos"><i class="fas fa-info-circle"></i> À propos</a>
    </nav>
    <div class="cart-icon">
        <i class="fas fa-shopping-bag"></i>
        <span class="cart-badge">3</span>
        <span style="font-size:0.8rem; opacity:0.7;">Panier</span>
    </div>
</header>

<!-- ============================================================ -->
<!-- PAGE ACCUEIL -->
<div class="page" id="page-accueil">
    <h1><span>Pantalons & Robes</span> · Élégance au quotidien</h1>
    <div class="subhead">Découvrez notre collection tendance, des pièces uniques pour chaque style.</div>
    <div class="product-grid">
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center" alt="Pantalon noir">
            <h3>Pantalon Taille Haute</h3>
            <div class="price">185 000 <small>Ar</small></div>
            <div class="desc">Coupe fluide, noir élégant</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-100" alt="Robe fleurie">
            <h3>Robe Fleurie</h3>
            <div class="price">210 000 <small>Ar</small></div>
            <div class="desc">Imprimé floral, manches ballon</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-50" alt="Pantalon carotte">
            <h3>Pantalon Carotte</h3>
            <div class="price">165 000 <small>Ar</small></div>
            <div class="desc">Beige, ceinture élastique</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
    </div>
    <div style="text-align:center; margin:1rem 0;"><i class="fas fa-arrow-down" style="color:#b3a89e;"></i> Nouvelle collection</div>
</div>

<!-- PAGE PRODUITS -->
<div class="page" id="page-produits">
    <h1><span>Nos produits</span></h1>
    <div class="subhead">Pantalons, robes et plus encore.</div>
    <div class="product-grid">
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center" alt="Pantalon noir">
            <h3>Pantalon Taille Haute</h3>
            <div class="price">35 000 <small>Ar</small></div>
            <div class="desc">Noir, coupe fluide</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-100" alt="Robe fleurie">
            <h3>Robe Fleurie</h3>
            <div class="price">42 000 <small>Ar</small></div>
            <div class="desc">Imprimé floral</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-50" alt="Pantalon carotte">
            <h3>Pantalon Carotte</h3>
            <div class="price">50 000 <small>Ar</small></div>
            <div class="desc">Beige, élastique</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=20" alt="Robe portefeuille">
            <h3>Robe Portefeuille</h3>
            <div class="price">70 000 <small>Ar</small></div>
            <div class="desc">Robe en soie</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-30" alt="Pantalon palazo">
            <h3>Pantalon Palazo</h3>
            <div class="price">75 000 <small>Ar</small></div>
            <div class="desc">Blanc, large</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-70" alt="Robe chemisier">
            <h3>Robe Chemisier</h3>
            <div class="price">65 000 <small>Ar</small></div>
            <div class="desc">Bleu ciel</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
    </div>
</div>

<!-- PAGE OFFRE -->
<div class="page" id="page-offre">
    <h1><span>Offres spéciales</span> 🔥</h1>
    <div class="subhead">Profitez de prix réduits sur une sélection limitée.</div>
    <div class="offre-banner">
        <div><h2><i class="fas fa-percent"></i> Jusqu'à -30%</h2><p>sur les robes et pantalons en stock</p></div>
        <div><span class="big">100 000 Ar</span> <span style="font-size:1.2rem;"> le lot de 3</span></div>
    </div>
    <div class="product-grid">
        <!-- Offre 1 -->
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center" alt="Pantalon taille haute">
            <h3>Pantalon Taille Haute</h3>
            <div class="price">48 000 <small>Ar</small> <span style="text-decoration:line-through; font-size:0.8rem; color:#a00;">85 000 Ar</span></div>
            <div class="desc">Noir · -20%</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-100" alt="Robe fleurie">
            <h3>Robe Fleurie</h3>
            <div class="price">68 000 <small>Ar</small> <span style="text-decoration:line-through; font-size:0.8rem; color:#a00;">88 000 Ar</span></div>
            <div class="desc">Imprimé · -20%</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
        <div class="product-card">
            <img src="https://images.unsplash.com/photo-1595777457583-95e059d581b8?w=400&h=500&fit=crop&crop=center&sat=-50" alt="Pantalon carotte">
            <h3>Pantalon Carotte</h3>
            <div class="price">102 000 <small>Ar</small> <span style="text-decoration:line-through; font-size:0.8rem; color:#a00;">95 000 Ar</span></div>
            <div class="desc">Beige · -20%</div>
            <button class="btn"><i class="fas fa-plus"></i> Ajouter</button>
        </div>
    </div>
</div>

<!-- PAGE CONTACT -->
<div class="page" id="page-contact">
    <h1><span>Contactez-nous</span></h1>
    <div class="subhead">Nous sommes à votre écoute.</div>
    <div class="contact-card">
        <div class="contact-item"><i class="fab fa-whatsapp"></i> <a href="https://wa.me/261340000000?text=Bonjour%2C%20je%20souhaite%20commander%20sur%20Mode%20%C3%89l%C3%A9gance" target="_blank">+261 34 00 000 00</a></div>
        <div class="contact-item"><i class="fas fa-phone-alt"></i> <a href="tel:+261340000000">+261 34 00 000 00</a></div>
        <div class="contact-item"><i class="fas fa-envelope"></i> <a href="mailto:contact@mode-elegance.mg">contact@mode-elegance.mg</a></div>
        <div class="contact-item"><i class="fas fa-map-pin"></i> Antananarivo, Madagascar</div>
    </div>
    <p style="color:#4a4a5a;">Réponse sous 24h, 7j/7.</p>
</div>

<!-- PAGE À PROPOS -->
<div class="page" id="page-a-propos">
    <h1><span>À propos</span></h1>
    <div class="subhead">Mode·Élégance, la passion du vêtement.</div>
    <div style="background:white; border-radius:32px; padding:2rem; border:1px solid #e8e2da; max-width:700px;">
        <p style="font-size:1.1rem;">Depuis 2018, nous sélectionnons des pantalons et robes alliant confort et tendance. Chaque pièce est choisie pour sa qualité et son originalité.</p>
        <p style="margin-top:1rem;"><i class="fas fa-check-circle" style="color:#e8b4b8;"></i> Paiement sécurisé</p>
        <p><i class="fas fa-check-circle" style="color:#e8b4b8;"></i> Livraison à Madagascar et îles</p>
        <p><i class="fas fa-check-circle" style="color:#e8b4b8;"></i> Service client réactif</p>
        <p style="margin-top:1rem; font-style:italic;">"La mode est une forme d'expression."</p>
    </div>
</div>

<!-- ===== PANIER (sidebar statique) ===== -->
<div class="cart-sidebar">
    <h2>
        <span><i class="fas fa-shopping-bag"></i> Mon panier</span>
        <button class="close-cart">&times;</button>
    </h2>
    <div>
        <div class="cart-item"><div><strong>Pantalon Taille Haute</strong> x1</div><div>95 000 Ar <span style="color:#b33a4a; margin-left:8px;"><i class="fas fa-trash-alt"></i></span></div></div>
        <div class="cart-item"><div><strong>Robe Fleurie</strong> x2</div><div>120 000 Ar <span style="color:#b33a4a; margin-left:8px;"><i class="fas fa-trash-alt"></i></span></div></div>
    </div>
    <div class="cart-total">Total : 130 000 Ar</div>
    <button class="btn" style="width:100%; justify-content:center;"><i class="fab fa-whatsapp"></i> Commander via WhatsApp</button>
    <p style="font-size:0.8rem; margin-top:0.8rem; color:#7a7a8a;"><i class="fas fa-phone"></i> +261 34 00 000 00</p>
</div>

<!-- ===== FOOTER ===== -->
<footer>
    <p>© 2026 Mode·Élégance · Tous droits réservés · <i class="fas fa-heart" style="color:#e8b4b8;"></i> Madagascar</p>
    <p style="font-size:0.8rem; margin-top:0.3rem;">Prix en Ariary (Ar) · Paiement à la livraison</p>
</footer>

<!-- ===== PETITE NAVIGATION PAR ANCRES (sans JS) ===== -->
<!-- Les liens du menu utilisent des ancres #page-xxx, le comportement par défaut du navigateur affiche la page correspondante -->
<!-- Pour que les pages s'affichent correctement, on utilise du CSS : #page-accueil est visible par défaut, les autres sont cachées -->
<!-- On ajoute un petit style pour que la page ciblée par l'ancre s'affiche (grâce à :target) -->
<style>
    /* Quand une page est ciblée par l'URL (ex: #page-produits), on l'affiche */
    .page:target {
        display: block;
    }
    /* On masque la page accueil par défaut si une autre est ciblée */
    .page:target ~ #page-accueil {
        display: none;
    }
    /* Mais si aucune page n'est ciblée, on affiche l'accueil */
    body:not(:has(:target)) #page-accueil {
        display: block;
    }
    /* On s'assure que si une page est ciblée, l'accueil est caché */
    body:has(:target) #page-accueil {
        display: none;
    }
    /* Petite correction pour que la page ciblée soit bien affichée */
    .page:target {
        display: block !important;
    }
    /* Pour que le lien actif soit stylé, on ajoute une classe active manuellement sur le lien correspondant */
    /* On utilise un peu de JS pour ça ? Non, on va juste mettre la classe active sur le lien Accueil par défaut, et on laisse l'utilisateur cliquer */
    /* On va plutôt utiliser un sélecteur d'attribut pour styler le lien actif en fonction de l'URL */
    nav a[href="#page-accueil"] { /* par défaut actif */ }
    /* On va gérer ça proprement avec un peu de CSS : le lien dont le href correspond à l'ID ciblé */
    /* On utilise :target pour modifier le lien parent ? Pas facile sans JS. On va juste laisser les liens sans classe active dynamique, c'est statique */
    /* On va remettre la classe active sur le lien Accueil en dur */
</style>

<!-- On remet le lien Accueil actif par défaut -->
<!-- On va ajouter un petit script nul pour que le lien actif change ? Non, on reste sans JS -->
<!-- On va simplement laisser le style actif sur le premier lien -->
</body>
</html>
