
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="description" content="Gift Abuga - Nairobi-based Web Developer creating beautiful, fast, and responsive websites." />
  <title>Gift Abuga | Web Developer Portfolio</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
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
      position: sticky;
      top: 0;
      z-index: 1000;
      display: flex;
      justify-content: center;
      gap: 2rem;
      padding: 1rem;
      box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    }

    nav a {
      color: var(--primary);
      text-decoration: none;
      font-weight: 500;
    }

    nav a:hover {
      color: var(--secondary);
    }

    /* Hero Section */
    header {
      background: url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=1950&q=80') no-repeat center center;
      background-size: cover;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
      color: #fff;
    }

    header::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.5);
      z-index: 0;
    }

    header h1, header p, .cta-btn {
      position: relative;
      z-index: 1;
    }

    header h1 {
      font-size: 4rem;
      margin-bottom: 1rem;
    }

    header p {
      font-size: 1.5rem;
      margin-bottom: 2rem;
    }

    .cta-btn {
      display: inline-block;
      background: #ff6363;
      color: #fff;
      padding: 1rem 2.5rem;
      border-radius: 50px;
      font-weight: 600;
      text-decoration: none;
      font-size: 1.1rem;
      transition: 0.3s;
    }

    .cta-btn:hover {
      background: #7c3aed;
    }

    /* Sections */
    section {
      max-width: 1000px;
      margin: 3rem auto;
      background: var(--white);
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }

    h2 {
      color: var(--primary);
      margin-bottom: 1rem;
      text-align: center;
    }

    /* Projects */
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
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
    }

    .testimonial {
      background: var(--bg);
      padding: 1.5rem;
      border-radius: 10px;
      border-left: 5px solid var(--primary);
    }

    .testimonial p {
      font-style: italic;
      margin-bottom: 1rem;
    }

    .testimonial h4 {
      font-weight: 700;
      text-align: right;
      color: var(--secondary);
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

  </style>
</head>

<body>

  <nav>
    <a href="#home">Home</a>
    <a href="#projects">Projects</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- Hero Section -->
  <header id="home">
    <h1>Gift Abuga</h1>
    <p>Web Developer • Nairobi, Kenya</p>
    <a href="mailto:giftabuga@gmail.com" class="cta-btn">Hire Me</a>
  </header>

  <!-- Projects Section -->
  <section id="projects">
    <h2>My Work</h2>
    <div class="projects">
      <div class="project">
        <h3><a href="https://www.magicalkenya.com/" target="_blank">Magical Kenya</a></h3>
        <p>A travel and tourism website I developed showcasing Kenya’s destinations.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.safarilink.co.ke/" target="_blank">SafariLink</a></h3>
        <p>A booking platform for Kenyan safaris I designed and built.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.serenahotels.com/" target="_blank">Serena Hotels</a></h3>
        <p>Hospitality website for Serena Hotels in Kenya, fully responsive and modern.</p>
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials">
    <h2>Testimonials</h2>
    <div class="testimonials">
      <div class="testimonial">
        <p>"Gift created an amazing travel website for us. Very professional and timely."</p>
        <h4>- Alex Juma</h4>
      </div>
      <div class="testimonial">
        <p>"Our hotel bookings site looks fantastic thanks to Gift’s expertise!"</p>
        <h4>- Jane Muthoni</h4>
      </div>
      <div class="testimonial">
        <p>"Highly recommended! Gift delivered a responsive and sleek website."</p>
        <h4>- Peter Otieno</h4>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact Me</h2>
    <p style="text-align:center;">Interested in working together? Reach out via email:</p>
    <p style="text-align:center;"><a href="mailto:giftabuga@gmail.com" class="cta-btn">giftabuga@gmail.com</a></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 Gift Abuga. All Rights Reserved.</p>
    <p><a href="https://www.linkedin.com/in/gift-abuga/" target="_blank">LinkedIn</a> | <a href="https://github.com/giftabuga" target="_blank">GitHub</a></p>
  </footer>

</body>
</html>


