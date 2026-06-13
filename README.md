<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Tarun A — AI Full Stack Java Developer at Cognizant. Building intelligent web experiences with Java, Spring, React and Node.js." />
  <meta name="author" content="Tarun A" />

  <!-- Open Graph / social preview -->
  <meta property="og:title" content="Tarun A — AI Full Stack Java Developer" />
  <meta property="og:description" content="AI Full Stack Java Developer at Cognizant. Java • Spring • React • Node.js" />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://tarunattuluri19.github.io/" />

  <title>Tarun A — AI Full Stack Java Developer</title>

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="style.css" />
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>👨‍💻</text></svg>" />
</head>
<body>
  <!-- Animated background blobs -->
  <div class="bg-blobs" aria-hidden="true">
    <span class="blob blob-1"></span>
    <span class="blob blob-2"></span>
    <span class="blob blob-3"></span>
  </div>

  <!-- ============ NAVBAR ============ -->
  <header class="navbar" id="navbar">
    <nav class="nav container">
      <a href="#home" class="nav__logo">
        <span class="logo-mark">&lt;/&gt;</span> Tarun&nbsp;A
      </a>

      <ul class="nav__menu" id="nav-menu">
        <li><a href="#home" class="nav__link active">Home</a></li>
        <li><a href="#about" class="nav__link">About</a></li>
        <li><a href="#skills" class="nav__link">Skills</a></li>
        <li><a href="#projects" class="nav__link">Projects</a></li>
        <li><a href="#contact" class="nav__link">Contact</a></li>
      </ul>

      <div class="nav__actions">
        <button class="theme-toggle" id="theme-toggle" aria-label="Toggle dark / light theme">
          <svg class="icon-sun" viewBox="0 0 24 24" width="20" height="20"><path d="M12 17a5 5 0 100-10 5 5 0 000 10zm0 2a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zm0-18a1 1 0 011 1v1a1 1 0 11-2 0V2a1 1 0 011-1zm10 11a1 1 0 010 2h-1a1 1 0 110-2h1zM3 12a1 1 0 010 2H2a1 1 0 110-2h1zm15.07-7.07a1 1 0 011.41 1.41l-.7.71a1 1 0 11-1.42-1.42l.71-.7zM5.64 17.66a1 1 0 011.41 1.41l-.7.71a1 1 0 11-1.42-1.42l.71-.7zm12.73 0l.7.71a1 1 0 01-1.41 1.41l-.71-.7a1 1 0 011.42-1.42zM6.34 4.93l.71.7A1 1 0 015.64 7.05l-.7-.71a1 1 0 011.41-1.41z" fill="currentColor"/></svg>
          <svg class="icon-moon" viewBox="0 0 24 24" width="20" height="20"><path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" fill="currentColor"/></svg>
        </button>

        <button class="nav__toggle" id="nav-toggle" aria-label="Open menu">
          <span></span><span></span><span></span>
        </button>
      </div>
    </nav>
  </header>

  <main>
    <!-- ============ HERO ============ -->
    <section class="hero section" id="home">
      <div class="container hero__grid">
        <div class="hero__content">
          <p class="hero__greet">👋 Hi there, I'm</p>
          <h1 class="hero__title">Tarun&nbsp;A</h1>
          <h2 class="hero__subtitle">
            A passionate <span class="typed" id="typed"></span>
          </h2>
          <p class="hero__text">
            I build intelligent, end‑to‑end web applications — blending solid Java &amp;
            Spring backends with modern React front‑ends, and exploring how AI can
            supercharge the way we ship software.
          </p>

          <div class="hero__cta">
            <a href="#projects" class="btn btn--primary">
              View My Work
              <svg viewBox="0 0 24 24" width="18" height="18"><path d="M5 12h14m-6-6l6 6-6 6" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </a>
            <a href="#contact" class="btn btn--ghost">Get in Touch</a>
          </div>

          <div class="hero__socials">
            <a href="https://github.com/tarunattuluri19" target="_blank" rel="noreferrer" aria-label="GitHub" class="social-link">
              <svg viewBox="0 0 24 24" width="22" height="22"><path fill="currentColor" d="M12 2C6.48 2 2 6.58 2 12.25c0 4.53 2.87 8.37 6.84 9.73.5.1.68-.22.68-.49l-.01-1.7c-2.78.62-3.37-1.21-3.37-1.21-.46-1.18-1.11-1.49-1.11-1.49-.9-.64.07-.62.07-.62 1 .07 1.53 1.05 1.53 1.05.89 1.56 2.34 1.11 2.91.85.09-.66.35-1.11.63-1.37-2.22-.26-4.55-1.14-4.55-5.06 0-1.12.39-2.03 1.03-2.75-.1-.26-.45-1.3.1-2.71 0 0 .84-.27 2.75 1.05a9.36 9.36 0 015 0c1.91-1.32 2.75-1.05 2.75-1.05.55 1.41.2 2.45.1 2.71.64.72 1.03 1.63 1.03 2.75 0 3.93-2.34 4.79-4.57 5.05.36.32.68.94.68 1.9l-.01 2.82c0 .27.18.6.69.49A10.02 10.02 0 0022 12.25C22 6.58 17.52 2 12 2z"/></svg>
            </a>
            <a href="https://tarunattuluri.netlify.app/" target="_blank" rel="noreferrer" aria-label="Blog / Portfolio" class="social-link">
              <svg viewBox="0 0 24 24" width="22" height="22"><path fill="currentColor" d="M19 3H5a2 2 0 00-2 2v14a2 2 0 002 2h14a2 2 0 002-2V5a2 2 0 00-2-2zM8 17H6v-2h2v2zm0-4H6v-2h2v2zm0-4H6V7h2v2zm10 8h-8v-2h8v2zm0-4h-8v-2h8v2zm0-4h-8V7h8v2z"/></svg>
            </a>
            <a href="mailto:tarun@example.com" aria-label="Email" class="social-link">
              <svg viewBox="0 0 24 24" width="22" height="22"><path fill="currentColor" d="M20 4H4a2 2 0 00-2 2v12a2 2 0 002 2h16a2 2 0 002-2V6a2 2 0 00-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
            </a>
          </div>
        </div>

        <div class="hero__visual">
          <div class="code-card">
            <div class="code-card__bar">
              <span class="dot dot--red"></span>
              <span class="dot dot--yellow"></span>
              <span class="dot dot--green"></span>
              <span class="code-card__file">Developer.java</span>
            </div>
