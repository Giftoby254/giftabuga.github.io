
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
      --transition: 0.4s ease;
    }

    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      background: var(--light);
      color: var(--dark);
    }

    /* NAVIGATION */
    nav {
      background: var(--primary);
      padding: 14px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 3px 8px rgba(0,0,0,0.1);
    }

    nav ul {
      display: flex;
      justify-content: center;
      list-style: none;
      margin: 0;
      padding: 0;
      flex-wrap: wrap;
    }

    nav ul li {
      margin: 0 15px;
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
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    h2 {
      color: var(--primary);
      margin-bottom: 20px;
      font-size: 2rem;
    }

    /* HERO */
    #home {
      background: url('https://images.unsplash.com/photo-1519389950473-47ba0277781c?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
      position: relative;
      color: white;
      overflow: hidden;
    }

    #home::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.55);
      z-index: 0;
    }

    .hero-content {
      position: relative;
      z-index: 1;
      max-width: 700px;
      animation: fadeIn 2s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .hero-content h1 {
      font-size: 3rem;
    }

    .hero-content p {
      font-size: 1.2rem;
      margin: 15px 0 25px;
    }

    .cta-buttons a {
      background: var(--primary);
      padding: 12px 25px;
      color: white;
      border-radius: 6px;
      margin: 5px;
      text-decoration: none;
      font-weight: bold;
      transition: var(--transition);
    }

    .cta-buttons a:hover {
      background: var(--secondary);
    }

    /* ABOUT */
    #about {
      background: url('https://images.unsplash.com/photo-1581090700227-1e37b190418e?auto=format&fit=crop&w=1600&q=80') center/cover;
      color: white;
      position: relative;
    }

    #about::after {
      content: "";
      position: absolute;
      inset: 0;
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
    }

    /* PROJECTS */
    #projects {
      background: #fff;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      max-width: 1100px;
      width: 100%;
    }

    .project-card {
      background: #f3f3f3;
      border-radius: 10px;
      overflow: hidden;
      transition: var(--transition);
    }

    .project-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .project-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 20px rgba(0,0,0,0.15);
    }

    /* BLOG */
    #blog {
      background: #f8f8f8;
    }

    .blog-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      max-width: 1100px;
    }

    .blog-card {
      background: white;
      border-radius: 10px;
      overflow: hidden;
      transition: var(--transition);
    }

    .blog-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }

    .blog-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .blog-card h3 {
      margin: 15px;
      color: var(--primary);
    }

    .blog-card p {
      margin: 0 15px 15px;
      font-size: 0.95rem;
    }

    .read-more {
      background: var(--primary);
      color: white;
      display: inline-block;
      margin: 0 0 20px 15px;
      padding: 8px 16px;
      border-radius: 5px;
      text-decoration: none;
      transition: var(--transition);
    }

    .read-more:hover {
      background: var(--secondary);
    }

    /* TESTIMONIALS */
    #testimonials {
      background: url('https://images.unsplash.com/photo-1581093588401-22a3c1a8e3a8?auto=format&fit=crop&w=1600&q=80') center/cover;
      position: relative;
      color: white;
    }

    #testimonials::after {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.6);
      z-index: 0;
    }

    .testimonial-container {
      position: relative;
      z-index: 1;
      max-width: 1100px;
      display: grid;
      gap: 20px;
    }

    .testimonial-card {
      background: rgba(255,255,255,0.1);
      padding: 25px;
      border-radius: 10px;
      backdrop-filter: blur(6px);
    }

    /* PRICING */
    #pricing {
      background: #fff;
    }

    .pricing-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      max-width: 1100px;
      width: 100%;
    }

    .pricing-card {
      background: #f3f3f3;
      border-radius: 10px;
      padding: 25px;
      transition: var(--transition);
    }

    .pricing-card:hover {
      transform: scale(1.05);
      box-shadow: 0 5px 15px rgba(0,0,0,0.15);
    }

    /* CONTACT */
    #contact {
      background: url('https://images.unsplash.com/photo-1521737604893-d14cc237f11d?auto=format&fit=crop&w=1600&q=80') center/cover;
      position: relative;
      color: white;
    }

    #contact::after {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.6);
      z-index: 0;
    }

    .contact-content {
      position: relative;
      z-index: 1;
      background: rgba(0,0,0,0.5);
      padding: 30px;
      border-radius: 10px;
      max-width: 600px;
    }

    .social-icons a img {
      width: 30px;
      margin: 5px;
      filter: brightness(0) invert(1);
      transition: var(--transition);
    }

    .social-icons a img:hover {
      transform: scale(1.2);
    }

    /* FOOTER */
    footer {
      background: var(--primary);
      color: white;
      padding: 30px 20px;
      text-align: center;
    }

    .useful-links {
      margin: 10px 0;
    }

    .useful-links a {
      color: white;
      margin: 0 10px;
      text-decoration: none;
      font-weight: bold;
      transition: var(--transition);
    }

    .useful-links a:hover {
      text-decoration: underline;
    }

    @media (max-width: 768px) {
      .hero-content h1 { font-size: 2.2rem; }
      .hero-content p { font-size: 1rem; }
    }
  </style>
