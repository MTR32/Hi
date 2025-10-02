<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MT2 Cooperation</title>
    <style>
        /* Reset and base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background-color: #121212; /* Matte black */
            color: #FFFFFF; /* White */
            line-height: 1.6;
        }

        /* Header */
        header {
            background-color: #000000; /* Matte black */
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid #333333; /* Dark gray */
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #FFFFFF;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 2rem;
        }

        .nav-links a {
            color: #A9A9A9; /* Gray */
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #FFFFFF;
        }

        /* Hero Section */
        .hero {
            background-color: #121212;
            text-align: center;
            padding: 150px 2rem 100px;
            border-bottom: 1px solid #333333;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: #FFFFFF;
        }

        .hero p {
            font-size: 1.2rem;
            color: #A9A9A9;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Sections */
        section {
            padding: 80px 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            text-align: center;
            color: #FFFFFF;
        }

        .about-content, .services-grid, .contact-form {
            display: grid;
            gap: 2rem;
        }

        .about-content p {
            color: #A9A9A9;
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .services-grid {
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        }

        .service-card {
            background-color: #000000;
            padding: 2rem;
            border: 1px solid #333333;
            border-radius: 8px;
            text-align: center;
        }

        .service-card h3 {
            color: #FFFFFF;
            margin-bottom: 1rem;
        }

        .service-card p {
            color: #A9A9A9;
        }

        /* Contact Form */
        .contact-form {
            grid-template-columns: 1fr;
            max-width: 600px;
            margin: 0 auto;
        }

        input, textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1rem;
            background-color: #000000;
            border: 1px solid #333333;
            color: #FFFFFF;
            border-radius: 4px;
        }

        input::placeholder, textarea::placeholder {
            color: #A9A9A9;
        }

        button {
            background-color: #333333; /* Gray */
            color: #FFFFFF;
            padding: 1rem 2rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #555555;
        }

        /* Footer */
        footer {
            background-color: #000000;
            text-align: center;
            padding: 2rem;
            border-top: 1px solid #333333;
            color: #A9A9A9;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2rem;
            }

            section {
                padding: 60px 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">MT2</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <h1>Welcome to MT2 Cooperation</h1>
        <p>Exploring innovative partnerships for a brighter future. Join us in building collaborative success.</p>
    </section>

    <section id="about">
        <h2>About MT2</h2>
        <div class="about-content">
            <p>MT2 is a forward-thinking cooperation dedicated to fostering strategic alliances and driving mutual growth. With a focus on innovation and reliability, we bridge opportunities across industries.</p>
        </div>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <div class="services-grid">
            <div class="service-card">
                <h3>Strategic Partnerships</h3>
                <p>Forming long-term collaborations that deliver value and sustainability.</p>
            </div>
            <div class="service-card">
                <h3>Consulting</h3>
                <p>Expert advice tailored to your business needs and goals.</p>
            </div>
            <div class="service-card">
                <h3>Innovation Labs</h3>
                <p>Co-creating cutting-edge solutions in a collaborative environment.</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form class="contact-form" id="contactForm">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea rows="5" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2025 MT2 Cooperation. All rights reserved.</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Contact form handling
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            this.reset();
        });
    </script>
</body>
</html>
