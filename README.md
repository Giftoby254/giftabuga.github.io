
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
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

    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; }
    body { background: var(--bg); color: var(--text); line-height: 1.6; scroll-behavior: smooth; }

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
    nav a { color: var(--primary); text-decoration: none; font-weight: 500; transition: color 0.3s; }
    nav a:hover { color: var(--secondary); }

    /* Hero Section */
    header.hero {
      background: url('https://images.unsplash.com/photo-1522202220652-31e0a3b20656?auto=format&fit=crop&w=1950&q=80') no-repeat center center/cover;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
      color: #fff;
    }
    header.hero::after {
      content: '';
      position: absolute;
      top:0; left:0; width:100%; height:100%;
      background-color: rgba(0,0,0,0.5);
      z-index:1;
    }
    header.hero .hero-content {
      position: relative;
      z-index:2;
    }
    header.hero h1 { font-size: 3rem; margin-bottom: 1rem; text-shadow: 2px 2px 8px rgba(0,0,0,0.5);}
    header.hero p { font-size: 1.3rem; margin-bottom: 2rem; text-shadow: 1px 1px 6px rgba(0,0,0,0.5);}
    .cta-btn {
      background: var(--primary);
      color: #fff;
      padding: 0.8rem 2rem;
      border-radius: 50px;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.3s ease;
    }
    .cta-btn:hover { background: var(--secondary); }

    /* Section Base */
    section {
      max-width: 1000px;
      margin: 3rem auto;
      background: var(--white);
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }
    h2 { color: var(--primary); margin-bottom: 1rem; text-align:center; }

    /* Toggle Buttons */
    .toggle-btns { text-align:center; margin-bottom: 2rem; }
    .toggle-btns button {
      padding: 0.5rem 1.5rem;
      margin: 0 0.5rem;
      border:none;
      border-radius: 25px;
      font-weight:600;
      cursor:pointer;
      transition: all 0.3s;
      background: var(--primary);
      color:#fff;
    }
    .toggle-btns button.active { background: var(--secondary); }

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
    .project h3 a { color: var(--secondary); text-decoration:none; }
    .project h3 a:hover { text-decoration:underline; }

    /* Testimonials */
    .testimonials { display: none; }
    .testimonial {
      background: #f3f4f6;
      padding: 1rem 1.5rem;
      margin-bottom: 1rem;
      border-left: 5px solid var(--primary);
      border-radius: 8px;
    }
    .testimonial p { font-style: italic; margin-bottom:0.5rem; }
    .testimonial span { font-weight:600; color:var(--secondary); }

    /* Footer */
    footer {
      text-align: center;
      padding: 2rem 1rem;
      background: var(--primary);
      color: var(--white);
    }
    footer a { color: #fff; text-decoration:none; font-weight: bold; }
    footer a:hover { text-decoration: underline; }
  </style>
</head>
<body>
  <!-- Navigation -->
  <nav>
    <a href="#home">Home</a>
    <a href="#projects">Portfolio</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- Hero Section -->
  <header class="hero" id="home">
    <div class="hero-content">
      <h1>Gift Abuga</h1>
      <p>Web Developer • Nairobi, Kenya</p>
      <a href="mailto:giftabuga@gmail.com" class="cta-btn">Hire Me</a>
    </div>
  </header>

  <!-- Portfolio Section with Toggle -->
  <section id="projects">
    <h2>Portfolio & Testimonials</h2>
    <div class="toggle-btns">
      <button id="show-projects" class="active">Projects</button>
      <button id="show-testimonials">Testimonials</button>
    </div>

    <!-- Projects -->
    <div class="projects" id="projects-list">
      <div class="project">
        <h3><a href="https://www.afrikanest.com/" target="_blank">Afrikanest</a></h3>
        <p>A property management website I built to handle tenant payments and billing.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.dala.co.ke/" target="_blank">Dala</a></h3>
        <p>Property management platform with lease tracking and reporting features.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.marima.co.ke/" target="_blank">Marima</a></h3>
        <p>Interactive website for property owners to manage listings and tenants.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.bomahut.com/" target="_blank">Bomahut</a></h3>
        <p>Website for landlords to handle payments, maintenance, and reports efficiently.</p>
      </div>
      <div class="project">
        <h3><a href="https://www.wingurent.com/" target="_blank">WinguRent</a></h3>
        <p>All-in-one platform for rent collection, tracking, and management for landlords.</p>
      </div>
    </div>

    <!-- Testimonials -->
    <div class="testimonials" id="testimonials-list">
      <div class="testimonial">
        <p>"Gift transformed our property management workflow completely. Highly recommend!"</p>
        <span>Alex Juma, Nairobi</span>
      </div>
      <div class="testimonial">
        <p>"Our travel website looks stunning and works flawlessly thanks to Gift!"</p>
        <span>Jane Muthoni, Mombasa</span>
      </div>
      <div class="testimonial">
        <p>"Professional, timely, and extremely skilled. Our hotel bookings system is now seamless."</p>
        <span>Michael Otieno, Kisumu</span>
      </div>
      <div class="testimonial">
        <p>"Gift delivered a modern and responsive website for our tour company. Our clients love it!"</p>
        <span>Grace Wanjiku, Naivasha</span>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <p style="text-align:center;">Email: <a href="mailto:giftabuga@gmail.com">giftabuga@gmail.com</a></p>
  </section>

  <!-- Footer -->
  <footer>
    &copy; 2025 Gift Abuga | Built with ❤️
  </footer>

  <!-- JS for Toggle -->
  <script>
    const showProjectsBtn = document.getElementById('show-projects');
    const showTestimonialsBtn = document.getElementById('show-testimonials');
    const projectsList = document.getElementById('projects-list');
    const testimonialsList = document.getElementById('testimonials-list');

    showProjectsBtn.addEventListener('click', () => {
      projectsList.style.display = 'grid';
      testimonialsList.style.display = 'none';
      showProjectsBtn.classList.add('active');
      showTestimonialsBtn.classList.remove('active');
    });

    showTestimonialsBtn.addEventListener('click', () => {
      projectsList.style.display = 'none';
      testimonialsList.style.display = 'block';
      showProjectsBtn.classList.remove('active');
      showTestimonialsBtn.classList.add('active');
    });
  </script>
</body>
</html>


