<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ECO-REBORN | Moda Circular & Upcycled Perú</title>
    
    <!-- Tipografías Premium -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;700&family=Urbanist:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <!-- Iconos -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>
        /* --- VARIABLES Y CONFIGURACIÓN PREMIUM --- */
        :root {
            --primary-color: #2e7d32;
            --primary-dark: #1b5e20;
            --bg-dark: #0F0F0F;
            --bg-card: #1A1A1A;
            --text-light: #E8E5D8;
            --text-muted: #A0A0A0;
            --white: #FFFFFF;
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Urbanist', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-light);
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
            background-color: rgba(15, 15, 15, 0.9);
            border-bottom: 1px solid #222;
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
            color: var(--white);
            text-decoration: none;
        }

        .logo span {
            color: var(--primary-color);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.5rem;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-muted);
            font-weight: 600;
            font-size: 1.1rem;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--white);
        }

        .cart-icon-btn {
            background: none;
            border: none;
            color: var(--text-light);
            font-size: 1.3rem;
            cursor: pointer;
            position: relative;
        }

        #cart-count {
            position: absolute;
            top: -10px;
            right: -12px;
            background-color: var(--primary-color);
            color: var(--white);
            font-size: 0.75rem;
            padding: 2px 6px;
            border-radius: 50%;
            font-family: 'Space Grotesk', sans-serif;
        }

        /* --- HERO --- */
        .hero {
            background: linear-gradient(rgba(15,15,15,0.7), rgba(15,15,15,0.95)), 
                        url('https://images.unsplash.com/photo-1544816155-12df9643f363?q=80&w=1200&auto=format&fit=crop') no-repeat center center/cover;
            height: 85vh;
            display: flex;
            align-items: center;
            position: relative;
        }

        .hero-content h1 {
            font-size: 5rem;
            line-height: 0.9;
            margin-bottom: 1.5rem;
            color: var(--white);
        }

        .hero-content p {
            font-size: 1.3rem;
            color: var(--text-muted);
            max-width: 650px;
            margin-bottom: 2.5rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: var(--white);
            padding: 1rem 2.5rem;
            text-decoration: none;
            font-weight: 700;
            border-radius: 4px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            text-transform: uppercase;
            font-family: 'Space Grotesk', sans-serif;
        }

        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
        }

        /* --- SECCIONES ESTRATÉGICAS --- */
        .section-padding {
            padding: 6rem 0;
        }

        .section-title {
            font-size: 2.5rem;
            color: var(--white);
            margin-bottom: 3rem;
            border-left: 5px solid var(--primary-color);
            padding-left: 20px;
        }

        /* Concepto Split */
        .concept-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .concept-text p {
            font-size: 1.15rem;
            color: var(--text-muted);
            margin-bottom: 1.5rem;
        }

        .accent { color: var(--primary-color); font-weight: 600; }

        .image-collage {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        .image-collage img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 8px;
            border: 1px solid #222;
        }

        /* --- STATS GRID --- */
        .stats-bg { background-color: #0A0A0A; }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            text-align: center;
        }

        .stat-item .number {
            font-size: 5rem;
            font-weight: 700;
            color: var(--primary-color);
            font-family: 'Space Grotesk', sans-serif;
            line-height: 1;
        }

        .stat-item p {
            font-size: 1.1rem;
            color: var(--text-muted);
            margin-top: 0.5rem;
        }

        /* --- CATÁLOGO DE PRODUCTOS --- */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
        }

        .product-card {
            background-color: var(--bg-card);
            border: 1px solid #222;
            border-radius: 12px;
            overflow: hidden;
            transition: var(--transition);
            display: flex;
            flex-direction: column;
        }

        .product-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-color);
        }

        .product-img-holder {
            width: 100%;
            height: 350px;
            overflow: hidden;
            position: relative;
            background-color: #050505;
        }

        .product-img-holder img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .product-card:hover .product-img-holder img {
            transform: scale(1.05);
        }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--primary-color);
            color: var(--white);
            padding: 4px 12px;
            font-family: 'Space Grotesk', sans-serif;
            font-size: 0.8rem;
            font-weight: 700;
            border-radius: 4px;
        }

        .product-info {
            padding: 2rem;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .product-info h3 {
            font-size: 1.5rem;
            color: var(--white);
            margin-bottom: 0.5rem;
        }

        .product-desc {
            color: var(--text-muted);
            font-size: 1rem;
            margin-bottom: 1.5rem;
            flex-grow: 1;
        }

        .product-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: auto;
            padding-top: 1.5rem;
            border-top: 1px solid #222;
        }

        .product-price {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--white);
        }

        .btn-sm {
            padding: 0.6rem 1.5rem;
            font-size: 0.9rem;
        }

        /* --- PANEL DE CARRITO LATERAL --- */
        .cart-sidebar {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100vh;
            background-color: var(--bg-card);
            border-left: 1px solid #222;
            z-index: 2000;
            box-shadow: -10px 0 30px rgba(0,0,0,0.5);
            transition: var(--transition);
            padding: 2.5rem;
            display: flex;
            flex-direction: column;
        }

        .cart-sidebar.open {
            right: 0;
        }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            border-bottom: 1px solid #222;
            padding-bottom: 1rem;
        }

        .close-cart {
            background: none;
            border: none;
            color: var(--text-muted);
            font-size: 1.5rem;
            cursor: pointer;
        }

        .cart-items-container {
            flex-grow: 1;
            overflow-y: auto;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            background: #111;
            padding: 10px;
            border-radius: 6px;
        }

        .cart-footer-panel {
            border-top: 1px solid #222;
            padding-top: 1.5rem;
        }

        .total-row {
            display: flex;
            justify-content: space-between;
            font-size: 1.3rem;
            font-family: 'Space Grotesk', sans-serif;
            margin-bottom: 1.5rem;
        }

        /* --- FOOTER --- */
        footer {
            background-color: #0A0A0A;
            border-top: 1px solid #222;
            padding: 4rem 0 2rem 0;
        }

        .footer-grid {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 3rem;
        }

        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            color: var(--white);
            text-decoration: none;
        }

        .footer-logo span { color: var(--primary-color); }

        .footer-socials a {
            color: var(--text-muted);
            font-size: 1.5rem;
            margin-left: 1.5rem;
            transition: var(--transition);
        }

        .footer-socials a:hover { color: var(--primary-color); }

        .footer-copy {
            text-align: center;
            color: #555;
            font-size: 0.9rem;
            border-top: 1px solid #111;
            padding-top: 2rem;
        }

        @media (max-width: 768px) {
            .concept-grid { grid-template-columns: 1fr; gap: 2rem; }
            .stats-grid { grid-template-columns: 1fr; gap: 3rem; }
            .hero-content h1 { font-size: 3.2rem; }
            .cart-sidebar { width: 100%; right: -100%; }
            .footer-grid { flex-direction: column; gap: 2rem; text-align: center; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>

    <!-- MENÚ / NAVEGACIÓN -->
    <header>
        <div class="container navbar">
            <a href="#inicio" class="logo">ECO-<span>REBORN</span></a>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#concepto">Concepto</a></li>
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

    <!-- HERO SECTION -->
    <section id="inicio" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>ECO-REBORN</h1>
                <p>Moda Up-cycled con Impacto Circular. Transformamos residuos de lona publicitaria y PVC en el futuro del estilo urbano de Lima.</p>
                <a href="#productos" class="btn">Explorar Catálogo</a>
            </div>
        </div>
    </section>

    <!-- MÉTRICAS DE IMPACTO -->
    <section class="section-padding stats-bg">
        <div class="container stats-grid">
            <div class="stat-item">
                <div class="number">500</div>
                <p>Años tarda el PVC de un banner publicitario tradicional en degradarse.</p>
            </div>
            <div class="stat-item">
                <div class="number">100%</div>
                <p>Impermeable, ultrarresistente y de patrón gráfico irrepetible.</p>
            </div>
            <div class="stat-item">
                <div class="number">0%</div>
                <p>Residuos plásticos añadidos. Economía e industria circular pura.</p>
            </div>
        </div>
    </section>

    <!-- CONCEPTO CON ENLACES ESTABLES -->
    <section id="concepto" class="section-padding">
        <div class="container concept-grid">
            <div class="concept-text">
                <h2 class="section-title">Diseño con Conciencia</h2>
                <p>Cada año, toneladas de gigantografías publicitarias terminan en vertederos peruanos. Interceptamos este material de alta ingeniería antes de que sea basura.</p>
                <p>A través de un proceso artesanal de corte y confección local, las texturas gráficas aleatorias dan vida a accesorios de <span class="accent">resistencia industrial</span> listos para el ritmo urbano.</p>
            </div>
            <div class="image-collage">
                <!-- Imagen de lona y taller (Enlaces Estables) -->
                <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=600&auto=format&fit=crop" alt="Texturas Abstractas Recicladas">
                <img src="https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?q=80&w=600&auto=format&fit=crop" alt="Manufactura Local Sostenible">
            </div>
        </div>
    </section>

    <!-- TIENDA / CATÁLOGO -->
    <section id="productos" class="section-padding" style="background-color: #0A0A0A;">
        <div class="container">
            <h2 class="section-title">Catálogo Oficial</h2>
            <div class="product-grid">

                <!-- Producto 1: Mochila Urbana -->
                <div class="product-card">
                    <div class="product-img-holder">
                        <span class="product-badge">Edición Limitada</span>
                        <img src="https://images.unsplash.com/photo-1553062407-98eeb64c6a62?q=80&w=600&auto=format&fit=crop" alt="Urban Backpack Reborn">
                    </div>
                    <div class="product-info">
                        <h3>Urban Backpack Reborn</h3>
                        <p class="product-desc">Compartimento acolchado para laptop de hasta 15", espaldar ergonómico y cuerpo completo de PVC publicitario recuperado. 100% a prueba de agua.</p>
                        <div class="product-footer">
                            <div class="product-price">S/ 179.00</div>
                            <button class="btn btn-sm" onclick="addToCart('Urban Backpack Reborn', 179)">Añadir</button>
                        </div>
                    </div>
                </div>

                <!-- Producto 2: Eco Tote -->
                <div class="product-card">
                    <div class="product-img-holder">
                        <img src="https://images.unsplash.com/photo-1544816155-12df9643f363?q=80&w=600&auto=format&fit=crop" alt="Eco Tote Urban">
                    </div>
                    <div class="product-info">
                        <h3>Eco Tote Bag</h3>
                        <p class="product-desc">El bolso urbano definitivo. Espacioso, con asas reforzadas para soportar el peso diario y texturas gráficas únicas recuperadas de paneles de la ciudad.</p>
                        <div class="product-footer">
                            <div class="product-price">S/ 89.00</div>
                            <button class="btn btn-sm" onclick="addToCart('Eco Tote Bag', 89)">Añadir</button>
                        </div>
                    </div>
                </div>

                <!-- Producto 3: Pouch Organizer -->
                <div class="product-card">
                    <div class="product-img-holder">
                        <img src="https://images.unsplash.com/photo-1622560480605-d83c853bc5c3?q=80&w=600&auto=format&fit=crop" alt="Pouch Utility Organizer">
                    </div>
                    <div class="product-info">
                        <h3>Pouch Utility Organizer</h3>
                        <p class="product-desc">Estuche compacto ideal para cables, llaves o cosméticos. Construido con mermas seleccionadas de lonas de PVC de alta flexibilidad.</p>
                        <div class="product-footer">
                            <div class="product-price">S/ 45.00</div>
                            <button class="btn btn-sm" onclick="addToCart('Pouch Utility Organizer', 45)">Añadir</button>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SIDEBAR DEL CARRITO INTERACTIVO -->
    <div id="sidebar-cart" class="cart-sidebar">
        <div class="cart-header">
            <h3>Tu Pedido</h3>
            <button class="close-cart" onclick="toggleCart()"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div id="cart-items" class="cart-items-container">
            <p style="color: var(--text-muted); text-align: center; margin-top: 2rem;">El carrito está vacío</p>
        </div>
        <div class="cart-footer-panel">
            <div class="total-row">
                <span>Total:</span>
                <span id="cart-total-price">S/ 0.00</span>
            </div>
            <button class="btn" style="width: 100%;" onclick="checkout()">Procesar Compra</button>
        </div>
    </div>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <a href="#inicio" class="footer-logo">ECO-<span>REBORN</span></a>
                <div class="footer-socials">
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-tiktok"></i></a>
                    <a href="#"><i class="fa-brands fa-facebook"></i></a>
                </div>
            </div>
            <div class="footer-copy">
                &copy; 2026 ECO-REBORN Perú - Manufactura Local y Sostenible. Lima, Perú.
            </div>
        </div>
    </footer>

    <!-- LÓGICA JAVASCRIPT DEL CARRITO -->
    <script>
        let cart = [];

        function toggleCart() {
            const sidebar = document.getElementById('sidebar-cart');
            sidebar.classList.toggle('open');
        }

        function addToCart(name, price) {
            cart.push({ name, price });
            updateCartUI();
            
            const sidebar = document.getElementById('sidebar-cart');
            if(!sidebar.classList.contains('open')) {
                sidebar.classList.add('open');
            }
        }

        function updateCartUI() {
            document.getElementById('cart-count').innerText = cart.length;
            const container = document.getElementById('cart-items');
            
            if (cart.length === 0) {
                container.innerHTML = `<p style="color: var(--text-muted); text-align: center; margin-top: 2rem;">El carrito está vacío</p>`;
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
                            <h4 style="color: white; font-size: 1.1rem;">${item.name}</h4>
                            <span style="color: var(--primary-color); font-weight: bold;">S/ ${item.price}.00</span>
                        </div>
                        <button onclick="removeItem(${index})" style="background:none; border:none; color: #ff5252; cursor:pointer;">
                            <i class="fa-solid fa-trash-can"></i>
                        </button>
                    </div>
                `;
            });

            document.getElementById('cart-total-price').innerText = `S/ ${total}.00`;
        }

        function removeItem(index) {
            cart.splice(index, 1);
            updateCartUI();
        }

        function checkout() {
            if(cart.length === 0) {
                alert("Tu carrito está vacío.");
                return;
            }
            alert("¡Pedido recibido con éxito! Redirigiendo a la pasarela de pago seguro.");
            cart = [];
            updateCartUI();
            toggleCart();
        }
    </script>
</body>
</html>
