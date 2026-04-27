# Ex01 Portfolio
## Date: 27/04/2026

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
HTML
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Pradeep Kumar Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <header>
        <h1>Pradeep Kumar R</h1>
        <p>Aspiring Data Scientist</p>
    </header>

    <nav>
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#skills">Skills</a>
        <a href="#contact">Contact</a>
    </nav>

    <section id="about">
        <h2>About Me</h2>
        <p>
            Aspiring Data Scientist skilled in Python, Java, and DSA. Passionate about Machine Learning,
            Deep Learning, and Computer Vision with strong analytical problem-solving ability.
        </p>
    </section>

    <section id="projects">
        <h2>Projects</h2>

        <div class="card">
            <h3>LLM-Based College Chatbot</h3>
            <p>Developed AI chatbot using LLM and NLP for student assistance.</p>
        </div>

        <div class="card">
            <h3>IPL Data Pipeline</h3>
            <p>Built scalable pipeline using PySpark and Kafka for analytics.</p>
        </div>

    </section>

    <section id="skills">
        <h2>Skills</h2>
        <ul>
            <li>Python, Java, SQL, R</li>
            <li>PySpark, Kafka, AWS</li>
            <li>Power BI</li>
            <li>DSA, Machine Learning</li>
        </ul>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <p>Email: pradeeprajendran008@gmail.com</p>
        <p>Phone: +91 8807142567</p>
    </section>

    <footer>
        <p>© 2026 Pradeep Kumar</p>
    </footer>

</body>

</html>
```
CSS
```
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');

:root {
    --bg-color: #0f172a;
    --text-primary: #f8fafc;
    --text-secondary: #cbd5e1;
    --accent: #38bdf8;
    --accent-gradient: linear-gradient(135deg, #38bdf8, #818cf8);
    --card-bg: #1e293b;
    --card-border: rgba(255, 255, 255, 0.1);
}

html {
    scroll-behavior: smooth;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Inter', sans-serif;
    background-color: var(--bg-color);
    color: var(--text-primary);
    line-height: 1.6;
    overflow-x: hidden;
}

header {
    background: var(--card-bg);
    padding: 100px 20px;
    text-align: center;
    border-bottom: 1px solid var(--card-border);
    position: relative;
    overflow: hidden;
}

header::before {
    content: '';
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(56,189,248,0.05) 0%, transparent 60%);
    pointer-events: none;
}

header h1 {
    font-size: 3.5rem;
    font-weight: 700;
    background: var(--accent-gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 15px;
    animation: fadeInDown 0.8s ease-out;
}

header p {
    font-size: 1.3rem;
    color: var(--text-secondary);
    font-weight: 300;
    animation: fadeInUp 0.8s ease-out 0.2s both;
}

nav {
    display: flex;
    justify-content: center;
    background: rgba(15, 23, 42, 0.85);
    backdrop-filter: blur(12px);
    position: sticky;
    top: 0;
    z-index: 1000;
    border-bottom: 1px solid var(--card-border);
    padding: 15px 0;
}

nav a {
    color: var(--text-primary);
    padding: 10px 25px;
    margin: 0 10px;
    text-decoration: none;
    font-weight: 600;
    border-radius: 8px;
    transition: all 0.3s ease;
}

nav a:hover {
    background: var(--accent-gradient);
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 4px 15px rgba(56, 189, 248, 0.4);
}

section {
    max-width: 900px;
    margin: 80px auto;
    padding: 0 20px;
    animation: fadeIn 1s ease-out;
}

section h2 {
    font-size: 2.2rem;
    color: var(--accent);
    margin-bottom: 40px;
    position: relative;
    display: inline-block;
}

section h2::after {
    content: '';
    position: absolute;
    width: 60%;
    height: 4px;
    bottom: -10px;
    left: 0;
    background: var(--accent-gradient);
    border-radius: 2px;
}

section p {
    color: var(--text-secondary);
    font-size: 1.15rem;
}

.card {
    background: var(--card-bg);
    padding: 30px;
    margin: 25px 0;
    border-radius: 16px;
    border: 1px solid var(--card-border);
    transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    cursor: pointer;
}

.card:hover {
    transform: translateY(-6px);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
    border-color: rgba(56, 189, 248, 0.5);
}

.card h3 {
    color: var(--text-primary);
    font-size: 1.5rem;
    margin-bottom: 12px;
}

.card p {
    font-size: 1.05rem;
    color: var(--text-secondary);
}

#skills ul {
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    margin-top: 20px;
}

#skills li {
    background: rgba(56, 189, 248, 0.1);
    color: var(--accent);
    padding: 12px 25px;
    border-radius: 30px;
    font-weight: 600;
    font-size: 1.1rem;
    border: 1px solid rgba(56, 189, 248, 0.2);
    transition: all 0.3s ease;
    cursor: default;
}

#skills li:hover {
    background: var(--accent-gradient);
    color: white;
    transform: scale(1.05);
    box-shadow: 0 5px 15px rgba(56, 189, 248, 0.3);
}

#contact p {
    margin: 15px 0;
    font-size: 1.15rem;
    display: flex;
    align-items: center;
    gap: 10px;
}

footer {
    text-align: center;
    background: var(--card-bg);
    color: var(--text-secondary);
    padding: 40px;
    margin-top: 80px;
    border-top: 1px solid var(--card-border);
    font-size: 1rem;
}

/* Animations */
@keyframes fadeInDown {
    from { opacity: 0; transform: translateY(-30px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
```

## OUTPUT
<img width="928" height="864" alt="Screenshot 2026-04-27 141236" src="https://github.com/user-attachments/assets/9bbe99a4-e3d4-4c0f-9568-fa93d8373bb5" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
