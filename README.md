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
      --primary-bg: #0D1B2A; /* Dark Blue Background */
      --header-footer-bg: #0A192F; /* Slightly darker blue for header & footer */
      --text-color: #FFFFFF;  /* White text */
      --accent: #FFA500;      /* Bold orange accent */
    }
    
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--primary-bg);
      color: var(--text-color);
      line-height: 1.6;
    }
    
    /* Header / Navigation */
    header {
      background-color: var(--header-footer-bg);
      padding: 1rem 0;
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
    
    /* Hero Section (Home) */
    .hero {
      background-image: url('your-hero-image.jpg'); /* Replace with your own hero image */
      background-size: cover;
      background-position: center;
      height: 70vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 0 2rem;
    }
    .hero h2 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.2rem;
      max-width: 700px;
      margin: 0 auto;
    }
    
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
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
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
    
    /* Override for the Products Section: Display items in a single horizontal line */
    #products .portfolio-container {
      flex-wrap: nowrap;
      justify-content: center;
      gap: 1rem;
      overflow-x: auto;
      padding: 0 1rem;
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
      box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
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

  <!-- Header / Navigation -->
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
    <div>
      <h2>Creativity in Every Pixel</h2>
      <p>Designs to make any event special to you.</p>
    </div>
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
          <source src="website prototype/website prototype/ryt designs presentation.pdf" type="video/mp4">
          Your browser does not support the video tag.
        </video>
        <h3>Project Title Four - Video</h3>
      </div>
      <div class="portfolio-item">
        <embed src="website prototype/ryt designs presentation.pdf" type="application/pdf" width="100%" height="400px" />
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
  </footer>
  
</body>
</html>
