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
    <title>Dress Shop - Commercial Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header & Navigation Bar -->
    <header class="header">
        <div class="logo">Boutique Glam</div>
        <nav class="nav-links">
            <a href="#home">Home</a>
            <a href="#products">Products</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Discover the Latest Fashion Trends</h1>
            <p>Shop exclusive dresses designed with elegance and style.</p>
            <a href="#products" class="btn">Explore Collection</a>
        </div>
    </section>

    <!-- Product Section (Using Flexbox) -->
    <section id="products" class="products-section">
        <h2>Featured Dress Collection</h2>
        <div class="product-container">
            
            <!-- Product 1 -->
            <div class="product-card">
                <img src="images/Casual Denim Set.jpg" alt="Casual Denim Set" class="product-img">
                <h3>Casual Denim Set</h3>
                <p>$59.99</p>
                <button class="cart-btn">Add to Cart</button>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <img src="images/Classic Evening Gown.jpg" alt="Classic Evening Gown" class="product-img">
                <h3>Classic Evening Gown</h3>
                <p>$129.99</p>
                <button class="cart-btn">Add to Cart</button>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <img src="images/Floral Summer Dress.jpg" alt="Floral Summer Dress" class="product-img">
                <h3>Floral Summer Dress</h3>
                <p>$45.99</p>
                <button class="cart-btn">Add to Cart</button>
            </div>

        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="contact-info">
            <p><strong>Phone:</strong> +1 (555) 456-7890</p>
            <p><strong>Address:</strong> 123 Fashion Avenue, Style City</p>
        </div>
    </section>

    <!-- Footer with Name and Register Number -->
    <footer class="footer">
        <p>&copy; 2026 BRINDHA A R. All rights reserved.</p>
    </footer>

</body>
</html>
```
## CSS
```
/* Global Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #fcfcfc;
    color: #333;
    line-height: 1.6;
}

/* Header & Navigation Bar using Flexbox */
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #2c3e50;
    color: #fff;
    padding: 1rem 5%;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
}

.nav-links {
    display: flex;
    gap: 2rem;
}

.nav-links a {
    color: #fff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #3498db;
}

/* Hero Section */
.hero {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), #34495e;
    color: white;
    padding: 5rem 2rem;
}

.hero-content h1 {
    font-size: 2.8rem;
    margin-bottom: 1rem;
}

.hero-content p {
    font-size: 1.1rem;
    margin-bottom: 1.5rem;
}

.btn {
    background-color: #e74c3c;
    color: white;
    padding: 0.75rem 1.5rem;
    text-decoration: none;
    border-radius: 4px;
    font-weight: bold;
}

.btn:hover {
    background-color: #c0392b;
}

/* Products Section */
.products-section {
    padding: 4rem 5%;
    text-align: center;
}

.products-section h2 {
    font-size: 2.2rem;
    margin-bottom: 2.5rem;
    color: #2c3e50;
}

/* Flexbox Grid Container */
.product-container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap; /* Allows cards to wrap nicely side-by-side */
    gap: 2rem;
}

/* Individual Flexbox Card */
.product-card {
    background: white;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    width: 280px;
    padding: 1.5rem;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: transform 0.3s ease;
}

.product-card:hover {
    transform: translateY(-5px);
}

/* Product Image Styling */
.product-img {
    width: 100%;
    height: 280px;
    object-fit: cover; /* Crops images neatly without distorting aspect ratio */
    border-radius: 6px;
    margin-bottom: 1rem;
}

.product-card h3 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
}

.product-card p {
    color: #e74c3c;
    font-weight: bold;
    margin-bottom: 1rem;
}

.cart-btn {
    background-color: #2ecc71;
    color: white;
    border: none;
    padding: 0.6rem 1rem;
    border-radius: 4px;
    cursor: pointer;
    font-weight: bold;
    transition: background 0.3s ease;
}

.cart-btn:hover {
    background-color: #27ae60;
}

/* Contact Section */
.section {
    background-color: #ecf0f1;
    padding: 2.5rem;
    text-align: center;
}

/* Footer Section */
.footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #2c3e50;
    color: white;
    padding: 1.5rem;
    text-align: center;
}
```
## OUTPUT
<img width="1917" height="982" alt="image" src="https://github.com/user-attachments/assets/994aa1f5-9948-4e9b-9496-f5888cda8592" />
<img width="1917" height="998" alt="image" src="https://github.com/user-attachments/assets/1d551a38-b3d4-46af-8a83-158ed2b8f16f" />
<img width="1917" height="1017" alt="image" src="https://github.com/user-attachments/assets/52709692-7a7b-4e89-9627-969ddec6318d" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
