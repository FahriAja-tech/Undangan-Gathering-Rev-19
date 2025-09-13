<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Undangan Gathering Sahabat IRMA</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@400;600;700&family=Roboto+Mono:wght@500&display=swap" rel="stylesheet" />

<style>
  /* Reset and base */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  html {
    scroll-behavior: smooth;
  }
  body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #f0f0f0;
    overflow-x: hidden;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2rem;
  }

  .container {
    background: rgba(20, 30, 45, 0.95);
    max-width: 700px;
    border-radius: 25px;
    padding: 3.5rem 4rem 4.5rem 4rem;
    box-shadow:
      0 0 20px rgba(255, 215, 0, 0.4),
      0 15px 40px rgba(0, 0, 0, 0.8);
    position: relative;
    opacity: 0; /* Initially hidden */
    animation: fadeSlideUp 1.8s ease 3s forwards; /* Delayed start */
    z-index: 10;
  }

  /* Elegant script for heading */
  h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 4.2rem;
    font-weight: 700;
    color: #ffd700;
    text-align: center;
    margin: 0 0 0.3rem 0;
    letter-spacing: 0.06em;
    text-shadow:
      0 0 10px #ffd700,
      0 0 25px #ffd700;
    animation: glowPulse 5s ease-in-out infinite;
  }

  h2 {
    font-weight: 600;
    font-size: 1.5rem;
    text-align: center;
    color: #eee;
    margin: 0 0 3rem 0;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    opacity: 0.9;
  }
  
  h3 {
    font-weight: 600;
    font-size: 1.3rem;
    text-align: center;
    color: #ffd700;
    margin: 3rem 0 1.5rem 0;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  p {
    font-size: 1.2rem;
    line-height: 1.75;
    margin-bottom: 2rem;
    color: #ddd;
  }

  p strong, .highlight {
    color: #ffd700;
    font-weight: 700;
  }

  a.location-link {
    color: #00d1ff;
    font-weight: 600;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  a.location-link:hover,
  a.location-link:focus {
    color: #00f0ff;
    text-decoration: underline;
    outline: none;
  }

  .footer {
    text-align: center;
    font-size: 1rem;
    color: #aaa;
    margin-top: 3.5rem;
    font-style: italic;
  }

  /* Animations */
  @keyframes fadeSlideUp {
    0% {
      opacity: 0;
      transform: translateY(40px);
    }
    100% {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes glowPulse {
    0%, 100% {
      text-shadow: 0 0 10px #ffd700, 0 0 25px #ffd700, 0 0 40px #ffd700;
      color: #ffd700;
    }
    50% {
      text-shadow: 0 0 20px #fffacd, 0 0 40px #fffacd, 0 0 60px #fffacd;
      color: #fffacd;
    }
  }
  
  /* --- CONVETY INTRO --- */
  #convety-overlay {
    position: fixed;
    inset: 0;
    background: linear-gradient(135deg, #0f2027, #2c5364);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    opacity: 1;
    animation: convetyFadeOut 1.5s ease-out 3s forwards;
  }
  #convety-overlay .convety-content {
      text-align: center;
  }
  #convety-overlay h1 {
    font-size: 4.8rem;
    animation: convetyTextPop 1.5s cubic-bezier(0.25, 1, 0.5, 1) 0.5s forwards;
    opacity: 0;
    transform: scale(0.8);
  }
  #convety-overlay p {
    font-weight: 600;
    font-size: 1.3rem;
    color: #ddd;
    margin-top: 0.5rem;
    letter-spacing: 0.05em;
    animation: convetyTextFade 1.5s ease 1.2s forwards;
    opacity: 0;
  }

  @keyframes convetyFadeOut {
    to { opacity: 0; pointer-events: none; }
  }
  @keyframes convetyTextPop {
    0% { opacity: 0; transform: scale(0.8) translateY(20px); }
    100% { opacity: 1; transform: scale(1) translateY(0); }
  }
  @keyframes convetyTextFade {
    0% { opacity: 0; transform: translateY(10px); }
    100% { opacity: 1; transform: translateY(0); }
  }
  
  /* --- COUNTDOWN TIMER --- */
  .countdown-container {
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    text-align: center;
    margin-bottom: 2rem;
  }
  .countdown-item {
    background: rgba(0, 0, 0, 0.2);
    padding: 1rem;
    border-radius: 10px;
    min-width: 90px;
    border: 1px solid rgba(255, 215, 0, 0.2);
  }
  .countdown-item span:first-child {
    display: block;
    font-family: 'Roboto Mono', monospace;
    font-size: 2.5rem;
    font-weight: 700;
    color: #ffd700;
    line-height: 1.1;
  }
  .countdown-item span:last-child {
    font-size: 0.9rem;
    text-transform: uppercase;
    color: #bbb;
    letter-spacing: 0.1em;
  }
  #countdown-finished {
      font-size: 1.5rem;
      color: #00ffaa;
      text-align: center;
      animation: glowPulse 2s infinite;
  }
  
  /* --- SPARKLES --- */
  .sparkle {
    position: absolute; border-radius: 50%; background: #ffd700; opacity: 0; filter: drop-shadow(0 0 5px #ffd700); animation: sparkle-animation 8s ease-in-out infinite;
  }
  .sparkle1 { width: 14px; height: 14px; top: 18px; left: 25px; animation-delay: 0s; }
  .sparkle2 { width: 10px; height: 10px; bottom: 30px; right: 35px; animation-delay: 2s; }
  .sparkle3 { width: 12px; height: 12px; top: 52%; right: 20px; animation-delay: 4s; }
  @keyframes sparkle-animation {
    0%, 100% { transform: translate(0, 0) scale(0.5); opacity: 0; }
    25%, 75% { opacity: 0.7; }
    50% { transform: translate(6px, -6px) scale(1.4); }
  }

  /* Responsive */
  @media (max-width: 700px) {
    body { padding: 1rem; }
    .container {
      padding: 2.5rem 1.5rem 3.5rem 1.5rem;
      max-width: 95vw;
    }
    h1 { font-size: 3.4rem; }
    h2 { font-size: 1.3rem; }
    p { font-size: 1.05rem; }
    .footer { font-size: 0.9rem; }
    
    .countdown-container { gap: 0.5rem; }
    .countdown-item { min-width: 70px; padding: 0.7rem; }
    .countdown-item span:first-child { font-size: 1.8rem; }
    .countdown-item span:last-child { font-size: 0.7rem; }
  }
