<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>RYT DESIGNS</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #E0F7FA; /* Lighter teal background */
            color: #000; /* Black text */
            line-height: 1.6;
        }

        /* Header Styles */
        header {
            background-color: #B2EBF2; /* Light teal header */
            color: #000; /* Black text */
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
        }

        nav ul {
            list-style: none;
            display: flex;
            position: relative;
        }

        nav li {
            margin-left: 1.5rem;
            position: relative;
        }

        nav a {
            color: #000; /* Black text */
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #ff6347;
        }

        /* Dropdown Menu Styles */
        .dropdown {
            position: relative;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background-color: #B2EBF2;
            min-width: 200px;
            box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
            z-index: 1;
        }

        .dropdown-content a {
            color: #000;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            font-weight: normal;
        }

        .dropdown-content a:hover {
            background-color: #E0F7FA;
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }

        /* Hero Section */
        .hero {
            background-image: url('your-hero-image.jpg');
            background-size: cover;
            background-position: center;
            height: 70vh;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #000; /* Black text */
            text-align: center;
            padding: 0 2rem;
            text-shadow: none; /* Remove text shadow */
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

        /* Portfolio Section */
        #portfolio {
            padding: 4rem 0;
        }

        #portfolio h2 {
            text-align: center;
            margin-bottom: 2rem;
            font-size: 2.5rem;
        }

        .portfolio-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }

        .portfolio-item {
            width: 300px;
            margin: 1rem;
            background-color: #fff;
            border: 1px solid #ddd;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .portfolio-item img {
            width: 100%;
            display: block;
        }

        .portfolio-item:hover {
            transform: translateY(-5px);
        }

        .portfolio-item h3 {
            padding: 1rem;
            font-size: 1.5rem;
            text-align: center;
        }

        /* Contact Section */
        #contact {
            background-color: #f4f4f4;
            padding: 4rem 0;
        }

        #contact h2 {
            text-align: center;
            margin-bottom: 2rem;
            font-size: 2.5rem;
        }

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
            color: #000; /* Black text */
            font-size: 2rem;
            transition: color 0.3s ease;
            text-decoration: none;
        }

        .social-links a:hover {
            color: #ff6347;
        }

        /* Footer Styles */
        footer {
            background-color: #B2EBF2; /* Light teal footer */
            color: #000; /* Black text */
            text-align: center;
            padding: 1rem 0;
        }

        footer p {
            margin-bottom: 0.5rem;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .hero h2 {
                font-size: 2.5rem;
            }

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

    <!-- Header -->
    <header>
        <div class="container">
            <h1>RYT DESIGNS</h1>
            <nav>
                <ul>
                    <li class="dropdown">
                        <a href="#portfolio">What You Can Get</a>
                        <div class="dropdown-content">
                            <a href="#">Presentations</a>
                            <a href="#">Posters/Flyers</a>
                            <a href="#">Videos for Events</a>
                            <a href="#">Business Cards</a>
                            <a href="#">Invitations</a>
                            <a href="#">Logos for Business and Non-Business Purposes</a>
                            <a href="#">YouTube Thumbnails</a>
                            <a href="#">Celebration Cards</a>
                            <a href="#">Banners</a>
                            <a href="#">Menus</a>
                            <a href="#">Itineraries</a>
                        </div>
                    </li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div>
            <h2>Bringing Visions to Life Through Online Design</h2>
            <p>Designs to make any event special to you.</p>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio">
        <h2>My Work</h2>
        <div class="portfolio-container">
            <!-- Portfolio items will go here -->
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
            <!-- Add more portfolio items as needed -->
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Get in Touch</h2>
        <div class="contact-container">
            <div class="contact-info">
                <p><strong>Phone:</strong> +1 226-977-9311</p>
                <p><strong>Phone:</strong> +1 226-977-9310</p>
                <p><strong>Email:</strong> <a href="mailto:youremail@example.com">youremail@example.com</a></p>
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
        <p>Designed by You</p>
    </footer>

</body>
</html>
