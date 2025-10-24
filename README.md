<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gift Abuga | Kenyan Web Developer</title>
  <link rel="icon" href="https://img.icons8.com/color/48/000000/code.png" />
  <style>
    :root {
      --primary: #00a859;
      --secondary: #006b3c;
      --light: #f9f9f9;
      --dark: #333;
      --transition: 0.3s ease-in-out;
    }

    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      background: var(--light);
      color: var(--dark);
      scroll-behavior: smooth;
    }

    /* Navigation */
    nav {
      background: var(--primary);
      padding: 10px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    }

    nav ul {
      display: flex;
      justify-content: center;
      list-style: none;
      margin: 0;
      padding: 0;
    }

    nav ul li {
      margin: 0 15px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-weight: 600;
      transition: var(--transition);
    }

    nav ul li a:hover {
      color: #e0e0e0;
    }

    /* Hero Section */
    .hero {
      background-image: url('https://images.unsplash.com/photo-1556761175-5973dc0f32e7?auto=format&fit=crop&w=1600&q=80');
      background-size: cover;
      background-position: center;
      height: 100vh;
      color: white;
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .overlay {
      background-color: rgba(0, 0, 0, 0.6);
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 0 20px;
    }

    .overlay h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }

    .overlay p {
      font-size: 1.2rem;
      margin-bottom: 25px;
    }

    .cta {
      padding: 12px 24px;
      background-color: var(--primary);
      color: white;
      text-decoration: none;
      border-radius: 5px;
      transition: var(--transition);
    }

    .cta:hover {
      background-color: var(--secondary);
    }

    /* Section Styling */
    section {
      padding: 80px 20px;
      max-width: 1000px;
      margin: auto;
    }

    h2 {
      color: var(--primary);
      margin-bottom: 20px;
      text-align: center;
      font-size: 2rem;
    }

    ul {
      list-style: none;
      padding: 0;
    }

    ul li {
      margin-bottom: 10px;
    }

    a {
      color: var(--primary);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    /* Project Section */
    .project-list a {
      display: inline-block;
      margin: 10px 0;
      padding: 10px 15px;
      border: 1px solid var(--primary);
      border-radius: 5px;
      transition: var(--transition);
    }

    .project-list a:hover {
      background-color: var(--primary);
      color: white;
    }

    /* Testimonials */
    blockquote {
      background: #fff;
      padding: 20px;
      margin: 20px 0;
      border-left: 5px solid var(--primary);
      font-style: italic;
    }

    /* Contact Form */
    form {
      display: flex;
      flex-direction: column;
      gap: 12px;
      max-width: 600px;
      margin: 20px auto;
    }

    input, textarea {
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1rem;
      width: 100%;
    }

    textarea {
      resize: vertical;
      min-height: 120px;
    }

    button {
      background-color: var(--primary);
      color: white;
      padding: 12px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
      transition: var(--transition);
    }

    button:hover {
      background-color: var(--secondary);
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background: var(--primary);
      color: white;
      font-size: 0.9rem;
    }

    /* WhatsApp Icon */
    .whatsapp-icon {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 999;
    }

    .whatsapp-icon img {
      width: 50px;
      height: 50px;
      transition: var(--transition);
    }

    .whatsapp-icon img:hover {
      transform: scale(1.1);
    }

    @media (max-width: 768px) {
      .overlay h1 {
        font-size: 2.2rem;
      }

      .overlay p {
        font-size: 1rem;
      }

      nav ul {
        flex-wrap: wrap;
      }
    }
  </style>
</head>

<body>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#testimonials">Testimonials</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <header id="home" class="hero">
    <div class="overlay">
      <h1>Gift Abuga</h1>
      <p>Web Developer • UI/UX Designer • Tech Consultant</p>
      <a href="#contact" class="cta">Let's Build Something Great</a>
    </div>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <p>I'm <strong>Gift Abuga</strong>, a passionate web developer based in Kenya. I build responsive, modern websites and optimize digital experiences for businesses across Africa. My goal is to merge design with functionality for impactful online presence.</p>
    <ul>
      <li><strong>Languages:</strong> HTML, CSS, JavaScript, PHP</li>
      <li><strong>Frameworks:</strong> React, Laravel</li>
      <li><strong>Certifications:</strong> Google UX Design, Meta Frontend</li>
    </ul>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <div class="project-list">
      <a href="https://touchwild.co.ke/" target="_blank">Touch Wild Tours</a><br>
      <a href="https://pegatours.co.ke/" target="_blank">Pega Tours Kenya</a><br>
      <a href="https://www.nyumbazetu.com/" target="_blank">Nyumba Zetu Property</a>
    </div>
  </section>

  <section id="services">
    <h2>Services</h2>
    <ul>
      <li>Website Design & Development</li>
      <li>UI/UX Consulting</li>
      <li>SEO Optimization</li>
      <li>Maintenance & Hosting</li>
    </ul>
  </section>

  <section id="testimonials">
    <h2>Testimonials</h2>
    <blockquote>“Gift’s work is exceptional. Our site traffic doubled!” – Wanjiku, Tour Operator</blockquote>
    <blockquote>“Professional, timely, and creative. Highly recommended.” – Kevin, Property Manager</blockquote>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <p>Email: <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
    <p>WhatsApp: <a href="https://wa.me/254111971411?text=Let's%20partner%20on%20a%20project." target="_blank">Chat Now</a></p>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 Gift Abuga. All rights reserved.</p>
  </footer>

  <div class="whatsapp-icon">
    <a href="https://wa.me/254111971411?text=Let's%20partner%20on%20a%20project." target="_blank">
      <img src="https://img.icons8.com/color/96/whatsapp--v1.png" alt="Chat with Gift on WhatsApp" />
    </a>
  </div>
</body>
</html>

