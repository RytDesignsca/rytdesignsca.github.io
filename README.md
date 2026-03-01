
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
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Inter",
        sans-serif;
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
      background: linear-gradient(
        to bottom,
        rgba(5, 6, 8, 0.9),
        rgba(5, 6, 8, 0.6),
        transparent
      );
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

    .hero-actions {
      display: flex;
      gap: 12px;
      align-items: center;
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
      transition: transform 0.18s ease, box-shadow 0.18s ease,
        background 0.18s ease;
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 18px 50px rgba(123, 92, 255, 0.45);
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
      transition: background 0.18s ease, border-color 0.18s ease,
        color 0.18s ease;
    }

    .btn-ghost:hover {
      background: rgba(255, 255, 255, 0.04);
      border-color: rgba(255, 255, 255, 0.2);
      color: var(--accent-strong);
    }

    .hero-panel {
      background: radial-gradient(circle at top left, #262a40, #101218 55%);
      border-radius: var(--radius-lg);
      padding: 20px 20px 18px;
      border: 1px solid rgba(255, 255, 255, 0.06);
      box-shadow: 0 26px 80px rgba(0, 0, 0, 0.6);
      position: relative;
      overflow: hidden;
    }

    .hero-panel-tag {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--accent-soft);
      margin-bottom: 10px;
    }

    .hero-panel-main {
      background: rgba(5, 6, 8, 0.6);
      border-radius: var(--radius-md);
      padding: 18px 16px;
      border: 1px solid rgba(255, 255, 255, 0.06);
    }

    .hero-panel-main h3 {
      margin: 0 0 6px;
      font-size: 1rem;
    }

    .hero-panel-main p {
      margin: 0;
      font-size: 0.8rem;
      color: var(--accent-soft);
    }

    .hero-panel-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 14px;
      font-size: 0.78rem;
      color: var(--accent-soft);
    }

    .hero-panel-chip {
      padding: 4px 10px;
      border-radius: var(--radius-sm);
      background: rgba(0, 0, 0, 0.45);
      border: 1px solid rgba(255, 255, 255, 0.08);
    }

    .hero-panel-orbit {
      position: absolute;
      inset: 0;
      pointer-events: none;
      opacity: 0.7;
      background: radial-gradient(
          circle at 10% 0,
          rgba(123, 92, 255, 0.4),
          transparent 55%
        ),
        radial-gradient(
          circle at 90% 100%,
          rgba(255, 255, 255, 0.08),
          transparent 55%
        );
      mix-blend-mode: screen;
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
      cursor: pointer;
      transition: transform 0.18s ease, box-shadow 0.18s ease,
        border-color 0.18s ease;
    }

    .project-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.7);
      border-color: rgba(255, 255, 255, 0.16);
    }

    .project-thumb {
      height: 190px;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }

    .project-body {
      padding: 16px 16px 14px;
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
      flex-wrap: wrap;
      gap: 6px;
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
      padding: 18px 18px 16px;
      display: flex;
      flex-direction: column;
      gap: 8px;
      transition: transform 0.18s ease, box-shadow 0.18s ease,
        border-color 0.18s ease;
    }

    .service-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 18px 50px rgba(0, 0, 0, 0.7);
      border-color: rgba(255, 255, 255, 0.16);
    }

    .service-title {
      font-size: 0.98rem;
    }

    .service-desc {
      font-size: 0.85rem;
      color: var(--accent-soft);
    }

    .service-meta {
      font-size: 0.78rem;
      color: var(--accent-soft);
      margin-top: 4px;
    }

    /* CONTACT */
    .contact-layout {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 32px;
      align-items: flex-start;
    }

    .contact-copy p {
      font-size: 0.9rem;
      color: var(--accent-soft);
      max-width: 360px;
    }

    form {
      background: var(--card);
      border-radius: var(--radius-md);
      border: 1px solid rgba(255, 255, 255, 0.08);
      padding: 18px 18px 16px;
      display: grid;
      gap: 12px;
    }

    label {
      font-size: 0.78rem;
      color: var(--accent-soft);
      display: block;
      margin-bottom: 4px;
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
      outline: none;
      resize: vertical;
      min-height: 0;
    }

    input::placeholder,
    textarea::placeholder {
      color: rgba(255, 255, 255, 0.35);
    }

    input:focus,
    textarea:focus {
      border-color: var(--highlight);
      box-shadow: 0 0 0 1px rgba(123, 92, 255, 0.4);
    }

    textarea {
      min-height: 110px;
    }

    .form-row {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
    }

    .form-footnote {
      font-size: 0.75rem;
      color: var(--accent-soft);
      margin-top: 4px;
    }

    .btn-submit {
      margin-top: 4px;
      border-radius: var(--radius-sm);
      padding: 9px 18px;
      font-size: 0.85rem;
      border: none;
      cursor: pointer;
      background: var(--highlight);
      color: #fff;
      justify-self: flex-start;
      transition: background 0.18s ease, transform 0.18s ease,
        box-shadow 0.18s ease;
      box-shadow: 0 12px 32px rgba(123, 92, 255, 0.35);
    }

    .btn-submit:hover {
      background: #8b6dff;
      transform: translateY(-1px);
      box-shadow: 0 16px 40px rgba(123, 92, 255, 0.45);
    }

    /* FOOTER */
    footer {
      border-top: 1px solid rgba(255, 255, 255, 0.06);
      padding: 18px 7vw 26px;
      font-size: 0.78rem;
      color: var(--accent-soft);
      display: flex;
      justify-content: space-between;
      gap: 10px;
      flex-wrap: wrap;
    }

    footer span {
      opacity: 0.9;
    }

    /* RESPONSIVE */
    @media (max-width: 880px) {
      .hero {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-panel {
        order: -1;
      }

      .contact-layout {
        grid-template-columns: minmax(0, 1fr);
      }

      nav {
        padding-inline: 5vw;
      }

      main {
        padding-inline: 5vw;
      }
    }

    @media (max-width: 640px) {
      .nav-links {
        gap: 18px;
        font-size: 0.8rem;
      }

      .hero {
        padding-top: 130px;
      }

      .section-header {
        flex-direction: column;
        align-items: flex-start;
      }

      .form-row {
        grid-template-columns: minmax(0, 1fr);
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

        <div class="hero-actions">
          <a href="#portfolio" class="btn-primary">View portfolio →</a>
          <a href="#contact" class="btn-ghost">Start a project</a>
        </div>
      </div>

      <aside class="hero-panel">
        <div class="hero-panel-orbit"></div>
        <div class="hero-panel-tag">Snapshot of my style</div>
        <div class="hero-panel-main">
          <h3>Balanced, minimal, intentional.</h3>
          <p>
            I focus on strong composition, typography, and contrast—so every piece feels considered, not crowded.
          </p>
        </div>
        <div class="hero-panel-footer">
          <span>Recent work: posters, logos, cover art</span>
          <span class="hero-panel-chip">Available for commissions</span>
        </div>
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
          <div
            class="project-thumb"
            style="background-image:url('images/design1.jpg');"
          ></div>
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
          <div
            class="project-thumb"
            style="background-image:url('images/design2.jpg');"
          ></div>
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
          <div
            class="project-thumb"
            style="background-image:url('images/design3.jpg');"
          ></div>
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
          <div
            class="project-thumb"
            style="background-image:url('images/design4.jpg');"
          ></div>
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
          <div class="service-meta">Includes: primary logo, basic usage guide, export files.</div>
        </article>

        <article class="service-card">
          <div class="service-title">Mini Brand Kit</div>
          <div class="service-desc">
            A compact identity system with logo, colors, and type choices so your brand feels consistent from day one.
          </div>
          <div class="service-meta">Includes: logo, color palette, font suggestions, simple style sheet.</div>
        </article>

        <article class="service-card">
          <div class="service-title">Poster / Cover Design</div>
          <div class="service-desc">
            A single strong visual for your event, release, or announcement—built to stand out online and offline.
          </div>
          <div class="service-meta">Includes: one key visual, export for print + social sizes.</div>
        </article>

        <article class="service-card">
          <div class="service-title">Custom Digital Artwork</div>
          <div class="service-desc">
            A one-off piece in my style—great for profiles, banners, or personal projects that need a unique look.
          </div>
          <div class="service-meta">Includes: high-res file, web-ready version.</div>
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
        <div class="contact-copy">
          <p>
            Whether you already have a clear idea or just a rough direction, I can help shape it into something visual, simple, and sharp.
          </p>
          <p>
            Use the form to reach out—include links or references if you have them. I’ll get back to you as soon as I can.
          </p>
        </div>

        <form action="https://formspree.io/f/mjkrwwpk" method="POST">
          <div class="form-row">
            <div>
              <label for="name">Name</label>
              <input
                type="text"
                id="name"
                name="name"
                placeholder="Your name"
                required
              />
            </div>
            <div>
              <label for="email">Email</label>
              <input
                type="email"
                id="email"
                name="_replyto"
                placeholder="you@example.com"
                required
              />
            </div>
          </div>

          <div>
            <label for="project">Project type</label>
            <input
              type="text"
              id="project"
              name="project_type"
              placeholder="Logo, poster, brand kit, digital art..."
            />
          </div>

          <div>
            <label for="message">Project details</label>
            <textarea
              id="message"
              name="message"
              placeholder="Tell me about your brand, style, timeline, and what you need designed."
              required
            ></textarea>
          </div>

          <button type="submit" class="btn-submit">Send message</button>
          <div class="form-footnote">
            This form uses Formspree to securely send your message.
          </div>
        </form>
      </div>
    </section>
  </main>

  <footer>
    <span>© 2026 Ryt Designs</span>
    <span>Minimal design for brands that like things clean.</span>
  </footer>
</body>
</html>
