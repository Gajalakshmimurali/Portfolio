# Ex01 Portfolio
## Date:13:08:2025

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
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gaja's Portfolio</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Roboto:wght@400;500&display=swap');

/* Reset */
* { margin: 0; padding: 0; box-sizing: border-box; }

/* Body & Background */
body {
    font-family: 'Roboto', sans-serif;
    background: linear-gradient(135deg, #1b1b2f, #0f0f1a);
    color: #e0e0e0;
    overflow-x: hidden;
}

/* Header / Hero */
header {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 4rem 2rem;
    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(5px);
}
header img {
    width: 160px;
    height: 160px;
    border-radius: 50%;
    border: 3px solid #00ffd5;
    margin-bottom: 1rem;
    object-fit: cover;
    box-shadow: 0 0 20px rgba(0,255,213,0.4);
}
header h1 {
    font-family: 'Orbitron', sans-serif;
    font-size: 3rem;
    color: #00ffd5;
    letter-spacing: 2px;
}
header p {
    margin-top: 0.5rem;
    font-size: 1.2rem;
    color: #c0c0c0;
}
nav {
    margin-top: 1.5rem;
}
nav a {
    margin: 0 1rem;
    text-decoration: none;
    color: #00ffd5;
    font-weight: 500;
    transition: 0.3s;
}
nav a:hover { color: #ffffff; }

/* Sections */
section {
    padding: 4rem 2rem;
    max-width: 1000px;
    margin: auto;
}
h2 {
    font-family: 'Orbitron', sans-serif;
    font-size: 2rem;
    color: #00ffd5;
    margin-bottom: 1rem;
    border-bottom: 2px solid #444;
    display: inline-block;
    padding-bottom: 0.2rem;
}

/* About Section */
#about p { font-size: 1.1rem; line-height: 1.6; margin-bottom: 1rem; }

/* Skills Section */
.skill-bar {
    background: rgba(255,255,255,0.1);
    border-radius: 12px;
    margin-bottom: 1rem;
    overflow: hidden;
}
.skill-bar span {
    display: block;
    height: 20px;
    width: 0;
    background: #00ffd5;
    border-radius: 12px;
    text-align: right;
    padding-right: 10px;
    box-shadow: 0 0 10px rgba(0,255,213,0.4);
    line-height: 20px;
    color: #000;
    font-weight: bold;
    animation: fillBar 2s forwards;
}
@keyframes fillBar {
    0% { width: 0; }
    100% { width: var(--skill-width); }
}

/* Projects Section */
.project-card {
    background: rgba(0,255,213,0.05);
    padding: 1.5rem;
    margin: 1rem 0;
    border-radius: 15px;
    box-shadow: 0 0 10px rgba(0,255,213,0.3);
    transition: transform 0.3s, box-shadow 0.3s;
    position: relative;
    overflow: hidden;
}
.project-card:hover {
    transform: translateY(-10px) scale(1.02);
    box-shadow: 0 0 20px rgba(0,255,213,0.6);
}
.project-card h3 { color: #00ffd5; margin-bottom: 0.5rem; }
.project-card p { color: #c0c0c0; }

/* Contact Section */
#contact p a {
    color: #00ffd5;
    text-decoration: none;
}
#contact p a:hover { text-decoration: underline; }

/* Footer */
footer {
    text-align: center;
    padding: 2rem 1rem;
    border-top: 1px solid #444;
    color: #888;
}

/* Animations */
@keyframes float {
    0% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
    100% { transform: translateY(0); }
}
.project-card { animation: float 4s ease-in-out infinite; }
</style>
</head>
<body>

<header>
    <img src="mee.jpg" alt="Gaja's Photo">
    <h1>Gajalakshmi</h1>
    <p>Cybersecurity Enthusiast | Ethical Hacker | second-Year Engineering Student</p>
    <nav>
        <a href="#about">About Me</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section id="about">
    <h2>About Me</h2>
    <p>Hello! I'm Gajalakshmi, a passionate cybersecurity enthusiast and ethical hacking learner. I love exploring vulnerabilities, securing systems, and participating in Capture The Flag (CTF) challenges. As a first-year engineering student, I enjoy experimenting with coding projects, understanding web security, and learning networking protocols. My goal is to contribute to digital security while continually growing my technical skills.</p>
    <p>Besides technology, I enjoy problem-solving, learning new programming languages, and working on creative projects that showcase my abilities.</p>
</section>

<section id="skills">
    <h2>Skills</h2>
    <p>Hover or watch the animation to see proficiency levels.</p>
    <div class="skill-bar"><span style="--skill-width:90%;">Python 90%</span></div>
    <div class="skill-bar"><span style="--skill-width:85%;">Penetration Testing 85%</span></div>
    <div class="skill-bar"><span style="--skill-width:80%;">Web Security 80%</span></div>
    <div class="skill-bar"><span style="--skill-width:75%;">Networking 75%</span></div>
    <div class="skill-bar"><span style="--skill-width:70%;">Linux & Bash 70%</span></div>
</section>

<section id="projects">
    <h2>Projects</h2>
    <div class="project-card">
        <h3>Growtern Intern Management System</h3>
        <p>Managed intern workflows using Python and Django. Features include tracking, status updates, mentor assignment, and dashboard visualization. Focused on clean design and secure data handling.</p>
    </div>
    <div class="project-card">
        <h3>CTF Challenges</h3>
        <p>Completed multiple Capture The Flag challenges in web security, cryptography, and network exploitation. Gained hands-on experience with SQL injection, XSS, and network security concepts.</p>
    </div>
    <div class="project-card">
        <h3>Cybersecurity Scripts</h3>
        <p>Created Python scripts for scanning, password generation, and monitoring. Practiced secure coding standards and tested scripts in safe environments.</p>
    </div>
</section>

<section id="contact">
    <h2>Contact Me</h2>
    <p>Email: <a href="mailto:gajalakshmi@example.com">gajalakshmi@example.com</a></p>
    <p>LinkedIn: <a href="#">linkedin.com/in/gajalakshmi</a></p>
    <p>GitHub: <a href="#">GitHub/gajalakshmi</a></p>
    <p>Phone: +91-8668082120</p>
</section>

<footer>
    <p>&copy; 2025 Gajalakshmi</p>
</footer>

</body>
</html>
```

## OUTPUT
<img width="1919" height="1087" alt="Screenshot 2025-08-13 213514" src="https://github.com/user-attachments/assets/09d0b751-488b-45df-810a-885fed9f2905" />

<img width="1899" height="1081" alt="Screenshot 2025-08-13 213548" src="https://github.com/user-attachments/assets/90219c1f-f4b8-4456-97b7-50e494a04320" />


<img width="1899" height="1081" alt="Screenshot 2025-08-13 213548" src="https://github.com/user-attachments/assets/85431e34-9b06-4ee6-b20d-4b2b8f6b3718" />



## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
