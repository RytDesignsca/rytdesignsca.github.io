<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="RYT DESIGNS - Creativity in Every Pixel.">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>RYT DESIGNS</title>
  <style>
    /* Global Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    /* Define Color Scheme: Dark Blue, White, Orange */
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
      /* Add top padding to avoid content being hidden behind fixed header */
      padding-top: 80px;
    }
    
    /* Header / Navigation (Banner) - Fixed so it always shows */
    header {
      background-color: var(--header-footer-bg);
      padding: 1rem 0;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 10;
    }
    header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 90%;
      margin: 0 auto;
    }
    header h1 {
      font-size: 2rem;
      color: var(--text-color);
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
    
    /* Home / Hero Section */
    .hero {
      position: relative;
      background-image: url('your-hero-image.jpg'); /* Replace with your own background image */
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
    .hero .hero-content {
      position: relative;
      z-index: 2;
      max-width: 800px;
      margin: 0 auto;
    }
    .hero h2 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 1rem;
    }
    /* Decorative images around the hero text */
    .design-image {
      position: absolute;
      opacity: 0.9;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }
    /* Position multiple decorative images */
    .design-image.img1 { top: 5%; left: 5%; width: 80px; }
    .design-image.img2 { top: 10%; right: 5%; width: 80px; }
    .design-image.img3 { bottom: 10%; left: 10%; width: 80px; }
    .design-image.img4 { bottom: 15%; right: 8%; width: 80px; }
    .design-image.img5 { top: 50%; left: 0%; width: 80px; }
    .design-image.img6 { bottom: 20%; right: 0%; width: 80px; }
    
    /* Section Title Styling */
    section {
      padding: 4rem 0;
    }
    section h2 {
      text-align: center;
      margin-bottom: 2rem;
      font-size: 2.5rem;
    }
    
    /* Portfolio / Products / Services Container */
    .portfolio-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }
    .portfolio-item {
      width: 300px;
      margin: 1rem;
      background-color: #FFFFFF;
      color: #000;
      border: 1px solid #ddd;
      overflow: hidden;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
      text-align: center;
    }
    .portfolio-item img {
      width: 100%;
      display: block;
    }
    .portfolio-item video,
    .portfolio-item embed {
      width: 100%;
      height: 400px;
      border: none;
    }
    .portfolio-item:hover {
      transform: translateY(-5px);
    }
    .portfolio-item h3 {
      padding: 1rem;
      font-size: 1.5rem;
    }
    
    /* Services Dropdown Menu */
    .dropdown {
      position: relative;
      display: inline-block;
      margin: 0 1rem;
    }
    .dropdown button {
      padding: 0.5rem 1rem;
      border: none;
      cursor: pointer;
      background-color: var(--accent);
      color: var(--text-color);
      font-weight: bold;
    }
    .dropdown-content {
      display: none;
      position: absolute;
      background-color: var(--header-footer-bg);
      min-width: 250px;
      box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
      z-index: 1;
      padding: 0.5rem 0;
    }
    .dropdown-content a {
      color: var(--text-color);
      padding: 12px 16px;
      text-decoration: none;
      display: flex;
      align-items: center;
      font-weight: normal;
    }
    .dropdown-content a img {
      width: 40px;
      height: 40px;
      margin-right: 10px;
      object-fit: cover;
      border-radius: 5px;
    }
    .dropdown-content a:hover {
      background-color: var(--primary-bg);
    }
    .dropdown:hover .dropdown-content {
      display: block;
    }
    
    /* Contact Section */
    .contact-container {
      display: flex;
      flex-direction: column;
      align-items: center;
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
      .portfolio-item {
        width: 90%;
      }
      header .container {
        flex-direction: column;
      }
      nav ul {
        flex-direction: column;
        align-items: center;
      }
      nav li {
        margin: 0.5rem 0;
      }
    }
  </style>
