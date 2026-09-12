---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<div class="nature-cover">
  <canvas id="natureCanvas" class="nature-bg"></canvas>
  <canvas id="snowCanvas" class="snow-layer"></canvas>
  <div class="cover-overlay">

    <!-- 🚄 高铁运行动画 -->
    <div class="train-scene" aria-hidden="true">
      <div class="catenary"></div>
      <div class="train-track">
        <div class="sleepers"></div>
        <div class="rail rail-a"></div>
        <div class="rail rail-b"></div>
      </div>
      <div class="train-wrap">
        <div class="train" id="trainUnit">
          <div class="carriage tail"><span class="wheels"></span></div>
          <div class="carriage body"><span class="wheels"></span></div>
          <div class="carriage body">
            <span class="pantograph"></span>
            <span class="wheels"></span>
          </div>
          <div class="carriage head"><span class="wheels"></span></div>
        </div>
      </div>
    </div>

    <!-- 新站点卡片（仿论文摘要框 · 放大版） -->
    <div class="site-card">
      <div class="card-inner">
        <div class="card-label">▸ 永久访问地址 ◂</div>
        <div class="new-site-url" id="natureNewUrl">https://zuojie-li.github.io</div>
        <div class="button-group">
          <a href="https://zuojie-li.github.io" id="natureVisitBtn" class="primary-btn" target="_blank" rel="noopener noreferrer">访问新站点 →</a>
          <button id="natureEditBtn" class="edit-btn">永远相信 · 美好的事情即将发生</button>
        </div>
        <p class="footer-note"></p>
      </div>
    </div>

    <!-- 底部期刊信息栏 -->
    <div class="footer-bar">
      <span>Springer Publishers Limited 2026</span>
      <span>|</span>
      <span>图像: 动态共现网络 © Zuojie_Li</span>
    </div>
  </div>
