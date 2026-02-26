<!DOCTYPE html>
<html>
<head>
    <title>Un mensaje para ti 💖</title>
    <meta charset="UTF-8">
    <style>
        body {
            margin: 0;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff8fb1, #c084fc);
            font-family: Arial, sans-serif;
            text-align: center;
            color: white;
        }

        .contenedor {
            background: rgba(255, 255, 255, 0.15);
            padding: 50px;
            border-radius: 30px;
            backdrop-filter: blur(15px);
            z-index: 10;
            max-width: 500px;
        }

        h1 {
            font-size: 42px;
            margin-bottom: 10px;
        }

        .nombre {
            opacity: 0;
            animation: aparecer 3s forwards;
            font-weight: bold;
            font-size: 24px;
            margin-top: 10px;
        }

        @keyframes aparecer {
            to { opacity: 1; }
        }

        .firma {
            margin-top: 25px;
            font-size: 14px;
            opacity: 0.7;
        }

        .corazon {
            position: absolute;
            top: -10px;
            font-size: 20px;
            animation: caer 6s linear infinite;
        }

        @keyframes caer {
            to { transform: translateY(110vh); }
        }

        button {
            margin-top: 20px;
            padding: 12px 25px;
            border: none;
            border-radius: 20px;
            background-color: white;
            color: #c084fc;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            background-color: #ffe4f0;
        }
    </style>
</head>
<body>

    <div class="contenedor">
        <h1>TE AMO ❤️</h1>
        <p>Estoy muy enamorada de ti</p>
        <p class="nombre">María Vittoria Torres García</p>
        <button onclick="mensaje()">Haz clic si también me amas 💕</button>
        <div class="firma">Hecho con amor por Anghy 🫀</div>
    </div>

    <script>
        function mensaje() {
            alert("Siempre voy a elegirte 💖");
        }

        function crearCorazon() {
            const corazon = document.createElement("div");
            corazon.classList.add("corazon");
            corazon.innerHTML = "💖";
            corazon.style.left = Math.random() * 100 + "vw";
            corazon.style.animationDuration = (Math.random() * 3 + 3) + "s";
            document.body.appendChild(corazon);

            setTimeout(() => {
                corazon.remove();
            }, 6000);
        }

        setInterval(crearCorazon, 300);
    </script>

</body>
</html>
