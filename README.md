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
      --header-footer-bg: #0A192F;      /* Slightly darker blue for header & footer */
      --text-color: #FFFFFF;           /* White text */
      --accent: #FFA500;               /* Bold orange accent */
    }
    
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--primary-bg);
      color: var(--text-color);
      line-height: 1.6;
      padding-top: 80px; /* leave room for fixed header */
    }
    
    /* Header / Navigation */
    header {
      background-color: var(--header-footer-bg);
      padding: 1rem 0;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      transition: transform 0.3s ease-in-out;
    }
    header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 90%;
      margin: 0 auto;
    }
    .brand h1 {
      font-size: 2rem;
      color: var(--text-color);
      border-bottom: 2px solid var(--text-color);
      padding-bottom: 5px;
    }
    nav ul {
      list-style: none;
      display: flex;
    }
    nav li {
      margin-left: 1.5rem;
    }
    nav a {
      color: var(--text-color);
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s ease;
    }
    nav a:hover {
      color: var(--accent);
    }
    
    /* Hero Section */
    .hero {
      position: relative;
      background-image: url('your-hero-image.jpg'); /* Replace with your hero background image */
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
    
    /* Decorative Images in Hero (optional) */
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
    
    /* -------------------- *
         New Sections
    * ---------------------*/
    
    /* Design Process Section (Image 1) */
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
    
    /* Popular Services Section (Image 2) */
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
    
    /* Design Packages Section (Image 3) */
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
    
    /* Freelance Banner Section (Image 4) */
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
    .banner-buttons {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
    }
    .banner-buttons button {
      background-color: var(--accent);
      padding: 0.5rem 1rem;
      border: none;
      color: var(--text-color);
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .banner-buttons button:hover {
      background-color: #e69500;
    }
    
    /* -------------------- *
         Existing Sections
    * ---------------------*/
    
    /* Our Products Section */
    section#products {
      padding: 4rem 0;
    }
    section#products h2 {
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
    section#contact {
      padding: 4rem 0;
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
    }
    .social-links a {
      margin: 0 1rem;
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
    
    /* Responsive Styles */
    @media (max-width: 768px) {
      header .container {
        flex-direction: row;
        justify-content: space-between;
      }
      nav ul {
        flex-direction: row;
      }
      nav li {
        margin-left: 1rem;
      }
      .brand h1 {
        font-size: 1.8rem;
        border-bottom: 2px solid var(--text-color);
        padding-bottom: 4px;
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
      .hero h2 {
        font-size: 2.5rem;
      }
      .hero p {
        font-size: 1rem;
      }
    }
    
    @media (max-width: 480px) {
      nav li {
        margin-left: 0.5rem;
      }
      .hero h2 {
        font-size: 2rem;
      }
      .hero p {
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body>
  <!-- Header / Navigation -->
  <header>
    <div class="container">
      <div class="brand">
        <h1>RYT DESIGNS</h1>
      </div>
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#design-process">Process</a></li>
          <li><a href="#popular-services">Services</a></li>
          <li><a href="#design-packages">Packages</a></li>
          <li><a href="#freelance-banner">Freelance</a></li>
          <li><a href="#products">Products</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>
  
  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <img src="Kt8o8usihonWLJtAAj5o6.png" alt="Full Logo" class="full-logo">
      <h2>Creativity in Every Pixel</h2>
      <p>
        At RYT DESIGNS, we transform your vision into immersive design experiences.
      </p>
      <p>
        Explore our process, services, packages, and products to see how we bring creativity to life.
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
  
  <!-- Design Process Section (Image 1) -->
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
  
  <!-- Popular Services Section (Image 2) -->
  <section id="popular-services" class="popular-services">
    <h2>Popular Services</h2>
    <div class="services-boxes">
      <div class="service-box">
        <img src="web-development-icon.png" alt="Website Development">
        <h3>Website Development</h3>
      </div>
      <div class="service-box">
        <img src="logo-design-icon.png" alt="Logo Design">
        <h3>Logo Design</h3>
      </div>
      <div class="service-box">
        <img src="seo-icon.png" alt="SEO">
        <h3>SEO</h3>
      </div>
      <div class="service-box">
        <img src="architecture-icon.png" alt="Architecture &amp; Interior">
        <h3>Architecture &amp; Interior</h3>
      </div>
      <div class="service-box">
        <img src="voice-over-icon.png" alt="Voice Over">
        <h3>Voice Over</h3>
      </div>
      <div class="service-box">
        <img src="social-media-icon.png" alt="Social Media Marketing">
        <h3>Social Media</h3>
      </div>
    </div>
  </section>
  
  <!-- Design Packages Section (Image 3) -->
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
  
  <!-- Freelance Banner Section (Image 4) -->
  <section id="freelance-banner" class="freelance-banner">
    <div class="banner-content">
      <h2>Our freelancers will take it from here</h2>
      <div class="search-container">
        <input type="text" placeholder="Search services..." />
        <button type="button">Search</button>
      </div>
      <div class="banner-buttons">
        <button>Website Development</button>
        <button>Logo Design</button>
        <button>Video Editing</button>
        <button>Architecture &amp; Design</button>
      </div>
    </div>
  </section>
  
  <!-- Our Products Section (Optional) -->
  <section id="products">
    <h2>Our Products</h2>
    <div class="portfolio-container">
      <div class="portfolio-item">
        <a href="website prototype/ryt designs video.mp4" target="_blank">
          <img src="website prototype/ryt designs video.mp4" alt="Event Videos">
        </a>
        <h3>Event Videos</h3>
      </div>
      <div class="portfolio-item">
        <a href="website prototype/ryt designs presentation.pdf" target="_blank">
          <img src="website prototype/ryt designs presentation.pdf" alt="Presentation">
        </a>
        <h3>Presentation</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/A A itinerary.png" alt="Itinerary">
        <h3>Itinerary</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/Banner 4 website.png" alt="Banner">
        <h3>Banner</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/business card proto.jpg" alt="Business Card">
        <h3>Business Card</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/celeb 4 website.png" alt="Birthday Card">
        <h3>Birthday Card</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/invitation 4 website.png" alt="Invitation">
        <h3>Invitation</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/Logo 4 website.png" alt="Logo">
        <h3>Logo</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/Menu 4 website.png" alt="Menu">
        <h3>Menu</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/youtube thumbnail 4 website.png" alt="YouTube Thumbnail">
        <h3>YouTube Thumbnail</h3>
      </div>
      <div class="portfolio-item">
        <img src="website prototype/website.png" alt="Website Prototype">
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
  
  <!-- JavaScript: Hide/Show Header on Scroll -->
  <script>
    let lastScroll = 0;
    const header = document.querySelector('header');
  
    window.addEventListener('scroll', function () {
      let currentScroll = window.pageYOffset || document.documentElement.scrollTop;
  
      if (currentScroll > lastScroll && currentScroll > 100) {
        header.style.transform = 'translateY(-100%)';
      } else {
        header.style.transform = 'translateY(0)';
      }
      lastScroll = currentScroll;
    });
  </script>
</body>
</html>