</div>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .nature-cover {
    position: relative;
    width: 100%;
    min-height: 760px;
    background: #fefef7;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.1), 0 0 0 1px rgba(0, 0, 0, 0.05);
    margin: 32px 0;
    font-family: 'Helvetica Neue', 'Inter', 'Arial', system-ui, sans-serif;
  }
  .nature-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: block;
    pointer-events: auto;
    z-index: 1;
  }

  /* ❄️ 雪花层：覆盖在内容之上，但不拦截鼠标事件 */
  .snow-layer {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: block;
    pointer-events: none;
    z-index: 3;
  }

  .cover-overlay {
    position: relative;
    z-index: 2;
    width: 100%;
    min-height: 760px;
    background: rgba(254, 254, 247, 0.82);
    backdrop-filter: blur(2px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 3rem 2rem 4.5rem 2rem;
    pointer-events: none;
  }

  /* ---------- 🚄 高铁运行动画 ---------- */
  .train-scene {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 132px;
    overflow: hidden;
    pointer-events: none;
    z-index: 5;
    background: linear-gradient(180deg,
      rgba(206, 228, 244, 0.55) 0%,
      rgba(233, 243, 250, 0.26) 55%,
      rgba(254, 254, 247, 0) 100%);
    border-bottom: 1px solid rgba(198, 216, 229, 0.45);
  }

  /* 接触网（顶线） */
  .catenary {
    position: absolute;
    left: 0;
    right: 0;
    top: 30px;
    height: 2px;
    border-radius: 2px;
    background: linear-gradient(90deg,
      transparent 0%,
      rgba(96, 118, 134, 0.45) 6%,
      rgba(96, 118, 134, 0.45) 94%,
      transparent 100%);
  }

  /* 铁轨 */
  .train-track {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 26px;
    height: 14px;
  }
  .rail {
    position: absolute;
    left: 0;
    right: 0;
    height: 3px;
    border-radius: 2px;
    background: linear-gradient(180deg, #c3d0da, #8c9aa7);
    box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.6);
  }
  .rail-a { bottom: 8px; }  /* 远轨 */
  .rail-b { bottom: 1px; }  /* 近轨 */
  .sleepers {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 11px;
    border-radius: 1px;
    background: repeating-linear-gradient(
      90deg,
      rgba(176, 139, 106, 0.5) 0px,
      rgba(176, 139, 106, 0.5) 6px,
      transparent 6px,
      transparent 20px
    );
  }

  /* 火车容器（负责定位与移动端缩放） */
  .train-wrap {
    position: absolute;
    left: 0;
    bottom: 40px;
    transform-origin: left bottom;
  }

  /* 火车本体（负责横向行驶动画） */
  .train {
    display: flex;
    align-items: flex-end;
    will-change: transform;
    animation-name: trainRun;
    animation-duration: 12s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
    filter: drop-shadow(0 5px 7px rgba(31, 62, 84, 0.16));
  }

  @keyframes trainRun {
    0%   { transform: translateX(-580px); }
    100% { transform: translateX(var(--train-end-x, 1400px)); }
  }

  /* 车厢通用 */
  .carriage {
    position: relative;
    height: 46px;
    margin-right: 10px;
    background: linear-gradient(180deg, #ffffff 0%, #eaf2f8 46%, #c3d5e3 100%);
    border: 1px solid rgba(150, 172, 189, 0.75);
    box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.9);
  }
  .carriage:last-child { margin-right: 0; }

  /* 车窗带 */
  .carriage::before {
    content: '';
    position: absolute;
    top: 9px;
    left: 12px;
    right: 12px;
    height: 13px;
    border-radius: 4px;
    opacity: 0.88;
    background: repeating-linear-gradient(
      90deg,
      rgba(58, 96, 124, 0.9) 0px,
      rgba(58, 96, 124, 0.9) 15px,
      transparent 15px,
      transparent 23px
    );
  }

  /* 蓝色腰线 */
  .carriage::after {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    bottom: 9px;
    height: 5px;
    opacity: 0.9;
    background: linear-gradient(90deg, #2b6ba3, #4d95c9 50%, #2b6ba3);
  }

  .carriage.body {
    width: 130px;
    border-radius: 9px;
  }

  /* 车头（朝右，流线型） */
  .carriage.head {
    width: 132px;
    border-radius: 12px 92px 92px 12px / 12px 32px 32px 12px;
    background: linear-gradient(180deg, #ffffff 0%, #e4eef7 40%, #adc7dc 100%);
  }
  .carriage.head::before {
    left: auto;
    right: 15px;
    top: 11px;
    width: 24px;
    height: 17px;
    border-radius: 5px 14px 5px 5px;
    background: linear-gradient(150deg, #2c5573, #5a94b8);
    opacity: 0.92;
  }
  .carriage.head::after {
    border-radius: 0 40px 40px 0 / 0 14px 14px 0;
  }

  /* 车尾（朝左，流线型） */
  .carriage.tail {
    width: 118px;
    border-radius: 92px 12px 12px 92px / 32px 12px 12px 32px;
  }
  .carriage.tail::before {
    left: 34px;
    right: 12px;
  }
  .carriage.tail::after {
    border-radius: 40px 0 0 40px / 14px 0 0 14px;
  }

  /* 车轮 */
  .wheels {
    position: absolute;
    left: 0;
    right: 0;
    bottom: -5px;
    height: 10px;
  }
  .wheels::before,
  .wheels::after {
    content: '';
    position: absolute;
    bottom: 0;
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background: radial-gradient(circle at 34% 28%, #7a8996, #2b3944 78%);
  }
  .wheels::before { left: 16%; }
  .wheels::after  { right: 16%; }

  /* 受电弓 */
  .pantograph {
    position: absolute;
    top: -22px;
    left: 50%;
    margin-left: -14px;
    width: 28px;
    height: 22px;
    opacity: 0.8;
    background: linear-gradient(180deg, #93a4b1, #6d808f);
    clip-path: polygon(46% 0, 54% 0, 100% 100%, 0 100%);
  }

  /* ---------- 放大的地址卡片 ---------- */
  .site-card {
    width: 100%;
    max-width: 720px;
    background: rgba(255, 255, 250, 0.97);
    border-radius: 32px;
    box-shadow: 0 14px 38px rgba(0, 0, 0, 0.07), 0 0 0 1px #dce5ec;
    padding: 2.6rem 3rem;
    pointer-events: auto;
    transition: 0.2s;
  }
  .card-inner {
    text-align: center;
  }
  .card-label {
    font-size: 0.85rem;
    letter-spacing: 3px;
    font-weight: 600;
    color: #2c6e9e;
    margin-bottom: 20px;
  }
  .new-site-url {
    font-family: 'SF Mono', 'Fira Code', monospace;
    font-size: 1.35rem;
    background: #f2f6f9;
    padding: 1rem 1.4rem;
    border-radius: 44px;
    color: #145c8a;
    word-break: break-all;
    margin-bottom: 28px;
    border: 1px solid #e2e8f0;
    line-height: 1.5;
  }
  .button-group {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .primary-btn, .edit-btn {
    border: none;
    padding: 13px 34px;
    font-size: 1rem;
    font-weight: 600;
    border-radius: 40px;
    cursor: pointer;
    transition: 0.15s;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 6px;
  }
  .primary-btn {
    background: #1e3b4f;
    color: white;
    box-shadow: 0 3px 10px rgba(0,0,0,0.12);
  }
  .primary-btn:hover {
    background: #0f2c3c;
    transform: translateY(-2px);
  }
  .edit-btn {
    background: #edf2f7;
    color: #2d4a6e;
    border: 1px solid #cad2db;
  }
  .edit-btn:hover {
    background: #e2e8f0;
  }
  .footer-note {
    font-size: 0.75rem;
    color: #6b7b8c;
    margin-top: 26px;
    border-top: 1px solid #eef2f5;
    padding-top: 16px;
    font-style: italic;
  }

  /* ---------- 底部信息栏 ---------- */
  .footer-bar {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 1.3rem;
    display: flex;
    justify-content: center;
    gap: 1rem;
    font-size: 0.65rem;
    color: #5a6e7c;
    padding: 0 1rem;
    pointer-events: none;
  }

  @media (max-width: 620px) {
    .cover-overlay { padding: 2rem 1rem 3.6rem 1rem; min-height: 680px; }
    .site-card { padding: 1.8rem 1.3rem; border-radius: 24px; }
    .card-label { font-size: 0.72rem; letter-spacing: 2px; margin-bottom: 14px; }
    .new-site-url { font-size: 0.88rem; padding: 0.75rem 0.9rem; margin-bottom: 20px; border-radius: 28px; }
    .primary-btn, .edit-btn { padding: 10px 20px; font-size: 0.85rem; }
    .footer-bar { font-size: 0.55rem; gap: 0.6rem; }

    /* 移动端：缩小场景与列车 */
    .train-scene { height: 104px; }
    .catenary { top: 32px; }
    .train-wrap {
      bottom: 26px;
      transform: scale(0.66);
    }
    .train-track { bottom: 14px; }
    .rail-a { bottom: 8px; }
    .rail-b { bottom: 1px; }
  }
</style>

<script>
  (function() {
    // ---------- 粒子网络（背景）----------
    const canvas = document.getElementById('natureCanvas');
    if (!canvas) return;
    let ctx = canvas.getContext('2d');
    let width, height;
    let particles = [];
    let mouseX = null, mouseY = null;
    let animFrame;

    const PARTICLE_COUNT = 105;
    const CONNECTION_DIST = 135;
    const MOUSE_RADIUS = 110;
    const REPULSION = 0.5;

    let currentUrl = "https://zuojie-li.github.io";
    const urlSpan = document.getElementById('natureNewUrl');
    const visitBtn = document.getElementById('natureVisitBtn');
    const editBtn = document.getElementById('natureEditBtn');

    function updateUrlUI() {
      if (urlSpan) urlSpan.innerText = currentUrl;
      if (visitBtn) visitBtn.href = currentUrl;
    }
    if (editBtn) {
      editBtn.addEventListener('click', () => {
        let newLink = prompt('✏️ 编辑新站点链接 (包含 https://)', currentUrl);
        if (newLink && newLink.trim() !== "") {
          currentUrl = newLink.trim();
          updateUrlUI();
        }
      });
    }
    updateUrlUI();

    function initParticles() {
      particles = [];
      for (let i = 0; i < PARTICLE_COUNT; i++) {
        particles.push({
          x: Math.random() * width,
          y: Math.random() * height,
          vx: (Math.random() - 0.5) * 0.4,
          vy: (Math.random() - 0.5) * 0.4,
          radius: Math.random() * 2.6 + 1.0,
          color: `hsla(${195 + Math.random() * 30}, 55%, 62%, 0.7)`
        });
      }
    }

    function drawGrid() {
      ctx.save();
      ctx.strokeStyle = "#e2e8f0";
      ctx.lineWidth = 0.5;
      const step = 42;
      for (let x = step; x < width; x += step) {
        ctx.beginPath();
        ctx.moveTo(x, 0);
        ctx.lineTo(x, height);
        ctx.stroke();
      }
      for (let y = step; y < height; y += step) {
        ctx.beginPath();
        ctx.moveTo(0, y);
        ctx.lineTo(width, y);
        ctx.stroke();
      }
      ctx.fillStyle = "#cbdbe6";
      for (let x = step/2; x < width; x += step) {
        for (let y = step/2; y < height; y += step) {
          ctx.beginPath();
          ctx.arc(x, y, 1.2, 0, Math.PI*2);
          ctx.fill();
        }
      }
      ctx.restore();
    }

    function updateParticles() {
      for (let p of particles) {
        if (mouseX !== null && mouseY !== null) {
          let dx = p.x - mouseX;
          let dy = p.y - mouseY;
          let dist = Math.hypot(dx, dy);
          if (dist < MOUSE_RADIUS) {
            let force = (MOUSE_RADIUS - dist) / MOUSE_RADIUS;
            let angle = Math.atan2(dy, dx);
            p.vx += Math.cos(angle) * force * REPULSION * 0.45;
            p.vy += Math.sin(angle) * force * REPULSION * 0.45;
          }
        }
        p.vx *= 0.99;
        p.vy *= 0.99;
        p.x += p.vx;
        p.y += p.vy;
        const margin = 15;
        if (p.x < margin) { p.x = margin; p.vx *= -0.6; }
        if (p.x > width - margin) { p.x = width - margin; p.vx *= -0.6; }
        if (p.y < margin) { p.y = margin; p.vy *= -0.6; }
        if (p.y > height - margin) { p.y = height - margin; p.vy *= -0.6; }
      }
    }

    function drawConnections() {
      for (let i = 0; i < particles.length; i++) {
        for (let j = i+1; j < particles.length; j++) {
          const dx = particles[i].x - particles[j].x;
          const dy = particles[i].y - particles[j].y;
          const dist = Math.hypot(dx, dy);
          if (dist < CONNECTION_DIST) {
            let opacity = (1 - dist / CONNECTION_DIST) * 0.45;
            ctx.beginPath();
            ctx.moveTo(particles[i].x, particles[i].y);
            ctx.lineTo(particles[j].x, particles[j].y);
            ctx.strokeStyle = `rgba(76, 138, 174, ${opacity * 0.9})`;
            ctx.lineWidth = 0.9;
            ctx.stroke();
          }
        }
      }
    }

    function drawParticles() {
      for (let p of particles) {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.radius, 0, Math.PI*2);
        ctx.fillStyle = p.color || "#568db3";
        ctx.fill();
        ctx.shadowBlur = 3;
        ctx.shadowColor = "rgba(86, 141, 179, 0.3)";
        ctx.fill();
        ctx.shadowBlur = 0;
        ctx.beginPath();
        ctx.arc(p.x-0.8, p.y-0.8, p.radius*0.3, 0, Math.PI*2);
        ctx.fillStyle = "rgba(255, 255, 245, 0.9)";
        ctx.fill();
      }
    }

    function animate() {
      if (!ctx) return;
      ctx.clearRect(0, 0, width, height);
      ctx.fillStyle = "#fefef7";
      ctx.fillRect(0, 0, width, height);
      drawGrid();
      drawConnections();
      drawParticles();
      updateParticles();
      animFrame = requestAnimationFrame(animate);
    }

    function resizeCanvas() {
      const container = canvas.parentElement;
      width = container.clientWidth;
      height = container.clientHeight;
      canvas.width = width;
      canvas.height = height;
      initParticles();
    }

    function handleMouseMove(e) {
      const rect = canvas.getBoundingClientRect();
      const scaleX = canvas.width / rect.width;
      const scaleY = canvas.height / rect.height;
      let clientX, clientY;
      if (e.touches) {
        if (e.touches.length) {
          clientX = e.touches[0].clientX;
          clientY = e.touches[0].clientY;
        } else {
          mouseX = null;
          return;
        }
      } else {
        clientX = e.clientX;
        clientY = e.clientY;
      }
      if (clientX >= rect.left && clientX <= rect.right && clientY >= rect.top && clientY <= rect.bottom) {
        mouseX = (clientX - rect.left) * scaleX;
        mouseY = (clientY - rect.top) * scaleY;
      } else {
        mouseX = null;
      }
    }

    function handleLeave() {
      mouseX = null;
    }

    window.addEventListener('resize', () => { resizeCanvas(); });
    canvas.addEventListener('mousemove', handleMouseMove);
    canvas.addEventListener('mouseleave', handleLeave);
    canvas.addEventListener('touchmove', handleMouseMove);
    canvas.addEventListener('touchend', handleLeave);
    canvas.addEventListener('touchcancel', handleLeave);

    resizeCanvas();
    animate();
  })();

  // ---------- 🚄 高铁行程计算 ----------
  (function trainTravel() {
    const coverEl = document.querySelector('.nature-cover');
    const trainEl = document.getElementById('trainUnit');
    if (!coverEl || !trainEl) return;

    let timer = null;

    function layoutTrain() {
      const w = coverEl.clientWidth || 1200;
      const endX = w + 140;                 // 驶出右边界
      coverEl.style.setProperty('--train-end-x', endX + 'px');

      const total = endX + 580;             // 起点 -580px
      const speed = 175;                    // 每秒行驶像素（可调）
      trainEl.style.animationDuration = Math.max(7, total / speed) + 's';
    }

    layoutTrain();
    window.addEventListener('resize', () => {
      clearTimeout(timer);
      timer = setTimeout(layoutTrain, 180);
    });
  })();

  // ---------- ❄️ 飘雪动画 ----------
  (function snowFall() {
    const snowCanvas = document.getElementById('snowCanvas');
    if (!snowCanvas) return;
    const sctx = snowCanvas.getContext('2d');
    const DPR = Math.min(window.devicePixelRatio || 1, 2);

    const RADII = [2.0, 2.8, 3.8, 5.0, 6.6];
    const ROT_STEPS = 6;
    const spriteCache = new Map();

    let W = 0, H = 0;
    let flakes = [];
    let rafId = null;

    /* 预渲染雪花精灵，避免逐帧绘制 6 条臂的开销 */
    function makeSprite(r, rot) {
      const pad = r * 0.7;
      const size = (r + pad) * 2;
      const cv = document.createElement('canvas');
      cv.width = Math.ceil(size * DPR);
      cv.height = Math.ceil(size * DPR);
      const g = cv.getContext('2d');
      g.scale(DPR, DPR);
      g.translate(size / 2, size / 2);
      g.rotate(rot);
      g.strokeStyle = 'rgba(122, 172, 210, 0.95)';
      g.lineWidth = Math.max(0.55, r * 0.13);
      g.lineCap = 'round';
      g.lineJoin = 'round';
      for (let i = 0; i < 6; i++) {
        g.rotate(Math.PI / 3);
        g.beginPath();
        g.moveTo(0, 0);
        g.lineTo(0, -r);
        g.moveTo(0, -r * 0.5);
        g.lineTo(r * 0.30, -r * 0.78);
        g.moveTo(0, -r * 0.5);
        g.lineTo(-r * 0.30, -r * 0.78);
        g.moveTo(0, -r * 0.82);
        g.lineTo(r * 0.20, -r * 1.0);
        g.moveTo(0, -r * 0.82);
        g.lineTo(-r * 0.20, -r * 1.0);
        g.stroke();
      }
      return { canvas: cv, size: size };
    }

    function getSprite(ri, rotIdx) {
      const key = ri + '-' + rotIdx;
      let s = spriteCache.get(key);
      if (!s) {
        s = makeSprite(RADII[ri], rotIdx * (Math.PI / 3) / ROT_STEPS);
        spriteCache.set(key, s);
      }
      return s;
    }

    function resetFlake(f, initial) {
      const ri = Math.floor(Math.random() * RADII.length);
      f.ri = ri;
      f.r = RADII[ri];
      f.rotIdx = Math.floor(Math.random() * ROT_STEPS);
      f.x = Math.random() * W;
      f.y = initial ? Math.random() * H : -20 - Math.random() * 80;
      f.vy = 0.30 + (f.r / 6.6) * 0.95 + Math.random() * 0.55;
      f.vx = (Math.random() - 0.5) * 0.30;
      f.swayAmp = 10 + Math.random() * 26;
      f.swaySpeed = 0.006 + Math.random() * 0.016;
      f.phase = Math.random() * Math.PI * 2;
      f.alpha = 0.30 + Math.random() * 0.50;
      f.flicker = 0.5 + Math.random() * 1.6;
    }

    function createFlakes() {
      const count = Math.round(Math.min(150, Math.max(50, (W * H) / 11000)));
      flakes = [];
      for (let i = 0; i < count; i++) {
        const f = {};
        resetFlake(f, true);
        flakes.push(f);
      }
    }

    function resizeSnow() {
      const rect = snowCanvas.parentElement.getBoundingClientRect();
      W = Math.max(1, Math.round(rect.width));
      H = Math.max(1, Math.round(rect.height));
      snowCanvas.width = Math.ceil(W * DPR);
      snowCanvas.height = Math.ceil(H * DPR);
      sctx.setTransform(DPR, 0, 0, DPR, 0, 0);
      createFlakes();
    }

    let lastT = performance.now();

    function frame(now) {
      const dt = Math.min(3, (now - lastT) / 16.667);
      lastT = now;

      sctx.clearRect(0, 0, W, H);

      for (let i = 0; i < flakes.length; i++) {
        const f = flakes[i];

        f.phase += f.swaySpeed * dt;
        f.y += f.vy * dt;
        f.x += (f.vx + Math.sin(f.phase) * f.swayAmp * 0.02) * dt;

        if (f.y - f.r * 2 > H + 20) {
          resetFlake(f, false);
          continue;
        }
        if (f.x < -40) f.x = W + 40;
        else if (f.x > W + 40) f.x = -40;

        const sp = getSprite(f.ri, f.rotIdx);
        const a = f.alpha * (0.72 + 0.28 * Math.sin(now * 0.001 * f.flicker + f.phase));
        sctx.globalAlpha = Math.max(0.06, Math.min(1, a));
        sctx.drawImage(
          sp.canvas,
          f.x - sp.size / 2,
          f.y - sp.size / 2,
          sp.size,
          sp.size
        );
      }

      sctx.globalAlpha = 1;
      rafId = requestAnimationFrame(frame);
    }

    let resizeTimer = null;
    window.addEventListener('resize', () => {
      clearTimeout(resizeTimer);
      resizeTimer = setTimeout(resizeSnow, 150);
    });

    resizeSnow();
    rafId = requestAnimationFrame(frame);
  })();
</script>

