<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ECO-REBORN | Conciencia Urbana & Upcycling</title>
    
    <!-- Tipografías Premium -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;700&family=Urbanist:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <!-- Iconos (FontAwesome para el logo de Instagram) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>
        /* --- ESTILEADO CLARO --- */
        :root {
            --clr-primary: #43a047;     /* Verde Claro Principal */
            --clr-light: #81c784;       /* Verde Más Claro */
            --clr-bg: #ffffff;          /* Fondo Puro Blanco */
            --clr-card: #f1f8e9;        /* Fondo Verde Menta muy sutil */
            --clr-dark: #1a1a1a;        /* Texto Principal */
            --clr-muted: #666666;       /* Texto Secundario */
            --clr-white: #ffffff;
            --clr-border: #e0e0e0;
            --speed: 0.3s;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Urbanist', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--clr-bg) !important;
            color: var(--clr-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        h1, h2, h3, .logo {
            font-family: 'Space Grotesk', sans-serif;
            text-transform: uppercase;
            letter-spacing: -0.5px;
        }

        /* --- NAVBAR --- */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            border-bottom: 1px solid var(--clr-border);
            position: sticky;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--clr-dark);
            text-decoration: none;
        }

        .logo span { color: var(--clr-primary); }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.5rem;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--clr-muted);
            font-weight: 600;
            font-size: 1.1rem;
            transition: var(--speed);
        }

        .nav-links a:hover { color: var(--clr-primary); }

        .cart-icon-btn {
            background: none;
            border: none;
            color: var(--clr-dark);
            font-size: 1.3rem;
            cursor: pointer;
            position: relative;
        }

        #cart-count {
            position: absolute;
            top: -10px;
            right: -12px;
            background-color: var(--clr-primary);
            color: var(--clr-white);
            font-size: 0.75rem;
            padding: 2px 6px;
            border-radius: 50%;
        }

        /* --- HERO --- */
        .hero-section {
            background: linear-gradient(rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0.95)), 
                        url('https://images.unsplash.com/photo-1541099649105-f69ad21f3246?q=80&w=1200&auto=format&fit=crop') no-repeat center center/cover;
            height: 60vh;
            display: flex;
            align-items: center;
        }

        .hero-content h1 {
            font-size: 4.5rem;
            line-height: 0.9;
            margin-bottom: 1.5rem;
            color: var(--clr-dark);
        }

        .hero-content p {
            font-size: 1.2rem;
            color: var(--clr-muted);
            max-width: 600px;
            margin-bottom: 2.5rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--clr-primary);
            color: var(--clr-white);
            padding: 1rem 2.5rem;
            text-decoration: none;
            font-weight: 700;
            border-radius: 4px;
            transition: var(--speed);
            border: none;
            cursor: pointer;
            text-transform: uppercase;
            font-family: 'Space Grotesk', sans-serif;
        }

        .btn:hover {
            background-color: var(--clr-light);
            transform: translateY(-3px);
        }

        /* --- SECCIONES --- */
        .section-padding { padding: 5rem 0; }

        .section-title {
            font-size: 2.3rem;
            color: var(--clr-dark);
            margin-bottom: 3rem;
            border-left: 5px solid var(--clr-primary);
            padding-left: 20px;
        }

        .concept-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .concept-text p {
            font-size: 1.15rem;
            color: var(--clr-muted);
            margin-bottom: 1.5rem;
        }

        .accent { color: var(--clr-primary); font-weight: 600; }

        .concept-image-wrapper img {
            width: 100%;
            height: 380px;
            object-fit: cover;
            border-radius: 8px;
            border: 1px solid var(--clr-border);
        }

        /* --- NUEVA SECCIÓN: ORIGEN DEL DISEÑO --- */
        .origin-section {
            background-color: var(--clr-card);
        }

        /* --- PRODUCTOS --- */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 2.5rem;
        }

        .product-card {
            background-color: var(--clr-bg);
            border: 1px solid var(--clr-border);
            border-radius: 12px;
            overflow: hidden;
            transition: var(--speed);
            display: flex;
            flex-direction: column;
        }

        .product-card:hover {
            transform: translateY(-10px);
            border-color: var(--clr-primary);
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
        }

        .product-img-holder {
            width: 100%;
            height: 380px;
            overflow: hidden;
            position: relative;
            background-color: var(--clr-white);
        }

        .product-img-holder img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--clr-primary);
            color: var(--clr-white);
            padding: 4px 12px;
            font-size: 0.8rem;
            font-weight: 700;
            border-radius: 4px;
            text-transform: uppercase;
        }

        .product-info { padding: 2rem; display: flex; flex-direction: column; flex-grow: 1; }
        .product-info h3 { font-size: 1.5rem; color: var(--clr-dark); margin-bottom: 0.5rem; }
        .product-desc { color: var(--clr-muted); font-size: 0.95rem; margin-bottom: 1.5rem; flex-grow: 1; }
        
        .product-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 1.5rem;
            border-top: 1px solid var(--clr-border);
        }

        .product-price { font-family: 'Space Grotesk', sans-serif; font-size: 1.7rem; font-weight: 700; color: var(--clr-dark); }
        .btn-sm { padding: 0.6rem 1.2rem; font-size: 0.9rem; }

        /* --- CARRITO SIDEBAR --- */
        .cart-sidebar {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100vh;
            background-color: var(--clr-white);
            border-left: 1px solid var(--clr-border);
            z-index: 2000;
            box-shadow: -10px 0 30px rgba(0,0,0,0.05);
            transition: var(--speed);
            padding: 2.5rem;
            display: flex;
            flex-direction: column;
        }

        .cart-sidebar.open { right: 0; }
        .cart-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 2rem; border-bottom: 1px solid var(--clr-border); padding-bottom: 1rem; }
        .close-cart { background: none; border: none; color: var(--clr-muted); font-size: 1.5rem; cursor: pointer; }
        .cart-items-container { flex-grow: 1; overflow-y: auto; }
        
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            background: var(--clr-white);
            padding: 10px;
            border-radius: 6px;
            border: 1px solid var(--clr-border);
        }

        .cart-footer-panel { border-top: 1px solid var(--clr-border); padding-top: 1.5rem; }
        .total-row { display: flex; justify-content: space-between; font-size: 1.3rem; font-family: 'Space Grotesk', sans-serif; margin-bottom: 1.5rem; color: var(--clr-dark); }

        /* --- FOOTER --- */
        footer { background-color: var(--clr-card); border-top: 1px solid var(--clr-border); padding: 4rem 0 2rem 0; }
        .footer-grid { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 2rem; }
        .footer-logo { font-size: 1.8rem; font-weight: 700; color: var(--clr-dark); text-decoration: none; }
        .footer-logo span { color: var(--clr-primary); }
        
        /* Enlace de Instagram Estilizado */
        .footer-social {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .instagram-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background-color: var(--clr-primary);
            color: var(--clr-white);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            font-size: 1.4rem;
            text-decoration: none;
            transition: var(--speed);
        }
        .instagram-link:hover {
            background-color: var(--clr-light);
            transform: scale(1.1);
        }
        .social-text {
            font-weight: 600;
            color: var(--clr-dark);
            font-size: 1rem;
        }

        .footer-copy { text-align: center; color: var(--clr-muted); font-size: 0.9rem; margin-top: 3rem; border-top: 1px solid var(--clr-border); padding-top: 1.5rem; }

        @media (max-width: 768px) {
            .concept-grid { grid-template-columns: 1fr; gap: 2rem; }
            .hero-content h1 { font-size: 3rem; }
            .cart-sidebar { width: 100%; right: -100%; }
            .nav-links { display: none; }
            .footer-grid { flex-direction: column; text-align: center; }
        }
    </style>
