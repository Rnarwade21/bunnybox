# bunnybox
#script.js#
function addReview() {
  const text = document.querySelector("textarea").value;
  if (!text) return;

  const review = document.createElement("div");
  review.innerText = text;
  review.style.marginTop = "10px";

  document.getElementById("reviewList").appendChild(review);
  document.querySelector("textarea").value = "";
}
:root {
  --white: #FFFFFF;
  --pink: #E281B1;
  --black: #050304;
  --green: #2A0E3C;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Georgia', serif;
}

body {
  background: var(--white);
  color: var(--black);
}

header {
  display: flex;
  justify-content: space-between;
  padding: 20px 40px;
  background: var(--pink);
}

.logo {
  font-size: 28px;
  font-weight: bold;
}
.logo span {
  color: var(--black);
}

nav a {
  margin: 0 15px;
  text-decoration: none;
  color: var(--black);
}

.hero {
  padding: 80px;
  text-align: center;
  background: linear-gradient(#fff, #f8e1ec);
}

section {
  padding: 60px 40px;
}

.cards, .product-grid {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.card {
  padding: 30px;
  background: #f9f9f9;
  border-radius: 15px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.1);
}

.product {
  width: 250px;
  text-align: center;
}

.product-3d {
  height: 200px;
  background: var(--pink);
  border-radius: 20px;
  transform-style: preserve-3d;
  transition: transform 0.6s;
}

.product-3d:hover {
  transform: rotateY(20deg) rotateX(10deg);
}

.skincare { background: #f3c7da; }
.mug { background: #d9b3c8; }

button {
  margin-top: 10px;
  padding: 10px;
  background: var(--black);
  color: white;
  border: none;
  cursor: pointer;
}

textarea {
  width: 100%;
  height: 80px;
  margin: 10px 0;
}

#style.css#
footer {
  padding: 20px;
  background: var(--pink);
  text-align: center;
}

/* LOTUS */
.lotus {
  position: fixed;
  top: 0;
  width: 80px;
  height: 100vh;
  background: linear-gradient(var(--green), transparent);
  animation: sway 4s ease-in-out infinite;
}
.left { left: 0; }
.right { right: 0; }

@keyframes sway {
  0%,100% { transform: rotate(0deg); }
  50% { transform: rotate(2deg); }
}
#index.html#
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Bunny Box | Premium Hampers</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<!-- LOTUS ANIMATION -->
<div class="lotus left"></div>
<div class="lotus right"></div>

<!-- HEADER -->
<header>
  <div class="logo">
    🐰 Bunny <span>Box</span>
  </div>
  <nav>
    <a href="#hampers">Hampers</a>
    <a href="#products">Products</a>
    <a href="#reviews">Reviews</a>
    <a href="#payment">Payment</a>
  </nav>
</header>

<!-- HERO -->
<section class="hero">
  <h1>Luxury Hampers, Curated with Love</h1>
  <p>Jewellery • Beauty • Skincare • Mugs</p>
</section>

<!-- HAMPERS -->
<section id="hampers">
  <h2>Gift Hampers</h2>
  <div class="cards">
    <div class="card">4 Items Hamper – ₹999</div>
    <div class="card">5 Items Hamper – ₹1299</div>
    <div class="card">6 Items Hamper – ₹1599</div>
    <div class="card">7 Items Hamper – ₹1899</div>
    <div class="card">8 Items Hamper – ₹2199</div>
    <div class="card">9 Items Hamper – ₹2499</div>
  </div>
</section>

<!-- PRODUCTS -->
<section id="products">
  <h2>Single Products</h2>

  <div class="product-grid">

    <div class="product">
      <div class="product-3d"></div>
      <h3>Elegant Ring</h3>
      <p>₹399</p>
      <button>Add to Cart</button>
    </div>

    <div class="product">
      <div class="product-3d skincare"></div>
      <h3>Luxury Lipstick</h3>
      <p>₹499</p>
      <button>Add to Cart</button>
    </div>

    <div class="product">
      <div class="product-3d mug"></div>
      <h3>Ceramic Mug</h3>
      <p>₹349</p>
      <button>Add to Cart</button>
    </div>

  </div>
</section>

<!-- REVIEWS -->
<section id="reviews">
  <h2>Customer Reviews</h2>

  <textarea placeholder="Write your review..."></textarea>
  <select>
    <option>⭐⭐⭐⭐⭐</option>
    <option>⭐⭐⭐⭐</option>
    <option>⭐⭐⭐</option>
    <option>⭐⭐</option>
    <option>⭐</option>
  </select>
  <button onclick="addReview()">Submit</button>

  <div id="reviewList"></div>
</section>

<!-- PAYMENT -->
<section id="payment">
  <h2>Payment</h2>
  <p>Accepted Payments:</p>
  <ul>
    <li>UPI</li>
    <li>Debit Card</li>
    <li>Credit Card</li>
    <li>Net Banking</li>
  </ul>
  <button class="pay">Pay in INR ₹</button>
</section>

<footer>
  © 2025 Bunny Box | Premium Gifting
</footer>

<script src="script.js"></script>
</body>
</html>

