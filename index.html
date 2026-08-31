<!DOCTYPE html>
<html lang="kmr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title id="appTitle">دڵی درەوشاوە و مینا</title>

  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="theme-color" content="#050205" id="metaThemeColor">
  <link rel="manifest" id="manifestPlaceholder">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      -webkit-touch-callout: none;
      -webkit-user-select: none;
      user-select: none;
      touch-action: none;
    }
    html, body {
      width: 100%;
      height: 100%;
      overflow: hidden;
      background-color: #050205;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    }
    canvas {
      display: block;
      width: 100vw;
      height: 100vh;
      position: absolute;
      top: 0;
      left: 0;
      z-index: 1;
    }

    .audio-banner {
      position: absolute;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 20;
      background: rgba(236, 72, 153, 0.9);
      color: #fff;
      padding: 10px 22px;
      border-radius: 20px;
      font-size: 14px;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0 4px 20px rgba(236, 72, 153, 0.5);
      backdrop-filter: blur(8px);
      transition: all 0.3s ease;
      border: 1px solid rgba(255,255,255,0.5);
      text-align: center;
    }
    .audio-banner.hidden {
      opacity: 0;
      pointer-events: none;
      transform: translate(-50%, -20px);
    }

    .controls-container {
      position: absolute;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 10;
      display: flex;
      flex-direction: column;
      gap: 10px;
      background: rgba(15, 10, 20, 0.65);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      padding: 12px 20px;
      border-radius: 24px;
      border: 1px solid rgba(255, 255, 255, 0.15);
      box-shadow: 0 15px 35px rgba(0,0,0,0.6);
      align-items: center;
      max-width: 95vw;
    }

    .row {
      display: flex;
      gap: 10px;
      align-items: center;
      justify-content: center;
      flex-wrap: wrap;
    }

    .btn {
      padding: 6px 12px;
      border-radius: 12px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      background: rgba(255, 255, 255, 0.08);
      color: #fff;
      font-size: 12px;
      cursor: pointer;
      transition: all 0.2s ease;
      outline: none;
    }

    .btn:hover, .btn.active {
      background: rgba(255, 255, 255, 0.25);
      border-color: #fff;
      transform: scale(1.05);
    }

    .color-btn {
      width: 28px;
      height: 28px;
      border-radius: 50%;
      border: 2px solid rgba(255, 255, 255, 0.6);
      cursor: pointer;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      outline: none;
    }

    .color-btn.active {
      transform: scale(1.2);
      border-color: #fff;
      box-shadow: 0 0 12px currentColor;
    }
  </style>
</head>
<body>

<!-- دوگمەی سەرەکی بۆ کارپێکردنی دەنگ بە یەک کلیک -->
<div id="audioBanner" class="audio-banner">🔊 لێرە کلیک بکە بۆ کارپێکردنی دەنگی "مینا"</div>

<canvas id="mainCanvas"></canvas>

<div class="controls-container">
  <div class="row" id="shapeSelector">
    <button class="btn active" data-shape="bigHeart">❤ دڵی گەورە</button>
    <button class="btn" data-shape="smallHeart">💕 دڵی بچووک</button>
    <button class="btn" data-shape="letterM">Ⓜ پیتێ </button>
    <button class="btn" data-shape="circle">⚪ بازنەی درەوشاوە</button>
  </div>
  <div class="row" id="colorPicker">
    <button class="color-btn active" style="background: #ec4899; color: #ec4899;" data-theme="pink"></button>
    <button class="color-btn" style="background: #3b82f6; color: #3b82f6;" data-theme="blue"></button>
    <button class="color-btn" style="background: #f59e0b; color: #f59e0b;" data-theme="gold"></button>
    <button class="color-btn" style="background: #a855f7; color: #a855f7;" data-theme="purple"></button>
    <button class="color-btn" style="background: #10b981; color: #10b981;" data-theme="green"></button>
    <button class="color-btn" style="background: #ef4444; color: #ef4444;" data-theme="red"></button>
  </div>
</div>

<script>
  let audioCtx = null;
  let soundReady = false;

  const banner = document.getElementById("audioBanner");
  banner.addEventListener("click", () => {
    try {
      audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      if (audioCtx.state === 'suspended') {
        audioCtx.resume();
      }
      soundReady = true;
      banner.classList.add("hidden");
      playMinaChime(); // لێدانی تاقیکردنەوەی دەنگ
    } catch(e) {}
  });

  // دەنگی تایبەت کە هاوشێوەی دەنگە ناسکەکان دەڵێت مینا
  function playMinaChime() {
    if (!audioCtx) return;
    try {
      const now = audioCtx.currentTime;
      
      // نۆتی یەکەم
      const osc1 = audioCtx.createOscillator();
      const gain1 = audioCtx.createGain();
      osc1.type = 'sine';
      osc1.frequency.setValueAtTime(523.25, now); // C5
      osc1.frequency.exponentialRampToValueAtTime(659.25, now + 0.15); // E5
      
      gain1.gain.setValueAtTime(0.25, now);
      gain1.gain.exponentialRampToValueAtTime(0.001, now + 0.35);
      
      osc1.connect(gain1);
      gain1.connect(audioCtx.destination);
      
      osc1.start(now);
      osc1.stop(now + 0.35);

      // نۆتی دووەم (دواکەوتوو بۆ ناسکی)
      const osc2 = audioCtx.createOscillator();
      const gain2 = audioCtx.createGain();
      osc2.type = 'triangle';
      osc2.frequency.setValueAtTime(783.99, now + 0.1); // G5
      osc2.frequency.exponentialRampToValueAtTime(1046.50, now + 0.3); // C6
      
      gain2.gain.setValueAtTime(0.2, now + 0.1);
      gain2.gain.exponentialRampToValueAtTime(0.001, now + 0.45);
      
      osc2.connect(gain2);
      gain2.connect(audioCtx.destination);
      
      osc2.start(now + 0.1);
      osc2.stop(now + 0.45);
    } catch(e) {}
  }

  const THEMES = {
    pink: { bg: "#050205", shades: ["#ec4899", "#f43f5e", "#f472b6", "#fb7185", "#fbcfe8", "#ff66c4"], glow: "#ec4899" },
    blue: { bg: "#020308", shades: ["#3b82f6", "#60a5fa", "#93c5fd", "#2563eb", "#1d4ed8", "#67e8f9"], glow: "#3b82f6" },
    gold: { bg: "#050502", shades: ["#f59e0b", "#fbbf24", "#fcd34d", "#d97706", "#b45309", "#fde047"], glow: "#f59e0b" },
    purple: { bg: "#040206", shades: ["#a855f7", "#c084fc", "#e879f9", "#9333ea", "#7e22ce", "#d8b4fe"], glow: "#a855f7" },
    green: { bg: "#020503", shades: ["#10b981", "#34d399", "#6ee7b7", "#059669", "#047857", "#a7f3d0"], glow: "#10b981" },
    red: { bg: "#050202", shades: ["#ef4444", "#f87171", "#dc2626", "#b91c1c", "#fca5a5", "#fee2e2"], glow: "#ef4444" }
  };

  let currentThemeKey = "pink";
  let currentShapeKey = "bigHeart";
  let theme = THEMES[currentThemeKey];

  let targetCenterX = window.innerWidth / 2;
  let targetCenterY = window.innerHeight / 2;
  let currentCenterX = targetCenterX;
  let currentCenterY = targetCenterY;
  let isDragging = false;

  const canvas = document.getElementById("mainCanvas");
  const ctx = canvas.getContext("2d");

  let width = canvas.width = window.innerWidth;
  let height = canvas.height = window.innerHeight;

  window.addEventListener("resize", () => {
    width = canvas.width = window.innerWidth;
    height = canvas.height = window.innerHeight;
  });

  document.querySelectorAll('.color-btn').forEach(btn => {
    btn.addEventListener('click', (e) => {
      document.querySelectorAll('.color-btn').forEach(b => b.classList.remove('active'));
      e.target.classList.add('active');
      currentThemeKey = e.target.getAttribute('data-theme');
      theme = THEMES[currentThemeKey];
      document.body.style.backgroundColor = theme.bg;
      document.getElementById('metaThemeColor').setAttribute('content', theme.bg);
    });
  });

  document.querySelectorAll('#shapeSelector .btn').forEach(btn => {
    btn.addEventListener('click', (e) => {
      document.querySelectorAll('#shapeSelector .btn').forEach(b => b.classList.remove('active'));
      e.target.classList.add('active');
      currentShapeKey = e.target.getAttribute('data-shape');
      targetCenterX = width / 2;
      targetCenterY = height / 2;
    });
  });

  function getShapePoint(shape, i, total) {
    let scale = (shape === 'bigHeart') ? 14 : (shape === 'smallHeart') ? 8 : (shape === 'letterM') ? 7 : 12;
    
    if (shape === 'bigHeart' || shape === 'smallHeart') {
      const t = (i / total) * Math.PI * 2;
      const hx = 16 * Math.pow(Math.sin(t), 3);
      const hy = -(13 * Math.cos(t) - 5 * Math.cos(2 * t) - 2 * Math.cos(3 * t) - Math.cos(4 * t));
      return { x: hx * scale, y: hy * scale };
    } 
    else if (shape === 'letterM') {
      const pIndex = i / total;
      let mx = 0, my = 0;
      if (pIndex < 0.25) {
        const t = pIndex * 4;
        mx = -12;
        my = 12 - t * 24;
      } else if (pIndex < 0.5) {
        const t = (pIndex - 0.25) * 4;
        mx = -12 + t * 12;
        my = -12 + t * 18;
      } else if (pIndex < 0.75) {
        const t = (pIndex - 0.5) * 4;
        mx = t * 12;
        my = 6 - t * 18;
      } else {
        const t = (pIndex - 0.75) * 4;
        mx = 12;
        my = -12 + t * 24;
      }
      return { x: mx * scale * 0.9, y: my * scale * 0.9 };
    } 
    else if (shape === 'circle') {
      const angle = (i / total) * Math.PI * 2;
      return { x: Math.cos(angle) * scale * 9, y: Math.sin(angle) * scale * 9 };
    }
    return { x: 0, y: 0 };
  }

  class Particle {
    constructor(index, total) {
      this.index = index;
      this.total = total;
      this.init();
    }

    init() {
      this.color = theme.shades[(Math.random() * theme.shades.length) | 0];
      this.size = Math.random() * 2.2 + 1;
      this.updateTarget();
      this.x = this.targetX;
      this.y = this.targetY;
    }

    updateTarget() {
      const pt = getShapePoint(currentShapeKey, this.index, this.total);
      this.targetX = currentCenterX + pt.x + (Math.random() - 0.5) * 5;
      this.targetY = currentCenterY + pt.y + (Math.random() - 0.5) * 5;
    }

    update() {
      this.updateTarget();
      this.x += (this.targetX - this.x) * 0.12;
      this.y += (this.targetY - this.y) * 0.12;
    }

    draw() {
      ctx.fillStyle = this.color;
      ctx.beginPath();
      ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
      ctx.fill();
    }
  }

  class Spark {
    constructor(x, y) {
      this.x = x;
      this.y = y;
      this.color = theme.shades[(Math.random() * theme.shades.length) | 0];
      const angle = Math.random() * Math.PI * 2;
      const speed = Math.random() * 5 + 1.5;
      this.vx = Math.cos(angle) * speed;
      this.vy = Math.sin(angle) * speed;
      this.size = Math.random() * 3 + 1;
      this.maxLife = Math.random() * 25 + 15;
      this.life = this.maxLife;
    }

    update() {
      this.x += this.vx;
      this.y += this.vy;
      this.life--;
    }

    draw() {
      ctx.globalAlpha = Math.max(0, this.life / this.maxLife);
      ctx.fillStyle = this.color;
      ctx.beginPath();
      ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
      ctx.fill();
      ctx.globalAlpha = 1.0;
    }
  }

  class FloatingText {
    constructor(x, y) {
      this.x = x;
      this.y = y;
      this.alpha = 1.0;
      this.vy = -1.5;
      this.color = theme.shades[0];
    }
    update() {
      this.y += this.vy;
      this.alpha -= 0.03;
    }
    draw() {
      if (this.alpha <= 0) return;
      ctx.save();
      ctx.globalAlpha = Math.max(0, this.alpha);
      ctx.font = "bold 22px sans-serif";
      ctx.fillStyle = this.color;
      ctx.shadowColor = this.color;
      ctx.shadowBlur = 12;
      ctx.fillText("مینا ✨", this.x - 25, this.y);
      ctx.restore();
    }
  }

  const PARTICLE_COUNT = 250;
  const particles = [];
  const sparks = [];
  const floatingTexts = [];

  for (let i = 0; i < PARTICLE_COUNT; i++) {
    particles.push(new Particle(i, PARTICLE_COUNT));
  }

  let lastSoundTime = 0;
  function triggerAction(x, y) {
    const now = Date.now();
    if (soundReady && now - lastSoundTime > 300) {
      lastSoundTime = now;
      playMinaChime();
    }
    if (navigator.vibrate) navigator.vibrate(30);
    
    for (let i = 0; i < 15; i++) {
      sparks.push(new Spark(x, y));
    }
    floatingTexts.push(new FloatingText(x, y));
  }

  function handleStart(x, y) {
    isDragging = true;
    targetCenterX = x;
    targetCenterY = y;
    triggerAction(x, y);
  }

  function handleMove(x, y) {
    if (isDragging) {
      targetCenterX = x;
      targetCenterY = y;
    }
  }

  function handleEnd() {
    isDragging = false;
  }

  window.addEventListener("touchstart", (e) => {
    if (e.target.closest('.controls-container') || e.target.closest('#audioBanner')) return;
    e.preventDefault();
    handleStart(e.touches[0].clientX, e.touches[0].clientY);
  }, { passive: false });

  window.addEventListener("touchmove", (e) => {
    if (e.target.closest('.controls-container') || e.target.closest('#audioBanner')) return;
    e.preventDefault();
    handleMove(e.touches[0].clientX, e.touches[0].clientY);
  }, { passive: false });

  window.addEventListener("touchend", handleEnd);

  window.addEventListener("mousedown", (e) => {
    if (e.target.closest('.controls-container') || e.target.closest('#audioBanner')) return;
    handleStart(e.clientX, e.clientY);
  });

  window.addEventListener("mousemove", (e) => {
    if (isDragging) {
      handleMove(e.clientX, e.clientY);
    }
  });

  window.addEventListener("mouseup", handleEnd);

  function animate() {
    currentCenterX += (targetCenterX - currentCenterX) * 0.15;
    currentCenterY += (targetCenterY - currentCenterY) * 0.15;

    ctx.globalCompositeOperation = "source-over";
    ctx.fillStyle = theme.bg + "40";
    ctx.fillRect(0, 0, width, height);

    ctx.globalCompositeOperation = "lighter";

    for (let i = 0; i < particles.length; i++) {
      let p = particles[i];
      if (Math.random() < 0.03) {
        p.color = theme.shades[(Math.random() * theme.shades.length) | 0];
      }
      p.update();
      p.draw();
    }

    for (let i = sparks.length - 1; i >= 0; i--) {
      let s = sparks[i];
      s.update();
      s.draw();
      if (s.life <= 0) sparks.splice(i, 1);
    }

    for (let i = floatingTexts.length - 1; i >= 0; i--) {
      let ft = floatingTexts[i];
      ft.update();
      ft.draw();
      if (ft.alpha <= 0) floatingTexts.splice(i, 1);
    }

    requestAnimationFrame(animate);
  }

  animate();
</script>

</body>
</html>
