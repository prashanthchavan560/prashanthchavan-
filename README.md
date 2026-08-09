[index.html](https://github.com/user-attachments/files/30867503/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday Ammu! ✨</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;600&display=swap');

    :root {
      --deep-rose: #904056;
      --accent-gold: #d4a373;
      --soft-pink: #f4acb7;
      --card-bg: rgba(255, 255, 255, 0.94);
      --glass-border: rgba(255, 255, 255, 0.5);
    }

    * {
      box-sizing: border-box;
      cursor: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="%23ff4d6d"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>'), auto;
    }

    body {
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
      background: #3d0c1a;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow-x: hidden;
      color: #33272a;
    }

    .bg-glow {
      position: fixed;
      width: 450px; height: 450px;
      background: radial-gradient(circle, rgba(244,172,183,0.45) 0%, rgba(144,64,86,0) 70%);
      top: 5%; left: 5%; border-radius: 50%;
      animation: floatGlow 8s infinite alternate ease-in-out;
      z-index: 0;
    }

    .bg-glow-2 {
      position: fixed;
      width: 550px; height: 550px;
      background: radial-gradient(circle, rgba(212,163,115,0.35) 0%, rgba(144,64,86,0) 70%);
      bottom: 5%; right: 5%; border-radius: 50%;
      animation: floatGlow 10s infinite alternate-reverse ease-in-out;
      z-index: 0;
    }

    @keyframes floatGlow {
      0% { transform: translate(0, 0) scale(1); }
      100% { transform: translate(50px, 30px) scale(1.15); }
    }

    .main-wrapper {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 30px;
      width: 100%;
      max-width: 1350px;
      padding: 20px;
      z-index: 10;
      position: relative;
    }

    /* Side Portrait Galleries for Empty Desktop Space */
    .side-gallery {
      display: none;
      flex-direction: column;
      gap: 20px;
      width: 220px;
      flex-shrink: 0;
    }

    @media (min-width: 1100px) {
      .side-gallery { display: flex; }
    }

    .side-card {
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(12px);
      border: 1px solid var(--glass-border);
      border-radius: 20px;
      padding: 10px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.25);
      transition: transform 0.3s ease;
      animation: floatSide 6s infinite ease-in-out alternate;
    }

    .side-card:nth-child(2) {
      animation-delay: 3s;
    }

    .side-card:hover {
      transform: translateY(-5px) scale(1.03);
    }

    .side-card img {
      width: 100%;
      height: 240px;
      object-fit: cover;
      border-radius: 14px;
      margin-bottom: 8px;
    }

    .side-card span {
      font-size: 0.8rem;
      font-weight: 600;
      color: var(--deep-rose);
      display: block;
    }

    @keyframes floatSide {
      0% { transform: translateY(0px); }
      100% { transform: translateY(-12px); }
    }

    .container {
      position: relative;
      width: 100%;
      max-width: 620px;
      background: var(--card-bg);
      backdrop-filter: blur(15px);
      padding: 32px 22px;
      border-radius: 28px;
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.35);
      text-align: center;
      border: 1px solid var(--glass-border);
      animation: fadeIn 0.8s ease-out;
      margin-bottom: 20px;
    }

    .screen { display: none; }
    .active { display: block; }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1.cursive {
      font-family: 'Great Vibes', cursive;
      font-size: 3.2rem;
      color: var(--deep-rose);
      margin: 0 0 10px 0;
    }

    p { line-height: 1.7; color: #555; font-size: 0.95rem; }

    input[type="password"], input[type="text"] {
      padding: 12px 20px;
      width: 80%; max-width: 250px;
      border: 2px solid var(--soft-pink);
      border-radius: 30px;
      text-align: center;
      font-size: 16px;
      outline: none;
      margin: 10px 0;
      background: rgba(255,255,255,0.9);
      transition: all 0.3s;
    }

    input[type="password"]:focus, input[type="text"]:focus {
      border-color: var(--deep-rose);
      box-shadow: 0 0 15px rgba(144, 64, 86, 0.3);
    }

    button {
      background: linear-gradient(135deg, #b5838d, var(--deep-rose));
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 30px;
      font-size: 14px;
      font-weight: 600;
      box-shadow: 0 4px 15px rgba(144, 64, 86, 0.25);
      transition: all 0.3s ease;
      margin: 6px;
    }

    button:hover {
      transform: translateY(-2px) scale(1.03);
      box-shadow: 0 6px 20px rgba(144, 64, 86, 0.4);
    }

    /* Countdown Timer Box */
    .countdown-box {
      display: flex;
      justify-content: center;
      gap: 12px;
      margin: 15px 0;
    }

    .time-unit {
      background: #fdf0ed;
      border: 1px solid var(--soft-pink);
      padding: 8px 12px;
      border-radius: 12px;
      min-width: 60px;
    }

    .time-unit span {
      display: block;
      font-weight: bold;
      font-size: 18px;
      color: var(--deep-rose);
    }

    .time-unit label {
      font-size: 10px;
      color: #777;
      text-transform: uppercase;
    }

    /* Floating Audio Controller */
    #music-control-panel {
      position: fixed;
      top: 15px; right: 15px;
      z-index: 100;
      background: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(8px);
      border: 1px solid var(--glass-border);
      padding: 8px 12px;
      border-radius: 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      display: flex;
      align-items: center;
      gap: 6px;
    }

    select.music-select {
      border: 1px solid var(--soft-pink);
      border-radius: 12px;
      padding: 4px 8px;
      font-size: 11px;
      outline: none;
      color: var(--deep-rose);
    }

    .teddy-banner {
      width: 120px; height: auto;
      margin-bottom: 10px;
      border-radius: 12px;
    }

    .teddy-box {
      margin: 15px auto;
      padding: 15px;
      background: #fdf0ed;
      border-radius: 20px;
      border: 1px dashed var(--soft-pink);
    }

    .rose-btn {
      font-size: 40px;
      background: none; border: none; box-shadow: none;
      cursor: pointer; margin-top: 5px;
      transition: transform 0.3s ease;
    }

    .rose-btn:hover {
      transform: scale(1.2) rotate(10deg);
      box-shadow: none;
    }

    /* Interactive 3D Envelope */
    .envelope-box {
      perspective: 1000px;
      margin: 20px auto;
      width: 220px;
      height: 120px;
      cursor: pointer;
    }

    .envelope-inner {
      width: 100%;
      height: 100%;
      background: #fdf0ed;
      border: 2px dashed var(--soft-pink);
      border-radius: 16px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      transition: transform 0.6s;
      transform-style: preserve-3d;
      box-shadow: 0 8px 20px rgba(0,0,0,0.05);
    }

    .envelope-box:hover .envelope-inner {
      transform: rotateY(15deg) scale(1.03);
    }

    /* Modal Sizing Fixes for Face Visibility */
    .modal-overlay {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.7);
      backdrop-filter: blur(6px);
      z-index: 1000;
      justify-content: center;
      align-items: center;
    }

    .modal-card {
      background: white;
      padding: 22px;
      border-radius: 24px;
      max-width: 420px;
      width: 88%;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.25);
      animation: popIn 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      position: relative;
    }

    @keyframes popIn {
      from { transform: scale(0.6); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    /* Portrait Image Display Fix - Entire Face & Body Visible */
    .modal-img {
      width: 100%;
      height: 320px;
      object-fit: contain;
      object-position: top center;
      border-radius: 16px;
      background: #fdf0ed;
      padding: 6px;
      border: 1px solid var(--soft-pink);
      margin-bottom: 12px;
    }

    .captions-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
      gap: 12px;
      margin: 20px 0;
    }

    .card {
      background: #fdf0ed;
      padding: 15px 10px;
      border-radius: 16px;
      font-size: 0.85rem;
      font-weight: 600;
      color: var(--deep-rose);
      border: 1px solid var(--soft-pink);
      transition: transform 0.2s;
    }

    .card:hover { transform: scale(1.03); }

    .timeline {
      text-align: left;
      margin: 20px 0;
      position: relative;
      padding-left: 15px;
      border-left: 3px solid var(--soft-pink);
    }

    .timeline-item {
      margin-bottom: 20px;
      position: relative;
      cursor: pointer;
    }

    .timeline-date {
      font-size: 0.8rem;
      font-weight: bold;
      color: var(--deep-rose);
      background: #fdf0ed;
      padding: 2px 8px;
      border-radius: 10px;
      display: inline-block;
      margin-bottom: 4px;
    }

    .timeline-text {
      font-size: 0.9rem;
      color: #444;
      line-height: 1.5;
    }

    .runaway-arena {
      height: 180px;
      position: relative;
      margin-top: 20px;
      border-radius: 16px;
      background: rgba(253, 240, 237, 0.5);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    #btn-no { position: absolute; transition: all 0.15s ease-out; background: #6c757d; }

    .wheel-box {
      margin: 20px auto;
      width: 200px; height: 200px;
      border-radius: 50%;
      border: 6px solid var(--deep-rose);
      display: flex;
      justify-content: center; align-items: center;
      font-size: 11px; font-weight: bold;
      color: var(--deep-rose); background: #ffffff;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
      transition: transform 3s cubic-bezier(0.15, 0.9, 0.15, 1);
      text-align: center;
      padding: 10px;
    }

    .particle {
      position: fixed;
      pointer-events: none;
      z-index: 2000;
      animation: fall 3s linear forwards;
    }

    @keyframes fall {
      0% { transform: translateY(-10vh) rotate(0deg); opacity: 1; }
      100% { transform: translateY(105vh) rotate(360deg); opacity: 0; }
    }

    footer {
      position: relative;
      z-index: 10;
      font-size: 10px;
      color: rgba(255, 255, 255, 0.6);
      text-align: center;
      margin-bottom: 15px;
      letter-spacing: 1px;
    }

    .error-msg { color: #d90429; font-size: 13px; display: none; }
  </style>
</head>
<body>

  <div class="bg-glow"></div>
  <div class="bg-glow-2"></div>

  <!-- Floating Audio Controller -->
  <div id="music-control-panel">
    <button onclick="toggleMusic()" id="music-toggle-btn" style="padding: 4px 10px; font-size: 11px; margin:0;">🎵 Play Music</button>
    <select id="track-select" class="music-select" onchange="changeTrack()">
      <option value="0">Blue Instrumental (Yung)</option>
      <option value="1">Soft Romantic Piano</option>
      <option value="2">Acoustic Love Melody</option>
    </select>
  </div>

  <audio id="bg-music" loop>
    <source id="music-source" src="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=blue-111666.mp3" type="audio/mpeg">
  </audio>

  <!-- Main Section Wrapper with Side Galleries -->
  <div class="main-wrapper">

    <!-- Left Side Portrait Gallery (Desktop) -->
    <div class="side-gallery">
      <div class="side-card" onclick="openPopup(img1, 'Pure Golden Heart ✨', 'Your heart is as pure, royal, and shining as gold!')">
        <img src="https://lh3.googleusercontent.com/d/1lHDxKxRuP_0H7yG5GgF1Sd8sNuPO2Z4l" alt="Ammu Black Saree">
        <span>✨ Royal Elegance</span>
      </div>
      <div class="side-card" onclick="openPopup(img3, 'Soft & Elegant Vibe 🌸', 'Everything about you is so graceful and beautiful.')">
        <img src="https://lh3.googleusercontent.com/d/1xOgH1V4VrlR4ftM_8LTMRagrTr-38rZy" alt="Ammu Green Saree">
        <span>🌸 Soft Grace</span>
      </div>
    </div>

    <!-- Center Main Container -->
    <div class="container">

      <!-- Screen 1: Password Gate & Countdown -->
      <div id="login-screen" class="screen active">
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3ZtdHZzdXpneDFuNDFsdGNsMnRjcTNwYmxoMmJtcXZicWh1Z3h3eCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Lp8al4A28BwO2B3TqV/giphy.gif" alt="Pookie Teddy" class="teddy-banner">
        <h1 class="cursive">Welcome Pookie ✨</h1>
        
        <p style="margin-bottom: 5px; font-weight: 600; color: var(--deep-rose);">Countdown to August 23rd Midnight ⏰</p>
        <div class="countdown-box">
          <div class="time-unit"><span id="cd-days">00</span><label>Days</label></div>
          <div class="time-unit"><span id="cd-hours">00</span><label>Hours</label></div>
          <div class="time-unit"><span id="cd-mins">00</span><label>Mins</label></div>
          <div class="time-unit"><span id="cd-secs">00</span><label>Secs</label></div>
        </div>

        <p>Enter the passcode to unlock your birthday surprise!</p>
        <input type="password" id="password-input" maxlength="4" placeholder="••••">
        <br>
        <button onclick="checkPassword()">Unlock Birthday Magic 💖</button>
        <p id="error-msg" class="error-msg">Incorrect passcode! Hint: Your birthday (2308) 😉</p>
      </div>

      <!-- Screen 2: Main Hub -->
      <div id="main-screen" class="screen">
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbnZ3ZHkyeDRldXdybHRoZXByaTl3bWN3ZHllcjlydzRkOWU0ZjZwNyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/MDJ9IbxxvDUQM/giphy.gif" alt="Cute White Teddy" class="teddy-banner">
        <h1 class="cursive">Happy Birthday, Ammu! 🌹</h1>
        <p style="letter-spacing: 2px; text-transform: uppercase; font-size: 0.8rem; color: #b5838d;">23 • 08 • 2010</p>
        
        <div class="teddy-box">
          <p style="margin: 5px 0; font-weight: 600; color: var(--deep-rose);">Pookie Teddy brought a special rose for you!</p>
          <p style="font-size: 0.85rem; color: #777;">Click the rose below to reveal your infinity promise 👇</p>
          <button class="rose-btn" onclick="openRingModal()">🌹</button>
        </div>

        <!-- Animated Envelope -->
        <div class="envelope-box" onclick="openModal('letter-modal')">
          <div class="envelope-inner">
            <div style="font-size: 38px;">💌</div>
            <div style="font-size: 0.85rem; font-weight: 600; color: var(--deep-rose);">Tap to Open Birthday Letter</div>
          </div>
        </div>

        <h3>Tap to Open Surprise Cards 🎁</h3>
        <div class="captions-grid">
          <div class="card" onclick="openPopup(img1, 'Pure Golden Heart ✨', 'Your heart is as pure, royal, and shining as gold!')">✨ Pure Golden Heart</div>
          <div class="card" onclick="openPopup(img3, 'Soft & Elegant Vibe 🌸', 'Everything about you is so graceful and beautiful.')">🌸 Soft & Elegant Vibe</div>
          <div class="card" onclick="openPopup(img4, 'Forever My Pookie 👑', 'No matter what, you will always be my Pookie!')">👑 Forever My Pookie</div>
          <div class="card" onclick="openPopup(img2, 'Sweetest Smile Ever 💖', 'Your smile instantly brightens up my whole day.')">💖 Sweetest Smile Ever</div>
        </div>

        <h3>Explore Your Pages 💖</h3>
        <button onclick="showScreen('timeline-screen')">📖 Our Memory Lane & Special Dates</button>
        <button onclick="showScreen('wish-screen')">✨ Make a Birthday Wish Box</button>
        <button onclick="showScreen('runaway-screen')">🔒 The Secret Question</button>
        <button onclick="showScreen('quiz-screen')">🧠 Pookie Quiz & Certificate</button>
        <button onclick="showScreen('wheel-screen')">🎡 Birthday Fortune Wheel</button>
        <button onclick="showScreen('game-screen')">🎈 Pop the Hearts</button>
      </div>

      <!-- Screen 3: Birthday Wish Box -->
      <div id="wish-screen" class="screen">
        <h1 class="cursive">Make Your Birthday Wish 🌠</h1>
        <p>Type your special birthday wish below and send it into the universe!</p>
        <input type="text" id="user-wish" placeholder="Type your birthday wish here..." style="width: 90%; max-width: 350px;">
        <br>
        <button onclick="triggerWishExplosion()">Submit Wish & Release Magic 🎆</button>
        <br><br>
        <button onclick="showScreen('main-screen')">⬅ Back to Main Menu</button>
      </div>

      <!-- Screen 4: Quiz & Certificate -->
      <div id="quiz-screen" class="screen">
        <h2>The Official Pookie Quiz 🧐</h2>
        <div id="quiz-container">
          <p id="quiz-question">Loading question...</p>
          <div id="quiz-options"></div>
        </div>
        <br>
        <button onclick="showScreen('main-screen')">⬅ Back to Main Menu</button>
      </div>

      <!-- Screen 5: Memory Lane -->
      <div id="timeline-screen" class="screen">
        <h1 class="cursive">Our Memory Lane 🗓️</h1>
        <p>A few unforgettable moments created with you...</p>

        <div class="timeline">
          <div class="timeline-item" onclick="openPopup(img1, 'The Proposal 💍', 'August 19, 2025: The magical day I poured my heart out and proposed to you!')">
            <span class="timeline-date">19 / 08 / 2025</span>
            <div class="timeline-text"><b>The Special Proposal:</b> The day I expressed my true feelings for you and asked you to be mine forever. 💖</div>
          </div>

          <div class="timeline-item" onclick="openPopup(img4, 'Endless Late Night Chat 📱', 'September 12, 2025: Hours flew by like minutes during our late-night WhatsApp conversation.')">
            <span class="timeline-date">12 / 09 / 2025</span>
            <div class="timeline-text"><b>Long WhatsApp Conversation:</b> We talked endlessly through the night, sharing our deepest thoughts, laughs, and secrets. 💬✨</div>
          </div>

          <div class="timeline-item" onclick="openPopup(img3, 'Our First Warm Hug 🤗', 'October 16, 2025: The moment time stood still when we shared our very first hug.')">
            <span class="timeline-date">16 / 10 / 2025</span>
            <div class="timeline-text"><b>Our First Warm Hug:</b> Holding you close for the very first time felt like the safest and sweetest place in the entire world. 🤗❤️</div>
          </div>

          <div class="timeline-item" onclick="openPopup(img5, 'Midnight Rose Bouquet 🌹', 'November 17, 2025 (12:48 AM): Sending a virtual rose bouquet to make sure you felt loved at midnight.')">
            <span class="timeline-date">17 / 11 / 2025 — 12:48 AM</span>
            <div class="timeline-text"><b>Midnight Rose Bouquet:</b> Right at 12:48 AM during the quiet midnight, sending you a lovely rose bouquet to bring a smile to your face before sleep. 🌹✨</div>
          </div>

          <div class="timeline-item" onclick="openPopup(img2, 'First Valentine KitKat 🍫', 'Our special Valentine KitKat chocolate memory!')">
            <span class="timeline-date">Special Valentine Memory</span>
            <div class="timeline-text"><b>First KitKat Chocolate:</b> Sweet memories shared with our favorite Valentine KitKat chocolate treat! 🍫💖</div>
          </div>
        </div>

        <button onclick="showScreen('main-screen')">⬅ Back to Main Menu</button>
      </div>

      <!-- Screen 6: Runaway No Game -->
      <div id="runaway-screen" class="screen">
        <h1 class="cursive">One Important Question...</h1>
        <h2>Will you always remain my Pookie? 🥺</h2>
        
        <div class="runaway-arena" id="arena">
          <button id="btn-yes" onclick="answerYes()" style="font-size: 18px; padding: 12px 28px;">YES! 💖</button>
          <button id="btn-no" onmouseover="dodgeNo()" onclick="dodgeNo()">NO 😜</button>
        </div>
        
        <div id="yes-result" style="display: none; margin-top: 15px;">
          <img id="yes-img-tag" class="modal-img" alt="Princess Treatment">
          <h3 style="color: var(--deep-rose); margin-bottom: 5px;">I knew it! 🥳✨</h3>
          <p style="font-size: 0.95rem; font-weight: 600; color: #333;">"Thank you for choosing me! I will treat you like a princess for as long as I live." 👑💖</p>
        </div>
        <br>
        <button onclick="showScreen('main-screen')">⬅ Back to Main Menu</button>
      </div>

      <!-- Screen 7: Fortune Wheel -->
      <div id="wheel-screen" class="screen">
        <h2>Spin Ammu's Fortune Wheel 🎡</h2>
        <p>Tap Spin to reveal your birthday surprise!</p>
        <div class="wheel-box" id="wheel">Spin to Reveal Wish! ✨</div>
        <br>
        <button onclick="spinWheel()">Spin Wheel ✨</button>
        <button onclick="showScreen('main-screen')">⬅ Back</button>
      </div>

      <!-- Screen 8: Heart Pop Game -->
      <div id="game-screen" class="screen">
        <h2>Pop Ammu's Hearts 💕</h2>
        <p>Tap 5 hearts as fast as you can!</p>
        <p>Score: <b><span id="score">0</span> / 5</b></p>
        <div id="game-box" style="width: 100%; height: 200px; background: #fef6f8; border-radius: 16px; position: relative; overflow: hidden; margin: 15px 0; border: 1px dashed var(--soft-pink);"></div>
        <button onclick="showScreen('main-screen')">⬅ Back</button>
        <button onclick="resetGame()">Play Again 🔄</button>
      </div>

    </div>

    <!-- Right Side Portrait Gallery (Desktop) -->
    <div class="side-gallery">
      <div class="side-card" onclick="openPopup(img2, 'Sweetest Smile Ever 💖', 'Your smile instantly brightens up my whole day.')">
        <img src="https://lh3.googleusercontent.com/d/1-_t3KYiHxRu2hDFQ6y3DyaBfNEJlRTGD" alt="Ammu Red Dress">
        <span>💖 Brightest Smile</span>
      </div>
      <div class="side-card" onclick="openPopup(img4, 'Forever My Pookie 👑', 'No matter what, you will always be my Pookie!')">
        <img src="https://lh3.googleusercontent.com/d/1iiQDNgk-bo6RUZ294-8U6ywvcRZ_uLmC" alt="Ammu Cute Selfie">
        <span>👑 Cutest Pookie</span>
      </div>
    </div>

  </div>

  <!-- Modal: Birthday Letter -->
  <div id="letter-modal" class="modal-overlay">
    <div class="modal-card">
      <h2 style="font-family: 'Great Vibes', cursive; font-size: 2.5rem; color: var(--deep-rose); margin: 0;">Dearest Ammu,</h2>
      <p style="text-align: left; font-size: 0.9rem; color: #444; line-height: 1.6; margin: 15px 0;">
        Happy Birthday to the sweetest soul who brings so much grace, warmth, and light into my life! Watching you grow into such an incredible person is a true gift. May this year fulfill all your wishes and fill your heart with endless joy. Never stop being the amazing Pookie you are! ✨💕
      </p>
      <button onclick="closeModal('letter-modal')">Close Letter 💌</button>
    </div>
  </div>

  <!-- Modal: Infinity Ring Promise -->
  <div id="ring-modal" class="modal-overlay">
    <div class="modal-card">
      <div style="font-size: 60px; margin-bottom: 5px;">♾️💍</div>
      <h2 style="color: var(--deep-rose); font-family: 'Great Vibes', cursive; font-size: 2.4rem; margin: 0;">My Infinity Promise</h2>
      <p style="color: #444; font-size: 0.95rem; margin: 15px 0;">
        "I promise to stay with you for a lifetime, through every laugh, every moment, and every single day. Infinity & beyond, you will always be my Pookie." 💖✨
      </p>
      <button onclick="closeModal('ring-modal')">Keep My Heart Forever 🔒</button>
    </div>
  </div>

  <!-- Modal: Official Pookie Certificate -->
  <div id="certificate-modal" class="modal-overlay">
    <div class="modal-card" style="border: 4px double var(--accent-gold); background: #fffdfa;">
      <div style="font-size: 50px;">👑📜</div>
      <h2 style="font-family: 'Great Vibes', cursive; font-size: 2.5rem; color: var(--deep-rose); margin:0;">Official Certificate</h2>
      <p style="font-size: 0.8rem; letter-spacing: 2px; text-transform: uppercase; color: var(--accent-gold);">Presented To</p>
      <h3 style="font-size: 1.8rem; color: var(--deep-rose); margin: 5px 0;">AMMU</h3>
      <p style="font-size: 0.9rem; color: #444; margin: 10px 0;">Is hereby certified as <b>100% The Cutest Pookie & Princess</b> in the whole universe! 💖✨</p>
      <button onclick="closeModal('certificate-modal')">Claim My Title 👑</button>
    </div>
  </div>

  <!-- Generic Image Pop-up Modal -->
  <div id="popup-modal" class="modal-overlay">
    <div class="modal-card">
      <img id="popup-img" src="" class="modal-img" alt="Pop up image">
      <h3 id="popup-title" style="color: var(--deep-rose); margin: 5px 0;"></h3>
      <p id="popup-desc" style="font-size: 0.9rem; color: #555; margin-bottom: 15px;"></p>
      <button onclick="closeModal('popup-modal')">Close ✨</button>
    </div>
  </div>

  <!-- Footer Credit -->
  <footer>
    prashanth webdeveloper
  </footer>

  <script>
    // Direct Google Drive Image Links
    const img1 = "https://lh3.googleusercontent.com/d/1lHDxKxRuP_0H7yG5GgF1Sd8sNuPO2Z4l"; 
    const img2 = "https://lh3.googleusercontent.com/d/1-_t3KYiHxRu2hDFQ6y3DyaBfNEJlRTGD"; 
    const img3 = "https://lh3.googleusercontent.com/d/1xOgH1V4VrlR4ftM_8LTMRagrTr-38rZy"; 
    const img4 = "https://lh3.googleusercontent.com/d/1iiQDNgk-bo6RUZ294-8U6ywvcRZ_uLmC"; 
    const img5 = "https://lh3.googleusercontent.com/d/1HtXdtBynAKqLl7CAmOThL4DZZtHMj2CV"; 

    const CORRECT_PASS = "2308";
    
    /* Music Tracks */
    const tracks = [
      "https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=blue-111666.mp3",
      "https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8a7321a.mp3?filename=romantic-piano-10821.mp3",
      "https://cdn.pixabay.com/download/audio/2022/10/25/audio_2e2b963bf7.mp3?filename=sweet-acoustic-124888.mp3"
    ];

    const audio = document.getElementById('bg-music');
    let isPlaying = false;

    function toggleMusic() {
      const btn = document.getElementById('music-toggle-btn');
      if (isPlaying) {
        audio.pause();
        btn.innerText = "🎵 Play Music";
      } else {
        audio.play().catch(e => console.log("Autoplay blocked"));
        btn.innerText = "⏸️ Pause";
      }
      isPlaying = !isPlaying;
    }

    function changeTrack() {
      const idx = document.getElementById('track-select').value;
      audio.src = tracks[idx];
      if (isPlaying) audio.play();
    }

    function checkPassword() {
      const input = document.getElementById('password-input').value;
      if (input === CORRECT_PASS) {
        showScreen('main-screen');
        if (!isPlaying) toggleMusic();
      } else {
        document.getElementById('error-msg').style.display = 'block';
      }
    }

    function showScreen(screenId) {
      document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
      document.getElementById(screenId).classList.add('active');
      if(screenId === 'game-screen') resetGame();
      if(screenId === 'runaway-screen') resetRunaway();
      if(screenId === 'quiz-screen') loadQuiz();
    }

    function openRingModal() { document.getElementById('ring-modal').style.display = 'flex'; }
    function openModal(modalId) { document.getElementById(modalId).style.display = 'flex'; }
    
    function openPopup(imgUrl, title, desc) {
      document.getElementById('popup-img').src = imgUrl;
      document.getElementById('popup-title').innerText = title;
      document.getElementById('popup-desc').innerText = desc;
      document.getElementById('popup-modal').style.display = 'flex';
    }

    function closeModal(modalId) { document.getElementById(modalId).style.display = 'none'; }

    /* Countdown Timer */
    function updateCountdown() {
      const now = new Date();
      let targetYear = now.getFullYear();
      let target = new Date(`August 23, ${targetYear} 00:00:00`);
      
      if (now > target) {
        target = new Date(`August 23, ${targetYear + 1} 00:00:00`);
      }

      const diff = target - now;
      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const mins = Math.floor((diff / 1000 / 60) % 60);
      const secs = Math.floor((diff / 1000) % 60);

      document.getElementById('cd-days').innerText = days < 10 ? '0' + days : days;
      document.getElementById('cd-hours').innerText = hours < 10 ? '0' + hours : hours;
      document.getElementById('cd-mins').innerText = mins < 10 ? '0' + mins : mins;
      document.getElementById('cd-secs').innerText = secs < 10 ? '0' + secs : secs;
    }
    setInterval(updateCountdown, 1000);
    updateCountdown();

    /* Wish Box Exploding Confetti Effect */
    function triggerWishExplosion() {
      const wish = document.getElementById('user-wish').value;
      if (!wish) {
        alert("Please type a wish first! ✨");
        return;
      }
      
      const symbols = ['💖', '✨', '🎈', '🌸', '🎂', '👑'];
      for (let i = 0; i < 40; i++) {
        const p = document.createElement('div');
        p.className = 'particle';
        p.innerText = symbols[Math.floor(Math.random() * symbols.length)];
        p.style.left = Math.random() * 100 + 'vw';
        p.style.fontSize = (Math.random() * 20 + 20) + 'px';
        p.style.animationDuration = (Math.random() * 2 + 1.5) + 's';
        document.body.appendChild(p);
        setTimeout(() => p.remove(), 3500);
      }
      alert(`Your wish: "${wish}" has been sent into the stars! May it all come true! ✨💖`);
    }

    /* Runaway Button Logic */
    function dodgeNo() {
      const btnNo = document.getElementById('btn-no');
      const arena = document.getElementById('arena');
      const maxX = arena.clientWidth - btnNo.clientWidth - 20;
      const maxY = arena.clientHeight - btnNo.clientHeight - 20;
      btnNo.style.left = Math.floor(Math.random() * maxX) + 'px';
      btnNo.style.top = Math.floor(Math.random() * maxY) + 'px';
    }

    function resetRunaway() {
      const btnNo = document.getElementById('btn-no');
      btnNo.style.left = '60%';
      btnNo.style.top = '40%';
      document.getElementById('yes-result').style.display = 'none';
    }

    function answerYes() {
      document.getElementById('yes-img-tag').src = img2;
      document.getElementById('yes-result').style.display = 'block';
    }

    /* Quiz Logic */
    const quizData = [
      { q: "What makes Ammu's birthday so special?", options: ["It comes once a year", "It's the day a princess was born 👑", "All of the above"], correct: 2 },
      { q: "What is Ammu's superpower?", options: ["Making everyone smile instantly 😊", "Being the cutest pookie", "Both!"], correct: 2 }
    ];

    let currentQ = 0;
    function loadQuiz() { currentQ = 0; showQuestion(); }

    function showQuestion() {
      if (currentQ >= quizData.length) {
        openModal('certificate-modal');
        return;
      }
      const q = quizData[currentQ];
      document.getElementById('quiz-question').innerText = q.q;
      const optionsDiv = document.getElementById('quiz-options');
      optionsDiv.innerHTML = '';
      q.options.forEach((opt) => {
        const btn = document.createElement('button');
        btn.style.width = '100%';
        btn.style.margin = '6px 0';
        btn.innerText = opt;
        btn.onclick = () => { currentQ++; showQuestion(); };
        optionsDiv.appendChild(btn);
      });
    }

    /* Heart Pop Game */
    let score = 0;
    function resetGame() { score = 0; document.getElementById('score').innerText = score; spawnHeart(); }

    function spawnHeart() {
      const box = document.getElementById('game-box');
      box.innerHTML = '';
      if (score >= 5) {
        box.innerHTML = '<h3 style="line-height:200px; color: var(--deep-rose); margin:0;">🎉 You unlocked infinite love! 💖✨</h3>';
        return;
      }
      const heart = document.createElement('div');
      heart.style.position = 'absolute';
      heart.style.fontSize = '32px';
      heart.style.cursor = 'pointer';
      const symbols = ['💖', '🌸', '✨', '👑', '🎂'];
      heart.innerText = symbols[Math.floor(Math.random() * symbols.length)];
      heart.style.left = Math.random() * (box.clientWidth - 50) + 'px';
      heart.style.top = Math.random() * (box.clientHeight - 50) + 'px';
      heart.onclick = function() {
        score++;
        document.getElementById('score').innerText = score;
        spawnHeart();
      };
      box.appendChild(heart);
    }

    /* Fortune Wheel */
    const fortunes = [
      { text: "Late Night Ice Cream & Long Drive 🍦🚘", img: img1 },
      { text: "Unlimited Favorite Treat Card 🍰", img: img2 },
      { text: "Lifetime Happiness Pass 💖", img: img3 },
      { text: "Your Biggest Wish Comes True ✨", img: img4 },
      { text: "Infinite Hugs Coupon 🤗", img: img5 }
    ];

    function spinWheel() {
      const wheel = document.getElementById('wheel');
      const randomRot = 1440 + Math.floor(Math.random() * 360);
      wheel.style.transform = `rotate(${randomRot}deg)`;
      
      setTimeout(() => {
        const picked = fortunes[Math.floor(Math.random() * fortunes.length)];
        wheel.innerText = picked.text;
        openPopup(picked.img, '🎉 Birthday Surprise Won!', `You won: ${picked.text}`);
      }, 3000);
    }
  </script>
</body>
</html>
