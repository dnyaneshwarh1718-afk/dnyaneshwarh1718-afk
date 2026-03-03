<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dnyaneshwar – GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;700;800;900&family=IBM+Plex+Mono:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #070a0f;
    --surface: #0d1117;
    --surface2: #161b22;
    --border: #21262d;
    --accent: #00ff88;
    --accent2: #7c3aed;
    --accent3: #f59e0b;
    --text: #e6edf3;
    --muted: #8b949e;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'IBM Plex Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background-image: 
      linear-gradient(rgba(0,255,136,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,255,136,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
    z-index: 0;
  }
  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 60px 24px;
    position: relative;
    z-index: 1;
  }
  .header {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 40px;
    align-items: center;
    margin-bottom: 60px;
    animation: fadeUp 0.8s ease both;
  }
  .status-tag {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(0,255,136,0.08);
    border: 1px solid rgba(0,255,136,0.25);
    border-radius: 2px;
    padding: 4px 12px;
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 20px;
  }
  .status-dot {
    width: 6px; height: 6px;
    background: var(--accent);
    border-radius: 50%;
    animation: pulse 2s ease infinite;
  }
  @keyframes pulse {
    0%,100%{opacity:1;transform:scale(1)}
    50%{opacity:0.5;transform:scale(1.5)}
  }
  h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(42px,7vw,72px);
    font-weight: 900;
    line-height: 0.95;
    letter-spacing: -2px;
    margin-bottom: 8px;
  }
  h1 .name-line1 { display: block; color: var(--text); }
  h1 .name-line2 {
    display: block;
    color: transparent;
    -webkit-text-stroke: 1px var(--accent);
    font-size: clamp(36px,6vw,62px);
  }
  .tagline {
    color: var(--muted);
    font-size: 13px;
    margin-top: 16px;
    line-height: 1.6;
    max-width: 380px;
  }
  .tagline span { color: var(--accent); }
  .avatar-wrap {
    position: relative;
    width: 140px; height: 140px;
    flex-shrink: 0;
  }
  .avatar-ring {
    position: absolute;
    inset: -8px;
    border-radius: 50%;
    border: 2px solid transparent;
    background: conic-gradient(var(--accent), var(--accent2), var(--accent3), var(--accent)) border-box;
    -webkit-mask: linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0);
    -webkit-mask-composite: destination-out;
    mask-composite: exclude;
    animation: spin 8s linear infinite;
  }
  @keyframes spin { to { transform: rotate(360deg); } }
  .avatar-inner {
    width: 140px; height: 140px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent2), #0d1117);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 48px;
    font-weight: 900;
    color: var(--accent);
  }
  .section { margin-bottom: 48px; animation: fadeUp 0.8s ease both; }
  .section:nth-child(2){animation-delay:.1s}
  .section:nth-child(3){animation-delay:.2s}
  .section:nth-child(4){animation-delay:.3s}
  .section:nth-child(5){animation-delay:.4s}
  .section:nth-child(6){animation-delay:.5s}
  @keyframes fadeUp {
    from{opacity:0;transform:translateY(24px)}
    to{opacity:1;transform:translateY(0)}
  }
  .section-label {
    font-size: 10px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
  .about-item {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 16px 20px;
    display: flex;
    align-items: flex-start;
    gap: 12px;
    transition: border-color 0.2s, transform 0.2s;
    cursor: default;
  }
  .about-item:hover { border-color: var(--accent); transform: translateY(-2px); }
  .about-icon { font-size: 18px; flex-shrink: 0; margin-top: 2px; }
  .about-text { font-size: 12px; color: var(--muted); line-height: 1.5; }
  .about-text strong { color: var(--text); font-weight: 400; }
  .socials { display: flex; flex-wrap: wrap; gap: 10px; }
  .social-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 18px;
    border: 1px solid var(--border);
    border-radius: 2px;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    text-decoration: none;
    transition: all 0.2s;
    background: var(--surface2);
    letter-spacing: 1px;
  }
  .social-btn:hover {
    color: var(--text);
    border-color: var(--accent);
    background: rgba(0,255,136,0.05);
    transform: translateY(-2px);
  }
  .social-btn svg { width: 14px; height: 14px; }
  .stack-grid { display: flex; flex-wrap: wrap; gap: 8px; }
  .tech-pill {
    padding: 6px 14px;
    border-radius: 2px;
    font-size: 10px;
    font-family: 'Space Mono', monospace;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    font-weight: 700;
    border: 1px solid;
    transition: all 0.2s;
    cursor: default;
  }
  .tech-pill:hover { transform: translateY(-3px) scale(1.05); }
  .pill-green  { color:#00ff88;border-color:rgba(0,255,136,.3);background:rgba(0,255,136,.07) }
  .pill-purple { color:#a78bfa;border-color:rgba(167,139,250,.3);background:rgba(167,139,250,.07) }
  .pill-amber  { color:#fbbf24;border-color:rgba(251,191,36,.3);background:rgba(251,191,36,.07) }
  .pill-blue   { color:#60a5fa;border-color:rgba(96,165,250,.3);background:rgba(96,165,250,.07) }
  .pill-pink   { color:#f472b6;border-color:rgba(244,114,182,.3);background:rgba(244,114,182,.07) }
  .pill-cyan   { color:#22d3ee;border-color:rgba(34,211,238,.3);background:rgba(34,211,238,.07) }
  .pill-red    { color:#fb7185;border-color:rgba(251,113,133,.3);background:rgba(251,113,133,.07) }
  .pill-orange { color:#fb923c;border-color:rgba(251,146,60,.3);background:rgba(251,146,60,.07) }
  .stats-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 16px; }
  .stat-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 28px 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s;
  }
  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg,transparent,var(--ca),transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }
  .stat-card:hover::before { opacity: 1; }
  .stat-card:nth-child(1){--ca:var(--accent)}
  .stat-card:nth-child(2){--ca:var(--accent2)}
  .stat-card:nth-child(3){--ca:var(--accent3)}
  .stat-card:nth-child(1):hover{border-color:var(--accent)}
  .stat-card:nth-child(2):hover{border-color:var(--accent2)}
  .stat-card:nth-child(3):hover{border-color:var(--accent3)}
  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 44px;
    font-weight: 900;
    line-height: 1;
    margin-bottom: 8px;
    display: block;
  }
  .stat-card:nth-child(1) .stat-num{color:var(--accent)}
  .stat-card:nth-child(2) .stat-num{color:#a78bfa}
  .stat-card:nth-child(3) .stat-num{color:var(--accent3)}
  .stat-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); }
  .stat-sub { font-size: 10px; color: var(--muted); margin-top: 6px; opacity: 0.6; }
  .contact-bar {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 20px 24px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 16px;
  }
  .contact-text { font-size: 12px; color: var(--muted); }
  .contact-email {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: var(--accent);
    text-decoration: none;
    border-bottom: 1px solid rgba(0,255,136,0.3);
    padding-bottom: 2px;
    transition: border-color 0.2s;
  }
  .contact-email:hover { border-color: var(--accent); }
  .footer {
    margin-top: 60px;
    padding-top: 24px;
    border-top: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 1px;
  }
  .footer-brand { font-family: 'Syne', sans-serif; font-weight: 800; color: var(--accent); font-size: 13px; }
  @media (max-width: 600px) {
    .header{grid-template-columns:1fr}
    .avatar-wrap{display:none}
    .about-grid{grid-template-columns:1fr}
    .stats-grid{grid-template-columns:1fr}
  }
</style>
</head>
<body>
<div class="container">

  <header class="header">
    <div class="header-left">
      <div class="status-tag">
        <span class="status-dot"></span>
        Available for collaboration
      </div>
      <h1>
        <span class="name-line1">Dnyaneshwar</span>
        <span class="name-line2">Hogade</span>
      </h1>
      <p class="tagline">
        Building at the intersection of <span>AI</span> &amp; full-stack engineering.
        Learning. Shipping. Iterating.
      </p>
    </div>
    <div class="avatar-wrap">
      <div class="avatar-ring"></div>
      <div class="avatar-inner">DH</div>
    </div>
  </header>

  <section class="section">
    <div class="section-label">// about</div>
    <div class="about-grid">
      <div class="about-item">
        <span class="about-icon">🚀</span>
        <div class="about-text"><strong>Currently learning</strong> Data Science and web development with a focus on real-world projects.</div>
      </div>
      <div class="about-item">
        <span class="about-icon">⚙️</span>
        <div class="about-text"><strong>Working on</strong> AI-powered projects and production-level ML pipelines.</div>
      </div>
      <div class="about-item">
        <span class="about-icon">🧠</span>
        <div class="about-text"><strong>Interested in</strong> full-stack development with integrated ML models end-to-end.</div>
      </div>
      <div class="about-item">
        <span class="about-icon">🏋️</span>
        <div class="about-text"><strong>Off-screen</strong> into warhammer painting and lifting weights. Balance is everything.</div>
      </div>
    </div>
  </section>

  <section class="section">
    <div class="section-label">// connect</div>
    <div class="socials">
      <a href="https://github.com/dnyaneshwarh1718-afk" class="social-btn" target="_blank">
        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"/></svg>
        GitHub
      </a>
      <a href="#" class="social-btn">
        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="#" class="social-btn">
        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
        X / Twitter
      </a>
      <a href="#" class="social-btn">
        <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
        Portfolio
      </a>
    </div>
  </section>

  <section class="section">
    <div class="section-label">// tech stack</div>
    <div class="stack-grid">
      <span class="tech-pill pill-green">Python</span>
      <span class="tech-pill pill-blue">C++</span>
      <span class="tech-pill pill-amber">LaTeX</span>
      <span class="tech-pill pill-orange">HTML5</span>
      <span class="tech-pill pill-purple">Django</span>
      <span class="tech-pill pill-cyan">FastAPI</span>
      <span class="tech-pill pill-red">Flask</span>
      <span class="tech-pill pill-amber">TensorFlow</span>
      <span class="tech-pill pill-orange">PyTorch</span>
      <span class="tech-pill pill-pink">Keras</span>
      <span class="tech-pill pill-green">Scikit-Learn</span>
      <span class="tech-pill pill-blue">Pandas</span>
      <span class="tech-pill pill-purple">NumPy</span>
      <span class="tech-pill pill-cyan">Matplotlib</span>
      <span class="tech-pill pill-amber">SciPy</span>
      <span class="tech-pill pill-green">OpenCV</span>
      <span class="tech-pill pill-blue">PostgreSQL</span>
      <span class="tech-pill pill-orange">MySQL</span>
      <span class="tech-pill pill-cyan">SQLite</span>
      <span class="tech-pill pill-red">Docker</span>
      <span class="tech-pill pill-purple">Git</span>
      <span class="tech-pill pill-amber">GitHub Actions</span>
      <span class="tech-pill pill-pink">Heroku</span>
      <span class="tech-pill pill-green">Postman</span>
      <span class="tech-pill pill-blue">Twilio</span>
      <span class="tech-pill pill-orange">Anaconda</span>
    </div>
  </section>

  <section class="section">
    <div class="section-label">// github stats</div>
    <div class="stats-grid">
      <div class="stat-card">
        <span class="stat-num" id="contributions">0</span>
        <div class="stat-label">Total Contributions</div>
        <div class="stat-sub">Sep 2021 – Present</div>
      </div>
      <div class="stat-card">
        <span class="stat-num" id="streak">0</span>
        <div class="stat-label">Current Streak</div>
        <div class="stat-sub">Keep going 🔥</div>
      </div>
      <div class="stat-card">
        <span class="stat-num" id="best">0</span>
        <div class="stat-label">Longest Streak</div>
        <div class="stat-sub">Mar 17 – Mar 22, 2024</div>
      </div>
    </div>
  </section>

  <section class="section">
    <div class="section-label">// contact</div>
    <div class="contact-bar">
      <div class="contact-text">Got an interesting project or idea? Let's build it.</div>
      <a href="mailto:dnyaneshwar@example.com" class="contact-email">dnyaneshwar@example.com</a>
    </div>
  </section>

  <footer class="footer">
    <span class="footer-brand">dnyaneshwarh1718-afk</span>
    <span>README.md · Made with 🖤</span>
  </footer>

</div>
<script>
  function animateCount(el, target, duration) {
    duration = duration || 1500;
    var start = performance.now();
    function update(now) {
      var progress = Math.min((now - start) / duration, 1);
      var eased = 1 - Math.pow(1 - progress, 3);
      el.textContent = Math.round(eased * target);
      if (progress < 1) requestAnimationFrame(update);
    }
    requestAnimationFrame(update);
  }
  var observer = new IntersectionObserver(function(entries) {
    entries.forEach(function(e) {
      if (e.isIntersecting) {
        animateCount(document.getElementById('contributions'), 417);
        animateCount(document.getElementById('streak'), 0, 300);
        animateCount(document.getElementById('best'), 6);
        observer.disconnect();
      }
    });
  }, { threshold: 0.3 });
  observer.observe(document.querySelector('.stats-grid'));
</script>
</body>
</html>
