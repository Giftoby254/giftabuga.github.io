<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gift Abuga | Web Developer</title>
<style>
:root {
  --primary: #00a859;
  --secondary: #00724d;
  --accent: #f7c948;
  --light: #f9f9f9;
  --dark: #222;
  --transition: 0.5s ease;
}

* { box-sizing: border-box; scroll-behavior: smooth; }
body { font-family: "Segoe UI", Arial, sans-serif; margin: 0; background: var(--light); color: var(--dark); }
a { text-decoration: none; color: inherit; }

header { position: sticky; top: 0; background: white; box-shadow: 0 2px 8px rgba(0,0,0,0.1); z-index: 1000; }
nav { display: flex; justify-content: space-between; align-items: center; max-width: 1100px; margin: auto; padding: 15px 20px; }
nav .logo { font-weight: bold; font-size: 1.5rem; color: var(--primary); }
nav ul { list-style: none; display: flex; gap: 20px; }
nav ul li a:hover { color: var(--accent); }

h1,h2,h3 { margin: 0; }
h2 { text-align: center; color: var(--primary); font-size: 2.2rem; margin-bottom: 40px; }
section { padding: 80px 20px; position: relative; opacity: 0; transform: translateY(30px); transition: opacity 0.8s ease, transform 0.8s ease; }
section.show { opacity: 1; transform: translateY(0); }
hr.section-divider { border: none; height: 4px; background: var(--primary); width: 80px; margin: 40px auto; border-radius: 2px; }

/* HERO */
#hero { background: url('https://images.unsplash.com/photo-1505238680356-667803448bb6?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat; color: white; text-align: center; padding: 120px 20px; position: relative; }
#hero::after { content: ''; position: absolute; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.5); z-index:0; }
#hero .content { position: relative; z-index:1; }
#hero h1 { font-size:3rem; margin-bottom:20px; }
#hero p { font-size:1.2rem; margin-bottom:30px; }
#hero a { background: var(--accent); color:#222; padding:12px 25px; border-radius:5px; font-weight:bold; transition: var(--transition); }
#hero a:hover { background:white; color:var(--primary); }

/* PROJECTS */
#projects { background: linear-gradient(to bottom right, #f5f7fa, #e4f1ed); }
.projects-grid { display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap:25px; max-width:1100px; margin:0 auto; }
.project-card { background:white; border-radius:12px; overflow:hidden; box-shadow:0 5px 10px rgba(0,0,0,0.1); transition:var(--transition); text-align:center; }
.project-card img { width:100%; height:180px; object-fit:cover; transition:var(--transition); }
.project-card:hover img { transform: scale(1.05); filter: brightness(0.8); }
.project-content { padding:20px; }
.project-content h3 { color: var(--primary); margin-bottom:10px; }
.project-content a { display:inline-block; margin-top:10px; padding:8px 16px; background: var(--primary); color:white; border-radius:5px; transition: var(--transition); }
.project-content a:hover { background: var(--secondary); }

