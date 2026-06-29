# giltcorvus
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Holding Company | Investment & Management</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            height: 100%;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            overflow: hidden;
        }

        /* Fullscreen background slideshow */
        #bg-slideshow {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            opacity: 0;
            transition: opacity 1.5s ease-in-out;
        }

        .slide.active {
            opacity: 1;
        }

        /* Frosted Glass (Glassmorphism) Content Box */
        .container {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            background: rgba(255, 255, 255, 0.08); /* Transparent base */
            backdrop-filter: blur(20px); /* The frosty blur effect */
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 16px;
            padding: 60px 80px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.3);
            color: #ffffff;
            width: 90%;
            max-width: 600px;
        }

        .logo {
            font-size: 2rem;
            font-weight: 700;
            letter-spacing: 0.15em;
            text-transform: uppercase;
            margin-bottom: 20px;
            color: #f8fafc;
        }

        .divider {
            width: 60px;
            height: 3px;
            background-color: #ffffff;
            margin: 0 auto 30px auto;
            border-radius: 2px;
        }

        .tagline {
            font-size: 1.1rem;
            font-weight: 300;
            letter-spacing: 0.05em;
            line-height: 1.6;
            margin-bottom: 40px;
            color: #e2e8f0;
        }

        .contact-btn {
            display: inline-block;
            text-decoration: none;
            color: #ffffff;
            background-color: rgba(255, 255, 255, 0.1);
            padding: 14px 32px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
            letter-spacing: 0.05em;
            transition: all 0.3s ease;
        }

        .contact-btn:hover {
            background-color: rgba(255, 255, 255, 0.25);
            transform: translateY(-2px);
        }
    </style>
</head>
<body>

    <!-- Background Slideshow -->
    <div id="bg-slideshow">
        <!-- Add your beautiful professional images here -->
        <div class="slide active" style="background-image: url('https://unsplash.com');"></div>
        <div class="slide" style="background-image: url('https://unsplash.com');"></div>
        <div class="slide" style="background-image: url('https://unsplash.com');"></div>
    </div>

    <!-- Centered Glassy Content -->
    <div class="container">
        <div class="logo">Nexus Holdings</div>
        <div class="divider"></div>
        <p class="tagline">Strategic investments and global management driving sustainable growth and innovation across our portfolio.</p>
        <a href="mailto:contact@nexus-holdings.com" class="contact-btn">Get in Touch</a>
    </div>

    <!-- Slideshow JavaScript -->
    <script>
        const slides = document.querySelectorAll('.slide');
        let currentSlide = 0;

        function nextSlide() {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        }

        // Change background every 6 seconds
        setInterval(nextSlide, 6000); 
    </script>
</body>
</html>
