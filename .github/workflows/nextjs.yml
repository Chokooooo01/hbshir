<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Feliz Cumpleaños Shirley</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;500;700&display=swap');

    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to top right, #ffe0f0, #fff0e6);
      font-family: 'Poppins', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
      text-align: center;
    }

    h1 {
      font-family: 'Pacifico', cursive;
      font-size: 3rem;
      color: #e91e63;
      margin-bottom: 0.5rem;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.1);
    }

    p {
      font-size: 1.5rem;
      color: #333;
      margin: 0.5rem 0;
      font-weight: 500;
    }

    button {
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      font-weight: 500;
      border: none;
      border-radius: 1.5rem;
      background-color: #e91e63;
      color: white;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #d81b60;
    }

    .balloon {
      position: absolute;
      bottom: -150px;
      width: 50px;
      height: 70px;
      background-color: #ff4081;
      border-radius: 50% 50% 50% 50%;
      animation: floatUp 10s linear infinite;
      opacity: 0.85;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 0.7rem;
      font-weight: bold;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
      pointer-events: none;
    }

    .balloon::after {
      content: "";
      position: absolute;
      bottom: -20px;
      left: 50%;
      width: 2px;
      height: 20px;
      background: #888;
      transform: translateX(-50%);
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) translateX(0);
        opacity: 1;
      }
      100% {
        transform: translateY(-110vh) translateX(-20px);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>Feliz Cumpleaños Shirley</h1>
  <p>Que tus metas despeguen hoy, pero primero unas cheee</p>
  <p>sms reset causitaaaaa</p>

  <!-- Botón para controlar la música -->
  <button id="btn-music">🔊 Pausar música</button>

  <audio id="bg-music" autoplay loop style="display: none">
    <source src="https://cdn.pixabay.com/audio/2023/06/07/audio_bf1e80828d.mp3" type="audio/mpeg" />
    Tu navegador no soporta audio HTML5.
  </audio>

  <script>
    const audio = document.getElementById('bg-music');
    const btn = document.getElementById('btn-music');

    // Iniciar reproducción en móviles tras interacción
    document.addEventListener('click', () => {
      if (audio.paused) audio.play().catch(() => {});
    }, { once: true });

    // Control de botón: pausa y reanuda la música
    btn.addEventListener('click', () => {
      if (audio.paused) {
        audio.play();
        btn.textContent = '🔊 Pausar música';
      } else {
        audio.pause();
        btn.textContent = '▶️ Reproducir música';
      }
    });

    // Generar globos aleatorios
    function createBalloon() {
      const balloon = document.createElement('div');
      balloon.classList.add('balloon');
      balloon.style.left = Math.random() * 100 + 'vw';
      balloon.style.backgroundColor = getRandomColor();
      balloon.style.animationDuration = (5 + Math.random() * 5) + 's';
      balloon.innerText = 'reset';
      document.body.appendChild(balloon);

      setTimeout(() => {
        balloon.remove();
      }, 10000);
    }

    function getRandomColor() {
      const colors = ['#ff4081', '#e91e63', '#7c4dff', '#40c4ff', '#69f0ae', '#ffab40'];
      return colors[Math.floor(Math.random() * colors.length)];
    }

    setInterval(createBalloon, 500);
  </script>
</body>
</html>
