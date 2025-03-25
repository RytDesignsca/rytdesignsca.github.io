<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="RYT DESIGNS - Creativity in Every Pixel." />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>RYT DESIGNS</title>
  <style>
    /* Global Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* New Color Scheme: white, black, gray with teal accents */
    :root {
      --primary-bg: #ffffff;            /* Main background (white) */
      --secondary-bg: #f7f7f7;           /* Light gray for some sections */
      --header-footer-bg: #333333;       /* Dark gray for navigation and footer */
      --text-color: #000000;             /* Text color (black) */
      --inverse-text-color: #ffffff;     /* For text on dark backgrounds */
      --accent: #008080;                 /* Teal accent */
    }

    body {
      background-color: var(--primary-bg);
      color: var(--text-color);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
    }

    a {
      color: var(--accent);
      text-decoration: none;
    }

    /* ------------------------------
         Side Navigation Menu (Left)
    ------------------------------*/
    #sideMenu {
      height: 100%;
      width: 0;
      position: fixed;
      z-index: 1000;
      top: 0;
      left: 0;
      background-color: var(--header-footer-bg);
      overflow-x: hidden;
      transition: 0.5s;
      padding-top: 60px;
    }
    #sideMenu a {
      padding: 10px 10px 10px 30px;
      font-size: 1.2rem;
      color: var(--inverse-text-color);
      display: block;
      transition: color 0.3s ease;
    }
    #sideMenu a:hover {
      color: var(--accent);
    }
    #sideMenu .close-btn {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 30px;
      cursor: pointer;
    }
    .open-menu-btn {
      position: fixed;
      top: 20px;
      left: 20px;
      background-color: var(--header-footer-bg);
      color: var(--inverse-text-color);
      border: none;
      font-size: 24px;
      padding: 8px;
      cursor: pointer;
      z-index: 1100;
    }

    /* ------------------------------
         Purchases Panel (Right - Cart)
    ------------------------------*/
    #purchasesPanel {
      height: 100%;
      width: 0;
      position: fixed;
      z-index: 2000;
      top: 0;
      right: 0;
      background-color: var(--header-footer-bg);
      color: var(--inverse-text-color);
      overflow-y: auto;
      transition: 0.5s;
      padding-top: 60px;
    }
    #purchasesPanel .close-btn {
      position: absolute;
      top: 10px;
      left: 20px;
      font-size: 30px;
      cursor: pointer;
    }
    #purchasesPanel h2 {
      text-align: center;
    }
    .open-purchases-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      background-color: var(--header-footer-bg);
      color: var(--inverse-text-color);
      border: none;
      font-size: 24px;
      padding: 8px;
      cursor: pointer;
      z-index: 2100;
    }

    /* ------------------------------
              Main Content
    ------------------------------*/
    .main-content {
      padding: 20px;
      transition: margin-left 0.5s;
    }

    /* Hero Section (Home) */
    .hero {
      position: relative;
      background-color: var(--primary-bg);
      padding: 4rem 2rem;
      min-height: 60vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      overflow: hidden;
    }
    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 800px;
      margin: 0 auto;
      padding: 0 1rem;
      /* Bounce-in animation – retrigger on every visit */
      animation: bounceIn 1s ease-out;
    }
    .full-logo {
      display: block;
      max-width: 200px;
      margin: 0 auto 20px;
    }
    .hero h2 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 1rem;
    }

    /* Bounce-in animation for hero content */
    @keyframes bounceIn {
      0% {
        transform: scale(0.5);
        opacity: 0;
      }
      60% {
        transform: scale(1.2);
        opacity: 1;
      }
      80% {
        transform: scale(0.9);
      }
      100% {
        transform: scale(1);
      }
    }

    /* New Search Bar (in Hero) */
    .hero .search-container {
      display: flex;
      align-items: center;
      width: 100%;
      max-width: 600px;
      margin: 1.5rem auto 0;
      background-color: #000000;
      border: 1px solid gray;
      border-radius: 5px;
      padding: 5px;
    }
    .hero .search-container input[type="text"] {
      flex-grow: 1;
      padding: 10px;
      border: none;
      outline: none;
      font-size: 16px;
      color: #555;
    }
    .hero .search-container button {
      background-color: #000000;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }
    .hero .search-container button:hover {
      background-color: #222222;
    }
    /* Inline SVG for a small teal magnifying glass */
    .hero .search-container button svg {
      display: block;
    }

    /* Search Results (in Hero) */
    .hero #searchResults {
      max-width: 800px;
      margin: 1rem auto 0;
      text-align: left;
    }
    .hero .search-result {
      background-color: var(--header-footer-bg);
      margin: 10px 0;
      padding: 10px;
      border-radius: 4px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: var(--inverse-text-color);
    }
    .hero .search-result button {
      background-color: var(--accent);
      border: none;
      color: var(--inverse-text-color);
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .hero .search-result button:hover {
      background-color: darkcyan;
    }
    .hero .search-result .preview-button {
      margin-left: 10px;
      background-color: gray;
      color: var(--inverse-text-color);
      border: none;
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .hero .search-result .preview-button:hover {
      background-color: darkgray;
    }

    /* Design Process Section */
    .design-process {
      padding: 4rem 2rem;
      text-align: center;
      background-color: var(--secondary-bg);
    }
    .design-process h2 {
      font-size: 2.5rem;
      margin-bottom: 2rem;
    }
    .process-steps {
      display: flex;
      justify-content: center;
      gap: 2rem;
    }
    .process-steps .step {
      background-color: var(--header-footer-bg);
      padding: 1rem;
      border-radius: 8px;
      width: 120px;
      transition: transform 0.3s ease;
      color: var(--inverse-text-color);
    }
    .process-steps .step:hover {
      transform: translateY(-5px);
    }
    .step-number {
      background-color: var(--accent);
      color: var(--inverse-text-color);
      border-radius: 50%;
      width: 40px;
      height: 40px;
      line-height: 40px;
      margin: 0 auto 0.5rem;
      font-weight: bold;
    }

    /* Popular Services Section */
    .popular-services {
      padding: 4rem 2rem;
      text-align: center;
      background-color: var(--primary-bg);
    }
    .popular-services h2 {
      font-size: 2.5rem;
      margin-bottom: 2rem;
    }
    .services-boxes {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
    }
    .service-box {
      background-color: var(--header-footer-bg);
      padding: 1rem;
      border-radius: 8px;
      width: 180px;
      transition: transform 0.3s ease;
      text-align: center;
      color: var(--inverse-text-color);
    }
    .service-box:hover {
      transform: translateY(-5px);
    }
    .service-box img {
      width: 60px;
      height: 60px;
      margin-bottom: 0.5rem;
    }

    /* Design Packages Section */
    .design-packages {
      padding: 4rem 2rem;
      text-align: center;
      background-color: var(--secondary-bg);
    }
    .design-packages h2 {
      font-size: 2.5rem;
      margin-bottom: 2rem;
    }
    .packages {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
    }
    .package-item {
      background-color: var(--header-footer-bg);
      padding: 1rem;
      border-radius: 8px;
      width: 220px;
      transition: transform 0.3s ease;
      color: var(--inverse-text-color);
    }
    .package-item:hover {
      transform: translateY(-5px);
    }
    .package-item h3 {
      margin-bottom: 0.5rem;
    }

    /* Preview Section */
    #preview {
      padding: 4rem 2rem;
      text-align: center;
      background-color: var(--primary-bg);
      display: none;  /* Hidden by default */
    }
    /* When preview section is shown, we now include a header title */
    #preview h2 {
      font-size: 2.5rem;
      margin-bottom: 2rem;
      text-align: center;
    }
    .portfolio-container {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      justify-content: center;
      text-align: center;
    }
    .portfolio-item {
      background-color: var(--header-footer-bg);
      padding: 1rem;
      border-radius: 8px;
      flex: 1 1 200px;
      transition: transform 0.3s ease;
      margin: 0.5rem;
      color: var(--inverse-text-color);
    }
    .portfolio-item:hover {
      transform: translateY(-5px);
    }
    .portfolio-item img {
      max-width: 100%;
      border-radius: 4px;
      margin-bottom: 0.5rem;
    }
    .portfolio-item a {
      color: var(--accent);
      text-decoration: none;
    }
    .show-all-btn {
      margin: 1rem auto;
      padding: 0.5rem 1rem;
      background-color: var(--accent);
      border: none;
      color: var(--inverse-text-color);
      cursor: pointer;
      border-radius: 4px;
      display: none; /* Only shown when filtering previews */
    }

    /* Toggle Previews Button – more attractive styling */
    #togglePreviewsBtn {
      display: block;
      margin: 2rem auto;
      padding: 0.75rem 1.5rem;
      background: linear-gradient(135deg, var(--accent), #00a3a3);
      border: none;
      color: var(--inverse-text-color);
      font-size: 1.2rem;
      font-weight: bold;
      cursor: pointer;
      border-radius: 8px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    #togglePreviewsBtn:hover {
      transform: scale(1.05);
      box-shadow: 0 4px 8px rgba(0, 128, 128, 0.4);
    }

    /* Contact Section */
    #contact {
      padding: 4rem 0;
      text-align: center;
      background-color: var(--primary-bg);
    }
    .contact-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
      padding: 0 1rem;
    }
    .contact-info {
      margin-bottom: 2rem;
      font-size: 1.2rem;
      text-align: center;
    }
    .contact-info p {
      margin: 0.5rem 0;
    }
    .social-links {
      display: flex;
      justify-content: center;
      gap: 1rem;
    }
    .social-links a {
      color: var(--accent);
      font-size: 1.5rem;
      transition: color 0.3s ease;
      text-decoration: none;
    }
    .social-links a:hover {
      color: var(--accent);
    }

    /* Footer */
    footer {
      background-color: var(--header-footer-bg);
      text-align: center;
      padding: 1rem 0;
      color: var(--inverse-text-color);
    }
    footer p {
      margin-bottom: 0.5rem;
    }
    footer a.back-to-home {
      color: var(--accent);
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s ease;
    }
    footer a.back-to-home:hover {
      color: var(--inverse-text-color);
    }

    /* Checkout Modal */
    .modal {
      display: none; 
      position: fixed; 
      z-index: 3000; 
      left: 0;
      top: 0;
      width: 100%; 
      height: 100%; 
      overflow: auto; 
      background-color: rgba(0,0,0,0.5); 
    }
    .modal-content {
      background-color: var(--header-footer-bg);
      margin: 10% auto;
      padding: 20px;
      border: 1px solid #888;
      width: 80%;
      max-width: 500px;
      border-radius: 8px;
      position: relative;
      color: var(--inverse-text-color);
    }
    .modal-content .close {
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 30px;
      font-weight: bold;
      cursor: pointer;
    }

    /* Responsive Styles */
    @media (max-width: 768px) {
      .hero h2 {
        font-size: 2.5rem;
      }
      .hero p {
        font-size: 1rem;
      }
      .full-logo {
        max-width: 150px;
        margin-bottom: 15px;
      }
    }
    @media (max-width: 480px) {
      .hero h2 {
        font-size: 2rem;
      }
      .hero p {
        font-size: 0.9rem;
      }
      #sideMenu a {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <!-- Side Navigation Menu -->
  <div id="sideMenu">
    <span class="close-btn" onclick="closeMenu()">&times;</span>
    <!-- "Home" now also triggers the hero animation -->
    <a href="#home" onclick="closeMenu(); triggerHeroAnimation();">Home</a>
    <a href="#design-process" onclick="closeMenu()">Process</a>
    <a href="#popular-services" onclick="closeMenu()">Services</a>
    <a href="#design-packages" onclick="closeMenu()">Packages</a>
    <!-- The "Previews" link toggles the preview section -->
    <a href="javascript:void(0)" onclick="togglePreviews(); closeMenu();">Previews</a>
    <a href="#contact" onclick="closeMenu()">Contact</a>
    <a href="javascript:void(0)" onclick="openPurchasesPanel(); closeMenu();">Purchases</a>
  </div>

  <!-- Purchases Panel (Cart) -->
  <div id="purchasesPanel">
    <span class="close-btn" onclick="closePurchasesPanel()">&times;</span>
    <div style="padding: 20px;">
      <h2>Your Cart</h2>
      <ul id="cartItems"></ul>
      <p id="cartTotal"></p>
      <button onclick="openCheckout()" style="padding: 10px 20px; margin-top: 10px; background-color: var(--accent); border: none; color: var(--inverse-text-color); cursor: pointer; border-radius: 4px;">Checkout</button>
    </div>
  </div>

  <!-- Hamburger Menu Buttons -->
  <button class="open-menu-btn" onclick="toggleMenu()">&#9776;</button>
  <button class="open-purchases-btn" onclick="openPurchasesPanel()">&#128722;</button>

  <!-- Checkout Modal -->
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

  <!-- Main Content -->
  <div class="main-content">
    <!-- Hero Section (Home) -->
    <section id="home" class="hero">
      <div class="hero-content">
        <img src="Kt8o8usihonWLJtAAj5o6.png" alt="Full Logo" class="full-logo" />
        <h2>Creativity in Every Pixel</h2>
        <p>At RYT DESIGNS, we transform your vision into immersive design experiences.</p>
        <p>Explore our process, services, packages, and more.</p>

        <!-- Product Search integrated into Home -->
        <div class="search-container">
          <input type="text" id="serviceSearch" placeholder="Search for any service..." />
          <button id="searchBtn" type="button">
            <!-- Inline SVG for a small teal magnifying glass -->
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="#008080" viewBox="0 0 16 16">
              <path d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001l3.85 3.85a1 1 0 0 0 1.414-1.414l-3.85-3.85zM6.5 11a4.5 4.5 0 1 1 0-9 4.5 4.5 0 0 1 0 9z"/>
            </svg>
          </button>
        </div>
        <div id="searchResults"></div>
      </div>
    </section>

    <!-- Design Process Section -->
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

    <!-- Popular Services Section -->
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
          <img src="social-media-icon.png" alt="Social Media Marketing" />
          <h3>Social Media</h3>
        </div>
      </div>
    </section>

    <!-- Design Packages Section -->
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

    <!-- Toggle Previews Button -->
    <button id="togglePreviewsBtn" onclick="togglePreviews()">Show Previews</button>

    <!-- Preview Section (hidden by default) -->
    <section id="preview">
      <!-- We now include a header title for the preview section -->
      <h2>Previews</h2>
      <button class="show-all-btn" id="showAllBtn" onclick="showAllPreviews()">Show All Previews</button>
      <div class="portfolio-container">
        <!-- Portfolio items – displayed as pictures -->
        <div class="portfolio-item" id="product-event-videos">
          <a href="website prototype/ryt designs video.mp4" target="_blank">
            <img src="website prototype/ryt designs video.mp4" alt="Event Videos">
          </a>
          <h3>Event Videos</h3>
        </div>
        <div class="portfolio-item" id="product-presentation">
          <a href="website prototype/ryt designs presentation.pdf" target="_blank">
            <img src="website prototype/ryt designs presentation.pdf" alt="Presentation">
          </a>
          <h3>Presentation</h3>
        </div>
        <div class="portfolio-item" id="product-itinerary">
          <img src="website prototype/A A itinerary.png" alt="Itinerary">
          <h3>Itinerary</h3>
        </div>
        <div class="portfolio-item" id="product-banner">
          <img src="website prototype/Banner 4 website.png" alt="Banner">
          <h3>Banner</h3>
        </div>
        <div class="portfolio-item" id="product-business-card">
          <img src="website prototype/business card proto.jpg" alt="Business Card">
          <h3>Business Card</h3>
        </div>
        <div class="portfolio-item" id="product-birthday-card">
          <img src="website prototype/celeb 4 website.png" alt="Birthday Card">
          <h3>Birthday Card</h3>
        </div>
        <div class="portfolio-item" id="product-invitation">
          <img src="website prototype/invitation 4 website.png" alt="Invitation">
          <h3>Invitation</h3>
        </div>
        <div class="portfolio-item" id="product-logo">
          <img src="website prototype/Logo 4 website.png" alt="Logo">
          <h3>Logo</h3>
        </div>
        <div class="portfolio-item" id="product-menu">
          <img src="website prototype/Menu 4 website.png" alt="Menu">
          <h3>Menu</h3>
        </div>
        <div class="portfolio-item" id="product-youtube-thumbnail">
          <img src="website prototype/youtube thumbnail 4 website.png" alt="YouTube Thumbnail">
          <h3>YouTube Thumbnail</h3>
        </div>
        <div class="portfolio-item" id="product-website-prototype">
          <img src="website prototype/website.png" alt="Website Prototype">
          <h3>Website Prototype</h3>
        </div>
        <div class="portfolio-item" id="product-poster-flyer">
          <h3>Poster/Flyer</h3>
        </div>
        <div class="portfolio-item" id="product-videos-for-events">
          <h3>Videos for events</h3>
        </div>
        <div class="portfolio-item" id="product-logos-for-businesses">
          <h3>Logos for businesses</h3>
        </div>
        <div class="portfolio-item" id="product-youtube-thumbnail-basic">
          <h3>YouTube Thumbnails(Basic)</h3>
        </div>
        <div class="portfolio-item" id="product-youtube-thumbnail-add-ons">
          <h3>YouTube Thumbnail(Add-ons)</h3>
        </div>
        <div class="portfolio-item" id="product-celebration-cards">
          <h3>Celebration cards</h3>
        </div>
        <div class="portfolio-item" id="product-presentations">
          <h3>Presentations</h3>
        </div>
        <div class="portfolio-item" id="product-menus">
          <h3>Menus</h3>
        </div>
        <div class="portfolio-item" id="product-banner-design">
          <h3>Banner</h3>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
      <h2>Get in Touch</h2>
      <div class="contact-container">
        <div class="contact-info">
          <p><strong>Phone:</strong> +1 226-977-9311</p>
          <p><strong>Alternate Phone:</strong> +1 226-977-9310</p>
          <p><strong>Email:</strong>
            <a href="mailto:rytdesignsca@gmail.com" style="color: var(--accent);">
              rytdesignsca@gmail.com
            </a>
          </p>
        </div>
        <div class="social-links">
          <a href="https://www.instagram.com/rytdesigns_/" target="_blank">Instagram</a>
          <a href="https://www.tiktok.com/@ryt.designs7" target="_blank">TikTok</a>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer>
      <p>&copy; 2025 RYT DESIGNS. All Rights Reserved.</p>
      <p>Designed by RYT DESIGNS</p>
      <p><a href="#home" class="back-to-home" onclick="triggerHeroAnimation()">Back to Home</a></p>
    </footer>
  </div>

  <!-- JavaScript for Interactions -->
  <script>
    // Side Menu functions
    const sideMenu = document.getElementById("sideMenu");
    const mainContent = document.querySelector(".main-content");
    const purchasesPanel = document.getElementById("purchasesPanel");

    function toggleMenu() {
      if (sideMenu.style.width === "250px") {
        closeMenu();
      } else {
        sideMenu.style.width = "250px";
      }
    }
    function closeMenu() {
      sideMenu.style.width = "0";
    }

    // Purchases Panel (Cart) functions
    function openPurchasesPanel() {
      purchasesPanel.style.width = "300px";
      updateCartUI();
    }
    function closePurchasesPanel() {
      purchasesPanel.style.width = "0";
    }

    // Global Cart array
    let cart = [];

    // Enhanced Search Functionality integrated in the hero section
    document.getElementById('searchBtn').addEventListener('click', performSearch);
    document.getElementById('serviceSearch').addEventListener('keypress', function(event) {
      if (event.key === 'Enter') {
        event.preventDefault();
        performSearch();
      }
    });
    function performSearch() {
      const query = document.getElementById('serviceSearch').value.toLowerCase().trim();
      const resultsContainer = document.getElementById('searchResults');
      resultsContainer.innerHTML = "";
      if(query === ""){
        return;
      }
      const queryTerms = query.split(/\s+/).filter(term => term.length > 0);
      const products = [
        { name: "Poster/Flyer", price: 15, id: "product-poster-flyer" },
        { name: "Videos for events", price: 25, id: "product-videos-for-events" },
        { name: "Business cards", price: 20, id: "product-business-card" },
        { name: "Invitations", price: 24, id: "product-invitation" },
        { name: "Logos for businesses", price: 30, id: "product-logos-for-businesses" },
        { name: "YouTube Thumbnails(Basic)", price: 20, id: "product-youtube-thumbnail-basic" },
        { name: "YouTube Thumbnail(Add-ons)", price: 35, id: "product-youtube-thumbnail-add-ons" },
        { name: "Celebration cards", price: 10, id: "product-celebration-cards" },
        { name: "Presentations", price: 30, id: "product-presentations" },
        { name: "Menus", price: 20, id: "product-menu" },
        { name: "Banner", price: 35, id: "product-banner-design" },
        { name: "Event Videos", price: 25, id: "product-event-videos" },
        { name: "Presentation", price: 30, id: "product-presentation" },
        { name: "Itinerary", price: 10, id: "product-itinerary" },
        { name: "Business Card", price: 20, id: "product-business-card" },
        { name: "Birthday Card", price: 15, id: "product-birthday-card" },
        { name: "Invitation", price: 24, id: "product-invitation" },
        { name: "Logo", price: 30, id: "product-logo" },
        { name: "Menu", price: 20, id: "product-menu" },
        { name: "YouTube Thumbnail", price: 20, id: "product-youtube-thumbnail" },
        { name: "Website Prototype", price: 50, id: "product-website-prototype" }
      ];
      
      let results = [];
      products.forEach(item => {
        let score = 0;
        const nameLower = item.name.toLowerCase();
        queryTerms.forEach(term => {
          if(nameLower.includes(term)){
            score++;
          }
        });
        if(score > 0) {
          results.push({...item, score});
        }
      });
      
      results.sort((a, b) => b.score - a.score);
      
      if(results.length === 0){
        resultsContainer.innerHTML = "<p>No products found.</p>";
        return;
      }
      
      results.forEach(item => {
        // Use a button for the preview link instead of an anchor
        const resultDiv = document.createElement('div');
        resultDiv.className = "search-result";
        resultDiv.innerHTML = `<span>${item.name} - $${item.price}</span>
          <button onclick='addToCart("${item.name}", ${item.price})'>Buy</button>
          <button type="button" class="preview-button" onclick="showOnlyPreview('${item.id}')">Preview</button>`;
        resultsContainer.appendChild(resultDiv);
      });
    }

    // Add to Cart function
    function addToCart(name, price) {
      const existing = cart.find(item => item.name === name);
      if(existing){
        existing.quantity += 1;
      } else {
        cart.push({ name, price, quantity: 1 });
      }
      alert(name + " has been added to your cart.");
      updateCartUI();
    }

    // Update Cart UI function
    function updateCartUI() {
      const cartItemsContainer = document.getElementById('cartItems');
      const cartTotalDisplay = document.getElementById('cartTotal');
      cartItemsContainer.innerHTML = "";
      let total = 0;
      cart.forEach(item => {
        total += item.price * item.quantity;
        const li = document.createElement('li');
        li.textContent = `${item.name} x ${item.quantity} - $${item.price * item.quantity}`;
        cartItemsContainer.appendChild(li);
      });
      cartTotalDisplay.textContent = "Total: $" + total;
    }

    // Checkout Modal functions
    function openCheckout() {
      if(cart.length === 0){
        alert("Your cart is empty.");
        return;
      }
      let total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0);
      document.getElementById("orderTotal").textContent = total;
      document.getElementById("checkoutModal").style.display = "block";
    }
    function closeCheckout() {
      document.getElementById("checkoutModal").style.display = "none";
    }
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

    // Preview Filtering Functions
    function showOnlyPreview(itemId) {
      const portfolioItems = document.querySelectorAll(".portfolio-item");
      portfolioItems.forEach(item => {
        item.style.display = (item.id === itemId) ? "block" : "none";
      });
      document.getElementById("showAllBtn").style.display = "block";
      document.getElementById("preview").scrollIntoView({ behavior: "smooth" });
    }
    function showAllPreviews() {
      const portfolioItems = document.querySelectorAll(".portfolio-item");
      portfolioItems.forEach(item => {
        item.style.display = "block";
      });
      document.getElementById("showAllBtn").style.display = "none";
    }

    // Toggle the entire preview section visibility and reset filtering
    function togglePreviews() {
      const previewSection = document.getElementById("preview");
      const toggleBtn = document.getElementById("togglePreviewsBtn");
      if (previewSection.style.display === "none" || previewSection.style.display === "") {
        previewSection.style.display = "block";
        toggleBtn.textContent = "Hide Previews";
      } else {
        previewSection.style.display = "none";
        toggleBtn.textContent = "Show Previews";
      }
      showAllPreviews();
    }

    // Trigger hero animation (reset and retrigger bounceIn)
    function triggerHeroAnimation() {
      const heroContent = document.querySelector('.hero-content');
      heroContent.style.animation = 'none';
      // Force reflow to reset animation
      void heroContent.offsetWidth;
      heroContent.style.animation = 'bounceIn 1s ease-out';
    }

    // On hash change to #home, trigger the hero animation
    window.addEventListener("hashchange", function() {
      if (location.hash === "#home") {
        triggerHeroAnimation();
      }
    });

    // On page load, if on #home (or no hash) trigger animation
    window.addEventListener("DOMContentLoaded", function() {
      if (!location.hash || location.hash === "#home") {
        triggerHeroAnimation();
      }
    });
  </script>
</body>
</html>
