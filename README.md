index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Discover elegant necklaces, rings, earrings and bracelets at Flores Beauty Collection.">
  <title>Flores Beauty Collection | Timeless Elegance</title>
  <style>
    :root {
      --teal: #397f82;
      --teal-dark: #245b5e;
      --mint: #dceeed;
      --ink: #172426;
      --muted: #6f7a7b;
      --cream: #fbfaf7;
      --gold: #c8a86b;
      --white: #fff;
      --shadow: 0 14px 40px rgba(20, 45, 46, .10);
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body { margin: 0; color: var(--ink); background: var(--white); font-family: Arial, Helvetica, sans-serif; line-height: 1.6; }
    img { display: block; width: 100%; object-fit: cover; }
    a { color: inherit; text-decoration: none; }
    button, input { font: inherit; }
    .topbar { padding: 10px 5%; display: flex; justify-content: space-between; align-items: center; gap: 18px; background: #fff; }
    .brand { font-family: Georgia, 'Times New Roman', serif; font-size: 1.65rem; font-style: italic; letter-spacing: .03em; color: var(--teal-dark); }
    .top-note { font-size: .76rem; color: var(--muted); letter-spacing: .1em; text-transform: uppercase; }
    .cart { border: 1px solid #dbe5e4; padding: 8px 13px; border-radius: 30px; font-size: .86rem; white-space: nowrap; }
    .nav { background: var(--teal); color: white; display: flex; justify-content: center; align-items: center; gap: clamp(14px, 4vw, 42px); padding: 12px 5%; }
    .nav a { font-size: .78rem; letter-spacing: .08em; text-transform: uppercase; }
    .nav a:hover { color: #f0d9a7; }
    .menu-btn { display: none; background: transparent; border: 0; color: var(--teal-dark); font-size: 1.5rem; }
    .hero { min-height: 490px; display: grid; grid-template-columns: 1fr 1fr; background: #101416; color: white; overflow: hidden; }
    .hero-copy { padding: clamp(38px, 7vw, 100px) 8% clamp(38px, 7vw, 90px) max(8%, calc((100vw - 1160px)/2)); align-self: center; }
    .eyebrow { color: var(--gold); text-transform: uppercase; letter-spacing: .2em; font-size: .72rem; font-weight: bold; }
    h1, h2, h3, p { margin-top: 0; }
    h1 { font-family: Georgia, 'Times New Roman', serif; font-size: clamp(2.5rem, 5vw, 4.8rem); font-weight: 400; line-height: 1.06; margin: 14px 0 22px; }
    .hero-copy p { color: #d2d7d7; max-width: 440px; font-size: .98rem; }
    .hero-image { min-height: 420px; background: linear-gradient(90deg, #101416 0%, transparent 25%), url('https://images.unsplash.com/photo-1535632066927-ab7c9ab60908?auto=format&fit=crop&w=1200&q=85') center 38%/cover; }
    .btn { display: inline-block; border: 0; border-radius: 30px; padding: 12px 23px; background: var(--teal); color: white; text-transform: uppercase; letter-spacing: .08em; font-size: .74rem; cursor: pointer; transition: .2s ease; }
    .btn:hover { background: var(--teal-dark); transform: translateY(-2px); }
    .btn.light { background: white; color: var(--teal-dark); }
    .btn.light:hover { background: var(--mint); }
    section { padding: 76px 5%; }
    .container { max-width: 1160px; margin: auto; }
    .section-heading { text-align: center; margin-bottom: 35px; }
    .section-heading h2 { font-size: clamp(1.5rem, 3vw, 2.2rem); margin: 7px 0 8px; text-transform: uppercase; letter-spacing: .04em; }
    .section-heading p { color: var(--muted); margin-bottom: 0; }
    .products { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; }
    .product-card { background: white; border: 1px solid #edf0ee; padding: 10px 10px 18px; text-align: center; transition: .25s ease; }
    .product-card:hover { transform: translateY(-5px); box-shadow: var(--shadow); }
    .product-card img { aspect-ratio: 1 / .82; background: var(--mint); }
    .product-card h3 { font-size: .95rem; margin: 15px 0 5px; }
    .product-card p { color: var(--muted); font-size: .82rem; margin: 0 0 10px; }
    .price { color: var(--teal-dark); font-weight: bold; margin-bottom: 12px; }
    .mini-btn { border: 1px solid var(--teal); background: transparent; color: var(--teal-dark); padding: 8px 15px; border-radius: 25px; font-size: .72rem; cursor: pointer; }
    .mini-btn:hover { background: var(--teal); color: white; }
    .about { background: var(--cream); }
    .split { max-width: 1080px; margin: auto; display: grid; grid-template-columns: 1fr 1fr; gap: clamp(30px, 6vw, 75px); align-items: center; }
    .about-pictures { position: relative; padding: 0 36px 30px 0; }
    .about-pictures img:first-child { height: 420px; }
    .about-pictures img:last-child { position: absolute; width: 42%; height: 180px; right: 0; bottom: 0; border: 8px solid var(--cream); }
    .split h2 { font-size: clamp(1.6rem, 3vw, 2.3rem); line-height: 1.2; margin: 10px 0 20px; }
    .split p { color: var(--muted); }
    .best { background: linear-gradient(135deg, #2d7779, #83b8b3); color: white; }
    .best .section-heading p { color: #e0f0ee; }
    .best .eyebrow { color: #f4dca8; }
    .best-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 18px; }
    .best-card { background: white; color: var(--ink); padding: 8px; border-radius: 4px; }
    .best-card img { height: 235px; }
    .best-card h3 { font-size: .87rem; margin: 12px 8px 2px; }
    .best-card p { font-size: .78rem; color: var(--muted); margin: 0 8px 12px; }
    .why-image img { height: 420px; }
    .testimonials { background: #fafafa; }
    .quotes { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; max-width: 1000px; margin: auto; }
    .quote { background: white; border: 1px solid #e5eeee; border-left: 4px solid var(--teal); border-radius: 4px 24px 4px 24px; padding: 28px; box-shadow: 0 6px 24px rgba(0,0,0,.035); }
    .quote-top { display: flex; gap: 13px; align-items: center; margin-bottom: 15px; }
    .quote-top img { width: 52px; height: 52px; border-radius: 50%; }
    .quote h3 { font-size: .92rem; margin: 0; }
    .stars { color: #d2a944; letter-spacing: .12em; font-size: .8rem; }
    .quote p { color: var(--muted); font-size: .88rem; margin: 0; }
    .gallery-grid { display: grid; grid-template-columns: repeat(4, 1fr); grid-auto-rows: 150px; gap: 10px; }
    .gallery-grid img { height: 100%; border-radius: 3px; transition: .25s; }
    .gallery-grid img:hover { filter: brightness(.85); }
    .gallery-grid img:nth-child(1), .gallery-grid img:nth-child(5) { grid-row: span 2; }
    .gallery-grid img:nth-child(4) { grid-column: span 2; }
    .newsletter { padding: 58px 5%; text-align: center; color: white; background: linear-gradient(90deg, rgba(41,111,114,.93), rgba(41,111,114,.85)), url('https://images.unsplash.com/photo-1617038220319-276d3cfab638?auto=format&fit=crop&w=1500&q=80') center/cover; }
    .newsletter h2 { font-size: clamp(1.5rem, 3vw, 2.1rem); margin-bottom: 8px; }
    .newsletter p { color: #e4f1ef; }
    .newsletter form { max-width: 520px; margin: 22px auto 0; display: flex; }
    .newsletter input { flex: 1; min-width: 0; border: 0; padding: 14px 16px; border-radius: 4px 0 0 4px; }
    .newsletter button { border-radius: 0 4px 4px 0; background: #f4f2ed; color: var(--teal-dark); }
    #newsletter-message { margin-top: 12px; font-size: .9rem; }
    footer { background: #fbfaf7; padding: 48px 5% 20px; }
    .footer-grid { max-width: 1160px; margin: auto; display: grid; grid-template-columns: 1.4fr repeat(3, 1fr); gap: 35px; }
    footer h3 { text-transform: uppercase; font-size: .8rem; letter-spacing: .08em; margin-bottom: 15px; }
    footer p, footer a { color: var(--muted); font-size: .83rem; }
    footer a { display: block; margin: 7px 0; }
    footer a:hover { color: var(--teal); }
    .socials { display: flex; gap: 9px; margin-top: 16px; }
    .socials a { border: 1px solid #cddedd; width: 31px; height: 31px; border-radius: 50%; display: grid; place-items: center; margin: 0; }
    .copyright { max-width: 1160px; margin: 30px auto 0; padding-top: 17px; border-top: 1px solid #e4e7e3; text-align: center; color: #899191; font-size: .75rem; }
    @media (max-width: 800px) {
      .top-note { display: none; }
      .menu-btn { display: block; }
      .nav { display: none; flex-direction: column; gap: 16px; align-items: stretch; text-align: center; }
      .nav.open { display: flex; }
      .hero { grid-template-columns: 1fr; }
      .hero-copy { padding: 54px 7%; }
      .hero-image { min-height: 330px; background-image: url('https://images.unsplash.com/photo-1535632066927-ab7c9ab60908?auto=format&fit=crop&w=1000&q=85'); }
      .products, .best-grid { grid-template-columns: repeat(2, 1fr); }
      .split { grid-template-columns: 1fr; }
      .about-pictures img:first-child, .why-image img { height: 330px; }
      .quotes { grid-template-columns: 1fr; }
      .footer-grid { grid-template-columns: repeat(2, 1fr); }
    }
    @media (max-width: 480px) {
      section { padding: 54px 5%; }
      .brand { font-size: 1.35rem; }
      .products, .best-grid { gap: 10px; }
      .product-card { padding: 7px 7px 14px; }
      .best-card img { height: 175px; }
      .gallery-grid { grid-template-columns: repeat(2, 1fr); grid-auto-rows: 125px; }
      .gallery-grid img:nth-child(4) { grid-column: span 1; }
      .newsletter form { flex-direction: column; gap: 8px; }
      .newsletter input, .newsletter button { border-radius: 4px; width: 100%; }
      .footer-grid { gap: 24px 16px; }
    }
  </style>
</head>
<body>
  <header>
    <div class="topbar">
      <button class="menu-btn" id="menu-toggle" aria-label="Toggle navigation" aria-expanded="false">☰</button>
      <a class="brand" href="#home">Flores Beauty Collection</a>
      <span class="top-note">Timeless pieces. Lasting memories.</span>
      <a class="cart" href="#products" aria-label="Shopping cart">♡ Bag <span id="cart-count">0</span></a>
    </div>
    <nav class="nav" id="main-nav" aria-label="Main navigation">
      <a href="#home">Home</a><a href="#products">Collections</a><a href="#about">Our Story</a>
      <a href="#bestsellers">Best Sellers</a><a href="#gallery">Gallery</a><a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <section class="hero" id="home" style="padding:0">
      <div class="hero-copy">
        <span class="eyebrow">Made to make you shine</span>
        <h1>Jewelry that tells your story.</h1>
        <p>Discover thoughtfully selected pieces made for your everyday moments, special celebrations, and everything in between.</p>
        <a class="btn light" href="#products">Explore collection</a>
      </div>
      <div class="hero-image" role="img" aria-label="Elegant jewelry and fashion portrait"></div>
    </section>

    <section id="products">
      <div class="container">
        <div class="section-heading"><span class="eyebrow">Find your signature piece</span><h2>Our Collections</h2><p>Little details. Beautiful differences.</p></div>
        <div class="products">
          <article class="product-card"><img loading="lazy" src="https://images.unsplash.com/photo-1611652022419-a9419f74343d?auto=format&fit=crop&w=700&q=80" alt="Gold earrings"><h3>Classic Earrings</h3><p>Elegant accents for every day</p><div class="price">₦18,500</div><button class="mini-btn add-cart">Add to bag</button></article>
          <article class="product-card"><img loading="lazy" src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?auto=format&fit=crop&w=700&q=80" alt="Diamond ring"><h3>Brilliant Rings</h3><p>Made for meaningful moments</p><div class="price">₦35,000</div><button class="mini-btn add-cart">Add to bag</button></article>
          <article class="product-card"><img loading="lazy" src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?auto=format&fit=crop&w=700&q=80" alt="Layered necklace"><h3>Fine Necklaces</h3><p>Subtle shine, timeless style</p><div class="price">₦22,000</div><button class="mini-btn add-cart">Add to bag</button></article>
          <article class="product-card"><img loading="lazy" src="https://images.unsplash.com/photo-1611591437281-460bfbe1220a?auto=format&fit=crop&w=700&q=80" alt="Gold bracelet"><h3>Modern Bracelets</h3><p>A finishing touch you'll love</p><div class="price">₦16,000</div><button class="mini-btn add-cart">Add to bag</button></article>
        </div>
      </div>
    </section>

    <section class="about" id="about">
      <div class="split">
        <div class="about-pictures">
          <img loading="lazy" src="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?auto=format&fit=crop&w=1000&q=85" alt="Fine jewelry arranged on a display">
          <img loading="lazy" src="https://images.unsplash.com/photo-1603561591411-07134e71a2a9?auto=format&fit=crop&w=600&q=80" alt="Close-up of a ring">
        </div>
        <div><span class="eyebrow">A little about us</span><h2>About Flores Beauty Collection</h2><p>At Flores Beauty Collection, we believe the right piece of jewelry can hold a memory, express your personality, and make an ordinary day feel special.</p><p>Our collection brings together graceful designs, thoughtful details, and versatile pieces you can treasure for years. Whether you're choosing a gift or treating yourself, we're here to help you find something meaningful.</p><a class="btn" href="#contact">Get to know us</a></div>
      </div>
    </section>

    <section class="best" id="bestsellers">
      <div class="container">
        <div class="section-heading"><span class="eyebrow">Loved by our customers</span><h2>Best Sellers</h2><p>Customer favourites with timeless appeal.</p></div>
        <div class="best-grid">
          <article class="best-card"><img loading="lazy" src="https://images.unsplash.com/photo-1617038220319-276d3cfab638?auto=format&fit=crop&w=700&q=80" alt="Statement pendant necklace"><h3>Golden Pendant</h3><p>Everyday elegance</p></article>
          <article class="best-card"><img loading="lazy" src="https://images.unsplash.com/photo-1611652022419-a9419f74343d?auto=format&fit=crop&w=700&q=80" alt="Elegant earrings"><h3>Golden Glow Hoops</h3><p>Bold but beautiful</p></article>
          <article class="best-card"><img loading="lazy" src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?auto=format&fit=crop&w=700&q=80" alt="Sparkling ring"><h3>Forever Ring</h3><p>For your special moments</p></article>
          <article class="best-card"><img loading="lazy" src="https://images.unsplash.com/photo-1611591437281-460bfbe1220a?auto=format&fit=crop&w=700&q=80" alt="Stacked bracelets"><h3>Classic Bracelet</h3><p>Simple, polished, versatile</p></article>
        </div>
      </div>
    </section>

    <section>
      <div class="split">
        <div><span class="eyebrow">The Chilso difference</span><h2>Why Choose Us</h2><p><strong>Thoughtful style.</strong> Pieces selected to complement your personal style, from understated classics to statement designs.</p><p><strong>Gifts with meaning.</strong> Find something special for birthdays, anniversaries, celebrations, and everyday surprises.</p><p><strong>A personal touch.</strong> We want choosing jewelry to feel easy, enjoyable, and memorable.</p><a class="btn" href="#products">Find your piece</a></div>
        <div class="why-image"><img loading="lazy" src="https://images.unsplash.com/photo-1599459183200-59c7687a0276?auto=format&fit=crop&w=1000&q=85" alt="Pendant necklace worn elegantly"></div>
      </div>
    </section>

    <section class="testimonials">
      <div class="container"><div class="section-heading"><span class="eyebrow">Kind words</span><h2>Client Testimonials</h2><p>What customers might say about their Flores Beauty Collection experience.</p></div>
        <div class="quotes">
          <article class="quote"><div class="quote-top"><img loading="lazy" src="flores-profile.jpg" alt="Joseph profile photo"><div><h3>Joseph</h3><div class="stars">★★★★★</div></div></div><p>“The piece is beautiful and easy to style. It feels special without being too much. I would happily shop here again.”</p></article>
          <article class="quote"><div class="quote-top"><img loading="lazy" src="flores-profile.jpg" alt="Mr Edet profile photo"><div><h3>Mr Edet</h3><div class="stars">★★★★★</div></div></div><p>“I found a lovely gift and the design was exactly the elegant look I wanted. A great addition to my jewellery collection.”</p></article>
        </div>
      </div>
    </section>

    <section id="gallery">
      <div class="container"><div class="section-heading"><span class="eyebrow">A closer look</span><h2>Gallery</h2><p>Jewelry inspiration for every occasion.</p></div>
        <div class="gallery-grid">
          <img loading="lazy" src="https://images.unsplash.com/photo-1535632066927-ab7c9ab60908?auto=format&fit=crop&w=700&q=80" alt="Model wearing statement earrings">
          <img loading="lazy" src="https://images.unsplash.com/photo-1617038220319-276d3cfab638?auto=format&fit=crop&w=700&q=80" alt="Gold jewelry close-up">
          <img loading="lazy" src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?auto=format&fit=crop&w=700&q=80" alt="Layered necklace">
          <img loading="lazy" src="https://images.unsplash.com/photo-1611652022419-a9419f74343d?auto=format&fit=crop&w=700&q=80" alt="Gold earrings on display">
          <img loading="lazy" src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?auto=format&fit=crop&w=700&q=80" alt="Engagement ring">
          <img loading="lazy" src="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?auto=format&fit=crop&w=700&q=80" alt="Jewelry collection">
          <img loading="lazy" src="https://images.unsplash.com/photo-1611591437281-460bfbe1220a?auto=format&fit=crop&w=700&q=80" alt="Bracelet details">
        </div>
      </div>
    </section>

    <section class="newsletter">
      <div class="container"><span class="eyebrow">Stay in the loop</span><h2>Join Our Newsletter</h2><p>Get new collection updates, styling inspiration, and special offers.</p>
        <form id="newsletter-form"><input id="email" type="email" placeholder="Enter your email address" aria-label="Email address" required><button class="btn" type="submit">Subscribe</button></form><div id="newsletter-message" aria-live="polite"></div>
      </div>
    </section>
  </main>

  <footer id="contact">
    <div class="footer-grid">
      <div><a class="brand" href="#home">Flores Beauty Collection</a><p>Timeless pieces for your most meaningful moments.</p><div class="socials"><a href="https://www.instagram.com/" aria-label="Instagram">ig</a><a href="https://www.facebook.com/" aria-label="Facebook">f</a><a href="https://www.pinterest.com/" aria-label="Pinterest">p</a></div></div>
      <div><h3>Quick Links</h3><a href="#home">Home</a><a href="#products">Collections</a><a href="#about">Our Story</a><a href="#gallery">Gallery</a></div>
      <div><h3>Information</h3><a href="#contact">Shipping & Delivery</a><a href="#contact">Returns</a><a href="#contact">Care Guide</a><a href="#contact">FAQs</a></div>
      <div><h3>Contact Us</h3><p>Email: hello@floresbeautycollection.com</p><p>Phone: +234 800 000 0000</p><p>Hours: Mon–Sat, 9am–6pm</p></div>
    </div>
    <div class="copyright">© <span id="year"></span> Flores Beauty Collection. Demo website — replace sample contact details, prices, and reviews before publishing.</div>
  </footer>

  <script>
    const menuToggle = document.getElementById('menu-toggle');
    const nav = document.getElementById('main-nav');
    menuToggle.addEventListener('click', () => {
      const isOpen = nav.classList.toggle('open');
      menuToggle.setAttribute('aria-expanded', String(isOpen));
    });
    nav.querySelectorAll('a').forEach(link => link.addEventListener('click', () => {
      nav.classList.remove('open');
      menuToggle.setAttribute('aria-expanded', 'false');
    }));

    let cartCount = 0;
    document.querySelectorAll('.add-cart').forEach(button => {
      button.addEventListener('click', () => {
        cartCount += 1;
        document.getElementById('cart-count').textContent = cartCount;
        button.textContent = 'Added ✓';
        setTimeout(() => button.textContent = 'Add to bag', 1200);
      });
    });

    document.getElementById('newsletter-form').addEventListener('submit', event => {
      event.preventDefault();
      const email = document.getElementById('email').value.trim();
      document.getElementById('newsletter-message').textContent =
        `Thanks! ${email} has been added to this demo signup form. Connect a mailing-list service to collect subscriptions.`;
      event.target.reset();
    });
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
