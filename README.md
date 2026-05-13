<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Hamza — GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Syne:wght@400;600;800&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d0f14;
    --surface: #13161d;
    --surface2: #1a1e28;
    --border: rgba(255,255,255,0.07);
    --border2: rgba(255,255,255,0.13);
    --accent: #7ee8a2;
    --accent2: #4fc3f7;
    --accent3: #f77f6e;
    --accent4: #c084fc;
    --text: #e8ecf3;
    --muted: #8892a4;
    --faint: #4a5568;
    --mono: 'JetBrains Mono', monospace;
    --sans: 'Syne', sans-serif;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--mono);
    min-height: 100vh;
    padding: 48px 24px 80px;
    line-height: 1.6;
  }

  .page {
    max-width: 860px;
    margin: 0 auto;
  }

  /* ── HEADER ── */
  .hero {
    text-align: center;
    padding: 64px 0 48px;
    position: relative;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: 0; left: 50%; transform: translateX(-50%);
    width: 600px; height: 300px;
    background: radial-gradient(ellipse at 50% 0%, rgba(126,232,162,0.08) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-tag {
    display: inline-block;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--accent);
    border: 1px solid rgba(126,232,162,0.25);
    padding: 5px 14px;
    border-radius: 100px;
    margin-bottom: 24px;
    animation: fadeUp 0.6s ease both;
  }

  .hero-name {
    font-family: var(--sans);
    font-size: clamp(48px, 7vw, 88px);
    font-weight: 800;
    letter-spacing: -2px;
    line-height: 0.95;
    margin-bottom: 20px;
    animation: fadeUp 0.6s 0.1s ease both;
  }

  .hero-name span {
    background: linear-gradient(135deg, var(--accent) 0%, var(--accent2) 60%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-sub {
    font-size: 14px;
    color: var(--muted);
    max-width: 520px;
    margin: 0 auto 36px;
    animation: fadeUp 0.6s 0.2s ease both;
  }

  .hero-badges {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    animation: fadeUp 0.6s 0.3s ease both;
  }

  .badge {
    font-size: 12px;
    padding: 6px 14px;
    border-radius: 6px;
    border: 1px solid var(--border2);
    background: var(--surface);
    color: var(--muted);
    white-space: nowrap;
  }

  .badge .dot {
    display: inline-block;
    width: 6px; height: 6px;
    border-radius: 50%;
    margin-right: 6px;
    vertical-align: middle;
    position: relative; top: -1px;
  }

  .dot-green { background: var(--accent); box-shadow: 0 0 6px var(--accent); }
  .dot-blue  { background: var(--accent2); }
  .dot-red   { background: var(--accent3); }
  .dot-purple{ background: var(--accent4); }

  /* ── DIVIDER ── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border2), transparent);
    margin: 48px 0;
  }

  /* ── SECTION LABEL ── */
  .section-label {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--faint);
    margin-bottom: 20px;
  }

  .section-label span {
    color: var(--accent);
    margin-right: 8px;
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 48px;
  }

  .about-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 18px 20px;
    transition: border-color 0.2s, background 0.2s;
  }

  .about-card:hover {
    border-color: var(--border2);
    background: var(--surface2);
  }

  .about-card .icon {
    font-size: 20px;
    margin-bottom: 10px;
  }

  .about-card .label {
    font-size: 11px;
    color: var(--faint);
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 4px;
  }

  .about-card .value {
    font-size: 13px;
    color: var(--text);
    line-height: 1.5;
  }

  .about-card .value a {
    color: var(--accent2);
    text-decoration: none;
  }

  /* ── PROJECTS ── */
  .projects { margin-bottom: 48px; }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 22px 24px;
    margin-bottom: 12px;
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: start;
    gap: 16px;
    transition: border-color 0.2s, transform 0.2s;
    text-decoration: none;
    color: inherit;
    display: block;
  }

  .project-card:hover {
    border-color: rgba(126,232,162,0.3);
    transform: translateX(4px);
  }

  .project-inner {
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: center;
    gap: 16px;
  }

  .project-name {
    font-family: var(--sans);
    font-size: 16px;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 6px;
  }

  .project-desc {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.6;
  }

  .project-tags {
    display: flex;
    gap: 6px;
    margin-top: 12px;
    flex-wrap: wrap;
  }

  .tag {
    font-size: 10px;
    padding: 3px 9px;
    border-radius: 4px;
    border: 1px solid var(--border2);
    color: var(--faint);
    letter-spacing: 0.5px;
  }

  .tag.green { border-color: rgba(126,232,162,0.2); color: var(--accent); }
  .tag.blue  { border-color: rgba(79,195,247,0.2); color: var(--accent2); }
  .tag.red   { border-color: rgba(247,127,110,0.2); color: var(--accent3); }
  .tag.purple{ border-color: rgba(192,132,252,0.2); color: var(--accent4); }

  .arrow {
    color: var(--faint);
    font-size: 18px;
    transition: color 0.2s, transform 0.2s;
  }

  .project-card:hover .arrow {
    color: var(--accent);
    transform: translate(2px, -2px);
  }

  /* ── TECH STACK ── */
  .stack { margin-bottom: 48px; }

  .stack-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
    gap: 8px;
  }

  .tech-pill {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 10px 12px;
    text-align: center;
    font-size: 12px;
    color: var(--muted);
    transition: all 0.2s;
  }

  .tech-pill:hover {
    border-color: var(--border2);
    color: var(--text);
    background: var(--surface2);
  }

  .tech-pill .t-icon {
    font-size: 16px;
    display: block;
    margin-bottom: 5px;
  }

  /* ── CONNECT ── */
  .connect { margin-bottom: 48px; }

  .connect-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 10px;
  }

  .connect-link {
    display: flex;
    align-items: center;
    gap: 12px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 16px;
    text-decoration: none;
    color: var(--muted);
    font-size: 13px;
    transition: all 0.2s;
  }

  .connect-link:hover {
    background: var(--surface2);
    border-color: var(--border2);
    color: var(--text);
  }

  .c-icon {
    width: 36px; height: 36px;
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 16px;
    flex-shrink: 0;
  }

  .c-linkedin { background: rgba(10,102,194,0.15); color: #4fc3f7; }
  .c-gmail    { background: rgba(234,67,53,0.15);  color: #f77f6e; }
  .c-insta    { background: rgba(192,132,252,0.15); color: var(--accent4); }
  .c-github   { background: rgba(126,232,162,0.12); color: var(--accent); }

  .connect-name { font-size: 13px; }
  .connect-handle { font-size: 11px; color: var(--faint); }

  /* ── GITHUB STATS ── */
  .stats { margin-bottom: 48px; }

  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .stats-img-wrap {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    padding: 4px;
  }

  .stats-img-wrap img {
    width: 100%;
    border-radius: 8px;
    display: block;
  }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    font-size: 12px;
    color: var(--faint);
    padding-top: 40px;
    border-top: 1px solid var(--border);
  }

  .footer .cursor {
    display: inline-block;
    width: 8px; height: 14px;
    background: var(--accent);
    margin-left: 4px;
    vertical-align: middle;
    animation: blink 1s step-end infinite;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0; }
  }

  /* ── COPY BUTTON ── */
  .copy-btn {
    display: block;
    width: fit-content;
    margin: 0 auto 40px;
    background: transparent;
    border: 1px solid var(--border2);
    color: var(--muted);
    font-family: var(--mono);
    font-size: 12px;
    padding: 8px 20px;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.2s;
    letter-spacing: 1px;
  }

  .copy-btn:hover {
    border-color: var(--accent);
    color: var(--accent);
  }

  /* responsive */
  @media (max-width: 560px) {
    .about-grid  { grid-template-columns: 1fr; }
    .stats-grid  { grid-template-columns: 1fr; }
    .hero-name   { font-size: 52px; }
  }
