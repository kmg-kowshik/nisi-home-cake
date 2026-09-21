<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Nisi Home Bakes — homemade birthday cakes, tea cakes, banana cakes and brownies.">
<title>Nisi Home Bakes | Sweet Moments, Made at Home</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=DM+Sans:wght@400;500;600;700&family=Great+Vibes&display=swap" rel="stylesheet">

<style>
:root{
  --ink:#321915;
  --cocoa:#5a2d25;
  --rose:#d85c78;
  --rose2:#ef8fa4;
  --blush:#f9dfe4;
  --cream:#fff9f4;
  --vanilla:#fffdf9;
  --gold:#c59a58;
  --line:#ecd5d0;
  --green:#1e8b57;
  --shadow:0 20px 60px rgba(75,38,29,.13);
  --radius:24px;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;background:var(--cream);color:var(--ink);
  font-family:"DM Sans",sans-serif;line-height:1.55;
}
body.cart-open{overflow:hidden}
a{text-decoration:none;color:inherit}
button,input,select{font:inherit}
button{cursor:pointer}
img{max-width:100%;display:block}
.container{width:min(1180px,92%);margin:auto}

/* TOP BAR */
.topbar{
  background:var(--ink);color:#ffece8;font-size:12px;
  letter-spacing:.4px;padding:8px 0;text-align:center;
}
.topbar strong{color:#fff}

/* NAV */
nav{
  position:sticky;top:0;z-index:80;background:rgba(255,249,244,.96);
  backdrop-filter:blur(14px);border-bottom:1px solid var(--line);
}
.nav-inner{min-height:76px;display:flex;align-items:center;gap:24px;justify-content:space-between}
.brand{display:flex;align-items:center;gap:11px;min-width:max-content}
.brand img{width:50px;height:50px;object-fit:cover;border-radius:50%;border:2px solid var(--blush)}
.brand-name{font:31px "Great Vibes",cursive;color:var(--ink)}
.links{display:flex;gap:23px;font-size:14px;font-weight:700;color:#68463d}
.links a:hover{color:var(--rose)}
.nav-actions{display:flex;align-items:center;gap:10px}
.nav-cart{
  position:relative;border:1px solid #e7c3c4;background:#fff;
  border-radius:999px;padding:10px 15px;font-weight:800;color:var(--cocoa);
}
.cart-count{
  position:absolute;right:-4px;top:-7px;min-width:21px;height:21px;
  padding:0 5px;border-radius:50%;background:var(--rose);color:white;
  display:grid;place-items:center;font-size:11px;border:2px solid var(--cream);
}
.order-btn{
  border:0;border-radius:999px;padding:11px 18px;background:var(--rose);
  color:white;font-weight:800;box-shadow:0 8px 22px rgba(216,92,120,.28)
}

/* HERO */
.hero{
  position:relative;overflow:hidden;padding:80px 0 70px;
  background:
   radial-gradient(circle at 0 15%,rgba(249,223,228,.95),transparent 27%),
   radial-gradient(circle at 100% 0,rgba(239,143,164,.18),transparent 30%),
   linear-gradient(135deg,#fffdf9 0%,#fff2ee 100%);
}
.hero:before,.hero:after{
  content:"♡";position:absolute;color:rgba(216,92,120,.12);
  font-family:"Great Vibes",cursive;font-size:240px;line-height:1;
}
.hero:before{left:-50px;bottom:-90px}.hero:after{right:-30px;top:-75px}
.hero-grid{position:relative;z-index:1;display:grid;grid-template-columns:1.05fr .95fr;gap:60px;align-items:center}
.eyebrow{
  display:inline-block;background:#ffe5ea;color:#a63d59;border:1px solid #f0c0ca;
  border-radius:999px;padding:7px 14px;font-size:11px;font-weight:800;letter-spacing:1.4px;text-transform:uppercase;
}
.hero h1{
  font:700 clamp(58px,7vw,92px)/.86 "Cormorant Garamond",serif;
  margin:19px 0 14px;letter-spacing:-2px;
}
.hero h1 span{display:block;color:var(--rose);font:normal .72em/1 "Great Vibes",cursive;margin-top:15px;letter-spacing:0}
.hero p{max-width:600px;font-size:18px;color:#75554c}
.actions{display:flex;gap:12px;flex-wrap:wrap;margin:26px 0 18px}
.btn{min-height:48px;padding:0 21px;border-radius:999px;display:inline-flex;align-items:center;justify-content:center;font-weight:800;border:1px solid transparent}
.btn-main{background:var(--rose);color:#fff;box-shadow:0 12px 26px rgba(216,92,120,.25)}
.btn-main:hover{background:#bd4562;transform:translateY(-2px)}
.btn-ghost{background:#fff;border-color:#dfb7bb;color:var(--cocoa)}
.badges{display:flex;gap:9px;flex-wrap:wrap}
.badge{background:#fff;border:1px solid var(--line);padding:7px 11px;border-radius:999px;font-size:12px;color:#74544b;font-weight:700}
.hero-art{
  background:#fff;border:1px solid var(--line);padding:13px;border-radius:32px;
  box-shadow:var(--shadow);transform:rotate(1deg);position:relative;
}
.hero-art img{width:100%;aspect-ratio:1/1;object-fit:cover;border-radius:23px}
.stamp{
  position:absolute;right:-20px;bottom:25px;width:116px;height:116px;border-radius:50%;
  background:var(--cocoa);color:#fff;display:grid;place-items:center;text-align:center;
  font:700 19px/1 "Cormorant Garamond",serif;border:6px solid var(--cream);transform:rotate(-8deg)
}

/* SECTION */
.section{padding:82px 0}
.soft{background:#fff0ec}
.section-head{text-align:center;max-width:720px;margin:0 auto 42px}
.kicker{font-size:11px;text-transform:uppercase;letter-spacing:2px;color:#a63d59;font-weight:900}
.section-title{font:700 49px/1 "Cormorant Garamond",serif;margin:8px 0 12px}
.section-head p{color:#7c5e55}

/* PRODUCTS */
.products{display:grid;grid-template-columns:repeat(4,1fr);gap:19px}
.product{
  background:#fff;border:1px solid var(--line);border-radius:var(--radius);
  overflow:hidden;box-shadow:0 10px 32px rgba(74,33,25,.07);transition:.25s;
}
.product:hover{transform:translateY(-5px);box-shadow:var(--shadow)}
.product-photo{height:220px;overflow:hidden;background:#f7e0da}
.product-photo img{width:100%;height:100%;object-fit:cover;transition:.3s}
.product:hover img{transform:scale(1.05)}
.product-body{padding:18px}
.product h3{font:700 28px/1 "Cormorant Garamond",serif;margin-bottom:6px}
.product p{font-size:13px;color:#80645b;min-height:40px}
.product-bottom{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-top:13px}
.product-price{font-size:16px;font-weight:900;color:#a63d59}
.add{
  border:0;background:var(--ink);color:#fff;border-radius:12px;padding:10px 13px;
  font-size:12px;font-weight:800
}
.add:hover{background:var(--rose)}

/* PRICE LIST */
.price-wrap{overflow:auto;border-radius:var(--radius);border:1px solid var(--line);background:#fff;box-shadow:var(--shadow)}
table{width:100%;min-width:650px;border-collapse:collapse}
th{background:var(--ink);color:#fff;text-align:left;padding:16px 18px;font-size:12px;letter-spacing:1px;text-transform:uppercase}
td{padding:15px 18px;border-bottom:1px solid #f1dddd}
tbody tr:nth-child(even){background:#fff8f6}
tbody tr:last-child td{border:0}
.price-note{margin-top:15px;background:#fff4df;border:1px solid #ebd29f;border-radius:15px;padding:14px 16px;font-size:13px;color:#6d4e2e}

/* ORIGINAL MENU */
.gallery{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.gallery-card{background:#fff;border:1px solid var(--line);padding:10px;border-radius:25px;box-shadow:0 10px 30px rgba(74,33,25,.08)}
.gallery-card img{width:100%;border-radius:17px}

/* CTA */
.cta{
  background:linear-gradient(135deg,#3a1c17 0%,#693329 52%,#c84868 100%);
  color:#fff;border-radius:34px;padding:50px;display:grid;grid-template-columns:1.15fr .85fr;
  gap:35px;align-items:center;box-shadow:var(--shadow);position:relative;overflow:hidden
}
.cta:after{content:"♡";position:absolute;right:-30px;top:-90px;color:rgba(255,255,255,.07);font:260px "Great Vibes",cursive}
.cta h2{font:700 55px/.92 "Cormorant Garamond",serif;margin:10px 0 14px;position:relative;z-index:1}
.cta p{color:#ffe6eb;max-width:600px;position:relative;z-index:1}
.contact-box{background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.2);border-radius:22px;padding:22px;position:relative;z-index:1}
.contact-row{padding:12px 0;border-bottom:1px solid rgba(255,255,255,.18)}
.contact-row:last-child{border:0}

/* CART DRAWER */
.cart-overlay{position:fixed;inset:0;background:rgba(36,16,13,.45);z-index:150;opacity:0;pointer-events:none;transition:.25s}
.cart-overlay.open{opacity:1;pointer-events:auto}
.cart{
  position:fixed;right:0;top:0;height:100%;width:min(450px,94vw);background:var(--vanilla);
  z-index:160;transform:translateX(100%);transition:.3s;box-shadow:-20px 0 60px rgba(0,0,0,.2);
  display:flex;flex-direction:column
}
.cart.open{transform:translateX(0)}
.cart-head{padding:22px 22px 16px;border-bottom:1px solid var(--line);display:flex;align-items:center;justify-content:space-between}
.cart-head h2{font:700 35px/1 "Cormorant Garamond",serif}
.close{width:38px;height:38px;border-radius:50%;border:1px solid var(--line);background:#fff;font-size:22px}
.cart-items{flex:1;overflow:auto;padding:15px 20px}
.empty{text-align:center;color:#84665d;padding:60px 15px}
.cart-item{display:grid;grid-template-columns:72px 1fr auto;gap:12px;padding:13px 0;border-bottom:1px solid #f0dede}
.cart-item img{width:72px;height:72px;border-radius:14px;object-fit:cover}
.cart-item h4{font-size:14px;margin:2px 0 4px}
.cart-item .ci-price{font-size:13px;font-weight:800;color:#a63d59}
.qty{display:flex;align-items:center;gap:7px;margin-top:7px}
.qty button{width:25px;height:25px;border-radius:7px;border:1px solid #e4c9c7;background:#fff}
.qty span{min-width:16px;text-align:center;font-size:13px;font-weight:800}
.remove{border:0;background:none;color:#a63d59;font-size:12px;margin-top:5px}
.cart-foot{border-top:1px solid var(--line);padding:17px 20px;background:#fff}
.total{display:flex;justify-content:space-between;font-size:19px;font-weight:900;margin-bottom:13px}
.checkout{
  width:100%;border:0;background:var(--green);color:#fff;border-radius:14px;
  padding:14px;font-weight:900
}
.clear{width:100%;margin-top:8px;border:1px solid #e2c8c5;background:#fff;color:#76544b;border-radius:12px;padding:9px;font-weight:700}

/* FOOTER */
footer{background:#29120e;color:#ffeaeb;padding:34px 0}
.footer{display:flex;align-items:center;justify-content:space-between;gap:20px}
.footer-name{font:31px "Great Vibes",cursive}
.footer-small{font-size:12px;color:#d9babb}

@media(max-width:960px){
  .links{display:none}
  .hero-grid,.cta{grid-template-columns:1fr}
  .products{grid-template-columns:repeat(2,1fr)}
}
@media(max-width:620px){
  .topbar{font-size:10px}
  .nav-inner{min-height:68px}
  .brand img{width:43px;height:43px}
  .brand-name{font-size:25px}
  .order-btn{padding:9px 13px;font-size:12px}
  .hero{padding:55px 0}
  .hero h1{font-size:61px}
  .hero p{font-size:16px}
  .section{padding:60px 0}
  .section-title{font-size:40px}
  .products,.gallery{grid-template-columns:1fr}
  .product-photo{height:245px}
  .cta{padding:31px 22px}
  .cta h2{font-size:44px}
  .footer{align-items:flex-start;flex-direction:column}
  .stamp{width:88px;height:88px;font-size:14px;right:-8px}
}
</style>
</head>

<body>

<div class="topbar">
  ♡ Homemade with love &nbsp; • &nbsp; <strong>Orders & Enquiries: 93605 81292</strong> &nbsp; • &nbsp; @nisi_homebakes
</div>

<nav>
  <div class="container nav-inner">
    <a class="brand" href="#home">
      <img src="nisi-logo.jpg" alt="Nisi Home Bakes logo">
      <span class="brand-name">Nisi Home Bakes</span>
    </a>

    <div class="links">
      <a href="#cakes">Cakes</a>
      <a href="#bakes">Bakes</a>
      <a href="#prices">Price List</a>
      <a href="#gallery">Gallery</a>
      <a href="#order">Contact</a>
    </div>

    <div class="nav-actions">
      <button class="nav-cart" onclick="openCart()" aria-label="Open shopping cart">
        🛒 Cart <span class="cart-count" id="cartCount">0</span>
      </button>
      <a class="order-btn" href="https://wa.me/919360581292?text=Hi%20Nisi%20Home%20Bakes%2C%20I%20would%20like%20to%20place%20an%20order." target="_blank">Order</a>
    </div>
  </div>
</nav>

<header class="hero" id="home">
  <div class="container hero-grid">
    <div>
      <span class="eyebrow">♡ Fresh • Homemade • Specially For You</span>
      <h1>Sweet moments<span>made at home.</span></h1>
      <p>
        Welcome to <strong>Nisi Home Bakes</strong>. Discover homemade birthday
        cakes, tea cakes, banana cakes and brownies prepared for your celebrations
        and everyday sweet moments.
      </p>

      <div class="actions">
        <a class="btn btn-main" href="#cakes">Shop Our Cakes</a>
        <button class="btn btn-ghost" onclick="openCart()">View Cart 🛒</button>
      </div>

      <div class="badges">
        <span class="badge">Made with quality ingredients</span>
        <span class="badge">No preservatives added</span>
        <span class="badge">Best enjoyed fresh</span>
      </div>
    </div>

    <div class="hero-art">
      <img src="nisi-logo.jpg" alt="Nisi Home Bakes original bakery artwork">
      <div class="stamp">BAKED<br>WITH<br>LOVE ♡</div>
    </div>
  </div>
</header>

<section class="section" id="cakes">
  <div class="container">
    <div class="section-head">
      <div class="kicker">Birthday favourites</div>
      <h2 class="section-title">Cakes Made For Your Moments</h2>
      <p>Choose a flavour, add it to your cart and send your complete order to Nisi Home Bakes on WhatsApp.</p>
    </div>

    <div class="products">

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/10891145/pexels-photo-10891145.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="White Forest cake">
        </div>
        <div class="product-body">
          <h3>White Forest</h3>
          <p>Soft, creamy celebration cake.</p>
          <div class="product-bottom">
            <span class="product-price">₹700 / 1 kg</span>
            <button class="add" onclick="addToCart('White Forest',700,'https://images.pexels.com/photos/10891145/pexels-photo-10891145.jpeg?auto=compress&cs=tinysrgb&w=500')">+ Add</button>
          </div>
        </div>
      </article>

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/4600633/pexels-photo-4600633.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="Black Forest cake">
        </div>
        <div class="product-body">
          <h3>Black Forest</h3>
          <p>Chocolate favourite for celebrations.</p>
          <div class="product-bottom">
            <span class="product-price">₹800 / 1 kg</span>
            <button class="add" onclick="addToCart('Black Forest',800,'https://images.pexels.com/photos/4600633/pexels-photo-4600633.jpeg?auto=compress&cs=tinysrgb&w=500')">+ Add</button>
          </div>
        </div>
      </article>

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/6990073/pexels-photo-6990073.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="Strawberry cake">
        </div>
        <div class="product-body">
          <h3>Strawberry</h3>
          <p>Fruity and celebration ready.</p>
          <div class="product-bottom">
            <span class="product-price">₹900 / 1 kg</span>
            <button class="add" onclick="addToCart('Strawberry',900,'https://images.pexels.com/photos/6990073/pexels-photo-6990073.jpeg?auto=compress&cs=tinysrgb&w=500')">+ Add</button>
          </div>
        </div>
      </article>

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/19651099/pexels-photo-19651099.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="Custom birthday cake">
        </div>
        <div class="product-body">
          <h3>Custom Cake</h3>
          <p>Theme, message and design made to request.</p>
          <div class="product-bottom">
            <span class="product-price">On Request</span>
            <button class="add" onclick="customCake()">Enquire</button>
          </div>
        </div>
      </article>

    </div>
  </div>
</section>

<section class="section soft" id="bakes">
  <div class="container">
    <div class="section-head">
      <div class="kicker">Homemade goodness</div>
      <h2 class="section-title">Tea Cakes & Brownies</h2>
      <p>Fresh bakes for tea time, gifting and everyday cravings.</p>
    </div>

    <div class="products">

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/6803031/pexels-photo-6803031.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="Vanilla tea cake">
        </div>
        <div class="product-body">
          <h3>Vanilla Tea Cake</h3>
          <p>10 pieces per box.</p>
          <div class="product-bottom">
            <span class="product-price">₹120 / box</span>
            <button class="add" onclick="addToCart('Vanilla Tea Cake - 10 pcs',120,'https://images.pexels.com/photos/6803031/pexels-photo-6803031.jpeg?auto=compress&cs=tinysrgb&w=500')">+ Add</button>
          </div>
        </div>
      </article>

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/4114120/pexels-photo-4114120.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="Banana cake">
        </div>
        <div class="product-body">
          <h3>Banana Cake</h3>
          <p>10 pieces per box.</p>
          <div class="product-bottom">
            <span class="product-price">₹280 / box</span>
            <button class="add" onclick="addToCart('Banana Cake - 10 pcs',280,'https://images.pexels.com/photos/4114120/pexels-photo-4114120.jpeg?auto=compress&cs=tinysrgb&w=500')">+ Add</button>
          </div>
        </div>
      </article>

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/12917988/pexels-photo-12917988.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="Classic brownie">
        </div>
        <div class="product-body">
          <h3>Classic Brownie</h3>
          <p>Rich chocolate brownie, ½ kg.</p>
          <div class="product-bottom">
            <span class="product-price">₹500 / ½ kg</span>
            <button class="add" onclick="addToCart('Classic Brownie - ½ kg',500,'https://images.pexels.com/photos/12917988/pexels-photo-12917988.jpeg?auto=compress&cs=tinysrgb&w=500')">+ Add</button>
          </div>
        </div>
      </article>

      <article class="product">
        <div class="product-photo">
          <img src="https://images.pexels.com/photos/28159488/pexels-photo-28159488.jpeg?auto=compress&cs=tinysrgb&w=1000" alt="Ragi brownie">
        </div>
        <div class="product-body">
          <h3>Ragi Brownie</h3>
          <p>Homemade ragi brownie, ½ kg.</p>
          <div class="product-bottom">
            <span class="product-price">₹500 / ½ kg</span>
            <button class="add" onclick="addToCart('Ragi Brownie - ½ kg',500,'https://images.pexels.com/photos/28159488/pexels-photo-28159488.jpeg?auto=compress&cs=tinysrgb&w=500')">+ Add</button>
          </div>
        </div>
      </article>

    </div>
  </div>
</section>

<section class="section" id="prices">
  <div class="container">
    <div class="section-head">
      <div class="kicker">Our menu</div>
      <h2 class="section-title">Birthday Cake Price List</h2>
      <p>Prices based on the menu supplied by Nisi Home Bakes.</p>
    </div>

    <div class="price-wrap">
      <table>
        <thead><tr><th>Variety</th><th>½ KG</th><th>1 KG</th></tr></thead>
        <tbody>
          <tr><td>White Forest</td><td>₹400</td><td>₹700</td></tr>
          <tr><td>Black Forest</td><td>₹400</td><td>₹800</td></tr>
          <tr><td>Black Currant</td><td>₹450</td><td>₹900</td></tr>
          <tr><td>Strawberry</td><td>₹450</td><td>₹900</td></tr>
          <tr><td>Blueberry</td><td>₹450</td><td>₹900</td></tr>
          <tr><td>Pineapple</td><td>₹450</td><td>₹900</td></tr>
          <tr><td>Butterscotch</td><td>₹500</td><td>₹1,000</td></tr>
          <tr><td>Red Velvet</td><td>₹550</td><td>₹1,100</td></tr>
          <tr><td>Rosemilk</td><td>₹550</td><td>₹1,100</td></tr>
        </tbody>
      </table>
    </div>
    <div class="price-note"><strong>Custom Birthday Cakes:</strong> Custom designs are available at a price on request. Contact us with your theme, flavour, size and message.</div>
  </div>
</section>

<section class="section soft" id="gallery">
  <div class="container">
    <div class="section-head">
      <div class="kicker">Original menu artwork</div>
      <h2 class="section-title">Nisi Home Bakes Gallery</h2>
      <p>Your supplied logo, birthday price list and rate card are displayed here.</p>
    </div>
    <div class="gallery">
      <div class="gallery-card"><img src="nisi-logo.jpg" alt="Nisi Home Bakes logo"></div>
      <div class="gallery-card"><img src="nisi-birthday-price.jpg" alt="Nisi birthday cake price list"></div>
      <div class="gallery-card"><img src="nisi-rate-card.jpg" alt="Nisi Home Bakes rate card"></div>
    </div>
  </div>
</section>

<section class="section" id="order">
  <div class="container">
    <div class="cta">
      <div>
        <div class="kicker" style="color:#ffd7df">For orders & enquiries</div>
        <h2>Make your celebration sweeter.</h2>
        <p>Build your cart, review the total and send the complete order directly to Nisi Home Bakes through WhatsApp.</p>
        <div class="actions">
          <button class="btn btn-main" style="background:#fff;color:#b23f5c" onclick="openCart()">Open Shopping Cart</button>
          <a class="btn btn-ghost" style="background:transparent;color:#fff;border-color:rgba(255,255,255,.5)" href="tel:+919360581292">Call 93605 81292</a>
        </div>
      </div>
      <div class="contact-box">
        <div class="contact-row"><strong>📞 Phone</strong><br><a href="tel:+919360581292">93605 81292</a></div>
        <div class="contact-row"><strong>📸 Instagram</strong><br><a href="https://instagram.com/nisi_homebakes" target="_blank">@nisi_homebakes</a></div>
        <div class="contact-row"><strong>♡ Promise</strong><br>Baked with love, made for you.</div>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="container footer">
    <div>
      <div class="footer-name">Nisi Home Bakes</div>
      <div class="footer-small">Baked with love • Made for you</div>
    </div>
    <div class="footer-small">© <span id="year"></span> Nisi Home Bakes</div>
  </div>
</footer>

<!-- CART -->
<div class="cart-overlay" id="overlay" onclick="closeCart()"></div>

<aside class="cart" id="cartDrawer" aria-label="Shopping cart">
  <div class="cart-head">
    <h2>Your Cart</h2>
    <button class="close" onclick="closeCart()" aria-label="Close cart">×</button>
  </div>

  <div class="cart-items" id="cartItems"></div>

  <div class="cart-foot">
    <div class="total">
      <span>Total</span>
      <span id="cartTotal">₹0</span>
    </div>
    <button class="checkout" onclick="checkoutWhatsApp()">✓ Send Order on WhatsApp</button>
    <button class="clear" onclick="clearCart()">Clear Cart</button>
  </div>
</aside>

<script>
const CART_KEY = "nisiHomeBakesCart";
let cart = JSON.parse(localStorage.getItem(CART_KEY) || "[]");

function money(n){
  return "₹" + Number(n).toLocaleString("en-IN");
}

function saveCart(){
  localStorage.setItem(CART_KEY, JSON.stringify(cart));
  renderCart();
}

function addToCart(name, price, image){
  const item = cart.find(x => x.name === name && x.price === price);
  if(item) item.qty += 1;
  else cart.push({name, price, image, qty:1});
  saveCart();
  openCart();
}

function changeQty(index, amount){
  if(!cart[index]) return;
  cart[index].qty += amount;
  if(cart[index].qty <= 0) cart.splice(index,1);
  saveCart();
}

function removeItem(index){
  cart.splice(index,1);
  saveCart();
}

function clearCart(){
  cart = [];
  saveCart();
}

function renderCart(){
  const box = document.getElementById("cartItems");
  const count = cart.reduce((sum,item) => sum + item.qty, 0);
  const total = cart.reduce((sum,item) => sum + item.price * item.qty, 0);

  document.getElementById("cartCount").textContent = count;
  document.getElementById("cartTotal").textContent = money(total);

  if(!cart.length){
    box.innerHTML = '<div class="empty"><div style="font-size:42px">🧁</div><h3>Your cart is empty</h3><p>Add a cake or bake from our menu.</p></div>';
    return;
  }

  box.innerHTML = cart.map((item,index) => `
    <div class="cart-item">
      <img src="${item.image}" alt="">
      <div>
        <h4>${escapeHtml(item.name)}</h4>
        <div class="ci-price">${money(item.price)} each</div>
        <div class="qty">
          <button onclick="changeQty(${index},-1)">−</button>
          <span>${item.qty}</span>
          <button onclick="changeQty(${index},1)">+</button>
        </div>
      </div>
      <button class="remove" onclick="removeItem(${index})">Remove</button>
    </div>
  `).join("");
}

function escapeHtml(value){
  return String(value).replace(/[&<>"']/g, c => ({
    "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#039;"
  }[c]));
}

function openCart(){
  document.getElementById("cartDrawer").classList.add("open");
  document.getElementById("overlay").classList.add("open");
  document.body.classList.add("cart-open");
}

function closeCart(){
  document.getElementById("cartDrawer").classList.remove("open");
  document.getElementById("overlay").classList.remove("open");
  document.body.classList.remove("cart-open");
}

function customCake(){
  const text = "Hi Nisi Home Bakes, I would like to enquire about a custom birthday cake.";
  window.open("https://wa.me/919360581292?text=" + encodeURIComponent(text), "_blank");
}

function checkoutWhatsApp(){
  if(!cart.length){
    alert("Your cart is empty. Please add an item first.");
    return;
  }

  const lines = cart.map((item,i) =>
    `${i+1}. ${item.name} x ${item.qty} = ${money(item.price * item.qty)}`
  );

  const total = cart.reduce((sum,item) => sum + item.price * item.qty, 0);

  const message =
`Hi Nisi Home Bakes! ♡

I would like to place this order:

${lines.join("\n")}

Total: ${money(total)}

Please confirm availability and delivery/pickup details. Thank you!`;

  window.open("https://wa.me/919360581292?text=" + encodeURIComponent(message), "_blank");
}

document.getElementById("year").textContent = new Date().getFullYear();
renderCart();
</script>

</body>
</html>
