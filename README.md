# FrontEnd-Test
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Responsive Landing Page</title>
    <style>
        /* Inline Critical CSS */
        body{font-family:Arial,sans-serif;line-height:1.6;background:#f9f9f9;margin:0;padding:0}
        .header{background:#333;color:#fff;padding:1rem;text-align:center}
        .hero{display:flex;flex-direction:column;justify-content:center;align-items:center;background:#007bff;color:#fff;padding:3rem 1rem;text-align:center}
        .footer{text-align:center;padding:1rem;background:#333;color:#fff;margin-top:2rem}
    </style>
    <link rel="stylesheet" href="styles.min.css" media="print" onload="this.media='all'">
</head>
<body>
    <!-- Header -->
    <header class="header">
        <nav class="navbar">
            <div class="logo">MyBrand</div>
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <picture>
            <source srcset="hero-bg.webp" type="image/webp">
            <img src="hero-bg.jpg" alt="Hero Background" loading="lazy">
        </picture>
        <div class="hero-content">
            <h1>Welcome to Our Landing Page</h1>
            <p>Discover the best solutions for your business.</p>
            <div class="hero-buttons">
                <button class="cta">Call to Action</button>
                <button class="see-more">See More</button>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="feature">
            <h2>Feature 1</h2>
            <p>Highlight the first unique feature of the product or service.</p>
        </div>
        <div class="feature">
            <h2>Feature 2</h2>
            <p>Provide insight into a second important feature.</p>
        </div>
        <div class="feature">
            <h2>Feature 3</h2>
            <p>Detail a third, equally compelling feature.</p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2024 MyBrand. All rights reserved.</p>
    </footer>
</body>
</html>


style.min.css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background: #f9f9f9;
  margin: 0;
}

a {
  text-decoration: none;
}

.header {
  background: #333;
  color: #fff;
  padding: 1rem;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1rem;
}

.hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #007bff;
  color: #fff;
  text-align: center;
  padding: 5rem 1rem;
}

.hero-content {
  max-width: 600px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
}

.hero-buttons button {
  padding: 0.7rem 1.5rem;
  border: none;
  cursor: pointer;
  font-size: 1rem;
  flex-grow: 1;
  flex-basis: 40%;
}

.cta {
  background: #007bff;
  color: #fff;
}

.see-more {
  background: #6c757d;
  color: #fff;
}

.features {
  display: flex;
  justify-content: center;
  gap: 2rem;
  padding: 2rem;
  flex-wrap: wrap;
}

.feature {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #f4f4f4;
  padding: 1rem;
  border-radius: 8px;
  text-align: center;
  flex: 1 1 calc(100% / 3 - 1rem);
}

.feature:nth-child(odd) {
  background: #e8e8e8;
}

.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 1rem;
  background: #333;
  color: #fff;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .features {
    flex-direction: column;
    gap: 1rem;
  }

  .hero-buttons {
    flex-direction: column;
  }

  .hero-buttons button {
    width: 100%;
  }

  .feature {
    flex: 1 1 100%;
  }
}

@media (max-width: 480px) {
  .hero {
    padding: 3rem 1rem;
  }

  .hero-content {
    text-align: center;
  }

  .nav-links {
    flex-direction: column;
    gap: 0.5rem;
  }
}
