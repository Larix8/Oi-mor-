<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedido Especial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffe6e6;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            position: relative;
        }

        h1 {
            font-size: 3em;
            color: #d63384;
        }

        .bear-img {
            width: 200px;
            height: auto;
        }

        .buttons {
            position: relative;
            margin-top: 20px;
        }

        button {
            font-size: 1.5em;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }

        .yes {
            background-color: #28a745;
            color: white;
        }

        .yes:hover {
            background-color: #218838;
        }

        .no {
            background-color: #dc3545;
            color: white;
            position: absolute;
        }
    </style>
</head>
<body>
    <h1>Trepa comigo? 💖</h1>
    <div class="buttons">
        <button class="yes" onclick="sayYes()">Sim</button>
        <button class="no" id="noButton">Não</button>
    </div>

    <script>
        function sayYes() {
            alert("Sabia que você ia dizer sim! 😏🔥");
        }

        function moveNo() {
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 100);
            document.getElementById("noButton").style.left = `${x}px`;
            document.getElementById("noButton").style.top = `${y}px`;
        }

        // No PC, o botão "Não" foge ao passar o mouse
        document.getElementById("noButton").addEventListener("mouseover", moveNo);

        // No celular, o botão "Não" foge ao tocar na tela
        document.getElementById("noButton").addEventListener("touchstart", moveNo);
    </script>
</body>
</html>