</head>
<body>

  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#blog">Blog</a></li>
      <li><a href="#testimonials">Testimonials</a></li>
      <li><a href="#pricing">Pricing</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <section id="home">
    <div class="hero-content">
      <h1>Gift Abuga</h1>
      <p>Building Modern, Interactive, and Scalable Websites for All Ages</p>
      <div class="cta-buttons">
        <a href="#projects">See My Work</a>
        <a href="#contact">Hire Me</a>
      </div>
    </div>
  </section>

  <section id="about">
    <div class="about-content">
      <h2>About Me</h2>
      <p>I’m <strong>Gift Abuga</strong>, a seasoned web developer and UI/UX designer from Kenya with a deep passion for digital innovation. My journey in technology is driven by creativity, inclusivity, and functionality — ensuring that every digital product I create is engaging and easy to use for people of all ages and backgrounds.</p>
      <p>I specialize in crafting high-performance websites and applications that merge clean design with robust code. I believe in the power of the web to connect, empower, and inspire.</p>
      <h2>Our Vision</h2>
      <p>To empower Africa and the world through technology that’s inclusive, accessible, and impactful — bridging the gap between creativity and functionality for every generation.</p>
    </div>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <div class="projects-grid">
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1556761175-5973dc0f32e7?auto=format&fit=crop&w=800&q=80" alt="Touch Wild Tours">
        <h3>Touch Wild Tours</h3>
        <p>Travel agency website showcasing tours and packages with booking integrations.</p>
      </div>
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=800&q=80" alt="Pega Tours Kenya">
        <h3>Pega Tours Kenya</h3>
        <p>Responsive tourism platform with gallery and dynamic itinerary builder.</p>
      </div>
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1560518883-ce09059eeffa?auto=format&fit=crop&w=800&q=80" alt="Nyumba Zetu Property">
        <h3>Nyumba Zetu Property</h3>
        <p>Real estate listing portal with admin dashboard and advanced filtering.</p>
      </div>
    </div>
  </section>

  <section id="blog">
    <h2>Latest Blog Posts</h2>
    <div class="blog-grid">
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1581276879432-15a19d654956?auto=format&fit=crop&w=800&q=80" alt="Web Trends">
        <h3>Top 5 Web Design Trends in 2025</h3>
        <p>Explore the latest in minimalism, accessibility, and interactivity shaping the modern web.</p>
        <a href="#" class="read-more">Read More</a>
      </div>
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1590608897129-79da98d159b4?auto=format&fit=crop&w=800&q=80" alt="UX Strategy">
        <h3>Designing for All Ages</h3>
        <p>How inclusive UX and responsive design can make technology accessible to everyone.</p>
        <a href="#" class="read-more">Read More</a>
      </div>
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1532619675605-1d9b53a68783?auto=format&fit=crop&w=800&q=80" alt="SEO Kenya">
        <h3>Why SEO Matters for Kenyan Businesses</h3>
        <p>Learn how to reach local and global clients through strategic optimization.</p>
        <a href="#" class="read-more">Read More</a>
      </div>
    </div>
  </section>

  <section id="testimonials">
    <h2>What Clients Say</h2>
    <div class="testimonial-container">
      <div class="testimonial-card">
        <p>"Gift’s technical expertise and attention to detail are unmatched. Our company website is not only beautiful but lightning fast. The results have been incredible!"</p>
        <h4>— Wanjiku Mwangi, Touch Wild Tours</h4>
      </div>
      <div class="testimonial-card">
        <p>"Working with Gift was a seamless experience. He understood our brand instantly and delivered an interactive, user-friendly platform that exceeded expectations."</p>
        <h4>— Kevin Otieno, Nyumba Zetu Property</h4>
      </div>
      <div class="testimonial-card">
        <p>"Professional, creative, and incredibly patient. Gift is a true partner in every sense. He goes above and beyond to make your digital vision a reality."</p>
        <h4>— Sarah Muthoni, EcoStyle Kenya</h4>
      </div>
    </div>
  </section>

  <section id="pricing">
    <h2>Website Packages (Kenyan Rates)</h2>
    <div class="pricing-container">
      <div class="pricing-card">
        <h3>Basic Website</h3>
        <p>For small businesses and personal portfolios</p>
        <p><strong>One-time:</strong> KES 25,000</p>
        <p><strong>Maintenance:</strong> KES 3,000/year</p>
      </div>
      <div class="pricing-card">
        <h3>Standard Website</h3>
        <p>For SMEs and service-based brands</p>
        <p><strong>One-time:</strong> KES 45,000</p>
        <p><strong>Maintenance:</strong> KES 5,000/year</p>
      </div>
      <div class="pricing-card">
        <h3>Dynamic Website</h3>
        <p>For eCommerce and large enterprises</p>
        <p><strong>One-time:</strong> KES 85,000</p>
        <p><strong>Maintenance:</strong> KES 10,000/year</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="contact-content">
      <h2>Get in Touch</h2>
      <p>Email: <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
      <p>WhatsApp: <a href="https://wa.me/254111971411">Chat on WhatsApp</a></p>
      <form>
        <input type="text" placeholder="Your Name" required />
        <input type="email" placeholder="Your Email" required />
        <textarea rows="5" placeholder="Your Message"></textarea>
        <button type="submit">Send Message</button>
      </form>
      <div class="social-icons">
        <a href="https://www.linkedin.com/in/gift-abuga/" target="_blank"><img src="https://img.icons8.com/ios-filled/50/linkedin.png" alt="LinkedIn"></a>
        <a href="https://wa.me/254111971411" target="_blank"><img src="https://img.icons8.com/color/48/whatsapp.png" alt="WhatsApp"></a>
      </div>
    </div>
  </section>

  <footer>
    <div class="useful-links">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#blog">Blog</a>
      <a href="#testimonials">Testimonials</a>
      <a href="#pricing">Pricing</a>
      <a href="#contact">Contact</a>
    </div>
    <p>&copy; 2025 Gift Abuga | Professional Web Developer | All Rights Reserved.</p>
  </footer>

</body>
</html>
