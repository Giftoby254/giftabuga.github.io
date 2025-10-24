
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gift Abuga | Professional Web Developer</title>
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

    h2 {
      text-align: center;
      color: var(--primary);
      font-size: 2.2rem;
      margin-bottom: 20px;
    }

    /* ------------------ INTERACTIVE TESTIMONIALS ------------------ */
    #testimonials {
      background: linear-gradient(to right, #00a859, #008c5e);
      color: white;
      padding: 80px 20px;
    }

    .testimonial-container {
      display: flex;
      overflow-x: auto;
      gap: 20px;
      scroll-snap-type: x mandatory;
      padding-bottom: 10px;
    }

    .testimonial-card {
      flex: 0 0 300px;
      scroll-snap-align: center;
      background: rgba(255, 255, 255, 0.15);
      border-radius: 10px;
      padding: 25px;
      backdrop-filter: blur(5px);
      transition: var(--transition);
      position: relative;
    }

    .testimonial-card:hover {
      background: rgba(255, 255, 255, 0.3);
      transform: scale(1.05);
    }

    .testimonial-card img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      border: 2px solid #fff;
      object-fit: cover;
      position: absolute;
      top: -30px;
      left: 20px;
    }

    .testimonial-text {
      margin-top: 40px;
      font-style: italic;
      font-size: 1rem;
    }

    .testimonial-name {
      margin-top: 10px;
      font-weight: bold;
      color: var(--accent);
    }

    /* ------------------ INTERACTIVE BLOG ------------------ */
    #blog {
      background: linear-gradient(to bottom right, #f5f7fa, #e4f1ed);
      padding: 80px 20px;
    }

    .blog-grid {
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
      box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    }

    .blog-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
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
      text-decoration: none;
      border-radius: 5px;
      transition: var(--transition);
    }

    .read-more:hover {
      background: var(--secondary);
    }

    /* ------------------ INTERACTIVE PRICING ------------------ */
    #pricing {
      background: linear-gradient(135deg, #ffffff, #f4fff9);
      padding: 80px 20px;
    }

    .pricing-container {
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
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      transition: var(--transition);
      position: relative;
      overflow: hidden;
    }

    .pricing-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
    }

    .pricing-card::before {
      content: "";
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(0,168,89,0.2), transparent 70%);
      transition: var(--transition);
      transform: scale(0);
      z-index: 0;
    }

    .pricing-card:hover::before {
      transform: scale(1);
    }

    .pricing-card h3 {
      color: var(--primary);
      font-size: 1.5rem;
      z-index: 1;
      position: relative;
    }

    .pricing-card p {
      z-index: 1;
      position: relative;
    }

    .price {
      font-size: 1.4rem;
      font-weight: bold;
      color: var(--secondary);
    }

    .highlight {
      background: var(--primary);
      color: white;
    }

    @media (max-width: 768px) {
      .testimonial-card {
        flex: 0 0 90%;
      }
      h2 {
        font-size: 1.8rem;
      }
    }
  </style>
</head>
<body>

  <!-- INTERACTIVE TESTIMONIALS -->
  <section id="testimonials">
    <h2>What Clients Say</h2>
    <div class="testimonial-container">
      <div class="testimonial-card">
        <img src="https://randomuser.me/api/portraits/women/65.jpg" alt="Client 1" />
        <div class="testimonial-text">"Gift built a visually stunning website that perfectly represents our brand. His attention to detail and creativity were beyond expectations."</div>
        <div class="testimonial-name">— Wanjiku Mwangi, Touch Wild Tours</div>
      </div>
      <div class="testimonial-card">
        <img src="https://randomuser.me/api/portraits/men/42.jpg" alt="Client 2" />
        <div class="testimonial-text">"I was impressed by how responsive and fast our new platform is. Gift made the process smooth and explained every step clearly."</div>
        <div class="testimonial-name">— Kevin Otieno, Nyumba Zetu Property</div>
      </div>
      <div class="testimonial-card">
        <img src="https://randomuser.me/api/portraits/women/12.jpg" alt="Client 3" />
        <div class="testimonial-text">"Professional, friendly, and extremely talented. Gift delivered a masterpiece website that helped boost our online engagement by 60%."</div>
        <div class="testimonial-name">— Sarah Muthoni, EcoStyle Kenya</div>
      </div>
    </div>
  </section>

  <!-- INTERACTIVE BLOG -->
  <section id="blog">
    <h2>Latest Blog Posts</h2>
    <div class="blog-grid">
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=800&q=80" alt="Web Trends" />
        <div class="blog-content">
          <h3>Top Web Design Trends in 2025</h3>
          <p>Explore cutting-edge trends shaping digital experiences — from AI personalization to motion design.</p>
          <a href="#" class="read-more">Read More</a>
        </div>
      </div>
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1557804506-669a67965ba0?auto=format&fit=crop&w=800&q=80" alt="Inclusive Design" />
        <div class="blog-content">
          <h3>Designing for All Ages</h3>
          <p>Inclusive UX design is not just about accessibility — it’s about creating joy and usability for everyone.</p>
          <a href="#" class="read-more">Read More</a>
        </div>
      </div>
      <div class="blog-card">
        <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=800&q=80" alt="SEO Kenya" />
        <div class="blog-content">
          <h3>Why SEO Matters for Kenyan Brands</h3>
          <p>Learn how local SEO strategies can help Kenyan businesses reach both national and international audiences.</p>
          <a href="#" class="read-more">Read More</a>
        </div>
      </div>
    </div>
  </section>

  <!-- INTERACTIVE PRICING -->
  <section id="pricing">
    <h2>Website Packages (Kenyan Rates)</h2>
    <div class="pricing-container">
      <div class="pricing-card">
        <h3>Basic Website</h3>
        <p>Perfect for individuals and small businesses starting online.</p>
        <p class="price">KES 25,000 (One-time)</p>
        <p>Maintenance: KES 3,000/year</p>
      </div>
      <div class="pricing-card highlight">
        <h3>Standard Website</h3>
        <p>Ideal for SMEs and professional service providers.</p>
        <p class="price">KES 45,000 (One-time)</p>
        <p>Maintenance: KES 5,000/year</p>
      </div>
      <div class="pricing-card">
        <h3>Dynamic Website</h3>
        <p>Best for eCommerce and advanced interactive systems.</p>
        <p class="price">KES 85,000 (One-time)</p>
        <p>Maintenance: KES 10,000/year</p>
      </div>
    </div>
  </section>
</body>
</html>