</head>
<body>
  <!-- Header / Navigation (Banner) -->
  <header>
    <div class="container">
      <h1>RYT DESIGNS</h1>
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#products">Products</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>
  
  <!-- Home / Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h2>Creativity in Every Pixel</h2>
      <p>Designs to make any event special to you.</p>
      <p>
        At RYT DESIGNS, we believe that each project is more than just a design—it's an immersive experience crafted with passion and dedication. Our innovative approach merges cutting-edge technology with creative artistry to bring your vision to life.
      </p>
      <p>
        Whether you're hosting a special event or building your brand, our designs are tailored to resonate with your audience and transform spaces into memories. Discover how our expertise can elevate your project and enhance your packaging, t-shirt designs, logos, and more.
      </p>
      <p>
        Scroll down to explore our products, services, and to get in touch with our creative team.
      </p>
    </div>
    <!-- Decorative images placed all around the hero text -->
    <img src="packaging.jpg" alt="Packaging Design" class="design-image img1">
    <img src="tshirt.jpg" alt="T-Shirt Design" class="design-image img2">
    <img src="logo.jpg" alt="Logo Design" class="design-image img3">
    <img src="poster.jpg" alt="Poster Design" class="design-image img4">
    <img src="brochure.jpg" alt="Brochure Design" class="design-image img5">
    <img src="packaging2.jpg" alt="Packaging Design 2" class="design-image img6">
  </section>
  
  <!-- Products Section -->
  <section id="products">
    <h2>Our Products</h2>
    <div class="portfolio-container">
      <div class="portfolio-item">
        <img src="design1.jpg" alt="Design 1">
        <h3>Project Title One</h3>
      </div>
      <div class="portfolio-item">
        <img src="design2.jpg" alt="Design 2">
        <h3>Project Title Two</h3>
      </div>
      <div class="portfolio-item">
        <img src="design3.jpg" alt="Design 3">
        <h3>Project Title Three</h3>
      </div>
      <div class="portfolio-item">
        <video controls>
          <source src="website-prototype/ryt designs video.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
        <h3>Project Title Four - Video</h3>
      </div>
      <div class="portfolio-item">
        <embed src="website-prototype/ryt designs presentation.pdf" type="application/pdf" width="100%" height="400px" />
        <h3>Project Title Five - PDF</h3>
      </div>
    </div>
  </section>
  
  <!-- Services Section -->
  <section id="services">
    <h2>Our Services</h2>
    <!-- Dropdown Menus for Service Categories -->
    <div class="dropdown">
      <button>Branding &amp; Identity</button>
      <div class="dropdown-content">
        <a href="#"><img src="service1.jpg" alt="Service 1">Logo Design</a>
        <a href="#"><img src="service2.jpg" alt="Service 2">Business Cards</a>
        <a href="#"><img src="service3.jpg" alt="Service 3">Brochures</a>
      </div>
    </div>
    <div class="dropdown">
      <button>Web &amp; Digital</button>
      <div class="dropdown-content">
        <a href="#"><img src="service4.jpg" alt="Service 4">Website Design</a>
        <a href="#"><img src="service5.jpg" alt="Service 5">Social Media Graphics</a>
        <a href="#"><img src="service6.jpg" alt="Service 6">Email Marketing</a>
      </div>
    </div>
    <!-- Showcase of Service Features -->
    <div class="portfolio-container">
      <div class="portfolio-item">
        <img src="design1.jpg" alt="Design 1">
        <h3>Full Branding Package</h3>
      </div>
      <div class="portfolio-item">
        <img src="design2.jpg" alt="Design 2">
        <h3>Custom Web Design</h3>
      </div>
      <div class="portfolio-item">
        <img src="design3.jpg" alt="Design 3">
        <h3>Social Media Management</h3>
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
        <p><strong>Email:</strong> <a href="mailto:rytdesignsca@gmail.com" style="color: var(--accent);">rytdesignsca@gmail.com</a></p>
      </div>
      <div class="social-links">
        <a href="https://www.instagram.com/rytdesigns_/" target="_blank">Instagram</a>
        <a href="https://www.tiktok.com/@ryt.designs7" target="_blank">TikTok</a>
      </div>
    </div>
  </section>
  
  <!-- Footer -->
  <footer>
    <p>&copy; 2025 Ryt Designs. All Rights Reserved.</p>
    <p>Designed by Ryt Designs</p>
    <p><a href="#home" class="back-to-home">Back to Home</a></p>
  </footer>
  
</body>
</html>
