<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aurora Jewellery 💎</title>
  <style>
    :root {
      --accent: #ffb6c1;
      --text: #111;
      --bg: #fff0f5;
    }
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: var(--bg);
      color: var(--text);
      scroll-behavior: smooth;
    }
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 6%;
      background: var(--accent);
      color: black;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 26px;
      letter-spacing: 1px;
    }
    nav a {
      margin: 0 12px;
      text-decoration: none;
      color: black;
      font-weight: 500;
    }
    nav a:hover {
      text-decoration: underline;
    }
    section {
      padding: 60px 8%;
    }
    h2 {
      font-family: 'Playfair Display', serif;
      text-align: center;
      font-size: 32px;
      color: var(--text);
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 24px;
      margin-top: 20px;
    }
    .product {
      background: white;
      border-radius: 14px;
      padding: 16px;
      text-align: center;
      box-shadow: 0 3px 6px rgba(0,0,0,0.1);
      transition: transform .2s;
    }
    .product:hover {
      transform: translateY(-5px);
    }
    .product img {
      width: 100%;
      border-radius: 10px;
      height: 200px;
      object-fit: cover;
    }
    .btn {
      background: var(--accent);
      border: none;
      padding: 10px 18px;
      border-radius: 10px;
      cursor: pointer;
      margin: 6px;
      font-weight: 600;
    }
    .btn:hover {
      background: #ff9ab3;
    }
    footer {
      background: var(--accent);
      padding: 40px 8%;
      color: black;
    }
    footer div {
      max-width: 800px;
      margin: 0 auto;
      text-align: center;
    }

    /* Popup message box 💬 */
    .popup {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 5px 25px rgba(0,0,0,0.2);
      z-index: 1000;
      width: 90%;
      max-width: 400px;
    }
    .popup h3 {
      margin-top: 0;
      text-align: center;
    }
    .popup input, .popup textarea {
      width: 100%;
      padding: 10px;
      border-radius: 10px;
      border: 1px solid #ccc;
      margin-top: 10px;
    }
    .popup button {
      margin-top: 12px;
      width: 100%;
      padding: 12px;
      background: var(--accent);
      border: none;
      border-radius: 10px;
      font-weight: 600;
      cursor: pointer;
    }
    .popup button:hover {
      background: #ff9ab3;
    }
    .overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(0,0,0,0.4);
      z-index: 999;
    }
    .close-btn {
      position: absolute;
      top: 10px;
      right: 14px;
      font-size: 20px;
      background: none;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>

<header>
  <h1>💎 Aurora Jewellery</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#collections">Collections</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section id="home">
  <h2>Welcome to Aurora Jewellery ✨</h2>
  <p style="text-align:center;max-width:700px;margin:20px auto;">
    Discover timeless, handcrafted jewellery made with love and care.  
    Elegant. Sustainable. Beautiful. 💖
  </p>
</section>

<section id="collections">
  <h2>Our Collections 💍</h2>
  <div class="grid">
    <div class="product">
      <img src="https://yourdomain.com/images/pearl-pendant.jpg" alt="Pearl Pendant">
      <h4>Pearl Pendant</h4>
      <p>$85</p>
      <button class="btn">Add to Cart</button>
      <button class="btn">View</button>
    </div>
    <div class="product">
      <img src="https://yourdomain.com/images/hoop-earrings.jpg" alt="Hoop Earrings">
      <h4>Hoop Earrings</h4>
      <p>$40</p>
      <button class="btn">Add to Cart</button>
      <button class="btn">View</button>
    </div>
    <div class="product">
      <img src="https://yourdomain.com/images/bar-necklace.jpg" alt="Bar Necklace">
      <h4>Bar Necklace</h4>
      <p>$60</p>
      <button class="btn">Add to Cart</button>
      <button class="btn">View</button>
    </div>
  </div>
</section>

<section id="about" style="background:white;">
  <h2>About Aurora Jewellery 💫</h2>
  <p style="max-width:800px;margin:20px auto;text-align:center;">
    Aurora Jewellery creates delicate, timeless pieces handcrafted with care  
    using ethically sourced materials from around the world.  
    Each design is inspired by nature, art, and everyday beauty. 🌸
  </p>
</section>

<section id="contact">
  <h2>Contact Us 💌</h2>
  <div style="max-width:700px;margin:0 auto;text-align:center;">
    <p><strong>📞 Phone:</strong> +64 123 456 789</p>
    <p><strong>📧 Email:</strong> ramandeol@example.com</p>
    <p><strong>📍 Address:</strong> Auckland, New Zealand</p>
  </div>
  <div style="text-align:center;margin-top:20px;">
    <button class="btn" onclick="openPopup()">💬 Message Us</button>
  </div>
</section>

<!-- Message popup 💌 -->
<div class="overlay" id="overlay" onclick="closePopup()"></div>
<div class="popup" id="popup">
  <button class="close-btn" onclick="closePopup()">✖</button>
  <h3>💌 Send us a message</h3>
  <form id="messageForm">
    <input type="text" name="name" placeholder="Your Name 😊" required>
    <input type="email" name="email" placeholder="Your Email 📧" required>
    <textarea name="message" rows="5" placeholder="Your Message 💖" required></textarea>
    <button type="submit">Send Message ✨</button>
  </form>
</div>

<footer>
  <div>
    <p>© 2025 Aurora Jewellery. Crafted with love 💗 in New Zealand.</p>
  </div>
</footer>

<script>
  function openPopup() {
    document.getElementById('popup').style.display = 'block';
    document.getElementById('overlay').style.display = 'block';
  }

  function closePopup() {
    document.getElementById('popup').style.display = 'none';
    document.getElementById('overlay').style.display = 'none';
  }

  document.getElementById('messageForm').addEventListener('submit', function(e){
    e.preventDefault();
    alert('💌 Thank you for your message! We’ll get back to you soon.');
    this.reset();
    closePopup();
  });
</script>

</body>
</html>


