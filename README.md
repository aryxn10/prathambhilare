<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pratham Bhilare | Project Manager & Mechanical Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #0a192f;
            --secondary: #64ffda;
            --text: #ccd6f6;
            --text-secondary: #8892b0;
            --accent: #f97316;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Roboto', sans-serif;
        }
        
        body {
            background-color: var(--primary);
            color: var(--text);
            line-height: 1.7;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        header {
            padding: 2rem 0;
            text-align: center;
            animation: fadeIn 1s ease-in;
        }
        
        .header-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .header-content p {
            color: var(--text-secondary);
            font-size: 1.2rem;
        }
        
        .badge-container {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 1.5rem 0;
            flex-wrap: wrap;
        }
        
        .badge {
            background-color: rgba(100, 255, 218, 0.1);
            border: 1px solid var(--secondary);
            color: var(--secondary);
            padding: 0.5rem 1rem;
            border-radius: 5px;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .badge:hover {
            background-color: rgba(100, 255, 218, 0.2);
            transform: translateY(-3px);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 1rem 0;
        }
        
        .social-links a {
            color: var(--text);
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--secondary);
            transform: translateY(-3px);
        }
        
        section {
            padding: 3rem 0;
            border-top: 1px solid rgba(100, 255, 218, 0.1);
            animation: slideUp 0.8s ease-in-out;
        }
        
        .section-title {
            display: inline-block;
            font-size: 1.8rem;
            margin-bottom: 2rem;
            position: relative;
            color: var(--text);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background: var(--secondary);
        }
        
        .about-content {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 2;
            min-width: 300px;
        }
        
        .skills-container {
            margin-top: 1.5rem;
        }
        
        .skill-category {
            margin-bottom: 1.5rem;
        }
        
        .skill-category h4 {
            color: var(--secondary);
            margin-bottom: 0.5rem;
        }
        
        .skill-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
        
        .skill-item {
            background-color: rgba(255, 255, 255, 0.05);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            background-color: rgba(100, 255, 218, 0.1);
            color: var(--secondary);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(500px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background-color: rgba(255, 255, 255, 0.03);
            border-radius: 8px;
            padding: 1.5rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(100, 255, 218, 0.1);
            height: 100%;
            display: flex;
            flex-direction: column;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px -15px rgba(0, 0, 0, 0.7);
            border-color: var(--secondary);
        }
        
        .project-title {
            color: var(--text);
            font-size: 1.3rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }
        
        .project-title i {
            color: var(--secondary);
            margin-right: 10px;
        }
        
        .project-achievements {
            margin: 1rem 0;
            flex-grow: 1;
        }
        
        .achievement-item {
            display: flex;
            margin-bottom: 0.5rem;
            align-items: baseline;
        }
        
        .achievement-item i {
            color: var(--secondary);
            margin-right: 10px;
            font-size: 0.8rem;
        }
        
        .project-links {
            margin-top: auto;
            display: flex;
            gap: 1rem;
        }
        
        .project-link {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
        }
        
        .project-link:hover {
            color: var(--secondary);
        }
        
        .project-link i {
            margin-right: 5px;
        }
        
        .education-timeline, .experience-timeline {
            position: relative;
            margin-left: 20px;
        }
        
        .timeline-item {
            position: relative;
            padding-left: 30px;
            margin-bottom: 2rem;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--secondary);
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            left: 5px;
            top: 12px;
            width: 2px;
            height: calc(100% + 1rem);
            background-color: rgba(100, 255, 218, 0.3);
        }
        
        .timeline-item:last-child::after {
            display: none;
        }
        
        .timeline-date {
            color: var(--secondary);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }
        
        .timeline-title {
            color: var(--text);
            font-size: 1.2rem;
            margin-bottom: 0.3rem;
        }
        
        .timeline-subtitle {
            color: var(--text-secondary);
            font-size: 1rem;
            font-style: italic;
        }
        
        .experience-details {
            margin-top: 1rem;
        }
        
        .experience-details ul {
            list-style-type: none;
        }
        
        .experience-details li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 0.5rem;
        }
        
        .experience-details li::before {
            content: '►';
            position: absolute;
            left: 0;
            color: var(--secondary);
            font-size: 0.7rem;
        }
        
        .publications-list {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }
        
        .publication-item {
            background-color: rgba(255, 255, 255, 0.03);
            border-radius: 8px;
            padding: 1.5rem;
            border: 1px solid rgba(100, 255, 218, 0.1);
            transition: all 0.3s ease;
        }
        
        .publication-item:hover {
            border-color: var(--secondary);
            background-color: rgba(255, 255, 255, 0.05);
        }
        
        .publication-title {
            color: var(--text);
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }
        
        .publication-journal {
            color: var(--secondary);
            font-style: italic;
            margin-bottom: 1rem;
        }
        
        .publication-link {
            display: inline-flex;
            align-items: center;
            color: var(--text-secondary);
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .publication-link:hover {
            color: var(--secondary);
        }
        
        .contact-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            transition: all 0.3s ease;
            padding: 1rem;
            border-radius: 8px;
            width: 100%;
            max-width: 400px;
            background-color: rgba(255, 255, 255, 0.03);
        }
        
        .contact-item:hover {
            background-color: rgba(100, 255, 218, 0.05);
            transform: translateX(5px);
        }
        
        .contact-icon {
            font-size: 1.5rem;
            color: var(--secondary);
        }
        
        .contact-info {
            flex-grow: 1;
        }
        
        .contact-label {
            font-size: 0.8rem;
            color: var(--text-secondary);
        }
        
        .contact-value {
            color: var(--text);
        }
        
        .contact-value a {
            color: inherit;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .contact-value a:hover {
            color: var(--secondary);
        }
        
        footer {
            text-align: center;
            padding: 2rem 0;
            color: var(--text-secondary);
            font-size: 0.9rem;
            border-top: 1px solid rgba(100, 255, 218, 0.1);
        }
        
        .highlight {
            color: var(--secondary);
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
            from { 
                opacity: 0;
                transform: translateY(20px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .header-content h1 {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="header-content">
                <h1>Pratham Bhilare</h1>
                <p>Project Manager & Mechanical Engineer specialized in Technology & Engineering Innovation</p>
                
                <div class="badge-container">
                    <div class="badge">Project Manager</div>
                    <div class="badge">Mechanical Engineer</div>
                    <div class="badge">Tech Enthusiast</div>
                </div>
                
                <div class="social-links">
                    <a href="https://linkedin.com/in/prathambhilare" target="_blank"><i class="fab fa-linkedin"></i></a>
                    <a href="mailto:pbhilar1@asu.edu"><i class="fas fa-envelope"></i></a>
                    <a href="https://github.com/prathambhilare" target="_blank"><i class="fab fa-github"></i></a>
                </div>
            </div>
        </header>
        
        <section id="about">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Hi! I'm <span class="highlight">Pratham Bhilare</span>, a passionate Project Manager and Mechanical Engineer specializing in Technology & Engineering Innovation. I love optimizing processes, solving problems, and leading projects that bridge technology with business strategy.</p>
                    
                    <div class="skills-container">
                        <div class="skill-category">
                            <h4>Key Skills</h4>
                            <div class="skill-list">
                                <span class="skill-item">Project Management</span>
                                <span class="skill-item">Leadership</span>
                                <span class="skill-item">Teamwork & Collaboration</span>
                                <span class="skill-item">Problem Solving</span>
                                <span class="skill-item">Strategic Planning</span>
                                <span class="skill-item">Process Optimization</span>
                            </div>
                        </div>
                        
                        <div class="skill-category">
                            <h4>Technical Tools</h4>
                            <div class="skill-list">
                                <span class="skill-item">SolidWorks</span>
                                <span class="skill-item">Ansys APDL</span>
                                <span class="skill-item">Microsoft Project</span>
                                <span class="skill-item">Excel</span>
                                <span class="skill-item">PowerPoint</span>
                                <span class="skill-item
                                <span class="skill-item">AutoCAD</span>
                               <span class="skill-item">Data Analysis</span>
                           </div>
                       </div>
                   </div>
               </div>
           </div>
       </section>
       
       <section id="projects">
           <h2 class="section-title">Featured Projects</h2>
           <div class="projects-grid">
               <div class="project-card">
                   <h3 class="project-title">
                       <i class="fas fa-fire"></i>
                       Heat Recovery from Solar Panels
                   </h3>
                   <div class="project-achievements">
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Increased efficiency from 18.22% to 20.34%</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Designed a cooling system for dry agricultural products</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Published in International Journal of Engineering Research & Technology</span>
                       </div>
                   </div>
                   <div class="project-links">
                       <a href="Publications/HeatRecovery_Paper.pdf" class="project-link">
                           <i class="fas fa-file-pdf"></i> Read Paper
                       </a>
                   </div>
               </div>
               
               <div class="project-card">
                   <h3 class="project-title">
                       <i class="fas fa-cogs"></i>
                       Stirling Engine
                   </h3>
                   <div class="project-achievements">
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Built a working Stirling engine prototype</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Created an industry-referenced technical report</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Optimized thermal efficiency through innovative design</span>
                       </div>
                   </div>
                   <div class="project-links">
                       <a href="Projects/StirlingEngine/" class="project-link">
                           <i class="fas fa-link"></i> View Project
                       </a>
                   </div>
               </div>
               
               <div class="project-card">
                   <h3 class="project-title">
                       <i class="fas fa-bullseye"></i>
                       Catapult Mechanism
                   </h3>
                   <div class="project-achievements">
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Designed a functional prototype</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Applied mechanical principles to real-world applications</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Conducted performance analysis and optimization</span>
                       </div>
                   </div>
                   <div class="project-links">
                       <a href="Projects/Catapult/" class="project-link">
                           <i class="fas fa-link"></i> View Project
                       </a>
                   </div>
               </div>
               
               <div class="project-card">
                   <h3 class="project-title">
                       <i class="fas fa-bolt"></i>
                       Energy from Rotating Doors
                   </h3>
                   <div class="project-achievements">
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Developed a revolving door mechanism that generates electricity</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Conducted research & designed an innovative system</span>
                       </div>
                       <div class="achievement-item">
                           <i class="fas fa-check-circle"></i>
                           <span>Created sustainable energy solution for public buildings</span>
                       </div>
                   </div>
                   <div class="project-links">
                       <a href="Projects/RotaryDoors/" class="project-link">
                           <i class="fas fa-link"></i> View Project
                       </a>
                   </div>
               </div>
           </div>
       </section>
       
       <section id="education">
           <h2 class="section-title">Education</h2>
           <div class="education-timeline">
               <div class="timeline-item">
                   <div class="timeline-date">2024 - 2026</div>
                   <h3 class="timeline-title">Masters in Management of Technology</h3>
                   <div class="timeline-subtitle">Arizona State University</div>
               </div>
               
               <div class="timeline-item">
                   <div class="timeline-date">2021 - 2024</div>
                   <h3 class="timeline-title">B.Tech in Mechanical Engineering</h3>
                   <div class="timeline-subtitle">Pillai College of Engineering, Mumbai University</div>
               </div>
               
               <div class="timeline-item">
                   <div class="timeline-date">2018 - 2021</div>
                   <h3 class="timeline-title">Diploma in Mechanical Engineering</h3>
                   <div class="timeline-subtitle">Agnel Polytechnic</div>
               </div>
           </div>
       </section>
       
       <section id="experience">
           <h2 class="section-title">Work Experience</h2>
           <div class="experience-timeline">
               <div class="timeline-item">
                   <div class="timeline-date">January 2024 - April 2024</div>
                   <h3 class="timeline-title">Maintenance Trainee</h3>
                   <div class="timeline-subtitle">Tata Power</div>
                   <div class="experience-details">
                       <ul>
                           <li>Performed routine equipment maintenance & safety checks</li>
                           <li>Collaborated to reduce downtime and improve efficiency</li>
                           <li>Participated in preventive maintenance planning</li>
                       </ul>
                   </div>
               </div>
               
               <div class="timeline-item">
                   <div class="timeline-date">December 2022 - January 2023</div>
                   <h3 class="timeline-title">Trainee</h3>
                   <div class="timeline-subtitle">Matharu Sons</div>
                   <div class="experience-details">
                       <ul>
                           <li>Optimized fuel dispenser manufacturing processes</li>
                           <li>Designed fabrication projects, ensuring client specifications</li>
                           <li>Contributed to quality control procedures</li>
                       </ul>
                   </div>
               </div>
           </div>
       </section>
       
       <section id="certifications">
           <h2 class="section-title">Certifications</h2>
           <div class="experience-timeline">
               <div class="timeline-item">
                   <div class="timeline-date">July 2024</div>
                   <h3 class="timeline-title">TCS Data Visualization Simulation</h3>
               </div>
               
               <div class="timeline-item">
                   <div class="timeline-date">February 2023</div>
                   <h3 class="timeline-title">Certified SolidWorks Associate (CSWA)</h3>
               </div>
               
               <div class="timeline-item">
                   <div class="timeline-date">December 2019</div>
                   <h3 class="timeline-title">Basic PLC, HMI & Servo Motion Course</h3>
               </div>
           </div>
       </section>
       
       <section id="publications">
           <h2 class="section-title">Publications</h2>
           <div class="publications-list">
               <div class="publication-item">
                   <h3 class="publication-title">Heat Recovery from Solar Photovoltaic (PV) Panel</h3>
                   <div class="publication-journal">International Journal of Engineering Research & Technology (April 2024)</div>
                   <p>Research on innovative methods to improve solar panel efficiency while utilizing waste heat for agricultural applications.</p>
                   <a href="Publications/HeatRecovery_Paper.pdf" class="publication-link">
                       <i class="fas fa-file-pdf"></i> Read Full Paper
                   </a>
               </div>
           </div>
       </section>
       
       <section id="contact">
           <h2 class="section-title">Connect with Me</h2>
           <div class="contact-container">
               <div class="contact-item">
                   <div class="contact-icon">
                       <i class="fas fa-envelope"></i>
                   </div>
                   <div class="contact-info">
                       <div class="contact-label">Email</div>
                       <div class="contact-value">
                           <a href="mailto:pbhilar1@asu.edu">pbhilar1@asu.edu</a>
                       </div>
                   </div>
               </div>
               
               <div class="contact-item">
                   <div class="contact-icon">
                       <i class="fab fa-linkedin"></i>
                   </div>
                   <div class="contact-info">
                       <div class="contact-label">LinkedIn</div>
                       <div class="contact-value">
                           <a href="https://linkedin.com/in/prathambhilare" target="_blank">linkedin.com/in/prathambhilare</a>
                       </div>
                   </div>
               </div>
               
               <div class="contact-item">
                   <div class="contact-icon">
                       <i class="fab fa-github"></i>
                   </div>
                   <div class="contact-info">
                       <div class="contact-label">GitHub</div>
                       <div class="contact-value">
                           <a href="https://github.com/prathambhilare" target="_blank">github.com/prathambhilare</a>
                       </div>
                   </div>
               </div>
           </div>
       </section>
       
       <footer>
           <p>© 2025 Pratham Bhilare. All rights reserved.</p>
           <p>Portfolio designed with <i class="fas fa-heart" style="color: var(--accent);"></i> and modern web technologies</p>
       </footer>
       </div>
   
   <script>
       // Add smooth scrolling for navigation
       document.querySelectorAll('a[href^="#"]').forEach(anchor => {
           anchor.addEventListener('click', function(e) {
               e.preventDefault();
               document.querySelector(this.getAttribute('href')).scrollIntoView({
                   behavior: 'smooth'
               });
           });
       });
       
       // Add animation to elements when they come into view
       const observer = new IntersectionObserver((entries) => {
           entries.forEach(entry => {
               if (entry.isIntersecting) {
                   entry.target.classList.add('animate');
               }
           });
       }, { threshold: 0.1 });
       
       document.querySelectorAll('section').forEach(section => {
           observer.observe(section);
       });
   </script>
</body>
</html>
