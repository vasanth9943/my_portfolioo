<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vasanth V | Software Developer</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* --- VARIABLES --- */
        :root {
            --bg-color: #0a192f;
            --bg-light: #112240;
            --text-primary: #e6f1ff;
            --text-secondary: #8892b0;
            --accent-color: #64ffda;
            --accent-tint: rgba(100, 255, 218, 0.1);
            --nav-height: 80px;
            --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
        }

        /* --- RESET & GLOBAL --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-primary);
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: var(--bg-color);
        }
        ::-webkit-scrollbar-thumb {
            background: #233554;
            border-radius: 5px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: var(--accent-color);
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
            display: inline-block;
        }

        ul { list-style: none; }

        /* --- UTILITIES --- */
        .highlight { color: var(--accent-color); }
        .mono { font-family: 'Fira Code', monospace; }
        
        /* --- NAVIGATION --- */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            height: var(--nav-height);
            padding: 0 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(10, 25, 47, 0.85);
            backdrop-filter: blur(10px); /* Glassmorphism */
            z-index: 1000;
            box-shadow: 0 10px 30px -10px rgba(2,12,27,0.7);
            transition: var(--transition);
        }

        .logo {
            font-family: 'Fira Code', monospace;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--accent-color);
            border: 2px solid var(--accent-color);
            width: 45px;
            height: 45px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 5px;
            cursor: pointer;
        }

        .logo:hover {
            background: var(--accent-tint);
        }

        .nav-links {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        .nav-item {
            font-family: 'Fira Code', monospace;
            font-size: 0.85rem;
            color: var(--text-primary);
        }

        .nav-item span { color: var(--accent-color); margin-right: 5px; }

        .nav-item:hover, .nav-item.active {
            color: var(--accent-color);
        }

        .resume-btn {
            border: 1px solid var(--accent-color);
            color: var(--accent-color);
            padding: 8px 16px;
            border-radius: 4px;
            font-family: 'Fira Code', monospace;
            font-size: 0.85rem;
        }

        .resume-btn:hover {
            background: var(--accent-tint);
        }

        /* Mobile Menu */
        .hamburger {
            display: none;
            cursor: pointer;
            z-index: 1002;
        }
        .bar {
            width: 30px;
            height: 3px;
            background: var(--accent-color);
            margin: 5px 0;
            transition: 0.4s;
        }

        /* --- HERO SECTION --- */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: flex-start;
            padding: 0 150px;
            padding-top: var(--nav-height);
        }

        .hero-intro {
            font-family: 'Fira Code', monospace;
            color: var(--accent-color);
            font-size: 1.1rem;
            margin-bottom: 20px;
        }

        .hero-name {
            font-size: clamp(40px, 8vw, 80px);
            font-weight: 700;
            color: var(--text-primary);
            line-height: 1.1;
        }

        .hero-tagline {
            font-size: clamp(30px, 6vw, 60px);
            font-weight: 700;
            color: var(--text-secondary);
            margin-bottom: 20px;
        }

        /* Typewriter Cursor */
        .typewriter::after {
            content: '|';
            animation: blink 1s step-start infinite;
        }

        @keyframes blink { 50% { opacity: 0; } }

        .hero-desc {
            max-width: 540px;
            font-size: 1.1rem;
            color: var(--text-secondary);
            margin-bottom: 50px;
        }

        .cta-btn {
            padding: 18px 25px;
            border: 1px solid var(--accent-color);
            border-radius: 5px;
            color: var(--accent-color);
            font-family: 'Fira Code', monospace;
            font-size: 1rem;
            margin-top: 20px;
        }

        .cta-btn:hover {
            background: var(--accent-tint);
            box-shadow: 4px 4px 0 var(--accent-color);
            transform: translate(-3px, -3px);
        }

        /* --- SECTIONS COMMON --- */
        section {
            padding: 100px 150px;
        }

        .section-header {
            display: flex;
            align-items: center;
            margin-bottom: 40px;
            width: 100%;
        }

        .section-header h2 {
            font-size: clamp(26px, 5vw, 32px);
            color: var(--text-primary);
            white-space: nowrap;
        }

        .section-header .num {
            font-family: 'Fira Code', monospace;
            color: var(--accent-color);
            font-size: 1.3rem;
            margin-right: 10px;
        }

        .section-header::after {
            content: "";
            display: block;
            width: 300px;
            height: 1px;
            background: #233554;
            margin-left: 20px;
        }

        /* --- ABOUT --- */
        .about-inner {
            display: grid;
            grid-template-columns: 3fr 2fr;
            gap: 50px;
        }

        .about-text p {
            margin-bottom: 15px;
            color: var(--text-secondary);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
            margin-top: 20px;
        }

        .skill-item {
            font-family: 'Fira Code', monospace;
            font-size: 0.85rem;
            color: var(--text-secondary);
            display: flex;
            align-items: center;
        }

        .skill-item::before {
            content: "▹";
            color: var(--accent-color);
            margin-right: 10px;
        }

        /* --- EXPERIENCE --- */
        .timeline {
            border-left: 2px solid #233554;
            margin-left: 10px;
            padding-left: 30px;
        }

        .job-card {
            position: relative;
            margin-bottom: 40px;
        }

        .job-card::before {
            content: "";
            position: absolute;
            left: -37px;
            top: 6px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            border: 2px solid var(--accent-color);
            background: var(--bg-color);
            transition: var(--transition);
        }

        .job-card:hover::before {
            background: var(--accent-color);
        }

        .job-title {
            font-size: 1.3rem;
            color: var(--text-primary);
            font-weight: 500;
        }

        .company { color: var(--accent-color); }

        .range {
            font-family: 'Fira Code', monospace;
            font-size: 0.85rem;
            color: var(--text-secondary);
            margin-bottom: 10px;
            display: block;
        }

        .job-list li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 10px;
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        .job-list li::before {
            content: "▹";
            position: absolute;
            left: 0;
            color: var(--accent-color);
        }

        /* --- PROJECTS --- */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 15px;
        }

        .project-card {
            background-color: var(--bg-light);
            padding: 30px;
            border-radius: 4px;
            transition: var(--transition);
            cursor: pointer;
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: translateY(-7px);
            box-shadow: 0 20px 30px -15px rgba(2,12,27,0.7);
        }

        .project-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 25px;
        }

        .folder-icon { color: var(--accent-color); font-size: 40px; }
        .external-links i { color: var(--text-secondary); font-size: 20px; transition: var(--transition); }
        .external-links i:hover { color: var(--accent-color); }

        .project-title {
            color: var(--text-primary);
            font-size: 1.4rem;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .project-desc {
            color: var(--text-secondary);
            font-size: 1rem;
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .tech-stack {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            font-family: 'Fira Code', monospace;
            font-size: 0.8rem;
            color: var(--text-secondary);
        }

        /* --- EDUCATION --- */
        .edu-item {
            background: var(--bg-light);
            padding: 20px;
            margin-bottom: 15px;
            border-radius: 5px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-left: 3px solid transparent;
            transition: var(--transition);
        }

        .edu-item:hover {
            border-left: 3px solid var(--accent-color);
            background: #152748;
        }

        .edu-details h4 { color: var(--text-primary); font-size: 1.1rem; }
        .edu-details p { color: var(--text-secondary); font-size: 0.9rem; }
        .edu-grade { 
            color: var(--accent-color); 
            font-family: 'Fira Code', monospace; 
            font-weight: bold; 
        }

        /* --- CONTACT --- */
        .contact-section {
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
            padding: 100px 0;
        }

        .contact-title {
            font-size: 3.5rem;
            color: var(--text-primary);
            font-weight: 700;
            margin-bottom: 20px;
        }

        .contact-desc {
            color: var(--text-secondary);
            font-size: 1.2rem;
            margin-bottom: 50px;
        }

        .socials {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
        }

        .socials a {
            color: var(--text-secondary);
            font-size: 1.5rem;
        }

        .socials a:hover {
            color: var(--accent-color);
            transform: translateY(-3px);
        }

        /* --- FOOTER --- */
        footer {
            text-align: center;
            padding: 20px;
            color: var(--text-secondary);
            font-family: 'Fira Code', monospace;
            font-size: 0.8rem;
        }

        /* --- ANIMATIONS & HIDDEN STATES --- */
        .hidden-section {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 1s, transform 1s;
        }

        .show-section {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- MEDIA QUERIES --- */
        @media (max-width: 768px) {
            /* General */
            section { padding: 80px 25px; }
            .hero { padding: 0 25px; align-items: flex-start; }
            .section-header::after { width: 100px; }

            /* Nav */
            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                height: 100vh;
                width: 75%;
                background-color: #112240;
                flex-direction: column;
                justify-content: center;
                transition: 0.3s;
                box-shadow: -10px 0px 30px -15px rgba(2,12,27,0.7);
            }
            .nav-links.active { right: 0; }
            .hamburger { display: block; }
            .hamburger.active .bar:nth-child(2) { opacity: 0; }
            .hamburger.active .bar:nth-child(1) { transform: translateY(8px) rotate(45deg); }
            .hamburger.active .bar:nth-child(3) { transform: translateY(-8px) rotate(-45deg); }

            /* Layouts */
            .about-inner { grid-template-columns: 1fr; }
            .edu-item { flex-direction: column; align-items: flex-start; gap: 10px; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo" onclick="window.scrollTo(0,0)">V</div>
        
        <div class="nav-links">
            <a href="#about" class="nav-item"><span>01.</span>About</a>
            <a href="#experience" class="nav-item"><span>02.</span>Experience</a>
            <a href="#projects" class="nav-item"><span>03.</span>Work</a>
            <a href="#contact" class="nav-item"><span>04.</span>Contact</a>
            <a href="#" class="resume-btn">Resume</a>
        </div>

        <div class="hamburger">
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
        </div>
    </nav>

    <section id="home" class="hero">
        <p class="hero-intro">Hi, my name is</p>
        <h1 class="hero-name">Vasanth V.</h1>
        <h2 class="hero-tagline"><span class="typewriter"></span></h2>
        <p class="hero-desc">
            I am a motivated Information Technology graduate specialized in Java, Web Development, and Machine Learning. 
            I focus on applying problem-solving skills to create professional, user-centric solutions.
        </p>
        <a href="#projects" class="cta-btn">Check out my work!</a>
    </section>

    <section id="about" class="hidden-section">
        <div class="section-header">
            <h2 class="num">01.</h2><h2>About Me</h2>
        </div>
        <div class="about-inner">
            <div class="about-text">
                <p>Hello! I'm Vasanth, a recent B.Tech graduate from Neyveli, Tamil Nadu. My passion lies in bridging the gap between complex algorithms and intuitive user interfaces.</p>
                <p>From designing seamless UI/UX prototypes to training deep learning models for medical diagnosis, I enjoy every aspect of the development lifecycle. I am currently looking for opportunities to contribute my skills to a forward-thinking IT team.</p>
                <p>Here are a few technologies I've been working with recently:</p>
                <div class="skills-grid">
                    <div class="skill-item">Java (Core & Adv)</div>
                    <div class="skill-item">JavaScript (ES6+)</div>
                    <div class="skill-item">HTML5 & CSS3</div>
                    <div class="skill-item">SQL / MySQL</div>
                    <div class="skill-item">Python / ML</div>
                    <div class="skill-item">Figma</div>
                </div>
            </div>
            <div class="about-img">
                </div>
        </div>
    </section>

    <section id="experience" class="hidden-section">
        <div class="section-header">
            <h2 class="num">02.</h2><h2>Where I've Worked</h2>
        </div>
        <div class="timeline">
            
            <div class="job-card">
                <h3 class="job-title">UI/UX Intern <span class="company">@ Astonish Infotech</span></h3>
                <span class="range">June 2025 - Aug 2025</span>
                <ul class="job-list">
                    <li>Designed user-friendly interfaces focusing on improving overall user experience for internal tools.</li>
                    <li>Gained professional hands-on experience with Figma for high-fidelity prototyping.</li>
                    <li>Collaborated closely with the development team to ensure design feasibility.</li>
                </ul>
            </div>

            <div class="job-card">
                <h3 class="job-title">Machine Learning Intern <span class="company">@ SmartiApps Technologies</span></h3>
                <span class="range">Feb 2025 - May 2025</span>
                <ul class="job-list">
                    <li>Contributed to a lung cancer prediction system using advanced machine learning algorithms.</li>
                    <li>Handled data preprocessing, model training, and real-time diagnosis enhancement.</li>
                    <li>Optimized the ResNeXt algorithm for better accuracy in medical imaging.</li>
                </ul>
            </div>

        </div>
    </section>

    <section id="projects" class="hidden-section">
        <div class="section-header">
            <h2 class="num">03.</h2><h2>Some Things I've Built</h2>
        </div>
        <div class="projects-grid">
            
            <div class="project-card" onclick="window.open('#', '_blank')">
                <div class="project-top">
                    <div class="folder-icon"><i class="far fa-folder"></i></div>
                    <div class="external-links"><i class="fas fa-external-link-alt"></i></div>
                </div>
                <h3 class="project-title">Lung Cancer Detection</h3>
                <p class="project-desc">
                    A deep learning model utilizing ResNeXt architecture to detect lung cancer from CT scans. Features CLAHE for image enhancement and CutMix augmentation.
                </p>
                <div class="tech-stack">
                    <span>Python</span>
                    <span>ResNeXt</span>
                    <span>Deep Learning</span>
                </div>
            </div>

            <div class="project-card" onclick="window.open('#', '_blank')">
                <div class="project-top">
                    <div class="folder-icon"><i class="far fa-folder"></i></div>
                    <div class="external-links"><i class="fas fa-external-link-alt"></i></div>
                </div>
                <h3 class="project-title">Conference Mgmt System</h3>
                <p class="project-desc">
                    A comprehensive Java-based system for handling employee records. Includes features for secure data storage, retrieval, and automated performance reporting.
                </p>
                <div class="tech-stack">
                    <span>Java</span>
                    <span>SQL</span>
                    <span>JDBC</span>
                </div>
            </div>

            <div class="project-card" onclick="window.open('#', '_blank')">
                <div class="project-top">
                    <div class="folder-icon"><i class="far fa-folder"></i></div>
                    <div class="external-links"><i class="fas fa-external-link-alt"></i></div>
                </div>
                <h3 class="project-title">E-Commerce for Farmers</h3>
                <p class="project-desc">
                    A dedicated web platform allowing farmers to sell produce directly to consumers. Features include inventory management, secure shopping cart, and user checkout.
                </p>
                <div class="tech-stack">
                    <span>Java</span>
                    <span>SQL</span>
                    <span>HTML/CSS</span>
                </div>
            </div>

        </div>
    </section>

    <section id="education" class="hidden-section">
        <div class="section-header">
            <h2 class="num">04.</h2><h2>Education</h2>
        </div>
        <div class="edu-container">
            <div class="edu-item">
                <div class="edu-details">
                    <h4>B.Tech Information Technology</h4>
                    <p>Anjalai Ammal Mahalingam Engineering College</p>
                    <p class="mono" style="font-size: 0.8rem; margin-top: 5px;">May 2025</p>
                </div>
                <div class="edu-grade">CGPA: 7.5/10</div>
            </div>
            
            <div class="edu-item">
                <div class="edu-details">
                    <h4>HSC (State Board)</h4>
                    <p>Karthi Vidhyalaya Matriculation Hr Sec School</p>
                    <p class="mono" style="font-size: 0.8rem; margin-top: 5px;">May 2021</p>
                </div>
                <div class="edu-grade">78%</div>
            </div>

            <div class="edu-item">
                <div class="edu-details">
                    <h4>SSLC (State Board)</h4>
                    <p>Karthi Vidhyalaya Matriculation Hr Sec School</p>
                    <p class="mono" style="font-size: 0.8rem; margin-top: 5px;">March 2019</p>
                </div>
                <div class="edu-grade">70%</div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact-section hidden-section">
        <p class="mono" style="color: var(--accent-color);">05. What's Next?</p>
        <h2 class="contact-title">Get In Touch</h2>
        <p class="contact-desc">
            I am actively looking for new opportunities in Software Development. 
            Whether you have a question, a project idea, or just want to say hi, feel free to drop a message!
        </p>
        <a href="mailto:vasanthmv230@gmail.com" class="cta-btn">Say Hello</a>

        <div class="socials">
            <a href="https://linkedin.com/vasanth" target="_blank"><i class="fab fa-linkedin-in"></i></a>
            <a href="https://github.com/vasanth" target="_blank"><i class="fab fa-github"></i></a>
            <a href="mailto:vasanthmv230@gmail.com"><i class="far fa-envelope"></i></a>
        </div>
    </section>

    <footer>
        <p>Designed & Built by Vasanth V</p>
    </footer>

    <script>
        // 1. MOBILE MENU TOGGLE
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        const navItems = document.querySelectorAll('.nav-item');

        hamburger.addEventListener('click', () => {
            hamburger.classList.toggle('active');
            navLinks.classList.toggle('active');
        });

        // Close menu when link is clicked
        navItems.forEach(item => {
            item.addEventListener('click', () => {
                hamburger.classList.remove('active');
                navLinks.classList.remove('active');
            });
        });

        // 2. SCROLL REVEAL ANIMATION
        const observerOptions = { threshold: 0.2 };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('show-section');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        document.querySelectorAll('.hidden-section').forEach(el => observer.observe(el));

        // 3. TYPEWRITER EFFECT
        const textToType = "I build things for the web & AI.";
        const typeWriterElement = document.querySelector('.typewriter');
        let i = 0;

        function typeWriter() {
            if (i < textToType.length) {
                typeWriterElement.innerHTML += textToType.charAt(i);
                i++;
                setTimeout(typeWriter, 100); // Speed of typing
            }
        }
        
        // Start typing after a short delay
        setTimeout(typeWriter, 1000);

        // 4. ACTIVE NAVIGATION HIGHLIGHTER
        const sections = document.querySelectorAll('section');
        const navLi = document.querySelectorAll('nav .nav-links a');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (scrollY >= (sectionTop - 200)) {
                    current = section.getAttribute('id');
                }
            });

            navLi.forEach(a => {
                a.classList.remove('active');
                if (a.getAttribute('href').includes(current)) {
                    a.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