<pre class="code-card__body"><code><span class="c-key">public class</span> <span class="c-cls">Developer</span> {
  <span class="c-key">String</span> name = <span class="c-str">"Tarun A"</span>;
  <span class="c-key">String</span> role = <span class="c-str">"AI Full Stack"</span>;
  <span class="c-key">String</span> company = <span class="c-str">"Cognizant"</span>;

  <span class="c-key">String[]</span> stack = {
    <span class="c-str">"Java"</span>, <span class="c-str">"Spring"</span>, <span class="c-str">"React"</span>,
    <span class="c-str">"Node.js"</span>, <span class="c-str">"Express"</span>
  };

  <span class="c-key">boolean</span> learning = <span class="c-num">true</span>; <span class="c-cmt">// AI 🚀</span>
}</code></pre>
          </div>
        </div>
      </div>
    </section>

    <!-- ============ ABOUT ============ -->
    <section class="section" id="about">
      <div class="container">
        <p class="section__eyebrow">Get to know me</p>
        <h2 class="section__title">About&nbsp;Me</h2>

        <div class="about__grid">
          <div class="about__text">
            <p>
              I'm a passionate <strong>AI Full Stack Java Developer</strong> who loves turning
              ideas into reliable, scalable products. My day‑to‑day blends clean backend
              architecture with delightful, responsive user interfaces.
            </p>
            <ul class="about__list">
              <li>🔭 I'm currently working at <strong>Cognizant</strong></li>
              <li>🌱 I'm currently learning <strong>AI‑led development</strong></li>
              <li>📝 I regularly write articles on
                <a href="https://tarunattuluri.netlify.app/" target="_blank" rel="noreferrer">tarunattuluri.netlify.app</a>
              </li>
              <li>💬 Ask me about <strong>Java, Spring, React &amp; full‑stack design</strong></li>
            </ul>
            <a href="https://tarunattuluri.netlify.app/" target="_blank" rel="noreferrer" class="btn btn--primary">Read My Blog</a>
          </div>

          <div class="about__cards">
            <div class="stat-card">
              <span class="stat-card__num">Full&nbsp;Stack</span>
              <span class="stat-card__label">End‑to‑end development</span>
            </div>
            <div class="stat-card">
              <span class="stat-card__num">AI&nbsp;+&nbsp;Web</span>
              <span class="stat-card__label">Smart applications</span>
            </div>
            <div class="stat-card">
              <span class="stat-card__num">Java&nbsp;☕</span>
              <span class="stat-card__label">Spring ecosystem</span>
            </div>
            <div class="stat-card">
              <span class="stat-card__num">Writer&nbsp;✍️</span>
              <span class="stat-card__label">Tech articles &amp; notes</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ============ SKILLS ============ -->
    <section class="section section--alt" id="skills">
      <div class="container">
        <p class="section__eyebrow">My toolbox</p>
        <h2 class="section__title">Languages &amp; Tools</h2>

        <div class="skills__grid">
          <a class="skill" href="https://www.java.com" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=java" alt="Java" loading="lazy" />
            <span>Java</span>
          </a>
          <a class="skill" href="https://spring.io" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=spring" alt="Spring" loading="lazy" />
            <span>Spring</span>
          </a>
          <a class="skill" href="https://react.dev" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=react" alt="React" loading="lazy" />
            <span>React</span>
          </a>
          <a class="skill" href="https://nodejs.org" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=nodejs" alt="Node.js" loading="lazy" />
            <span>Node.js</span>
          </a>
          <a class="skill" href="https://expressjs.com" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=express" alt="Express" loading="lazy" />
            <span>Express</span>
          </a>
          <a class="skill" href="https://developer.mozilla.org/docs/Web/JavaScript" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=js" alt="JavaScript" loading="lazy" />
            <span>JavaScript</span>
          </a>
          <a class="skill" href="https://developer.mozilla.org/docs/Web/HTML" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=html" alt="HTML5" loading="lazy" />
            <span>HTML5</span>
          </a>
          <a class="skill" href="https://developer.mozilla.org/docs/Web/CSS" target="_blank" rel="noreferrer">
            <img src="https://skillicons.dev/icons?i=css" alt="CSS3" loading="lazy" />
            <span>CSS3</span>
          </a>
        </div>
      </div>
    </section>

    <!-- ============ PROJECTS ============ -->
    <section class="section" id="projects">
      <div class="container">
        <p class="section__eyebrow">Things I've built</p>
        <h2 class="section__title">Featured Projects</h2>
        <p class="section__lead">
          A few highlights — swap these out with your real repositories any time.
        </p>

        <div class="projects__grid">
          <article class="project-card">
            <div class="project-card__top">
              <span class="project-card__icon">🤖</span>
              <div class="project-card__links">
                <a href="https://github.com/tarunattuluri19" target="_blank" rel="noreferrer" aria-label="Source code">
                  <svg viewBox="0 0 24 24" width="20" height="20"><path fill="currentColor" d="M12 2C6.48 2 2 6.58 2 12.25c0 4.53 2.87 8.37 6.84 9.73.5.1.68-.22.68-.49l-.01-1.7c-2.78.62-3.37-1.21-3.37-1.21-.46-1.18-1.11-1.49-1.11-1.49-.9-.64.07-.62.07-.62 1 .07 1.53 1.05 1.53 1.05.89 1.56 2.34 1.11 2.91.85.09-.66.35-1.11.63-1.37-2.22-.26-4.55-1.14-4.55-5.06 0-1.12.39-2.03 1.03-2.75-.1-.26-.45-1.3.1-2.71 0 0 .84-.27 2.75 1.05a9.36 9.36 0 015 0c1.91-1.32 2.75-1.05 2.75-1.05.55 1.41.2 2.45.1 2.71.64.72 1.03 1.63 1.03 2.75 0 3.93-2.34 4.79-4.57 5.05.36.32.68.94.68 1.9l-.01 2.82c0 .27.18.6.69.49A10.02 10.02 0 0022 12.25C22 6.58 17.52 2 12 2z"/></svg>
                </a>
              </div>
            </div>
            <h3 class="project-card__title">AI Assistant Platform</h3>
            <p class="project-card__desc">
              A full‑stack app pairing a Spring Boot API with a React UI to deliver
              AI‑powered chat and content generation.
            </p>
            <ul class="project-card__tags">
              <li>Java</li><li>Spring</li><li>React</li>
            </ul>
          </article>

          <article class="project-card">
            <div class="project-card__top">
              <span class="project-card__icon">🛒</span>
              <div class="project-card__links">
                <a href="https://github.com/tarunattuluri19" target="_blank" rel="noreferrer" aria-label="Source code">
                  <svg viewBox="0 0 24 24" width="20" height="20"><path fill="currentColor" d="M12 2C6.48 2 2 6.58 2 12.25c0 4.53 2.87 8.37 6.84 9.73.5.1.68-.22.68-.49l-.01-1.7c-2.78.62-3.37-1.21-3.37-1.21-.46-1.18-1.11-1.49-1.11-1.49-.9-.64.07-.62.07-.62 1 .07 1.53 1.05 1.53 1.05.89 1.56 2.34 1.11 2.91.85.09-.66.35-1.11.63-1.37-2.22-.26-4.55-1.14-4.55-5.06 0-1.12.39-2.03 1.03-2.75-.1-.26-.45-1.3.1-2.71 0 0 .84-.27 2.75 1.05a9.36 9.36 0 015 0c1.91-1.32 2.75-1.05 2.75-1.05.55 1.41.2 2.45.1 2.71.64.72 1.03 1.63 1.03 2.75 0 3.93-2.34 4.79-4.57 5.05.36.32.68.94.68 1.9l-.01 2.82c0 .27.18.6.69.49A10.02 10.02 0 0022 12.25C22 6.58 17.52 2 12 2z"/></svg>
                </a>
              </div>
            </div>
            <h3 class="project-card__title">Commerce API</h3>
            <p class="project-card__desc">
              A robust REST backend with Node.js &amp; Express handling products, carts
              and secure checkout flows.
            </p>
            <ul class="project-card__tags">
              <li>Node.js</li><li>Express</li><li>JavaScript</li>
            </ul>
          </article>

          <article class="project-card">
            <div class="project-card__top">
              <span class="project-card__icon">📊</span>
              <div class="project-card__links">
                <a href="https://github.com/tarunattuluri19" target="_blank" rel="noreferrer" aria-label="Source code">
                  <svg viewBox="0 0 24 24" width="20" height="20"><path fill="currentColor" d="M12 2C6.48 2 2 6.58 2 12.25c0 4.53 2.87 8.37 6.84 9.73.5.1.68-.22.68-.49l-.01-1.7c-2.78.62-3.37-1.21-3.37-1.21-.46-1.18-1.11-1.49-1.11-1.49-.9-.64.07-.62.07-.62 1 .07 1.53 1.05 1.53 1.05.89 1.56 2.34 1.11 2.91.85.09-.66.35-1.11.63-1.37-2.22-.26-4.55-1.14-4.55-5.06 0-1.12.39-2.03 1.03-2.75-.1-.26-.45-1.3.1-2.71 0 0 .84-.27 2.75 1.05a9.36 9.36 0 015 0c1.91-1.32 2.75-1.05 2.75-1.05.55 1.41.2 2.45.1 2.71.64.72 1.03 1.63 1.03 2.75 0 3.93-2.34 4.79-4.57 5.05.36.32.68.94.68 1.9l-.01 2.82c0 .27.18.6.69.49A10.02 10.02 0 0022 12.25C22 6.58 17.52 2 12 2z"/></svg>
                </a>
              </div>
            </div>
            <h3 class="project-card__title">Dev Blog</h3>
            <p class="project-card__desc">
              My personal space where I write articles and share what I learn about
              full‑stack and AI development.
            </p>
            <ul class="project-card__tags">
              <li>HTML</li><li>CSS</li><li>JavaScript</li>
            </ul>
          </article>
        </div>

        <div class="projects__more">
          <a href="https://github.com/tarunattuluri19?tab=repositories" target="_blank" rel="noreferrer" class="btn btn--ghost">
            See all on GitHub
            <svg viewBox="0 0 24 24" width="18" height="18"><path d="M5 12h14m-6-6l6 6-6 6" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </a>
        </div>
      </div>
    </section>

    <!-- ============ CONTACT ============ -->
    <section class="section section--alt" id="contact">
      <div class="container">
        <p class="section__eyebrow">Let's connect</p>
        <h2 class="section__title">Get In Touch</h2>
        <p class="section__lead">
          Got an idea, an opportunity, or just want to talk tech? My inbox is always open.
        </p>

        <div class="contact__actions">
          <a href="mailto:tarun@example.com" class="btn btn--primary">
            <svg viewBox="0 0 24 24" width="18" height="18"><path fill="currentColor" d="M20 4H4a2 2 0 00-2 2v12a2 2 0 002 2h16a2 2 0 002-2V6a2 2 0 00-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
            Say Hello
          </a>
          <a href="https://github.com/tarunattuluri19" target="_blank" rel="noreferrer" class="btn btn--ghost">Follow on GitHub</a>
        </div>
      </div>
    </section>
  </main>

  <!-- ============ FOOTER ============ -->
  <footer class="footer">
    <div class="container footer__inner">
      <a href="#home" class="nav__logo"><span class="logo-mark">&lt;/&gt;</span> Tarun&nbsp;A</a>
      <p class="footer__text">Designed &amp; built with ☕ &amp; ❤️ by Tarun A.</p>
      <p class="footer__copy">© <span id="year"></span> Tarun A. All rights reserved.</p>
    </div>
  </footer>

  <a href="#home" class="to-top" id="to-top" aria-label="Back to top">
    <svg viewBox="0 0 24 24" width="22" height="22"><path d="M12 19V5m-7 7l7-7 7 7" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
  </a>

  <script src="script.js"></script>
</body>
</html>
