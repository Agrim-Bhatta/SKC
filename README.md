<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="Portfolio of Mr. AB showcasing skills, projects, and contact information."/>
  <meta name="author" content="Mr. AB"/>
  <title>Mr. AB | Web Developer Portfolio</title>
  <style>
    /* Reset and base styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

html, body {
  height: 100%;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
}

body > main {
  flex: 1;
}

body {
  line-height: 1.6;
  background-color: #f9f9f9;
  color: #333;
}

a {
  text-decoration: none;
  color: inherit;
}

/* Navbar */
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 15px 0;
  background-color: #1f1f1f;
  color: #fff;
  z-index: 1000;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.navbar .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.logo {
  font-size: 2rem;
  font-weight: bold;
  color: #ffd700;
  text-transform: uppercase;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links li a {
  color: #fff;
  font-size: 1.1rem;
  text-transform: uppercase;
  padding: 10px;
  position: relative;
  display: inline-block;
  letter-spacing: 0.5px;
  transition: color 0.3s ease, transform 0.3s ease;
}

.nav-links li a:hover {
  color: #ffd700;
  transform: translateY(-3px);
}

.nav-links li a::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #ffd700;
  transition: width 0.3s ease;
}

.nav-links li a:hover::after {
  width: 100%;
}

/* Hero Section */
.hero {
  background: url('file:///C:/Users/Birendra%20king/Downloads/mr_ab_portfolio/bannar.jpeg') no-repeat center center/cover;
  height: 100vh;
  color: #fff;
  text-align: center;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 20px;
}

.hero::before {
  content: "";
  position: absolute;
  top: 0; left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.4);
  z-index: 0;
}

.hero .container {
  position: relative;
  z-index: 1;
}

.hero h1 {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 20px;
  animation: fadeIn 2s ease-out;
}

.hero p {
  font-size: 1.2rem;
  margin-bottom: 30px;
}

.btn {
  background-color: #ffd700;
  color: #333;
  padding: 12px 25px;
  border-radius: 5px;
  font-weight: bold;
  transition: background-color 0.3s ease;
  display: inline-block;
}

.btn:hover {
  background-color: #333;
  color: #ffd700;
}

/* About Section */
#about {
  padding: 120px 0 80px; /* Adds space for navbar */
  background-color: #f1f1f1;
  text-align: center;
}

.about-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start; /* <-- aligns items to top */
  gap: 50px;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  text-align: left;
}

.about-content img {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  border: 5px solid #ffd700;
  transition: transform 0.3s ease, border-color 0.3s ease;
}

.about-content img:hover {
  transform: scale(1.05);
  border-color: #fff;
}

.about-content p {
  font-size: 1.1rem;
  max-width: 600px;
  line-height: 1.6;
}

/* Skills Section */
#skills {
  padding: 80px 0;
  background-color: #fff;
  text-align: center;
}

#skills h2 {
  font-size: 2.5rem;
  margin-bottom: 40px;
}

.skills-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.skills-list li {
  background-color: #1f1f1f;
  color: #fff;
  padding: 15px 30px;
  border-radius: 5px;
  font-weight: bold;
  transition: transform 0.3s ease;
}

.skills-list li:hover {
  transform: translateY(-10px);
}

/* Projects Section */
#projects {
  padding: 80px 0;
  background-color: #ffffff;
  text-align: center;
}

#projects h2 {
  font-size: 2.5rem;
  margin-bottom: 40px;
}

.projects-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
}

.project-card {
  background-color: #585858;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-10px);
}

.project-card h3 {
  font-size: 1.5rem;
  margin-bottom: 20px;
  color: #333;
}

/* Contact Section */
#contact {
  padding: 80px 0;
  background-color: #1f1f1f;
  color: #fff;
  text-align: center;
}

#contact h2 {
  font-size: 2.5rem;
  margin-bottom: 30px;
}

#contact p {
  font-size: 1.1rem;
  margin-bottom: 20px;
}

.contact-links {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin-top: 20px;
}

.contact-links a {
  color: #ffd700;
  font-size: 1.5rem;
  transition: color 0.3s ease;
}

.contact-links a:hover {
  color: #fff;
}

