<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tarun Attuluri — Java Full Stack Engineer</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet" />
  <style>
    /* ─── TOKENS ─────────────────────────────────────────────── */
    :root {
      --bg:        #0B0F1A;
      --surface:   #111827;
      --border:    #1E2A3A;
      --accent:    #00D4FF;
      --accent2:   #7C3AED;
      --text:      #E8EDF5;
      --muted:     #7A8AA0;
      --tag-bg:    #152030;
      --tag-text:  #5BB8D4;
      --mono:      'JetBrains Mono', monospace;
      --sans:      'Space Grotesk', sans-serif;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--sans);
      font-size: 16px;
      line-height: 1.7;
      -webkit-font-smoothing: antialiased;
    }

    /* ─── SCANLINE OVERLAY ───────────────────────────────────── */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background: repeating-linear-gradient(
        0deg,
        transparent,
        transparent 2px,
        rgba(0,0,0,0.04) 2px,
        rgba(0,0,0,0.04) 4px
      );
      pointer-events: none;
      z-index: 1000;
    }

    /* ─── NAV ────────────────────────────────────────────────── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2.5rem;
      background: rgba(11, 15, 26, 0.85);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
    }

    .nav-logo {
      font-family: var(--mono);
      font-size: 0.85rem;
      color: var(--accent);
      letter-spacing: 0.08em;
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
    }

    .nav-links a {
      font-family: var(--mono);
      font-size: 0.75rem;
      color: var(--muted);
      text-decoration: none;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      transition: color 0.2s;
    }

    .nav-links a:hover { color: var(--accent); }

    /* ─── HERO ───────────────────────────────────────────────── */
    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 8rem 2.5rem 4rem;
      max-width: 1100px;
      margin: 0 auto;
      position: relative;
    }

    /* The signature element: a live terminal-style prompt */
    .terminal-prompt {
      font-family: var(--mono);
      font-size: 0.8rem;
      color: var(--accent);
      margin-bottom: 1.5rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .terminal-prompt::before {
      content: '▶';
      animation: blink 1.2s step-end infinite;
    }

    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }

    h1 {
      font-size: clamp(2.8rem, 7vw, 5.5rem);
      font-weight: 700;
      line-height: 1.0;
      letter-spacing: -0.03em;
      margin-bottom: 0.4rem;
    }

    .name-accent {
      background: linear-gradient(135deg, var(--accent) 0%, var(--accent2) 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .hero-role {
      font-family: var(--mono);
      font-size: 1rem;
      color: var(--muted);
      margin-bottom: 2rem;
      letter-spacing: 0.04em;
    }

    .hero-desc {
      max-width: 580px;
      font-size: 1.05rem;
      color: #B0BDCe;
      line-height: 1.8;
      margin-bottom: 2.5rem;
    }

    .hero-actions {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.75rem 1.5rem;
      border-radius: 6px;
      font-family: var(--mono);
      font-size: 0.8rem;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      text-decoration: none;
      transition: all 0.2s;
      cursor: pointer;
      border: none;
    }

    .btn-primary {
      background: var(--accent);
      color: var(--bg);
      font-weight: 600;
    }

    .btn-primary:hover {
      background: #33DEFF;
      transform: translateY(-2px);
      box-shadow: 0 8px 30px rgba(0, 212, 255, 0.25);
    }

    .btn-outline {
      background: transparent;
      color: var(--text);
      border: 1px solid var(--border);
    }

    .btn-outline:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-2px);
    }

    /* ─── STATS BAR ──────────────────────────────────────────── */
    .stats-bar {
      display: flex;
      gap: 3rem;
      flex-wrap: wrap;
      margin-top: 4rem;
      padding-top: 2rem;
      border-top: 1px solid var(--border);
    }

    .stat-item { }

    .stat-value {
      font-size: 2rem;
      font-weight: 700;
      color: var(--accent);
      line-height: 1;
    }

    .stat-label {
      font-family: var(--mono);
      font-size: 0.7rem;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: 0.1em;
      margin-top: 0.25rem;
    }

    /* ─── SECTION WRAPPER ────────────────────────────────────── */
    .section {
      max-width: 1100px;
      margin: 0 auto;
      padding: 5rem 2.5rem;
    }

    .section-label {
      font-family: var(--mono);
      font-size: 0.7rem;
      color: var(--accent);
      text-transform: uppercase;
      letter-spacing: 0.15em;
      margin-bottom: 0.75rem;
    }

    .section-title {
      font-size: clamp(1.6rem, 3.5vw, 2.4rem);
      font-weight: 700;
      letter-spacing: -0.02em;
      margin-bottom: 3rem;
    }

    .divider {
      border: none;
      border-top: 1px solid var(--border);
    }

    /* ─── SKILLS GRID ────────────────────────────────────────── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 1.25rem;
    }

    .skill-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1.5rem;
      transition: border-color 0.2s, transform 0.2s;
    }

    .skill-card:hover {
      border-color: var(--accent);
      transform: translateY(-3px);
    }

    .skill-category {
      font-family: var(--mono);
      font-size: 0.65rem;
      color: var(--accent);
      text-transform: uppercase;
      letter-spacing: 0.12em;
      margin-bottom: 0.75rem;
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
    }

    .tag {
      background: var(--tag-bg);
      color: var(--tag-text);
      font-family: var(--mono);
      font-size: 0.72rem;
      padding: 0.25rem 0.6rem;
      border-radius: 4px;
      letter-spacing: 0.04em;
    }

    /* ─── EXPERIENCE ─────────────────────────────────────────── */
    .exp-list {
      display: flex;
      flex-direction: column;
      gap: 2.5rem;
    }

    .exp-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 2rem;
      position: relative;
      transition: border-color 0.2s;
    }

    .exp-card:hover { border-color: rgba(0, 212, 255, 0.4); }

    .exp-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 3px;
      height: 100%;
      border-radius: 10px 0 0 10px;
      background: linear-gradient(180deg, var(--accent), var(--accent2));
    }

    .exp-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 0.5rem;
    }

    .exp-role {
      font-size: 1.15rem;
      font-weight: 600;
    }

    .exp-period {
      font-family: var(--mono);
      font-size: 0.7rem;
      color: var(--muted);
      letter-spacing: 0.06em;
      background: var(--tag-bg);
      padding: 0.25rem 0.6rem;
      border-radius: 4px;
    }

    .exp-company {
      font-family: var(--mono);
      font-size: 0.8rem;
      color: var(--accent);
      margin-bottom: 1.25rem;
    }

    .exp-highlights {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
    }

    .exp-highlights li {
      font-size: 0.92rem;
      color: #B0BDCe;
      padding-left: 1.2rem;
      position: relative;
    }

    .exp-highlights li::before {
      content: '›';
      position: absolute;
      left: 0;
      color: var(--accent);
      font-weight: 700;
    }

    .exp-metrics {
      display: flex;
      gap: 1.5rem;
      flex-wrap: wrap;
      margin-top: 1.5rem;
      padding-top: 1.25rem;
      border-top: 1px solid var(--border);
    }

    .metric {
      display: flex;
      flex-direction: column;
    }

    .metric-val {
      font-size: 1.35rem;
      font-weight: 700;
      color: var(--accent);
    }

    .metric-desc {
      font-family: var(--mono);
      font-size: 0.65rem;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    /* ─── PROJECTS ───────────────────────────────────────────── */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
      gap: 1.5rem;
    }

    .project-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1.75rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      transition: border-color 0.2s, transform 0.2s;
    }

    .project-card:hover {
      border-color: rgba(124, 58, 237, 0.5);
      transform: translateY(-4px);
    }

    .project-icon {
      font-size: 1.6rem;
    }

    .project-name {
      font-size: 1.05rem;
      font-weight: 600;
    }

    .project-desc {
      font-size: 0.88rem;
      color: var(--muted);
      line-height: 1.7;
    }

    .project-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-top: auto;
    }

    /* ─── CERTIFICATIONS ─────────────────────────────────────── */
    .certs-list {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.25rem;
    }

    .cert-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1.5rem;
      display: flex;
      align-items: center;
      gap: 1.25rem;
      transition: border-color 0.2s;
    }

    .cert-card:hover { border-color: var(--accent); }

    .cert-badge {
      width: 48px;
      height: 48px;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.4rem;
      flex-shrink: 0;
    }

    .cert-badge-aws  { background: rgba(255,153,0,0.12); }
    .cert-badge-azure{ background: rgba(0,120,212,0.12); }
    .cert-badge-ant  { background: rgba(0,212,255,0.12); }

    .cert-info { }

    .cert-name {
      font-size: 0.92rem;
      font-weight: 600;
    }

    .cert-issuer {
      font-family: var(--mono);
      font-size: 0.7rem;
      color: var(--muted);
      margin-top: 0.25rem;
    }

    /* ─── CONTACT ────────────────────────────────────────────── */
    .contact-wrap {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 3rem;
      text-align: center;
    }

    .contact-headline {
      font-size: 2rem;
      font-weight: 700;
      margin-bottom: 0.75rem;
      letter-spacing: -0.02em;
    }

    .contact-sub {
      color: var(--muted);
      margin-bottom: 2rem;
      max-width: 480px;
      margin-left: auto;
      margin-right: auto;
    }

    .contact-links {
      display: flex;
      justify-content: center;
      gap: 1rem;
      flex-wrap: wrap;
    }

    /* ─── FOOTER ─────────────────────────────────────────────── */
    footer {
      text-align: center;
      padding: 2rem;
      font-family: var(--mono);
      font-size: 0.7rem;
      color: var(--muted);
      border-top: 1px solid var(--border);
    }

    /* ─── SCROLL REVEAL ──────────────────────────────────────── */
    .reveal {
      opacity: 0;
      transform: translateY(24px);
      transition: opacity 0.55s ease, transform 0.55s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ─── RESPONSIVE ─────────────────────────────────────────── */
    @media (max-width: 640px) {
      nav { padding: 1rem 1.25rem; }
      .nav-links { gap: 1rem; }
      .hero { padding: 7rem 1.25rem 3rem; }
      .section { padding: 3.5rem 1.25rem; }
      .stats-bar { gap: 2rem; }
      .exp-metrics { gap: 1rem; }
      .contact-wrap { padding: 2rem 1.25rem; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { animation: none !important; transition: none !important; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <span class="nav-logo">tarun.attuluri</span>
  <ul class="nav-links">
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Work</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="terminal-prompt">tarun@dev ~ java-fullstack-engineer</div>
  <h1>
    Tarun<br/>
    <span class="name-accent">Attuluri</span>
  </h1>
  <p class="hero-role">// Java Full Stack Engineer · 3.5 yrs · Bengaluru</p>
  <p class="hero-desc">
    Building scalable microservices and high-performance web applications with Java 17, Spring Boot, ReactJS, Kafka, and AWS. Currently at Cognizant working with Société Générale and Oxford University Press.
  </p>
  <div class="hero-actions">
    <a href="mailto:tarunattuluri19@gmail.com" class="btn btn-primary">✉ Get in Touch</a>
    <a href="https://linkedin.com" target="_blank" class="btn btn-outline">LinkedIn ↗</a>
    <a href="https://github.com" target="_blank" class="btn btn-outline">GitHub ↗</a>
  </div>

  <div class="stats-bar">
    <div class="stat-item">
      <div class="stat-value">3.5</div>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-item">
      <div class="stat-value">40%</div>
      <div class="stat-label">Perf Boost</div>
    </div>
    <div class="stat-item">
      <div class="stat-value">30%</div>
      <div class="stat-label">Sprint Velocity↑</div>
    </div>
    <div class="stat-item">
      <div class="stat-value">3</div>
      <div class="stat-label">Cloud Certs</div>
    </div>
  </div>
</section>

<hr class="divider" />

<!-- SKILLS -->
<section class="section reveal" id="skills">
  <p class="section-label">Toolbox</p>
  <h2 class="section-title">Technical Skills</h2>

  <div class="skills-grid">
    <div class="skill-card">
      <div class="skill-category">Languages</div>
      <div class="skill-tags">
        <span class="tag">Java 17</span>
        <span class="tag">JavaScript</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-category">Backend</div>
      <div class="skill-tags">
        <span class="tag">Spring Boot</span>
        <span class="tag">Microservices</span>
        <span class="tag">REST APIs</span>
        <span class="tag">Node.js</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-category">Frontend</div>
      <div class="skill-tags">
        <span class="tag">React.js</span>
        <span class="tag">Redux</span>
        <span class="tag">HTML</span>
        <span class="tag">CSS</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-category">Databases</div>
      <div class="skill-tags">
        <span class="tag">PostgreSQL</span>
        <span class="tag">MySQL</span>
        <span class="tag">MongoDB</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-category">Cloud & DevOps</div>
      <div class="skill-tags">
        <span class="tag">AWS</span>
        <span class="tag">Docker</span>
        <span class="tag">Kubernetes</span>
        <span class="tag">Jenkins</span>
        <span class="tag">CI/CD</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-category">Messaging & Security</div>
      <div class="skill-tags">
        <span class="tag">Apache Kafka</span>
        <span class="tag">JWT</span>
        <span class="tag">OAuth2</span>
        <span class="tag">SSO</span>
        <span class="tag">Auth0</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-category">Testing & AI Tools</div>
      <div class="skill-tags">
        <span class="tag">JUnit5</span>
        <span class="tag">Git</span>
        <span class="tag">Claude Code</span>
        <span class="tag">GitHub Copilot</span>
      </div>
    </div>
  </div>
</section>

<hr class="divider" />

<!-- EXPERIENCE -->
<section class="section reveal" id="experience">
  <p class="section-label">Career</p>
  <h2 class="section-title">Experience</h2>

  <div class="exp-list">

    <div class="exp-card">
      <div class="exp-header">
        <div class="exp-role">Software Engineer 2</div>
        <div class="exp-period">Sep 2023 – Present</div>
      </div>
      <div class="exp-company">Cognizant · Bengaluru · Clients: Société Générale / Oxford University Press</div>
      <ul class="exp-highlights">
        <li>Developed authentication microservices with Spring Boot, ReactJS, Redux, JWT, and SSO for secure role-based enterprise access.</li>
        <li>Built scalable full-stack applications with RESTful APIs, optimized CRUD operations, pagination, and responsive UI components.</li>
        <li>Integrated Auth0 and JWT-based mechanisms for secure login flows and authorization management.</li>
        <li>Leveraged Claude Code and GitHub Copilot to accelerate debugging, feature delivery, and unit test generation.</li>
        <li>Implemented Kafka-based async communication between services for event-driven workflows.</li>
        <li>Worked with Docker and CI/CD pipelines using Git and Jenkins for streamlined deployments.</li>
        <li>Integrated a chatbot to streamline user access request tracking without additional navigation.</li>
      </ul>
      <div class="exp-metrics">
        <div class="metric">
          <span class="metric-val">30%</span>
          <span class="metric-desc">Sprint velocity increase</span>
        </div>
        <div class="metric">
          <span class="metric-val">40%</span>
          <span class="metric-desc">Page load time reduction</span>
        </div>
      </div>
    </div>

    <div class="exp-card">
      <div class="exp-header">
        <div class="exp-role">Full Stack Intern</div>
        <div class="exp-period">Jan 2023 – Aug 2023</div>
      </div>
      <div class="exp-company">Cognizant · Bengaluru</div>
      <ul class="exp-highlights">
        <li>Developed a POC for Cognizant's internal business group using external APIs, Java, Spring Boot, AWS, REST, and AuthN/AuthZ.</li>
        <li>Implemented a reliable and scalable Employee Management System during the internship.</li>
      </ul>
    </div>

  </div>
</section>

<hr class="divider" />

<!-- PROJECTS -->
<section class="section reveal" id="projects">
  <p class="section-label">Built</p>
  <h2 class="section-title">Projects</h2>

  <div class="projects-grid">
    <div class="project-card">
      <div class="project-icon">🔐</div>
      <div class="project-name">Learn AUTH</div>
      <p class="project-desc">A full-stack MERN authentication app with sign up, log in, log out, and JWT-protected route