/* TESTIMONIALS */
#testimonials .testimonial-container { display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap:25px; max-width:1100px; margin:0 auto; }
.testimonial-card { background:white; border-radius:15px; padding:30px; text-align:center; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition: var(--transition); }
.testimonial-card:hover { transform:translateY(-5px); box-shadow:0 10px 25px rgba(0,0,0,0.15); }
.testimonial-card p { font-size:0.95rem; line-height:1.6; color:#333; margin-bottom:15px; }
.testimonial-card .testimonial-name { font-weight:bold; color: var(--primary); }

/* BLOG */
#blog .blog-grid { display:grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap:25px; max-width:1100px; margin:0 auto; }
.blog-card { background:white; border-radius:12px; overflow:hidden; transition:var(--transition); box-shadow:0 5px 10px rgba(0,0,0,0.1); }
.blog-card:hover { transform:translateY(-10px); box-shadow:0 10px 20px rgba(0,0,0,0.15); }
.blog-card img { width:100%; height:200px; object-fit:cover; transition:var(--transition); }
.blog-card:hover img { filter: brightness(0.8); }
.blog-content { padding:20px; }
.blog-content h3 { color: var(--primary); margin-bottom:10px; }
.blog-content p { font-size:0.95rem; color:#444; }
.read-more { display:inline-block; margin-top:10px; padding:8px 16px; background: var(--primary); color:white; border-radius:5px; transition:var(--transition); }
.read-more:hover { background: var(--secondary); }

/* PRICING */
#pricing .pricing-container { display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap:25px; max-width:1100px; margin:0 auto; }
.pricing-card { background:white; border-radius:15px; padding:30px; text-align:center; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition: var(--transition); position: relative; overflow: hidden; }
.pricing-card:hover { transform:translateY(-10px); box-shadow:0 10px 25px rgba(0,0,0,0.15); }
.pricing-card h3 { color: var(--primary); font-size:1.5rem; margin-bottom:10px; }
.pricing-card p { margin:10px 0; font-size:0.95rem; }
.price { font-size:1.4rem; font-weight:bold; color: var(--secondary); margin-bottom:15px; }
.highlight { background: var(--primary); color:white; }
.highlight .price { color:white; }
.plan-icon { font-size:2rem; margin-bottom:10px; }

/* FOOTER */
footer { background: var(--dark); color:white; text-align:center; padding:30px 20px; }
footer a { color: var(--accent); }

@media (max-width:768px) {
  h2 { font-size:1.8rem; }
  nav ul { flex-direction: column; gap:10px; }
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
<hr class="section-divider">

<!-- PROJECTS -->
<section id="projects">
<h2>My Projects</h2>
<div class="projects-grid">
  <div class="project-card">
    <img src="https://images.unsplash.com/photo-1590080870790-168b0b6aa9a7?auto=format&fit=crop&w=800&q=80" alt="Project 1">
    <div class="project-content">
      <h3>EcoStyle Kenya</h3>
      <p>Responsive e-commerce website for sustainable products.</p>
      <a href="#" target="_blank">View Project</a>
    </div>
  </div>
  <div class="project-card">
    <img src="https://images.unsplash.com/photo-1509395176047-4a66953fd231?auto=format&fit=crop&w=800&q=80" alt="Project 2">
    <div class="project-content">
      <h3>Touch Wild Tours</h3>
      <p>Interactive tour booking platform with stunning visuals.</p>
      <a href="#" target="_blank">View Project</a>
    </div>
  </div>
  <div class="project-card">
    <img src="https://images.unsplash.com/photo-1572276596237-6a1b40b7bb34?auto=format&fit=crop&w=800&q=80" alt="Project 3">
    <div class="project-content">
      <h3>Nyumba Zetu Property</h3>
      <p>Real estate listing platform with advanced search features.</p>
      <a href="#" target="_blank">View Project</a>
    </div>
  </div>
</div>
</section>
<hr class="section-divider">

<!-- TESTIMONIALS -->
<section id="testimonials">
<h2>What Clients Say</h2>
<div class="testimonial-container">
  <div class="testimonial-card">
    <p>"Working with Gift was an absolute pleasure. He took the time to understand our brand, the target audience, and our objectives. The final website exceeded all expectations, with a seamless user experience and a design that truly reflects our values."</p>
    <div class="testimonial-name">— Kofi Mensah</div>
  </div>
  <div class="testimonial-card">
    <p>"Gift is a true professional. From the initial consultation to the final launch, every step was handled with great care and attention. He translated our ideas into a visually stunning and highly functional platform. Thanks to Gift, our online engagement has increased significantly."</p>
    <div class="testimonial-name">— Amina Njeri</div>
  </div>
  <div class="testimonial-card">
    <p>"The website Gift developed for us is exceptional. Beyond aesthetics, the performance, responsiveness, and usability are remarkable. Gift went above and beyond by providing ongoing support even after the launch."</p>
    <div class="testimonial-name">— Thabo Dlamini</div>
  </div>
</div>
</section>
<hr class="section-divider">

<!-- BLOG -->
<section id="blog">
<h2>Latest Blog Posts</h2>
<div class="blog-grid">
  <div class="blog-card">
    <img src="https://images.unsplash.com/photo-1559526324-593bc073d938?auto=format&fit=crop&w=800&q=80" alt="Blog 1">
    <div class="blog-content">
      <h3>Web Design Trends 2025</h3>
      <p>Explore the latest trends in web design that will dominate 2025 and beyond.</p>
      <a class="read-more" href="#">Read More</a>
    </div>
  </div>
  <div class="blog-card">
    <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=800&q=80" alt="Blog 2">
    <div class="blog-content">
      <h3>Improving UX for Mobile</h3>
      <p>Tips and techniques for enhancing user experience on mobile devices.</p>
      <a class="read-more" href="#">Read More</a>
    </div>
  </div>
  <div class="blog-card">
    <img src="https://images.unsplash.com/photo-1518779578993-ec3579fee39f?auto=format&fit=crop&w=800&q=80" alt="Blog 3">
    <div class="blog-content">
      <h3>SEO Basics for 2025</h3>
      <p>Learn the fundamentals of SEO and how to rank your website higher in search engines.</p>
      <a class="read-more" href="#">Read More</a>
    </div>
  </div>
</div>
</section>
<hr class="section-divider">

<!-- PRICING -->
<section id="pricing">
<h2>Pricing Plans</h2>
<div class="pricing-container">
  <div class="pricing-card">
    <div class="plan-icon">💻</div>
    <h3>Basic</h3>
    <p class="price">$199</p>
    <p>Landing page design</p>
    <p>Responsive layout</p>
    <p>Email support</p>
  </div>
  <div class="pricing-card highlight">
    <div class="plan-icon">🚀</div>
    <h3>Pro</h3>
    <p class="price">$499</p>
    <p>Full website design</p>
    <p>Responsive & SEO optimized</p>
    <p>Priority support</p>
  </div>
  <div class="pricing-card">
    <div class="plan-icon">🌐</div>
    <h3>Enterprise</h3>
    <p class="price">$999</p>
    <p>Custom web applications</p>
    <p>Advanced SEO & analytics</p>
    <p>Dedicated support</p>
  </div>
</div>
</section>
<hr class="section-divider">

<!-- FOOTER -->
<footer>
<p>&copy; 2025 Gift Abuga. All rights reserved. | <a href="mailto:contact@giftabuga.com">contact@giftabuga.com</a></p>
</footer>

<script>
// Scroll animation
const sections = document.querySelectorAll('section');
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if(entry.isIntersecting) entry.target.classList.add('show');
  });
}, { threshold: 0.1 });

sections.forEach(section => observer.observe(section));
</script>

</body>
</html>
