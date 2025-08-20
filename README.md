<html>
<head>
  <meta charset="UTF-8">
  <title>Te Amo Val</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: black;
      overflow: hidden;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    h1 {
      font-size: 60px;
      color: red;
      text-shadow: 0 0 20px pink, 0 0 40px red;
      animation: glow 2s infinite alternate;
      z-index: 10;
      position: relative;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px pink, 0 0 20px red; }
      to   { text-shadow: 0 0 20px red, 0 0 40px pink; }
    }

    .heart {
      position: fixed;
      top: -10vh;
      color: red;
      font-size: 24px;
      animation: fall linear forwards;
      pointer-events: none;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>❤️ Te amo Val ❤️</h1>

  <!-- Música de YouTube oculta -->
  <iframe width="0" height="0" 
    src="https://www.youtube.com/embed/XpPRXTAUw_o?autoplay=1&loop=1&playlist=XpPRXTAUw_o"
    frameborder="0" allow="autoplay">
  </iframe>

  <script>
    // Crear corazones en cascada
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (3 + Math.random() * 4) + "s";
      document.body.appendChild(heart);
      setTimeout(() => { heart.remove(); }, 7000);
    }
    setInterval(createHeart, 300);
  </script>
</body>
</html>
