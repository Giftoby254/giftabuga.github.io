
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gift Abuga | Web Developer</title>
  <style>
    :root {
      --primary: #00a859;
      --secondary: #00724d;
      --accent: #f7c948;
      --light: #f9f9f9;
      --dark: #222;
      --transition: 0.4s ease;
    }

    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: "Segoe UI", Arial, sans-serif;
      margin: 0;
      background: var(--light);
      color: var(--dark);
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    header {
      position: sticky;
      top: 0;
      background: white;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      z-index: 1000;
    }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: 1100px;
      margin: auto;
      padding: 15px 20px;
    }

    nav .logo {
      font-weight: bold;
      font-size: 1.5rem;
      color: var(--primary);
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    nav ul li a:hover {
      color: var(--accent);
    }

    h1, h2, h3 {
      margin: 0;
    }

    h2 {
      text-align: center;
      color: var(--primary);
      font-size: 2.2rem;
      margin-bottom: 40px;
    }

    section {
      padding: 80px 20px;
    }

    /* ------------------ HERO ------------------ */
    #hero {
      background: url('https://images.unsplash.com/photo-1521791136064-7986c2920216?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
      color: white;
      text-align: center;
      padding: 120px 20px;
      position: relative;
    }

    #hero::after {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.5);
      z-index: 0;
    }

    #hero .content {
      position: relative;
      z-index: 1;
    }

    #hero h1 {
      font-size: 3rem;
      margin-bottom: 20px;
    }

    #hero p {
      font-size: 1.2rem;
      margin-bottom: 30px;
    }

    #hero a {
      background: var(--accent);
      color: #222;
      padding: 12px 25px;
      border-radius: 5px;
      font-weight: bold;
      transition: var(--transition);
    }

    #hero a:hover {
      background: white;
      color: var(--primary);
    }

    /* ------------------ PROJECTS / PORTFOLIO ------------------ */
    #projects {
      background: linear-gradient(to bottom right, #f5f7fa, #e4f1ed);
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
      max-width: 1100px;
      margin: 0 auto;
    }

    .project-card {
      background: white;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 5px 10px rgba(0,0,0,0.1);
      transition: var(--transition);
      position: relative;
    }

    .project-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      transition: var(--transition);
    }

    .project-card:hover img {
      transform: scale(1.05);
      filter: brightness(0.8);
    }

    .project-content {
      padding: 20px;
      text-align: center;
    }

    .project-content h3 {
      color: var(--primary);
      margin-bottom: 10px;
    }

    /* ------------------ TESTIMONIALS ------------------ */
    #testimonials {
      background: #f9f9f9;
      color: var(--dark);
    }

    .testimonial-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 25px;
      max-width: 1100px;
      margin: 0 auto;
    }

    .testimonial-card {
      flex: 1 1 300px;
      max-width: 350px;
      background: white;
      border-radius: 12px;
      padding: 30px 20px 20px 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      text-align: center;
      transition: var(--transition);
      position: relative;
    }

    .testimonial-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0,0,0,0.15);
    }

    .testimonial-card img {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      border: 3px solid var(--primary);
      object-fit: cover;
      margin-top: -60px;
      background: white;
    }

    .testimonial-text {
      font-style: italic;
      margin: 20px 0;
      font-size: 0.95rem;
      line-height: 1.4;
    }

    .testimonial-name {
      font-weight: bold;
      color: var(--primary);
    }

    /* ------------------ BLOG ------------------ */
    #blog .blog-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 25px;
      max-width: 1100px;
      margin: 0 auto;
    }

    .blog-card {
      background: white;
      border-radius: 12px;
      overflow: hidden;
      transition: var(--transition);
      box-shadow: 0 5px 10px rgba(0,0,0,0.1);
    }

    .blog-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 20px rgba(0,0,0,0.15);
    }

    .blog-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      transition: var(--transition);
    }

    .blog-card:hover img {
      filter: brightness(0.8);
    }

    .blog-content {
      padding: 20px;
    }

    .blog-content h3 {
      color: var(--primary);
      margin-bottom: 10px;
    }

    .blog-content p {
      font-size: 0.95rem;
      color: #444;
    }

    .read-more {
      display: inline-block;
      margin-top: 10px;
      padding: 8px 16px;
      background: var(--primary);
      color: white;
      border-radius: 5px;
      transition: var(--transition);
    }

    .read-more:hover {
      background: var(--secondary);
    }

    /* ------------------ PRICING ------------------ */
    #pricing .pricing-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
      max-width: 1100px;
      margin: 0 auto;
    }

    .pricing-card {
      background: white;
      border-radius: 15px;
      padding: 30px;
      text-align: center;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      transition: var(--transition);
      position: relative;
      overflow: hidden;
    }

    .pricing-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }

    .pricing-card h3 {
      color: var(--primary);
      font-size: 1.5rem;
      margin-bottom: 10px;
    }

    .pricing-card p {
      margin: 10px 0;
      font-size: 0.95rem;
    }

    .price {
      font-size: 1.4rem;
      font-weight: bold;
      color: var(--secondary);
      margin-bottom: 15px;
    }

    .highlight {
      background: var(--primary);
      color: white;
    }

    .highlight .price {
      color: white;
    }

    .plan-icon {
      font-size: 2rem;
      margin-bottom: 10px;
    }

    /* ------------------ FOOTER ------------------ */
    footer {
      background: var(--dark);
      color: white;
      text-align: center;
      padding: 30px 20px;
    }

    footer a {
      color: var(--accent);
    }

    /* ------------------ MEDIA QUERIES ------------------ */
    @media (max-width: 768px) {
      .testimonial-card {
        flex: 1 1 90%;
      }
      h2 {
        font-size: 1.8rem;
      }
      nav ul {
        flex-direction: column;
        gap: 10px;
      }
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <header>
    <nav>
      <div class="logo">Gift Abuga</div>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#testimonials">Testimonials</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#pricing">Pricing</a></li>
      </ul>
    </nav>
  </header>

  <!-- HERO -->
  <section id="hero">
    <div class="content">
      <h1>Professional Web Development Services</h1>
      <p>Creating stunning, responsive websites that grow your business.</p>
      <a href="#projects">See My Work</a>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <h2>My Projects</h2>
    <div class="projects-grid">
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1581091012184-9fcd5ff6f0c1?auto=format&fit=crop&w=800&q=80" alt="Project 1" />
        <div class="project-content">
          <h3>EcoStyle Kenya</h3>
          <p>Responsive e-commerce website for sustainable products.</p>
        </div>
      </div>
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1581091012182-9322f97ff1fc?auto=format&fit=crop&w=800&q=80" alt="Project 2" />
        <div class="project-content">
          <h3>Touch Wild Tours</h3>
          <p>Interactive tour booking platform with stunning visuals.</p>
        </div>
      </div>
      <div class="project-card">
        <img src="https://images.unsplash.com/photo-1581091012175-35d1c86f3c4b?auto=format&fit=crop&w=800&q=80" alt="Project 3" />
        <div class="project-content">
          <h3>Nyumba Zetu Property</h3>
          <p>Real estate listing platform with advanced search features.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <section id="testimonials">
    <h2>What Clients Say</h2>
    <div class="testimonial-container">
      <div class="testimonial-card">
        <img src="https://randomuser.me/api/portraits/women/65.jpg" alt="Client 1" />
        <div class="testimonial-text">"Gift built a visually stunning website that perfectly represents our brand. His attention to detail was exceptional."</div>
        <div class="testimonial-name">— Wanjiku Mwangi</div>
      </div>
      <div class="testimonial-card">
        <img src="https://randomuser.me/api/portraits/men/42.jpg" alt="Client 2" />
        <div class="testimonial-text">"I was impressed by how responsive and fast our new platform is. Gift made the process smooth and explained every step clearly."</div>
        <div class="testimonial-name">— Kevin Otieno</div>
      </div>
      <div class="testimonial-card">
        <img src="https://randomuser.me/api/portraits/women/12.jpg" alt="Client 3" />
        <div class="testimonial-text">"Professional, friendly, and extremely talented. Gift delivered a masterpiece website that boosted our engagement by 60%."</div>
        <div class="testimonial-name">— Sarah Muthoni</div>
      </div>
    </div>
  </section>

  <!-- BLOG -->
  <section id="blog">
    <h2>Latest Blog Posts</h2>
    <div class="blog-grid">
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=800&q=80" alt="Web Trends" />
        <div class="blog-content">
          <h3>Top Web Design Trends 2025</h3>
          <p>Explore cutting-edge trends shaping digital experiences from AI personalization to motion design.</p>
          <a href="#" class="read-more">Read More</a>
        </div>
      </div>
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1557804506-669a67965ba0?auto=format&fit=crop&w=800&q=80" alt="SEO Tips" />
        <div class="blog-content">
          <h3>Boost Your SEO in 5 Steps</h3>
          <p>Learn actionable strategies to increase your website traffic and improve search engine rankings.</p>
          <a href="#" class="read-more">Read More</a>
        </div>
      </div>
    </div>
  </section>

  <!-- PRICING -->
  <section id="pricing">
    <h2>Pricing Plans</h2>
    <div class="pricing-container">
      <div class="pricing-card">
        <div class="plan-icon">🥈</div>
        <h3>Basic</h3>
        <div class="price">$199</div>
        <p>Perfect for small projects or personal websites.</p>
        <ul>
          <li>5 Pages</li>
          <li>Responsive Design</li>
          <li>Email Support</li>
        </ul>
        <a href="#" class="read-more">Choose Plan</a>
      </div>

      <div class="pricing-card highlight">
        <div class="plan-icon">🥇</div>
        <h3>Professional</h3>
        <div class="price">$499</div>
        <p>Most recommended plan for businesses and startups.</p>
        <ul>
          <li>15 Pages</li>
          <li>Custom Design</li>
          <li>SEO Optimization</li>
          <li>Priority Support</li>
        </ul>
        <a href="#" class="read-more">Choose Plan</a>
      </div>

      <div class="pricing-card">
        <div class="plan-icon">🥉</div>
        <h3>Premium</h3>
        <div class="price">$899</div>
        <p>Advanced plan for e-commerce or large-scale projects.</p>
        <ul>
          <li>Unlimited Pages</li>
          <li>Custom Features</li>
          <li>SEO & Marketing Tools</li>
          <li>24/7 Support</li>
        </ul>
        <a href="#" class="read-more">Choose Plan</a>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    &copy; 2025 Gift Abuga. All Rights Reserved. <br />
    Designed with ❤️ by Gift Abuga. 
  </footer>

</body>
</html>