</style>
</head>
<body>

<div id="convety-overlay" role="dialog" aria-modal="true" aria-label="Selamat Datang di Undangan Gathering Sahabat IRMA">
  <div class="convety-content">
    <h1>Gathering Sahabat IRMA</h1>
    <p>Sebuah Momen Kebersamaan</p>
  </div>
</div>

<main class="container" role="main" aria-labelledby="main-heading">
  <div class="sparkle sparkle1" aria-hidden="true"></div>
  <div class="sparkle sparkle2" aria-hidden="true"></div>
  <div class="sparkle sparkle3" aria-hidden="true"></div>

  <h1 id="main-heading">Gathering & Outbound</h1>
  <h2>Sahabat IRMA</h2>

  <p>Assalamu’alaikum Warahmatullahi Wabarakatuh,</p>

  <p>Dengan penuh semangat dan kebersamaan, Panitia Gathering Masjid Darul Iman mengundang Sahabat IRMA untuk hadir dalam acara <strong>Gathering & Outbound</strong> yang akan menjadi momen berharga untuk mempererat tali silaturahmi dan menikmati suasana alam yang menyegarkan.</p>
  
  <h3>Hitung Mundur Menuju Acara</h3>
  <div id="countdown" class="countdown-container" role="timer" aria-live="polite">
    <div class="countdown-item">
      <span id="days">00</span>
      <span>Hari</span>
    </div>
    <div class="countdown-item">
      <span id="hours">00</span>
      <span>Jam</span>
    </div>
    <div class="countdown-item">
      <span id="minutes">00</span>
      <span>Menit</span>
    </div>
    <div class="countdown-item">
      <span id="seconds">00</span>
      <span>Detik</span>
    </div>
  </div>


  <p><span class="highlight">Dresscode:</span> Atasan hitam kaos, bawahan hitam celana panjang. Jangan lupa membawa baju dan celana cadangan agar tetap nyaman selama kegiatan berlangsung.</p>

  <p><span class="highlight">Waktu & Tanggal:</span> Pukul 08:00 - 15:00 WITA, <time datetime="2025-09-14">14 September 2025</time></p>

  <p><span class="highlight">Lokasi:</span> <a href="https://maps.app.goo.gl/example" target="_blank" rel="noopener" class="location-link" aria-label="Lokasi Gathering di Google Maps">Binalatung Beach, Tarakan Timur, Tarakan City</a></p>

  <p>Kami sangat menantikan kehadiran Sahabat IRMA untuk bersama-sama menciptakan kenangan indah dan memperkuat ukhuwah.</p>

  <p>Wassalamu’alaikum Warahmatullahi Wabarakatuh,<br />Panitia Gathering Masjid Darul Iman</p>

  <div class="footer" aria-hidden="true">"Bersama kita kuat, bersama kita bahagia."</div>
