<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>I'm Sorry Yashu 💔</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
      color: white;
      height: 100vh;
      overflow: hidden;
      text-align: center;
      position: relative;
    }

    .stars {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('https://raw.githubusercontent.com/VincentGarreau/particles.js/master/demo/media/star.png') repeat;
      animation: moveStars 200s linear infinite;
      z-index: -1;
    }

    @keyframes moveStars {
      from { background-position: 0 0; }
      to { background-position: -10000px 5000px; }
    }

    h1 {
      font-size: 3em;
      color: #ff7eb3;
      margin-top: 10vh;
      letter-spacing: 2px;
    }

    .typewriter {
      font-size: 1.2em;
      width: 80%;
      max-width: 600px;
      margin: 2em auto;
      border-right: 3px solid #ff4b2b;
      white-space: nowrap;
      overflow: hidden;
      animation: typing 4s steps(40) 1s forwards, blink 0.75s step-end infinite;
    }

    @keyframes typing {
      from { width: 0; }
      to { width: 100%; }
    }

    @keyframes blink {
      50% { border-color: transparent; }
    }

    button {
      padding: 15px 30px;
      font-size: 1.2em;
      background-color: #ff4b2b;
      border: none;
      color: white;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: #ff416c;
      transform: scale(1.1);
    }

    .heart {
      position: absolute;
      width: 30px;
      height: 30px;
      background-color: pink;
      transform: rotate(45deg);
      animation: floatHeart 10s infinite;
      opacity: 0.8;
    }

    .heart::before, .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: pink;
      border-radius: 50%;
    }

    .heart::before { top: -10px; left: 0; }
    .heart::after { left: -10px; top: 0; }

    @keyframes floatHeart {
      0% { transform: translateY(100vh) rotate(45deg); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-10vh) rotate(45deg); opacity: 0; }
    }
  </style>
</head>
<body>

  <div class="stars"></div>

  <h1>I'm Sorry Yashu 💔</h1>
  <p class="typewriter">
    Hi Yashu I am Truly sorry for how i acted can u pls forgive me i truly love you bohot bohot zyaada i know ive made a lot of mistakes and i promise u ill do better
  <button onclick="alert('Yay! You forgave me 😭💘')">Forgive me, Yashu?</button>

  <script>
    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = 5 + Math.random() * 5 + "s";
      document.body.appendChild(heart);
      setTimeout(() => { heart.remove(); }, 10000);
    }
    setInterval(createHeart, 300);
  </script>

</body>
</html>
