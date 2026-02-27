<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>Pretty Lashes by Diamond</title>
    <style>
        /* --- GLOBAL STYLES & RESET --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: black;
            overflow-x: hidden; /* Prevent horizontal scroll on mobile */
        }

        /* --- BETTER CURSIVE FONT STACK --- */
        .cursive-font {
            font-family: 'Playfair Display', 'Times New Roman', serif;
            font-style: italic;
            font-weight: 700;
            letter-spacing: 0.02em;
        }

        /* Apply to all cursive elements */
        .brand-title, .book-now-btn, .booking-title, .form-group label, 
        .submit-btn, .page-links a, footer, .cursive-text {
            font-family: 'Playfair Display', 'Georgia', 'Times New Roman', serif;
            font-style: italic;
            font-weight: 700;
        }

        /* Import Playfair Display for better cursive look */
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,700&display=swap');

        /* --- LAYOUT: IMAGES TOUCH CORNERS/SIDES & STACK --- */
        .full-width-image {
            display: block;
            width: 100%;
            height: auto;
            vertical-align: bottom;
            margin: 0;
            padding: 0;
            border: none;
        }

        .image-section {
            line-height: 0;
            font-size: 0;
            margin: 0;
            padding: 0;
            width: 100%;
        }

        /* --- HERO SECTION WITH OVERLAY --- */
        .hero-container {
            position: relative;
            width: 100%;
            line-height: 0;
        }

        .hero-image {
            display: block;
            width: 100%;
            height: auto;
            min-height: 300px; /* Better mobile display */
            object-fit: cover;
        }

        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.35);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            line-height: 1.3;
            padding: 15px;
        }

        /* --- HOT PINK WITH WHITE OUTLINE & NEON GLOW - MOBILE OPTIMIZED --- */
        .brand-title {
            font-size: clamp(2.2rem, 10vw, 7rem);
            color: #FF69B4;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white,
                0 0 15px #FF69B4,
                0 0 30px #FF69B4,
                0 0 45px #FF69B4;
            font-weight: 800;
            margin-bottom: 20px;
            letter-spacing: 2px;
            background-color: rgba(0, 0, 0, 0.25);
            padding: 10px 25px;
            border-radius: 60px;
            border: 3px solid #FF69B4;
            box-shadow: 0 0 40px #FF69B4, inset 0 0 15px #FF69B4;
            max-width: 95%;
            word-break: break-word;
        }

        .book-now-btn {
            display: inline-block;
            background-color: black;
            color: #FF69B4;
            font-size: clamp(1.5rem, 6vw, 3.5rem);
            font-weight: 800;
            text-decoration: none;
            padding: 15px 40px;
            border: 4px solid #FF69B4;
            border-radius: 60px;
            box-shadow: 
                0 0 25px #FF69B4,
                0 0 50px #FF69B4,
                inset 0 0 12px #FF69B4;
            transition: all 0.3s ease;
            letter-spacing: 2px;
            line-height: 1.2;
            text-transform: uppercase;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white;
            white-space: nowrap;
        }

        /* Mobile adjustment for button */
        @media (max-width: 480px) {
            .book-now-btn {
                padding: 12px 30px;
                white-space: normal;
                font-size: 1.8rem;
            }
            
            .brand-title {
                padding: 8px 20px;
                font-size: 2.5rem;
            }
        }

        .book-now-btn:hover {
            background-color: #FF69B4;
            color: black;
            border-color: white;
            box-shadow: 0 0 40px #FF69B4, 0 0 70px #FF69B4, inset 0 0 25px black;
            transform: scale(1.03);
            text-shadow: none;
        }

        /* --- BOOKING PAGE STYLES - MOBILE FRIENDLY --- */
        .booking-page {
            background-color: black;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px 15px;
            font-family: sans-serif;
            border-top: 12px solid #FF69B4;
            border-bottom: 12px solid #FF69B4;
            position: relative;
        }

        .booking-container {
            max-width: 900px;
            width: 100%;
            background-color: #0a0a0a;
            border: 6px solid #FF69B4;
            border-radius: 40px;
            padding: 40px 30px;
            box-shadow: 
                0 0 60px #FF69B4,
                inset 0 0 25px rgba(255, 105, 180, 0.5);
        }

        /* Tablet adjustments */
        @media (min-width: 768px) and (max-width: 1024px) {
            .booking-container {
                padding: 50px 40px;
                max-width: 700px;
            }
        }

        /* Mobile adjustments */
        @media (max-width: 767px) {
            .booking-container {
                padding: 30px 20px;
                border-width: 4px;
                border-radius: 30px;
            }
            
            .booking-page {
                padding: 15px 10px;
            }
        }

        .booking-title {
            color: #FF69B4;
            font-size: clamp(2.8rem, 8vw, 5rem);
            text-align: center;
            margin-bottom: 35px;
            text-shadow: 
                -2px -2px 0 white,  
                2px -2px 0 white,
                -2px 2px 0 white,
                2px 2px 0 white,
                0 0 25px #FF69B4,
                0 0 50px #FF69B4,
                0 0 75px #FF69B4;
            line-height: 1.3;
            word-break: break-word;
            background-color: black;
            padding: 15px 25px;
            border-radius: 80px;
            border: 4px solid #FF69B4;
            display: inline-block;
            width: auto;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0 0 50px #FF69B4;
            max-width: 95%;
        }

        .booking-form {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        /* Mobile gap adjustment */
        @media (max-width: 480px) {
            .booking-form {
                gap: 20px;
            }
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .form-group label {
            color: #FF69B4;
            font-weight: 700;
            font-size: clamp(1.3rem, 4vw, 1.8rem);
            letter-spacing: 1px;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white,
                0 0 12px #FF69B4;
            font-style: italic;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            background-color: black;
            border: 3px solid #FF69B4;
            border-radius: 20px;
            padding: 15px 20px;
            color: white;
            font-size: 1rem;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            box-shadow: 0 0 15px #FF69B4, inset 0 0 4px #FF69B4;
            width: 100%;
            -webkit-appearance: none; /* Better mobile styling */
            appearance: none;
        }

        /* Mobile input padding */
        @media (max-width: 480px) {
            .form-group input,
            .form-group select,
            .form-group textarea {
                padding: 12px 15px;
                font-size: 16px; /* Prevents zoom on mobile */
            }
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            box-shadow: 0 0 30px #FF69B4, inset 0 0 8px #FF69B4;
            border-color: white;
            background-color: #111;
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: #aaa;
            font-style: italic;
            font-size: 0.95rem;
        }

        .form-group select {
            background-image: linear-gradient(45deg, transparent 50%, #FF69B4 50%);
            background-position: calc(100% - 20px) calc(1em + 5px);
            background-size: 10px 10px;
            background-repeat: no-repeat;
            cursor: pointer;
        }

        .form-group select option {
            background-color: black;
            color: #FF69B4;
            padding: 12px;
        }

        .submit-btn {
            background-color: #FF69B4;
            color: black;
            border: 4px solid white;
            font-size: clamp(2rem, 6vw, 3rem);
            padding: 20px 30px;
            border-radius: 80px;
            cursor: pointer;
            margin-top: 30px;
            font-weight: 800;
            box-shadow: 
                0 0 40px #FF69B4,
                0 0 70px #FF69B4,
                inset 0 0 15px black;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 3px;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white;
            width: 100%;
            font-style: italic;
        }

        /* Mobile button */
        @media (max-width: 480px) {
            .submit-btn {
                padding: 15px 20px;
                font-size: 2rem;
                border-width: 3px;
                margin-top: 20px;
            }
        }

        .submit-btn:hover {
            background-color: black;
            color: #FF69B4;
            border-color: #FF69B4;
            box-shadow: 0 0 60px #FF69B4, 0 0 100px #FF69B4;
            transform: scale(1.02);
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white;
        }

        /* Page links - mobile responsive */
        .page-links {
            background-color: black;
            padding: 20px 15px;
            text-align: center;
            border-bottom: 6px solid #FF69B4;
            border-top: 6px solid #FF69B4;
            box-shadow: 0 0 40px #FF69B4;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .page-links a {
            color: #FF69B4;
            font-size: clamp(1.5rem, 5vw, 2.5rem);
            text-decoration: none;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white,
                0 0 15px #FF69B4,
                0 0 30px #FF69B4;
            padding: 10px 25px;
            border: 3px solid #FF69B4;
            border-radius: 60px;
            background-color: rgba(255, 105, 180, 0.1);
            transition: all 0.3s;
            font-style: italic;
            font-weight: 700;
            display: inline-block;
            white-space: nowrap;
        }

        /* Mobile nav */
        @media (max-width: 480px) {
            .page-links {
                flex-direction: column;
                align-items: center;
                gap: 10px;
                padding: 15px;
            }
            
            .page-links a {
                width: 80%;
                white-space: normal;
                padding: 8px 15px;
                font-size: 2rem;
            }
        }

        .page-links a:hover {
            background-color: #FF69B4;
            color: black;
            box-shadow: 0 0 50px #FF69B4;
            border-color: white;
            text-shadow: none;
        }

        footer {
            background-color: black;
            color: #FF69B4;
            text-align: center;
            padding: 25px 15px;
            border-top: 6px solid #FF69B4;
            border-bottom: 6px solid #FF69B4;
            font-size: clamp(1.2rem, 4vw, 1.8rem);
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white,
                0 0 15px #FF69B4;
            letter-spacing: 2px;
            font-style: italic;
            font-weight: 700;
        }

        /* Pink accents between images */
        .image-section {
            border-bottom: 4px solid #FF69B4;
            border-top: 4px solid #FF69B4;
            margin-top: -1px;
            box-shadow: 0 0 30px rgba(255, 105, 180, 0.5);
        }
        
        .image-section:first-of-type {
            border-top: none;
        }
        
        .image-section:last-of-type {
            border-bottom: none;
        }

        .full-width-image {
            border-left: 4px solid #FF69B4;
            border-right: 4px solid #FF69B4;
            box-shadow: 0 0 40px #FF69B4;
        }

        /* Last image section */
        .last-image-section {
            line-height: 0;
            font-size: 0;
            margin: 0;
            padding: 0;
            width: 100%;
            border-top: 8px solid #FF69B4;
            border-bottom: 8px solid #FF69B4;
            box-shadow: 0 0 50px #FF69B4;
        }

        .last-image-section img {
            border-left: 6px solid #FF69B4;
            border-right: 6px solid #FF69B4;
        }

        /* Mobile border adjustments */
        @media (max-width: 480px) {
            .image-section {
                border-bottom-width: 3px;
                border-top-width: 3px;
            }
            
            .full-width-image {
                border-left-width: 3px;
                border-right-width: 3px;
            }
            
            .last-image-section {
                border-top-width: 5px;
                border-bottom-width: 5px;
            }
            
            .last-image-section img {
                border-left-width: 4px;
                border-right-width: 4px;
            }
            
            .page-links {
                border-bottom-width: 4px;
                border-top-width: 4px;
            }
            
            footer {
                border-top-width: 4px;
                border-bottom-width: 4px;
            }
            
            .booking-page {
                border-top-width: 8px;
                border-bottom-width: 8px;
            }
        }

        /* Ensure images don't overflow */
        img {
            max-width: 100%;
            height: auto;
        }

        /* Touch-friendly improvements */
        button, a, input, select, textarea {
            touch-action: manipulation;
        }

        /* Better spacing for mobile */
        @media (max-width: 380px) {
            .brand-title {
                font-size: 2rem;
                padding: 8px 15px;
            }
            
            .booking-title {
                font-size: 2.2rem;
                padding: 12px 18px;
            }
            
            .form-group label {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Page Links - Mobile Optimized -->
    <div class="page-links">
        <a href="#home">Home</a>
        <a href="#book">Book Now</a>
    </div>

    <!-- HOME PAGE -->
    <div id="home">
        <!-- TOP IMAGE -->
        <div class="image-section">
            <img class="full-width-image" src="https://i.postimg.cc/fTHgBgQ5/Screenshot-2026-02-27-094113.png" alt="Top Image - Replace with direct image link">
        </div>

        <!-- HERO IMAGE WITH OVERLAY -->
        <div class="hero-container">
            <img class="hero-image" src="https://i.pinimg.com/736x/0a/a8/3b/0aa83b57dca86a1ca88d871a4c564840.jpg" alt="Hero Image with lashes">
            <div class="hero-overlay">
                <div class="brand-title">Pretty Lashes by Diamond</div>
                <a href="#book" class="book-now-btn">Book Now</a>
            </div>
        </div>

        <!-- IMAGE 2 -->
        <div class="image-section">
            <img class="full-width-image" src="https://i.postimg.cc/c4D5X5G9/Screenshot-2026-02-27-094048.png" alt="Lashes Info 2 - Replace with direct image link">
        </div>

        <!-- IMAGE 3 -->
        <div class="image-section">
            <img class="full-width-image" src="https://i.postimg.cc/xTsFtFVt/Screenshot-2026-02-27-094001.png" alt="Lashes Info 3 - Replace with direct image link">
        </div>
    </div>

    <!-- BOOKING PAGE -->
    <div id="book" class="booking-page">
        <div class="booking-container">
            <h1 class="booking-title">Pretty Lashes by Diamond</h1>
            <form class="booking-form">
                <div class="form-group">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" name="name" placeholder="Jane Doe" required>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" placeholder="jane@example.com" required>
                </div>
                <div class="form-group">
                    <label for="phone">Phone</label>
                    <input type="tel" id="phone" name="phone" placeholder="(123) 456-7890" required>
                </div>
                <div class="form-group">
                    <label for="service">Service</label>
                    <select id="service" name="service" required>
                        <option value="" disabled selected>Select a service</option>
                        <option value="classic">Classic Lashes</option>
                        <option value="volume">Volume Lashes</option>
                        <option value="hybrid">Hybrid Lashes</option>
                        <option value="fill">Lash Fill</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="date">Preferred Date</label>
                    <input type="date" id="date" name="date" required>
                </div>
                <div class="form-group">
                    <label for="notes">Notes (optional)</label>
                    <textarea id="notes" name="notes" rows="3" placeholder="Any special requests?"></textarea>
                </div>
                <button type="submit" class="submit-btn">Confirm Booking</button>
            </form>
        </div>
    </div>

    <!-- LAST IMAGE placed UNDER booking page -->
    <div class="last-image-section">
        <img class="full-width-image" src="https://i.postimg.cc/X72DQD6y/Screenshot-2026-02-27-093912.png" alt="Lashes Info 4 - Replace with direct image link">
    </div>

    <footer>
        Pretty Lashes by Diamond
    </footer>

    <script>
        // Smooth scroll for navigation with mobile support
        document.querySelectorAll('.page-links a, .book-now-btn').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                const href = this.getAttribute('href');
                if (href && href.startsWith('#')) {
                    e.preventDefault();
                    const target = document.querySelector(href);
                    if (target) {
                        target.scrollIntoView({ 
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                }
            });
        });

        // Add touch optimization
        if ('ontouchstart' in window) {
            document.documentElement.classList.add('touch');
        }
    </script>
</body>
</html>
