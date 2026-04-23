<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Chirag Kaushik — GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg: #0a0a0f;
    --bg2: #111118;
    --bg3: #16161f;
    --card: #1a1a25;
    --border: rgba(120,100,255,0.18);
    --accent: #7c6fff;
    --accent2: #ff6fd8;
    --accent3: #6fffd4;
    --text: #e8e6ff;
    --muted: #8884aa;
    --mono: 'JetBrains Mono', monospace;
    --sans: 'Syne', sans-serif;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Starfield bg */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      radial-gradient(1px 1px at 10% 15%, rgba(255,255,255,0.4) 0%, transparent 100%),
      radial-gradient(1px 1px at 25% 55%, rgba(255,255,255,0.25) 0%, transparent 100%),
      radial-gradient(1px 1px at 40% 30%, rgba(255,255,255,0.35) 0%, transparent 100%),
      radial-gradient(1px 1px at 60% 70%, rgba(255,255,255,0.3) 0%, transparent 100%),
      radial-gradient(1px 1px at 75% 20%, rgba(255,255,255,0.4) 0%, transparent 100%),
      radial-gradient(1px 1px at 85% 80%, rgba(255,255,255,0.2) 0%, transparent 100%),
      radial-gradient(1px 1px at 92% 45%, rgba(255,255,255,0.35) 0%, transparent 100%),
      radial-gradient(1px 1px at 5% 88%, rgba(255,255,255,0.3) 0%, transparent 100%),
      radial-gradient(1px 1px at 50% 5%, rgba(255,255,255,0.25) 0%, transparent 100%),
      radial-gradient(1px 1px at 18% 72%, rgba(255,255,255,0.2) 0%, transparent 100%);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 60px 24px;
    position: relative;
    z-index: 1;
  }

  /* ─── HERO ─── */
  .hero {
    text-align: center;
    padding: 60px 0 48px;
    animation: fadeUp 0.8s ease both;
  }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(124,111,255,0.1);
    border: 1px solid rgba(124,111,255,0.3);
    border-radius: 999px;
    padding: 6px 18px;
    font-size: 12px;
    font-family: var(--mono);
    color: var(--accent);
    letter-spacing: 0.08em;
    margin-bottom: 28px;
  }

  .hero-badge::before {
    content: '';
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--accent3);
    animation: pulse 2s infinite;
  }

  .hero-name {
    font-size: clamp(42px, 7vw, 72px);
    font-weight: 800;
    letter-spacing: -0.03em;
    line-height: 1.05;
    background: linear-gradient(135deg, #fff 0%, #c0b8ff 40%, #ff6fd8 80%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 16px;
  }

  .hero-title {
    font-size: 18px;
    color: var(--muted);
    font-weight: 400;
    margin-bottom: 28px;
    font-family: var(--mono);
  }

  .hero-title span { color: var(--accent3); }

  .hero-contacts {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 40px;
  }

  .contact-chip {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 7px 16px;
    border-radius: 999px;
    border: 1px solid var(--border);
    background: var(--card);
    font-size: 12px;
    font-family: var(--mono);
    color: var(--muted);
    text-decoration: none;
    transition: all 0.2s;
  }

  .contact-chip:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(124,111,255,0.08);
    transform: translateY(-2px);
  }

  .contact-chip svg { width: 13px; height: 13px; fill: currentColor; }

  /* ─── GITHUB STATS SECTION ─── */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-bottom: 20px;
    animation: fadeUp 0.9s 0.1s ease both;
  }

  .stats-grid img, .stat-wide img {
    width: 100%;
    border-radius: 12px;
    border: 1px solid var(--border);
    display: block;
    background: var(--card);
  }

  .stat-wide {
    margin-bottom: 16px;
    animation: fadeUp 0.9s 0.15s ease both;
  }

  .stats-row3 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 16px;
    margin-bottom: 40px;
    animation: fadeUp 0.9s 0.2s ease both;
  }

  .stats-row3 img {
    width: 100%;
    border-radius: 12px;
    border: 1px solid var(--border);
    display: block;
    background: var(--card);
  }

  /* ─── SECTION LABELS ─── */
  .section {
    margin-bottom: 48px;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 24px;
  }

  .section-label {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 0.15em;
    text-transform: uppercase;
  }

  .section-line {
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border) 0%, transparent 100%);
  }

  .section-title {
    font-size: 24px;
    font-weight: 700;
    margin-bottom: 20px;
    letter-spacing: -0.02em;
  }

  /* ─── ABOUT CARD ─── */
  .about-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 32px;
    position: relative;
    overflow: hidden;
  }

  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--accent), var(--accent2), var(--accent3));
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px 40px;
    margin-top: 20px;
  }

  .about-item {
    display: flex;
    align-items: flex-start;
    gap: 12px;
  }

  .about-icon {
    font-size: 18px;
    margin-top: 2px;
    flex-shrink: 0;
  }

  .about-text {
    font-size: 14px;
    line-height: 1.6;
    color: var(--muted);
  }

  .about-text strong {
    color: var(--text);
    font-weight: 600;
    display: block;
    margin-bottom: 2px;
  }

  /* ─── EXPERIENCE CARD ─── */
  .exp-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 28px 32px;
    margin-bottom: 16px;
    position: relative;
    transition: border-color 0.2s, transform 0.2s;
  }

  .exp-card:hover {
    border-color: rgba(124,111,255,0.4);
    transform: translateY(-2px);
  }

  .exp-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 16px;
    margin-bottom: 14px;
    flex-wrap: wrap;
  }

  .exp-role { font-size: 17px; font-weight: 700; }
  .exp-company { font-size: 14px; color: var(--accent); font-family: var(--mono); margin-top: 3px; }
  .exp-date {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
    background: rgba(124,111,255,0.08);
    border: 1px solid var(--border);
    border-radius: 999px;
    padding: 4px 12px;
    white-space: nowrap;
  }

  .exp-bullets { list-style: none; padding: 0; }
  .exp-bullets li {
    font-size: 14px;
    color: var(--muted);
    line-height: 1.7;
    padding-left: 18px;
    position: relative;
    margin-bottom: 4px;
  }
  .exp-bullets li::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: var(--accent3);
    font-size: 11px;
    top: 3px;
  }

  /* ─── PROJECTS ─── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px;
    text-decoration: none;
    display: block;
    transition: all 0.25s;
    position: relative;
    overflow: hidden;
  }

  .project-card::after {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(124,111,255,0.04), transparent);
    opacity: 0;
    transition: opacity 0.3s;
    border-radius: 16px;
  }

  .project-card:hover {
    border-color: rgba(124,111,255,0.45);
    transform: translateY(-4px);
  }

  .project-card:hover::after { opacity: 1; }

  .project-icon {
    font-size: 28px;
    margin-bottom: 12px;
    display: block;
  }

  .project-name {
    font-size: 15px;
    font-weight: 700;
    margin-bottom: 6px;
    color: var(--text);
  }

  .project-desc {
    font-size: 13px;
    color: var(--muted);
    line-height: 1.6;
    margin-bottom: 14px;
  }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .tag {
    font-family: var(--mono);
    font-size: 10px;
    padding: 3px 9px;
    border-radius: 999px;
    border: 1px solid rgba(124,111,255,0.25);
    color: var(--accent);
    background: rgba(124,111,255,0.07);
  }

  .tag.green { border-color: rgba(111,255,212,0.25); color: var(--accent3); background: rgba(111,255,212,0.07); }
  .tag.pink { border-color: rgba(255,111,216,0.25); color: var(--accent2); background: rgba(255,111,216,0.07); }

  .project-link {
    position: absolute;
    top: 20px; right: 20px;
    font-size: 16px;
    color: var(--muted);
    transition: color 0.2s;
    text-decoration: none;
  }

  .project-card:hover .project-link { color: var(--accent); }

  /* ─── TECH STACK ─── */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
    gap: 10px;
  }

  .tech-item {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 12px 8px;
    text-align: center;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
    transition: all 0.2s;
    cursor: default;
  }

  .tech-item:hover {
    border-color: var(--accent);
    color: var(--text);
    background: rgba(124,111,255,0.08);
    transform: translateY(-2px);
  }

  .tech-item .tech-icon { font-size: 22px; display: block; margin-bottom: 6px; }

  /* ─── ACHIEVEMENTS ─── */
  .achievements-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .achievement-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 20px;
    display: flex;
    align-items: flex-start;
    gap: 14px;
    transition: all 0.2s;
  }

  .achievement-card:hover {
    border-color: rgba(124,111,255,0.4);
    transform: translateY(-2px);
  }

  .ach-medal { font-size: 26px; flex-shrink: 0; }

  .ach-title {
    font-size: 14px;
    font-weight: 600;
    margin-bottom: 2px;
  }

  .ach-sub {
    font-size: 12px;
    color: var(--muted);
    font-family: var(--mono);
  }

  /* ─── DSA CARD ─── */
  .dsa-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 28px 32px;
    display: flex;
    align-items: center;
    gap: 32px;
    flex-wrap: wrap;
  }

  .dsa-stat {
    text-align: center;
  }

  .dsa-num {
    font-size: 40px;
    font-weight: 800;
    font-family: var(--mono);
    background: linear-gradient(135deg, var(--accent), var(--accent3));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1;
    margin-bottom: 4px;
  }

  .dsa-label {
    font-size: 12px;
    color: var(--muted);
    font-family: var(--mono);
  }

  .dsa-divider { width: 1px; height: 60px; background: var(--border); }

  .dsa-topics { flex: 1; }

  .dsa-topic-list {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .dsa-topic {
    font-family: var(--mono);
    font-size: 11px;
    padding: 5px 12px;
    border-radius: 999px;
    border: 1px solid var(--border);
    color: var(--muted);
    background: var(--bg3);
  }

  /* ─── LEETCODE CARD ─── */
  .lc-wrap { margin-top: 20px; }
  .lc-wrap img {
    border-radius: 12px;
    border: 1px solid var(--border);
    max-width: 500px;
    display: block;
  }

  /* ─── FOOTER ─── */
  .footer {
    text-align: center;
    padding: 48px 0 24px;
    font-family: var(--mono);
    font-size: 13px;
    color: var(--muted);
  }

  .footer-quote {
    font-size: 20px;
    font-weight: 600;
    font-family: var(--sans);
    color: var(--text);
    margin-bottom: 16px;
    letter-spacing: -0.02em;
  }

  .footer-quote span { color: var(--accent); }

  .views-badge { margin-top: 16px; }
  .views-badge img { border-radius: 999px; }

  /* ─── ANIMATIONS ─── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.85); }
  }

  @keyframes shimmer {
    0% { background-position: -200% center; }
    100% { background-position: 200% center; }
  }

  /* ─── ACTIVITY GRAPH ─── */
  .activity-wrap img {
    width: 100%;
    border-radius: 12px;
    border: 1px solid var(--border);
    display: block;
  }

  /* ─── RESEARCH ─── */
  .research-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    border-radius: 0 12px 12px 0;
    padding: 18px 22px;
    margin-bottom: 12px;
    transition: all 0.2s;
  }

  .research-card:hover {
    background: rgba(124,111,255,0.06);
    border-left-color: var(--accent3);
  }

  .research-title { font-size: 15px; font-weight: 600; margin-bottom: 4px; }

  .research-meta { font-size: 12px; color: var(--accent3); font-family: var(--mono); }

  /* RESPONSIVE */
  @media(max-width: 600px) {
    .stats-grid, .projects-grid, .achievements-grid { grid-template-columns: 1fr; }
    .stats-row3 { grid-template-columns: 1fr 1fr; }
    .about-grid { grid-template-columns: 1fr; }
    .dsa-card { flex-direction: column; gap: 16px; }
    .dsa-divider { width: 60px; height: 1px; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║           HERO               ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="hero">
    <div class="hero-badge">available for internship · delhi, india</div>
    <h1 class="hero-name">Chirag Kaushik</h1>
    <p class="hero-title">Full-Stack <span>AI Developer</span> · B.Tech AI &amp; DS @ VIPS-TC</p>

    <div class="hero-contacts">
      <a class="contact-chip" href="mailto:kaushikchirag187@gmail.com">
        <svg viewBox="0 0 24 24"><path d="M20 4H4a2 2 0 00-2 2v12a2 2 0 002 2h16a2 2 0 002-2V6a2 2 0 00-2-2zm0 4.6l-8 5-8-5V6l8 5 8-5v2.6z"/></svg>
        kaushikchirag187@gmail.com
      </a>
      <a class="contact-chip" href="https://www.linkedin.com/in/chirag-kaushik-2744982bb/" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a class="contact-chip" href="https://github.com/Chiraggksh" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
      <a class="contact-chip" href="https://leetcode.com/u/chiraggksh/" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M13.483 0a1.374 1.374 0 00-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 00-1.209 2.104 5.35 5.35 0 00-.125.513 5.527 5.527 0 00.062 2.362 5.83 5.83 0 00.349 1.017 5.938 5.938 0 001.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 00-1.951-.003l-2.396 2.392a3.021 3.021 0 01-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 01.066-.523 2.545 2.545 0 01.619-1.164L9.13 8.114c1.058-1.134 3.204-1.27 4.43-.278l3.501 2.831c.593.48 1.461.387 1.94-.207a1.384 1.384 0 00-.207-1.943l-3.5-2.831c-.8-.647-1.766-1.045-2.774-1.202l2.015-2.158A1.384 1.384 0 0013.483 0zm-2.866 12.815a1.38 1.38 0 00-1.38 1.382 1.38 1.38 0 001.38 1.382H20.79a1.38 1.38 0 001.38-1.382 1.38 1.38 0 00-1.38-1.382z"/></svg>
        LeetCode
      </a>
      <a class="contact-chip" href="https://x.com/chiraggksh" target="_blank">
        <svg viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.741l7.73-8.835L1.254 2.25H8.08l4.253 5.622zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
        @chiraggksh
      </a>
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║         GITHUB STATS         ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// github stats</span>
      <div class="section-line"></div>
    </div>

    <div class="stats-grid">
      <img src="https://github-readme-stats.vercel.app/api?username=Chiraggksh&show_icons=true&theme=transparent&title_color=7c6fff&icon_color=6fffd4&text_color=c0b8ff&border_color=3a3660&hide_border=false&rank_icon=github&include_all_commits=true&count_private=true" alt="GitHub Stats" loading="lazy" />
      <img src="https://streak-stats.demolab.com?user=Chiraggksh&theme=transparent&background=00000000&border=3a3660&ring=7c6fff&fire=ff6fd8&currStreakLabel=c0b8ff&sideLabels=8884aa&currStreakNum=ffffff&sideNums=c0b8ff&dates=6b6890" alt="GitHub Streak" loading="lazy" />
    </div>

    <div class="stat-wide">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=Chiraggksh&theme=react-dark&bg_color=1a1a25&color=c0b8ff&line=7c6fff&point=ff6fd8&area=true&area_color=7c6fff&hide_border=false&border_color=3a3660" alt="Activity Graph" loading="lazy" />
    </div>

    <div class="stats-row3">
      <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Chiraggksh&theme=transparent" alt="Profile Details" loading="lazy" />
      <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Chiraggksh&theme=transparent" alt="Languages" loading="lazy" />
      <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Chiraggksh&theme=transparent" alt="Commit Stats" loading="lazy" />
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║           ABOUT              ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// about me</span>
      <div class="section-line"></div>
    </div>

    <div class="about-card">
      <p style="font-size:15px; color:var(--muted); line-height:1.8;">
        AI &amp; Data Science undergrad with hands-on experience in full-stack web development, DSA, and ML integration. 
        Proven ability to build scalable systems, lead hackathon teams, and communicate complex ideas clearly. 
        <strong style="color:var(--accent)">Seeking an internship</strong> in AI and Web Development.
      </p>

      <div class="about-grid">
        <div class="about-item">
          <span class="about-icon">🎓</span>
          <div class="about-text">
            <strong>Education</strong>
            B.Tech AI &amp; DS @ VIPS-TC, IPU · GPA 9.12/10 · 3rd Year
          </div>
        </div>
        <div class="about-item">
          <span class="about-icon">🏆</span>
          <div class="about-text">
            <strong>Hackathon Winner</strong>
            1st Place Math-e-thon among 400+ teams · SIH 2025 Top 3
          </div>
        </div>
        <div class="about-item">
          <span class="about-icon">💡</span>
          <div class="about-text">
            <strong>Superpower</strong>
            Transforming ideas into real working products end-to-end
          </div>
        </div>
        <div class="about-item">
          <span class="about-icon">📍</span>
          <div class="about-text">
            <strong>Location</strong>
            Delhi, India · Open to remote &amp; hybrid roles
          </div>
        </div>
        <div class="about-item">
          <span class="about-icon">🔬</span>
          <div class="about-text">
            <strong>Currently</strong>
            Full Stack Dev Intern @ ByoSync · Enhancing DSA in Java
          </div>
        </div>
        <div class="about-item">
          <span class="about-icon">📞</span>
          <div class="about-text">
            <strong>Phone</strong>
            +91 9250556184
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║         EXPERIENCE           ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// experience</span>
      <div class="section-line"></div>
    </div>

    <div class="exp-card">
      <div class="exp-header">
        <div>
          <div class="exp-role">Full Stack Developer Intern</div>
          <div class="exp-company">ByoSync</div>
        </div>
        <div class="exp-date">Feb 2026 – Present · Hybrid</div>
      </div>
      <ul class="exp-bullets">
        <li>Built and optimized full-stack features using React.js, Node.js, Express, and MongoDB for a production web platform.</li>
        <li>Developed 15+ REST APIs with JWT authentication, improving performance by 30%.</li>
      </ul>
    </div>

    <div class="exp-card">
      <div class="exp-header">
        <div>
          <div class="exp-role">Technical Core Member</div>
          <div class="exp-company">Career Development Centre, VIPS-TC</div>
        </div>
        <div class="exp-date">Jan 2025 – Present</div>
      </div>
      <ul class="exp-bullets">
        <li>Developed &amp; optimized placement portal features with MERN stack for real-world use.</li>
        <li>Conducted hands-on workshops for 500+ students on full-stack development.</li>
      </ul>
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║           PROJECTS           ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// featured projects</span>
      <div class="section-line"></div>
    </div>

    <div class="projects-grid">
      <a class="project-card" href="https://github.com/Chiraggksh/women_safety" target="_blank">
        <a class="project-link" href="https://github.com/Chiraggksh/women_safety" target="_blank">↗</a>
        <span class="project-icon">🛡️</span>
        <div class="project-name">SASHAKT — AI Women Safety</div>
        <div class="project-desc">ML-based danger-zone prediction using real crime data with interactive map alerts and Flask-powered backend.</div>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag pink">Flask</span>
          <span class="tag">ML</span>
          <span class="tag green">OpenCV</span>
        </div>
      </a>

      <a class="project-card" href="https://github.com/Chiraggksh/AI-Powered-License-Plate-Recognition-System" target="_blank">
        <a class="project-link" href="https://github.com/Chiraggksh/AI-Powered-License-Plate-Recognition-System" target="_blank">↗</a>
        <span class="project-icon">📹</span>
        <div class="project-name">Watchdog AI — Surveillance</div>
        <div class="project-desc">YOLOv8-based license plate detection at 95% accuracy with real-time alert system and Flask interface.</div>
        <div class="project-tags">
          <span class="tag">YOLOv8</span>
          <span class="tag green">CV</span>
          <span class="tag pink">Flask</span>
          <span class="tag">Python</span>
        </div>
      </a>

      <a class="project-card" href="https://github.com/Chiraggksh/dbms_project" target="_blank">
        <a class="project-link" href="https://github.com/Chiraggksh/dbms_project" target="_blank">↗</a>
        <span class="project-icon">🎵</span>
        <div class="project-name">Spotify Clone — Full Stack</div>
        <div class="project-desc">Authentication, playlists, song CRUD APIs. Built with React, Node.js, Express &amp; MongoDB.</div>
        <div class="project-tags">
          <span class="tag">React</span>
          <span class="tag">Node.js</span>
          <span class="tag green">MongoDB</span>
          <span class="tag pink">Express</span>
        </div>
      </a>

      <a class="project-card" href="https://github.com/Chiraggksh" target="_blank">
        <a class="project-link" href="https://github.com/Chiraggksh" target="_blank">↗</a>
        <span class="project-icon">🌿</span>
        <div class="project-name">Pragati Path — AI Civic</div>
        <div class="project-desc">AI civic issue reporting system using NLP, CV, and predictive analytics to streamline reporting.</div>
        <div class="project-tags">
          <span class="tag">NLP</span>
          <span class="tag green">CV</span>
          <span class="tag">Python</span>
          <span class="tag pink">ML</span>
        </div>
      </a>

      <a class="project-card" href="https://github.com/Chiraggksh" target="_blank" style="grid-column: span 2;">
        <a class="project-link" href="https://github.com/Chiraggksh" target="_blank">↗</a>
        <span class="project-icon">🏕️</span>
        <div class="project-name">Project Camp Backend</div>
        <div class="project-desc">Scalable REST API with JWT auth, RBAC, task management, and file uploads. Built with Node.js, Express, and MongoDB using best-practice architecture patterns.</div>
        <div class="project-tags">
          <span class="tag">Node.js</span>
          <span class="tag green">MongoDB</span>
          <span class="tag">JWT</span>
          <span class="tag pink">RBAC</span>
          <span class="tag">REST API</span>
        </div>
      </a>
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║           TECH STACK         ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// tech stack</span>
      <div class="section-line"></div>
    </div>

    <div class="tech-grid">
      <div class="tech-item"><span class="tech-icon">⚡</span>JavaScript</div>
      <div class="tech-item"><span class="tech-icon">🐍</span>Python</div>
      <div class="tech-item"><span class="tech-icon">☕</span>Java</div>
      <div class="tech-item"><span class="tech-icon">🗄️</span>SQL</div>
      <div class="tech-item"><span class="tech-icon">⚛️</span>React.js</div>
      <div class="tech-item"><span class="tech-icon">🔄</span>Redux</div>
      <div class="tech-item"><span class="tech-icon">🌊</span>Tailwind</div>
      <div class="tech-item"><span class="tech-icon">🎨</span>Bootstrap</div>
      <div class="tech-item"><span class="tech-icon">🟢</span>Node.js</div>
      <div class="tech-item"><span class="tech-icon">🚂</span>Express.js</div>
      <div class="tech-item"><span class="tech-icon">🌶️</span>Flask</div>
      <div class="tech-item"><span class="tech-icon">🍃</span>MongoDB</div>
      <div class="tech-item"><span class="tech-icon">🐬</span>MySQL</div>
      <div class="tech-item"><span class="tech-icon">🐙</span>Git/GitHub</div>
      <div class="tech-item"><span class="tech-icon">👁️</span>OpenCV</div>
      <div class="tech-item"><span class="tech-icon">🤖</span>YOLOv8</div>
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║           DSA & CP           ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// dsa &amp; competitive coding</span>
      <div class="section-line"></div>
    </div>

    <div class="dsa-card">
      <div class="dsa-stat">
        <div class="dsa-num">200+</div>
        <div class="dsa-label">problems solved</div>
      </div>
      <div class="dsa-divider"></div>
      <div class="dsa-topics">
        <div style="font-size:13px; color:var(--muted); margin-bottom:10px; font-family:var(--mono)">strong in:</div>
        <div class="dsa-topic-list">
          <span class="dsa-topic">Arrays</span>
          <span class="dsa-topic">Linked Lists</span>
          <span class="dsa-topic">Recursion</span>
          <span class="dsa-topic">Backtracking</span>
          <span class="dsa-topic">Dynamic Programming</span>
          <span class="dsa-topic">Graphs</span>
          <span class="dsa-topic">Trees</span>
          <span class="dsa-topic">Hashing</span>
        </div>
      </div>
    </div>

    <div class="lc-wrap">
      <img src="https://leetcard.jacoblin.cool/chiraggksh?theme=dark&border=1&radius=12&ext=heatmap" alt="LeetCode Stats" loading="lazy" />
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║           RESEARCH           ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// research publications</span>
      <div class="section-line"></div>
    </div>

    <div class="research-card">
      <div class="research-title">Watchdog AI: An AI-Powered Surveillance System</div>
      <div class="research-meta">YOLOv8 + Flask · Real-time computer vision · Submitted 2025</div>
    </div>
    <div class="research-card">
      <div class="research-title">Comparative Analysis on Duplicate Detection Models</div>
      <div class="research-meta">Deep Learning · Accuracy benchmarking · Accepted 2025</div>
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║         ACHIEVEMENTS         ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <section class="section">
    <div class="section-header">
      <span class="section-label">// achievements &amp; certifications</span>
      <div class="section-line"></div>
    </div>

    <div class="achievements-grid">
      <div class="achievement-card">
        <div class="ach-medal">🥇</div>
        <div>
          <div class="ach-title">1st Place — Math-e-thon 2025</div>
          <div class="ach-sub">among 400+ teams</div>
        </div>
      </div>
      <div class="achievement-card">
        <div class="ach-medal">🥈</div>
        <div>
          <div class="ach-title">Top 3 — Smart India Hackathon 2025</div>
          <div class="ach-sub">Internal Winner · 5000+ participants</div>
        </div>
      </div>
      <div class="achievement-card">
        <div class="ach-medal">🥉</div>
        <div>
          <div class="ach-title">4th Place — Smart Delhi Ideathon 2025</div>
          <div class="ach-sub">Civic tech innovation track</div>
        </div>
      </div>
      <div class="achievement-card">
        <div class="ach-medal">🎖️</div>
        <div>
          <div class="ach-title">Finalist — Clash of Codes</div>
          <div class="ach-sub">Programming competition</div>
        </div>
      </div>
      <div class="achievement-card">
        <div class="ach-medal">📜</div>
        <div>
          <div class="ach-title">Advanced Deep Learning</div>
          <div class="ach-sub">Winter School Certification</div>
        </div>
      </div>
      <div class="achievement-card">
        <div class="ach-medal">🔬</div>
        <div>
          <div class="ach-title">2× Research Publications</div>
          <div class="ach-sub">AI/ML · Computer Vision · 2025</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ╔══════════════════════════════╗ -->
  <!-- ║            FOOTER            ║ -->
  <!-- ╚══════════════════════════════╝ -->
  <footer class="footer">
    <div class="footer-quote">"I build. I learn. I <span>grow</span> ;^)"</div>
    <div>feel free to ⭐ repos or connect!</div>
    <div class="views-badge" style="margin-top:16px;">
      <img src="https://komarev.com/ghpvc/?username=Chiraggksh&label=Profile+Views&color=7c6fff&style=flat-square" alt="Profile Views" />
    </div>
  </footer>

</div>
</body>
</html>