</head>
<body>

    <!-- NAVEGACIÓN -->
    <header>
        <div class="container navbar">
            <a href="#inicio" class="logo">ECO-<span>REBORN</span></a>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#concepto">Proceso</a></li>
                <li><a href="#origen">Origen</a></li>
                <li><a href="#productos">Productos</a></li>
                <li>
                    <button class="cart-icon-btn" onclick="toggleCart()">
                        <i class="fa-solid fa-bag-shopping"></i>
                        <span id="cart-count">0</span>
                    </button>
                </li>
            </ul>
        </div>
    </header>

    <!-- BANNER PRINCIPAL -->
    <section id="inicio" class="hero-section">
        <div class="container">
            <div class="hero-content">
                <h1>Mocarti Design</h1>
                <p>Estética upcycled de alta resistencia. Creamos piezas únicas a partir de mezclilla denim recuperada y materiales de lona sintética industrial.</p>
                <a href="#productos" class="btn">Explorar Tienda</a>
            </div>
        </div>
    </section>

    <!-- PROCESO -->
    <section id="concepto" class="section-padding">
        <div class="container concept-grid">
            <div class="concept-text">
                <h2 class="section-title">El Arte del Upcycling</h2>
                <p>No creamos materiales nuevos; transformamos los que ya cumplieron un ciclo. Seleccionamos cuidadosamente <span class="accent">telas de jean densas</span> y las fusionamos con soportes impermeables de PVC reciclado.</p>
                <p>Cada accesorio es cosido artesanalmente en Lima, garantizando un patrón geométrico exclusivo y una durabilidad extrema para el uso diario en la ciudad.</p>
            </div>
            <div class="concept-image-wrapper">
                <img src="blob:https://web.whatsapp.com/13076233-df3b-4591-96d4-5fcc090ed8a0" alt="Textura Denim Reciclado Sostenible">
            </div>
        </div>
    </section>

    <!-- NUEVA SECCIÓN: POR QUÉ SE CREÓ ESTA MOCHILA -->
    <section id="origen" class="section-padding origin-section">
        <div class="container concept-grid">
            <div class="concept-image-wrapper">
                <!-- Imagen representativa de diseño, costura y patronaje industrial libre -->
                <img src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?q=80&w=600&auto=format&fit=crop" alt="Diseño y Confección del Modelo Urban">
            </div>
            <div class="concept-text">
                <h2 class="section-title">Origen de la Mochila Urban</h2>
                <p>Este modelo nació bajo una premisa clara: <span class="accent">responder al desgaste del entorno urbano moderno</span> sin generar más desperdicios en el planeta.</p>
                <p>Las mochilas comerciales suelen romperse rápido en las costuras y bases debido al peso diario. Diseñamos este formato híbrido integrando el <strong>grosor estructural de los vaqueros recuperados</strong> en el cuerpo superior, y una base impenetrable de <strong>PVC impermeable</strong> en la parte inferior.</p>
                <p>El resultado es una mochila ligera, de formato ergonómico, resistente al clima de Lima y completamente irrepetible en sus tonalidades.</p>
            </div>
        </div>
    </section>

    <!-- CATÁLOGO -->
    <section id="productos" class="section-padding" style="background-color: var(--clr-white);">
        <div class="container">
            <h2 class="section-title">Catálogo de Productos</h2>
            <div class="product-grid">

                <!-- PRODUCTO 1 -->
                <div class="product-card">
                    <div class="product-img-holder">
                        <span class="product-badge">Hecho a Mano</span>
                        <img src="https://images.unsplash.com/photo-1622560480605-d83c853bc5c3?q=80&w=600&auto=format&fit=crop" alt="Mochila Diseño Urbano Upcycled">
                    </div>
                    <div class="product-info">
                        <h3>Mochila Urban Denim & PVC</h3>
                        <p class="product-desc">Compartimento principal espacioso e impermeable. Diseñada combinando secciones de lona reciclada industrial de PVC negro y acabados frontales en denim azul clásico reforzado. Logotipo mocarti cosido al frente.</p>
                        <div class="product-footer">
                            <div class="product-price">S/ 185.00</div>
                            <button class="btn btn-sm" onclick="addToCart('Mochila Urban Denim & PVC', 185)">Añadir</button>
                        </div>
                    </div>
                </div>

                <!-- PRODUCTO 2 -->
                <div class="product-card">
                    <div class="product-img-holder">
                        <span class="product-badge">Impermeable</span>
                        <img src="https://images.unsplash.com/photo-1544816155-12df9643f363?q=80&w=600&auto=format&fit=crop" alt="Cartuchera Pouch de Textura Industrial">
                    </div>
                    <div class="product-info">
                        <h3>Cartuchera Pouch Utility</h3>
                        <p class="product-desc">Estuche cilíndrico de alta resistencia para herramientas, cables o útiles escolares. Base inferior de PVC verde oliva anti-rasgaduras y costura superior en tela de jean azul denim. Cierre negro grueso.</p>
                        <div class="product-footer">
                            <div class="product-price">S/ 49.00</div>
                            <button class="btn btn-sm" onclick="addToCart('Cartuchera Pouch Utility', 49)">Añadir</button>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- CARRITO SIDEBAR -->
    <div id="sidebar-cart" class="cart-sidebar">
        <div class="cart-header">
            <h3>Tu Carrito</h3>
            <button class="close-cart" onclick="toggleCart()"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div id="cart-items" class="cart-items-container">
            <p style="color: var(--clr-muted); text-align: center; margin-top: 2rem;">El carrito está vacío</p>
        </div>
        <div class="cart-footer-panel">
            <div class="total-row">
                <span>Total:</span>
                <span id="cart-total-price">S/ 0.00</span>
            </div>
            <button class="btn" style="width: 100%;" onclick="checkout()">Comprar por WhatsApp</button>
        </div>
    </div>

    <!-- PIE DE PÁGINA (CON ENLACE A INSTAGRAM) -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <a href="#inicio" class="footer-logo">ECO-<span>REBORN</span></a>
                
                <!-- Botón de Instagram Comercial -->
                <div class="footer-social">
                    <span class="social-text">Síguenos en Instagram:</span>
                    <a href="https://www.instagram.com/ecore_born/" target="_blank" class="instagram-link" title="Visitar Instagram de ECO-REBORN">
                        <i class="fa-brands fa-instagram"></i>
                    </a>
                </div>
            </div>
            <div class="footer-copy">
                Mocarti Concept © 2026 - Confección de alta resistencia - Sostenibilidad desde Lima, Perú.
            </div>
        </div>
    </footer>

    <script>
        let cart = [];
        function toggleCart() { document.getElementById('sidebar-cart').classList.toggle('open'); }
        
        function addToCart(name, price) {
            cart.push({ name, price });
            updateCartUI();
            document.getElementById('sidebar-cart').classList.add('open');
        }

        function updateCartUI() {
            document.getElementById('cart-count').innerText = cart.length;
            const container = document.getElementById('cart-items');
            if (cart.length === 0) {
                container.innerHTML = `<p style="color: var(--clr-muted); text-align: center; margin-top: 2rem;">El carrito está vacío</p>`;
                document.getElementById('cart-total-price').innerText = 'S/ 0.00';
                return;
            }
            container.innerHTML = '';
            let total = 0;
            cart.forEach((item, index) => {
                total += item.price;
                container.innerHTML += `
                    <div class="cart-item">
                        <div>
                            <h4 style="color: var(--clr-dark); font-size: 1.1rem;">${item.name}</h4>
                            <span style="color: var(--clr-primary); font-weight: bold;">S/ ${item.price}.00</span>
                        </div>
                        <button onclick="removeItem(${index})" style="background:none; border:none; color: #ff5252; cursor:pointer;"><i class="fa-solid fa-trash-can"></i></button>
                    </div>`;
            });
            document.getElementById('cart-total-price').innerText = `S/ ${total}.00`;
        }

        function removeItem(index) { cart.splice(index, 1); updateCartUI(); }
        function checkout() { alert("Redireccionando al WhatsApp de ECO-REBORN para coordinar tu entrega."); cart = []; updateCartUI(); toggleCart(); }
    </script>
</body>
</html>
