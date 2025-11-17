<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alex Styles | Professional Portfolio</title>
    <style>
        /* Base Reset and Variables */
        :root {
            --primary-color: #007BFF; /* A professional blue */
            --secondary-color: #333;
            --background-color: #F4F7F6;
            --card-background: #FFFFFF;
            --text-color: #4A4A4A;
            --transition-speed: 0.3s;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            /* Using a common fallback font since the link isn't included in this single file */
            font-family: 'Roboto', Arial, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--background-color);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- Header & Navigation --- */
        .main-header {
            background-color: var(--card-background);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .main-header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        nav ul {
            list-style: none;
            display: flex;
        }

        nav a {
            text-decoration: none;
            color: var(--secondary-color);
            padding: 10px 15px;
            transition: color var(--transition-speed);
        }

        /* Hover Effect for Navigation */
        nav a:hover {
            color: var(--primary-color);
            border-bottom: 2px solid var(--primary-color);
        }

        /* --- Hero Section --- */
        .hero-section {
            padding: 80px 0;
            text-align: center;
        }

        .profile-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 20px;
            border: 5px solid var(--primary-color);
        }

        .hero-section h2 {
            color: var(--secondary-color);
            margin-bottom: 10px;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 12px 25px;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 20px;
            transition: background-color var(--transition-speed), transform var(--transition-speed);
        }

        /* Hover Effect for CTA Button */
        .cta-button:hover {
            background-color: #0056b3; /* Darker blue */
            transform: translateY(-2px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        /* --- Portfolio Grid --- */
        .portfolio-section {
            padding: 60px 0;
            background-color: white;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .project-card {
            background-color: var(--background-color);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            transition: transform var(--transition-speed), box-shadow var(--transition-speed);
            text-align: center;
            cursor: pointer;
        }

        .project-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            display: block;
        }

        .project-card h4 {
            color: var(--primary-color);
            margin: 15px 0 5px;
        }

        .project-card p {
            font-size: 0.9em;
            color: #888;
            padding-bottom: 15px;
        }

        /* Hover Effect for Project Cards (Polished Design) */
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }

        .view-details {
            display: block;
            padding: 10px;
            background-color: var(--primary-color);
            color: white;
            font-weight: bold;
            opacity: 0.9;
            transition: opacity var(--transition-speed);
        }

        .project-card:hover .view-details {
            opacity: 1;
        }

        /* --- Skills List --- */
        .skills-section {
            padding: 60px 0;
        }

        .skills-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }

        .skills-list li {
            background-color: var(--card-background);
            padding: 8px 15px;
            border-radius: 20px;
            border: 1px solid var(--primary-color);
            font-weight: 500;
        }

        /* --- Footer --- */
        .main-footer {
            background-color: var(--secondary-color);
            color: white;
            padding: 20px 0;
        }

        .main-footer .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .social-links a {
            color: white;
            text-decoration: none;
            margin-left: 15px;
            opacity: 0.8;
            transition: opacity var(--transition-speed);
        }

        .social-links a:hover {
            opacity: 1;
            text-decoration: underline;
        }

        /* --- CSS Tooltip (Interactive UI/UX Feature) --- */
        .project-card {
            position: relative; /* Needed for the tooltip position */
        }

        .project-card::before {
            content: "Click to see more!"; /* The tooltip text */
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            background-color: var(--secondary-color);
            color: white;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 0.8em;
            white-space: nowrap;
            opacity: 0; /* Initially hidden */
            pointer-events: none; /* Allows clicks to go through to the element below */
            transition: opacity 0.2s;
        }

        .project-card:hover::before {
            opacity: 1; /* Show on hover */
        }
    </style>
</head>
<body>

    <header class="main-header">
        <div class="container">
            <h1>Alex Styles</h1>
            <nav>
                <ul>
                    <li><a href="#hero">Home</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section id="hero" class="hero-section">
            <div class="container">
                <img src="https://via.placeholder.com/150/007BFF/FFFFFF?text=AS" alt="Alex Styles Profile Photo" class="profile-photo">
                <h2>Creative Developer & UX Designer</h2>
                <p>Building beautiful and functional digital experiences.</p>
                <a href="#portfolio" class="cta-button">View My Work</a>
            </div>
        </section>

        <section id="portfolio" class="portfolio-section">
            <div class="container">
                <h3>Selected Projects</h3>
                <div class="project-grid">
                    <div class="project-card">
                        <img src="https://via.placeholder.com/300x200/4CAF50/FFFFFF?text=Project+One" alt="Project Thumbnail 1">
                        <h4>Project Title One</h4>
                        <p>Web Development | UI Design</p>
                        <span class="view-details">View Details</span>
                    </div>

                    <div class="project-card">
                        <img src="https://via.placeholder.com/300x200/FF9800/FFFFFF?text=Project+Two" alt="Project Thumbnail 2">
                        <h4>Project Title Two</h4>
                        <p>Branding | Mobile App</p>
                        <span class="view-details">View Details</span>
                    </div>

                    <div class="project-card">
                        <img src="https://via.placeholder.com/300x200/9C27B0/FFFFFF?text=Project+Three" alt="Project Thumbnail 3">
                        <h4>Project Title Three</h4>
                        <p>Data Visualization | Backend</p>
                        <span class="view-details">View Details</span>
                    </div>
                </div>
            </div>
        </section>

        <section id="skills" class="skills-section">
            <div class="container">
                <h3>Core Skills</h3>
                <ul class="skills-list">
                    <li>HTML5</li>
                    <li>CSS3 (Flexbox/Grid)</li>
                    <li>JavaScript</li>
                    <li>React</li>
                    <li>Figma/Sketch</li>
                    <li>UI/UX Design</li>
                </ul>
            </div>
        </section>

        <section id="contact" class="skills-section">
            <div class="container" style="text-align: center;">
                <h3>Get In Touch</h3>
                <p>Ready to start a project? Email me at <a href="mailto:alex@example.com" style="color: var(--primary-color); text-decoration: none;">alex@example.com</a></p>
            </div>
        </section>
    </main>

    <footer class="main-footer">
        <div class="container">
            <p>&copy; 2025 Alex Styles. All rights reserved.</p>
            <div class="social-links">
                <a href="#">LinkedIn</a>
                <a href="#">GitHub</a>
            </div>
        </div>
    </footer>

</body>
</html>
