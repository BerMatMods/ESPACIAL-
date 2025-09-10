
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Feliz Día de las Flores Amarillas 💛</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;600;700&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">

  <style>
    /* Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: end;
      min-height: 100vh;
      overflow: hidden;
      background-color: #121212;
      font-family: 'Poppins', sans-serif;
      cursor: pointer;
      position: relative;
      transition: background-color 0.6s ease;
      color: #fff;
    }

    /* Evitar selección */
    body, .menu-toggle, .menu, .love-letter, .explosion-item, .rain-word, .credits {
      -webkit-user-select: none;
      -moz-user-select: none;
      -ms-user-select: none;
      user-select: none;
    }

    /* === Título (arriba) === */
    .title-container {
      position: absolute;
      top: 30px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 1100;
    }

    .title-box {
      background: rgba(0, 0, 0, 0.8);
      color: #FFD700;
      padding: 12px 30px;
      border-radius: 25px;
      border: 2px solid #FFD700;
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.4);
      text-align: center;
      font-family: 'Dancing Script', cursive;
      font-size: 2em;
      font-weight: 700;
      text-shadow: 0 0 10px rgba(255, 215, 0, 0.6);
      transition: all 0.3s ease;
    }

    /* === Carta (más abajo) === */
    .love-letter {
      position: absolute;
      top: 180px;
      left: 50%;
      transform: translateX(-50%);
      width: 85%;
      max-width: 600px;
      background: rgba(0, 0, 0, 0.9);
      color: #fff;
      padding: 30px;
      border-radius: 20px;
      border: 2px solid #FFD700;
      box-shadow: 0 0 40px rgba(255, 215, 0, 0.5);
      text-align: center;
      z-index: 1000;
      font-family: 'Poppins', sans-serif;
      font-size: 1.1em;
      line-height: 1.9;
      backdrop-filter: blur(8px);
      overflow: hidden;
      transition: all 0.3s ease;
    }

    .typing {
      border-right: 2px solid #FFD700;
      animation: blink-caret 0.6s step-end infinite;
      color: #fff;
      font-weight: 600;
      line-height: 2;
    }

    @keyframes blink-caret {
      from, to { border-color: transparent; }
      50% { border-color: #FFD700; }
    }

    /* === Menú de Tres Rayas === */
    .menu-toggle {
      position: absolute;
      top: 20px;
      left: 20px;
      width: 50px;
      height: 50px;
      background: linear-gradient(145deg, #b84900, #faa200);
      border: 2px solid #FFD700;
      border-radius: 50%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      z-index: 2000;
      transition: all 0.3s ease;
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.4);
    }

    .menu-toggle span {
      width: 26px;
      height: 3px;
      background: #fff;
      margin: 3px 0;
      border-radius: 2px;
      transition: 0.3s;
    }

    .menu-toggle:hover {
      transform: scale(1.1);
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.6);
    }

    /* Menú Desplegable */
    .menu {
      position: absolute;
      top: 80px;
      left: 20px;
      width: 300px;
      background: rgba(20, 20, 20, 0.98);
      backdrop-filter: blur(10px);
      border: 2px solid #FFD700;
      border-radius: 16px;
      padding: 25px;
      box-shadow: 0 0 30px rgba(255, 215, 0, 0.3);
      color: #fff;
      z-index: 2000;
      display: none;
      font-size: 1em;
      line-height: 1.7;
      transition: all 0.3s ease;
    }

    .menu.active {
      display: block;
    }

    .menu h3 {
      color: #FFD700;
      margin-bottom: 10px;
      font-size: 1.3em;
      font-weight: 700;
    }

    .menu p {
      color: #ccc;
      margin-bottom: 15px;
      font-size: 0.95em;
    }

    .menu-btn {
      display: block;
      width: 100%;
      background: #444;
      color: white;
      padding: 10px 15px;
      margin: 8px 0;
      border: none;
      border-radius: 8px;
      text-align: left;
      cursor: pointer;
      font-size: 0.95em;
      transition: background 0.3s;
    }

    .menu-btn:hover {
      background: #555;
    }

    .menu-btn.lang {
      background: #007BFF;
    }

    .menu-btn.theme {
      background: #b84900;
    }

    .menu-btn.info {
      background: #6c757d;
    }

    .whatsapp-btn {
      display: inline-block;
      background: #25D366;
      color: white;
      padding: 12px 20px;
      border-radius: 10px;
      text-decoration: none;
      font-weight: bold;
      font-size: 1em;
      margin-top: 15px;
      transition: all 0.3s;
      box-shadow: 0 0 10px rgba(37, 211, 102, 0.4);
    }

    /* === Sunflower (100% original) === */
    .sun-flower {
      position: absolute;
      top: 0;
      left: 80%;
      transform: translateY(-100%) rotate(1deg);
      z-index: 1;
    }
    .sun-flower__wrapper {
      position: absolute;
      animation: moving 10s infinite;
    }
    .sun-flower__circle {
      width: 10vmin;
      height: 10vmin;
      border-radius: 50%;
      position: relative;
    }
    .sun-flower__circle > div {
      position: absolute;
      left: 50%;
      top: 50%;
      width: 6vmin;
      height: 6vmin;
      border-radius: 50%;
      transform: translate(-50%, -50%);
      background-color: #b84900;
    }
    .sun-flower__circle > div::after {
      content: "";
      position: absolute;
      z-index: 100;
      left: 50%;
      top: 50%;
      width: 8vmin;
      height: 8vmin;
      border-radius: 50%;
      transform: translate(-110%, 5%);
      border: 0.2vmin solid #faa200;
      background-image: repeating-linear-gradient(45deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(112.5deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(22.5deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(67.5deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(45deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(157.5deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(112.5deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(90deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(90deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(135deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(67.5deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(135deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        repeating-linear-gradient(90deg, rgba(0, 0, 0, 0.03) 0px, rgba(0, 0, 0, 0.03) 1px, transparent 1px, transparent 12px), 
                        linear-gradient(90deg, #b84900, #b84900);
    }
    .sun-flower__circle--small {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 10vmin;
      height: 10vmin;
      border-radius: 100% 2% 100% 2%;
      background-color: #ffc628;
      transform-origin: left bottom;
    }
    .sun-flower__circle--small:nth-child(1) { transform: translate(-50%, -50%) rotate(40deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(2) { transform: translate(-50%, -50%) rotate(80deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(3) { transform: translate(-50%, -50%) rotate(120deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(4) { transform: translate(-50%, -50%) rotate(160deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(5) { transform: translate(-50%, -50%) rotate(200deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(6) { transform: translate(-50%, -50%) rotate(240deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(7) { transform: translate(-50%, -50%) rotate(280deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(8) { transform: translate(-50%, -50%) rotate(320deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(9) { transform: translate(-50%, -50%) rotate(360deg); z-index: 2; }
    .sun-flower__circle--small:nth-child(10) { transform: translate(-50%, -50%) rotate(400deg); z-index: 2; }
    .sun-flower__circle--top {
      transform-origin: left bottom;
      transform: translate(-50%, -50%) rotate(20deg) !important;
    }
    .sun-flower__circle--top > * {
      background-image: linear-gradient(to left bottom, #fbd603 40%, #ff7d04);
    }
    .sun-flower__line .line {
      width: 12vmin;
      height: 36vmin;
      border-radius: 100% 0 0 0;
      border-left: 1.2vmin solid #bec827;
      border-top: 1vmin solid #bec827;
      -webkit-mask-image: linear-gradient(to top, transparent, #bec827 5%);
    }
    .sun-flower__leaf {
      position: absolute;
      left: 25%;
      top: 25%;
      width: 15vmin;
      height: 12vmin;
      border-radius: 90% 0% 100% 20%;
      background-image: linear-gradient(to right bottom, #a7ad27 50%, #bec827 50%);
      transform-origin: left;
      transform: perspective(100px) rotateX(40deg) scale(0.7);
    }
    .sun-flower__leaf:nth-child(odd) {
      left: 10%;
      transform: perspective(100px) rotateY(180deg) rotateX(30deg) rotate(-10deg) scale(0.6);
    }
    .sun-flower__leaf::after {
      content: "";
      position: absolute;
      width: 4vmin;
      height: 6vmin;
      border-radius: 100% 0 0 0;
      border-left: 1vmin solid #bec827;
      border-top: 1vmin solid #bec827;
      bottom: 0;
      left: 0;
      transform: translate(-57%, 72%);
      z-index: -1;
    }
    .sun-flower__leaf--1 { top: 35%; }
    .sun-flower__leaf--2::after { transform: translate(-84%, 72%); }
    .sun-flower__leaf--3 {
      left: 20%;
      top: 55%;
      transform: perspective(100px) rotateX(40deg) scale(0.5);
    }
    .sun-flower__leaf--3::after { transform: translate(-64%, 72%); }
    .sun-flower__leaf--4 {
      left: 5% !important;
      top: 50%;
      transform: perspective(100px) rotateY(180deg) rotateX(30deg) rotate(-10deg) scale(0.45) !important;
    }

    @keyframes moving {
      0%, 100% { transform: rotate(-6deg); }
      50% { transform: rotate(-10deg); }
    }

    /* === Lluvia de palabras === */
    .rain-word {
      position: absolute;
      top: -40px;
      padding: 8px 14px;
      border: 2px solid #FFD700;
      border-radius: 25px;
      font-family: 'Poppins', sans-serif;
      font-weight: 600;
      font-size: 1.3em;
      white-space: nowrap;
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.4);
      z-index: 2;
      opacity: 0.95;
      animation: fall linear infinite;
    }

    /* Colores según modo */
    body .rain-word {
      background: rgba(20, 20, 20, 0.9);
      color: #FFD700;
    }

    body.light-mode .rain-word {
      background: #000;
      color: #fff;
      border-color: #000;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
    }

    @keyframes fall {
      0% {
        transform: translateY(-50px);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      100% {
        transform: translateY(105vh);
        opacity: 0;
      }
    }

    /* === Explosión === */
    .explosion-item {
      position: absolute;
      font-size: 1.8em;
      pointer-events: none;
      z-index: 2000;
      animation: explode 1.8s ease-out forwards;
      filter: drop-shadow(0 0 5px gold);
    }

    @keyframes explode {
      0% {
        transform: translate(0, 0) scale(0);
        opacity: 1;
      }
      100% {
        transform: translate(var(--dx), var(--dy)) scale(1.8);
        opacity: 0;
      }
    }

    /* === Créditos === */
    .credits-container {
      position: absolute;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 1000;
    }

    .credits {
      display: inline-block;
      background: linear-gradient(45deg, #b84900, #faa200);
      color: white;
      padding: 8px 16px;
      border-radius: 20px;
      font-family: 'Poppins', sans-serif;
      font-size: 1.4vmin;
      font-weight: 700;
      text-shadow: 0 0 8px rgba(255, 215, 0, 0.8);
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.4);
      border: 1px solid #FFD700;
    }

    /* === Modo Claro === */
    body.light-mode {
      background-color: #fff9e6;
      color: #333;
    }

    body.light-mode .title-box,
    body.light-mode .love-letter,
    body.light-mode .menu {
      background: rgba(255, 255, 255, 0.95);
      color: #333;
      border-color: #FFD700;
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.3);
    }

    body.light-mode .title-box,
    body.light-mode .love-letter h2,
    body.light-mode .menu h3 {
      color: #FFD700;
    }

    body.light-mode .typing {
      color: #333;
      border-right-color: #b84900;
    }
  </style>
</head>
<body id="body">

  <!-- Título -->
  <div class="title-container">
    <div class="title-box" id="titleText">🌻 Feliz Día de las Flores Amarillas 💛</div>
  </div>

  <!-- Carta -->
  <div class="love-letter">
    <p id="typed-text" class="typing"></p>
  </div>

  <!-- Menú de Tres Rayas -->
  <div class="menu-toggle" id="menuToggle">
    <span></span>
    <span></span>
    <span></span>
  </div>

  <div class="menu" id="menu">
    <h3>⚙️ Menú</h3>
    <button class="menu-btn theme" id="themeToggle">🌙 Activar Modo Claro</button>
    <button class="menu-btn lang" id="langToggle">🌐 Cambiar a Inglés</button>
    <div class="menu-btn info">ℹ️ Información del Proyecto</div>
    <p>Diseñado por <strong>BerMatMods</strong>.<br>Perfecto para regalar o sorprender.</p>
    <a href="https://wa.me/51930569195" target="_blank" class="whatsapp-btn">💬 Personalizar por WhatsApp</a>
  </div>

  <!-- Sunflower (original) -->
  <div class="sun-flower__wrapper">
    <div class="sun-flower">
      <div class="sun-flower__circle">
        <div class="sun-flower__circle--bottom">
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
        </div>
        <div class="sun-flower__circle--top">
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
          <div class="sun-flower__circle--small"></div>
        </div>
      </div>
    </div>
    <div class="sun-flower__line">
      <div class="line"></div>
      <div class="sun-flower__leaf sun-flower__leaf--1"></div>
      <div class="sun-flower__leaf sun-flower__leaf--2"></div>
      <div class="sun-flower__leaf sun-flower__leaf--3"></div>
      <div class="sun-flower__leaf sun-flower__leaf--4"></div>
    </div>
  </div>

  <!-- Créditos -->
  <div class="credits-container">
    <div class="credits">By AnthZz Berrocal BerMatMods</div>
  </div>

  <!-- Música -->
  <audio id="bgMusic" loop>
    <source src="https://cdn.pixabay.com/audio/2022/04/26/audio_8f9c9c3eb5.mp3" type="audio/mpeg">
  </audio>

  <!-- Scripts -->
  <script>
    const menuToggle = document.getElementById("menuToggle");
    const menu = document.getElementById("menu");
    const themeToggle = document.getElementById("themeToggle");
    const langToggle = document.getElementById("langToggle");
    const body = document.getElementById("body");
    const titleText = document.getElementById("titleText");
    const typedTextElement = document.getElementById("typed-text");

    // Textos más románticos
    const texts = {
      es: {
        title: "🌻 Feliz Día de las Flores Amarillas 💛",
        card: `Mi amor... 💖\n\nHoy el universo conspira para que te sientas amada, porque eres la flor más hermosa en mi jardín del alma. 🌻\n\nComo este girasol, siempre buscas la luz, irradias calor, das vida con tu presencia. 🌼\n\nCada latido mío canta tu nombre, cada suspiro lleva tu esencia. 💌\n\nEres mi refugio, mi paz, mi eterno amanecer. 🌅\n\nGracias por brillar tanto, por ser tan fuerte, tan dulce, tan tú.\n\nTe amo con cada pétalo de este girasol, con cada rayo de sol, con cada latido. ❤️\n\nHoy y siempre… eres mi todo. 🌌✨`
      },
      en: {
        title: "🌻 Happy Yellow Flowers Day 💛",
        card: `My love... 💖\n\nToday the universe conspires to make you feel loved, because you're the most beautiful flower in the garden of my soul. 🌻\n\nLike this sunflower, you always seek the light, radiate warmth, and bring life with your presence. 🌼\n\nEvery heartbeat of mine sings your name, every breath carries your essence. 💌\n\nYou are my shelter, my peace, my eternal sunrise. 🌅\n\nThank you for shining so bright, for being so strong, so sweet, so *you*.\n\nI love you with every petal of this sunflower, with every ray of sunlight, with every heartbeat. ❤️\n\nToday and always… you are my everything. 🌌✨`
      }
    };

    let currentLang = 'es';

    // Menú toggle
    menuToggle.addEventListener("click", () => {
      menu.classList.toggle("active");
    });

    // Modo claro
    themeToggle.addEventListener("click", () => {
      body.classList.toggle("light-mode");
      themeToggle.textContent = body.classList.contains("light-mode") 
        ? "🌞 Activar Modo Oscuro" 
        : "🌙 Activar Modo Claro";
    });

    // Cambiar idioma
    langToggle.addEventListener("click", () => {
      currentLang = currentLang === 'es' ? 'en' : 'es';
      titleText.textContent = texts[currentLang].title;
      typedTextElement.textContent = '';
      type();
      langToggle.textContent = currentLang === 'es' ? '🌐 Change to English' : '🌐 Cambiar a Español';
    });

    // Música
    const music = document.getElementById("bgMusic");
    music.volume = 0.2;
    document.body.addEventListener("click", function playMusic() {
      music.play().catch(e => console.log("Error:", e));
      document.body.removeEventListener("click", playMusic);
    }, { once: true });

    // Escritura automática
    function type() {
      let index = 0;
      const fullText = texts[currentLang].card;
      typedTextElement.textContent = '';
      function addChar() {
        if (index < fullText.length) {
          const char = fullText.charAt(index);
          typedTextElement.textContent += char === '\n' ? '\n' : char;
          index++;
          setTimeout(addChar, 40);
        }
      }
      addChar();
    }

    setTimeout(type, 1000);

    // Lluvia de palabras
    const loveWords = [
      "Amor 💖", "Corazón ❤️", "Mi vida 🌟", "Eres hermosa ✨", "Te adoro 💌", 
      "Para siempre 💍", "Gracias 🙏", "Te adoro 🥰", "Mi sol ☀️", "Mi todo 💞", 
      "🌼", "💛", "💜", "💕", "💞", "💖", "💗", "💓", "💝", "🌻", "💫"
    ];

    function createRainWord() {
      const word = document.createElement("div");
      word.classList.add("rain-word");
      word.textContent = loveWords[Math.floor(Math.random() * loveWords.length)];
      word.style.left = Math.random() * 90 + 5 + "vw";
      word.style.animationDuration = (Math.random() * 12 + 6) + "s";
      document.body.appendChild(word);
      setTimeout(() => word.remove(), 15000);
    }

    setInterval(createRainWord, 350);
    for (let i = 0; i < 20; i++) setTimeout(createRainWord, i * 400);

    // Explosión
    document.body.addEventListener("click", (e) => {
      for (let i = 0; i < 35; i++) {
        const item = document.createElement("div");
        item.classList.add("explosion-item");
        item.textContent = Math.random() > 0.4 ? "🌻" : "❤️‍🔥";
        item.style.left = e.clientX + "px";
        item.style.top = e.clientY + "px";
        const angle = Math.random() * Math.PI * 2;
        const distance = Math.random() * 200 + 100;
        const dx = Math.cos(angle) * distance;
        const dy = Math.sin(angle) * distance;
        item.style.setProperty('--dx', dx + 'px');
        item.style.setProperty('--dy', dy + 'px');
        document.body.appendChild(item);
        setTimeout(() => item.remove(), 1800);
      }
    });
  </script>
</body>
</html>
