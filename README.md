
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="description" content="Gift Abuga - Nairobi-based Web Developer creating modern, responsive websites for Kenyan businesses." />
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

    /* Navigation */
    nav {
      background: rgba(255,255,255,0.95);
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      display: flex;
      justify-content: flex-end;
      gap: 2rem;
      padding: 1rem 3rem;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
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

    /* HERO SECTION */
    header.hero {
      background: url('https://images.unsplash.com/photo-1522202220652-31e0a3b20656?auto=format&fit=crop&w=2560&q=100') no-repeat center center/cover;
      min-height: 100vh;
      width: 100%;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
      background-attachment: fixed;
      background-repeat: no-repeat;
      background-size: cover;
      image-rendering: -webkit-optimize-contrast;
      image-rendering: crisp-edges;
      overflow: hidden;
    }

    header.hero::after {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.35);
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
      text-shadow: 2px 2px 12px rgba(0,0,0,0.5);
    }

    header.hero p {
      font-size: 1.3rem;
      margin-bottom: 2rem;
      text-shadow: 1px 1px 8px rgba(0,0,0,0.4);
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

    /* Sections */
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
    }

    .project h3 a {
      color: var(--secondary);
      text-decoration: none;
    }

    .project h3 a:hover {
      text-decoration: underline;
    }

    /* Testimonials */
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

    /* Analytics Section */
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

    /* Responsive */
    @media (max-width: 768px) {
      header.hero h1 { font-size: 2.2rem; }
      header.hero p { font-size: 1rem; }
      header.hero .cta-btn { padding: 0.8rem 1.5rem; }
    }
  </style>
</head>

<body>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href="#vision">Vision</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#analytics">Analytics</a>
    <a href="#contact">Contact</a>
  </nav>

  <header class="hero" id="home">
    <div class="hero-content">
      <h1>Gift Abuga</h1>
      <p>Web Developer • Building Fast, Responsive & Stunning Websites from Nairobi, Kenya</p>
      <a href="mailto:giftabuga@gmail.com" class="cta-btn">Hire Me</a>
    </div>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <p>
      I’m <strong>Gift Abuga</strong>, a Nairobi-based web developer dedicated to crafting elegant, functional, and user-friendly digital experiences.
      I specialize in responsive websites that deliver measurable results for businesses.
    </p>
  </section>

  <section id="projects">
    <h2>Featured Projects</h2>
    <div class="projects">
      <div class="project">
        <h3><a href="https://www.kenyatours.co.ke/" target="_blank">Kenya Tours</a></h3>
        <p>Travel & safari booking platform designed with a seamless user interface for smooth exploration.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.builditkenya.com/" target="_blank">Buildit Kenya</a></h3>
        <p>Professional construction & property management website with portfolio and client showcases.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.sunafricahotels.com/" target="_blank">Sun Africa Hotels</a></h3>
        <p>Elegant hospitality website offering online bookings and beautiful photo galleries for Kenyan resorts.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.jambotoursandtravel.com/" target="_blank">Jambo Tours & Travel</a></h3>
        <p>Tour operator website that simplifies trip planning and travel inquiries.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.silverstoneair.com/" target="_blank">Silverstone Air</a></h3>
        <p>Airline website focusing on user experience, mobile responsiveness, and online flight booking.</p>
      </div>
    </div>
  </section>

  <section id="vision">
    <h2>Vision & Goals</h2>
    <p>
      My vision is to empower African businesses through modern, affordable, and effective web solutions.  
      I aim to help clients grow by combining creativity, data, and technology into seamless experiences.
    </p>
  </section>

  <section id="testimonials">
    <h2>What My Clients Say</h2>
    <div class="testimonials">
      <div class="testimonial">
        <p>"Gift brought our hotel website to life with a modern touch and smooth booking functionality. Highly recommended!"</p>
        <h4>— Jane Muthoni, Hotel Manager</h4>
      </div>
      <div class="testimonial">
        <p>"His work on our travel platform exceeded expectations — sleek, fast, and user-friendly!"</p>
        <h4>— Alex Juma, CEO of Jambo Tours</h4>
      </div>
      <div class="testimonial">
        <p>"Professional and detail-oriented. Gift transformed our brand presence with a stunning website."</p>
        <h4>— Brian Otieno, Buildit Kenya</h4>
      </div>
    </div>
  </section>

  <section id="analytics">
    <h2>My Web Impact</h2>
    <div class="analytics">
      <div>
        <h3>50+</h3>
        <p>Websites Built</p>
      </div>
      <div>
        <h3>100%</h3>
        <p>Client Satisfaction</p>
      </div>
      <div>
        <h3>10K+</h3>
        <p>Monthly Visitors on Client Sites</p>
      </div>
    </div>
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
