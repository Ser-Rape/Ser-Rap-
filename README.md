<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tienda de Productos</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            background-color: #D2B48C; /* Marrón claro */
            font-family: Arial, sans-serif;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            text-align: center;
            margin: 20px 0;
        }
        img.logo {
            max-width: 150px;
        }
        .product-images {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 20px 0;
        }
        .product-images img {
            width: 200px; /* Ajusta según sea necesario */
            cursor: pointer;
            transition: transform 0.2s;
        }
        .product-images img:hover {
            transform: scale(1.05);
        }
        .gallery {
            margin: 20px 0;
        }
        .gallery img {
            width: 100px; /* Ajusta según sea necesario */
            margin: 5px;
            cursor: pointer;
        }
        .accordion, .faq {
            margin: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .accordion-item {
            padding: 10px;
            border-bottom: 1px solid #ccc;
            cursor: pointer;
        }
        .faq-item {
            padding: 10px;
            border-bottom: 1px solid #ccc;
            cursor: pointer;
        }
        .hidden {
            display: none;
        }
        footer {
            text-align: center;
            margin: 20px 0;
        }
    </style>
</head>
<body>

<header>
    <img src="logo.png" alt="Logo" class="logo">
    <p>Descripción de la tienda de productos</p>
</header>

<section class="product-images">
    <div>
        <img src="rape.jpg" alt="Rapé" onclick="expandImage('rape.jpg')">
        <p>Precio: $XX.XX</p>
    </div>
    <div>
        <img src="kuripe.jpg" alt="Kuripé" onclick="expandImage('kuripe.jpg')">
        <p>Precio: $XX.XX</p>
    </div>
    <div>
        <img src="tepi.jpg" alt="Tepi" onclick="expandImage('tepi.jpg')">
        <p>Precio: $XX.XX</p>
    </div>
    <div>
        <img src="porta_rape.jpg" alt="Porta Rapé" onclick="expandImage('porta_rape.jpg')">
        <p>Precio: $XX.XX</p>
    </div>
</section>

<section class="gallery">
    <h2>Galerías</h2>
    <div>
        <h3>Variedades de Rapé</h3>
        <div class="gallery">
            <!-- Repite para cada imagen -->
            <img src="variedad_rape_1.jpg" alt="Variedad Rapé 1" onclick="expandImage('variedad_rape_1.jpg')">
            <!-- ... -->
        </div>
    </div>
    <div>
        <h3>Variedades de Kuripés</h3>
        <div class="gallery">
            <img src="variedad_kuripe_1.jpg" alt="Variedad Kuripé 1" onclick="expandImage('variedad_kuripe_1.jpg')">
            <!-- ... -->
        </div>
    </div>
    <div>
        <h3>Variedades de Tepís</h3>
        <div class="gallery">
            <img src="variedad_tepi_1.jpg" alt="Variedad Tepi 1" onclick="expandImage('variedad_tepi_1.jpg')">
            <!-- ... -->
        </div>
    </div>
    <div>
        <h3>Variedades de Porta Rapé</h3>
        <div class="gallery">
            <img src="variedad_porta_rape_1.jpg" alt="Variedad Porta Rapé 1" onclick="expandImage('variedad_porta_rape_1.jpg')">
            <!-- ... -->
        </div>
    </div>
</section>

<section class="accordion">
    <h2>Variedades de Rapé</h2>
    <div class="accordion-item" onclick="toggleAccordion(this)">
        <h3>Variedad 1</h3>
        <div class="hidden">Descripción de la variedad 1</div>
    </div>
    <!-- Repite para cada variedad -->
</section>

<section class="faq">
    <h2>Preguntas Frecuentes</h2>
    <div class="faq-item" onclick="toggleFAQ(this)">
        <h3>¿Cuál es la función del rapé?</h3>
        <div class="hidden">Respuesta sobre la función del rapé.</div>
    </div>
    <!-- Repite para cada pregunta -->
</section>

<footer>
    <a href="https://wa.me/numero_de_telefono"><img src="whatsapp.png" alt="WhatsApp"></a>
    <a href="https://instagram.com/tu_instagram"><img src="instagram.png" alt="Instagram"></a>
</footer>

<script>
    function expandImage(src) {
        const img = document.createElement('img');
        img.src = src;
        img.style.width = '80%';
        img.style.maxHeight = '80%';
        img.style.position = 'fixed';
        img.style.top = '50%';
        img.style.left = '50%';
        img.style.transform = 'translate(-50%, -50%)';
        img.style.zIndex = '1000';
        img.onclick = () => document.body.removeChild(img);
        document.body.appendChild(img);
    }

    function toggleAccordion(element) {
        const content = element.querySelector('.hidden');
        content.classList.toggle('hidden');
    }

    function toggleFAQ(element) {
        const content = element.querySelector('.hidden');
        content.classList.toggle('hidden');
    }
</script>

</body>
</html>
