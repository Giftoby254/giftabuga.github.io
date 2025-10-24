
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gift Abuga | Professional Web Developer from Kenya</title>
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

    /* SECTIONS */
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

    /* HERO SECTION */
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

    /* ABOUT SECTION */
    #about {
      background: url('https://images.unsplash.com/photo-1581090700227-1e37b190418e?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      background-attachment: fixed;
      color: white;
      position: relative;
    }

    #about::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.6);
      z-index: 0;
    }

    .about-content {
      position: relative;
      z-index: 1;
      max-width: 900px;
      background: rgba(0,0,0,0.5);
      padding: 30px;
      border-radius: 10px;
      line-height: 1.7;
    }

    .about-content p {
      font-size: 1.05rem;
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

    /* TESTIMONIALS SECTION */
    #testimonials {
      background: url('https://images.unsplash.com/photo-1581093588401-22a3c1a8e3a8?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      background-attachment: fixed;
      color: white;
      position: relative;
    }

    #testimonials::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.6);
      z-index: 0;
    }

    .testimonial-container {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      max-width: 1100px;
      width: 100%;
    }

    .testimonial-card {
      background: rgba(255,255,255,0.1);
      border-radius: 10px;
      padding: 25px;
      backdrop-filter: blur(8px);
      transition: var(--transition);
      line-height: 1.6;
    }

    .testimonial-card:hover {
      transform: translateY(-5px);
      background: rgba(255,255,255,0.25);
    }

    .testimonial-card h4 {
      color: #00ff88;
      margin-top: 15px;
    }

    /* PRICING SECTION */
    #pricing {
      background: url('https://images.unsplash.com/photo-1605902711622-cfb43c4437d1?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      background-attachment: fixed;
      color: white;
      position: relative;
    }

    #pricing::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.6);
      z-index: 0;
    }

    .pricing-container {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      max-width: 1100px;
      width: 100%;
    }

    .pricing-card {
      background: rgba(255,255,255,0.1);
      border-radius: 10px;
      padding: 25px;
      backdrop-filter: blur(8px);
      transition: var(--transition);
    }

    .pricing-card:hover {
      transform: translateY(-5px);
      background: rgba(255,255,255,0.25);
    }

    .pricing-card h3 {
      color: #00ff88;
      margin-bottom: 10px;
    }

    .pricing-card p {
      margin: 5px 0;
    }

    .pricing-price {
      font-size: 1.6rem;
      font-weight: bold;
      color: #fff;
      margin-top: 15px;
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

    footer {
      text-align: center;
      background: var(--primary);
      color: white;
      padding: 20px;
    }

    .social-icons a {
      margin: 0 10px;
      display: inline-block;
    }

    .social-icons img {
      width: 30px;
      height: 30px;
      filter: brightness(0) invert(1);
      transition: var(--transition);
    }

    .social-icons img:hover {
      transform: scale(1.1);
    }

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
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#testimonials">Testimonials</a></li>
      <li><a href="#pricing">Pricing</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HOME -->
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

  <!-- ABOUT -->
  <section id="about">
    <div class="about-content">
      <h2>About Me</h2>
      <p>I'm <strong>Gift Abuga</strong>, a professional web developer and digital solutions expert based in Kenya. With over 5 years of experience, I craft responsive, scalable, and user-centered web applications that help businesses grow and connect with their customers. I specialize in front-end and back-end technologies, ensuring that each project I deliver is fast, secure, and visually stunning.</p>
      <p>My expertise spans HTML, CSS, JavaScript, PHP, Laravel, React, and UX strategy. I’m passionate about turning great ideas into functional, high-performing digital products that empower businesses to thrive in an ever-changing digital world.</p>
      <h2>Our Vision</h2>
      <p>To empower African and global businesses with transformative digital tools and user-focused design, bridging technology and creativity to build a connected and prosperous digital ecosystem.</p>
    </div>
  </section>

  <!-- PROJECTS -->
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

  <!-- TESTIMONIALS -->
  <section id="testimonials">
    <h2>Testimonials</h2>
    <div class="testimonial-container">
      <div class="testimonial-card">
        <p>"Gift transformed our tour company’s online presence into something truly world-class. Our website now attracts more visitors, loads faster, and converts leads effortlessly. His attention to detail and professionalism made the entire experience smooth and stress-free."</p>
        <h4>– Wanjiku Mwangi, CEO, Touch Wild Tours</h4>
      </div>
      <div class="testimonial-card">
        <p>"We needed a website that would stand out in the competitive real estate industry, and Gift delivered beyond expectations. His UI/UX approach brought our brand to life with a sleek, modern look and user experience that keeps our clients engaged."</p>
        <h4>– Kevin Otieno, Manager, Nyumba Zetu Property</h4>
      </div>
      <div class="testimonial-card">
        <p>"From concept to deployment, Gift was an absolute professional. He not only developed our eCommerce platform but also guided us on SEO, hosting, and scalability. Our online sales have grown tremendously since the launch."</p>
        <h4>– Sarah Muthoni, Founder, EcoStyle Kenya</h4>
      </div>
    </div>
  </section>

  <!-- PRICING -->
  <section id="pricing">
    <h2>Website Packages (Kenyan Rates)</h2>
    <div class="pricing-container">
      <div class="pricing-card">
        <h3>Basic Website</h3>
        <p>Ideal for small businesses or personal portfolios</p>
        <p>✔ Up to 3 pages (Home, About, Contact)</p>
        <p>✔ Mobile Responsive</p>
        <p>✔ Basic SEO setup</p>
        <p>✔ Delivery: 3–5 days</p>
        <p class="pricing-price">One-time: KES 25,000</p>
        <p>Maintenance: KES 3,000/year</p>
      </div>
      <div class="pricing-card">
        <h3>Standard Website</h3>
        <p>Perfect for SMEs and service-based companies</p>
        <p>✔ Up to 7 pages</p>
        <p>✔ Custom Design + Blog Setup</p>
        <p>✔ Analytics Integration</p>
        <p>✔ SEO Optimization</p>
        <p>✔ Delivery: 5–7 days</p>
        <p class="pricing-price">One-time: KES 45,000</p>
        <p>Maintenance: KES 5,000/year</p>
      </div>
      <div class="pricing-card">
        <h3>Dynamic Website</h3>
        <p>Best for eCommerce or database-driven systems</p>
        <p>✔ Unlimited Pages</p>
        <p>✔ Admin Dashboard</p>
        <p>✔ Payment Integration</p>
        <p>✔ SEO + Analytics</p>
        <p>✔ Delivery: 10–14 days</p>
        <p class="pricing-price">One-time: KES 85,000</p>
        <p>Maintenance: KES 10,000/year</p>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="contact-content">
      <h2>Get in Touch</h2>
      <p>Email: <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
      <p>WhatsApp: <a href="https://wa.me/254111971411?text=Hi%20Gift,%20I%20want%20to%20discuss%20a%20project.">Chat on WhatsApp</a></p>
      <form>
        <input type="text" placeholder="Your Name" required />
        <input type="email" placeholder="Your Email" required />
        <textarea placeholder="Your Message" rows="5"></textarea>
        <button type="submit">Send Message</button>
      </form>
      <div class="social-icons">
        <a href="https://www.linkedin.com/in/gift-abuga/" target="_blank"><img src="https://img.icons8.com/ios-filled/50/linkedin.png" alt="LinkedIn"></a>
        <a href="https://wa.me/254111971411" target="_blank"><img src="https://img.icons8.com/color/48/whatsapp.png" alt="WhatsApp"></a>
      </div>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 Gift Abuga | Professional Web Developer | All Rights Reserved.</p>
  </footer>
</body>
</html>
