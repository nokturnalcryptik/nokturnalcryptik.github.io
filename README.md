<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Averis – #1 Group Management Hub for Roblox Groups | Free</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Geist:wght@300;400;500;600;700;800;900&family=Geist+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0a0f;
    --bg2: #0f0f18;
    --surface: #13131e;
    --surface2: #1a1a28;
    --border: rgba(255,255,255,0.07);
    --border2: rgba(255,255,255,0.12);
    --text: #f0f0f8;
    --muted: #8888a8;
    --accent: #6c63ff;
    --accent2: #4f46e5;
    --accent-glow: rgba(108,99,255,0.3);
    --green: #22c55e;
    --red: #ef4444;
    --yellow: #f59e0b;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Geist', sans-serif;
    line-height: 1.6;
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
  }

  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 2rem;
    height: 60px;
    background: rgba(10,10,15,0.8);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    font-weight: 700;
    font-size: 1.1rem;
    color: var(--text);
    text-decoration: none;
  }

  .logo-icon {
    width: 28px; height: 28px;
    background: linear-gradient(135deg, var(--accent), #8b5cf6);
    border-radius: 7px;
    display: flex; align-items: center; justify-content: center;
    font-size: 14px;
    font-weight: 900;
    color: white;
  }

  .nav-links {
    display: flex;
    align-items: center;
    gap: 1.5rem;
    list-style: none;
  }

  .nav-links a {
    color: var(--muted);
    text-decoration: none;
    font-size: 0.875rem;
    font-weight: 500;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--text); }

  .nav-cta { display: flex; align-items: center; gap: 0.75rem; }

  .btn {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.5rem 1.125rem;
    border-radius: 8px;
    font-size: 0.875rem;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.2s;
    border: none;
    font-family: inherit;
  }

  .btn-ghost {
    background: transparent;
    color: var(--muted);
    border: 1px solid var(--border2);
  }

  .btn-ghost:hover {
    background: var(--surface);
    color: var(--text);
  }

  .btn-primary {
    background: var(--accent);
    color: white;
    box-shadow: 0 0 20px var(--accent-glow);
  }

  .btn-primary:hover {
    background: #7c73ff;
    box-shadow: 0 0 30px rgba(108,99,255,0.5);
    transform: translateY(-1px);
  }

  .btn-lg {
    padding: 0.75rem 1.75rem;
    font-size: 1rem;
    border-radius: 10px;
  }

  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 8rem 2rem 4rem;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -200px; left: 50%;
    transform: translateX(-50%);
    width: 800px; height: 600px;
    background: radial-gradient(ellipse, rgba(108,99,255,0.15) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: rgba(108,99,255,0.12);
    border: 1px solid rgba(108,99,255,0.3);
    color: #a5a0ff;
    padding: 0.35rem 0.875rem;
    border-radius: 100px;
    font-size: 0.8rem;
    font-weight: 600;
    margin-bottom: 1.75rem;
    letter-spacing: 0.02em;
  }

  .hero-badge .dot {
    width: 6px; height: 6px;
    background: var(--accent);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  .hero h1 {
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    font-weight: 900;
    line-height: 1.1;
    letter-spacing: -0.03em;
    max-width: 820px;
    margin-bottom: 1.5rem;
    background: linear-gradient(180deg, #ffffff 0%, #a0a0c8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero h1 span {
    background: linear-gradient(90deg, var(--accent), #a78bfa);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-sub {
    font-size: 1.125rem;
    color: var(--muted);
    max-width: 560px;
    margin-bottom: 2.5rem;
    line-height: 1.7;
  }

  .hero-actions {
    display: flex;
    align-items: center;
    gap: 1rem;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 1.5rem;
  }

  .hero-note {
    font-size: 0.8rem;
    color: var(--muted);
    display: flex;
    align-items: center;
    gap: 0.4rem;
    flex-wrap: wrap;
    justify-content: center;
  }

  .hero-note .check { color: var(--green); }

  .stats-bar {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 3rem;
    padding: 2rem;
    background: var(--surface);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    flex-wrap: wrap;
  }

  .stat { text-align: center; }

  .stat-num {
    font-size: 1.75rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--accent), #a78bfa);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .stat-label { font-size: 0.8rem; color: var(--muted); font-weight: 500; margin-top: 0.1rem; }

  .mockup-section { padding: 5rem 2rem; max-width: 1100px; margin: 0 auto; }

  .dashboard-mock {
    background: var(--surface);
    border: 1px solid var(--border2);
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 40px 120px rgba(0,0,0,0.6), 0 0 0 1px rgba(108,99,255,0.1);
  }

  .mock-titlebar {
    background: var(--bg2);
    padding: 0.875rem 1.25rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    border-bottom: 1px solid var(--border);
  }

  .mock-dot { width: 12px; height: 12px; border-radius: 50%; }
  .mock-dot.r { background: #ef4444; }
  .mock-dot.y { background: #f59e0b; }
  .mock-dot.g { background: #22c55e; }

  .mock-url {
    margin-left: 1rem;
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 0.3rem 0.875rem;
    font-size: 0.75rem;
    color: var(--muted);
    font-family: 'Geist Mono', monospace;
    flex: 1;
    max-width: 300px;
  }

  .mock-body { display: flex; min-height: 380px; }

  .mock-sidebar {
    width: 200px;
    background: var(--bg2);
    border-right: 1px solid var(--border);
    padding: 1.25rem;
    flex-shrink: 0;
  }

  .mock-sidebar-title {
    font-size: 0.7rem;
    font-weight: 700;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 0.875rem;
    margin-top: 0.5rem;
  }

  .mock-nav-item {
    display: flex;
    align-items: center;
    gap: 0.6rem;
    padding: 0.5rem 0.6rem;
    border-radius: 7px;
    font-size: 0.8rem;
    font-weight: 500;
    color: var(--muted);
    margin-bottom: 0.25rem;
  }

  .mock-nav-item.active { background: rgba(108,99,255,0.15); color: #a5a0ff; }

  .mock-content { flex: 1; padding: 1.5rem; overflow: hidden; }

  .mock-content-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.25rem;
  }

  .mock-content-title { font-size: 1rem; font-weight: 700; }

  .mock-stat-cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0.75rem;
    margin-bottom: 1.25rem;
  }

  .mock-stat-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1rem;
  }

  .mock-stat-card-label { font-size: 0.7rem; color: var(--muted); font-weight: 500; margin-bottom: 0.35rem; }
  .mock-stat-card-value { font-size: 1.5rem; font-weight: 800; }
  .mock-stat-card-value.accent { color: var(--accent); }
  .mock-stat-card-value.green { color: var(--green); }
  .mock-stat-card-value.yellow { color: var(--yellow); }

  .mock-table-header {
    display: grid;
    grid-template-columns: 2fr 1.5fr 1fr 1fr 80px;
    gap: 0.5rem;
    padding: 0.5rem 0.875rem;
    font-size: 0.7rem;
    font-weight: 600;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    background: var(--bg2);
    border-radius: 8px 8px 0 0;
    border: 1px solid var(--border);
    border-bottom: none;
  }

  .mock-table-row {
    display: grid;
    grid-template-columns: 2fr 1.5fr 1fr 1fr 80px;
    gap: 0.5rem;
    padding: 0.625rem 0.875rem;
    font-size: 0.78rem;
    border: 1px solid var(--border);
    border-top: none;
    background: var(--surface2);
    align-items: center;
  }

  .mock-table-row:last-child { border-radius: 0 0 8px 8px; }

  .badge {
    display: inline-flex;
    align-items: center;
    padding: 0.15rem 0.55rem;
    border-radius: 100px;
    font-size: 0.68rem;
    font-weight: 700;
  }

  .badge.ban { background: rgba(239,68,68,0.15); color: #f87171; }
  .badge.warn { background: rgba(245,158,11,0.15); color: #fbbf24; }
  .badge.kick { background: rgba(108,99,255,0.15); color: #a5a0ff; }
  .badge.open { background: rgba(34,197,94,0.15); color: #4ade80; }
  .badge.closed { background: rgba(100,100,120,0.2); color: var(--muted); }

  .section { padding: 5rem 2rem; max-width: 1100px; margin: 0 auto; }

  .section-tag {
    font-size: 0.75rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: var(--accent);
    margin-bottom: 0.75rem;
  }

  .section-title {
    font-size: clamp(1.75rem, 3.5vw, 2.75rem);
    font-weight: 800;
    letter-spacing: -0.025em;
    line-height: 1.2;
    margin-bottom: 1rem;
  }

  .section-sub { font-size: 1.05rem; color: var(--muted); max-width: 520px; line-height: 1.7; }

  .features-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
    margin-top: 3.5rem;
  }

  .feature-card { background: var(--surface); padding: 2rem; transition: background 0.2s; }
  .feature-card:hover { background: var(--surface2); }

  .feature-icon {
    width: 40px; height: 40px;
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 1rem;
    font-size: 18px;
  }

  .feature-icon.purple { background: rgba(108,99,255,0.15); }
  .feature-icon.green { background: rgba(34,197,94,0.12); }
  .feature-icon.blue { background: rgba(59,130,246,0.12); }
  .feature-icon.orange { background: rgba(249,115,22,0.12); }
  .feature-icon.pink { background: rgba(236,72,153,0.12); }
  .feature-icon.cyan { background: rgba(6,182,212,0.12); }

  .feature-title { font-size: 0.975rem; font-weight: 700; margin-bottom: 0.5rem; }
  .feature-desc { font-size: 0.85rem; color: var(--muted); line-height: 1.65; }

  .pricing-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.25rem; margin-top: 3.5rem; }

  .pricing-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 2rem;
    position: relative;
  }

  .pricing-card.popular {
    border-color: var(--accent);
    box-shadow: 0 0 40px rgba(108,99,255,0.15);
  }

  .popular-badge {
    position: absolute;
    top: -12px; left: 50%;
    transform: translateX(-50%);
    background: var(--accent);
    color: white;
    font-size: 0.7rem;
    font-weight: 700;
    padding: 0.25rem 0.75rem;
    border-radius: 100px;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    white-space: nowrap;
  }

  .plan-name { font-size: 0.85rem; font-weight: 700; color: var(--muted); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 0.875rem; }
  .plan-price { font-size: 2.5rem; font-weight: 900; letter-spacing: -0.03em; margin-bottom: 0.25rem; }
  .plan-price sup { font-size: 1rem; font-weight: 600; vertical-align: super; letter-spacing: 0; }
  .plan-period { font-size: 0.8rem; color: var(--muted); margin-bottom: 1.5rem; }
  .plan-divider { height: 1px; background: var(--border); margin-bottom: 1.5rem; }

  .plan-features { list-style: none; margin-bottom: 2rem; }

  .plan-features li {
    display: flex;
    align-items: flex-start;
    gap: 0.6rem;
    font-size: 0.85rem;
    color: var(--muted);
    margin-bottom: 0.7rem;
    line-height: 1.4;
  }

  .plan-features li .check { color: var(--green); flex-shrink: 0; margin-top: 2px; }
  .plan-features li .x { color: #555; flex-shrink: 0; margin-top: 2px; }

  .testimonials-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.25rem; margin-top: 3.5rem; }

  .testimonial-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 1.5rem;
  }

  .stars { color: #f59e0b; font-size: 0.85rem; margin-bottom: 0.875rem; }
  .testimonial-text { font-size: 0.875rem; color: var(--muted); line-height: 1.7; margin-bottom: 1.25rem; }
  .testimonial-author { display: flex; align-items: center; gap: 0.75rem; }

  .author-avatar {
    width: 34px; height: 34px;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-weight: 700; font-size: 0.8rem; color: white;
  }

  .author-name { font-size: 0.85rem; font-weight: 600; }
  .author-role { font-size: 0.75rem; color: var(--muted); }

  .cta-section { padding: 6rem 2rem; text-align: center; position: relative; }

  .cta-section::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at center, rgba(108,99,255,0.12) 0%, transparent 70%);
    pointer-events: none;
  }

  .cta-box { max-width: 640px; margin: 0 auto; position: relative; }
  .cta-box h2 { font-size: clamp(1.75rem, 3.5vw, 2.5rem); font-weight: 800; letter-spacing: -0.025em; margin-bottom: 1rem; }
  .cta-box p { color: var(--muted); margin-bottom: 2rem; font-size: 1.05rem; }

  footer { border-top: 1px solid var(--border); padding: 3rem 2rem 2rem; }
  .footer-inner { max-width: 1100px; margin: 0 auto; }

  .footer-top { display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 3rem; margin-bottom: 3rem; }
  .footer-brand p { font-size: 0.85rem; color: var(--muted); margin-top: 0.875rem; line-height: 1.7; max-width: 260px; }
  .footer-col-title { font-size: 0.8rem; font-weight: 700; color: var(--text); text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 1rem; }

  .footer-col a { display: block; font-size: 0.85rem; color: var(--muted); text-decoration: none; margin-bottom: 0.6rem; transition: color 0.2s; }
  .footer-col a:hover { color: var(--text); }

  .footer-bottom {
    display: flex; align-items: center; justify-content: space-between;
    padding-top: 2rem; border-top: 1px solid var(--border);
    font-size: 0.8rem; color: var(--muted);
  }

  .chip {
    display: inline-flex; align-items: center; gap: 0.4rem;
    background: var(--surface2); border: 1px solid var(--border2);
    border-radius: 6px; padding: 0.2rem 0.6rem;
    font-size: 0.72rem; font-weight: 600; color: var(--muted);
    font-family: 'Geist Mono', monospace;
  }

  .text-center { text-align: center; }

  @media (max-width: 768px) {
    .nav-links { display: none; }
    .features-grid, .pricing-grid, .testimonials-grid { grid-template-columns: 1fr; }
    .footer-top { grid-template-columns: 1fr 1fr; }
    .mock-sidebar { display: none; }
    .mock-stat-cards { grid-template-columns: 1fr 1fr; }
    .stats-bar { gap: 1.5rem; }
  }
</style>
</head>
<body>

<nav>
  <a href="#" class="nav-logo">
    <div class="logo-icon">P</div>
    Averis
  </a>
  <ul class="nav-links">
    <li><a href="#">Home</a></li>
    <li><a href="#">Pricing</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Documentation</a></li>
    <li><a href="#">Guides</a></li>
  </ul>
  <div class="nav-cta">
    <a href="#" class="btn btn-ghost">Sign in</a>
    <a href="#" class="btn btn-primary">Get Started Free</a>
  </div>
</nav>

<section class="hero">
  <div class="hero-badge">
    <span class="dot"></span>
    #1 Moderation Hub for Roblox Groups
  </div>
  <h1>The <span>all-in-one</span> moderation platform for Roblox groups</h1>
  <p class="hero-sub">Track cases, upload evidence, manage staff, and maintain full accountability — free forever. Set up in under 5 minutes with no credit card required.</p>
  <div class="hero-actions">
    <a href="#" class="btn btn-primary btn-lg">Get Started — It's Free</a>
    <a href="#" class="btn btn-ghost btn-lg">View Documentation</a>
  </div>
  <p class="hero-note">
    <span class="check">✓</span> No credit card required &nbsp;·&nbsp;
    <span class="check">✓</span> Free forever plan &nbsp;·&nbsp;
    <span class="check">✓</span> Setup in 5 minutes
  </p>
</section>

<div class="stats-bar">
  <div class="stat"><div class="stat-num">12,000+</div><div class="stat-label">Groups using Averis</div></div>
  <div class="stat"><div class="stat-num">850K+</div><div class="stat-label">Cases logged</div></div>
  <div class="stat"><div class="stat-num">99.9%</div><div class="stat-label">Uptime SLA</div></div>
  <div class="stat"><div class="stat-num">Free</div><div class="stat-label">Forever base plan</div></div>
</div>

<div class="mockup-section">
  <div class="dashboard-mock">
    <div class="mock-titlebar">
      <div class="mock-dot r"></div>
      <div class="mock-dot y"></div>
      <div class="mock-dot g"></div>
      <div class="mock-url">app.withprova.app/dashboard</div>
    </div>
    <div class="mock-body">
      <div class="mock-sidebar">
        <div style="font-size:0.9rem;font-weight:700;margin-bottom:1.5rem;display:flex;align-items:center;gap:0.5rem;">
          <div class="logo-icon" style="width:22px;height:22px;font-size:11px;">P</div>
          Aervis
        </div>
        <div class="mock-sidebar-title">General</div>
        <div class="mock-nav-item active">⊞ &nbsp;Dashboard</div>
        <div class="mock-nav-item">◈ &nbsp;Cases</div>
        <div class="mock-nav-item">◉ &nbsp;Staff</div>
        <div class="mock-nav-item">◎ &nbsp;Evidence</div>
        <div class="mock-sidebar-title" style="margin-top:1rem;">Settings</div>
        <div class="mock-nav-item">⚙ &nbsp;Settings</div>
      </div>
      <div class="mock-content">
        <div class="mock-content-header">
          <div class="mock-content-title">Dashboard Overview</div>
          <div style="display:flex;gap:0.5rem;align-items:center;">
            <span class="chip">Last 30 days</span>
            <span class="btn btn-primary" style="padding:0.3rem 0.75rem;font-size:0.75rem;border-radius:6px;">+ New Case</span>
          </div>
        </div>
        <div class="mock-stat-cards">
          <div class="mock-stat-card"><div class="mock-stat-card-label">Total Cases</div><div class="mock-stat-card-value accent">1,284</div></div>
          <div class="mock-stat-card"><div class="mock-stat-card-label">Resolved</div><div class="mock-stat-card-value green">1,187</div></div>
          <div class="mock-stat-card"><div class="mock-stat-card-label">Open</div><div class="mock-stat-card-value yellow">97</div></div>
        </div>
        <div class="mock-table-header">
          <span>User</span><span>Moderator</span><span>Action</span><span>Status</span><span>Date</span>
        </div>
        <div class="mock-table-row">
          <span>xXDarkKnight99</span>
          <span style="color:var(--muted);">mod_alpha</span>
          <span><span class="badge ban">Ban</span></span>
          <span><span class="badge closed">Closed</span></span>
          <span style="color:var(--muted);font-size:0.72rem;font-family:'Geist Mono',monospace;">Mar 26</span>
        </div>
        <div class="mock-table-row">
          <span>ProGamer2025</span>
          <span style="color:var(--muted);">mod_beta</span>
          <span><span class="badge warn">Warn</span></span>
          <span><span class="badge open">Open</span></span>
          <span style="color:var(--muted);font-size:0.72rem;font-family:'Geist Mono',monospace;">Mar 27</span>
        </div>
        <div class="mock-table-row">
          <span>BloxFan5000</span>
          <span style="color:var(--muted);">mod_alpha</span>
          <span><span class="badge kick">Kick</span></span>
          <span><span class="badge closed">Closed</span></span>
          <span style="color:var(--muted);font-size:0.72rem;font-family:'Geist Mono',monospace;">Mar 25</span>
        </div>
      </div>
    </div>
  </div>
</div>

<section class="section">
  <div class="section-tag">Features</div>
  <h2 class="section-title">Everything your group needs<br>to stay accountable</h2>
  <p class="section-sub">Built specifically for Roblox group owners and their moderation teams.</p>
  <div class="features-grid">
    <div class="feature-card"><div class="feature-icon purple">🗂️</div><div class="feature-title">Case Management</div><p class="feature-desc">Create, track, and resolve moderation cases with a full audit trail. Never lose track of a ban, kick, or warning again.</p></div>
    <div class="feature-card"><div class="feature-icon green">📎</div><div class="feature-title">Evidence Upload</div><p class="feature-desc">Attach screenshots, video links, and notes directly to cases. Keep all evidence organized and accessible to your team.</p></div>
    <div class="feature-card"><div class="feature-icon blue">👥</div><div class="feature-title">Staff Management</div><p class="feature-desc">Manage your moderation team, assign roles, and track staff activity and performance from one central hub.</p></div>
    <div class="feature-card"><div class="feature-icon orange">📣</div><div class="feature-title">Appeal System</div><p class="feature-desc">Built-in appeal forms let banned users request review. You control the process, rules, and outcomes entirely.</p></div>
    <div class="feature-card"><div class="feature-icon pink">🔔</div><div class="feature-title">Activity Logs</div><p class="feature-desc">Full audit logs of every action taken. Know who did what, when, and why — with timestamps and moderator attribution.</p></div>
    <div class="feature-card"><div class="feature-icon cyan">⚡</div><div class="feature-title">Instant Setup</div><p class="feature-desc">Connect your Roblox group and be fully operational in under 5 minutes. No technical knowledge required.</p></div>
  </div>
</section>

<section class="section">
  <div class="text-center">
    <div class="section-tag" style="display:inline-block;">Pricing</div>
    <h2 class="section-title">Simple, transparent pricing</h2>
    <p class="section-sub" style="margin:0 auto;">Start free. Upgrade when you need more power.</p>
  </div>
  <div class="pricing-grid">
    <div class="pricing-card">
      <div class="plan-name">Free</div>
      <div class="plan-price">$0</div>
      <div class="plan-period">forever</div>
      <div class="plan-divider"></div>
      <ul class="plan-features">
        <li><span class="check">✓</span> Up to 500 cases/month</li>
        <li><span class="check">✓</span> 3 staff members</li>
        <li><span class="check">✓</span> Basic case tracking</li>
        <li><span class="check">✓</span> Evidence attachments</li>
        <li><span class="x">✕</span> <span style="opacity:0.5">Custom appeal forms</span></li>
        <li><span class="x">✕</span> <span style="opacity:0.5">Priority support</span></li>
        <li><span class="x">✕</span> <span style="opacity:0.5">API access</span></li>
      </ul>
      <a href="#" class="btn btn-ghost" style="width:100%;justify-content:center;">Get Started Free</a>
    </div>
    <div class="pricing-card popular">
      <div class="popular-badge">Most Popular</div>
      <div class="plan-name">Pro</div>
      <div class="plan-price"><sup>$</sup>9</div>
      <div class="plan-period">per month</div>
      <div class="plan-divider"></div>
      <ul class="plan-features">
        <li><span class="check">✓</span> Unlimited cases</li>
        <li><span class="check">✓</span> Unlimited staff members</li>
        <li><span class="check">✓</span> Advanced case tracking</li>
        <li><span class="check">✓</span> Evidence attachments</li>
        <li><span class="check">✓</span> Custom appeal forms</li>
        <li><span class="check">✓</span> Priority support</li>
        <li><span class="x">✕</span> <span style="opacity:0.5">API access</span></li>
      </ul>
      <a href="#" class="btn btn-primary" style="width:100%;justify-content:center;">Start Pro Trial</a>
    </div>
    <div class="pricing-card">
      <div class="plan-name">Enterprise</div>
      <div class="plan-price"><sup>$</sup>29</div>
      <div class="plan-period">per month</div>
      <div class="plan-divider"></div>
      <ul class="plan-features">
        <li><span class="check">✓</span> Everything in Pro</li>
        <li><span class="check">✓</span> Multiple groups</li>
        <li><span class="check">✓</span> API access</li>
        <li><span class="check">✓</span> Custom integrations</li>
        <li><span class="check">✓</span> Dedicated support</li>
        <li><span class="check">✓</span> SLA guarantee</li>
        <li><span class="check">✓</span> White-label options</li>
      </ul>
      <a href="#" class="btn btn-ghost" style="width:100%;justify-content:center;">Contact Sales</a>
    </div>
  </div>
</section>

<section class="section">
  <div class="text-center">
    <div class="section-tag" style="display:inline-block;">Testimonials</div>
    <h2 class="section-title">Loved by group owners</h2>
    <p class="section-sub" style="margin:0 auto;">Thousands of Roblox groups trust Averis to keep their communities safe.</p>
  </div>
  <div class="testimonials-grid">
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">"Averis completely changed how we handle moderation. We went from a chaotic Discord spreadsheet to a fully organized system overnight. Absolutely essential for any serious group."</p>
      <div class="testimonial-author">
        <div class="author-avatar" style="background:linear-gradient(135deg,#6c63ff,#a78bfa);">JR</div>
        <div><div class="author-name">JakesRblx</div><div class="author-role">Owner · 50K member group</div></div>
      </div>
    </div>
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">"The evidence upload feature alone is worth it. Now when users appeal bans, we have everything documented and ready. Our staff team is so much more confident."</p>
      <div class="testimonial-author">
        <div class="author-avatar" style="background:linear-gradient(135deg,#22c55e,#16a34a);">ST</div>
        <div><div class="author-name">StarTeam_Dev</div><div class="author-role">Head Moderator · 28K group</div></div>
      </div>
    </div>
    <div class="testimonial-card">
      <div class="stars">★★★★★</div>
      <p class="testimonial-text">"Set it up in literally 3 minutes. The free plan covers everything a small group needs. When we grew, upgrading to Pro was a no-brainer. Best tool in the Roblox space."</p>
      <div class="testimonial-author">
        <div class="author-avatar" style="background:linear-gradient(135deg,#f59e0b,#d97706);">NX</div>
        <div><div class="author-name">NovaxGroup</div><div class="author-role">Owner · 12K member group</div></div>
      </div>
    </div>
  </div>
</section>

<section class="cta-section">
  <div class="cta-box">
    <h2>Ready to bring order to your group?</h2>
    <p>Join thousands of Roblox group owners who trust Averis for their moderation. Free forever — no credit card needed.</p>
    <div style="display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;">
      <a href="#" class="btn btn-primary btn-lg">Get Started Free</a>
      <a href="#" class="btn btn-ghost btn-lg">View Pricing</a>
    </div>
  </div>
</section>

<footer>
  <div class="footer-inner">
    <div class="footer-top">
      <div class="footer-brand">
        <a href="#" class="nav-logo"><div class="logo-icon">P</div> Averis</a>
        <p>The #1 free moderation hub for Roblox groups. Track cases, manage staff, and maintain full accountability.</p>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">Product</div>
        <a href="#">Home</a>
        <a href="#">Pricing</a>
        <a href="#">About Averis</a>
        <a href="#">Documentation</a>
        <a href="#">Guides & Tutorials</a>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">Support</div>
        <a href="#">Contact Support</a>
        <a href="#">Appeal a Case</a>
        <a href="#">Status Page</a>
        <a href="#">Changelog</a>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">Legal</div>
        <a href="#">Privacy Policy</a>
        <a href="#">Terms of Service</a>
        <a href="#">Cookie Policy</a>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2025 Averis. All rights reserved.</span>
      <span>Not affiliated with Roblox Corporation.</span>
    </div>
  </div>
</footer>

</body>
</html>