/* Footer */
footer {
  background-color: #000;
  color: #fff;
  padding: 20px 0;
  text-align: center;
  margin-top: auto;
}

/* Animations */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Responsive */
@media (max-width: 768px) {
  .nav-links {
    display: none;
  }

  .hero h1 {
    font-size: 2.2rem;
  }

  .about-content {
    flex-direction: column;
    text-align: center;
  }

  .skills-list li {
    padding: 10px 20px;
  }

  .project-card {
    padding: 20px;
  }
}

  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar">
    <div class="container">
      <div class="logo">Mr. AB</div>
      <ul class="nav-links">
        <li><a href="about.html">About</a></li>
        <li><a href="skills.html">Skills</a></li>
        <li><a href="projects.html">Projects</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="hero">
    <div class="container">
      <h1>Hello, I'm Mr. AB</h1>
      <p>A Passionate Web Developer and Creative Designer</p>
      <a href="contact.html" class="btn">Find me</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about">
    <div class="container about-content">
      <img src="C:\Users\Birendra king\Downloads\mr_ab_portfolio//profile.jpg" alt="Mr. AB">
      <p>
        I’m Mr. AB, a student, web developer, and learner with a passion for clean design and functional development. <br><br>
        I love using tools like Blender 🌀, VS Code 💻, Copen 🖥, and Canva 🎨 to bring ideas to life. I create content on YouTube 📹, X (Twitter) 🐦, and Facebook 📘.<br><br>
        Music runs in my veins 🎶. I play and sing with my guitar 🎸, and I love traveling to find peace and inspiration 🌍. Sleeping is my superpower 💤, and I cherish exploring new places.<br><br>
        I follow Lord Shiva 🙏, and believe life is a grand simulation — nothing is as it seems 🌌.<br><br>
        I’m also deeply interested in the ancient Greek language 🇬🇷 — its wisdom, power, and history fascinate me endlessly.<br><br>
        “Η ζωή είναι ένας αγώνας για να βρεις την αλήθεια, και η αλήθεια βρίσκεται μέσα σου.”<br>
        <i>(Life is a struggle to find the truth, and the truth lies within you.)</i><br><br>
        “Το σύμπαν είναι το έργο της συνείδησης.”<br>
        <i>(The universe is the work of consciousness.)</i><br><br>
        Let's create, connect, and explore the infinite. 🚀
      </p>
    </div>
  </section>

  <!-- Skills Section -->
  <section id="skills">
    <div class="container">
      <h2>My Skills</h2>
      <ul class="skills-list">
        <li>HTML-Intermediate</li>
        <li>CSS-Intermediate</li>
        <li>WordPress-Basic</li>
        <li>C Programming-Intermediate</li>
        <li>Canva-Intermediate</li>
        <li>Blander-Basic</li>
      </ul>
    </div>
  </section>
<p><b><i>I'm tring to improve my skills and also tring to learn new skills.</p></b></i>

 <!-- Projects Section -->
 <section id="projects">
    <div class="container">
      <h2>Projects</h2>
      <div class="projects-container">
        <div class="project-card">
          <h3>project1</h3>
          <p>Not ready.</p>
        </div>
        <div class="project-card">
          <h3>project2</h3>
          <p>Not ready.</p>
        </div>
        <div class="project-card">
          <h3>project3</h3>
          <p>Not ready</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
<section id="contact">
    <div class="container">
      <h2>Contact Me</h2>
      <p>Have a project in mind or want to connect? Reach out to me!</p>
      <div class="contact-links">
        <a href="mailto:agrimbhatta1@gmail.com" title="Email">
          <i class="fas fa-envelope"></i>
        </a>
        <a href="https://github.com/agrimbhatta" target="_blank" title="GitHub">
          <i class="fab fa-github"></i>
        </a>
        <a href="https://twitter.com/agrimbhatta" target="_blank" title="Twitter">
          <i class="fab fa-twitter"></i>
        </a>
        <a href="https://www.linkedin.com/" target="_blank" title="LinkedIn">
          <i class="fab fa-linkedin"></i>
        </a>
      </div>
    </div>
  </section>

  <!-- Footer -->
<footer>
  <div class="container">
  <p>.Mr.AB.❤️❤️❤️ .</p>
</div>
</footer>

</body>
</html>
