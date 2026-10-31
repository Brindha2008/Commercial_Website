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
    <title>Commercial Website - BRINDHA A R</title>
    <style>
        /* Global Styles (Step 6) */
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
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            z-index: 1000;
        }

        .logo {
            font-size: 20px;
            font-weight: bold;
            color: #007bff;
        }

        nav {
            display: flex;
            gap: 20px;
            align-items: center;
        }

        nav a {
            text-decoration: none;
            color: #555;
            font-weight: 600;
            transition: color 0.3s ease; /* Step 9 */
        }

        nav a:hover {
            color: #007bff; /* Step 9 */
        }

        .account-link {
            background: #007bff;
            color: #fff !important;
            padding: 8px 15px;
            border-radius: 4px;
            transition: background 0.3s ease; /* Step 9 */
        }

        .account-link:hover {
            background: #0056b3; /* Step 9 */
        }

        /* Homepage / Hero Section (Step 4, 10) */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://picsum.photos/1920/1080') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding: 0 20px;
        }

        .profile-img {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #fff;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            margin-bottom: 20px;
        }

        .hero-content h1 {
            font-size: 42px;
            margin-bottom: 10px;
        }

        .hero-content p {
            font-size: 18px;
            margin-bottom: 25px;
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
            margin-bottom: 20px;
            color: #222;
        }

        /* Products / Services Cards Layout (Step 8 - Flexbox) */
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
            width: 300px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease; /* Step 9 */
        }

        .card:hover {
            transform: translateY(-8px); /* Step 9 */
            box-shadow: 0 10px 15px rgba(0,0,0,0.1); /* Step 9 */
        }

        .card img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .card h3 {
            margin: 15px 0 10px;
            color: #333;
        }

        .card p {
            padding: 0 15px 20px;
            color: #666;
            font-size: 14px;
        }

        /* Buttons & Text */
        .btn {
            display: inline-block;
            background: #007bff;
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
            background: #0056b3; /* Step 9 */
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
            background: #222;
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
            color: #bbb;
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
        <div class="logo">BRINDHA A R</div>
        <nav>
            <a href="#home">Home</a>
            <a href="#services">Products / Services</a>
            <a href="#about">About Us</a>
            <a href="#contact">Contact</a>
            <a href="#account" class="account-link">User Account</a>
        </nav>
    </header>

    <!-- Homepage Section (Step 4) -->
    <section id="home" class="hero">
        <img src="images/profile.jpg" alt="BRINDHA A R" class="profile-img">
        <div class="hero-content">
            <h1>Welcome to Our Commercial Platform</h1>
            <p>Providing professional business solutions and services.</p>
            <a href="#services" class="btn">Explore Now</a>
        </div>
    </section>

    <!-- Products / Services Section (Step 4, 10, 11) -->
    <section id="services" class="section">
        <h2>Products / Services</h2>
        <div class="card-container">
            <div class="card">
                <img src="https://picsum.photos/300/180?random=1" alt="Service 1">
                <h3>Service One</h3>
                <p>High-quality digital solutions customized for your business success.</p>
            </div>
            <div class="card">
                <img src="https://picsum.photos/300/180?random=2" alt="Service 2">
                <h3>Service Two</h3>
                <p>Reliable infrastructure, consulting, and modern tool support.</p>
            </div>
            <div class="card">
                <img src="https://picsum.photos/300/180?random=3" alt="Service 3">
                <h3>Service Three</h3>
                <p>Dedicated customer service strategies tailored to scale growth.</p>
            </div>
        </div>
    </section>

    <!-- About Us Section (Step 4) -->
    <section id="about" class="section alt-bg">
        <h2>About Us</h2>
        <p class="about-text">We are an enterprise committed to delivering excellence, high performance, and innovative solutions for our clients worldwide.</p>
    </section>

    <!-- Contact Details Section (Step 4) -->
    <section id="contact" class="section">
        <h2>Contact Details</h2>
        <p>Get in touch with our team for business inquiries and partnerships.</p>
        <div class="contact-info">
            <p><strong>Email:</strong> contact@commercialwebsite.com</p>
            <p><strong>Phone:</strong> +1 (555) 321-7654</p>
            <p><strong>Address:</strong> 456 Enterprise Ave, Business District</p>
        </div>
    </section>

    <!-- User Account Section (Step 4) -->
    <section id="account" class="section alt-bg">
        <h2>User Account</h2>
        <p>Access your client portal, review active subscriptions, and update settings.</p>
        <br>
        <button class="btn">Log In / Sign Up</button>
    </section>

    <!-- Footer with Social Media Links & Copyright (Step 5) -->
    <footer>
        <div class="social-links">
            <a href="#">Facebook</a>
            <a href="#">Twitter</a>
            <a href="#">LinkedIn</a>
            <a href="#">Instagram</a>
        </div>
        <p>&copy; 2026 BRINDHA A R. All rights reserved.</p>
    </footer>

</body>
</html>
```

## OUTPUT
<img width="1917" height="1011" alt="image" src="https://github.com/user-attachments/assets/04efa478-e0a9-47a6-9e35-a85cbdf2d15f" />
<img width="1916" height="952" alt="image" src="https://github.com/user-attachments/assets/3d1c0272-cc25-4ed9-8059-1cf90d8e67da" />

<img width="1917" height="907" alt="image" src="https://github.com/user-attachments/assets/571452e7-044b-4b51-90bf-e6dacbbb8609" />

## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
