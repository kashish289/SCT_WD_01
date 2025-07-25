# SCT_WD_01
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Modern Commercial Website</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      color: #fff;
      background-color: #111;
    }

    /* ===== NAVIGATION BAR ===== */
    .navbar {
      position: fixed;
      width: 100%;
      top: 0;
      left: 0;
      padding: 20px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background-color: transparent;
      transition: 0.4s ease;
      z-index: 1000;
    }

    .navbar.scrolled {
      background-color: rgba(0, 0, 0, 0.9);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
    }

    .logo {
      font-size: 28px;
      font-weight: bold;
      color: #fff;
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 30px;
    }

    .nav-links a {
      color: #fff;
      text-decoration: none;
      font-size: 16px;
      padding: 8px 12px;
      border-radius: 4px;
      transition: background 0.3s ease;
    }

    .nav-links a:hover {
      background-color: #fff;
      color: #000;
    }

    /* ===== HERO SECTION ===== */
    .hero {
      height: 100vh;
      background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      text-align: center;
    }

    .overlay {
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.5);
    }

    .hero-content {
      position: relative;
      z-index: 1;
      color: #fff;
      max-width: 800px;
      padding: 20px;
      animation: fadeInUp 1.5s ease;
    }

    .hero-content h1 {
      font-size: 50px;
      margin-bottom: 20px;
    }

    .hero-content p {
      font-size: 20px;
      margin-bottom: 30px;
    }

    .hero-btn {
      text-decoration: none;
      padding: 12px 28px;
      background: #fff;
      color: #000;
      font-weight: bold;
      border-radius: 30px;
      transition: background 0.3s ease;
    }

    .hero-btn:hover {
      background: #ddd;
    }

    /* ===== CONTENT SECTION ===== */
    .content {
      padding: 80px 60px;
      background-color: #fff;
      color: #333;
      text-align: center;
    }

    .content h2 {
      font-size: 32px;
      margin-bottom: 20px;
    }

    .content p {
      font-size: 18px;
      max-width: 700px;
      margin: auto;
    }

    /* ===== ANIMATION ===== */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <nav class="navbar" id="navbar">
    <div class="logo"> yaho</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Hero Section -->
  <header class="hero">
    <div class="overlay"></div>
    <div class="hero-content">
      <h1>Build Your Future</h1>
      <p>Professional solutions for modern businesses.</p>
      <a href="#" class="hero-btn">Get Started</a>
    </div>
  </header>

  <!-- Content Section -->
  <section class="content">
    <h2>Why Choose Us</h2>
    <p>We combine technology, creativity, and strategy to deliver outstanding results for your business.</p>
  </section>

  <!-- JavaScript -->
  <script>
    const navbar = document.getElementById("navbar");
    window.addEventListener("scroll", () => {
      navbar.classList.toggle("scrolled", window.scrollY > 50);
    });
  </script>

</body>
</html>
