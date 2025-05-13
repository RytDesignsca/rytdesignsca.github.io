
html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="RYT DESIGNS - Creativity in Every Pixel." />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>RYT DESIGNS</title>
  <style>
    /* --- All your existing CSS remains unchanged --- */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    :root {
      --primary-bg: #ffffff;
      --secondary-bg: #f7f7f7;
      --header-footer-bg: #333333;
      --text-color: #000000;
      --inverse-text-color: #ffffff;
      --accent: #008080;
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
    #sideMenu {height:100%;width:0;position:fixed;z-index:1000;top:0;left:0;background-color:var(--header-footer-bg);overflow-x:hidden;transition:0.5s;padding-top:60px;}
    #sideMenu a {padding:10px 10px 10px 30px;font-size:1.2rem;color:var(--inverse-text-color);display:block;transition:color .3s ease;}
    #sideMenu a:hover {color:var(--accent);}
    #sideMenu .close-btn {position:absolute;top:10px;right:20px;font-size:30px;cursor:pointer;}
    .open-menu-btn {position:fixed;top:20px;left:20px;background-color:var(--header-footer-bg);color:var(--inverse-text-color);border:none;font-size:24px;padding:8px;cursor:pointer;z-index:1100;}
    #purchasesPanel {height:100%;width:0;position:fixed;z-index:2000;top:0;right:0;background-color:var(--header-footer-bg);color:var(--inverse-text-color);overflow-y:auto;transition:0.5s;padding-top:60px;}
    #purchasesPanel .close-btn {position:absolute;top:10px;left:20px;font-size:30px;cursor:pointer;}
    #purchasesPanel h2 {text-align:center;}
    .open-purchases-btn {position:fixed;top:20px;right:20px;background-color:var(--header-footer-bg);color:var(--inverse-text-color);border:none;font-size:24px;padding:8px;cursor:pointer;z-index:2100;}
    .main-content {padding:20px;transition:margin-left 0.5s;}
    #productsContent {display:none;}
    /* --- HERO (NEW HOMEPAGE LAYOUT) --- */
    .hero {
      position: relative;
      background: linear-gradient(120deg, #e0fbfc 0 30%, #ffffff 100%);
      padding: 5rem 2rem 4rem 2rem;
      min-height: 68vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      overflow: hidden;
    }
    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 600px;
      margin: 0 auto;
      padding: 0 1rem;
      animation: bounceIn 1s ease-out;
    }
    .full-logo {
      display: block;
      max-width: 180px;
      margin: 0 auto 24px;
      filter: drop-shadow(0 0 8px #dde6e6);
    }
    .hero h2 {
      font-size: 2.7rem;
      font-weight: 700;
      color: #163d3c;
      margin-bottom: 1.2rem;
      line-height: 1.1;
      letter-spacing: -1px;
      text-shadow: 0 3px 8px rgba(0,0,0,0.03);
    }
    .hero .subtitle {
      color: #295c5b;
      font-size: 1.19rem;
      margin-bottom: 2rem;
      line-height: 1.6;
      opacity: 0.92;
    }
    .hero-buttons {
      margin: 2.5rem 0 0 0;
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
      justify-content: center;
    }
    .btn-primary, .btn-secondary {
      font-size: 1.04rem;
      padding: 13px 32px;
      cursor: pointer;
      border-radius: 30px;
      border: none;
      transition: background 0.22s, color 0.22s, box-shadow 0.22s;
      font-weight: 600;
      letter-spacing: 1px;
      margin: 0.2rem 0;
    }
    .btn-primary {
      background: var(--accent);
      color: #fff;
      box-shadow: 0 2px 12px rgba(0,128,128,0.06);
    }
    .btn-primary:hover { background: #005b5b; }
    .btn-secondary {
      background: #fff;
      color: var(--accent);
      border: 2px solid var(--accent);
    }
    .btn-secondary:hover {
      background: #e7f5f4;
      color: #005b5b;
    }
    .search-container {
      display: flex;
      align-items: center;
      width: 100%;
      max-width: 460px;
      margin: 2.5rem auto 0;
      background-color: #fff;
      border: 1px solid #c7e2e2;
      border-radius: 40px;
      padding: 5px 8px;
      box-shadow: 0 2px 8px rgba(0,128,128,0.04);
    }
    .search-container input[type="text"] {
      flex-grow: 1;
      padding: 13px 18px;
      border: none;
      outline: none;
      font-size: 1rem;
      color: #444;
      border-radius: 40px;
      background: transparent;
    }
    .search-container button {
      background-color: var(--accent);
      border: none;
      height: 42px;
      width: 42px;
      border-radius: 50%;
      cursor: pointer;
      margin-left: 3px;
      display: flex; align-items: center; justify-content: center;
    }
    .search-container button:hover { background: #005b5b; }
    .search-container button svg { fill: #fff; }
    #searchResults {
      max-width: 800px;
      margin: 1rem auto 0;
      text-align: left;
    }
    .popular-keywords {
      margin-top: 2.1rem;
      font-size: 0.98rem;
      color: #268989;
      opacity: 0.92;
    }
    .popular-keywords a { color: var(--accent); margin: 0 2px; }
    .popular-keywords a:hover { text-decoration: underline;}
    @keyframes bounceIn {
      0% { transform: scale(0.5); opacity: 0; }
      60% { transform: scale(1.12); opacity: 1; }
      80% { transform: scale(0.95); }
      100% { transform: scale(1);}
    }
    /* Remaining original styles unchanged! */
    .design-process {padding:4rem 2rem;text-align:center;background-color:var(--secondary-bg);}
    .design-process h2 {font-size:2.5rem;margin-bottom:2rem;}
    .process-steps {display:flex;justify-content:center;gap:2rem;}
    .process-steps .step {background-color:var(--header-footer-bg);padding:1rem;border-radius:8px;width:120px;transition:transform 0.3s ease;color:var(--inverse-text-color);}
    .process-steps .step:hover {transform:translateY(-5px);}
    .step-number {background-color:var(--accent);color:var(--inverse-text-color);border-radius:50%;width:40px;height:40px;line-height:40px;margin:0 auto 0.5rem;font-weight:bold;}
    .popular-services {padding:4rem 2rem;text-align:center;background-color:var(--primary-bg);}
    .popular-services h2 {font-size:2.5rem;margin-bottom:2rem;}
    .services-boxes {display:flex;flex-wrap:wrap;justify-content:center;gap:1rem;}
    .service-box {background-color:var(--header-footer-bg);padding:1rem;border-radius:8px;width:180px;transition:transform 0.3s ease;text-align:center;color:var(--inverse-text-color);}
    .service-box:hover {transform:translateY(-5px);}
    .service-box img {width:60px;height:60px;margin-bottom:0.5rem;}
    .design-packages {padding:4rem 2rem;text-align:center;background-color:var(--secondary-bg);}
    .design-packages h2 {font-size:2.5rem;margin-bottom:2rem;}
    .packages {display:flex;flex-wrap:wrap;justify-content:center;gap:1rem;}
    .package-item {background-color:var(--header-footer-bg);padding:1rem;border-radius:8px;width:220px;transition:transform 0.3s ease;color:var(--inverse-text-color);}
    .package-item:hover {transform:translateY(-5px);}
    .package-item h3 {margin-bottom:0.5rem;}
    #contact {padding:4rem 0;text-align:center;background-color:var(--primary-bg);}
    .contact-container {display:flex;flex-direction:column;align-items:center;gap:1rem;padding:0 1rem;}
    .contact-info {margin-bottom:2rem;font-size:1.2rem;text-align:center;}
    .contact-info p {margin:0.5rem 0;}
    .social-links {display:flex;justify-content:center;gap:1rem;}
    .social-links a {color:var(--accent);font-size:1.5rem;transition:color 0.3s ease;text-decoration:none;}
    .social-links a:hover {color:var(--accent);}
    footer {background-color:var(--header-footer-bg);text-align:center;padding:1rem 0;color:var(--inverse-text-color);}
    footer p {margin-bottom:0.5rem;}
    footer a.back-to-home {color:var(--accent);text-decoration:none;font-weight:bold;transition:color 0.3s ease;}
    footer a.back-to-home:hover {color:var(--inverse-text-color);}
    .modal {display:none;position:fixed;z-index:3000;left:0;top:0;width:100%;height:100%;overflow:auto;background-color:rgba(0,0,0,0.5);}
    .modal-content {background-color:var(--header-footer-bg);margin:10% auto;padding:20px;border:1px solid #888;width:80%;max-width:500px;border-radius:8px;position:relative;color:var(--inverse-text-color);}
    .modal-content .close {position:absolute;top:10px;right:20px;font-size:30px;font-weight:bold;cursor:pointer;}
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
    @media (max-width: 768px) {
      .hero h2 {font-size:2.1rem;}
      .hero .subtitle {font-size:1rem;}
    }
    @media (max-width: 480px) {
      .hero h2 {font-size:1.2rem;}
      .hero .subtitle {font-size:0.95rem;}
      #sideMenu a {font-size:1rem;}
    }
  </style>
</head>
<body>
  <!-- Side Navigation Menu -->
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
  <button class="open-menu-btn" onclick="toggleMenu()">&#9776;</button>
  <button class="open-purchases-btn" onclick="openPurchasesPanel()">&#128722;</button>
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

  <!-- Main Content Container -->
  <div class="main-content">
    <!-- Home Content (Visible by default) -->
    <div id="homeContent">
      <!-- HERO (NEW) -->
      <section id="home" class="hero">
        <div class="hero-content">
          <img src="Kt8o8usihonWLJtAAj5o6.png" alt="Full Logo" class="full-logo" />
          <h2>Grow Your Business with Great Design</h2>
          <div class="subtitle">We combine creativity and strategy to help entrepreneurs, startups, and brands look amazing.<br>
            Get custom logos, stunning websites, and branding that elevates your impact.</div>
          <div class="hero-buttons">
            <button class="btn-primary" onclick="location.hash='#popular-services';">Explore Services</button>
            <button class="btn-secondary" onclick="location.hash='#contact';">Contact Us</button>
          </div>
          <div class="search-container">
            <input type="text" id="serviceSearch" placeholder="What design do you need?" />
            <button id="searchBtn" type="button">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="#ffffff" viewBox="0 0 16 16">
                <path d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001l3.85 3.85a1 1 0 0 0 1.414-1.414l-3.85-3.85zM6.5 11a4.5 4.5 0 1 1 0-9 4.5 4.5 0 0 1 0 9z"/>
              </svg>
            </button>
          </div>
          <div id="searchResults"></div>
          <div class="popular-keywords">
            <span>Popular:&nbsp;</span>
            <a href="#" onclick="document.getElementById('serviceSearch').value='Logo Design'; performSearch(); return false;">Logo Design</a>,
            <a href="#" onclick="document.getElementById('serviceSearch').value='Website'; performSearch(); return false;">Website</a>,
            <a href="#" onclick="document.getElementById('serviceSearch').value='Flyer'; performSearch(); return false;">Flyer</a>
          </div>
        </div>
      </section>

      <!-- Remaining homepage sections are untouched -->
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
      <footer>
        <p>&copy; 2025 RYT DESIGNS. All Rights Reserved.</p>
        <p>Designed by RYT DESIGNS</p>
        <p>
          <a href="#home" class="back-to-home" onclick="triggerHeroAnimation(); showHome();">
            Back to Home
          </a>
        </p>
      </footer>
    </div>
    <!-- Products Content (Hidden by default) -->
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
  <!-- JavaScript for Interactions -->
  <script>
    // Side Menu functions
    const sideMenu = document.getElementById("sideMenu");
    const purchasesPanel = document.getElementById("purchasesPanel");
    function toggleMenu() {if (sideMenu.style.width === "250px") {closeMenu();} else {sideMenu.style.width = "250px";}}
    function closeMenu() {sideMenu.style.width = "0";}
    function openPurchasesPanel() {purchasesPanel.style.width = "300px";updateCartUI();}
    function closePurchasesPanel() {purchasesPanel.style.width = "0";}
    let cart = [];
    document.getElementById('searchBtn').addEventListener('click', performSearch);
    document.getElementById('serviceSearch').addEventListener('keypress', function(event) {if (event.key === 'Enter') {event.preventDefault();performSearch();}});
    function performSearch() {
      const query = document.getElementById('serviceSearch').value.toLowerCase().trim();
      const resultsContainer = document.getElementById('searchResults');
      resultsContainer.innerHTML = "";
      if(query === ""){return;}
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
        queryTerms.forEach(term => {if(nameLower.includes(term)){score++;}});
        if(score > 0){results.push({...item, score});}
      });
      results.sort((a, b) => b.score - a.score);
      if(results.length === 0){
        resultsContainer.innerHTML = "<p>No products found.</p>";
        return;
      }
      results.forEach(item => {
        const resultDiv = document.createElement('div');
        resultDiv.className = "search-result";
        resultDiv.innerHTML = `<span>${item.name} - $${item.price}</span>
          <button onclick='addToCart("${item.name}", ${item.price})'>Buy</button>
          <button onclick="showProducts()">Products</button>`;
        resultsContainer.appendChild(resultDiv);
      });
    }
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
    function showHome() {
      document.getElementById("homeContent").style.display = "block";
      document.getElementById("productsContent").style.display = "none";
    }
    function showProducts() {
      document.getElementById("homeContent").style.display = "none";
      document.getElementById("productsContent").style.display = "block";
    }
    function triggerHeroAnimation() {
      const heroContent = document.querySelector('.hero-content');
      heroContent.style.animation = 'none';
      void heroContent.offsetWidth;
      heroContent.style.animation = 'bounceIn 1s ease-out';
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
