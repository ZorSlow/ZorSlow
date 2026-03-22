<h1 align="center">👋 Hi, I'm Boubacar Bah!</h1>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=ZorSlow&label=Profile%20views&color=0e75b6&style=flat" alt="ZorSlow" />
</p>

<p align="center">
  <b>💻 Junior Web Developer | Business Informatics Student</b><br>
  📍 Brussels, Belgium 🇧🇪
</p>

---

<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Boubacar Bah — Dev Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:ital,wght@0,300;0,400;1,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #080c14;
    --surface: #0d1420;
    --surface2: #111927;
    --border: rgba(99,202,255,0.12);
    --accent: #63caff;
    --accent2: #ff6b6b;
    --accent3: #a8ff78;
    --text: #e8f4ff;
    --muted: #6a8aaa;
    --glow: rgba(99,202,255,0.18);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Grid bg */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(99,202,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(99,202,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 780px;
    margin: 0 auto;
    padding: 60px 24px 80px;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    margin-bottom: 56px;
    animation: fadeUp 0.8s ease both;
  }

  .avatar-wrap {
    position: relative;
    display: inline-block;
    margin-bottom: 28px;
  }

  .avatar-ring {
    width: 110px; height: 110px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent2), var(--accent3));
    padding: 3px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    animation: spin 8s linear infinite;
  }

  .avatar-inner {
    width: 100%; height: 100%;
    border-radius: 50%;
    background: var(--bg);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 48px;
  }

  .status-dot {
    position: absolute;
    bottom: 6px; right: 6px;
    width: 18px; height: 18px;
    background: var(--accent3);
    border-radius: 50%;
    border: 3px solid var(--bg);
    animation: pulse 2s ease infinite;
  }

  h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem, 6vw, 3rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    line-height: 1.1;
    background: linear-gradient(135deg, #fff 30%, var(--accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 10px;
  }

  .role-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 100px;
    padding: 6px 18px;
    font-size: 0.78rem;
    color: var(--accent);
    letter-spacing: 0.08em;
    margin-bottom: 14px;
  }

  .role-badge::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--accent3);
    border-radius: 50%;
  }

  .location {
    font-size: 0.8rem;
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  .quote {
    margin-top: 22px;
    font-style: italic;
    font-size: 0.85rem;
    color: var(--muted);
    position: relative;
    display: inline-block;
  }

  .quote::before, .quote::after {
    content: '"';
    color: var(--accent);
    font-size: 1.4rem;
    line-height: 0;
    vertical-align: -0.4em;
  }

  /* ── SECTION ── */
  .section {
    margin-bottom: 40px;
    animation: fadeUp 0.8s ease both;
  }
  .section:nth-child(2) { animation-delay: 0.1s; }
  .section:nth-child(3) { animation-delay: 0.2s; }
  .section:nth-child(4) { animation-delay: 0.3s; }
  .section:nth-child(5) { animation-delay: 0.4s; }

  .section-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.65rem;
    font-weight: 600;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── SKILLS ── */
  .skills-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .skill-chip {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 8px 16px;
    font-size: 0.78rem;
    color: var(--text);
    letter-spacing: 0.04em;
    transition: all 0.2s ease;
    cursor: default;
    position: relative;
    overflow: hidden;
  }

  .skill-chip::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, var(--accent), transparent);
    opacity: 0;
    transition: opacity 0.2s;
  }

  .skill-chip:hover {
    border-color: var(--accent);
    color: #fff;
    box-shadow: 0 0 16px var(--glow);
    transform: translateY(-2px);
  }

  .skill-chip:hover::before { opacity: 0.08; }

  .skill-chip .icon { margin-right: 6px; }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 14px;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    transition: all 0.25s ease;
    position: relative;
    overflow: hidden;
  }

  .stat-card::after {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    background: linear-gradient(180deg, var(--accent), var(--accent2));
    opacity: 0;
    transition: opacity 0.25s;
  }

  .stat-card:hover {
    border-color: rgba(99,202,255,0.3);
    transform: translateY(-3px);
    box-shadow: 0 8px 32px rgba(0,0,0,0.4);
  }

  .stat-card:hover::after { opacity: 1; }

  .stat-value {
    font-family: 'Syne', sans-serif;
    font-size: 1.8rem;
    font-weight: 800;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 4px;
  }

  .stat-label {
    font-size: 0.72rem;
    color: var(--muted);
    letter-spacing: 0.06em;
  }

  /* ── CONNECT ── */
  .connect-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .connect-btn {
    display: flex;
    align-items: center;
    gap: 10px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 12px 20px;
    text-decoration: none;
    color: var(--text);
    font-size: 0.82rem;
    font-family: 'DM Mono', monospace;
    letter-spacing: 0.04em;
    transition: all 0.25s ease;
    flex: 1;
    min-width: 180px;
    justify-content: center;
  }

  .connect-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 24px rgba(0,0,0,0.4);
  }

  .connect-btn.linkedin:hover { border-color: #0077b5; box-shadow: 0 6px 24px rgba(0,119,181,0.3); }
  .connect-btn.portfolio:hover { border-color: var(--accent3); box-shadow: 0 6px 24px rgba(168,255,120,0.2); }
  .connect-btn.email:hover { border-color: var(--accent2); box-shadow: 0 6px 24px rgba(255,107,107,0.3); }

  .btn-icon { font-size: 1.1rem; }

  /* ── TERMINAL BLOCK ── */
  .terminal {
    background: #06090f;
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }

  .terminal-bar {
    background: var(--surface2);
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 6px;
    border-bottom: 1px solid var(--border);
  }

  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot.r { background: #ff5f57; }
  .dot.y { background: #ffbd2e; }
  .dot.g { background: #28c840; }

  .terminal-title {
    margin-left: 8px;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 0.08em;
  }

  .terminal-body {
    padding: 20px 24px;
    font-size: 0.82rem;
    line-height: 2;
  }

  .line { display: block; }
  .prompt { color: var(--accent3); }
  .cmd { color: var(--text); }
  .out { color: var(--muted); }
  .hi { color: var(--accent); }
  .hi2 { color: var(--accent2); }
  .hi3 { color: var(--accent3); }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes spin {
    to { transform: rotate(360deg); }
  }

  @keyframes pulse {
    0%, 100% { box-shadow: 0 0 0 0 rgba(168,255,120,0.4); }
    50% { box-shadow: 0 0 0 6px rgba(168,255,120,0); }
  }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    margin-top: 56px;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 0.08em;
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="avatar-wrap">
      <div class="avatar-ring">
        <div class="avatar-inner">👨🏾‍💻</div>
      </div>
      <div class="status-dot"></div>
    </div>
    <h1>Boubacar Bah</h1>
    <div class="role-badge">Junior Web Developer · Business Informatics</div>
    <div class="location">📍 Brussels, Belgium 🇧🇪</div>
    <div class="quote">Curious, Motivated, Rigorous and Determined</div>
  </div>

  <!-- TERMINAL -->
  <div class="section">
    <div class="section-label">whoami</div>
    <div class="terminal">
      <div class="terminal-bar">
        <div class="dot r"></div>
        <div class="dot y"></div>
        <div class="dot g"></div>
        <span class="terminal-title">boubacar@dev ~ profile.sh</span>
      </div>
      <div class="terminal-body">
        <span class="line"><span class="prompt">$ </span><span class="cmd">cat profile.json</span></span>
        <span class="line"><span class="out">{</span></span>
        <span class="line"><span class="out">&nbsp;&nbsp;"name":</span> <span class="hi">"Boubacar Bah"</span><span class="out">,</span></span>
        <span class="line"><span class="out">&nbsp;&nbsp;"role":</span> <span class="hi">"Junior Web Developer"</span><span class="out">,</span></span>
        <span class="line"><span class="out">&nbsp;&nbsp;"studies":</span> <span class="hi2">"Business Informatics"</span><span class="out">,</span></span>
        <span class="line"><span class="out">&nbsp;&nbsp;"location":</span> <span class="hi3">"Brussels 🇧🇪"</span><span class="out">,</span></span>
        <span class="line"><span class="out">&nbsp;&nbsp;"open_to_work":</span> <span class="hi3">true</span><span class="out">,</span></span>
        <span class="line"><span class="out">&nbsp;&nbsp;"passion":</span> <span class="hi">"Building clean, impactful web experiences"</span></span>
        <span class="line"><span class="out">}</span></span>
        <span class="line"><span class="prompt">$ </span><span class="cmd">_</span></span>
      </div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section">
    <div class="section-label">Stack & Outils</div>
    <div class="skills-grid">
      <div class="skill-chip"><span class="icon">🌐</span> HTML5</div>
      <div class="skill-chip"><span class="icon">🎨</span> CSS3</div>
      <div class="skill-chip"><span class="icon">⚡</span> JavaScript</div>
      <div class="skill-chip"><span class="icon">🐍</span> Python</div>
      <div class="skill-chip"><span class="icon">🗄️</span> MySQL</div>
      <div class="skill-chip"><span class="icon">🔀</span> Git</div>
      <div class="skill-chip"><span class="icon">🐧</span> Linux</div>
      <div class="skill-chip"><span class="icon">💻</span> VS Code</div>
    </div>
  </div>

  <!-- STATS -->
  <div class="section">
    <div class="section-label">GitHub Activity</div>
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-value">∞</div>
        <div class="stat-label">curiosité &amp; envie d'apprendre</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">100%</div>
        <div class="stat-label">open to work</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">2+</div>
        <div class="stat-label">langages maîtrisés</div>
      </div>
      <div class="stat-card">
        <div class="stat-value">🔥</div>
        <div class="stat-label">streak en cours</div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-label">Me contacter</div>
    <div class="connect-grid">
      <a href="https://www.linkedin.com/in/boubacar-bah-dev" target="_blank" class="connect-btn linkedin">
        <span class="btn-icon">💼</span> LinkedIn
      </a>
      <a href="https://zorslow.github.io/portfolio/" target="_blank" class="connect-btn portfolio">
        <span class="btn-icon">🌍</span> Portfolio
      </a>
      <a href="mailto:Boubacar_Bah@outlook.be" class="connect-btn email">
        <span class="btn-icon">✉️</span> Email
      </a>
    </div>
  </div>

  <div class="footer">
    Made with ❤️ by Boubacar · Brussels © 2025
  </div>

</div>
</body>
</html>

<p align="center">
  <i>"Learning, practicing, and building."</i>
</p>
