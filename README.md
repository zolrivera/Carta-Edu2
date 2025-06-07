# Carta-Edu2
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Feliz Cumpleaños, Amor</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: radial-gradient(circle at top, #ffd1dc 0%, #ffb6c1 100%);
      font-family: 'Georgia', serif;
      overflow-x: hidden;
      height: 100vh;
    }

    .carta {
      max-width: 700px;
      margin: 80px auto;
      background: #fff;
      padding: 50px 40px;
      border-radius: 20px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
      text-align: center;
      animation: aparecer 2s ease forwards;
      opacity: 0;
      transform: scale(0.9);
      z-index: 10;
    }

    @keyframes aparecer {
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    h1 {
      font-size: 2.8em;
      color: #e91e63;
      margin-bottom: 15px;
    }

    p {
      font-size: 1.3em;
      color: #444;
      line-height: 1.6;
    }

    .firma {
      margin-top: 40px;
      font-style: italic;
      color: #d81b60;
    }

    .boton {
      margin-top: 30px;
      background-color: #e91e63;
      color: white;
      border: none;
      padding: 12px 24px;
      font-size: 1.1em;
      border-radius: 30px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .boton:hover {
      background-color: #c2185b;
    }

    .regalo {
      margin-top: 30px;
      display: none;
      animation: zoomIn 1s ease;
    }

    .regalo img {
      max-width: 90%;
      border-radius: 20px;
      margin: 10px auto;
      box-shadow: 0 10px 20px rgba(0,0,0,0.2);
    }

    @keyframes zoomIn {
      0% {
        transform: scale(0.2);
        opacity: 0;
      }
      100% {
        transform: scale(1);
        opacity: 1;
      }
    }

    .corazon, .petalo {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: flotar 10s infinite ease-in;
      z-index: 1;
    }

    .corazon::before,
    .corazon::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .corazon::before {
      top: -10px;
      left: 0;
    }

    .corazon::after {
      left: -10px;
      top: 0;
    }

    .petalo {
      background: pink;
      border-radius: 50%;
      transform: rotate(20deg);
      width: 14px;
      height: 18px;
    }

    @keyframes flotar {
      0% {
        bottom: -50px;
        opacity: 0;
        transform: translateX(0) rotate(45deg);
      }
      50% {
        opacity: 1;
        transform: translateX(30px) rotate(45deg);
      }
      100% {
        bottom: 100%;
        opacity: 0;
        transform: translateX(-30px) rotate(45deg);
      }
    }
  </style>
</head>
<body>
  <audio autoplay loop volume="0.2">
    <source src="musica.mp3" type="audio/mpeg">
    Tu navegador no soporta el audio HTML5.
  </audio>

  <script>
    for (let i = 0; i < 15; i++) {
      const heart = document.createElement('div');
      heart.classList.add('corazon');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (6 + Math.random() * 5) + 's';
      heart.style.opacity = Math.random();
      document.body.appendChild(heart);
    }

    for (let i = 0; i < 15; i++) {
      const petal = document.createElement('div');
      petal.classList.add('petalo');
      petal.style.left = Math.random() * 100 + 'vw';
      petal.style.animationDuration = (6 + Math.random() * 4) + 's';
      petal.style.opacity = Math.random();
      document.body.appendChild(petal);
    }
  </script>

  <div class="carta">
    <h1>¡Feliz Cumpleaños, Amor! 🎉❤️</h1>
    <p>
      Hoy es un día especial porque celebramos tu existencia. Gracias por hacer mi mundo más bonito. 💕
    </p>
    <p class="firma">
      Con amor,<br>Tu persona favorita 😘
    </p>

    <button class="boton" onclick="mostrarRegalo()">Ver tu regalo 🎁</button>

    <div class="regalo" id="regalo">
      <img src="IMG_20230628_211452.jpg" alt="Foto juntos">
      <img src="IMG_20230628_211402.jpg" alt="Foto del cumpleañero con la torta">
    </div>
  </div>

  <script>
    function mostrarRegalo() {
      document.getElementById("regalo").style.display = "block";
    }
  </script>
</body>
</html>
