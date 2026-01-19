<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Te Amo ❤️</title>

<style>
body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ffb6c1, #ff69b4);
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    font-family: Arial, sans-serif;
}

.teamo {
    font-size: clamp(60px, 15vw, 120px);
    font-weight: bold;
    color: white;
    text-shadow:
        0 0 20px #ff004f,
        0 0 40px #ff004f,
        0 0 60px #ff004f;
    animation: pulse 3s infinite;
    z-index: 2;
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

.rosa {
    position: absolute;
    font-size: 36px;
    animation: fall linear infinite;
    pointer-events: none;
}

@keyframes fall {
    0% {
        transform: translateY(110vh) rotate(0deg);
        opacity: 0;
    }
    10% { opacity: 1; }
    100% {
        transform: translateY(-120vh) rotate(360deg);
        opacity: 0;
    }
}
</style>
</head>

<body>

<div class="teamo">TE AMO ❤️</div>

<script>
setInterval(() => {
    const rosa = document.createElement("div");
    rosa.className = "rosa";
    rosa.textContent = "🌹";
    rosa.style.left = Math.random() * 100 + "vw";
    rosa.style.animationDuration = (4 + Math.random() * 5) + "s";
    document.body.appendChild(rosa);

    setTimeout(() => rosa.remove(), 9000);
}, 350);
</script>

</body>
</html>
