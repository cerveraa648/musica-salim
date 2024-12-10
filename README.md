<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Aceites para Autos</title>
    <style>
        /* General Styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #171616;
            overflow-x: hidden;
        }
        h1, h2, h3 {
            color: #ffffff;
            text-align: center;
        }
        a {
            text-decoration: none;
            color: inherit;
        }

        /* Header Styles */
        header {
            background: #2c3e50;
            color: white;
            padding: 10px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        nav {
            display: flex;
            justify-content: space-around;
            align-items: center;
        }
        nav a {
            color: white;
            padding: 15px;
            font-size: 18px;
            transition: 0.3s;
        }
        nav a:hover {
            background-color: #34495e;
            border-radius: 5px;
        }

        /* Main Section */
        .hero {
            background-image: url('https://www.xtrafondos.com/wallpapers/resized/jeep-wrangler-rubicon-2021-8816.jpg?s=large');
            background-size: cover;
            background-position: center;
            height: 400px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.7);
        }
        .hero h1 {
            font-size: 3rem;
        }

        /* Product Grid */
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            padding: 40px;
            transition: all 0.3s ease;
        }
        .product-card {
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            text-align: center;
            cursor: pointer;
            transition: transform 0.3s ease;
        }
        .product-card:hover {
            transform: scale(1.05);
        }
        .product-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            transition: opacity 0.5s ease-in-out;
        }
        .product-info {
            padding: 20px;
        }
        .product-name {
            font-size: 1.2rem;
            color: #2c3e50;
            margin-bottom: 10px;
        }
        .product-price {
            font-size: 1.4rem;
            color: #e74c3c;
        }

        /* Footer */
        footer {
            background-color: #2c3e50;
            color: white;
            padding: 20px;
            text-align: center;
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            width: 60%;
            text-align: center;
            animation: fadeInUp 0.6s ease-out;
        }
        .modal img {
            width: 100%;
            height: auto;
            margin-bottom: 20px;
        }
        .close-btn {
            background-color: #e74c3c;
            color: white;
            padding: 10px 15px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .close-btn:hover {
            background-color: #c0392b;
        }

        /* Animations */
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }

        @keyframes fadeInUp {
            0% { opacity: 0; transform: translateY(50px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        /* Mobile Styles */
        @media screen and (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            nav {
                flex-direction: column;
            }
        }

        /* Audio and Video Container */
        .audio-container, .video-container {
            background-color: #2c3e50;
            padding: 20px;
            text-align: center;
        }
        audio {
            width: 100%;
            max-width: 600px;
            margin: 20px auto;
            border-radius: 5px;
        }
        iframe {
            width: 100%;
            max-width: 800px;
            height: 450px;
            margin: 20px auto;
            border-radius: 5px;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <nav>
            <a href="#">Inicio</a>
            <a href="#productos">Productos</a>
            <a href="#contacto">Contacto</a>
            <a href="#comprar" class="fade-in">Comprar Ahora</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Aceites para tu Automóvil</h1>
    </section>

    <!-- Product Section -->
    <section id="productos" class="products fade-in">
        <h2>Productos Destacados</h2>
        <div class="product-card" onclick="openModal('aceite1')">
            <img src="https://prod-resize.tiendainglesa.com.uy/images/small/P386775-1.jpg?20220824200055,Aceite-Sintetico-CASTROL-Edge-946-ml-en-Tienda-Inglesa" alt="Aceite 1" class="product-image">
            <div class="product-info">
                <h3 class="product-name">Aceite Sintético Premium</h3>
                <p class="product-price">$29.99</p>
            </div>
        </div>
        <div class="product-card" onclick="openModal('aceite2')">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQL23DZvLi8Z-qYYveSzg_W2U9vFMoLQJjvvQ&s" alt="Aceite 2" class="product-image">
            <div class="product-info">
                <h3 class="product-name">Aceite 5W-30</h3>
                <p class="product-price">$19.99</p>
            </div>
        </div>
        <div class="product-card" onclick="openModal('aceite3')">
            <img src="https://prod-resize.tiendainglesa.com.uy/images/small/P550256-1.jpg?20230621150124,Lubricante-AMALIE-10W-40-Envase-1-L-en-Tienda-Inglesa" alt="Aceite 3" class="product-image">
            <div class="product-info">
                <h3 class="product-name">Aceite 10W-40</h3>
                <p class="product-price">$24.99</p>
            </div>
        </div>
    </section>

    <!-- Modal -->
    <div id="modal" class="modal">
        <div class="modal-content">
            <h2 id="modal-title"></h2>
            <img id="modal-image" src="" alt="">
            <p id="modal-description"></p>
            <button class="close-btn" onclick="closeModal()">Cerrar</button>
        </div>
    </div>

    <!-- Footer -->
    <footer id="contacto">
        <p>&copy; Contamos con los mejores aceites para carros</p>
        <p><a href="mailto:salimjesus@gmail.com">Contáctanos</a></p>
    </footer>

    <!-- Reproductor de música visible -->
    <div class="audio-container">
        <audio controls autoplay loop>
            <source src="https://www.dropbox.com/scl/fi/xk3eo45rmnxgtorfgtseu/Six-Days-Lyrics-Tokyo-Drift-it-s-only-monday.mp3?raw=1" type="audio/mpeg">
            Tu navegador no soporta la etiqueta de audio.
        </audio>
    </div>

    <!-- Reproductor de video de YouTube -->
    <div class="video-container">
        <iframe src="https://www.youtube.com/embed/40KfV-ANuD8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>

    <script>
        // JavaScript para animaciones
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.fade-in');
            sections.forEach(section => {
                const sectionTop = section.getBoundingClientRect().top;
                if (sectionTop < window.innerHeight - 50) {
                    section.classList.add('fade-in');
                }
            });
        });

        // Función para abrir el modal con la información del aceite
        function openModal(aceite) {
            let title, image, description;

            // Dependiendo del aceite seleccionado, cambia los datos
            if (aceite === 'aceite1') {
                title = 'Aceite Sintético Premium';
                image = 'https://www.carcare.org/wp-content/uploads/2020/12/full-synthetic-oil.jpg';
                description = 'Aceite sintético de alta calidad para motores de última generación.';
            } else if (aceite === 'aceite2') {
                title = 'Aceite 5W-30';
                image = 'https://www.autoexpert.com.au/wp-content/uploads/2021/08/synthetic-oil-2.jpg';
                description = 'Ideal para vehículos de uso frecuente en todo tipo de condiciones climáticas.';
            } else if (aceite === 'aceite3') {
                title = 'Aceite 10W-40';
                image = 'https://www.holtsauto.com/wp-content/uploads/2020/06/motor-oil-synthetic-blend-2.jpg';
                description = 'Aceite multiusos para motores de alto rendimiento.';
            }

            // Establecer los valores en el modal
            document.getElementById('modal-title').textContent = title;
            document.getElementById('modal-image').src = image;
            document.getElementById('modal-description').textContent = description;

            // Mostrar el modal
            document.getElementById('modal').style.display = 'flex';
        }

        // Función para cerrar el modal
        function closeModal() {
            document.getElementById('modal').style.display = 'none';
        }
    </script>

</body>
</html>
