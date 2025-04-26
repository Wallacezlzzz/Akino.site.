<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Eu Te Amo</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      background: radial-gradient(#000, #111);
      overflow: hidden;
      height: 100vh;
      font-family: 'Arial', sans-serif;
      position: relative;
    }

    .heart {
      position: absolute;
      color: red;
      animation: float 6s ease-in-out infinite;
      opacity: 0.7;
    }

    .text {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-family: 'Great Vibes', cursive;
      font-size: 60px;
      background: linear-gradient(45deg, #ff4d4d, #ff99cc);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 0 15px rgba(255, 0, 100, 0.6);
      animation: fadeInOut 4s ease-in-out infinite;
    }

    @keyframes float {
      0% {
        transform: translateY(0) scale(1);
        opacity: 0.8;
      }
      50% {
        transform: translateY(-80px) scale(1.2);
        opacity: 0.3;
      }
      100% {
        transform: translateY(0) scale(1);
        opacity: 0.8;
      }
    }

    @keyframes fadeInOut {
      0%, 100% { opacity: 0; }
      50% { opacity: 1; }
    }
  </style>
</head>
<body>

  <div class="text">Eu te amo</div>

  <script>
    const colors = ['#ff4d4d', '#ff6666', '#ff1a1a', '#ff9999'];
    for (let i = 0; i < 30; i++) {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.innerText = '❤️';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.top = Math.random() * 100 + 'vh';
      heart.style.fontSize = (Math.random() * 20 + 20) + 'px';
      heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
      heart.style.color = colors[Math.floor(Math.random() * colors.length)];
      document.body.appendChild(heart);
    }
  </script>
</body>
</html>
