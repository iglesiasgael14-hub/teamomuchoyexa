<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Cartita para mi loba yexini 💖</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

  body {
    margin: 0;
    padding: 0;
    font-family: 'Montserrat', sans-serif;
    background: radial-gradient(circle at center, #ffe6f0 0%, #f9d5e5 100%);
    overflow-x: hidden;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
  }

  .container {
    background: rgba(255, 255, 255, 0.98);
    width: 95vw;
    max-width: 600px;
    border-radius: 20px;
    box-shadow: 0 8px 30px rgba(200, 100, 150, 0.3);
    padding: 2rem 2.5rem;
    text-align: center;
    position: relative;
    z-index: 10;
    box-sizing: border-box;
  }

  h1 {
    font-size: 2.4rem;
    color: #b2225e;
    margin-bottom: 1rem;
  }

  .message {
    font-size: 1.2rem;
    color: #4a4a4a;
    margin: 1rem 0;
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease, transform 0.6s ease;
    height: 0;
    overflow: hidden;
  }

  .message.visible {
    opacity: 1;
    transform: translateY(0);
    height: auto;
  }

  .big-heart {
    position: absolute;
    width: 50px;
    height: 45px;
    background: transparent;
    animation: floatSlow 10s linear infinite;
    opacity: 0.3;
  }

  .heart-pink {
    --heart-color: #e91e63cc;
  }
  .heart-red {
    --heart-color: #ff0046cc;
  }
  .heart-purple {
    --heart-color: #9600c8cc;
  }

  .big-heart::before,
  .big-heart::after {
    content: "";
    position: absolute;
    width: 50px;
    height: 45px;
    background: var(--heart-color);
    border-radius: 50% 50% 0 0;
    top: 0;
    left: 0;
    transform-origin: center bottom;
  }

  .big-heart::before {
    border-radius: 50% 50% 0 0;
    transform: rotate(-45deg);
    left: 0;
  }
  .big-heart::after {
    border-radius: 50% 50% 0 0;
    transform: rotate(45deg);
    left: 25px;
  }

  .big-heart {
    background: var(--heart-color);
    clip-path: polygon(
      50% 100%,
      0% 60%,
      0% 20%,
      25% 0%,
      50% 20%,
      75% 0%,
      100% 20%,
      100% 60%
    );
  }

  @keyframes floatSlow {
    0% {
      transform: translateY(100vh) rotate(0deg);
      opacity: 0;
    }
    50% {
      opacity: 0.5;
    }
    100% {
      transform: translateY(-20vh) rotate(0deg);
      opacity: 0;
    }
  }

  .emoji {
    position: absolute;
    font-size: 28px;
    animation: floatEmoji 8s ease-in-out infinite;
    user-select: none;
    opacity: 0.7;
  }

  @keyframes floatEmoji {
    0%, 100% {
      transform: translateY(0);
      opacity: 0.7;
    }
    50% {
      transform: translateY(-20px);
      opacity: 1;
    }
  }

  @media (max-width: 480px) {
    h1 {
      font-size: 2rem;
    }
    .message {
      font-size: 1rem;
      margin: 0.8rem 0;
    }
  }
</style>
</head>
<body>

<div class="container" role="main" aria-label="Carta interactiva para mi novia">
  <h1>Para mi loba, mi todo, mi yexini 💖</h1>
  
  <p id="msg1" class="message visible">Desde que te conocí, mi vida fue más feliz alv, teamo...</p>
  <p id="msg2" class="message">Eres la persona que ilumina mis días con tu sonrisa, 
  con tu humor, con todo lo que tú tienes, simplemente me haces sentir increíble, teamo.</p>
  <p id="msg3" class="message">Quiero construir mil recuerdos más a tu lado pq la neta sí teamo.</p>
  <p id="msg4" class="message">Gracias por ser tú, simplemente perfecta para mí, para mi vida. Gracias por llegar y quedarte, gracias por aguantarme. Te amo muchísimo.</p>
  <p id="msg5" class="message">Te amo más de lo que las palabras pueden expresar, así que 
  te hice una playlist en Spotify alv, recuérdame en pasártela. 
  ¿Ya te dije que te amo mucho no?</p>

  <!-- Mensaje final -->
  <p id="finalMsg" class="message">Te amo muchísimo mi yexini 💕🐺 gracias por ser mi todo, para siempre 🫶</p>
</div>

<!-- Corazones grandes -->
<div class="big-heart heart-pink" style="left: 10vw; animation-delay: 0s;"></div>
<div class="big-heart heart-red" style="left: 40vw; animation-delay: 3s;"></div>
<div class="big-heart heart-purple" style="left: 70vw; animation-delay: 6s;"></div>
<div class="big-heart heart-pink" style="left: 85vw; animation-delay: 8s;"></div>

<!-- Emojis -->
<div class="emoji" style="left: 15vw; top: 30vh; animation-delay: 1s;">🐺</div>
<div class="emoji" style="left: 60vw; top: 20vh; animation-delay: 3s;">🌸</div>
<div class="emoji" style="left: 75vw; top: 45vh; animation-delay: 5s;">🐺</div>
<div class="emoji" style="left: 35vw; top: 60vh; animation-delay: 2s;">🌸</div>
<div class="emoji" style="left: 20vw; top: 50vh; animation-delay: 4s;">✨</div>
<div class="emoji" style="left: 55vw; top: 65vh; animation-delay: 6s;">❤️</div>

<script>
  const messages = [
    document.getElementById('msg1'),
    document.getElementById('msg2'),
    document.getElementById('msg3'),
    document.getElementById('msg4'),
    document.getElementById('msg5'),
  ];

  const finalMessage = document.getElementById('finalMsg');
  let current = 0;

  const showNextMessage = () => {
    current++;
    if (current < messages.length) {
      messages[current].classList.add('visible');
    } else {
      clearInterval(timer);
      setTimeout(() => {
        finalMessage.classList.add('visible');
      }, 4000);
    }
  };

  const timer = setInterval(showNextMessage, 4000);
</script>

</body>
</html>

