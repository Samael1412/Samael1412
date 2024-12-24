<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¡Feliz Navidad!</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(to bottom, #1e3c72, #2a5298); /* Fondo azul navideño */
            color: #fff;
            text-align: center;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        /* Efecto de nieve */
        .snow {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .snowflake {
            position: absolute;
            top: -10px;
            color: #fff;
            font-size: 1em;
            animation: snow 10s linear infinite;
        }

        @keyframes snow {
            0% {
                transform: translateY(0);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh);
                opacity: 0.2;
            }
        }

        .snowflake:nth-child(odd) {
            animation-duration: 8s;
        }

        h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 4em;
            margin: 0;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
        }

        p {
            font-size: 1.2em;
            margin: 10px 20px;
        }

        .button {
            background: #ff6b6b;
            color: #fff;
            font-size: 1.2em;
            padding: 15px 30px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
            transition: transform 0.3s, background 0.3s;
        }

        .button:hover {
            background: #ff4444;
            transform: scale(1.1);
        }

        .button:active {
            transform: scale(0.9);
        }
    </style>
</head>
<body>
    <div class="snow">
        <div class="snowflake">❄</div>
        <div class="snowflake">❅</div>
        <div class="snowflake">❆</div>
        <div class="snowflake">❄</div>
        <div class="snowflake">❅</div>
        <div class="snowflake">❆</div>
    </div>

    <h1>¡Feliz Navidad!</h1>
    <p>Que esta Navidad esté llena de paz, amor y felicidad para ti y tus seres queridos.</p>
    <button class="button" onclick="alert('¡Que tengas unas fiestas increíbles! 🎄✨')">Haz clic aquí</button>

    <script>
        // Generar copos de nieve dinámicos
        const snowContainer = document.querySelector('.snow');

        for (let i = 0; i < 50; i++) {
            const snowflake = document.createElement('div');
            snowflake.classList.add('snowflake');
            snowflake.style.left = Math.random() * 100 + 'vw';
            snowflake.style.animationDelay = Math.random() * 5 + 's';
            snowflake.style.fontSize = Math.random() * 1.5 + 0.5 + 'em';
            snowflake.textContent = ['❄', '❅', '❆'][Math.floor(Math.random() * 3)];
            snowContainer.appendChild(snowflake);
        }
    </script>
</body>
</html>
