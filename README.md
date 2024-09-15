<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Un Rincón Romántico</title>
    <!-- Bootstrap CSS -->
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
    <style>
        /* Estilo general */
        body {
            font-family: 'Arial', sans-serif;
            color: #333;
            overflow-x: hidden;
            background-color: #f8f9fa; /* Color de fondo claro y suave */
        }

        /* Navegación personalizada */
        .navbar-custom {
            background-color: #e83e8c; /* Color rosa suave */
            border-bottom: 3px solid #ff6f61; /* Rosa más intenso */
        }

        .navbar-custom .navbar-brand {
            color: #fff;
            font-size: 1.5em;
            font-weight: bold;
            animation: slideIn 2s ease-in-out;
        }

        .navbar-custom .nav-link {
            color: #fff;
            font-size: 1.2em;
            padding: 10px 15px;
            transition: background-color 0.3s, color 0.3s;
            animation: fadeIn 3s ease-in-out;
        }

        .navbar-custom .nav-link:hover {
            background-color: #ff6f61;
            color: #fff;
            border-radius: 5px;
        }

        /* Encabezado con animación de corazones */
        .header {
            text-align: center;
            padding: 80px 20px;
            background-color: #e83e8c; /* Rosa suave */
            border-bottom: 5px solid #ff6f61; /* Rosa más intenso */
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            margin: 20px auto;
            max-width: 800px;
        }

        .header h1 {
            font-size: 3.5em;
            color: #fff;
            margin: 0;
            animation: fadeIn 2s ease-in-out, glow 1.5s infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 0 0 10px #ff6f61, 0 0 20px #ff6f61, 0 0 30px #ff6f61, 0 0 40px #ff6f61, 0 0 50px #ff6f61, 0 0 60px #ff6f61, 0 0 70px #ff6f61;
            }
            to {
                text-shadow: 0 0 15px #ff4b6c, 0 0 30px #ff4b6c, 0 0 45px #ff4b6c, 0 0 60px #ff4b6c, 0 0 75px #ff4b6c, 0 0 90px #ff4b6c, 0 0 105px #ff4b6c;
            }
        }

        /* Sección de introducción */
        .introduction {
            padding: 60px 20px;
            text-align: center;
            background-color: rgba(255, 255, 255, 0.95); /* Blanco con opacidad */
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            margin: 20px auto;
            max-width: 800px;
            position: relative;
            animation: slideUp 2s ease-in-out;
        }

        .introduction p {
            font-size: 1.4em;
            color: #333; /* Texto en gris oscuro */
            margin-bottom: 20px;
            animation: fadeIn 3s ease-in-out;
        }

        .main-image {
            text-align: center;
            margin-bottom: 20px;
            position: relative;
        }

        .main-image img {
            width: 100%; /* Ajuste completo del ancho */
            height: auto;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
            animation: move 10s ease-in-out infinite, scaleUp 5s ease-in-out infinite;
        }

        @keyframes move {
            0% { transform: translateY(-5px); }
            50% { transform: translateY(10px); }
            100% { transform: translateY(-5px); }
        }

        @keyframes scaleUp {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        /* Botón de ver galería */
        .btn-gallery {
            background-color: #ff6f61; /* Rosa intenso */
            color: #fff;
            font-size: 1.2em;
            padding: 15px 30px;
            border: none;
            border-radius: 10px;
            transition: background-color 0.3s, transform 0.3s;
            text-decoration: none;
            display: inline-block;
            margin-top: 20px;
            text-align: center;
            animation: bounce 1s ease-in-out;
        }

        .btn-gallery:hover {
            background-color: #ff4b6c; /* Rosa más intenso */
            transform: scale(1.1);
        }

        @keyframes bounce {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        /* Corazones animados con imagen */
        .heart {
            position: absolute;
            width: 50px;
            height: 50px;
            background-image: url('https://static.vecteezy.com/system/resources/previews/001/187/492/original/heart-png.png');
            background-size: cover;
            opacity: 0.9;
            z-index: 1;
        }

        .heart:nth-child(1) {
            top: -10%;
            left: 5%;
            animation: float 2s linear infinite;
        }

        .heart:nth-child(2) {
            top: -20%;
            left: 25%;
            animation: float 2.5s linear infinite;
        }

        .heart:nth-child(3) {
            top: -15%;
            left: 45%;
            animation: float 3s linear infinite;
        }

        .heart:nth-child(4) {
            top: -5%;
            left: 65%;
            animation: float 3.5s linear infinite;
        }

        .heart:nth-child(5) {
            top: -10%;
            left: 85%;
            animation: float 4s linear infinite;
        }

        @keyframes float {
            0% { transform: translateY(-20px); }
            50% { transform: translateY(40px); }
            100% { transform: translateY(-20px); }
        }

        /* Animaciones de letras */
        @keyframes slideIn {
            from {
                transform: translateX(-100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes slideUp {
            from {
                transform: translateY(50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        /* Contenedor fijo para el audio */
        #audio-container {
            position: fixed;
            bottom: 0;
            width: 100%;
            text-align: center;
            z-index: 9999;
        }

        /* Estilos responsivos */
        @media (max-width: 768px) {
            .navbar-custom .navbar-brand {
                font-size: 1.2em;
            }

            .navbar-custom .nav-link {
                font-size: 1em;
            }

            .header h1 {
                font-size: 2.5em;
            }

            .introduction p {
                font-size: 1.2em;
            }

            .btn-gallery {
                font-size: 1em;
                padding: 10px 20px;
            }
        }

        @media (max-width: 576px) {
            .navbar-custom .navbar-brand {
                font-size: 1em;
            }

            .navbar-custom .nav-link {
                font-size: 0.9em;
            }

            .header h1 {
                font-size: 2em;
            }

            .introduction p {
                font-size: 1em;
            }

            .btn-gallery {
                font-size: 0.9em;
                padding: 8px 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Navegación -->
    <nav class="navbar navbar-expand-lg navbar-custom">
        <a class="navbar-brand" href="index.html">Inicio</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item">
                    <a class="nav-link" href="gallery.html">Galería</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="phrases.html">Frases Románticas</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="contact.html">Contacto</a>
                </li>
            </ul>
        </div>
    </nav>

    <!-- Imagen de fondo y contenedor principal -->
    <div class="background">
        <!-- Encabezado con una animación de corazones -->
        <header class="header">
            <div class="heart"></div>
            <div class="heart"></div>
            <div class="heart"></div>
            <div class="heart"></div>
            <div class="heart"></div>
            <h1>Descubre Nuestro Espacio Especial</h1>
        </header>

        <!-- Sección de introducción -->
        <section class="introduction">
            <p>Este es un espacio especial dedicado a ti, lleno de recuerdos, amor y momentos que siempre quiero atesorar.</p>
            <div class="main-image">
                <img src="https://www.imagenesvarias.com/wp-content/uploads/2017/12/Fondos-de-pantalla-de-Parejas-Enamoradas-23.jpg" alt="Imagen Romántica Principal">
            </div>
            <a class="btn-gallery" href="gallery.html">Ver Galería</a>
        </section>
    </div>

    <!-- Contenedor para el audio -->
    <div id="audio-container">
        <iframe src="audio.html" style="border:none; width:100%; height:100px;" scrolling="no"></iframe>
    </div>

    <!-- Bootstrap JS and dependencies -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.2/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
    
    <!-- JavaScript para controlar el audio -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            var audio = document.getElementById('background-audio');
            var isPlaying = localStorage.getItem('isPlaying') === 'true';
    
            if (isPlaying) {
                audio.play();
            } else {
                audio.pause();
            }
    
            audio.addEventListener('play', function() {
                localStorage.setItem('isPlaying', 'true');
            });
    
            audio.addEventListener('pause', function() {
                localStorage.setItem('isPlaying', 'false');
            });
    
            // Reiniciar el audio cuando se acabe
            audio.addEventListener('ended', function() {
                this.currentTime = 0; // Reiniciar el audio
                this.play(); // Reproducir el audio nuevamente
            });
        });
    </script>
    
</body>
</html>
