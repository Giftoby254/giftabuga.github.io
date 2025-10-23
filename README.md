
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gift Abuga | Web Developer Portfolio</title>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');

    :root {
      --primary: #4f46e5;
      --secondary: #7c3aed;
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

    /* NAVIGATION */
    nav {
      background: rgba(255, 255, 255, 0.95);
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
    }

    nav .logo {
      font-weight: 700;
      font-size: 1.2rem;
      color: var(--primary);
    }

    .nav-links {
      display: flex;
      gap: 2rem;
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

    .menu-toggle {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }

    .menu-toggle span {
      background: var(--primary);
      height: 3px;
      width: 25px;
      margin: 4px 0;
      transition: all 0.3s ease;
    }

    /* HERO SECTION */
    header.hero {
      background: url('https://images.unsplash.com/photo-1522202220652-31e0a3b20656?auto=format&fit=crop&w=1950&q=100') no-repeat center center;
      background-size: cover;
      height: 100vh;
      width: 100%;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
    }

    header.hero::after {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.5);
      z-index: 1;
    }

    header.hero .hero-content {
      position: relative;
      z-index: 2;
      max-width: 800px;
      padding: 2rem;
      animation: fadeInUp 1.5s ease-in-out;
    }

    header.hero h1 {
      font-size: 3.5rem;
      margin-bottom: 1rem;
      text-shadow: 2px 2px 12px rgba(0, 0, 0, 0.5);
    }

    header.hero p {
      font-size: 1.3rem;
      margin-bottom: 2rem;
      text-shadow: 1px 1px 8px rgba(0, 0, 0, 0.4);
    }

    header.hero .cta-btn {
      display: inline-block;
      background: #ffffff;
      color: #4f46e5;
      padding: 1rem 2rem;
      border-radius: 50px;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.3s ease;
    }

    header.hero .cta-btn:hover {
      background: rgba(255, 255, 255, 0.9);
      color: #7c3aed;
      transform: translateY(-3px);
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* SECTIONS */
    section {
      max-width: 1000px;
      margin: 5rem auto;
      background: var(--white);
      padding: 3rem;
      border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }

    h2 {
      color: var(--primary);
      margin-bottom: 1rem;
      text-align: center;
    }

    p {
      text-align: center;
    }

    /* PROJECTS */
    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }

    .project {
      background: var(--bg);
      padding: 1rem;
      border-radius: 8px;
      border-left: 5px solid var(--secondary);
      transition: transform 0.3s ease;
    }

    .project:hover {
      transform: translateY(-5px);
    }

    .project img {
      width: 100%;
      border-radius: 8px;
      margin-bottom: 0.8rem;
    }

    .project h3 a {
      color: var(--secondary);
      text-decoration: none;
    }

    .project h3 a:hover {
      text-decoration: underline;
    }

    /* TESTIMONIALS */
    .testimonials {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }

    .testimonial {
      background: var(--bg);
      border-left: 5px solid var(--primary);
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }

    .testimonial p {
      font-style: italic;
      margin-bottom: 0.8rem;
    }

    .testimonial h4 {
      color: var(--secondary);
      font-weight: 600;
    }

    /* ANALYTICS */
    .analytics {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
      gap: 2rem;
      text-align: center;
    }

    .analytics div {
      flex: 1;
      min-width: 150px;
      background: var(--bg);
      border-radius: 10px;
      padding: 1.5rem;
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    }

    .analytics h3 {
      font-size: 2rem;
      color: var(--primary);
    }

    .analytics p {
      font-size: 1rem;
      color: var(--text);
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 2rem 1rem;
      background: var(--primary);
      color: var(--white);
      margin-top: 3rem;
    }

    footer a {
      color: var(--white);
      text-decoration: none;
      font-weight: bold;
    }

    footer a:hover {
      text-decoration: underline;
    }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      .menu-toggle {
        display: flex;
      }

      .nav-links {
        display: none;
        position: absolute;
        top: 70px;
        right: 20px;
        background: #fff;
        flex-direction: column;
        gap: 1rem;
        padding: 1rem 2rem;
        box-shadow: 0 2px 8px rgba(0,0,0,0.15);
        border-radius: 8px;
      }

      .nav-links.active {
        display: flex;
      }

      header.hero h1 { font-size: 2.4rem; }
      header.hero p { font-size: 1rem; }
      header.hero .cta-btn { padding: 0.8rem 1.5rem; }
    }
  </style>
</head>

<body>
  <!-- Navigation -->
  <nav>
    <div class="logo">Gift Abuga</div>
    <div class="menu-toggle" id="menu-toggle">
      <span></span><span></span><span></span>
    </div>
    <div class="nav-links" id="nav-links">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#vision">Vision</a>
      <a href="#testimonials">Testimonials</a>
      <a href="#analytics">Analytics</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- Hero -->
  <header class="hero" id="home">
    <div class="hero-content">
      <h1>Gift Abuga</h1>
      <p>Web Developer • Building Modern, Responsive & Impactful Websites in Nairobi, Kenya</p>
      <a href="mailto:giftabuga@gmail.com" class="cta-btn">Hire Me</a>
    </div>
  </header>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <p>I’m <strong>Gift Abuga</strong>, a Nairobi-based web developer focused on crafting clean, high-performing websites that empower businesses and individuals to grow online.</p>
  </section>

  <!-- Vision -->
  <section id="vision">
    <h2>Vision & Goals</h2>
    <p>My vision is to help African entrepreneurs and companies thrive online through smart, scalable web solutions. My goal is to provide each client with a unique digital presence that drives engagement and results.</p>
  </section>

  <!-- Testimonials -->
  <section id="testimonials">
    <h2>What My Clients Say</h2>
    <div class="testimonials">
      <div class="testimonial">
        <p>"Gift redesigned our hotel website, and the new design doubled our online bookings. Excellent work!"</p>
        <h4>— Jane Muthoni, Hotel Manager</h4>
      </div>
      <div class="testimonial">
        <p>"Working with Gift was seamless. He understood our vision and brought it to life beautifully."</p>
        <h4>— Alex Juma, Travel Consultant</h4>
      </div>
      <div class="testimonial">
        <p>"He delivered our property website ahead of schedule and optimized it for search engines. Brilliant developer!"</p>
        <h4>— Brian Otieno, Buildit Kenya</h4>
      </div>
    </div>
  </section>

  <!-- Analytics -->
  <section id="analytics">
    <h2>My Web Impact</h2>
    <div class="analytics">
      <div><h3>50+</h3><p>Websites Developed</p></div>
      <div><h3>98%</h3><p>Client Retention</p></div>
      <div><h3>20K+</h3><p>Monthly Visitors on Client Sites</p></div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact</h2>
    <p>📧 <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
    <p>📱 <a href="tel:+254111971411">+254 111 971 411</a></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 Gift Abuga — Web Developer</p>
    <p><a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a> | <a href="tel:+254111971411">+254 111 971 411</a></p>
  </footer>

  <script>
    const toggle = document.getElementById('menu-toggle');
    const links = document.getElementById('nav-links');
    toggle.addEventListener('click', () => {
      links.classList.toggle('active');
    });
  </script>
</body>
</html>
