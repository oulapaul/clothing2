<!DOCTYPE html>  
<html lang="en">  

<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Clothing Store</title>  
    <style>  
        body {  
            font-family: Arial, sans-serif;  
            margin: 0;  
            padding: 0;  
            background-color: #e0510e;  
        }  

        header {  
            background-color: #00ff4c;  
            color: rgb(218, 10, 10);  
            padding: 15px 20px;  
            text-align: center;  
        }  

        nav ul {  
            list-style-type: none;  
            padding: 0;  
        }  

        nav ul li {  
            display: inline;  
            margin: 0 15px;  
        }  

        nav ul li a {  
            color: rgb(16, 170, 221);  
            text-decoration: none;  
        }  

        main {  
            padding: 20px;  
        }  

        form {  
            background-color: rgb(163, 93, 13);  
            padding: 20px;  
            border-radius: 5px;  
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);  
            max-width: 400px;  
            margin: auto;  
        }  

        form label {  
            display: block;  
            margin-bottom: 5px;  
        }  

        form input,  
        form textarea {  
            width: 100%;  
            padding: 10px;  
            margin-bottom: 15px;  
        }  

        form button {  
            background-color: #007bff;  
            color: white;  
            border: none;  
            padding: 10px;  
            border-radius: 5px;  
            cursor: pointer;  
        }  

        form button:hover {  
            background-color: #0056b3;  
        }  

        footer {  
            text-align: center;  
            padding: 10px;  
            background-color: #007bff;  
            color: white;  
            position: relative;  
            bottom: 0;  
            width: 100%;  
            margin-top: 20px;  
        }  

        .category {  
            margin-bottom: 20px;  
        }  
    </style>  
    <script>  
        function showPage(page) {  
            document.querySelectorAll('.content').forEach(content => {  
                content.style.display = 'none';  
            });  
            document.getElementById(page).style.display = 'block';  
        }  

        document.addEventListener('DOMContentLoaded', () => {  
            showPage('home'); // Show home page by default  
        });  

        function handleSubmit(formId, alertMessage) {  
            document.getElementById(formId).onsubmit = function () {  
                alert(alertMessage);  
                return false; // Prevent actual form submission for demonstration  
            };  
        }  

        handleSubmit('contactForm', 'Message sent!');  
        handleSubmit('signInForm', 'Sign In functionality not implemented.');  
        handleSubmit('forgotPasswordForm', 'Password reset link sent!');  
    </script>  
</head>  

<body>  
    <header>  
        <h1>Clothing Store</h1>  
        <nav>  
            <ul>  
                <li><a href="#" onclick="showPage('home')">Home</a></li>  
                <li><a href="#" onclick="showPage('contact')">Contact</a></li>  
                <li><a href="#" onclick="showPage('menu')">Menu</a></li>  
                <li><a href="#" onclick="showPage('signIn')">Sign In</a></li>  
                <li><a href="#" onclick="showPage('forgotPassword')">Forgot Password</a></li>  
            </ul>  
        </nav>  
    </header>  

    <main>  
        <div id="home" class="content">  
            <h2>Welcome to Our Clothing Store!</h2>  
            <p>Discover the latest trends in fashion. Shop now!</p>  
        </div>  

        <div id="contact" class="content" style="display: none;">  
            <h2>Contact Us</h2>  
            <form id="contactForm">  
                <label for="name">Name:</label>  
                <input type="text" id="name" required>  
                <label for="email">Email:</label>  
                <input type="email" id="email" required>  
                <label for="message">Message:</label>  
                <textarea id="message" required></textarea>  
                <button type="submit">Send Message</button>  
            </form>  
        </div>  

        <div id="menu" class="content" style="display: none;">  
            <h2>Menu Dashboard</h2>  
            <div class="category">  
                <h3>Men's Clothing</h3>  
                <ul>  
                    <li>T-Shirts</li>  
                    <li>Jeans</li>  
                    <li>Shirts</li>  
                    <li>Jackets</li>  
                    <li>Shorts</li>  
                </ul>  
            </div>  
            <div class="category">  
                <h3>Women's Clothing</h3>  
                <ul>  
                    <li>Dresses</li>  
                    <li>Blouses</li>  
                    <li>Skirts</li>  
                    <li>Leggings</li>  
                    <li>Coats</li>  
                </ul>  
            </div>  
            <div class="category">  
                <h3>Accessories</h3>  
                <ul>  
                    <li>Bags</li>  
                    <li>Watches</li>  
                    <li>Belts</li>  
                    <li>Sunglasses</li>  
                    <li>Scarves</li>  
                </ul>  
            </div>  
            <div class="category">  
                <h3>Sale Items</h3>  
                <ul>  
                    <li>Discounted T-Shirts</li>  
                    <li>Clearance Jeans</li>  
                    <li>End of Season Dresses</li>  
                    <li>Seasonal Accessories</li>  
                    <li>Special Offer Coats</li>  
                </ul>  
            </div>  
        </div>  

        <div id="signIn" class="content" style="display: none;">  
            <h2>Sign In</h2>  
            <form id="signInForm">  
                <label for="loginEmail">Email:</label>  
                <input type="email" id="loginEmail" required>  
                <label for="loginPassword">Password:</label>  
                <input type="password" id="loginPassword" required>  
                <button type="submit">Sign In</button>  
            </form>  
        </div>  

        <div id="forgotPassword" class="content" style="display: none;">  
            <h2>Forgot Password</h2>  
            <form id="forgotPasswordForm">  
                <label for="resetEmail">Email:</label>  
                <input type="email" id="resetEmail" required>  
                <button type="submit">Reset Password</button>  
            </form>  
        </div>  
    </main>  

    <footer>  
        <p>© PAUL 2024 Clothing Store. All rights reserved.</p>  
    </footer>  
</body>  

</html>
