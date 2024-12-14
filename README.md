<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lolirine Online Pool Store</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: url('IMG_5658.jpeg') no-repeat center center fixed;
            background-size: cover;
        }

        header {
            background: url('path-to-banner-image.jpg') no-repeat center center;
            background-size: cover;
            height: 300px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.7);
            position: relative;
        }

        header img {
            position: absolute;
            top: 10px;
            left: 10px;
            height: 60px;
        }

        header h1 {
            font-size: 2.5rem;
            margin: 0;
        }

        nav {
            background-color: #ff4d4d;
            padding: 1rem;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: space-around;
            margin: 0;
            padding: 0;
        }

        nav ul li {
            margin: 0;
        }

        nav ul li a {
            text-decoration: none;
            color: white;
            font-weight: bold;
        }

        section {
            padding: 2rem;
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }

        .product {
            border: 1px solid #ddd;
            border-radius: 10px;
            overflow: hidden;
            width: 300px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s ease-in-out;
        }

        .product:hover {
            transform: scale(1.05);
        }

        .product img {
            width: 100%;
            height: auto;
        }

        .product-details {
            padding: 1rem;
            text-align: center;
        }

        .product-details h3 {
            margin: 0.5rem 0;
            font-size: 1.25rem;
            color: #333;
        }

        .product-details p {
            margin: 0.5rem 0;
            color: #666;
        }

        .product-details button {
            background-color: #007bff;
            border: none;
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
        }

        .product-details button:hover {
            background-color: #0056b3;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1rem;
        }

        footer p {
            margin: 0;
        }

        .contact-form {
            max-width: 500px;
            margin: 2rem auto;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            background-color: #f9f9f9;
        }

        .contact-form h2 {
            text-align: center;
            color: #333;
        }

        .contact-form label {
            display: block;
            margin-top: 1rem;
            color: #666;
        }

        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 0.5rem;
            margin-top: 0.5rem;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .contact-form button {
            background-color: #007bff;
            color: white;
            padding: 0.5rem 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 1rem;
            display: block;
            width: 100%;
        }

        .contact-form button:hover {
            background-color: #0056b3;
        }

        .sub-products {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin-top: 1rem;
        }

        .sub-product {
            border: 1px solid #ddd;
            border-radius: 10px;
            width: 200px;
            text-align: center;
            padding: 1rem;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .sub-product img {
            width: 100%;
            height: auto;
            margin-bottom: 0.5rem;
        }

        .sub-product h4 {
            margin: 0.5rem 0;
            color: #333;
            font-size: 1rem;
        }

        .sub-product p {
            color: #666;
        }

        .payment-methods {
            max-width: 600px;
            margin: 2rem auto;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            background-color: #f9f9f9;
            text-align: center;
        }

        .payment-methods h2 {
            color: #333;
            margin-bottom: 1rem;
        }

        .payment-methods a {
            display: inline-block;
            margin: 0.5rem;
            padding: 0.5rem 1rem;
            background-color: #007bff;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.2s ease-in-out;
        }

        .payment-methods a:hover {
            background-color: #0056b3;
        }
    .achievements-gallery {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            background-color: #f9f9f9;
            text-align: center;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin-top: 1rem;
        }

        .gallery-item {
            border: 1px solid #ddd;
            border-radius: 10px;
            overflow: hidden;
            width: 300px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .gallery-item img {
            width: 100%;
            height: auto;
        }

        .gallery-item p {
            margin: 0.5rem 0;
            color: #333;
            font-size: 1rem;
        }
</style>
</head>
<body>
    <script>
        console.log('Page is loading...');

        const translations = {
            en: {
                welcome: "Welcome to the Pool Store",
                aboutUs: "About Us",
                contact: "Contact",
                achievements: "Our Achievements",
                signup: "Sign Up",
                cart: "Your Cart",
                payment: "Choose Your Payment Method",
                shop: "Shop",
                home: "Home",
                submit: "Submit",
                name: "Name",
                email: "Email",
                password: "Password",
                message: "Message",
                addToCart: "Add to Cart",
                viewSubProducts: "View Sub-products"
            },
            fr: {
                welcome: "Bienvenue à la boutique de piscine",
                aboutUs: "À propos de nous",
                contact: "Contact",
                achievements: "Nos Réalisations",
                signup: "S'inscrire",
                cart: "Votre Panier",
                payment: "Choisissez votre méthode de paiement",
                shop: "Boutique",
                home: "Accueil",
                submit: "Envoyer",
                name: "Nom",
                email: "E-mail",
                password: "Mot de passe",
                message: "Message",
                addToCart: "Ajouter au panier",
                viewSubProducts: "Voir les sous-produits"
            },
            nl: {
                welcome: "Welkom bij de Zwembadwinkel",
                aboutUs: "Over ons",
                contact: "Contact",
                achievements: "Onze Realisaties",
                signup: "Inschrijven",
                cart: "Uw Winkelwagen",
                payment: "Kies uw betaalmethode",
                shop: "Winkel",
                home: "Home",
                submit: "Versturen",
                name: "Naam",
                email: "E-mail",
                password: "Wachtwoord",
                message: "Bericht",
                addToCart: "Toevoegen aan winkelwagen",
                viewSubProducts: "Bekijk subproducten"
            }
        };

        function setLanguage(lang) {
            document.querySelector('#welcome-message').innerText = translations[lang].welcome;
            document.querySelectorAll('[data-translate]').forEach(element => {
                const key = element.getAttribute('data-translate');
                element.innerText = translations[lang][key];
            });
        }

        let translations = {
            en: {
                welcome: "Welcome to the Pool Store",
                aboutUs: "About Us",
                contact: "Contact",
                achievements: "Our Achievements",
                cart: "Your Cart",
                payment: "Choose Your Payment Method",
            },
            fr: {
                welcome: "Bienvenue à la boutique de piscine",
                aboutUs: "À propos de nous",
                contact: "Contact",
                achievements: "Nos Réalisations",
                cart: "Votre Panier",
                payment: "Choisissez votre méthode de paiement",
            },
            nl: {
                welcome: "Welkom bij de Zwembadwinkel",
                aboutUs: "Over ons",
                contact: "Contact",
                achievements: "Onze Realisaties",
                cart: "Uw Winkelwagen",
                payment: "Kies uw betaalmethode",
            }
        };

        function setLanguage(lang) {
            document.getElementById('welcome-message').innerText = translations[lang].welcome;
            document.getElementById('about-us-title').innerText = translations[lang].aboutUs;
            document.getElementById('contact-title').innerText = translations[lang].contact;
            document.getElementById('achievements-title').innerText = translations[lang].achievements;
            document.getElementById('cart-title').innerText = translations[lang].cart;
            document.getElementById('payment-title').innerText = translations[lang].payment;
        } // Log when the page starts loading
    </script>
    <header>
        <div class="language-switcher">
            <a href="#" onclick="setLanguage('en')">English</a> |
            <a href="#" onclick="setLanguage('fr')">Français</a> |
            <a href="#" onclick="setLanguage('nl')">Nederlands</a>
        </div>
        <img src="logo.png" alt="Pool Store Logo">
        <h1>Welcome to the Pool Store</h1>
        <script>
            console.log('Header loaded successfully.'); // Confirm header is loaded
        </script>
    </header>
    
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Shop</a></li>
            <li><a href="#about-us">About Us</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <script>
            console.log('Navigation menu rendered.'); // Log when navigation menu is rendered
        </script>
    </nav>

    <section id="achievements">
        <div class="achievements-gallery">
            <h2>Our Achievements</h2>
            <p>Take a look at some of our proudest accomplishments. We ensure the best quality and customer satisfaction in every project we undertake.</p>
            <div class="gallery">
                <div class="gallery-item">
                    <img src="achievement1.jpg" alt="Achievement 1">
                    <p>Luxury Pool Installation</p>
                </div>
                <div class="gallery-item">
                    <img src="achievement2.jpg" alt="Achievement 2">
                    <p>Modern Pool Design</p>
                </div>
                <div class="gallery-item">
                    <img src="achievement3.jpg" alt="Achievement 3">
                    <p>Eco-Friendly Pool Solutions</p>
                </div>
                <!-- Add more gallery items as needed -->
            </div>
        </div>
    </section>

    <section id="signup">
        <div class="contact-form">
            <h2>Sign Up</h2>
            <form id="signup-form">
                <label for="signup-name">Name:</label>
                <input type="text" id="signup-name" name="name" placeholder="Your Name" required>

                <label for="signup-email">Email:</label>
                <input type="email" id="signup-email" name="email" placeholder="Your Email" required>

                <label for="signup-password">Password:</label>
                <input type="password" id="signup-password" name="password" placeholder="Your Password" required>

                <button type="submit">Sign Up</button>
            </form>
            <p id="signup-confirmation" style="display: none; color: green;">Thank you for signing up! You will receive a confirmation email shortly.</p>
        </div>
    </section>

    <section>
        <script>
            console.log('Product section starts rendering.'); // Log before products are rendered
        </script>
        <div class="product">
            <img src="water-treatment.jpg" alt="Water Treatment">
            <div class="product-details">
                <h3>Traitement Eau Piscine</h3>
                <p>Maintain crystal-clear and safe water with our treatment solutions.</p>
                <button onclick="location.href='#water-treatment-sub-products'">View Sub-products</button>
                <button onclick="addToCart('Traitement Eau Piscine')">Add to Cart</button>
            </div>
        </div>
        </script>
        <div class="product">
            <img src="heating-main.jpg" alt="Heating">
            <div class="product-details">
                <h3>Heating</h3>
                <p>Explore our range of efficient pool heating solutions.</p>
                <button onclick="location.href='#heating-sub-products'">View Sub-products</button>
                <button onclick="addToCart('Heating')">Add to Cart</button>
            </div>
        </div>
        </script>
        <div class="product">
            <img src="photo_category_Raccords_PVC_pression_piscine25_1.jpg" alt="Accessories">
            <div class="product-details">
                <h3>Accessories</h3>
                <p>Discover a wide range of pool accessories.</p>
                <button onclick="location.href='#accessories-sub-products'">View Sub-products</button>
                <button onclick="addToCart('Accessories')">Add to Cart</button>
            </div>
        </div>
        </script>
        <div class="product">
            <img src="5-person-spa-origin-spa-p-910-2.jpg" alt="Jacuzzi">
            <div class="product-details">
                <h3>Jacuzzi</h3>
                <p>Experience luxury with our high-end Jacuzzis.</p>
                <button onclick="location.href='#jacuzzi-sub-products'">View Sub-products</button>
            </div>
        </div>
        <div class="product">
            <img src="pool-product1.jpg" alt="Pool Pump">
            <div class="product-details">
                <h3>Pool Pump</h3>
                <p>High efficiency pool pump for crystal clear water.</p>
                <button onclick="location.href='#pool-pump-sub-products'">View Sub-products</button>
            </div>
        </div>

        <div class="product">
            <img src="pool-product2.jpg" alt="Pool Cleaner">
            <div class="product-details">
                <h3>Automatic Pool Cleaner</h3>
                <p>Keep your pool spotless effortlessly.</p>
                <button onclick="location.href='#pool-cleaner-sub-products'">View Sub-products</button>
            </div>
        </div>

        <div class="product">
            <img src="pool-product3.jpg" alt="Pool Filter">
            <div class="product-details">
                <h3>Pool Filter</h3>
                <p>Top quality filter for clean and safe swimming.</p>
                <button onclick="location.href='#pool-filter-sub-products'">View Sub-products</button>
            </div>
        </div>
        <script>
            console.log('Product section finished rendering.'); // Log after products are rendered
        </script>
    </section>

    <!-- Payment methods section -->
    <section class="payment-methods">
        <h2>Choose Your Payment Method</h2>
        <a href="https://www.bancontact.com/en/" target="_blank">Pay with Bancontact</a>
        <a href="https://www.paypal.com" target="_blank">Pay with PayPal</a>
        <a href="https://www.visa.com" target="_blank">Pay with Visa</a>
        <a href="https://www.mastercard.com" target="_blank">Pay with MasterCard</a>
        <a href="https://www.americanexpress.com" target="_blank">Pay with American Express</a>
    </section>

    <!-- Sub-product sections -->
    <section id="water-treatment-sub-products">
        <h2>Traitement Eau Piscine - Sub-products</h2>
        <div class="sub-products">
            <div class="sub-product">
                <img src="chlorine.jpg" alt="Chlorine">
                <h4>Chlorine Tablets</h4>
                <p>$49.99</p>
                <button onclick="addToCart('Chlorine Tablets')">Add to Cart</button>
            </div>
            <div class="sub-product">
                <img src="ph-regulator.jpg" alt="pH Regulator">
                <h4>pH Regulator</h4>
                <p>$29.99</p>
                <button onclick="addToCart('pH Regulator')">Add to Cart</button>
            </div>
            <div class="sub-product">
                <img src="algaecide.jpg" alt="Algaecide">
                <h4>Algaecide</h4>
                <p>$39.99</p>
                <button onclick="addToCart('Algaecide')">Add to Cart</button>
            </div>
        </div>
    </section>
    <section id="heating-sub-products">
        <h2>Heating - Sub-products</h2>
        <div class="sub-products">
            <div class="sub-product">
                <img src="heating-solar.jpg" alt="Solar Heating">
                <h4>Solar Heating System</h4>
                <p>$499.99</p>
                <button onclick="addToCart('Solar Heating System')">Add to Cart</button>
            </div>
            <div class="sub-product">
                <img src="heating-electric.jpg" alt="Electric Heating">
                <h4>Electric Heating System</h4>
                <p>$799.99</p>
                <button onclick="addToCart('Electric Heating System')">Add to Cart</button>
            </div>
            <div class="sub-product">
                <img src="heating-gas.jpg" alt="Gas Heating">
                <h4>Gas Heating System</h4>
                <p>$999.99</p>
                <button onclick="addToCart('Gas Heating System')">Add to Cart</button>
            </div>
        </div>
    </section>
    <section id="accessories-sub-products">
        <h2>Accessories - Sub-products</h2>
        <div class="sub-products">
            <div class="sub-product">
                <img src="accessory1.jpg" alt="Accessory Model 1">
                <h4>Accessory Model 1</h4>
                <p>$19.99</p>
                <button onclick="addToCart('Accessory Model 1')">Add to Cart</button>
            </div>
            <div class="sub-product">
                <img src="accessory2.jpg" alt="Accessory Model 2">
                <h4>Accessory Model 2</h4>
                <p>$29.99</p>
                <button onclick="addToCart('Accessory Model 2')">Add to Cart</button>
            </div>
            <div class="sub-product">
                <img src="accessory3.jpg" alt="Accessory Model 3">
                <h4>Accessory Model 3</h4>
                <p>$39.99</p>
                <button onclick="addToCart('Accessory Model 3')">Add to Cart</button>
            </div>
        </div>
    </section>
    <section id="jacuzzi-sub-products">
        <h2>Jacuzzi - Sub-products</h2>
        <div class="sub-products">
            <div class="sub-product">
                <img src="sub-jacuzzi1.jpg" alt="Jacuzzi Model 1">
                <h4>Jacuzzi Model 1</h4>
                <p>$4,999.99</p>
                <a href="https://www.paypal.com" target="_blank" class="payment-button">Buy Now</a>
            </div>
            <div class="sub-product">
                <img src="sub-jacuzzi2.jpg" alt="Jacuzzi Model 2">
                <h4>Jacuzzi Model 2</h4>
                <p>$6,499.99</p>
                <a href="https://www.paypal.com" target="_blank" class="payment-button">Buy Now</a>
            </div>
            <div class="sub-product">
                <img src="sub-jacuzzi3.jpg" alt="Jacuzzi Model 3">
                <h4>Jacuzzi Model 3</h4>
                <p>$8,999.99</p>
                <a href="https://www.paypal.com" target="_blank" class="payment-button">Buy Now</a>
            </div>
        </div>
    </section>
    <section id="pool-pump-sub-products">
        <h2>Pool Pump - Sub-products</h2>
        <div class="sub-products">
            <div class="sub-product">
                <img src="sub-pool-pump1.jpg" alt="Pump Model 1">
                <h4>Pump Model 1</h4>
                <p>$199.99</p>
            </div>
            <div class="sub-product">
                <img src="sub-pool-pump2.jpg" alt="Pump Model 2">
                <h4>Pump Model 2</h4>
                <p>$249.99</p>
            </div>
            <!-- Add more sub-products as needed -->
        </div>
    </section>

    <section id="pool-cleaner-sub-products">
        <h2>Automatic Pool Cleaner - Sub-products</h2>
        <div class="sub-products">
            <div class="sub-product">
                <img src="sub-pool-cleaner1.jpg" alt="Cleaner Model 1">
                <h4>Cleaner Model 1</h4>
                <p>$299.99</p>
            </div>
            <div class="sub-product">
                <img src="sub-pool-cleaner2.jpg" alt="Cleaner Model 2">
                <h4>Cleaner Model 2</h4>
                <p>$349.99</p>
            </div>
            <!-- Add more sub-products as needed -->
        </div>
    </section>

    <section id="pool-filter-sub-products">
        <h2>Pool Filter - Sub-products</h2>
        <div class="sub-products">
            <div class="sub-product">
                <img src="sub-pool-filter1.jpg" alt="Filter Model 1">
                <h4>Filter Model 1</h4>
                <p>$129.99</p>
            </div>
            <div class="sub-product">
                <img src="sub-pool-filter2.jpg" alt="Filter Model 2">
                <h4>Filter Model 2</h4>
                <p>$159.99</p>
            </div>
            <!-- Add more sub-products as needed -->
        </div>
    </section>

    <section id="about-us">
        <h2>About Us</h2>
        <p>Welcome to Piscine Lolirine, your trusted partner for all your pool needs. We take pride in offering top-quality products, fast and reliable delivery, competitive pricing, and exceptional after-sales service. Our mission is to make your pool experience seamless, enjoyable, and stress-free. Whether you need advanced pool equipment, cleaning solutions, or expert guidance, we are here to support you with professionalism and care.</p>
    </section>

    <section id="contact">
        <div class="contact-form">
            <h2>Contact Us</h2>
            <form>
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" placeholder="Your Name" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" placeholder="Your Email" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" placeholder="Your Message" rows="5" required></textarea>

                <button type="submit">Submit</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Pool Store. All rights reserved.</p>
        <script>
            console.log('Footer rendered successfully.'); // Confirm footer is rendered
        </script>
    </footer>
    <script>
        const signupForm = document.getElementById('signup-form');
        const signupConfirmation = document.getElementById('signup-confirmation');

        signupForm.addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent the default form submission

            // Mock email sending
            console.log('Sending confirmation email to:', document.getElementById('signup-email').value);

            // Show confirmation message
            signupConfirmation.style.display = 'block';

            // Clear the form
            signupForm.reset();
        });
    </script>
    <section id="cart">
        <h2>Your Cart</h2>
        <div id="cart-items">
            <p>Your cart is empty.</p>
        </div>
        <button onclick="checkout()" style="margin-top: 1rem; padding: 0.5rem 1rem; background-color: #007bff; color: white; border: none; border-radius: 5px; cursor: pointer;">Proceed to Checkout</button>
    </section>

    <script>
        let cart = [];

        function addToCart(product) {
            cart.push(product);
            displayCart();
        }

        function displayCart() {
            const cartItems = document.getElementById('cart-items');
            if (cart.length === 0) {
                cartItems.innerHTML = '<p>Your cart is empty.</p>';
            } else {
                cartItems.innerHTML = '<ul>' + cart.map(item => `<li>${item}</li>`).join('') + '</ul>';
            }
        }

        function checkout() {
            if (cart.length === 0) {
                alert('Your cart is empty. Add some products before proceeding to checkout.');
            } else {
                const paymentOptions = `
                    <div class="payment-options">
                        <h3>Select a Payment Method</h3>
                        <button onclick="redirectToPayment('https://www.bancontact.com/en/')">Pay with Bancontact</button>
                        <button onclick="redirectToPayment('https://www.paypal.com')">Pay with PayPal</button>
                        <button onclick="redirectToPayment('https://www.visa.com')">Pay with Visa</button>
                        <button onclick="redirectToPayment('https://www.mastercard.com')">Pay with MasterCard</button>
                        <button onclick="redirectToPayment('https://www.americanexpress.com')">Pay with American Express</button>
                    </div>
                `;
                const cartItems = document.getElementById('cart-items');
                cartItems.innerHTML = paymentOptions;
            }
        }

        function redirectToPayment(url) {
            alert('Redirecting to the selected payment platform...');
            window.location.href = url;
        } else {
                alert('Redirecting to payment gateway...');
                window.location.href = 'https://www.paypal.com';
            }
        }
    </script>
</body>
</html>
