<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para Ti ❤️</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        background: linear-gradient(135deg, #1e1e2f, #2b1055);
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Courier New', monospace;
        color: white;
        overflow: hidden;
        text-align: center;
    }

    .container {
        max-width: 600px;
    }

    h1 {
        font-size: 2.5rem;
        margin-bottom: 20px;
    }

    #mensaje {
        font-size: 1.3rem;
        min-height: 100px;
    }

    button {
        margin-top: 30px;
        padding: 12px 25px;
        border: none;
        border-radius: 30px;
        background-color: #ff4da6;
        color: white;
        font-size: 1rem;
        cursor: pointer;
        transition: 0.3s;
    }

    button:hover {
        background-color: #ff1a8c;
        transform: scale(1.1);
    }

    .corazon {
        position: absolute;
        color: #ff4da6;
        font-size: 20px;
        animation: flotar 5s linear infinite;
    }

    @keyframes flotar {
        0% { transform: translateY(100vh); opacity: 0; }
        50% { opacity: 1; }
        100% { transform: translateY(-10vh); opacity: 0; }
    }
</style>
</head>
<body>

<div class="container">
    <h1>Para la mujer más increíble 💖</h1>
    <div id="mensaje"></div>
    <button onclick="sorpresa()">Haz clic aquí ✨</button>
</div>

<script>
const texto = "No es aniversario. No es una fecha especial.\n" +
              "Pero pensé en ti.\n" +
              "Y eso ya lo hace especial.\n\n" +
              "Gracias por existir.\n" +
              "Gracias por ser tú.\n" +
              "Te elegiría una y mil veces más ❤️";

let i = 0;
function escribir() {
    if (i < texto.length) {
        document.getElementById("mensaje").innerHTML += texto.charAt(i);
        i++;
        setTimeout(escribir, 40);
    }
}
escribir();

function sorpresa() {
    alert("Plot twist: Me sigues gustando más cada día 💘");
    for (let j = 0; j < 30; j++) {
        let corazon = document.createElement("div");
        corazon.classList.add("corazon");
        corazon.innerHTML = "❤️";
        corazon.style.left = Math.random() * 100 + "vw";
        corazon.style.animationDuration = (Math.random() * 3 + 2) + "s";
        document.body.appendChild(corazon);
    }
}
</script>

</body>
</html>
