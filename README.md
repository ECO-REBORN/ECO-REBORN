<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ECO-REBORN | Mochilas de PVC Reciclado</title>
    <style>
        /* --- ESTILOS GENERALES --- */
        :root {
            --primary-color: #2e7d32;
            --primary-light: #a5d6a7;
            --dark-color: #212121;
            --light-bg: #f5f5f5;
            --white: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light-bg);
            color: var(--dark-color);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* --- HEADER Y NAVEGACIÓN --- */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary-color);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .logo span {
            color: var(--dark-color);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* --- HERO SECTION --- */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&q=80&w=1200') no-repeat center center/cover;
            height: 70vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: var(--white);
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: var(--white);
            padding: 0.8rem 2rem;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #1b5e20;
        }

        /* --- CONCEPTO / INFO --- */
        .concept {
            padding: 5rem 0;
            text-align: center;
            background-color: var(--white);
        }

        .concept h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
        }

        .concept p {
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.1rem;
            color: #555;
        }

        /* --- PRODUCTOS --- */
        .products {
            padding: 5rem 0;
        }

        .products h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--dark-color);
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background-color: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
            display: flex;
            flex-direction: column;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-img {
            width: 100%;
            height: 300px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #666;
            /* Simulación de imágenes con colores placeholder */
            background: linear-gradient(45deg, var(--primary-light), #b0bec5);
        }

        .product-info {
            padding: 1.5rem;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .product-title {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }

        .product-desc {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 1rem;
            flex-grow: 1;
        }

        .product-price {
            font-size: 1.6rem;
            font-weight: bold;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--dark-color);
            color: var(--white);
            text-align: center;
            padding: 2rem 0;
            margin-top: 5rem;
        }

        footer p {
            font-size: 0.9rem;
            opacity: 0.8;
        }
    </style>
</head>
<body>

    <!-- NAVEGACIÓN -->
    <header>
        <div class="container navbar">
            <div class="logo">ECO-<span>REBORN</span></div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#concepto">Concepto</a></li>
                <li><a href="#productos">Mochilas</a></li>
            </ul>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="inicio" class="hero">
        <div class="container hero-content">
            <h1>Segunda Vida al PVC</h1>
            <p>Descubre nuestra colección de mochilas ultrarresistentes, impermeables y hechas 100% con banners y lonas de PVC recicladas en Perú.</p>
            <a href="#productos" class="btn">Ver Catálogo</a>
        </div>
    </section>

    <!-- CONCEPTO -->
    <section id="concepto" class="concept">
        <div class="container">
            <h2>El Concepto ECO-REBORN</h2>
            <p>
                Cada año, toneladas de lonas publicitarias de PVC terminan en los vertederos tardando cientos de años en degradarse. En <strong>ECO-REBORN</strong> transformamos estos materiales de alta resistencia en mochilas de diseño único y urbano. Al ser material reciclado, cada mochila tiene un patrón de diseño irrepetible, es completamente impermeable y está lista para resistir el ritmo de la ciudad.
            </p>
        </div>
    </section>

    <!-- PRODUCTOS -->
    <section id="productos" class="products">
        <div class="container">
            <h2>Nuestras Mochilas</h2>
            <div class="product-grid">
                
                <!-- Producto 1 -->
                <div class="product-card">
                    <div class="product-img" style="background: linear-gradient(135deg, #2e7d32, #1b5e20);">
                        URBAN PACK PVC
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Mochila Urban Pack</h3>
                        <p class="product-desc">Perfecta para el día a día en la universidad o el trabajo. Compartimento para laptop de hasta 15" y 100% a prueba de lluvia limeña.</p>
                        <div class="product-price">S/ 149.00</div>
                        <button class="btn" onclick="agregarCarrito('Urban Pack')">Comprar</button>
                    </div>
                </div>

                <!-- Producto 2 -->
                <div class="product-card">
                    <div class="product-img" style="background: linear-gradient(135deg, #0277bd, #001f3f);">
                        ROLLTOP ADVENTURE
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Rolltop Adventure</h3>
                        <p class="product-desc">Diseño expandible ideal para ciclistas y viajeros. Cierre hermético superior y espalda acolchada con material respirable.</p>
                        <div class="product-price">S/ 189.00</div>
                        <button class="btn" onclick="agregarCarrito('Rolltop Adventure')">Comprar</button>
                    </div>
                </div>

                <!-- Producto 3 -->
                <div class="product-card">
                    <div class="product-img" style="background: linear-gradient(135deg, #f57c00, #e65100);">
                        MINI ECO SLING
                    </div>
                    <div class="product-info">
                        <h3 class="product-title">Mini Eco Sling</h3>
                        <p class="product-desc">Mochila cruzada ligera para llevar lo esencial (celular, llaves, billetera). Estilo urbano, cómodo y sumamente resistente.</p>
                        <div class="product-price">S/ 89.00</div>
                        <button class="btn" onclick="agregarCarrito('Mini Eco Sling')">Comprar</button>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <p>&copy; 2026 ECO-REBORN Perú - Moda Sostenible y Consciente. Todos los derechos reservados.</p>
        </div>
    </footer>

    <!-- LÓGICA JAVASCRIPT -->
    <script>
        function agregarCarrito(nombreProducto) {
            alert(`¡Genial! Has añadido la mochila "${nombreProducto}" a tu carrito de compras.`);
        }
    </script>
</body>
</html>
