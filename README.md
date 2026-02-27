
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
            overflow-x: hidden;
        }

        /* Import Playfair Display for elegant cursive */
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,700&display=swap');

        /* Apply to all cursive elements */
        .brand-title, .book-now-btn, .booking-title, .form-group label, 
        .submit-btn, .page-links a, footer, .cursive-text {
            font-family: 'Playfair Display', 'Georgia', 'Times New Roman', serif;
            font-style: italic;
            font-weight: 700;
        }

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

        /* --- HOT PINK WITH WHITE OUTLINE & NEON GLOW - DEVICE OPTIMIZED --- */
        .brand-title {
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
            border-radius: 60px;
            border: 3px solid #FF69B4;
            box-shadow: 0 0 40px #FF69B4, inset 0 0 15px #FF69B4;
            word-break: break-word;
        }

        .book-now-btn {
            display: inline-block;
            background-color: black;
            color: #FF69B4;
            font-weight: 800;
            text-decoration: none;
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
        }

        .book-now-btn:hover {
            background-color: #FF69B4;
            color: black;
            border-color: white;
            box-shadow: 0 0 40px #FF69B4, 0 0 70px #FF69B4, inset 0 0 25px black;
            transform: scale(1.03);
            text-shadow: none;
        }

        /* --- BOOKING PAGE STYLES --- */
        .booking-page {
            background-color: black;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            font-family: sans-serif;
            border-top: 12px solid #FF69B4;
            border-bottom: 12px solid #FF69B4;
            position: relative;
        }

        .booking-container {
            width: 100%;
            background-color: #0a0a0a;
            border: 6px solid #FF69B4;
            border-radius: 40px;
            box-shadow: 
                0 0 60px #FF69B4,
                inset 0 0 25px rgba(255, 105, 180, 0.5);
        }

        .booking-title {
            color: #FF69B4;
            text-align: center;
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
            border-radius: 80px;
            border: 4px solid #FF69B4;
            display: inline-block;
            width: auto;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0 0 50px #FF69B4;
        }

        .booking-form {
            display: flex;
            flex-direction: column;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            color: #FF69B4;
            font-weight: 700;
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
            color: white;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            box-shadow: 0 0 15px #FF69B4, inset 0 0 4px #FF69B4;
            width: 100%;
            -webkit-appearance: none;
            appearance: none;
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
        }

        .submit-btn {
            background-color: #FF69B4;
            color: black;
            border: 4px solid white;
            border-radius: 80px;
            cursor: pointer;
            font-weight: 800;
            box-shadow: 
                0 0 40px #FF69B4,
                0 0 70px #FF69B4,
                inset 0 0 15px black;
            transition: all 0.3s ease;
            text-transform: uppercase;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white;
            width: 100%;
            font-style: italic;
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

        /* Page links */
        .page-links {
            background-color: black;
            text-align: center;
            border-bottom: 6px solid #FF69B4;
            border-top: 6px solid #FF69B4;
            box-shadow: 0 0 40px #FF69B4;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }

        .page-links a {
            color: #FF69B4;
            text-decoration: none;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white,
                0 0 15px #FF69B4,
                0 0 30px #FF69B4;
            border: 3px solid #FF69B4;
            border-radius: 60px;
            background-color: rgba(255, 105, 180, 0.1);
            transition: all 0.3s;
            font-style: italic;
            font-weight: 700;
            display: inline-block;
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
            border-top: 6px solid #FF69B4;
            border-bottom: 6px solid #FF69B4;
            text-shadow: 
                -1px -1px 0 white,  
                1px -1px 0 white,
                -1px 1px 0 white,
                1px 1px 0 white,
                0 0 15px #FF69B4;
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

        img {
            max-width: 100%;
            height: auto;
        }

        button, a, input, select, textarea {
            touch-action: manipulation;
        }

        /* ===== DEVICE-SPECIFIC OPTIMIZATIONS ===== */

        /* --- MOBILE (up to 767px) --- */
        @media (max-width: 767px) {
            /* Hero section */
            .brand-title {
                font-size: clamp(2.2rem, 8vw, 3.5rem);
                padding: 10px 20px;
                margin-bottom: 15px;
            }
            
            .book-now-btn {
                font-size: clamp(1.5rem, 5vw, 2.2rem);
                padding: 12px 30px;
                white-space: normal;
            }
            
            /* Booking page */
            .booking-page {
                padding: 15px 10px;
                border-top-width: 8px;
                border-bottom-width: 8px;
            }
            
            .booking-container {
                max-width: 100%;
                padding: 25px 18px;
                border-width: 4px;
                border-radius: 30px;
            }
            
            .booking-title {
                font-size: clamp(2.2rem, 7vw, 3rem);
                padding: 12px 18px;
                margin-bottom: 25px;
                border-width: 3px;
            }
            
            .booking-form {
                gap: 18px;
            }
            
            .form-group {
                gap: 6px;
            }
            
            .form-group label {
                font-size: 1.3rem;
            }
            
            .form-group input,
            .form-group select,
            .form-group textarea {
                padding: 12px 15px;
                font-size: 16px;
                border-width: 2px;
            }
            
            .submit-btn {
                font-size: 1.8rem;
                padding: 15px 20px;
                margin-top: 20px;
                border-width: 3px;
            }
            
            /* Navigation */
            .page-links {
                flex-direction: column;
                align-items: center;
                gap: 10px;
                padding: 15px;
                border-bottom-width: 4px;
                border-top-width: 4px;
            }
            
            .page-links a {
                width: 80%;
                font-size: 1.8rem;
                padding: 8px 15px;
                white-space: normal;
            }
            
            /* Footer */
            footer {
                font-size: 1.2rem;
                padding: 18px 12px;
                border-top-width: 4px;
                border-bottom-width: 4px;
            }
            
            /* Image borders */
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
        }

        /* --- TABLET (768px to 1024px) --- */
        @media (min-width: 768px) and (max-width: 1024px) {
            /* Hero section */
            .brand-title {
                font-size: clamp(3.5rem, 7vw, 5rem);
                padding: 15px 35px;
                margin-bottom: 25px;
                border-width: 4px;
            }
            
            .book-now-btn {
                font-size: clamp(2rem, 4.5vw, 3rem);
                padding: 18px 50px;
            }
            
            /* Booking page */
            .booking-page {
                padding: 30px 25px;
                border-top-width: 10px;
                border-bottom-width: 10px;
            }
            
            .booking-container {
                max-width: 700px;
                padding: 45px 40px;
                border-width: 5px;
                border-radius: 45px;
            }
            
            .booking-title {
                font-size: clamp(3.2rem, 6vw, 4.2rem);
                padding: 18px 28px;
                margin-bottom: 35px;
            }
            
            .booking-form {
                gap: 22px;
            }
            
            .form-group label {
                font-size: 1.6rem;
            }
            
            .form-group input,
            .form-group select,
            .form-group textarea {
                padding: 16px 22px;
                font-size: 1.1rem;
                border-width: 3px;
            }
            
            .submit-btn {
                font-size: 2.4rem;
                padding: 18px 30px;
                margin-top: 25px;
            }
            
            /* Navigation */
            .page-links {
                gap: 20px;
                padding: 18px;
            }
            
            .page-links a {
                font-size: 2.2rem;
                padding: 12px 30px;
            }
            
            /* Footer */
            footer {
                font-size: 1.6rem;
                padding: 22px 18px;
            }
            
            /* Keep image borders consistent */
            .image-section {
                border-bottom-width: 4px;
                border-top-width: 4px;
            }
            
            .full-width-image {
                border-left-width: 4px;
                border-right-width: 4px;
            }
        }

        /* --- COMPUTER/DESKTOP (1025px and above) --- */
        @media (min-width: 1025px) {
            /* Hero section - larger and more dramatic */
            .brand-title {
                font-size: clamp(5rem, 8vw, 7rem);
                padding: 20px 60px;
                margin-bottom: 35px;
                border-width: 5px;
                box-shadow: 0 0 60px #FF69B4, inset 0 0 25px #FF69B4;
            }
            
            .book-now-btn {
                font-size: clamp(2.5rem, 4vw, 3.5rem);
                padding: 25px 80px;
                border-width: 5px;
                box-shadow: 0 0 40px #FF69B4, 0 0 70px #FF69B4, inset 0 0 15px #FF69B4;
            }
            
            .book-now-btn:hover {
                transform: scale(1.05);
            }
            
            /* Booking page - spacious and elegant */
            .booking-page {
                padding: 50px 30px;
                border-top-width: 15px;
                border-bottom-width: 15px;
            }
            
            .booking-container {
                max-width: 900px;
                padding: 60px 60px;
                border-width: 8px;
                border-radius: 60px;
            }
            
            .booking-title {
                font-size: 5rem;
                padding: 25px 45px;
                margin-bottom: 45px;
                border-width: 5px;
            }
            
            .booking-form {
                gap: 30px;
            }
            
            .form-group {
                gap: 10px;
            }
            
            .form-group label {
                font-size: 1.9rem;
                letter-spacing: 1.5px;
            }
            
            .form-group input,
            .form-group select,
            .form-group textarea {
                padding: 18px 25px;
                font-size: 1.2rem;
                border-width: 4px;
                border-radius: 25px;
            }
            
            .submit-btn {
                font-size: 3rem;
                padding: 25px 40px;
                margin-top: 35px;
                border-width: 5px;
            }
            
            /* Navigation */
            .page-links {
                gap: 40px;
                padding: 25px;
                border-bottom-width: 8px;
                border-top-width: 8px;
            }
            
            .page-links a {
                font-size: 2.5rem;
                padding: 15px 40px;
                border-width: 4px;
                transition: all 0.3s ease;
            }
            
            .page-links a:hover {
                transform: scale(1.05);
            }
            
            /* Footer */
            footer {
                font-size: 1.9rem;
                padding: 30px 25px;
                border-top-width: 8px;
                border-bottom-width: 8px;
            }
            
            /* Image borders - more prominent on desktop */
            .image-section {
                border-bottom-width: 5px;
                border-top-width: 5px;
            }
            
            .full-width-image {
                border-left-width: 5px;
                border-right-width: 5px;
            }
            
            .last-image-section {
                border-top-width: 10px;
                border-bottom-width: 10px;
            }
            
            .last-image-section img {
                border-left-width: 8px;
                border-right-width: 8px;
            }
        }

        /* --- LARGE DESKTOP (1440px and above) --- */
        @media (min-width: 1440px) {
            .booking-container {
                max-width: 1100px;
                padding: 70px 80px;
            }
            
            .brand-title {
                font-size: 7rem;
                padding: 25px 80px;
            }
            
            .book-now-btn {
                font-size: 3.5rem;
                padding: 30px 100px;
            }
            
            .page-links {
                padding: 30px;
            }
            
            .page-links a {
                font-size: 2.8rem;
                padding: 18px 50px;
            }
        }
    </style>
</head>
<body>

    <!-- Page Links -->
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
        // Smooth scroll for navigation
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

        // Add touch optimization class
        if ('ontouchstart' in window) {
            document.documentElement.classList.add('touch');
        }
    </script>
</body>
</html>
