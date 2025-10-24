
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
  --transition: 0.5s ease;
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
  position: relative;
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease, transform 0.8s ease;
}

section.show {
  opacity: 1;
  transform: translateY(0);
}

/* ------------------ HERO ------------------ */
#hero {
  background: url('https://images.unsplash.com/photo-1505238680356-667803448bb6?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
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

#hero .contact-buttons a {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: var(--accent);
  color: #222;
  padding: 12px 25px;
  border-radius: 5px;
  font-weight: bold;
  margin: 5px;
  transition: var(--transition);
}

#hero .contact-buttons a:hover {
  background: white;
  color: var(--primary);
}

/* ------------------ PROJECTS ------------------ */
#projects {
  background: linear-gradient(to bottom right, #f5f7fa, #e4f1ed);
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  max-width: 1100px;
  margin: 0 auto;
}

.project-card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  transition: var(--transition);
  position: relative;
  text-align: center;
}

.project-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  transition: var(--transition);
}

.project-card:hover img {
  transform: scale(1.05);
  filter: brightness(0.85);
}

.project-content {
  padding: 20px;
}

.project-content h3 {
  color: var(--primary);
  margin-bottom: 15px;
  font-size: 1.4rem;
}

.project-content p {
  margin-bottom: 15px;
  color: #444;
  font-size: 1rem;
}

.project-content a {
  display: inline-block;
  padding: 10px 20px;
  background: var(--primary);
  color: white;
  border-radius: 5px;
  font-weight: bold;
  transition: var(--transition);
}

.project-content a:hover {
  background: var(--accent);
  color: #222;
}

/* ------------------ PRICING ------------------ */
#pricing .pricing-container,
#testimonials .testimonial-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
  max-width: 1100px;
  margin: 0 auto;
}

.pricing-card, .testimonial-card {
  background: white;
  border-radius: 15px;
  padding: 30px;
  text-align: center;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}

.pricing-card:hover, .testimonial-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.15);
}

