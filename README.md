<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gift Abuga | Web Developer Portfolio</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --primary: #4f46e5;
      --secondary: #7c3aed;
      --accent: #ff6363;
      --bg: #f9fafb;
      --text: #333;
      --white: #fff;
    }

    * { box-sizing: border-box; margin:0; padding:0; font-family:'Poppins',sans-serif;}
    body { background: var(--bg); color: var(--text); scroll-behavior: smooth; line-height: 1.6;}

    /* Navbar */
    nav {
      background: rgba(255,255,255,0.95);
      position: sticky; top:0; z-index:1000;
      display:flex; justify-content:center; gap:2rem;
      padding:1rem 0; box-shadow:0 2px 8px rgba(0,0,0,0.05);
    }
    nav a { text-decoration:none; color: var(--primary); font-weight:500; transition:0.3s;}
    nav a:hover { color: var(--secondary); }

    /* Hero Section Full-Screen */
    header {
      background: url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=1950&q=80') no-repeat center/cover;
      height: 100vh; display:flex; flex-direction:column;
      justify-content:center; align-items:center;
      text-align:center; position:relative; color: var(--white);
    }
    header::before {
      content: ''; position:absolute; top:0; left:0; width:100%; height:100%;
      background: rgba(0,0,0,0.5); z-index:0;
    }
    header h1, header p, .cta-btn { position: relative; z-index:1;}
    header h1 { font-size:4rem; margin-bottom:1rem; text-shadow:2px 2px 10px rgba(0,0,0,0.7);}
    header p { font-size:1.5rem; margin-bottom:2rem; text-shadow:1px 1px 8px rgba(0,0,0,0.7);}
    .cta-btn {
      display:inline-block; background:var(--accent); color:var(--white);
      padding:1rem 2.5rem; border-radius:50px; font-weight:600; text-decoration:none;
      font-size:1.1rem; transition:0.3s;
    }
    .cta-btn:hover { background:var(--secondary); }

    /* Sections */
    section {
      max-width:1000px; margin:3rem auto;
      padding:2rem; background:var(--white);
      border-radius:10px; box-shadow:0 4px 15px rgba(0,0,0,0.05);
    }
    h2 { color:var(--primary); margin-bottom:1rem; text-align:center;}

    /* Projects */
    .projects { display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:1.5rem;}
    .project { border-radius:8px; overflow:hidden; border-left:5px solid var(--secondary); background:var(--bg);}
    .project img { width:100%; display:block; transition: transform 0.3s; }
    .project img:hover { transform: scale(1.05); }
    .project h3 { padding:1rem; color: var(--secondary);}
    .project p { padding:0 1rem 1rem 1rem;}
    .project h3 a { text-decoration:none; color:var(--secondary);}
    .project h3 a:hover { text-decoration:underline;}

    /* Skills */
    .skills { display:flex; flex-wrap:wrap; justify-content:center; gap:1rem;}
    .skill { background: var(--primary); color:var(--white); padding:0.8rem 1.5rem; border-radius:50px; font-weight:500;}

    /* Testimonials */
    .testimonial { background: var(--bg); padding:1.5rem; margin-bottom:1rem; border-left:5px solid var(--secondary); border-radius:8px;}
    .testimonial p { font-style:italic; }
    .testimonial span { display:block; margin-top:0.5rem; font-weight:600; color:var(--primary);}

    /* Contact */
    .contact-form { display:flex; flex-direction:column; gap:1rem; max-width:500px; margin:auto;}
    .contact-form input, .contact-form textarea {
      padding:0.8rem; border-radius:5px; border:1px solid #ccc; font-size:1rem;
    }
    .contact-form button {
      background: var(--primary); color: var(--white); padding:0.8rem 2rem;
      border:none; border-radius:50px; font-weight:600; cursor:pointer; transition:0.3s;
    }
    .contact-form button:hover { background: var(--secondary); }

    /* Footer */
    footer { text-align:center; padding:2rem 1rem; background: var(--primary); color:var(--white);}
    footer a { color:var(--white); text-decoration:none; font-weight:bold;}
    footer a:hover { text-decoration:underline;}

    /* Responsive */
    @media(max-width:768px){
      header h1{ font-size:3rem;}
      header p{ font-size:1.2rem;}
      .cta-btn{ padding:0.8rem 2rem; font-size:1rem;}
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav>
    <a href="#home">Home</a>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- Hero Section -->
  <header id="home">
    <h1>Gift Abuga</h1>
    <p>Web Developer • Nairobi, Kenya</p>
    <a href="#contact" class="cta-btn">Hire Me</a>
  </header>

  <!-- Projects Section -->
  <section id="projects">
    <h2>My Projects</h2>
    <div class="projects">
      <div class="project">
        <img src="https://images.unsplash.com/photo-1581091215368-7f3d1efb4d85?auto=format&fit=crop&w=800&q=80" alt="Project 1">
        <h3><a href="#">Portfolio Website</a></h3>
        <p>A modern responsive portfolio website built with HTML, CSS, and JS.</p>
      </div>
      <div class="project">
        <img src="https://images.unsplash.com/photo-1581091215368-7f3d1efb4d85?auto=format&fit=crop&w=800&q=80" alt="Project 2">
        <h3><a href="#">E-commerce Platform</a></h3>
        <p>A full-stack e-commerce app built with React and Node.js.</p>
      </div>
      <div class="project">
        <img src="https://images.unsplash.com/photo-1581091215368-7f3d1efb4d85?auto=format&fit=crop&w=800&q=80" alt="Project 3">
        <h3><a href="#">Blog Platform</a></h3>
        <p>A content management system with modern design and accessibility.</p>
      </div>
    </div>
  </section>

  <!-- Skills Section -->
  <section id="skills">
    <h2>My Skills</h2>
    <div class="skills">
      <span class="skill">HTML</span>
      <span class="skill">CSS</span>
      <span class="skill">JavaScript</span>
      <span class="skill">React</span>
      <span class="skill">Node.js</span>
      <span class="skill">Git & GitHub</span>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials">
    <h2>Testimonials</h2>
    <div class="testimonial">
      <p>"Gift built our company website with amazing speed and quality. Highly recommended!"</p>
      <span>- John Doe, CEO</span>
    </div>
    <div class="testimonial">
      <p>"Professional, creative, and responsive. A pleasure to work with!"</p>
      <span>- Jane Smith, Startup Founder</span>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form class="contact-form" action="mailto:giftabuga@gmail.com" method="POST" enctype="text/plain">
      <input type="text" name="name" placeholder="Your Name" required>
      <input type="email" name="email" placeholder="Your Email" required>
      <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 Gift Abuga | <a href="mailto:giftabuga@gmail.com">Contact Me</a></p>
  </footer>

</body>
</html>

