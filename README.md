<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Caro &#x2764;</title>
    <link rel="icon" href="https://static.vecteezy.com/system/resources/previews/011/026/769/non_2x/watercolor-balloon-heart-happy-valentine-s-day-clipart-free-png.png">
    <style>
        body {
            --tw-bg-opacity: 1;
            background-color: rgb(190 24 93 / var(--tw-bg-opacity));
            font-family: Arial, sans-serif;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            text-align: center;
        }
        h1 {
            color: #6B7280;
            font-size: 2rem;
        }
        .heart-img {
            width: 150px;
            transition: transform 0.5s ease-in-out;
        }
        .message {
            font-size: 1.2rem;
            color: #F59E0B;
            margin-bottom: 20px;
        }
        button {
            background-color: #F59E0B;
            color: white;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-right: 10px;
        }
        button:hover {
            background-color: #FBBF24;
        }
        .animate-heart {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¿Quieres ser mi San Valentín?</h1>
        <img src="https://i.pinimg.com/originals/f6/a5/f7/f6a5f7ddff1f05cbcc560256b9f98c2e.gif" alt="Heart" class="heart-img">
        <p class="message">¡Vamos, respóndeme!</p>
        <button id="siBtn">Sí</button>
        <button id="noBtn">No</button>
    </div>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            var messages = [
                "¿Segurisima?",
                "¿Estás completamente segura?",
                "¿No te arrepentirás?",
                "¿Pero si estás segura?",
                "No hay vuelta atrás",
                "No hay devoluciones",
                "No hay reembolsos",
                "No hay garantías",
                "No hay cambios",
                "No hay nada",
                "No hay",
                "Que no hay"
            ];
            var messageIndex = 0;

            document.getElementById("siBtn").addEventListener("click", function() {
                document.querySelector(".message").innerText = "¡Gracias por aceptar, te quiero mucho! ❤️";
                document.querySelector(".heart-img").classList.add("animate-heart");
                document.querySelector(".heart-img").src = "https://i.pinimg.com/originals/e4/9d/7b/e49d7b7e965f09e31b498314b02e3662.gif";
                setTimeout(function() {
                    document.querySelector(".heart-img").classList.remove("animate-heart");
                }, 500);
                messageIndex = 0; // Reiniciar el contador al principio del array
            });

            document.getElementById("noBtn").addEventListener("click", function() {
                document.querySelector(".message").innerText = messages[messageIndex];
                document.querySelector(".heart-img").classList.add("animate-heart");
                document.querySelector(".heart-img").src = "https://media.tenor.com/ivKWdfdbV3EAAAAi/goma-goma-cat.gif";
                setTimeout(function() {
                    document.querySelector(".heart-img").classList.remove("animate-heart");
                }, 500);
                messageIndex = (messageIndex + 1) % messages.length;
            });
        });
    </script>
</body>
</html>
