<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gift Abuga | Web Developer from Kenya</title>
  <link rel="icon" href="https://img.icons8.com/color/48/000000/code.png" />
  <style>
    :root {
      --primary: #00a859;
      --secondary: #006b3c;
      --light: #f9f9f9;
      --dark: #222;
      --transition: 0.3s ease-in-out;
    }

    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      background: var(--light);
      color: var(--dark);
      scroll-behavior: smooth;
    }

    /* NAVIGATION */
    nav {
      background: var(--primary);
      padding: 12px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    }

    nav ul {
      display: flex;
      list-style: none;
      margin: 0;
      padding: 0;
    }

    nav ul li {
      margin: 0 20px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      transition: var(--transition);
    }

    nav ul li a:hover {
      color: #e0e0e0;
    }

    /* SECTIONS BASE */
    section {
      min-height: 100vh;
      padding: 80px 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-align: center;
    }

    h2 {
      color: var(--primary);
      margin-bottom: 20px;
      font-size: 2rem;
    }

    /* HERO / HOME SECTION */
    #home {
      background: url('https://images.unsplash.com/photo-1519389950473-47ba0277781c?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      position: relative;
      color: white;
    }

    #home::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0, 0, 0, 0.55);
      z-index: 0;
    }

    .hero-content {
      position: relative;
      z-index: 1;
      max-width: 700px;
    }

    .hero-content h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }

    .hero-content p {
      font-size: 1.2rem;
      margin-bottom: 30px;
    }

    .cta-buttons a {
      display: inline-block;
      margin: 5px 10px;
      padding: 12px 25px;
      background: var(--primary);
      color: white;
      border-radius: 5px;
      text-decoration: none;
      font-weight: bold;
      transition: var(--transition);
    }

    .cta-buttons a:hover {
      background: var(--secondary);
    }

    /* PROJECTS SECTION */
    #projects {
      background: url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      background-attachment: fixed;
      color: white;
      text-shadow: 0 2px 6px rgba(0,0,0,0.7);
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      max-width: 1100px;
      width: 100%;
      z-index: 1;
    }

    .project-card {
      background: rgba(255, 255, 255, 0.15);
      border-radius: 10px;
      padding: 15px;
      backdrop-filter: blur(5px);
      transition: var(--transition);
    }

    .project-card:hover {
      transform: translateY(-5px);
      background: rgba(255,255,255,0.3);
    }

    .project-card img {
      width: 100%;
      border-radius: 8px;
      height: 180px;
      object-fit: cover;
    }

    .project-card h3 {
      margin: 10px 0;
      color: #fff;
    }

    .project-card a {
      color: #fff;
      text-decoration: underline;
      font-weight: bold;
    }

    /* CONTACT SECTION */
    #contact {
      background: url('https://images.unsplash.com/photo-1521737604893-d14cc237f11d?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      color: white;
      position: relative;
    }

    #contact::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0, 0, 0, 0.6);
      z-index: 0;
    }

    .contact-content {
      position: relative;
      z-index: 1;
      background: rgba(0,0,0,0.5);
      padding: 30px;
      border-radius: 10px;
      max-width: 600px;
      width: 100%;
    }

    .contact-content p a {
      color: #00ff88;
      text-decoration: none;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: 20px;
    }

    input, textarea {
      padding: 10px;
      border: none;
      border-radius: 5px;
      width: 100%;
      font-size: 1rem;
    }

    button {
      background: var(--primary);
      color: white;
      border: none;
      padding: 12px;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
      transition: var(--transition);
    }

    button:hover {
      background: var(--secondary);
    }

    /* FOOTER */
    footer {
      text-align: center;
      background: var(--primary);
      color: white;
      padding: 20px;
    }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      .hero-content h1 {
        font-size: 2.2rem;
      }
      .hero-content p {
        font-size: 1rem;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HOME SECTION -->
  <section id="home">
    <div class="hero-content">
      <h1>Gift Abuga</h1>
      <p>Web Developer • UI/UX Designer • Tech Consultant from Kenya</p>
      <div class="cta-buttons">
        <a href="#projects">View My Projects</a>
        <a href="#contact">Hire Me</a>
      </div>
    </div>
  </section>

  <!-- PROJECTS SECTION -->
  <section id="projects">
    <h2>Projects</h2>
    <div class="projects-grid">
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1556761175-5973dc0f32e7?auto=format&fit=crop&w=800&q=80" alt="Touch Wild Tours">
        <h3>Touch Wild Tours</h3>
        <a href="https://touchwild.co.ke/" target="_blank">Visit Site</a>
      </div>
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=800&q=80" alt="Pega Tours Kenya">
        <h3>Pega Tours Kenya</h3>
        <a href="https://pegatours.co.ke/" target="_blank">Visit Site</a>
      </div>
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1560518883-ce09059eeffa?auto=format&fit=crop&w=800&q=80" alt="Nyumba Zetu Property">
        <h3>Nyumba Zetu Property</h3>
        <a href="https://www.nyumbazetu.com/" target="_blank">Visit Site</a>
      </div>
    </div>
  </section>

  <!-- CONTACT SECTION -->
  <section id="contact">
    <div class="contact-content">
      <h2>Contact Me</h2>
      <p>Email: <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
      <p>WhatsApp: <a href="https://wa.me/254111971411" target="_blank">Chat on WhatsApp</a></p>

      <form>
        <input type="text" placeholder="Your Name" required />
        <input type="email" placeholder="Your Email" required />
        <textarea placeholder="Your Message" rows="5" required></textarea>
        <button type="submit">Send Message</button>
      </form>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>&copy; 2025 Gift Abuga. All rights reserved.</p>
  </footer>

</body>
</html>
