# Ex02 Commercial Website
## Date:

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ChicWardrobe - Online Dress Shopping</title>
    <style>
        /* Global Styles (Step 6) */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #fafafa;
            color: #333;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        /* Header & Navigation Bar (Step 3, 7 - Flexbox) */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: #ffffff;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            z-index: 1000;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #d63384;
            letter-spacing: 1px;
        }

        nav {
            display: flex;
            gap: 25px;
            align-items: center;
        }

        nav a {
            text-decoration: none;
            color: #555;
            font-weight: 600;
            transition: color 0.3s ease; /* Step 9 */
        }

        nav a:hover {
            color: #d63384; /* Step 9 */
        }

        .cart-link {
            background: #d63384;
            color: #fff !important;
            padding: 8px 16px;
            border-radius: 4px;
            transition: background 0.3s ease; /* Step 9 */
        }

        .cart-link:hover {
            background: #b02a6b; /* Step 9 */
        }

        /* Homepage / Hero Section (Step 4, 10) */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('https://picsum.photos/1920/1080?fashion') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding: 0 20px;
        }

        .hero-content h1 {
            font-size: 50px;
            margin-bottom: 15px;
            letter-spacing: 1px;
        }

        .hero-content p {
            font-size: 20px;
            margin-bottom: 25px;
            font-weight: 300;
        }

        /* General Sections (Step 7) */
        .section {
            padding: 100px 50px 80px;
            text-align: center;
        }

        .alt-bg {
            background-color: #f1f3f5;
        }

        .section h2 {
            font-size: 36px;
            margin-bottom: 15px;
            color: #222;
        }

        /* Products Grid Layout (Step 8 - Flexbox) */
        .card-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .card {
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            width: 280px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease; /* Step 9 */
        }

        .card:hover {
            transform: translateY(-8px); /* Step 9 */
            box-shadow: 0 10px 20px rgba(0,0,0,0.1); /* Step 9 */
        }

        .card img {
            width: 100%;
            height: 320px;
            object-fit: cover;
        }

        .card h3 {
            margin: 15px 0 5px;
            color: #333;
            font-size: 18px;
        }

        .price {
            color: #d63384;
            font-weight: bold;
            font-size: 16px;
            margin-bottom: 15px;
        }

        .card p {
            padding: 0 15px 15px;
            color: #666;
            font-size: 13px;
        }

        /* Buttons & Text */
        .btn {
            display: inline-block;
            background: #d63384;
            color: #fff;
            padding: 10px 25px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: background 0.3s ease; /* Step 9 */
        }

        .btn:hover {
            background: #b02a6b; /* Step 9 */
        }

        .buy-btn {
            width: 85%;
            margin-bottom: 20px;
            padding: 9px 0;
            font-size: 14px;
        }

        .about-text {
            max-width: 700px;
            margin: 0 auto;
            color: #555;
            font-size: 18px;
        }

        .contact-info {
            margin-top: 20px;
            font-size: 18px;
            color: #555;
        }

        /* Footer Section with Social Media Links (Step 5) */
        footer {
            background: #1a1a1a;
            color: #fff;
            text-align: center;
            padding: 40px 20px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }

        .social-links a {
            color: #aaa;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: #fff;
        }
    </style>
</head>
<body>

    <!-- Header & Navigation Bar (Step 3) -->
    <header>
        <div class="logo">ChicWardrobe</div>
        <nav>
            <a href="#home">Home</a>
            <a href="#products">Dresses</a>
            <a href="#about">About Us</a>
            <a href="#contact">Contact</a>
            <a href="#account" class="cart-link">Cart (0)</a>
        </nav>
    </header>

    <!-- Homepage Section (Step 4) -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Elevate Your Everyday Style</h1>
            <p>Explore the newest trends in apparel and designer outfits.</p>
            <a href="#products" class="btn">Shop Collection</a>
        </div>
    </section>

    <!-- Products / Services Section (Step 4, 10, 11) -->
    <section id="products" class="section">
        <h2>Trending Dresses</h2>
        <p>Discover our best-selling seasonal outfits crafted for comfort and elegance.</p>
        <div class="card-container">
            <div class="card">
                <img src="images/Floral Summer Dress.jpg" alt="Floral Summer Dress">
                <h3>Floral Summer Dress</h3>
                <div class="price">$45.00</div>
                <p>Lightweight fabric perfect for sunny days and weekend outings.</p>
                <button class="btn buy-btn">Add to Cart</button>
            </div>
            <div class="card">
                <img src="images/Classic Evening Gown.jpg" alt="Classic Evening Gown">
                <h3>Classic Evening Gown</h3>
                <div class="price">$89.00</div>
                <p>Elegant design tailored for formal events and special celebrations.</p>
                <button class="btn buy-btn">Add to Cart</button>
            </div>
            <div class="card">
                <img src="images/Casual Denim Set.jpg" alt="Casual Denim Outfit">
                <h3>Casual Denim Set</h3>
                <div class="price">$60.00</div>
                <p>Trendy, durable, and effortlessly stylish everyday wear.</p>
                <button class="btn buy-btn">Add to Cart</button>
            </div>
        </div>
    </section>

    <!-- About Us Section (Step 4) -->
    <section id="about" class="section alt-bg">
        <h2>About Us</h2>
        <p class="about-text">At ChicWardrobe, we believe fashion should empower confidence and express individuality. We curate high-end apparel blending sustainable materials with cutting-edge fashion trends.</p>
    </section>

    <!-- Contact Details Section (Step 4) -->
    <section id="contact" class="section">
        <h2>Contact Details</h2>
        <p>Have questions about sizes, shipping, or returns? Get in touch with us!</p>
        <div class="contact-info">
            <p><strong>Email:</strong> support@chicwardrobe.com</p>
            <p><strong>Phone:</strong> +1 (555) 456-7890</p>
            <p><strong>Address:</strong> 123 Fashion Avenue, Style City</p>
        </div>
    </section>

    <!-- User Account Section (Step 4) -->
    <section id="account" class="section alt-bg">
        <h2>User Account</h2>
        <p>Log in to track your orders, view wishlists, and manage shipping addresses.</p>
        <br>
        <button class="btn">Log In / Sign Up</button>
    </section>

    <!-- Footer with Social Media Links & Copyright (Step 5) -->
    <footer>
        <div class="social-links">
            <a href="#">Instagram</a>
            <a href="#">Facebook</a>
            <a href="#">Pinterest</a>
            <a href="#">Twitter</a>
        </div>
        <p>&copy; 2026 BRINDHA A R. All rights reserved.</p>
    </footer>

</body>
</html>
```
## OUTPUT
<img width="1917" height="982" alt="image" src="https://github.com/user-attachments/assets/994aa1f5-9948-4e9b-9496-f5888cda8592" />
<img width="1917" height="998" alt="image" src="https://github.com/user-attachments/assets/1d551a38-b3d4-46af-8a83-158ed2b8f16f" />
<img width="1917" height="1017" alt="image" src="https://github.com/user-attachments/assets/52709692-7a7b-4e89-9627-969ddec6318d" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
