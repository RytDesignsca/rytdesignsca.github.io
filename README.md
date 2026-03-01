
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ryt Designs — Portfolio</title>

  <style>
    :root {
      --bg: #050608;
      --card: #101218;
      --accent: #f5f5f5;
      --accent-soft: #b3b7c9;
      --accent-strong: #ffffff;
      --highlight: #7b5cff;
      --highlight-soft: rgba(123, 92, 255, 0.18);
      --radius-lg: 18px;
      --radius-md: 12px;
      --radius-sm: 999px;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: "Inter", sans-serif;
      background: radial-gradient(circle at top, #151827 0, #050608 55%);
      color: var(--accent);
      scroll-behavior: smooth;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* NAVBAR */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 100;
      backdrop-filter: blur(18px);
      background: rgba(5, 6, 8, 0.7);
      border-bottom: 1px solid rgba(255, 255, 255, 0.04);
      padding: 14px 7vw;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-weight: 700;
      letter-spacing: 0.16em;
      font-size: 0.9rem;
      text-transform: uppercase;
    }

    .nav-links {
      display: flex;
      gap: 26px;
      font-size: 0.9rem;
    }

    .nav-links a {
      color: var(--accent-soft);
      position: relative;
      padding-bottom: 4px;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: 0;
      width: 0;
      height: 1px;
      background: var(--highlight);
      transition: width 0.25s ease;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    /* LAYOUT */
    main {
      padding: 110px 7vw 70px;
      max-width: 1200px;
      margin: 0 auto;
    }

    section {
      margin-bottom: 90px;
    }

    .section-label {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--accent-soft);
      margin-bottom: 12px;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 20px;
      margin-bottom: 32px;
    }

    .section-header h2 {
      margin: 0;
      font-size: 1.7rem;
    }

    .section-header p {
      margin: 0;
      font-size: 0.9rem;
      color: var(--accent-soft);
      max-width: 360px;
    }

    /* HERO */
    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 40px;
      align-items: center;
      margin-bottom: 80px;
    }

    .hero-title {
      font-size: clamp(2.6rem, 4vw, 3.4rem);
      line-height: 1.05;
      letter-spacing: -0.04em;
      margin-bottom: 18px;
    }

    .hero-sub {
      color: var(--accent-soft);
      font-size: 0.98rem;
      max-width: 420px;
      margin-bottom: 26px;
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 26px;
    }

    .pill {
      border-radius: var(--radius-sm);
      border: 1px solid rgba(255, 255, 255, 0.08);
      padding: 6px 14px;
      font-size: 0.78rem;
      color: var(--accent-soft);
      background: rgba(255, 255, 255, 0.02);
    }

    .btn-primary {
      border-radius: var(--radius-sm);
      padding: 10px 20px;
      font-size: 0.9rem;
      border: none;
      cursor: pointer;
      background: var(--highlight);
      color: #fff;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      box-shadow: 0 14px 40px rgba(123, 92, 255, 0.35);
      transition: 0.18s ease;
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      background: #8b6dff;
    }

    .btn-ghost {
      border-radius: var(--radius-sm);
      padding: 9px 18px;
      font-size: 0.85rem;
      border: 1px solid rgba(255, 255, 255, 0.12);
      background: transparent;
      color: var(--accent-soft);
      cursor: pointer;
      transition: 0.18s ease;
    }

    .btn-ghost:hover {
      background: rgba(255, 255, 255, 0.04);
      color: var(--accent-strong);
    }

    .hero-panel {
      background: #101218;
      border-radius: var(--radius-lg);
      padding: 20px;
      border: 1px solid rgba(255, 255, 255, 0.06);
    }

    /* PORTFOLIO GRID */
    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 22px;
    }

    .project-card {
      background: var(--card);
      border-radius: var(--radius-md);
      border: 1px solid rgba(255, 255, 255, 0.06);
      overflow: hidden;
      transition: 0.18s ease;
    }

    .project-card:hover {
      transform: translateY(-4px);
      border-color: rgba(255, 255, 255, 0.16);
    }

    .project-thumb {
      height: 190px;
      background-size: cover;
      background-position: center;
    }

    .project-body {
      padding: 16px;
    }

    .project-title {
      font-size: 0.98rem;
      margin-bottom: 6px;
    }

    .project-meta {
      font-size: 0.8rem;
      color: var(--accent-soft);
      margin-bottom: 10px;
    }

    .project-tags {
      display: flex;
      gap: 6px;
      flex-wrap: wrap;
    }

    .tag {
      font-size: 0.72rem;
      padding: 4px 10px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.08);
      color: var(--accent-soft);
    }

    /* SERVICES */
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 22px;
    }

    .service-card {
      background: var(--card);
      border-radius: var(--radius-md);
      border: 1px solid rgba(255, 255, 255, 0.06);
      padding: 18px;
      transition: 0.18s ease;
    }

    .service-card:hover {
      transform: translateY(-3px);
      border-color: rgba(255, 255, 255, 0.16);
    }

    .service-title {
      font-size: 0.98rem;
    }

    .service-desc {
      font-size: 0.85rem;
      color: var(--accent-soft);
    }

    /* CONTACT */
    .contact-layout {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 32px;
    }

    form {
      background: var(--card);
      border-radius: var(--radius-md);
      border: 1px solid rgba(255, 255, 255, 0.08);
      padding: 18px;
      display: grid;
      gap: 12px;
    }

    label {
      font-size: 0.78rem;
      color: var(--accent-soft);
    }

    input,
    textarea {
      width: 100%;
      border-radius: 10px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      background: rgba(5, 6, 8, 0.7);
      color: var(--accent-strong);
      padding: 9px 10px;
      font-size: 0.85rem;
    }

    textarea {
      min-height: 110px;
    }

    .btn-submit {
      border-radius: var(--radius-sm);
      padding: 9px 18px;
      font-size: 0.85rem;
      border: none;
      cursor: pointer;
      background: var(--highlight);
      color: #fff;
      transition: 0.18s ease;
    }

    .btn-submit:hover {
      background: #8b6dff;
    }

    /* FOOTER */
    footer {
      border-top: 1px solid rgba(255, 255, 255, 0.06);
      padding: 18px 7vw 26px;
      font-size: 0.78rem;
      color: var(--accent-soft);
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
    }

    @media (max-width: 880px) {
      .hero {
        grid-template-columns: 1fr;
      }
      .contact-layout {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>

<body>
  <nav>
    <div class="logo">Ryt Designs</div>
    <div class="nav-links">
      <a href="#home">Home</a>
      <a href="#portfolio">Work</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <main>
    <!-- HERO -->
    <section id="home" class="hero">
      <div>
        <div class="section-label">Graphic design studio</div>
        <h1 class="hero-title">Minimal visuals. Clear stories. Ryt for your brand.</h1>
        <p class="hero-sub">
          I design clean, modern graphics with just enough personality to feel human—perfect for brands that want to look sharp without shouting.
        </p>

        <div class="hero-tags">
          <span class="pill">Logos & identity</span>
          <span class="pill">Posters & layouts</span>
          <span class="pill">Digital artwork</span>
        </div>

        <a href="#portfolio" class="btn-primary">View portfolio →</a>
      </div>

      <aside class="hero-panel">
        <h3>Balanced, minimal, intentional.</h3>
        <p>
          I focus on strong composition, typography, and contrast—so every piece feels considered, not crowded.
        </p>
      </aside>
    </section>

    <!-- PORTFOLIO -->
    <section id="portfolio">
      <div class="section-header">
        <div>
          <div class="section-label">Selected work</div>
          <h2>How I design.</h2>
        </div>
        <p>
          A mix of branding, posters, and digital pieces that show how I use space, type, and color to keep things minimal but expressive.
        </p>
      </div>

      <div class="portfolio-grid">
        <article class="project-card">
          <div class="project-thumb" style="background-image:url('images/design1.jpg');"></div>
          <div class="project-body">
            <div class="project-title">Monochrome Poster Study</div>
            <div class="project-meta">Exploring hierarchy with type, shape, and negative space.</div>
            <div class="project-tags">
              <span class="tag">Poster</span>
              <span class="tag">Typography</span>
              <span class="tag">Minimal</span>
            </div>
          </div>
        </article>

        <article class="project-card">
          <div class="project-thumb" style="background-image:url('images/design2.jpg');"></div>
          <div class="project-body">
            <div class="project-title">Brand Mark Concept</div>
            <div class="project-meta">A simple, flexible logo built to work at any size.</div>
            <div class="project-tags">
              <span class="tag">Logo</span>
              <span class="tag">Identity</span>
              <span class="tag">Vector</span>
            </div>
          </div>
        </article>

        <article class="project-card">
          <div class="project-thumb" style="background-image:url('images/design3.jpg');"></div>
          <div class="project-body">
            <div class="project-title">Digital Cover Artwork</div>
            <div class="project-meta">Layered gradients and shapes with a clean focal point.</div>
            <div class="project-tags">
              <span class="tag">Digital art</span>
              <span class="tag">Cover</span>
              <span class="tag">Color</span>
            </div>
          </div>
        </article>

        <article class="project-card">
          <div class="project-thumb" style="background-image:url('images/design4.jpg');"></div>
          <div class="project-body">
            <div class="project-title">Minimal Social Graphic</div>
            <div class="project-meta">Designed to be scroll-stopping without feeling loud.</div>
            <div class="project-tags">
              <span class="tag">Social</span>
              <span class="tag">Layout</span>
              <span class="tag">Clean</span>
            </div>
          </div>
        </article>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services">
      <div class="section-header">
        <div>
          <div class="section-label">Services</div>
          <h2>What you can book me for.</h2>
        </div>
        <p>
          Clear packages so you know exactly what you’re getting—no guesswork, just focused design work tailored to your project.
        </p>
      </div>

      <div class="services-grid">
        <article class="service-card">
          <div class="service-title">Logo & Wordmark</div>
          <div class="service-desc">
            A clean, versatile logo or wordmark designed to work on screens, print, and everywhere in between.
          </div>
        </article>

        <article class="service-card">
          <div class="service-title">Mini Brand Kit</div>
          <div class="service-desc">
            A compact identity system with logo, colors, and type choices so your brand feels consistent from day one.
          </div>
        </article>

        <article class="service-card">
          <div class="service-title">Poster / Cover Design</div>
          <div class="service-desc">
            A single strong visual for your event, release, or announcement—built to stand out online and offline.
          </div>
        </article>

        <article class="service-card">
          <div class="service-title">Custom Digital Artwork</div>
          <div class="service-desc">
            A one-off piece in my style—great for profiles, banners, or personal projects that need a unique look.
          </div>
        </article>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="section-header">
        <div>
          <div class="section-label">Contact</div>
          <h2>Tell me what you’re building.</h2>
        </div>
        <p>
          Share a bit about your project, timeline, and what you’re looking for. I’ll reply with next steps and options.
        </p>
      </div>

      <div class="contact-layout">
        <form action="https://formspree.io/f/mjkrwwpk" method="POST">
          <label>Name</label>
          <input type="text" name="name" required />

          <label>Email</label>
          <input type="email" name="_replyto" required />

          <label>Project Type</label>
          <input type="text" name="project_type" placeholder="Logo, poster, brand kit..." />

          <label>Message</label>
          <textarea name="message" required></textarea>

          <button type="submit" class="btn-submit">Send Message</button>
        </form>
      </div>
    </section>
  </main>

  <footer>
    <span>© 2026 Ryt Designs</span>
    <span>Minimal design for brands that like things clean.</span>
  </footer>
</