</style>
</head>
<body>

<div class="page">

  <!-- HERO -->
  <header class="hero">
    <div class="hero-tag">👋 available for collaboration</div>
    <h1 class="hero-name">Hi, I'm <span>Hamza</span></h1>
    <p class="hero-sub">Software engineer obsessed with scalable systems, warehouse optimization, and the kind of backend architecture that actually holds up under pressure.</p>
    <div class="hero-badges">
      <span class="badge"><span class="dot dot-green"></span>Open to work</span>
      <span class="badge"><span class="dot dot-blue"></span>Node.js · TypeScript</span>
      <span class="badge"><span class="dot dot-red"></span>Istanbul 🇹🇷</span>
      <span class="badge"><span class="dot dot-purple"></span>Building in public</span>
    </div>
  </header>

  <div class="divider"></div>

  <!-- ABOUT -->
  <section>
    <div class="section-label"><span>//</span> about</div>
    <div class="about-grid">
      <div class="about-card">
        <div class="icon">🔭</div>
        <div class="label">currently building</div>
        <div class="value">Centralized Rate-Limiting Middleware for Distributed Systems</div>
      </div>
      <div class="about-card">
        <div class="icon">🌱</div>
        <div class="label">diving deep into</div>
        <div class="value">Next.js · RxJS · Kubernetes Sidecar Patterns</div>
      </div>
      <div class="about-card">
        <div class="icon">💬</div>
        <div class="label">ask me about</div>
        <div class="value">Warehouse optimization, scalable backends, architectural design</div>
      </div>
      <div class="about-card">
        <div class="icon">📫</div>
        <div class="label">reach me at</div>
        <div class="value"><a href="mailto:hamzamalfawaer@email.com">hamzamalfawaer@email.com</a></div>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- PROJECTS -->
  <section class="projects">
    <div class="section-label"><span>//</span> projects</div>

    <a class="project-card" href="https://github.com/hamzamalfawaer/rate-limiter" target="_blank">
      <div class="project-inner">
        <div>
          <div class="project-name">RateLimiter Service</div>
          <div class="project-desc">Centralized rate-limiter with weight-based logic and custom middleware — built for distributed environments.</div>
          <div class="project-tags">
            <span class="tag green">Node.js</span>
            <span class="tag red">Express</span>
            <span class="tag blue">Redis</span>
            <span class="tag">Kubernetes</span>
          </div>
        </div>
        <div class="arrow">↗</div>
      </div>
    </a>

    <a class="project-card" href="https://github.com/hamzamalfawaer/reactive-pipeline-ide" target="_blank">
      <div class="project-inner">
        <div>
          <div class="project-name">Reactive Pipeline IDE</div>
          <div class="project-desc">Visual interface for composing reactive workflows using RxJS — drag, connect, observe.</div>
          <div class="project-tags">
            <span class="tag blue">Next.js</span>
            <span class="tag purple">RxJS</span>
            <span class="tag">Tailwind</span>
          </div>
        </div>
        <div class="arrow">↗</div>
      </div>
    </a>

    <a class="project-card" href="https://github.com/hamzamalfawaer/warehouse-audit" target="_blank">
      <div class="project-inner">
        <div>
          <div class="project-name">Warehouse Audit Tool</div>
          <div class="project-desc">CLI + web tool to assess and visualize warehouse performance metrics end-to-end.</div>
          <div class="project-tags">
            <span class="tag green">Python</span>
            <span class="tag red">Flask</span>
            <span class="tag blue">D3.js</span>
          </div>
        </div>
        <div class="arrow">↗</div>
      </div>
    </a>
  </section>

  <div class="divider"></div>

  <!-- TECH STACK -->
  <section class="stack">
    <div class="section-label"><span>//</span> tech stack</div>
    <div class="stack-grid">
      <div class="tech-pill"><span class="t-icon">⬡</span>Node.js</div>
      <div class="tech-pill"><span class="t-icon">𝕋</span>TypeScript</div>
      <div class="tech-pill"><span class="t-icon">▲</span>Next.js</div>
      <div class="tech-pill"><span class="t-icon">⚛</span>React</div>
      <div class="tech-pill"><span class="t-icon">🐳</span>Docker</div>
      <div class="tech-pill"><span class="t-icon">☸</span>K8s</div>
      <div class="tech-pill"><span class="t-icon">🐘</span>PostgreSQL</div>
      <div class="tech-pill"><span class="t-icon">⚡</span>Redis</div>
      <div class="tech-pill"><span class="t-icon">~</span>gRPC</div>
      <div class="tech-pill"><span class="t-icon">◎</span>NATS</div>
      <div class="tech-pill"><span class="t-icon">∿</span>RxJS</div>
      <div class="tech-pill"><span class="t-icon">🐧</span>Linux</div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- GITHUB STATS -->
  <section class="stats">
    <div class="section-label"><span>//</span> github stats</div>
    <div class="stats-grid">
      <div class="stats-img-wrap">
        <img src="https://github-readme-stats.vercel.app/api?username=hamzamalfawaer&show_icons=true&theme=dark&bg_color=13161d&title_color=7ee8a2&icon_color=4fc3f7&text_color=8892a4&border_color=1a1e28&hide_border=false" alt="GitHub Stats" />
      </div>
      <div class="stats-img-wrap">
        <img src="https://streak-stats.demolab.com?user=hamzamalfawaer&theme=dark&background=13161d&ring=7ee8a2&fire=f77f6e&currStreakLabel=4fc3f7&sideNums=8892a4&dates=4a5568&border=1a1e28" alt="GitHub Streak" />
      </div>
      <div class="stats-img-wrap" style="grid-column: 1 / -1;">
        <img src="https://github-readme-stats.vercel.app/api/top-langs?username=hamzamalfawaer&layout=compact&theme=dark&bg_color=13161d&title_color=7ee8a2&text_color=8892a4&border_color=1a1e28&langs_count=8" alt="Top Languages" />
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- CONNECT -->
  <section class="connect">
    <div class="section-label"><span>//</span> let's connect</div>
    <div class="connect-grid">
      <a class="connect-link" href="https://linkedin.com/in/hamzamalfawaer" target="_blank">
        <div class="c-icon c-linkedin">in</div>
        <div>
          <div class="connect-name">LinkedIn</div>
          <div class="connect-handle">hamzamalfawaer</div>
        </div>
      </a>
      <a class="connect-link" href="mailto:hamzamalfawaer@email.com">
        <div class="c-icon c-gmail">@</div>
        <div>
          <div class="connect-name">Gmail</div>
          <div class="connect-handle">hamzamalfawaer</div>
        </div>
      </a>
      <a class="connect-link" href="https://instagram.com/hamzamalfawaer" target="_blank">
        <div class="c-icon c-insta">◈</div>
        <div>
          <div class="connect-name">Instagram</div>
          <div class="connect-handle">@hamzamalfawaer</div>
        </div>
      </a>
      <a class="connect-link" href="https://github.com/hamzamalfawaer" target="_blank">
        <div class="c-icon c-github">⌥</div>
        <div>
          <div class="connect-name">GitHub</div>
          <div class="connect-handle">hamzamalfawaer</div>
        </div>
      </a>
    </div>
  </section>

  <!-- COPY BUTTON -->
  <button class="copy-btn" onclick="copyReadme()">copy markdown readme ↗</button>

  <footer class="footer">
    <p>built with ❤️ · hamza al-fawaer<span class="cursor"></span></p>
  </footer>

