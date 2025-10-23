
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Gift Abuga - Nairobi-based Web Developer creating beautiful, responsive, and modern websites.">
  <title>Gift Abuga | Web Developer Portfolio</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --primary: #4f46e5;
      --secondary: #7c3aed;
      --accent: #ff5a5f;
      --bg: #f9fafb;
      --text: #333;
      --white: #fff;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Poppins', sans-serif; }
    body { background: var(--bg); color: var(--text); scroll-behavior: smooth; line-height: 1.6; }

    /* Navigation */
    nav {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      background: rgba(255, 255, 255, 0.95);
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
      z-index: 1000;
    }
    nav .logo { font-weight: 700; color: var(--primary); font-size: 1.2rem; }
    nav .links a {
      margin: 0 1rem;
      text-decoration: none;
      color: var(--primary);
      font-weight: 500;
      transition: 0.3s;
    }
    nav .links a:hover { color: var(--secondary); }
    .toggle-btns { display: flex; align-items: center; gap: 0.5rem; }
    .toggle-btns button {
      border: none; background: var(--primary); color: #fff;
      padding: 0.4rem 1rem; border-radius: 25px; cursor: pointer; font-weight: 500;
    }
    .toggle-btns button.active { background: var(--secondary); }

    /* Hero Section */
    header.hero {
      background: url('https://images.unsplash.com/photo-1522202220652-31e0a3b20656?auto=format&fit=crop&w=1950&q=80') no-repeat center center/cover;
      height: 100vh;
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
      background: rgba(0,0,0,0.5);
    }
    .hero-content {
      z-index: 2;
      position: relative;
      padding: 2rem;
      animation: fadeIn 2s ease-in-out;
    }
    .hero-content h1 { font-size: 3rem; margin-bottom: 1rem; text-shadow: 2px 2px 8px rgba(0,0,0,0.5); }
    .hero-content p { font-size: 1.3rem; margin-bottom: 2rem; text-shadow: 1px 1px 6px rgba(0,0,0,0.5); }
    .cta-btn {
      background: var(--primary); color: #fff;
      padding: 0.8rem 2rem; border-radius: 50px;
      font-weight: 600; text-decoration: none; transition: all 0.3s;
    }
    .cta-btn:hover { background: var(--secondary); }

    @keyframes fadeIn { from { opacity: 0; transform: translateY(30px);} to { opacity: 1; transform: translateY(0);} }

    section {
      max-width: 1000px; margin: 4rem auto; background: var(--white);
      padding: 2rem; border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }
    h2 { color: var(--primary); text-align: center; margin-bottom: 1.5rem; }

    /* Vision Section */
    .vision-goals {
      text-align: center;
      background: linear-gradient(135deg, #f9f9ff, #eef2ff);
      padding: 2rem;
      border-radius: 12px;
      background-image: url('https://images.unsplash.com/photo-1581091012184-5c3584b9c3b1?auto=format&fit=crop&w=1350&q=80');
      background-size: cover;
      background-position: center;
      color: #fff;
      position: relative;
    }
    .vision-goals::after {
      content: '';
      position: absolute;
      top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.6);
      z-index: 1;
      border-radius: 12px;
    }
    .vision-goals h3, .vision-goals p { position: relative; z-index: 2; }

    /* Projects */
    .projects.active {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }
    .project {
      background: var(--bg);
      border-radius: 8px;
      border-left: 5px solid var(--secondary);
      overflow: hidden;
      transition: transform 0.3s ease;
    }
    .project:hover { transform: translateY(-5px); }
    .project img { width: 100%; height: 180px; object-fit: cover; }
    .project-content { padding: 1rem; }
    .project h3 a { color: var(--secondary); text-decoration: none; }
    .project h3 a:hover { text-decoration: underline; }

    /* Testimonials */
    .testimonials { display: none; }
    .testimonials.active { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1rem; }
    .testimonial {
      background: #f3f4f6;
      padding: 1.2rem;
      border-left: 5px solid var(--primary);
      border-radius: 8px;
      text-align: center;
    }
    .testimonial img {
      width: 80px; height: 80px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 1rem;
    }
    .testimonial p { font-style: italic; margin-bottom: 0.5rem; }
    .testimonial span { color: var(--secondary); font-weight: 600; }

    /* Analytics */
    .analytics {
      display: flex;
      justify-content: space-around;
      align-items: center;
      flex-wrap: wrap;
      gap: 1.5rem;
      text-align: center;
      background-image: url('https://images.unsplash.com/photo-1556761175-4b46a572b786?auto=format&fit=crop&w=1350&q=80');
      background-size: cover;
      background-position: center;
      border-radius: 12px;
      padding: 2rem;
      color: white;
      position: relative;
    }
    .analytics::after {
      content: '';
      position: absolute;
      top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.6);
      border-radius: 12px;
    }
    .metric { position: relative; z-index: 2; flex: 1 1 200px; }
    .metric h3 { font-size: 2rem; color: var(--accent); }

    footer {
      background: var(--primary);
      color: #fff;
      text-align: center;
      padding: 2rem;
    }
    footer a { color: #fff; text-decoration:none; font-weight:bold; }
    footer a:hover { text-decoration: underline; }
  </style>
</head>
<body>

  <!-- Navigation -->
  <nav>
    <div class="logo">Gift Abuga</div>
    <div class="links">
      <a href="#home">Home</a>
      <a href="#vision">Vision</a>
      <a href="#projects">Portfolio</a>
      <a href="#contact">Contact</a>
    </div>
    <div class="toggle-btns">
      <button id="toggle-projects" class="active">Projects</button>
      <button id="toggle-testimonials">Testimonials</button>
    </div>
  </nav>

  <!-- Hero Section -->
  <header class="hero" id="home">
    <div class="hero-content">
      <h1>Gift Abuga</h1>
      <p>Web Developer • Nairobi, Kenya</p>
      <a href="#contact" class="cta-btn">Hire Me</a>
    </div>
  </header>

  <!-- Vision Section -->
  <section id="vision" class="vision-goals">
    <h2>My Vision & Goals</h2>
    <h3>Empowering African Businesses through Digital Innovation</h3>
    <p>
      My vision is to help Kenyan businesses grow their digital footprint through fast, scalable, and visually compelling websites.
      I aim to transform how brands connect with their audience online by providing tailored, results-driven web solutions.
    </p>
  </section>

  <!-- Projects -->
  <section id="projects">
    <h2>Portfolio Showcase</h2>

    <div class="projects active" id="projects-list">
      <div class="project">
        <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1000&q=80" alt="Afrikanest">
        <div class="project-content">
          <h3><a href="https://www.afrikanest.com/" target="_blank">Afrikanest</a></h3>
          <p>Property management platform built for seamless tenant payment tracking and reporting.</p>
        </div>
      </div>
      <div class="project">
        <img src="https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?auto=format&fit=crop&w=1000&q=80" alt="Dala">
        <div class="project-content">
          <h3><a href="https://www.dala.co.ke/" target="_blank">Dala</a></h3>
          <p>Responsive real estate platform with integrated management tools and listings.</p>
        </div>
      </div>
      <div class="project">
        <img src="https://images.unsplash.com/photo-1618220179428-22790b461013?auto=format&fit=crop&w=1000&q=80" alt="Marima Apartments">
        <div class="project-content">
          <h3><a href="https://www.marima.co.ke/" target="_blank">Marima</a></h3>
          <p>Website for modern apartment rentals with inquiry and booking integration.</p>
        </div>
      </div>
      <div class="project">
        <img src="https://images.unsplash.com/photo-1554995207-c18c203602cb?auto=format&fit=crop&w=1000&q=80" alt="Bomahut">
        <div class="project-content">
          <h3><a href="https://www.bomahut.com/" target="_blank">Bomahut</a></h3>
          <p>Smart property management solution for landlords and tenants in Kenya.</p>
        </div>
      </div>
      <div class="project">
        <img src="https://images.unsplash.com/photo-1505691723518-36a0f673d4f4?auto=format&fit=crop&w=1000&q=80" alt="WinguRent">
        <div class="project-content">
          <h3><a href="https://www.wingurent.com/" target="_blank">WinguRent</a></h3>
          <p>Digital rental management platform streamlining property operations across Kenya.</p>
        </div>
      </div>
    </div>

    <!-- Testimonials -->
    <div class="testimonials" id="testimonials-list">
      <div class="testimonial">
        <img src="https://images.unsplash.com/photo-1607746882042-944635dfe10e?auto=format&fit=crop&w=400&q=80" alt="Alex Juma">
        <p>"Gift built a professional and fast website that boosted our online visibility immensely."</p>
        <span>Alex Juma – Nairobi</span>
      </div>
      <div class="testimonial">
        <img src="https://images.unsplash.com/photo-1552374196-c4e7ffc6e126?auto=format&fit=crop&w=400&q=80" alt="Jane Muthoni">
        <p>"Our tourism site now attracts more clients thanks to Gift’s creative and responsive design."</p>
        <span>Jane Muthoni – Mombasa</span>
      </div>
      <div class="testimonial">
        <img src="https://images.unsplash.com/photo-1603415526960-f7e0328ad682?auto=format&fit=crop&w=400&q=80" alt="Michael Otieno">
        <p>"Reliable and professional. Gift brought our digital vision to life!"</p>
        <span>Michael Otieno – Kisumu</span>
      </div>
      <div class="testimonial">
        <img src="https://images.unsplash.com/photo-1607746882042-944635dfe10e?auto=format&fit=crop&w=400&q=80" alt="Grace Wanjiku">
        <p>"Our property website now converts more visitors into leads—amazing work!"</p>
        <span>Grace Wanjiku – Naivasha</span>
      </div>
    </div>
  </section>

  <!-- Analytics -->
  <section id="analytics">
    <h2>My Analytics</h2>
    <div class="analytics">
      <div class="metric">
        <h3>35+</h3>
        <p>Web Projects Completed</p>
      </div>
      <div class="metric">
        <h3>25+</h3>
        <p>Happy Clients Across Kenya</p>
      </div>
      <div class="metric">
        <h3>5+</h3>
        <p>Years of Experience</p>
      </div>
      <div class="metric">
        <h3>98%</h3>
        <p>Client Satisfaction</p>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form action="https://formspree.io/f/mqkvrynp" method="POST">
      <input type="text" name="name" placeholder="Your Name" required>
      <input type="email" name="_replyto" placeholder="Your Email" required>
      <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit" class="submit-btn">Send Message</button>
    </form>
  </section>

  <footer>
    <p>© 2025 Gift Abuga | Designed & Developed by Gift Abuga</p>
    <p><a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
  </footer>

  <script>
    const projectsBtn = document.getElementById('toggle-projects');
    const testimonialsBtn = document.getElementById('toggle-testimonials');
    const projectsList = document.getElementById('projects-list');
    const testimonialsList = document.getElementById('testimonials-list');

    projectsBtn.addEventListener('click', () => {
      projectsList.classList.add('active');
      testimonialsList.classList.remove('active');
      projectsBtn.classList.add('active');
      testimonialsBtn.classList.remove('active');
    });

    testimonialsBtn.addEventListener('click', () => {
      projectsList.classList.remove('active');
      testimonialsList.classList.add('active');
      testimonialsBtn.classList.add('active');
      projectsBtn.classList.remove('active');
    });
  </script>

</body>
</html>


