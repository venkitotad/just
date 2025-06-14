<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday Chilli !</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #ff6ec4;
      --secondary: #7873f5;
      --accent: #fdd835;
    }

    body {
      margin: 0;
      font-family: 'Dancing Script', cursive;
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      overflow: hidden;
      color: white;
    }

    h1 {
      font-size: 4rem;
      color: var(--accent);
      text-shadow:
        0 0 10px var(--accent),
        0 0 20px var(--accent),
        0 0 30px var(--accent),
        0 0 40px var(--primary);
      animation: float 3s ease-in-out infinite, glow 1.s ease-in-out infinite;
      margin: 2rem;
      text-align: center;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }

    @keyframes glow {
      0%, 100% {
        text-shadow:
          0 0 10px var(--accent),
          0 0 20px var(--accent),
          0 0 30px var(--accent),
          0 0 40px var(--primary);
      }
      50% {
        text-shadow:
          0 0 5px var(--accent),
          0 0 10px var(--accent),
          0 0 15px var(--accent),
          0 0 20px var(--primary);
      }
    }

    .btn {
      background: linear-gradient(135deg, #ff6b6b, #ff1493);
      color: white;
      padding: 0.8rem 1.5rem;
      font-size: 1.2rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
      transition: transform 0.3s ease;
      animation: pulse 2s infinite;
      margin-top: 1rem;
    }

    .btn:hover {
      transform: scale(1.1);
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }

    #cake {
      font-size: 6rem;
      cursor: pointer;
      animation: float 4s ease-in-out infinite;
    }

    @keyframes sparkleFade {
      0% { opacity: 1; transform: scale(1); }
      100% { opacity: 0; transform: scale(2); }
    }

    @keyframes floatHeart {
      0% { transform: translateY(0); }
      50% { transform: translateY(-50px); }
      100% { transform: translateY(0); }
    }
  </style>
</head>
<body>

  <h1>🎉 Happy Birthday Sarah 🎂</h1>
  <div id="cake"></div>
  <button class="btn" onclick="createHearts()">Click for a Surprise</button>

  <audio id="birthdayAudio" autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <script>
    function createHearts() {
      for (let i = 0; i < 20; i++) {
        const heart = document.createElement('div');
        heart.textContent = '💖';
        heart.style.position = 'fixed';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.top = Math.random() * 100 + 'vh';
        heart.style.fontSize = Math.random() * 24 + 16 + 'px';
        heart.style.opacity = 0.8;
        heart.style.animation = floatHeart ${2 + Math.random() * 4}s ease-in-out infinite;
        heart.style.zIndex = 999;
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 10000);
      }
    }

    function sparkleEffect() {
      for (let i = 0; i < 15; i++) {
        const sparkle = document.createElement('div');
        sparkle.textContent = '✨';
        sparkle.style.position = 'fixed';
        sparkle.style.left = (window.innerWidth / 2) + (Math.random() * 100 - 50) + 'px';
        sparkle.style.top = (window.innerHeight / 2) + (Math.random() * 100 - 50) + 'px';
        sparkle.style.opacity = 0.8;
        sparkle.style.fontSize = '20px';
        sparkle.style.animation = 'sparkleFade 1s ease-out';
        sparkle.style.zIndex = 1000;
        document.body.appendChild(sparkle);
        setTimeout(() => sparkle.remove(), 1000);
      }
    }

    document.getElementById('cake').addEventListener('click', sparkleEffect);
  </script>

</body>
</html>
 
 
