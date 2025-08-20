<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Te amo Val ❤️</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #000;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
    }
    h1 {
      position: relative;
      z-index: 2;
      font-size: 4rem;
      color: #fff;
      text-shadow: 0 0 15px red, 0 0 30px crimson;
      animation: heartbeat 1.5s infinite;
      text-align: center;
    }
    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
    .heart {
      position: absolute;
      top: -10%;
      font-size: 2rem;
      color: red;
      animation: fall linear forwards;
      opacity: 0.8;
    }
    @keyframes fall {
      to {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>❤️ Te amo Val ❤️</h1>

  <iframe width="320" height="180"
    src="https://www.youtube.com/embed/XpPRXTAUw_o?autoplay=1&loop=1&playlist=XpPRXTAUw_o"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
    style="border-radius:12px; display:block; margin:20px auto;">
  </iframe>

  <script>
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.textContent = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (Math.random() * 20 + 20) + "px";
      heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
      document.body.appendChild(heart);
      setTimeout(() => heart
