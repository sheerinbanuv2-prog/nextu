# nextu
Digital protofile
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>- NextYou-sheerin banu V</title>
  <style>
    /* Base Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    
    body {
      background-color: #f9f9f9;
      color: #333;
      line-height: 1.6;
      overflow-x: hidden;
    }
    
    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }
    
    h1, h2, h3 {
      margin-bottom: 20px;
    }
    
    /* Header Styles with Animation */
    header {
      background: linear-gradient(135deg, #6e8efb, #a777e3);
      color: white;
      text-align: center;
      padding: 60px 20px;
      position: relative;
      overflow: hidden;
    }
    
    header::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,128L48,117.3C96,107,192,85,288,112C384,139,480,213,576,218.7C672,224,768,160,864,138.7C960,117,1056,139,1152,149.3C1248,160,1344,160,1392,160L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
      background-size: cover;
      background-position: center;
      animation: waveAnimation 10s linear infinite;
    }
    
    @keyframes waveAnimation {
      0% {
        transform: translateX(0) translateY(0);
      }
      50% {
        transform: translateX(-25%) translateY(10%);
      }
      100% {
        transform: translateX(0) translateY(0);
      }
    }
    
    header h1 {
      font-size: 3.5rem;
      margin-bottom: 10px;
      opacity: 0;
      animation: fadeInDown 1s ease forwards 0.5s;
      position: relative;
    }
    
    header p {
      font-size: 1.2rem;
      opacity: 0;
      animation: fadeInUp 1s ease forwards 0.8s;
      position: relative;
    }
    
    /* Home Section with Animation */
    .home {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      min-height: 80vh;
    }
    
    .home .text {
      flex: 1;
      min-width: 300px;
      padding: 20px;
      opacity: 0;
      transform: translateX(-50px);
      animation: slideInLeft 1s ease forwards 1s;
    }
    
    .home .text h2 {
      font-size: 2.5rem;
      margin-bottom: 20px;
    }
    
    .home .text span {
      color: #a777e3;
      font-weight: bold;
    }
    
    .home .image {
      flex: 1;
      min-width: 300px;
      text-align: center;
      opacity: 0;
      transform: translateX(50px);
      animation: slideInRight 1s ease forwards 1s;
    }
    
    .home .image img {
      width: 100%;
      max-width: 350px;
      height: auto;
      border-radius: 50%;
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
      transition: all 0.5s ease;
    }
    
    .home .image img:hover {
      transform: scale(1.05) rotate(5deg);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
    }
    
    /* About Section with Animation */
    .about {
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      padding: 40px;
      margin: 40px auto;
      opacity: 0;
      transform: translateY(50px);
      animation: fadeInUp 1s ease forwards 1.2s;
    }
    
    .about h2 {
      color: #6e8efb;
      text-align: center;
      margin-bottom: 30px;
      position: relative;
    }
    
    .about h2::after {
      content: '';
      position: absolute;
      bottom: -10px;
      left: 50%;
      transform: translateX(-50%);
      width: 80px;
      height: 4px;
      background: linear-gradient(to right, #6e8efb, #a777e3);
      border-radius: 2px;
    }
    
    .about p {
      font-size: 1.1rem;
      text-align: center;
      max-width: 800px;
      margin: 0 auto;
    }
    
    /* Project Section with Animation */
    .project {
      background: linear-gradient(135deg, #6e8efb, #a777e3);
      color: white;
      border-radius: 10px;
      padding: 40px;
      margin: 40px auto;
      opacity: 0;
      transform: translateY(50px);
      animation: fadeInUp 1s ease forwards 1.4s;
    }
    
    .project h2 {
      text-align: center;
      margin-bottom: 30px;
    }
    
    .project p {
      font-size: 1.1rem;
      text-align: center;
      max-width: 800px;
      margin: 0 auto;
    }
    
    /* Contact Section with Animation */
    .contact {
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      padding: 40px;
      margin: 40px auto;
      opacity: 0;
      transform: translateY(50px);
      animation: fadeInUp 1s ease forwards 1.6s;
    }
    
    .contact h2 {
      color: #6e8efb;
      text-align: center;
      margin-bottom: 30px;
    }
    
    #contactForm {
      display: flex;
      flex-direction: column;
      max-width: 600px;
      margin: 0 auto;
    }
    
    #contactForm input,
    #contactForm textarea {
      padding: 15px;
      margin-bottom: 20px;
      border: 1px solid #ddd;
      border-radius: 5px;
      font-size: 1rem;
      transition: all 0.3s ease;
    }
    
    #contactForm input:focus,
    #contactForm textarea:focus {
      outline: none;
      border-color: #a777e3;
      box-shadow: 0 0 0 2px rgba(167, 119, 227, 0.2);
      transform: scale(1.02);
    }
    
    #contactForm button {
      padding: 15px;
      background: linear-gradient(to right, #6e8efb, #a777e3);
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 1.1rem;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    
    #contactForm button:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    }
    
    #contactForm button:active {
      transform: translateY(0);
    }
    
    #msg {
      text-align: center;
      margin-top: 20px;
      font-weight: bold;
      opacity: 0;
      transition: opacity 0.3s ease;
    }
    
    /* Footer Styles */
    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
    
    /* Animation Keyframes */
    @keyframes fadeInDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    @keyframes slideInLeft {
      from {
        opacity: 0;
        transform: translateX(-50px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }
    
    @keyframes slideInRight {
      from {
        opacity: 0;
        transform: translateX(50px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }
    
    /* Media Queries for Responsiveness */
    @media (max-width: 768px) {
      .home {
        flex-direction: column;
        text-align: center;
      }
      
      header h1 {
        font-size: 2.5rem;
      }
      
      .home .text h2 {
        font-size: 2rem;
      }
      
      section {
        padding: 60px 20px;
      }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <h1>NextYou</h1>
    <p>A Creative Digital Portfolio</p>
  </header>

  <!-- Home Section -->
  <section class="home">
    <div class="text">
      <h2>Hello, I’m <span>sheerin banu V</span></h2>
      <p>2nd Year BCAB Student at MMES Women’s Arts & Science College</p>
    </div>
    <div class="image">
      <img src="https://via.placeholder.com/350x350.png?text=FutureMe" alt="Profile Picture">
    </div>
  </section>

  <!-- About Section -->
  <section class="about">
    <h2>About Me</h2>
    <p>I am a student learning web technologies like HTML, CSS, and JavaScript.  
       I enjoy designing clean websites and simple portfolios.  
       My goal is to improve step by step and grow as a web developer.</p>
  </section>

  <!-- Project Section -->
  <section class="project">
    <h2>🌐 About NextYou</h2>
    <p>Driven by a love for problem-solving and a flair for creativity, I craft digital experiences that engage, inspire, and deliver impact. By merging technical expertise with innovative thinking, I develop solutions that are not only functional but also intuitive, scalable, and visually stunning
     </p>
  </section>

  <!-- Contact Section -->
  <section class="contact">
    <h2>📩 Contact Me</h2>
    <form id="contactForm">
      <input type="text" id="name" placeholder="Your Name" required>
      <input type="email" id="email" placeholder="Your Email" required>
      <textarea id="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="msg"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 NextYou | sheerin banu V</p>
  </footer>

  <script>
    // Form submission handling
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      e.preventDefault();
      
      // Get form values
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const message = document.getElementById('message').value;
      
      // Simple validation
      if (name && email && message) {
        // Show success message with animation
        const msgElement = document.getElementById('msg');
        msgElement.textContent = 'Thank you for your message! I will get back to you soon.';
        msgElement.style.color = '#4CAF50';
        msgElement.style.opacity = '1';
        
        // Reset form
        document.getElementById('contactForm').reset();
        
        // Hide message after 5 seconds
        setTimeout(() => {
          msgElement.style.opacity = '0';
        }, 5000);
      } else {
        // Show error message
        const msgElement = document.getElementById('msg');
        msgElement.textContent = 'Please fill in all fields.';
        msgElement.style.color = '#F44336';
        msgElement.style.opacity = '1';
        
        // Hide message after 5 seconds
        setTimeout(() => {
          msgElement.style.opacity = '0';
        }, 5000);
      }
    });
    
    // Add scroll animations for sections
    document.addEventListener('DOMContentLoaded', function() {
      const sections = document.querySelectorAll('section');
      
      // Intersection Observer for scroll animations
      const observerOptions = {
        root: null,
        rootMargin: '0px',
        threshold: 0.1
      };
      
      const observer = new IntersectionObserver(function(entries, observer) {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.opacity = '1';
            entry.target.style.transform = 'translateY(0)';
            observer.unobserve(entry.target);
          }
        });
      }, observerOptions);
      
      // Observe all sections except home (which already has animation)
      document.querySelectorAll('.about, .project, .contact').forEach(section => {
        observer.observe(section);
      });
    });
  </script>
</body>
</html>
