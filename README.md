<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EcoMochilas - Estilo Sostenible</title>
    <style>
        /* --- ESTILOS GENERALES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            color: #333;
            background-color: #f9f9f6;
            line-height: 1.6;
        }

        header {
            background-color: #2e4a3f; /* Verde ecológico oscuro */
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        header h1 {
            font-size: 1.5rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-weight: 600;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #a3c9a8; /* Verde claro al pasar el mouse */
        }

        /* --- HERO SECTION --- */
        .hero {
            background: linear-gradient(rgba(46, 74, 63, 0.7), rgba(46, 74, 63, 0.7)), url('https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
            height: 60vh;
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 10px;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 20px;
            max-width: 600px;
        }

        .btn-main {
            background-color: #84a98c;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 25px;
            transition: background 0.3s;
        }

        .btn-main:hover {
            background-color: #52796f;
        }

        /* --- SECCIONES CONTENEDORAS --- */
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        h3 {
            text-align: center;
            font-size: 2rem;
            color: #2e4a3f;
            margin-bottom: 30px;
        }

        /* --- PRODUCTOS --- */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-img {
            width: 100%;
            height: 250px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #666;
            font-weight: bold;
            /* Simulación de imágenes reales con Unsplash */
            background-size: cover;
            background-position: center;
        }

        .product-info {
            padding: 20px;
            text-align: center;
        }

        .product-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #2e4a3f;
        }

        .product-desc {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 15px;
        }

        .product-price {
            font-size: 1.3rem;
            font-weight: bold;
            color: #354f52;
            margin-bottom: 15px;
        }

        .btn-buy {
            display: block;
            background-color: #2e4a3f;
            color: white;
            padding: 10px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
        }

        .btn-buy:hover {
            background-color: #84a98c;
        }

        /* --- SOBRE NOSOTROS --- */
        .about-section {
            background-color: #ecefe6;
            padding: 60px 20px;
            text-align: center;
            border-radius: 10px;
            margin-top: 50px;
        }

        .about-section p {
            max-width: 800px;
            margin: 0 auto 20px auto;
            font-size: 1.1rem;
        }

        /* --- CONTACTO --- */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #2e4a3f;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .btn-submit {
            background-color: #2e4a3f;
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 1rem;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            font-weight: bold;
            transition: background 0.3s;
        }

        .btn-submit:hover {
            background-color: #52796f;
        }

        /* --- FOOTER --- */
        footer {
            background-color: #2e4a3f;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 60px;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <!-- Encabezado / Navegación -->
    <header>
        <h1>🌱 EcoMochilas</h1>
        <nav>
            <a href="#productos">Productos</a>
            <a href="#nosotros">Nosotros</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>

    <!-- Sección Principal (Hero) -->
    <section class="hero">
        <h2>Lleva el futuro en tu espalda</h2>
        <p>Mochilas premium hechas al 100% con botellas plásticas recuperadas del océano y textiles reciclados.</p>
        <a href="#productos" class="btn-main">Ver Colección</a>
    </section>

    <!-- Sección de Productos -->
    <section id="productos" class="container">
        <h3>Nuestros Modelos Sostenibles</h3>
        <div class="products-grid">
            
            <!-- Producto 1 -->
            <div class="product-card">
                <div class="product-img" style="background-image: url('https://images.unsplash.com/photo-1553062407-98eeb64c6a62?auto=format&fit=crop&w=400&q=80');"></div>
                <div class="product-info">
                    <div class="product-title">Mochila Eco-Urbana</div>
                    <div class="product-desc">Perfecta para el día a día o la universidad. Hecha con 25 botellas PET recicladas. Impermeable y con compartimento para laptop.</div>
                    <div class="product-price">$45.00</div>
                    <a href="#" class="btn-buy" onclick="alert('¡Gracias por tu interés! Aquí conectarías tu pasarela de pago (como PayPal, Stripe o WhatsApp).')">Comprar Ahora</a>
                </div>
            </div>

            <!-- Producto 2 -->
            <div class="product-card">
                <div class="product-img" style="background-image: url('https://images.unsplash.com/photo-1622560480605-d83c853bc5c3?auto=format&fit=crop&w=400&q=80');"></div>
                <div class="product-info">
                    <div class="product-title">Aventurera Pro (Cáñamo y PET)</div>
                    <div class="product-desc">Diseñada para trekkings y viajes largos. Costuras reforzadas, ergonómica y con materiales 100% biodegradables y reciclados.</div>
                    <div class="product-price">$65.00</div>
                    <a href="#" class="btn-buy" onclick="alert('¡Gracias por tu interés!')">Comprar Ahora</a>
                </div>
            </div>

            <!-- Producto 3 -->
            <div class="product-card">
                <div class="product-img" style="background-image: url('https://images.unsplash.com/photo-1581605405669-fcdf81165afa?auto=format&fit=crop&w=400&q=80');"></div>
                <div class="product-info">
                    <div class="product-title">Maletín Ejecutivo Verde</div>
                    <div class="product-desc">Estilo elegante y profesional sin remordimientos ambientales. Tela hecha de descarte textil de algodón orgánico.</div>
                    <div class="product-price">$55.00</div>
                    <a href="#" class="btn-buy" onclick="alert('¡Gracias por tu interés!')">Comprar Ahora</a>
                </div>
            </div>

        </div>
    </section>

    <!-- Sección Sobre Nosotros -->
    <section id="nosotros" class="container">
        <div class="about-section">
            <h3>Nuestra Misión Verde</h3>
            <p>No somos solo una marca de mochilas; somos un movimiento para limpiar nuestro planeta. Cada año, millones de toneladas de plástico terminan en nuestros océanos. Nosotros las recolectamos, las procesamos y las transformamos en un accesorio duradero, útil y con un diseño increíble.</p>
            <p><strong>Por cada mochila que compras, retiras 1 kg de basura del mar.</strong></p>
        </div>
    </section>

    <!-- Sección de Contacto -->
    <section id="contacto" class="container">
        <h3>¿Tienes dudas o quieres compras al por mayor?</h3>
        <div class="contact-form">
            <form action="#" method="POST" onsubmit="event.preventDefault(); alert('¡Mensaje enviado! Te contactaremos pronto.');">
                <div class="form-group">
                    <label for="name">Nombre:</label>
                    <input type="text" id="name" required placeholder="Tu nombre">
                </div>
                <div class="form-group">
                    <label for="email">Correo Electrónico:</label>
                    <input type="email" id="email" required placeholder="tu@correo.com">
                </div>
                <div class="form-group">
                    <label for="message">Mensaje:</label>
                    <textarea id="message" rows="4" required placeholder="¿En qué podemos ayudarte?"></textarea>
                </div>
                <button type="submit" class="btn-submit">Enviar Mensaje</button>
            </form>
        </div>
    </section>

    <!-- Pie de página -->
    <footer>
        <p>&copy; 2026 EcoMochilas S.A. Todos los derechos reservados. Diseñado con ❤️ para el planeta.</p>
    </footer>

</body>
</html>
