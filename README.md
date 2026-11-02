# Ex01 Portfolio
## Date:31/10/2026

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio | Software Developer</title>

    <style>
        /* =========================================
           1. GLOBAL STYLES
        ========================================= */

        :root {
            --background: #0b1120;
            --secondary: #111c32;
            --card: #152238;
            --accent: #38bdf8;
            --text: #f1f5f9;
            --muted: #aab8cc;
            --border: #263449;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 30px;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: var(--background);
            color: var(--text);
            line-height: 1.7;
        }

        a {
            text-decoration: none;
        }

        section {
            scroll-margin-top: 20px;
        }

        /* =========================================
           2. NAVIGATION BAR
        ========================================= */

        header {
            width: 100%;
            background: var(--background);
        }

        .navbar {
            width: 100%;
            max-width: 1280px;
            min-height: 86px;
            margin: auto;
            padding: 20px 40px;

            display: flex;
            align-items: center;
            justify-content: space-between;

            border-bottom: 1px solid var(--border);
        }

        .logo {
            font-size: 22px;
            font-weight: bold;
            color: var(--text);
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            color: var(--muted);
            font-size: 14px;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        /* =========================================
           3. HOME / HERO SECTION
        ========================================= */

        .hero {
            width: 100%;
            max-width: 1280px;
            min-height: 680px;
            margin: auto;
            padding: 90px 40px;

            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 80px;
        }

        .hero-content {
            flex: 1.5;
        }

        .hero-content .intro {
            color: var(--accent);
            font-size: 14px;
            font-weight: bold;
            letter-spacing: 4px;
            margin-bottom: 35px;
        }

        .hero-content h1 {
            font-size: 58px;
            font-weight: bold;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-content h2 {
            color: var(--accent);
            font-size: 25px;
            margin-bottom: 20px;
        }

        .hero-content .description {
            color: var(--muted);
            font-size: 16px;
            max-width: 570px;
            margin-bottom: 25px;
        }

        /* =========================================
           4. PROFILE IMAGE
        ========================================= */

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .profile-photo {
            width: 250px;
            height: 250px;
            object-fit: cover;
            object-position: center;
            border-radius: 50%;
            border: 3px solid var(--accent);

            box-shadow: 0 0 30px rgba(56, 189, 248, 0.15);
            transition: 0.3s;
            display: block;
        }

        .profile-photo:hover {
            transform: scale(1.05);
            box-shadow: 0 0 40px rgba(56, 189, 248, 0.3);
        }

        /* =========================================
           5. HERO BUTTONS
        ========================================= */

        .hero-buttons {
            display: flex;
            gap: 14px;
            margin-top: 25px;
        }

        .btn {
            display: inline-block;
            padding: 12px 22px;
            border-radius: 6px;

            font-size: 14px;
            font-weight: bold;

            transition: 0.3s;
        }

        .primary-btn {
            background: var(--accent);
            color: #07111f;
            border: 1px solid var(--accent);
        }

        .primary-btn:hover {
            background: #0ea5e9;
            transform: translateY(-3px);
        }

        .secondary-btn {
            color: var(--accent);
            border: 1px solid var(--accent);
        }

        .secondary-btn:hover {
            background: var(--accent);
            color: #07111f;
            transform: translateY(-3px);
        }

        /* =========================================
           6. COMMON SECTION STYLES
        ========================================= */

        .section {
            width: 100%;
            max-width: 1200px;
            margin: auto;
            padding: 90px 40px;
        }

        .alternate {
            max-width: 100%;
            background: var(--secondary);
        }

        .section-title {
            text-align: center;
            font-size: 32px;
            margin-bottom: 45px;
        }

        .section-title span {
            color: var(--accent);
        }

        /* =========================================
           7. ABOUT SECTION
        ========================================= */

        .about-content {
            max-width: 1000px;
            margin: auto;
            padding: 35px;

            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 12px;

            color: var(--muted);
            font-size: 16px;
            line-height: 1.9;
        }

        .about-content p {
            margin-bottom: 15px;
        }

        .about-content p:last-child {
            margin-bottom: 0;
        }

        /* =========================================
           8. SKILLS SECTION
        ========================================= */

        .skills-container {
            max-width: 1120px;
            margin: auto;

            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 22px;
        }

        .skill-card {
            background: var(--card);
            padding: 30px 22px;

            border: 1px solid var(--border);
            border-radius: 10px;

            text-align: center;
            transition: 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-7px);
            border-color: var(--accent);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        .skill-card h3 {
            color: var(--accent);
            font-size: 18px;
            margin-bottom: 12px;
        }

        .skill-card p {
            color: var(--muted);
            font-size: 14px;
        }

        /* =========================================
           9. PROJECTS SECTION
        ========================================= */

        .projects-container {
            max-width: 1120px;
            margin: auto;

            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: var(--card);
            padding: 30px 25px;

            border: 1px solid var(--border);
            border-radius: 12px;

            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-7px);
            border-color: var(--accent);

            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .project-icon {
            width: 45px;
            height: 45px;

            display: flex;
            justify-content: center;
            align-items: center;

            background: rgba(56, 189, 248, 0.12);
            color: var(--accent);

            border-radius: 8px;
            font-weight: bold;

            margin-bottom: 20px;
        }

        .project-card h3 {
            font-size: 19px;
            margin-bottom: 12px;
        }

        .project-card p {
            color: var(--muted);
            font-size: 14px;
            margin-bottom: 15px;
        }

        .project-card .tech {
            color: var(--accent);
            font-size: 13px;
            font-weight: bold;
        }

        .project-link {
            display: inline-block;
            color: var(--accent);
            font-size: 14px;
            font-weight: bold;
            margin-top: 5px;
        }

        .project-link:hover {
            color: white;
        }

        /* =========================================
           10. EDUCATION SECTION
        ========================================= */

        .education-card {
            max-width: 850px;
            margin: auto;
            padding: 35px;

            background: var(--card);
            border-left: 4px solid var(--accent);
            border-radius: 10px;

            transition: 0.3s;
        }

        .education-card:hover {
            transform: translateY(-5px);
        }

        .education-card h3 {
            font-size: 21px;
            margin-bottom: 10px;
        }

        .education-card p {
            color: var(--muted);
            font-size: 15px;
            margin-bottom: 6px;
        }

        .education-card .college {
            color: var(--accent);
            font-size: 17px;
            font-weight: bold;
        }

        /* =========================================
           11. CONTACT SECTION
        ========================================= */

        .contact-description {
            text-align: center;
            color: var(--muted);
            font-size: 16px;
            margin-bottom: 30px;
        }

        .contact-details {
            max-width: 650px;
            margin: 0 auto 30px;
            padding: 30px;

            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 10px;
        }

        .contact-details p {
            color: var(--muted);
            font-size: 15px;
            margin-bottom: 16px;
            overflow-wrap: anywhere;
        }

        .contact-details p:last-child {
            margin-bottom: 0;
        }

        .contact-details a {
            color: var(--accent);
            transition: 0.3s;
        }

        .contact-details a:hover {
            color: white;
        }

        #contact > .btn {
            display: table;
            margin: auto;
        }

        /* =========================================
           12. FOOTER
        ========================================= */

        footer {
            width: 100%;
            background: #070d19;
            border-top: 1px solid var(--border);

            text-align: center;
            padding: 28px 15px;
        }

        footer p {
            color: var(--muted);
            font-size: 13px;
            margin: 5px 0;
        }

        /* =========================================
           13. TABLET RESPONSIVENESS
        ========================================= */

        @media (max-width: 1000px) {

            .navbar {
                padding: 20px 25px;
            }

            .nav-links {
                gap: 17px;
            }

            .hero {
                gap: 40px;
                padding: 80px 30px;
            }

            .hero-content h1 {
                font-size: 45px;
            }

            .profile-photo {
                width: 210px;
                height: 210px;
            }

            .skills-container {
                grid-template-columns: repeat(2, 1fr);
            }

            .projects-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* =========================================
           14. MOBILE RESPONSIVENESS
        ========================================= */

        @media (max-width: 600px) {

            .navbar {
                flex-direction: column;
                gap: 15px;
                padding: 20px 12px;
            }

            .nav-links {
                justify-content: center;
                flex-wrap: wrap;
                gap: 12px 18px;
            }

            .nav-links a {
                font-size: 12px;
            }

            .hero {
                flex-direction: column-reverse;
                text-align: center;

                padding: 65px 20px;
                min-height: auto;
                gap: 35px;
            }

            .hero-content h1 {
                font-size: 36px;
            }

            .hero-content h2 {
                font-size: 20px;
            }

            .hero-content .intro {
                margin-bottom: 20px;
            }

            .hero-content .description {
                font-size: 14px;
            }

            .hero-buttons {
                justify-content: center;
                flex-wrap: wrap;
            }

            .profile-photo {
                width: 170px;
                height: 170px;
            }

            .section {
                padding: 65px 20px;
            }

            .section-title {
                font-size: 26px;
            }

            .skills-container,
            .projects-container {
                grid-template-columns: 1fr;
            }

            .skill-card {
                padding: 24px;
            }

            .education-card {
                padding: 22px;
            }

            .education-card h3 {
                font-size: 17px;
            }

            .about-content {
                padding: 22px;
                font-size: 14px;
            }

            .contact-details {
                padding: 22px;
            }
        }

        /* =========================================
           15. LARGE DESKTOP SCREENS
        ========================================= */

        @media (min-width: 1400px) {

            .hero-content h1 {
                font-size: 64px;
            }

            .hero-content h2 {
                font-size: 27px;
            }

            .hero-content .description {
                font-size: 17px;
            }

            .profile-photo {
                width: 270px;
                height: 270px;
            }
        }

    </style>
</head>

<body>

    <!-- Navigation -->
    <header>
        <nav class="navbar">

            <a href="#" class="logo">MyPortfolio<span>.</span></a>

            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

        </nav>
    </header>

    <!-- Home Section -->
    <section id="home" class="hero">

        <div class="hero-content">

            <p class="intro">HELLO, I'M</p>

            <h1>Priyadharshini R</h1>

            <h2>Computer Science Student</h2>

            <p class="description">
                Aspiring Software Developer passionate about Java,
                problem-solving, backend development, and building
                practical technology solutions.
            </p>

            <div class="hero-buttons">
                <a href="#projects" class="btn primary-btn">
                    View Projects
                </a>

                <a href="#contact" class="btn secondary-btn">
                    Contact Me
                </a>
            </div>

        </div>

        <!-- Profile Photo -->
        <div class="hero-image">

            <img
                src="IMAGE.jpeg"
                alt="Priyadharshini's profile photo"
                class="profile-photo"
            >

        </div>

    </section>

    <!-- About Section -->
    <section id="about" class="section">

        <h2 class="section-title">
            About <span>Me</span>
        </h2>

        <div class="about-content">

            <p>
                I am a Computer Science and Engineering student interested
                in software development and emerging technologies. I enjoy
                learning programming concepts, solving coding challenges,
                and developing applications that solve real-world problems.
            </p>

            <p>
                Currently, I am strengthening my Java, Data Structures
                and Algorithms, database, and software development skills
                to build a strong foundation for my career.
            </p>

        </div>

    </section>

    <!-- Skills Section -->
    <section id="skills" class="section alternate">

        <h2 class="section-title">
            My <span>Skills</span>
        </h2>

        <div class="skills-container">

            <div class="skill-card">
                <h3>Programming</h3>
                <p>Java, Python, C</p>
            </div>

            <div class="skill-card">
                <h3>Web Development</h3>
                <p>HTML, CSS, JavaScript</p>
            </div>

            <div class="skill-card">
                <h3>Core Concepts</h3>
                <p>OOP, DSA, DBMS, SQL</p>
            </div>

            <div class="skill-card">
                <h3>Tools</h3>
                <p>Git, GitHub, VS Code</p>
            </div>

        </div>

    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">

        <h2 class="section-title">
            My <span>Projects</span>
        </h2>

        <div class="projects-container">

            <div class="project-card">

                <div class="project-icon">01</div>

                <h3>Portfolio Website</h3>

                <p>
                    A responsive personal portfolio website built using
                    HTML and CSS to showcase my skills and projects.
                </p>

                <p class="tech">HTML | CSS</p>

                <a href="#" class="project-link">
                    View Project &rarr;
                </a>

            </div>

            <div class="project-card">

                <div class="project-icon">02</div>

                <h3>Student Management System</h3>

                <p>
                    An application concept for managing student details,
                    academic records, and related information efficiently.
                </p>

                <p class="tech">Java | SQL</p>

                <a href="#" class="project-link">
                    View Project &rarr;
                </a>

            </div>

            <div class="project-card">

                <div class="project-icon">03</div>

                <h3>AI-Powered Application</h3>

                <p>
                    An application concept that integrates AI capabilities
                    to provide useful and intelligent features for users.
                </p>

                <p class="tech">Java | AI APIs</p>

                <a href="#" class="project-link">
                    View Project &rarr;
                </a>

            </div>

        </div>

    </section>

    <!-- Education Section -->
    <section id="education" class="section alternate">

        <h2 class="section-title">
            My <span>Education</span>
        </h2>

        <div class="education-card">

            <h3>B.E. Computer Science and Engineering</h3>

            <p class="college">Your College Name</p>

            <p>2024 – 2028</p>

            <p>
                Relevant areas: Java, DSA, DBMS, Software Engineering
            </p>

        </div>

    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">

        <h2 class="section-title">
            Contact <span>Me</span>
        </h2>

        <p class="contact-description">
            Have an opportunity or project in mind? Feel free to connect.
        </p>

        <div class="contact-details">

            <p>
                Email:
                <a href="mailto:yourmail@example.com">
                    yourmail@example.com
                </a>
            </p>

            <p>
                LinkedIn:
                <a href="https://www.linkedin.com/"
                   target="_blank"
                   rel="noopener noreferrer">
                    My LinkedIn Profile
                </a>
            </p>

            <p>
                GitHub:
                <a href="https://github.com/"
                   target="_blank"
                   rel="noopener noreferrer">
                    My GitHub Profile
                </a>
            </p>

        </div>

        <a href="mailto:yourmail@example.com" class="btn primary-btn">
            Send Email
        </a>

    </section>

    <!-- Footer -->
    <footer>

        <p>&copy; 2026 Priyadharshini R. All rights reserved.</p>

        <p>Built with HTML and CSS.</p>

    </footer>

</body>
</html>
```




## OUTPUT
<img width="1920" height="1152" alt="image" src="https://github.com/user-attachments/assets/1850e07e-e595-419e-8284-d0459afa3120" />
<img width="1920" height="1152" alt="image" src="https://github.com/user-attachments/assets/d8ee1558-72d9-42af-bd54-ac7e6c8c6b50" />
<img width="1920" height="1152" alt="image" src="https://github.com/user-attachments/assets/403fdebd-d74e-49a2-8117-99ca5e1d7763" />




## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
