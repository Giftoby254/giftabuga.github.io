
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Gift Abuga | Kenyan Web Developer</title>
  <link rel="icon" href="https://img.icons8.com/color/48/000000/code.png" />
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      background: #f9f9f9;
      color: #333;
    }

    nav {
      background: #00a859;
      padding: 10px;
      position: sticky;
      top: 0;
      z-index: 1000;
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
      font-weight: bold;
    }

    .hero {
      background-image: url('https://source.unsplash.com/1600x900/?kenya,technology');
      background-size: cover;
      background-position: center;
      height: 100vh;
      position: relative;
      color: white;
    }

    .overlay {
      background-color: rgba(0, 0, 0, 0.6);
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 0 20px;
    }

    .cta {
      margin-top: 20px;
      padding: 12px 24px;
      background-color: #00a859;
      color: white;
      text-decoration: none;
      border-radius: 5px;
    }

    .section {
      padding: 60px 20px;
      max-width: 900px;
      margin: auto;
    }

    .section h2 {
      color: #00a859;
      margin-bottom: 20px;
    }

    .section ul {
      list-style: none;
      padding: 0;
    }

    .section ul li {
      margin-bottom: 10px;
    }

    .section a {
      color: #00a859;
      text-decoration: none;
      font-weight: bold;
    }

    blockquote {
      background: #fff;
      padding: 20px;
      margin: 20px 0;
      border-left: 5px solid #00a859;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
      margin-top: 20px;
    }

    input, textarea {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      background-color: #00a859;
      color: white;
      padding: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #00a859;
      color: white;
    }

    .whatsapp-icon {
      position: fixed;
      bottom: 20px;
      right: 20px;
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

  <section id="home" class="hero">
    <div class="overlay">
      <h1>Gift Abuga</h1>
      <p>Kenyan Web Developer | UI/UX Designer | Tech Consultant</p>
      <a href="#contact" class="cta">Let's Build Something Great</a>
    </div>
  </section>

  <section id="about" class="section">
    <h2>About Me</h2>
    <p>I'm Gift Abuga, a passionate web developer based in Kenya. I specialize in building responsive websites, optimizing user experience, and integrating modern tools for businesses across Africa.</p>
    <ul>
      <li>Languages: HTML, CSS, JavaScript, PHP</li>
      <li>Frameworks: React, Laravel</li>
      <li>Certifications: Google UX Design, Meta Frontend</li>
    </ul>
  </section>

  <section id="projects" class="section">
    <h2>Projects</h2>
    <ul>
      <li><a href="https://touchwild.co.ke/">Touch Wild Tours</a></li>
      <li><a href="https://pegatours.co.ke/">Pega Tours Kenya</a></li>
      <li><a href="https://www.nyumbazetu.com/">Nyumba Zetu Property</a></li>
    </ul>
  </section>

  <section id="services" class="section">
    <h2>Services</h2>
    <ul>
      <li>Website Design & Development</li>
      <li>UI/UX Consulting</li>
      <li>SEO Optimization</li>
      <li>Maintenance & Hosting</li>
    </ul>
  </section>

  <section id="testimonials" class="section">
    <h2>Testimonials</h2>
    <blockquote>"Gift's work is exceptional. Our site traffic doubled!" – Wanjiku, Tour Operator</blockquote>
    <blockquote>"Professional, timely, and creative. Highly recommended." – Kevin, Property Manager</blockquote>
  </section>

  <section id="contact" class="section">
    <h2>Contact Me</h2>
    <p>Email: <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
    <p>WhatsApp: <a href="https://wa.me/254111971411?text=let's%20partner%20in%20a%20project.">Chat Now</a></p>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message"></textarea>
      <button type="submit">Send</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 Gift Abuga. All rights reserved.</p>
  </footer>

  <div class="whatsapp-icon">
    <a href="https://wa.me/254111971411?text=let's%20partner%20in%20a%20project." target="_blank">
      <img src="https://img.icons8.com/color/48/000000/whatsapp.png" alt="Chat with us on WhatsApp" />
    </a>
  </div>
</body>
</html>
