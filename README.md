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

    /* Colour Scheme Variables */
    :root {
      --primary-bg: #0D1B2A;           /* Dark Blue Background */
      --header-footer-bg: #0A192F;      /* Slightly darker blue for header, footer & side panels */
      --text-color: #FFFFFF;           /* White text */
      --accent: #FFA500;               /* Bold orange accent */
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--primary-bg);
      color: var(--text-color);
      line-height: 1.6;
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
      text-decoration: none;
      font-size: 1.2rem;
      color: var(--text-color);
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
      color: var(--text-color);
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
      z-index: 1000;
      top: 0;
      right: 0;
      background-color: var(--header-footer-bg);
      color: var(--text-color);
      overflow-x: hidden;
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
    .open-purchases-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      background-color: var(--header-footer-bg);
      color: var(--text-color);
      border: none;
      font-size: 24px;
      padding: 8px;
      cursor: pointer;
      z-index: 1100;
    }

    /* ------------------------------
              Main Content
    ------------------------------*/
    .main-content {
      padding: 20px;
      transition: margin-left 0.5s, margin-right 0.5s;
    }

    /* Hero Section */
    .hero {
      position: relative;
      background-image: url('your-hero-image.jpg'); /* Replace with your hero image */
      background-size: cover;
      background-position: center;
      padding: 4rem 2rem;
      min-height: 90vh;
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
    }
    .full-logo {
      display: block;
      max-width: 200px;
      margin: 0 auto 20px auto;
    }
    .hero h2 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 1rem;
    }

    /* Optional decorative images in hero */
    .design-image {
      position: absolute;
      opacity: 0.9;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      z-index: 1;
    }
    .design-image.img1 { top: 30%; left: 5%; width: 80px; }
    .design-image.img2 { top: 30%; right: 5%; width: 80px; }
    .design-image.img3 { bottom: 10%; left: 10%; width: 80px; }
    .design-image.img4 { bottom: 15%; right: 8%; width: 80px; }
    .design-image.img5 { top: 50%; left: 0%; width: 80px; }
    .design-image.img6 { bottom: 20%; right: 0%; width: 80px; }

    /* Design Process Section */
    .design-process {
      padding: 4rem 2rem;
      text-align: center;
      background-color: var(--primary-bg);
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
    }
    .process-steps .step:hover {
      transform: translateY(-5px);
    }
    .step-number {
      background-color: var(--accent);
      color: var(--text-color);
      border-radius: 50%;
      width: 40px;
      height: 40px;
      line-height: 40px;
      margin: 0 auto 0.5rem auto;
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
      background-color: var(--primary-bg);
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
    }
    .package-item:hover {
      transform: translateY(-5px);
    }
    .package-item h3 {
      margin-bottom: 0.5rem;
    }

    /* Freelance Banner Section with Search */
    .freelance-banner {
      padding: 4rem 2rem;
      text-align: center;
      background-color: var(--header-footer-bg);
      color: var(--text-color);
    }
    .freelance-banner .banner-content {
      max-width: 800px;
      margin: 0 auto;
    }
    .freelance-banner h2 {
      font-size: 2.5rem;
      margin-bottom: 1.5rem;
    }
    .search-container {
      display: flex;
      justify-content: center;
      margin-bottom: 1rem;
    }
    .search-container input[type="text"] {
      padding: 0.5rem;
      width: 60%;
      border: none;
      border-radius: 4px 0 0 4px;
    }
    .search-container button {
      padding: 0.5rem 1rem;
      border: none;
      background-color: var(--accent);
      color: var(--text-color);
      border-radius: 0 4px 4px 0;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .search-container button:hover {
      background-color: #e69500;
    }
    /* Search Results Styling */
    #searchResults {
      max-width: 800px;
      margin: 20px auto;
      text-align: left;
    }
    .search-result {
      background-color: var(--header-footer-bg);
      margin: 10px 0;
      padding: 10px;
      border-radius: 4px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .search-result button {
      background-color: var(--accent);
      border: none;
      color: var(--text-color);
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .search-result button:hover {
      background-color: #e69500;
    }

    /* Previews Section (changed from Our Products) */
    #previews {
      padding: 4rem 0;
    }
    #previews h2 {
      text-align: center;
      margin-bottom: 2rem;
      font-size: 2.5rem;
    }
    .portfolio-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
    }
    .portfolio-item {
      width: 300px;
      background-color: #FFFFFF;
      color: #000;
      border: 1px solid #ddd;
      overflow: hidden;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
      text-align: center;
    }
    .portfolio-item:hover {
      transform: translateY(-5px);
    }
    .portfolio-item img,
    .portfolio-item video,
    .portfolio-item embed {
      width: 100%;
      display: block;
    }
    .portfolio-item h3 {
      padding: 1rem;
      font-size: 1.5rem;
    }

    /* Contact Section */
    #contact {
      padding: 4rem 0;
      text-align: center;
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
      color: var(--text-color);
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
      color: var(--text-color);
    }

    /* Checkout Modal Styles */
    .modal {
      display: none; /* Hidden by default */
      position: fixed; 
      z-index: 2000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0,0,0,0.8);
    }
    .modal-content {
      background-color: #fefefe;
      margin: 10% auto;
      padding: 20px;
      border: 1px solid #888;
      width: 90%;
      max-width: 500px;
      color: #000;
      border-radius: 8px;
    }
    .modal .close {
      color: #aaa;
      float: right;
      font-size: 28px;
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
      .design-image {
        width: 60px;
      }
      .design-image.img1 { top: 5%; left: 5%; }
      .design-image.img2 { top: 5%; right: 5%; }
      .design-image.img3 { bottom: 5%; left: 5%; }
      .design-image.img4 { bottom: 5%; right: 5%; }
      .design-image.img5,
      .design-image.img6 { display: none; }
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
  <!-- Side Navigation Menu (Hidden by default) -->
  <div id="sideMenu">
    <span class="close-btn" onclick="closeMenu()">&times;</span>
    <a href="#home" onclick="closeMenu()">Home</a>
    <a href="#design-process" onclick="closeMenu()">Process</a>
    <a href="#popular-services" onclick="closeMenu()">Services</a>
    <a href="#design-packages" onclick="closeMenu()">Packages</a>
    <a href="#freelance-banner" onclick="closeMenu()">Freelance</a>
    <a href="#previews" onclick="closeMenu()">Previews</a>
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
      <button onclick="openCheckout()" style="padding: 10px 20px; margin-top: 10px; background-color: var(--accent); border: none; color: var(--text-color); cursor: pointer; border-radius: 4px;">Checkout</button>
    </div>
  </div>

  <!-- Buttons to open side panels -->
  <button class="open-menu-btn" onclick="openMenu()">&#9776;</button>
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
        <button type="submit" style="padding: 10px 20px; background-color: var(--accent); border: none; color: var(--text-color); cursor: pointer; border-radius: 4px;">Submit Payment</button>
      </form>
    </div>
  </div>

  <!-- Main Content -->
  <div class="main-content">
    <!-- Hero Section -->
    <section id="home" class="hero">
      <div class="hero-content">
        <img src="Kt8o8usihonWLJtAAj5o6.png" alt="Full Logo" class="full-logo" />
        <h2>Creativity in Every Pixel</h2>
        <p>
          At RYT DESIGNS, we transform your vision into immersive design experiences.
        </p>
        <p>
          Explore our process, services, packages, previews, and more to see how we bring creativity to life.
        </p>
      </div>
      <!-- Optional Decorative Images -->
      <!--
      <img src="packaging.jpg" alt="Packaging Design" class="design-image img1">
      <img src="tshirt.jpg" alt="T-Shirt Design" class="design-image img2">
      <img src="logo.jpg" alt="Logo Design" class="design-image img3">
      <img src="poster.jpg" alt="Poster Design" class="design-image img4">
      <img src="brochure.jpg" alt="Brochure Design" class="design-image img5">
      <img src="packaging2.jpg" alt="Packaging Design 2" class="design-image img6">
      -->
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
          <p>Get print-ready designs in one go.</p>
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

    <!-- Freelance Banner Section with Search for Services -->
    <section id="freelance-banner" class="freelance-banner">
      <div class="banner-content">
        <h2>Search for Services</h2>
        <div class="search-container">
          <input type="text" id="serviceSearch" placeholder="Search services..." />
          <button id="searchBtn" type="button">Search</button>
        </div>
        <div id="searchResults"></div>
        <p style="margin-top: 1rem;">Available services: Presentations, Posters/Flyers, Videos for Events, Business Cards, Invitations, Logos for Businesses, YouTube Thumbnails (Basic &amp; Add-ons), Celebration Cards, Menus, Banner.</p>
      </div>
    </section>

    <!-- Previews Section (changed from Our Products) -->
    <section id="previews">
      <h2>Previews</h2>
      <div class="portfolio-container">
        <div class="portfolio-item">
          <a href="website prototype/ryt designs video.mp4" target="_blank">
            <img src="website prototype/ryt designs video.mp4" alt="Event Videos" />
          </a>
          <h3>Event Videos</h3>
        </div>
        <div class="portfolio-item">
          <a href="website prototype/ryt designs presentation.pdf" target="_blank">
            <img src="website prototype/ryt designs presentation.pdf" alt="Presentation" />
          </a>
          <h3>Presentation</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/A A itinerary.png" alt="Itinerary" />
          <h3>Itinerary</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/Banner 4 website.png" alt="Banner" />
          <h3>Banner</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/business card proto.jpg" alt="Business Card" />
          <h3>Business Card</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/celeb 4 website.png" alt="Birthday Card" />
          <h3>Birthday Card</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/invitation 4 website.png" alt="Invitation" />
          <h3>Invitation</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/Logo 4 website.png" alt="Logo" />
          <h3>Logo</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/Menu 4 website.png" alt="Menu" />
          <h3>Menu</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/youtube thumbnail 4 website.png" alt="YouTube Thumbnail" />
          <h3>YouTube Thumbnail</h3>
        </div>
        <div class="portfolio-item">
          <img src="website prototype/website.png" alt="Website Prototype" />
          <h3>Website Prototype</h3>
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
          <p>
            <strong>Email:</strong>
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
      <p><a href="#home" class="back-to-home">Back to Home</a></p>
    </footer>
  </div>

  <!-- JavaScript for Functionality -->
  <script>
    // Side Menu Functions
    function openMenu() {
      document.getElementById("sideMenu").style.width = "250px";
    }
    function closeMenu() {
      document.getElementById("sideMenu").style.width = "0";
    }

    // Purchases Panel (Cart) Functions
    function openPurchasesPanel() {
      document.getElementById("purchasesPanel").style.width = "300px";
      updateCartUI();
    }
    function closePurchasesPanel() {
      document.getElementById("purchasesPanel").style.width = "0";
    }

    // Global Cart Array
    let cart = [];

    // Services Database for Search
    const services = [
      { name: "Posters/Flyers", price: 15 },
      { name: "Videos for Events", price: 25 },
      { name: "Business Cards", price: 20 },
      { name: "Invitations", price: 24 },
      { name: "Logos for Businesses", price: 30 },
      { name: "YouTube Thumbnails (Basic)", price: 20 },
      { name: "YouTube Thumbnails (Add-ons)", price: 35 },
      { name: "Celebration Cards", price: 10 },
      { name: "Presentations", price: 30 },
      { name: "Menus", price: 20 },
      { name: "Banner", price: 35 }
    ];

    // Search Functionality
    document.getElementById('searchBtn').addEventListener('click', function() {
      const query = document.getElementById('serviceSearch').value.toLowerCase().trim();
      const resultsContainer = document.getElementById('searchResults');
      resultsContainer.innerHTML = "";
      if(query === ""){
        resultsContainer.innerHTML = "<p>Please enter a search term.</p>";
        return;
      }
      const results = services.filter(item => item.name.toLowerCase().includes(query));
      if(results.length === 0){
        resultsContainer.innerHTML = "<p>No services found.</p>";
        return;
      }
      results.forEach(item => {
        const resultDiv = document.createElement('div');
        resultDiv.className = "search-result";
        resultDiv.innerHTML = `<span>${item.name} - $${item.price}</span>
          <button onclick='addToCart("${item.name}", ${item.price})'>Buy</button>`;
        resultsContainer.appendChild(resultDiv);
      });
    });

    // Add to Cart Function
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

    // Update Cart UI
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

    // Checkout Modal Functions
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

    // Handle Checkout Form Submission
    document.getElementById("checkoutForm").addEventListener("submit", function(e) {
      e.preventDefault();
      alert("Payment successful! Thank you for your purchase.");
      cart = [];
      updateCartUI();
      closeCheckout();
      closePurchasesPanel();
    });
  </script>
</body>
</html>
