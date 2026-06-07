<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ECO-REBORN | Moda Circular & Upcycled Perú</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;700&family=Urbanist:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>
        /* --- CONFIGURACIÓN ESTÉTICA PREMIUM (Modo Oscuro) --- */
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

        .logo span { color: var(--primary-color); }

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

        .nav-links a:hover { color: var(--white); }

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
        }

        /* --- HERO --- */
        .hero {
            background: linear-gradient(rgba(15,15,15,0.7), rgba(15,15,15,0.95)), 
                        url('https://images.unsplash.com/photo-1544816155-12df9643f363?q=80&w=1200&auto=format&fit=crop') no-repeat center center/cover;
            height: 75vh;
            display: flex;
            align-items: center;
        }

        .hero-content h1 {
            font-size: 4.5rem;
            line-height: 0.9;
            margin-bottom: 1.5rem;
            color: var(--white);
        }

        .hero-content p {
            font-size: 1.2rem;
            color: var(--text-muted);
            max-width: 600px;
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

        /* --- SECCIONES --- */
        .section-padding { padding: 5rem 0; }

        .section-title {
            font-size: 2.3rem;
            color: var(--white);
            margin-bottom: 3rem;
            border-left: 5px solid var(--primary-color);
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

        /* --- STATS --- */
        .stats-bg { background-color: #0A0A0A; border-top: 1px solid #111; border-bottom: 1px solid #111; }
        .stats-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem; text-align: center; }
        .stat-item .number { font-size: 4.5rem; font-weight: 700; color: var(--primary-color); font-family: 'Space Grotesk', sans-serif; }
        .stat-item p { color: var(--text-muted); font-size: 1rem; }

        /* --- PRODUCTOS --- */
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
        }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--primary-color);
            color: var(--white);
            padding: 4px 12px;
            font-size: 0.8rem;
            font-weight: 700;
            border-radius: 4px;
        }

        .product-info { padding: 2rem; display: flex; flex-direction: column; flex-grow: 1; }
        .product-info h3 { font-size: 1.4rem; color: var(--white); margin-bottom: 0.5rem; }
        .product-desc { color: var(--text-muted); font-size: 0.95rem; margin-bottom: 1.5rem; flex-grow: 1; }
        
        .product-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 1.5rem;
            border-top: 1px solid #222;
        }

        .product-price { font-family: 'Space Grotesk', sans-serif; font-size: 1.6rem; font-weight: 700; color: var(--white); }
        .btn-sm { padding: 0.6rem 1.2rem; font-size: 0.9rem; }

        /* --- CARRITO SIDEBAR --- */
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

        .cart-sidebar.open { right: 0; }
        .cart-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 2rem; border-bottom: 1px solid #222; padding-bottom: 1rem; }
        .close-cart { background: none; border: none; color: var(--text-muted); font-size: 1.5rem; cursor: pointer; }
        .cart-items-container { flex-grow: 1; overflow-y: auto; }
        
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            background: #111;
            padding: 10px;
            border-radius: 6px;
        }

        .cart-footer-panel { border-top: 1px solid #222; padding-top: 1.5rem; }
        .total-row { display: flex; justify-content: space-between; font-size: 1.3rem; font-family: 'Space Grotesk', sans-serif; margin-bottom: 1.5rem; }

        /* --- FOOTER --- */
        footer { background-color: #0A0A0A; border-top: 1px solid #222; padding: 4rem 0 2rem 0; }
        .footer-grid { display: flex; justify-content: space-between; align-items: center; margin-bottom: 3rem; }
        .footer-logo { font-size: 2rem; font-weight: 700; color: var(--white); text-decoration: none; }
        .footer-logo span { color: var(--primary-color); }
        .footer-socials a { color: var(--text-muted); font-size: 1.5rem; margin-left: 1.5rem; }
        .footer-copy { text-align: center; color: #555; font-size: 0.9rem; padding-top: 2rem; border-top: 1px solid #111; }

        @media (max-width: 768px) {
            .concept-grid { grid-template-columns: 1fr; gap: 2rem; }
            .stats-grid { grid-template-columns: 1fr; gap: 3rem; }
            .hero-content h1 { font-size: 3rem; }
            .cart-sidebar { width: 100%; right: -100%; }
            .footer-grid { flex-direction: column; gap: 2rem; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>

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

    <section id="inicio" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>ECO-REBORN</h1>
                <p>Moda Up-cycled con Impacto Circular. Transformamos residuos de lona publicitaria y PVC en el futuro del estilo urbano de Lima.</p>
                <a href="#productos" class="btn">Explorar Catálogo</a>
            </div>
        </div>
    </section>

    <section class="section-padding stats-bg">
        <div class="container stats-grid">
            <div class="stat-item">
                <div class="number">500</div>
                <p>Años tarda el PVC de un banner en degradarse.</p>
            </div>
            <div class="stat-item">
                <div class="number">100%</div>
                <p>Impermeable y de patrón único irrepetible.</p>
            </div>
            <div class="stat-item">
                <div class="number">0%</div>
                <p>Residuos plásticos añadidos. Economía circular.</p>
            </div>
        </div>
    </section>

    <section id="concepto" class="section-padding">
        <div class="container concept-grid">
            <div class="concept-text">
                <h2 class="section-title">Diseño con Conciencia</h2>
                <p>Cada año, toneladas de gigantografías publicitarias terminan en vertederos peruanos. Interceptamos este material antes de que sea basura.</p>
                <p>A través de un proceso artesanal de corte y confección local, las texturas dan vida a accesorios de <span class="accent">resistencia industrial</span>.</p>
            </div>
            <div class="image-collage">
                <img src="concepto1.png" alt="Eco Reborn Lona Verde">
                <img src="concepto2.png" alt="Detalle Mochila Upcycled">
            </div>
        </div>
    </section>

    <section id="productos" class="section-padding" style="background-color: #0A0A0A;">
        <div class="container">
            <h2 class="section-title">Catálogo Oficial</h2>
            <div class="product-grid">

                <div class="product-card">
                    <div class="product-img-holder">
                        <span class="product-badge">Edición Única</span>
                        <img src="mochila.png" alt="Urban Backpack Reborn">
                    </div>
                    <div class="product-info">
                        <h3>Urban Backpack Reborn</h3>
                        <p class="product-desc">Compartimento acolchado para laptop de hasta 15", cierres reforzados y cuerpo de PVC recuperado. Impermeable.</p>
                        <div class="product-footer">
                            <div class="product-price">S/ 179.00</div>
                            <button class="btn btn-sm" onclick="addToCart('Urban Backpack Reborn', 179)">Añadir</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-img-holder">
                        <img src="combo.png" alt="Eco Tote Bag mas Pouch">
                    </div>
                    <div class="product-info">
                        <h3>Eco Tote + Pouch Utility</h3>
                        <p class="product-desc">El juego urbano definitivo. Un amplio bolso de mano resistente al peso diario junto a su estuche organizador multiusos.</p>
                        <div class="product-footer">
                            <div class="product-price">S/ 119.00</div>
                            <button class="btn btn-sm" onclick="addToCart('Eco Tote + Pouch Utility', 119)">Añadir</button>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

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

    <footer>
        <div class="container">
            <div class="footer-grid">
                <a href="#inicio" class="footer-logo">ECO-<span>REBORN</span></a>
                <div class="footer-socials">
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-tiktok"></i></a>
                </div>
            </div>
            <div class="footer-copy">
                &copy; 2026 ECO-REBORN Perú - Manufactura Sostenible. Lima.
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
                        <button onclick="removeItem(${index})" style="background:none; border:none; color: #ff5252; cursor:pointer;"><i class="fa-solid fa-trash-can"></i></button>
                    </div>`;
            });
            document.getElementById('cart-total-price').innerText = `S/ ${total}.00`;
        }

        function removeItem(index) { cart.splice(index, 1); updateCartUI(); }
        function checkout() { alert("¡Pedido recibido! Conectando pasarela."); cart = []; updateCartUI(); toggleCart(); }
    </script>
</body>
</html>