.pricing-card h3, .testimonial-card h3 {
  color: var(--primary);
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.pricing-card p, .testimonial-card p {
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

/* ------------------ TESTIMONIALS ------------------ */
.testimonial-card p {
  font-style: italic;
  color: #555;
}

.testimonial-card h3 {
  margin-top: 15px;
  font-weight: bold;
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
  h2 {
    font-size: 1.8rem;
  }
  nav ul {
    flex-direction: column;
    gap: 10px;
  }
}

/* ------------------ FLOATING BUTTONS ------------------ */
.floating-buttons {
  position: fixed;
  bottom: 20px;
  right: 20px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  z-index: 1000;
}

.floating-buttons a {
  background: var(--primary);
  color: white;
  padding: 12px;
  border-radius: 50%;
  text-align: center;
  font-size: 20px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
  transition: var(--transition);
}

.floating-buttons a:hover {
  background: var(--accent);
  color: #222;
}

/* ------------------ SIDE FLOATING WHATSAPP ------------------ */
.side-whatsapp {
  position: fixed;
  right: 0;
  top: 40%;
  background: var(--primary);
  color: white;
  padding: 15px;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
  font-size: 20px;
  text-align: center;
  z-index: 1000;
  transition: var(--transition);
}

.side-whatsapp:hover {
  background: var(--accent);
  color: #222;
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
      <li><a href="#pricing">Pricing</a></li>
      <li><a href="#testimonials">Testimonials</a></li>
    </ul>
  </nav>
</header>

<!-- HERO -->
<section id="hero">
  <div class="content">
    <h1>Professional Web Development Services</h1>
    <p>Creating stunning, responsive websites that grow your business.</p>
    <div class="contact-buttons">
      <a href="https://wa.me/254111971411?text=lets%20partner%20in%20a%20project." target="_blank">
        📱 WhatsApp
      </a>
      <a href="tel:+254111971411">
        📞 Call Me
      </a>
    </div>
  </div>
</section>
<hr class="section-divider">

<!-- PROJECTS -->
<section id="projects">
  <h2>My Projects</h2>
  <div class="projects-grid">
    <div class="project-card">
      <img src="https://trippygotours.com/wp-content/uploads/2023/03/homepage.jpg" alt="TrippyGO Tours">
      <div class="project-content">
        <h3>TrippyGO Tours & Travel</h3>
        <p>A dynamic and user-friendly travel website showcasing tours and booking features.</p>
        <a href="https://trippygotours.com/" target="_blank">View Project</a>
      </div>
    </div>

    <div class="project-card">
      <img src="https://ritzhospitality.co.ke/wp-content/uploads/2023/03/homepage.jpg" alt="Ritz Hospitality">
      <div class="project-content">
        <h3>Ritz Hospitality</h3>
        <p>An elegant hospitality website that improves client engagement and online presence.</p>
        <a href="https://ritzhospitality.co.ke/" target="_blank">View Project</a>
      </div>
    </div>

    <div class="project-card">
      <img src="https://iricongroup.co.ke/wp-content/uploads/2023/03/homepage.jpg" alt="Iricon Group">
      <div class="project-content">
        <h3>Iricon Group</h3>
        <p>A professional website showcasing company services, portfolio, and client projects.</p>
        <a href="https://iricongroup.co.ke/" target="_blank">View Project</a>
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
      <div class="plan-icon">🖥️</div>
      <h3>Basic</h3>
      <div class="price">$19</div>
      <p>Responsive website design</p>
      <p>3 pages</p>
      <p>Email support</p>
    </div>
    <div class="pricing-card highlight">
      <div class="plan-icon">🚀</div>
      <h3>Pro</h3>
      <div class="price">$29</div>
      <p>Responsive website + CMS</p>
      <p>Up to 5 pages</p>
      <p>Priority support</p>
    </div>
    <div class="pricing-card">
      <div class="plan-icon">💼</div>
      <h3>Premium</h3>
      <div class="price">$49</div>
      <p>Custom web development</p>
      <p>Unlimited pages</p>
      <p>Full support</p>
    </div>
  </div>
</section>
<hr class="section-divider">

<!-- TESTIMONIALS -->
<section id="testimonials">
  <h2>What Clients Say</h2>
  <div class="testimonial-container">
    <div class="testimonial-card">
      <p>"Gift built our company website in record time. Truly professional!"</p>
      <h3>James Mwangi</h3>
    </div>
    <div class="testimonial-card">
      <p>"Amazing work! Our bookings have increased thanks to the new site."</p>
      <h3>Faith Wanjiru</h3>
    </div>
    <div class="testimonial-card">
      <p>"Very responsive and attentive. Highly recommend for web development."</p>
      <h3>David Omondi</h3>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  &copy; 2025 Gift Abuga. 
  <a href="https://wa.me/254111971411?text=lets%20partner%20in%20a%20project." target="_blank">WhatsApp Me</a> | 
  <a href="tel:+254111971411">Call Me</a>
</footer>

<!-- FLOATING BUTTONS -->
<div class="floating-buttons">
  <a href="https://wa.me/254111971411?text=lets%20partner%20in%20a%20project." target="_blank">📱</a>
  <a href="tel:+254111971411">📞</a>
</div>

<!-- SIDE FLOATING WHATSAPP -->
<a href="https://wa.me/254111971411?text=lets%20partner%20in%20a%20project." target="_blank" class="side-whatsapp">💬 WhatsApp</a>

<script>
// Fade-in on scroll
const sections = document.querySelectorAll('section');
window.addEventListener('scroll', () => {
  const triggerBottom = window.innerHeight * 0.85;
  sections.forEach(section => {
    const sectionTop = section.getBoundingClientRect().top;
    if(sectionTop < triggerBottom) {
      section.classList.add('show');
    }
  });
});
</script>

</body>
</html>
