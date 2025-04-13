<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Talayora | Authentic Italian Pizza</title>
    <style>
        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #fffaf0;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background-color: #ff6b6b;
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 32px;
            font-weight: bold;
            font-family: 'Brush Script MT', cursive;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            font-size: 18px;
            transition: all 0.3s ease;
        }

        .nav-links a:hover {
            color: #ffe66d;
            transform: translateY(-3px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), url('/api/placeholder/1200/600') center/cover no-repeat;
            height: 70vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
        }

        .hero h1 {
            font-size: 64px;
            margin-bottom: 20px;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.6);
            font-family: 'Playfair Display', serif;
        }

        .hero p {
            font-size: 24px;
            margin-bottom: 40px;
            max-width: 700px;
            text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.6);
        }

        .btn {
            display: inline-block;
            background-color: #4ecdc4;
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 18px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .btn:hover {
            background-color: #ff9f1c;
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }

        .btn-primary {
            background-color: #ff9f1c;
        }

        .btn-primary:hover {
            background-color: #f76f8e;
        }

        /* About Section */
        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
            color: #ff6b6b;
            font-size: 42px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: #ff9f1c;
            border-radius: 2px;
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }

        .about-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            color: #ff6b6b;
            font-size: 28px;
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 18px;
        }

        /* Menu Section */
        .menu-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .menu-card {
            background-color: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .menu-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .menu-img {
            height: 200px;
            overflow: hidden;
        }

        .menu-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .menu-card:hover .menu-img img {
            transform: scale(1.1);
        }

        .menu-info {
            padding: 20px;
        }

        .menu-title {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .menu-title h3 {
            font-size: 22px;
            color: #333;
        }

        .menu-price {
            font-size: 20px;
            font-weight: bold;
            color: #ff6b6b;
        }

        .menu-desc {
            color: #666;
            margin-bottom: 15px;
            font-size: 16px;
        }

        .add-to-cart {
            background-color: #4ecdc4;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .add-to-cart:hover {
            background-color: #ff9f1c;
        }

        /* Gallery Section */
        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }

        .gallery-item {
            height: 250px;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.6);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        /* Reservation Section */
        .reservation {
            background-color: #ff9f1c;
            text-align: center;
            padding: 100px 0;
            color: white;
        }

        .reservation h2 {
            color: white;
            margin-bottom: 30px;
        }

        /* Order Section */
        .order-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #333;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            transition: border-color 0.3s ease;
        }

        .form-control:focus {
            outline: none;
            border-color: #4ecdc4;
        }

        /* Footer Styles */
        footer {
            background-color: #333;
            color: white;
            padding: 60px 0 20px;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col {
            flex: 1;
            min-width: 250px;
        }

        .footer-col h3 {
            font-size: 22px;
            margin-bottom: 20px;
            color: #ff9f1c;
        }

        .footer-col p {
            margin-bottom: 10px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background-color: #4ecdc4;
            border-radius: 50%;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background-color: #ff9f1c;
            transform: translateY(-3px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background-color: white;
            padding: 40px;
            border-radius: 15px;
            max-width: 500px;
            width: 90%;
            position: relative;
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 24px;
            cursor: pointer;
            color: #ff6b6b;
        }

        .modal-title {
            text-align: center;
            color: #ff6b6b;
            margin-bottom: 30px;
        }

        /* Cart Styles */
        .cart-icon {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #ff6b6b;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            z-index: 100;
        }

        .cart-icon:hover {
            background-color: #ff9f1c;
            transform: scale(1.1);
        }

        .cart-count {
            position: absolute;
            top: -5px;
            right: -5px;
            background-color: #4ecdc4;
            width: 25px;
            height: 25px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 14px;
            font-weight: bold;
        }

        .cart-items {
            max-height: 300px;
            overflow-y: auto;
            margin-bottom: 20px;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }

        .cart-item-info {
            flex: 1;
        }

        .cart-item-title {
            font-weight: bold;
            color: #333;
        }

        .cart-item-price {
            color: #ff6b6b;
        }

        .cart-item-quantity {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .cart-quantity-btn {
            width: 25px;
            height: 25px;
            background-color: #eee;
            border: none;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            font-size: 18px;
            font-weight: bold;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 2px solid #eee;
        }

        /* Animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animate {
            animation: fadeIn 1s ease;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 20px;
            }
            
            .nav-links {
                flex-direction: column;
                gap: 15px;
                text-align: center;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .section-title {
                font-size: 32px;
            }
            
            .footer-content {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo">Talayora</div>
                <div class="nav-links">
                    <a href="#about">About Us</a>
                    <a href="#menu">Menu</a>
                    <a href="#gallery">Gallery</a>
                    <a href="#order">Order Now</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Welcome to Talayora</h1>
        <p>Authentic Italian pizza made with love in the heart of Italy</p>
        <a href="#reservation" class="btn btn-primary">Reserve a Table</a>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">Our Story</h2>
            <div class="about-content">
                <div class="about-img">
                    <img src="/api/placeholder/600/400" alt="Talayora Restaurant">
                </div>
                <div class="about-text">
                    <h3>A Taste of Italy</h3>
                    <p>Established in 2010, Talayora brings the authentic flavors of Italy to your plate. Our pizzas are crafted with traditional recipes passed down through generations, using only the freshest ingredients sourced locally.</p>
                    <p>Our wood-fired ovens create the perfect crust - crispy on the outside, soft on the inside - while our passionate chefs ensure each pizza is a masterpiece of flavor and texture.</p>
                    <a href="#menu" class="btn">Explore Our Menu</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="menu">
        <div class="container">
            <h2 class="section-title">Our Delicious Menu</h2>
            <div class="menu-container">
                <!-- Menu Item 1 -->
                <div class="menu-card">
                    <div class="menu-img">
                        <img src="/api/placeholder/400/300" alt="Margherita Pizza">
                    </div>
                    <div class="menu-info">
                        <div class="menu-title">
                            <h3>Pizza Margherita</h3>
                            <span class="menu-price">€12</span>
                        </div>
                        <p class="menu-desc">Classic tomato sauce, mozzarella, fresh basil, and extra virgin olive oil</p>
                        <button class="add-to-cart" data-name="Pizza Margherita" data-price="12">Add to Order</button>
                    </div>
                </div>
                
                <!-- Menu Item 2 -->
                <div class="menu-card">
                    <div class="menu-img">
                        <img src="/api/placeholder/400/300" alt="Diavola Pizza">
                    </div>
                    <div class="menu-info">
                        <div class="menu-title">
                            <h3>Pizza Diavola</h3>
                            <span class="menu-price">€14</span>
                        </div>
                        <p class="menu-desc">Spicy tomato sauce, mozzarella, spicy salami, and chili flakes</p>
                        <button class="add-to-cart" data-name="Pizza Diavola" data-price="14">Add to Order</button>
                    </div>
                </div>
                
                <!-- Menu Item 3 -->
                <div class="menu-card">
                    <div class="menu-img">
                        <img src="/api/placeholder/400/300" alt="Quattro Formaggi Pizza">
                    </div>
                    <div class="menu-info">
                        <div class="menu-title">
                            <h3>Quattro Formaggi</h3>
                            <span class="menu-price">€15</span>
                        </div>
                        <p class="menu-desc">Mozzarella, gorgonzola, parmesan, and fontina cheeses</p>
                        <button class="add-to-cart" data-name="Quattro Formaggi" data-price="15">Add to Order</button>
                    </div>
                </div>
                
                <!-- Menu Item 4 -->
                <div class="menu-card">
                    <div class="menu-img">
                        <img src="/api/placeholder/400/300" alt="Prosciutto Pizza">
                    </div>
                    <div class="menu-info">
                        <div class="menu-title">
                            <h3>Prosciutto e Rucola</h3>
                            <span class="menu-price">€16</span>
                        </div>
                        <p class="menu-desc">Tomato sauce, mozzarella, prosciutto, arugula, and parmesan shavings</p>
                        <button class="add-to-cart" data-name="Prosciutto e Rucola" data-price="16">Add to Order</button>
                    </div>
                </div>
                
                <!-- Menu Item 5 -->
                <div class="menu-card">
                    <div class="menu-img">
                        <img src="/api/placeholder/400/300" alt="Vegetariana Pizza">
                    </div>
                    <div class="menu-info">
                        <div class="menu-title">
                            <h3>Vegetariana</h3>
                            <span class="menu-price">€13</span>
                        </div>
                        <p class="menu-desc">Tomato sauce, mozzarella, grilled zucchini, eggplant, bell peppers, and mushrooms</p>
                        <button class="add-to-cart" data-name="Vegetariana" data-price="13">Add to Order</button>
                    </div>
                </div>
                
                <!-- Menu Item 6 -->
                <div class="menu-card">
                    <div class="menu-img">
                        <img src="/api/placeholder/400/300" alt="Capricciosa Pizza">
                    </div>
                    <div class="menu-info">
                        <div class="menu-title">
                            <h3>Capricciosa</h3>
                            <span class="menu-price">€15</span>
                        </div>
                        <p class="menu-desc">Tomato sauce, mozzarella, ham, mushrooms, artichokes, olives, and oregano</p>
                        <button class="add-to-cart" data-name="Capricciosa" data-price="15">Add to Order</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="gallery">
        <div class="container">
            <h2 class="section-title">Gallery</h2>
            <div class="gallery-container">
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Restaurant Interior">
                    <div class="gallery-overlay">Restaurant Interior</div>
                </div>
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Pizza Making">
                    <div class="gallery-overlay">Pizza Making</div>
                </div>
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Outdoor Seating">
                    <div class="gallery-overlay">Outdoor Seating</div>
                </div>
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Special Events">
                    <div class="gallery-overlay">Special Events</div>
                </div>
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Wood-fired Oven">
                    <div class="gallery-overlay">Wood-fired Oven</div>
                </div>
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Chef's Special">
                    <div class="gallery-overlay">Chef's Special</div>
                </div>
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Fresh Ingredients">
                    <div class="gallery-overlay">Fresh Ingredients</div>
                </div>
                <div class="gallery-item">
                    <img src="/api/placeholder/400/400" alt="Happy Customers">
                    <div class="gallery-overlay">Happy Customers</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reservation Section -->
    <section id="reservation" class="reservation">
        <div class="container">
            <h2 class="section-title">Make a Reservation</h2>
            <p>Book your table now and enjoy an authentic Italian dining experience</p>
            <button class="btn" id="reservationBtn">Reserve a Table</button>
        </div>
    </section>

    <!-- Order Section -->
    <section id="order" class="order">
        <div class="container">
            <h2 class="section-title">Order for Delivery</h2>
            <div class="order-form">
                <div class="form-group">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" class="form-control" placeholder="Enter your name">
                </div>
                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" class="form-control" placeholder="Enter your phone number">
                </div>
                <div class="form-group">
                    <label for="address">Delivery Address</label>
                    <textarea id="address" class="form-control" rows="3" placeholder="Enter your delivery address"></textarea>
                </div>
                <div class="form-group">
                    <label for="notes">Special Instructions</label>
                    <textarea id="notes" class="form-control" rows="2" placeholder="Any special instructions for your order"></textarea>
                </div>
                <button class="btn btn-primary" id="submitOrder">Place Order</button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-col">
                    <h3>Talayora</h3>
                    <p>Authentic Italian Pizza Restaurant</p>
                    <p>Bringing the true taste of Italy to your plate since 2010</p>
                </div>
                <div class="footer-col">
                    <h3>Contact Us</h3>
                    <p>123 Pizza Street, Rome, Italy</p>
                    <p>Phone: +39 123 456 7890</p>
                    <p>Email: info@talayora.com</p>
                </div>
                <div class="footer-col">
                    <h3>Opening Hours</h3>
                    <p>Monday - Friday: 12:00 - 22:00</p>
                    <p>Saturday & Sunday: 12:00 - 23:00</p>
                </div>
                <div class="footer-col">
                    <h3>Follow Us</h3>
                    <div class="social-links">
                        <a href="#" aria-label="Facebook">f</a>
                        <a href="#" aria-label="Instagram">i</a>
                        <a href="#" aria-label="Twitter">t</a>
                        <a href="#" aria-label="TripAdvisor">ta</a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Talayora. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Cart Icon -->
    <div class="cart-icon" id="cartIcon">
        🛒
        <span class="cart-count" id="cartCount">0</span>
    </div>

    <!-- Reservation Modal -->
    <div class="modal" id="reservationModal">
        <div class="modal-content">
            <span class="close-modal" id="closeReservation">&times;</span>
            <h3 class="modal-title">Reserve a Table</h3>
            <div class="form-group">
                <label for="reservationName">Name</label>
                <input type="text" id="reservationName" class="form-control" placeholder="Enter your name">
            </div>
            <div class="form-group">
                <label for="reservationPhone">Phone Number</label>
                <input type="tel" id="reservationPhone" class="form-control" placeholder="Enter your phone number">
            </div>
            <div class="form-group">
                <label for="reservationDate">Date</label>
                <input type="date" id="reservationDate" class="form-control">
            </div>
            <div class="form-group">
                <label for="reservationTime">Time</label>
                <input type="time" id="reservationTime" class="form-control">
            </div>
            <div class="form-group">
                <label for="reservationGuests">Number of Guests</label>
                <input type="number" id="reservationGuests" class="form-control" min="1" max="20" value="2">
            </div>
            <button class="btn btn-primary" id="confirmReservation">Confirm Reservation</button>
        </div>
    </div>

    <!-- Cart Modal -->
    <div class="modal" id="cartModal">
        <div class="modal-content">
            <span class="close-modal" id="closeCart">&times;</span>
            <h3 class="modal-title">Your Order</h3>
            <div class="cart-items" id="cartItems">
                <!-- Cart items will be added here dynamically -->
            </div>
            <div class="cart-total">
                <span>Total:</span>
                <span id="cartTotal">€0</span>
            </div>
            <button class="btn btn-primary" id="checkoutBtn">Proceed to Checkout</button>
        </div>
    </div>

    <!-- JavaScript -->
    <script>
        // DOM Elements
        const addToCartButtons = document.querySelectorAll('.add-to-cart');
        const cartIcon = document.getElementById('cartIcon');
        const cartModal = document.getElementById('cartModal');
        const cartItems = document.getElementById('cartItems');
        const cartTotal = document.getElementById('cartTotal');
        const cartCount = document.getElementById('cartCount');
        const closeCart = document.getElementById('closeCart');
        const checkoutBtn = document.getElementById('checkoutBtn');
        const reservationBtn = document.getElementById('reservationBtn');
        const reservationModal = document.getElementById('reservationModal');
