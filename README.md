
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="RYT DESIGNS - Creativity in Every Pixel." />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>RYT DESIGNS</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Segoe+UI:700,400">
  <style>
    :root {
      --primary-bg: #fff;
      --secondary-bg: #f7f7f7;
      --header-footer-bg: #333;
      --text-color: #000;
      --inverse-text-color: #fff;
      --accent: #008080;
      --slider-bg: #e7f2fa;
      --beige: #fffacd;
      --shadow: 0 2px 18px 2px rgba(44,44,45,0.09);
      --light-border: #e5e5e5;
    }
    body {
      background: var(--primary-bg);
      color: var(--text-color);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 0;
    }
    a { color: var(--accent); text-decoration: none; }

    /* Header Bar */
    .headerbar {
      width: 100%;
      height: 58px;
      background: var(--primary-bg);
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-sizing: border-box;
      position: relative;
      border: 0;
      margin-bottom: 0.7rem;
    }
    .header-logo {
      text-align: center;
      flex: 1;
      z-index: 1;
    }
    .header-logo h1 {
      color: var(--accent);
      font-size: 2.3rem;
      margin: 0;
      font-weight: bold;
      letter-spacing: .5px;
      display: inline-block;
      vertical-align: middle;
    }
    .header-divider {
      position: absolute;
      left: 0; right: 0;
      height: 1px;
      background: #ecf1f2;
      top: 50px;
      z-index: 0;
      width: 90%;
      margin: 0 auto;
      right: 5%; left: 5%;
    }
    /* Hamburger */
    .open-menu-btn {
      background-color: var(--header-footer-bg);
      color: var(--inverse-text-color);
      border: none;
      width: 40px;
      height: 58px;
      font-size: 32px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 0;
      margin-left: 12px;
      box-sizing: border-box;
      flex-shrink:0;
    }
    .burger-icon {
      display: block;
      width: 28px;
      height: 28px;
      position: relative;
    }
    .burger-icon span {
      display: block;
      position: absolute;
      height: 3px;
      width: 100%;
      background: #fff;
      border-radius: 2px;
      opacity: 1;
      left: 0;
      transition: .16s;
    }
    .burger-icon span:nth-child(1) { top: 3px; }
    .burger-icon span:nth-child(2) { top: 12px; }
    .burger-icon span:nth-child(3) { top: 21px; }
    /* Cart */
    .open-purchases-btn {
      background-color: var(--header-footer-bg);
      color: var(--inverse-text-color);
      border: none;
      width: 40px;
      height: 58px;
      font-size: 25px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 0;
      margin-right: 12px;
      flex-shrink:0;
      position:relative;
    }
    .cart-ico::before {
      content: "";
    }
    .cart-ico {
      font-size: 28px;
      /* Using emoji/Font awesome here is preferred for live */
      /* fallback: */
      background: url('https://img.icons8.com/material-outlined/24/ffffff/shopping-cart--v2.png') no-repeat center;
      width: 28px; height: 28px; display: block;
      filter: brightness(0) invert(1);
    }
    /* Side Menu */
    #sideMenu {
      height: 100%;
      width: 0;
      position: fixed;
      z-index: 2500;
      top: 0;
      left: 0;
      background-color: var(--header-footer-bg);
      overflow-x: hidden;
      transition: 0.4s;
      padding-top: 58px;
    }
    #sideMenu .close-btn {
      position: absolute;
      top: 14px; right: 18px;
      font-size: 42px;
      color: #fff;
      cursor: pointer;
      line-height: 1;
    }
    #sideMenu a {
      padding: 14px 32px;
      font-size: 1.21rem;
      color: var(--inverse-text-color);
      display: block;
      transition: color .2s;
      border-bottom: 1px solid rgba(255,255,255,0.04);
      font-weight: 500;
      letter-spacing: .2px;
    }
    #sideMenu a:hover { color: var(--accent); background: #232323; }
    /* Cart Panel */
    #purchasesPanel {
      height: 100%;
      width: 0;
      position: fixed;
      z-index: 2400;
      top: 0; right: 0;
      background-color: var(--header-footer-bg);
      color: var(--inverse-text-color);
      overflow-y: auto;
      transition: 0.5s;
      padding-top: 58px;
    }
    #purchasesPanel .close-btn {
      position: absolute;
      top: 14px; left: 18px;
      font-size: 38px;
      color: #fff;
      cursor: pointer;
      line-height: 1;
    }
    #purchasesPanel h2 {text-align:center;}
    #purchasesPanel ul {
      list-style: none;
      padding: 0 0 0 0;
      margin: 12px 0;
    }
    #purchasesPanel li {
      background: #454545;
      border-radius: 4px;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 10px 12px;
      font-size: 1rem;
    }
    #purchasesPanel li button {
      background: var(--accent);
      color: #fff;
      border: none;
      border-radius: 4px;
      padding: 3px 9px;
      cursor: pointer;
      margin-left: 12px;
      font-size: 0.95rem;
    }
    #purchasesPanel button[onclick="openCheckout()"] {
      display:block;
      width:100%;
      margin: 12px 0 0 0;
      font-size:1.1rem;
      padding:10px 0;
    }
    /* Modal */
    .modal {display:none;position:fixed;z-index:3000;left:0;top:0;width:100%;height:100%;overflow:auto;background-color:rgba(0,0,0,0.5);}
    .modal-content {background-color:var(--header-footer-bg);margin:10% auto;padding:20px;border:1px solid #888;width:90%;max-width:480px;border-radius:9px;position:relative;color:var(--inverse-text-color);}
    .modal-content .close {position:absolute;top:10px;right:20px;font-size:32px;font-weight:bold;cursor:pointer;}
    /* --- HERO LAYOUT --- */
    .hero-flex {
      display: flex;
      justify-content: center;
      align-items: stretch;
      min-height: 80vh;
      gap: 56px;
      background: #fff;
      max-width: 1280px;
      margin: 0 auto;
      width: 100%;
    }
    @media (max-width:1100px) { .hero-flex { gap: 24px; } }
    @media (max-width:900px) {
      .hero-flex { flex-direction: column; align-items: center; gap: 18px; margin-top:32px;}
    }
    .slider-section {
      flex: 1 1 500px;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      min-width: 0;
      justify-content: center;
    }
    /* --- SLIDER --- */
    #hero-slider {
      width: 470px;
      max-width: 95vw;
      height: 350px;
      border-radius: 24px;
      background: #e1f3f8;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow: hidden;
      box-shadow: var(--shadow);
    }
    @media (max-width:600px){
      #hero-slider { max-width:99vw; height: 200px;}
    }
    .slider-item {
      width: 100%;
      height: 100%;
      position: absolute;
      left: 0; top: 0;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.52s cubic-bezier(0.4,0,0.2,1);
      z-index: 0;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .slider-item.active {
      opacity: 1;
      pointer-events: auto;
      z-index: 1;
    }
    .slider-item img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      display: block;
      background: #b1d7e9;
    }
    #slider-dots {
      display: flex;
      justify-content: center;
      gap: 11px;
      position: absolute;
      bottom: 20px;
      left: 0; right: 0;
      z-index:5;
      margin-top:0;
    }
    #slider-dots span {
      width: 14px;
      height: 14px;
      border-radius: 50%;
      background: #ddd;
      display: inline-block;
      cursor: pointer;
      border: none;
      transition: background 0.17s;
    }
    #slider-dots .active-dot {
      background: var(--header-footer-bg);
    }
    /* SLIDER CAPTION ONLY SHOW FOR T-SHIRT DESIGN */
    .slider-caption {
      display:none;
      position: absolute;
      left: 36px;
      bottom: 44px;
      background: var(--beige);
      color: #333;
      border-radius: 22px;
      padding: 9px 29px;
      font-size: 1.11rem;
      font-weight: 500;
      box-shadow: 0 2px 10px rgba(120,120,120,0.11);
      z-index: 2;
      transition: opacity .3s;
    }
    .slider-item.active .slider-caption { display: inline-block; }
    .slider-item:not(.tshirt-slide) .slider-caption { display:none !important; }
    .slider-label {
      position: absolute;
      left: 36px;
      bottom: 18px;
      color: #868686;
      font-size: 1rem;
      font-style: italic;
      opacity: 0.86;
      letter-spacing:0.2px;
    }
    .slider-item:not(.active) .slider-label { display:none !important;}
    .slider-item img {border-radius:0;}
    .hero-side {
      flex: 1.33 1 320px;
      min-width: 0;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: flex-start;
      padding-top:48px;
    }
    @media (max-width:1050px){ .hero-side {padding-top:10px;}}
    .hero-side h2 {
      font-size: 3.55rem;
      font-weight: 700;
      color: var(--accent);
      margin-bottom: .6rem;
      line-height: 1.08;
      letter-spacing: -2px;
      text-align: left;
      border-bottom: 1px solid #ebecec;
      padding-bottom:12px;
      margin-right:0;
      max-width: 640px;
      width: 100%;
    }
    .hero-side .subtitle {
      color: #222;
      font-size: 1.18rem;
      margin-bottom: 1.95rem;
      margin-top: 0.6rem;
      line-height: 1.6;
      opacity: 0.96;
      text-align: left;
      max-width: 460px;
    }
    .home-search-row {
      display: flex;
      width: 100%;
      margin-bottom: 1.2rem;
      background: #fff;
      border-radius: 17px;
      box-shadow: 0 2px 9px #eee5;
      border: 1px solid #e5e5e5;
      overflow: hidden;
      max-width: 470px;
      align-items: stretch;
    }
    .home-search-row input[type="text"] {
      flex: 1;
      padding: 20px;
      font-size: 1.11rem;
      border: none;
      background: #fff;
      outline: none;
      border-radius: 0;
    }
    .home-search-row button {
      background: var(--header-footer-bg);
      color: #fff;
      font-weight: 600;
      border: none;
      border-radius: 0 25px 25px 0;
      padding: 0 36px;
      font-size: 1.15rem;
      cursor: pointer;
      transition: background 0.2s;
      margin-left: 0;
    }
    .home-search-row button:hover { background: var(--accent);}
    .popular-tags {
      display: flex;
      gap: 8px;
      margin-top: 0.4rem;
      align-items: center;
    }
    .popular-label {
      color: #666;
      font-size: 1.05rem;
      margin-right: 8px;
    }
    .tag-btn {
      background: #ededed;
      color: #333;
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      padding: 8px 19px;
      font-weight: 600;
      cursor: pointer;
      transition: background 0.16s, color 0.16s;
      box-shadow: 0 1px 5px #e7e7e7;
      opacity:.98;
    }
    .tag-btn:hover, .tag-btn.active {
      background: var(--accent);
      color: #fff;
    }
    #searchResults { margin:12px 0 0 0;}
    .search-result {
      background: #f0f0f0;
      margin-bottom: 6px;
      padding: 9px 8px;
      border-radius: 6px;
      font-size: 1.01rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .search-result button {
      background: var(--accent);
      color: #fff !important;
      border: none;
      border-radius: 11px;
      margin-left: 7px;
      padding: 3px 13px;
      font-size: 0.95rem;
      cursor: pointer;
    }
    .search-result button:last-child {
      background: #333;
    }
    .design-process, .popular-services, .design-packages, #contact {width:100%;margin:0 auto;}
    .design-process {padding:3.2rem 0 2.2rem 0;text-align:center;background-color:var(--secondary-bg);}
    .design-process h2 {font-size:2.1rem;margin-bottom:2rem;}
    .process-steps {display:flex;justify-content:center;gap:2rem;flex-wrap:wrap;}
    .process-steps .step {background-color:var(--header-footer-bg);padding:1rem;border-radius:8px;width:120px;transition:transform 0.3s ease;color:var(--inverse-text-color);}
    .process-steps .step:hover {transform:translateY(-5px);}
    .step-number {background-color:var(--accent);color:var(--inverse-text-color);border-radius:50%;width:40px;height:40px;line-height:40px;margin:0 auto 0.5rem;font-weight:bold;}
    .popular-services {padding:3.2rem 0 2.2rem 0;text-align:center;background-color:var(--primary-bg);}
    .popular-services h2 {font-size:2.1rem;margin-bottom:2rem;}
    .services-boxes {display:flex;flex-wrap:wrap;justify-content:center;gap:1rem;}
    .service-box {background-color:var(--header-footer-bg);padding:1rem;border-radius:8px;width:180px;transition:transform 0.3s ease;text-align:center;color:var(--inverse-text-color);}
    .service-box:hover {transform:translateY(-5px);}
    .service-box img {width:60px;height:60px;margin-bottom:0.5rem;}
    .design-packages {padding:3.2rem 0 2.2rem 0;text-align:center;background-color:var(--secondary-bg);}
    .design-packages h2 {font-size:2.1rem;margin-bottom:2rem;}
    .packages {display:flex;flex-wrap:wrap;justify-content:center;gap:1rem;}
    .package-item {background-color:var(--header-footer-bg);padding:1rem;border-radius:8px;width:220px;transition:transform 0.3s ease;color:var(--inverse-text-color);}
    .package-item:hover {transform:translateY(-5px);}
    .package-item h3 {margin-bottom:0.5rem;}
    #contact {padding:3.2rem 0 2.2rem 0;text-align:center;background-color:var(--primary-bg);}
    .contact-container {display:flex;flex-direction:column;align-items:center;gap:1rem;padding:0 1rem;}
    .contact-info {margin-bottom:2rem;font-size:1.17rem;text-align:center;}
    .contact-info p {margin:0.5rem 0;}
    .social-links {display:flex;justify-content:center;gap:1.3rem;font-size:1.2rem;}
    .social-links a {color:var(--accent);font-size:1.5rem;transition:color 0.3s ease;text-decoration:none;}
    .social-links a:hover {color:var(--header-footer-bg);}
    footer {background-color:var(--header-footer-bg);text-align:center;padding:1.1rem 0;color:var(--inverse-text-color);}
    footer p {margin-bottom:0.3rem;}
    footer a.back-to-home {color:var(--accent);text-decoration:none;font-weight:bold;transition:color 0.3s ease;}
    footer a.back-to-home:hover {color:var(--inverse-text-color);}
    #productsContent {display:none;}
    #productsContent header {background-color:var(--header-footer-bg);color:var(--inverse-text-color);padding:1rem;text-align:center;}
    #productsContent header h1 {font-size:2rem;}
    #productsContent .container {max-width:1200px;margin:2rem auto;padding:1rem;}
    #productsContent .product-grid {display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));grid-gap:1.5rem;}
    #productsContent .product-item {background-color:var(--secondary-bg);border:1px solid #ccc;border-radius:8px;padding:1rem;text-align:center;transition:transform 0.3s ease;}
    #productsContent .product-item:hover {transform:translateY(-5px);}
    #productsContent .product-item h3 {margin-bottom:0.5rem;font-size:1.5rem;}
    #productsContent .product-item p {font-size:1.2rem;margin-bottom:1rem;}
    #productsContent .back-home {display:block;margin-top:2rem;text-align:center;font-size:1.1rem;text-decoration:none;color:var(--accent);}
    #productsContent .back-home:hover {text-decoration:underline;}
    @media (max-width: 600px) {
      .header-logo h1 { font-size: 1.3rem; }
      #hero-slider { max-width:99vw; height: 180px;}
      .slider-caption {font-size:0.92rem;padding:6px 18px;bottom:18px;left:12px;}
      .slider-label { font-size:0.8rem; left: 12px;bottom:6px;}
      .hero-side h2 {font-size:1.39rem;}
      .subtitle {font-size:0.98rem;}
      .popular-tags {flex-wrap:wrap;}
    }
  </style>
</head>
<body>
  <div class="headerbar">
    <button class="open-menu-btn" onclick="toggleMenu()" aria-label="Open menu">
      <span class="burger-icon"><span></span><span></span><span></span></span>
    </button>
    <div class="header-logo">
      <h1>Ryt Designs</h1>
    </div>
    <button class="open-purchases-btn" onclick="openPurchasesPanel()" aria-label="Cart">
      <span class="cart-ico"></span>
    </button>
    <div class="header-divider"></div>
  </div>
  <div id="sideMenu">
    <span class="close-btn" onclick="closeMenu()">&times;</span>
    <a href="#home" onclick="showHome(); closeMenu(); triggerHeroAnimation();">Home</a>
    <a href="#design-process" onclick="showHome(); closeMenu();">Process</a>
    <a href="#popular-services" onclick="showHome(); closeMenu();">Services</a>
    <a href="#design-packages" onclick="showHome(); closeMenu();">Packages</a>
    <a href="#products" onclick="showProducts(); closeMenu();">Products</a>
    <a href="#contact" onclick="showHome(); closeMenu();">Contact</a>
    <a href="javascript:void(0)" onclick="openPurchasesPanel(); closeMenu();">Purchases</a>
  </div>
  <div id="purchasesPanel">
    <span class="close-btn" onclick="closePurchasesPanel()">&times;</span>
    <div style="padding: 20px;">
      <h2>Your Cart</h2>
      <ul id="cartItems"></ul>
      <p id="cartTotal"></p>
      <button onclick="openCheckout()" style="padding: 10px 20px; margin-top: 10px; background-color: var(--accent); border: none; color: var(--inverse-text-color); cursor: pointer; border-radius: 4px;">Checkout</button>
    </div>
  </div>
  <div id="checkoutModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeCheckout()">&times;</span>
      <h2>Checkout</h2>
      <form id="checkoutForm">
        <p>Order Total: $<span id="orderTotal"></span></p>
        <label for="cardholder">Cardholder Name:</label><br>
        <input type="text" id="cardholder" required style="width: 100%; padding: 8px; margin: 5px 0;"><br>
        <label for="cardNumber">Card Number:</label><br>
        <input type="text" id="cardNumber" required style="width: 100%; padding: 8px; margin: 5px 0;"><br>
        <label for="expiry">Expiry Date:</label><br>
        <input type="text" id="expiry" placeholder="MM/YY" required style="width: 100%; padding: 8px; margin: 5px 0;"><br>
        <label for="cvv">CVV:</label><br>
        <input type="text" id="cvv" required style="width: 100%; padding: 8px; margin: 5px 0;"><br>
        <button type="submit" style="padding: 10px 20px; background-color: var(--accent); border: none; color: var(--inverse-text-color); cursor: pointer; border-radius: 4px;">Submit Payment</button>
      </form>
    </div>
  </div>
  <div class="main-content">
    <div id="homeContent">
      <div class="hero-flex">
        <div class="slider-section">
          <div id="hero-slider">
            <div id="slider-dots"></div>
            <div class="slider-item">
              <img src="https://rytdesignsca.github.io/website%20prototype/Album%20cover.png" alt="Album cover design">
              <div class="slider-label">RYT DESIGNS</div>
            </div>
            <div class="slider-item tshirt-slide">
              <img src="https://rytdesignsca.github.io/website%20prototype/T-Shirt%20design.png" alt="T-Shirt design">
              <div class="slider-caption">T-Shirt design</div>
              <div class="slider-label">RYT DESIGNS</div>
            </div>
            <div class="slider-item">
              <img src="https://rytdesignsca.github.io/website%20prototype/Ryt%20Skin.png" alt="Ryt Skin branding">
              <div class="slider-label">RYT DESIGNS</div>
            </div>
            <div class="slider-item">
              <img src="https://rytdesignsca.github.io/website%20prototype/Ryt%20Designs%20Poster.png" alt="Poster design">
              <div class="slider-label">RYT DESIGNS</div>
            </div>
          </div>
        </div>
        <div class="hero-side">
          <h2>Creativity in<br>every pixel</h2>
          <div class="subtitle">
            Your Vision, My Creativity—Limitless Possibilities.
          </div>
          <form class="home-search-row" onsubmit="performSearch(); return false;">
            <input type="text" id="serviceSearch" placeholder="What do you need designed?" autocomplete="off" />
            <button id="searchBtn" type="submit">Get a design</button>
          </form>
          <div class="popular-tags">
            <span class="popular-label">Popular:</span>
            <button class="tag-btn" type="button" onclick="document.getElementById('serviceSearch').value='Logo design'; performSearch();">Logo design</button>
            <button class="tag-btn" type="button" onclick="document.getElementById('serviceSearch').value='Website'; performSearch();">Website</button>
            <button class="tag-btn" type="button" onclick="document.getElementById('serviceSearch').value='Branding'; performSearch();">Branding</button>
          </div>
          <div id="searchResults"></div>
        </div>
      </div>
      <section id="design-process" class="design-process">
        <h2>Our Design Process</h2>
        <div class="process-steps">
          <div class="step">
            <div class="step-number">1</div>
            <p>Concept</p>
          </div>
          <div class="step">
            <div class="step-number">2</div>
            <p>Draft</p>
          </div>
          <div class="step">
            <div class="step-number">3</div>
            <p>Feedback</p>
          </div>
          <div class="step">
            <div class="step-number">4</div>
            <p>Final</p>
          </div>
        </div>
      </section>
      <section id="popular-services" class="popular-services">
        <h2>Popular Services</h2>
        <div class="services-boxes">
          <div class="service-box">
            <img src="web-development-icon.png" alt="Website Development" />
            <h3>Website Development</h3>
          </div>
          <div class="service-box">
            <img src="logo-design-icon.png" alt="Logo Design" />
            <h3>Logo Design</h3>
          </div>
          <div class="service-box">
            <img src="seo-icon.png" alt="SEO" />
            <h3>SEO</h3>
          </div>
          <div class="service-box">
            <img src="voice-over-icon.png" alt="Voice Over" />
            <h3>Voice Over</h3>
          </div>
          <div class="service-box">
            <img src="social-media-icon.png" alt="Social Media" />
            <h3>Social Media</h3>
          </div>
        </div>
      </section>
      <section id="design-packages" class="design-packages">
        <h2>Design Packages</h2>
        <div class="packages">
          <div class="package-item">
            <h3>Logo &amp; Business Card Design</h3>
            <p>Perfect for cohesive branding.</p>
          </div>
          <div class="package-item">
            <h3>Logo &amp; Business Card Printing</h3>
            <p>Get print‑ready designs in one go.</p>
          </div>
          <div class="package-item">
            <h3>Logo &amp; Website</h3>
            <p>Establish your online presence with a complete package.</p>
          </div>
          <div class="package-item">
            <h3>Logo &amp; Social Media Design</h3>
            <p>Consistent branding for your digital footprint.</p>
          </div>
        </div>
      </section>
      <section id="contact">
        <h2>Get in Touch</h2>
        <div class="contact-container">
          <div class="contact-info">
            <p><strong>Phone:</strong> +1 226-977-9311</p>
            <p><strong>Alternate Phone:</strong> +1 226-977-9310</p>
            <p><strong>Email:</strong>
              <a href="mailto:rytdesignsca@gmail.com" style="color: var(--accent);">rytdesignsca@gmail.com</a>
            </p>
          </div>
          <div class="social-links">
            <a href="https://www.instagram.com/rytdesigns_/" target="_blank">Instagram</a>
            <a href="https://www.tiktok.com/@ryt.designs7" target="_blank">TikTok</a>
          </div>
        </div>
      </section>
      <footer>
        <p>&copy; 2025 RYT DESIGNS. All Rights Reserved.</p>
        <p>Designed by RYT DESIGNS</p>
        <p><a href="#home" class="back-to-home">Back to Home</a></p>
      </footer>
    </div>
    <div id="productsContent">
      <header>
        <h1>RYT DESIGNS Products</h1>
      </header>
      <div class="container">
        <div class="product-grid">
          <div class="product-item"><h3>Poster/Flyer</h3><p>$15</p></div>
          <div class="product-item"><h3>Videos for events</h3><p>$25</p></div>
          <div class="product-item"><h3>Business cards</h3><p>$20</p></div>
          <div class="product-item"><h3>Invitations</h3><p>$24</p></div>
          <div class="product-item"><h3>Logos for businesses</h3><p>$30</p></div>
          <div class="product-item"><h3>YouTube Thumbnails (Basic)</h3><p>$20</p></div>
          <div class="product-item"><h3>YouTube Thumbnail (Add-ons)</h3><p>$35</p></div>
          <div class="product-item"><h3>Celebration cards</h3><p>$10</p></div>
          <div class="product-item"><h3>Presentations</h3><p>$30</p></div>
          <div class="product-item"><h3>Menus</h3><p>$20</p></div>
          <div class="product-item"><h3>Banner</h3><p>$35</p></div>
        </div>
        <a class="back-home" href="#home" onclick="showHome();">Back to Home</a>
      </div>
    </div>
  </div>
<script>
let current = 0, timer = null;
document.addEventListener("DOMContentLoaded", function() {
  // SLIDER LOGIC
  const items = document.querySelectorAll("#hero-slider .slider-item");
  const dotsContainer = document.getElementById("slider-dots");
  function show(idx) {
    items.forEach((slide, i) => {
      slide.classList.toggle("active", i === idx);
    });
    [...dotsContainer.children].forEach((d, i) => {
      d.className = i === idx ? "active-dot" : "";
    });
    current = idx;
  }
  items.forEach((el, i) => {
    const d = document.createElement("span");
    d.ariaLabel = `Go to slide ${i + 1}`;
    d.onclick = function(){ show(i); resetAuto(); }
    dotsContainer.appendChild(d);
  });
  function nextSlide() {
    clearInterval(timer); // Stop the timer
    show((current + 1) % items.length);
    autoSlide(); // Restart the timer
  }
  function autoSlide(){timer = setInterval(nextSlide, 4500);}
  function resetAuto(){clearInterval(timer);autoSlide();}
  show(0);autoSlide();

  document.querySelectorAll('.back-to-home').forEach(el=>
    el.onclick = e => { document.getElementById("homeContent").style.display="block";
                        document.getElementById("productsContent").style.display="none"; }
  );
  window.showHome = function(){
    document.getElementById("homeContent").style.display="block";
    document.getElementById("productsContent").style.display="none";
  }
  window.showProducts = function(){
    document.getElementById("homeContent").style.display="none";
    document.getElementById("productsContent").style.display="block";
  }
});
const sideMenu = document.getElementById("sideMenu");
const purchasesPanel = document.getElementById("purchasesPanel");
let cart = [];
function toggleMenu() {if (sideMenu.style.width === "200px") {closeMenu();} else {sideMenu.style.width = "200px";}}
function closeMenu() {sideMenu.style.width = "0";}
function openPurchasesPanel() {purchasesPanel.style.width = "260px";updateCartUI();}
function closePurchasesPanel() {purchasesPanel.style.width = "0";}
function performSearch() {}
function addToCart(id, name, price) {
  const existing = cart.find(item => item.id === id);
  if (existing) {
    existing.quantity += 1;
  } else {
    cart.push({ id, name, price, quantity: 1 });
  }
  updateCartUI();
}
function updateCartUI() {
  const cartItemsContainer = document.getElementById('cartItems');
  const cartTotalDisplay = document.getElementById('cartTotal');
  cartItemsContainer.innerHTML = "";
  cart.forEach((item, index) => {
    const li = document.createElement('li');
    li.textContent = `${item.name} x ${item.quantity} - $${item.price * item.quantity}`;
    const removeBtn = document.createElement('button');
    removeBtn.textContent = "Remove";
    removeBtn.onclick = () => {
      cart.splice(index, 1);
      updateCartUI();
    };
    li.appendChild(removeBtn);
    cartItemsContainer.appendChild(li);
  });
  cartTotalDisplay.textContent = "Total: $" + cart.reduce((sum, item) => sum + item.price * item.quantity, 0);
}
function openCheckout() {
  if(cart.length === 0){
    alert("Your cart is empty.");
    return;
  }
  let total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0);
  document.getElementById("orderTotal").textContent = total;
  document.getElementById("checkoutModal").style.display = "block";
}
function closeCheckout() { document.getElementById("checkoutModal").style.display = "none"; }
document.getElementById("checkoutForm").addEventListener("submit", function(e) {
  e.preventDefault();
  alert("Payment successful! Thank you for your purchase.");
  cart = [];
  updateCartUI();
  closeCheckout();
  closePurchasesPanel();
});
window.onclick = function(event) {
  const modal = document.getElementById("checkoutModal");
  if (event.target === modal) {
    closeCheckout();
  }
}
function triggerHeroAnimation() {
  const heroContent = document.querySelector('.hero-side');
  if(heroContent){
    heroContent.style.animation = 'none';
    void heroContent.offsetWidth;
    heroContent.style.animation = 'bounceIn 1s ease-out';
  }
}
window.addEventListener("hashchange", function() {
  if (location.hash === "#home") {
    triggerHeroAnimation();
  }
});
window.addEventListener("DOMContentLoaded", function() {
  if (!location.hash || location.hash === "#home") {
    showHome();
    triggerHeroAnimation();
  }
});
</script>
</body>
</html>