</main>

<audio id="bg-music" loop preload="auto" aria-label="Lagu latar gathering">
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_1a1a7a7a7a.mp3?filename=chill-out-ambient-11043.mp3" type="audio/mpeg" />
  Browser Anda tidak mendukung elemen audio.
</audio>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    // --- Audio Logic ---
    const audio = document.getElementById('bg-music');
    if (audio) {
      audio.volume = 0.15; // Set initial volume

      const playAudio = () => {
        audio.play().catch(error => {
          console.log('Autoplay was prevented. User must interact with the page first.');
          // On some browsers, we need a user interaction to start audio.
          // We'll add a listener that tries to play on the first click anywhere.
          document.body.addEventListener('click', playAudio, { once: true });
        });
      };
      
      // Delay play slightly to allow other elements to load
      setTimeout(playAudio, 3500);
    }
    
    // --- Remove Convety Overlay ---
    const convety = document.getElementById('convety-overlay');
    if (convety) {
      setTimeout(() => {
        convety.style.display = 'none';
      }, 4500); // Wait until all animations are finished
    }

    // --- Countdown Timer Logic ---
    const countdownElement = document.getElementById('countdown');
    const daysEl = document.getElementById('days');
    const hoursEl = document.getElementById('hours');
    const minutesEl = document.getElementById('minutes');
    const secondsEl = document.getElementById('seconds');
    
    // Target date: 14 September 2025, 08:00:00 WITA (UTC+8)
    // JavaScript Date object handles timezones based on string format
    const targetDate = new Date('2025-09-14T08:00:00+08:00').getTime();

    const updateCountdown = () => {
      const now = new Date().getTime();
      const distance = targetDate - now;

      if (distance < 0) {
        clearInterval(countdownInterval);
        countdownElement.innerHTML = `<div id="countdown-finished">Acara Telah Dimulai!</div>`;
        return;
      }

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      daysEl.innerText = String(days).padStart(2, '0');
      hoursEl.innerText = String(hours).padStart(2, '0');
      minutesEl.innerText = String(minutes).padStart(2, '0');
      secondsEl.innerText = String(seconds).padStart(2, '0');
    };

    const countdownInterval = setInterval(updateCountdown, 1000);
    updateCountdown(); // Initial call
  });
</script>

</body>
</html>
