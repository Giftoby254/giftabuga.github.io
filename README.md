<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="description" content="Gift Abuga - Nairobi-based Web Developer creating beautiful, fast, and responsive websites." />
  <title>Gift Abuga | Web Developer Portfolio</title>

  <style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');

:root {
  --primary: #4f46e5;
  --secondary: #7c3aed;
  --accent: #22d3ee;
  --bg: #f9fafb;
  --text: #333;
  --white: #fff;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: 'Poppins', sans-serif;
}

body {
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
  scroll-behavior: smooth;
}

/* Navigation */
nav {
  background: rgba(255, 255, 255, 0.95);
  position: sticky;
  top: 0;
  z-index: 1000;
  display: flex;
  justify-content: center;
  gap: 2rem;
  padding: 1rem 2rem;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

nav a {
  color: var(--primary);
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

nav a:hover {
  color: var(--secondary);
}

/* Hero Section */
header.hero {
  background-image: url('https://images.unsplash.com/photo-1522202220652-31e0a3b20656?auto=format&fit=crop&w=1950&q=80');
  background-size: cover;
  background-position: center;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  text-align: center;
  color: var(--white);
}

header.hero::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5); /* overlay for readability */
  z-index: 1;
}

header.hero .hero-content {
  position: relative;
  z-index: 2;
}

header.hero h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.7);
}

header.hero p {
  font-size: 1.2rem;
  margin-bottom: 2rem;
  text-shadow: 1px 1px 8px rgba(0, 0, 0, 0.7);
}

.cta-btn {
  display: inline-block;
  background: var(--primary);
  color: var(--white);
  padding: 0.8rem 2rem;
  border-radius: 50px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
}

.cta-btn:hover {
  background: var(--secondary);
  transform: translateY(-3px);
}

/* Sections */
section {
  max-width: 1000px;
  margin: 3rem auto;
  background: var(--white);
  padding: 2.5rem;
  border-radius: 12px;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.08);
  transition: transform 0.3s ease;
}

section:hover {
  transform: translateY(-5px);
}

h2 {
  color: var(--primary);
  margin-bottom: 1.5rem;
  text-align: center;
}

/* Projects */
.projects {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}

.project {
  background: var(--bg);
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project img {
  width: 100%;
  display: block;
}

.project:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.project h3 a {
  color: var(--secondary);
  text-decoration: none;
}

.project h3 a:hover {
  text-decoration: underline;
}

/* Skills / Lists */
ul {
  list-style: none;
  padding-left: 1rem;
}

ul li::before {
  content: "✔ ";
  color: var(--accent);
  font-weight: bold;
}

/* Testimonials */
blockquote {
  font-style: italic;
  color: #555;
  border-left: 4px solid var(--secondary);
  padding-left: 1rem;
  margin: 1rem 0;
  background: #f0f4ff;
  border-radius: 8px;
}

/* Footer */
footer {
  text-align: center;
  padding: 2rem 1rem;
  background: var(--primary);
  color: var(--white);
}

footer a {
  color: var(--white);
  text-decoration: none;
  font-weight: bold;
}

footer a:hover {
  text-decoration: underline;
}

/* Responsive Text */
@media (max-width: 768px) {
  header.hero h1 {
    font-size: 2.2rem;
  }
  
  header.hero p {
    font-size: 1rem;
  }
  
  .cta-btn {
    padding: 0.6rem 1.5rem;
  }
}
  </style>
</head>
<body>

  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
  </nav>

  <header id="home">
    <h1>Gift Abuga</h1>
    <p>Web Developer • Nairobi, Kenya</p>
    <a href="mailto:giftabuga@gmail.com" class="cta-btn">Hire Me</a>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <p>
      I’m <strong>Gift Abuga</strong>, a Nairobi-based web developer who builds
      modern, responsive websites that deliver results. My passion is creating
      elegant designs that are both functional and user-friendly.
    </p>
  </section>

  <section id="projects">
    <h2>Featured Projects</h2>
    <div class="projects">
      <div class="project">
        <h3><a href="https://www.kenyatours.co.ke/" target="_blank">Kenya Tours</a></h3>
        <p>Travel & safari booking platform with clean visuals and user-focused design.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.builditkenya.com/" target="_blank">Buildit Kenya</a></h3>
        <p>Professional construction website showcasing services and portfolio.</p>
      </div>
      <div class="project">
        <h3><a href="https://goldenstar.co.ke/" target="_blank">Goldenstar Restaurant</a></h3>
        <p>Restaurant site featuring menu display, gallery, and contact information.</p>
      </div>
    </div>
  </section>

  <section id="skills">
    <h2>Tools & Skills</h2>
    <ul>
      <li>Frontend: HTML, CSS, JavaScript</li>
      <li>Backend / CMS: WordPress, PHP</li>
      <li>Design: Figma, Canva</li>
      <li>SEO: Google Analytics, Search Console</li>
      <li>Hosting: Netlify, Vercel, GitHub Pages</li>
    </ul>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>📧 <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
    <p>📱 <a href="tel:+254111971411">+254 111 971 411</a></p>
  </section>

  <footer>
    <p>© 2025 Gift Abuga — Web Developer</p>
    <p><a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a> | <a href="tel:+254111971411">+254 111 971 411</a></p>
  </footer>

</body>
</html>