</div>

<script>
  const readme = `<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=32&pause=1000&color=7EE8A2&center=true&vCenter=true&width=500&lines=Hi+%F0%9F%91%8B%2C+I'm+Hamza;Software+Engineer;Systems+Designer" alt="Typing SVG" />
</h1>

<p align="center">
  <em>Scalable systems · Warehouse optimization · Backend architecture that holds up</em>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=hamzamalfawaer&label=Profile+views&color=7ee8a2&style=flat" />
  <a href="https://linkedin.com/in/hamzamalfawaer"><img src="https://img.shields.io/badge/LinkedIn-%230077B5?style=flat&logo=linkedin" /></a>
  <a href="https://instagram.com/hamzamalfawaer"><img src="https://img.shields.io/badge/Instagram-%23E4405F?style=flat&logo=instagram&logoColor=white" /></a>
  <a href="mailto:hamzamalfawaer@email.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white" /></a>
</p>

---

### 🧠 About Me

| | |
|---|---|
| 🔭 **Building** | Centralized Rate-Limiting Middleware for Distributed Systems |
| 🌱 **Learning** | Next.js · RxJS · Kubernetes Sidecar Patterns |
| 💬 **Ask me about** | Warehouse optimization, scalable backends, architecture |
| 📫 **Reach me** | hamzamalfawaer@email.com |
| 📍 **Location** | Istanbul 🇹🇷 |

---

### 🚀 Projects

| Project | Description | Stack |
|---------|-------------|-------|
| [**RateLimiter Service**](https://github.com/hamzamalfawaer/rate-limiter) | Centralized rate-limiter with weight-based logic | Node.js · Express · Redis · K8s |
| [**Reactive Pipeline IDE**](https://github.com/hamzamalfawaer/reactive-pipeline-ide) | Visual RxJS workflow composer | Next.js · RxJS · Tailwind |
| [**Warehouse Audit Tool**](https://github.com/hamzamalfawaer/warehouse-audit) | CLI + web warehouse performance assessment | Python · Flask · D3.js |

---

### 🛠 Tech Stack

\`\`\`
Node.js  TypeScript  Next.js  React  Docker  Kubernetes
PostgreSQL  Redis  gRPC  NATS  RxJS  Linux  Git
\`\`\`

---

### 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=hamzamalfawaer&show_icons=true&theme=tokyonight" height="160" />
  <img src="https://streak-stats.demolab.com?user=hamzamalfawaer&theme=tokyonight" height="160" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=hamzamalfawaer&layout=compact&theme=tokyonight&langs_count=8" />
</p>

---

### 🤝 Connect

<p align="left">
  <a href="https://linkedin.com/in/hamzamalfawaer"><img src="https://img.shields.io/badge/LinkedIn-%230077B5?style=for-the-badge&logo=linkedin" /></a>
  <a href="https://instagram.com/hamzamalfawaer"><img src="https://img.shields.io/badge/Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" /></a>
  <a href="mailto:hamzamalfawaer@email.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>
`;

  function copyReadme() {
    navigator.clipboard.writeText(readme).then(() => {
      const btn = document.querySelector('.copy-btn');
      btn.textContent = '✓ copied to clipboard';
      btn.style.borderColor = 'var(--accent)';
      btn.style.color = 'var(--accent)';
      setTimeout(() => {
        btn.textContent = 'copy markdown readme ↗';
        btn.style.borderColor = '';
        btn.style.color = '';
      }, 2500);
    });
  }
</script>

</body>
</html>
