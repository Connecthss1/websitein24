<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Websitein24 | Fast Sites. Built Right.</title>
    <meta name="description" content="Professional websites delivered fast. Custom web design for business owners - fast, quality, and creative solutions that drive results.">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #334155;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #155e75 100%);
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 80px;
            right: 40px;
            width: 300px;
            height: 300px;
            background: linear-gradient(45deg, #06b6d4, #3b82f6);
            border-radius: 50%;
            filter: blur(80px);
            opacity: 0.2;
            animation: pulse 3s infinite;
        }

        .hero::after {
            content: '';
            position: absolute;
            bottom: 80px;
            left: 40px;
            width: 400px;
            height: 400px;
            background: linear-gradient(45deg, #3b82f6, #06b6d4);
            border-radius: 50%;
            filter: blur(80px);
            opacity: 0.2;
            animation: pulse 3s infinite 1.5s;
        }

        .hero-content {
            text-align: center;
            position: relative;
            z-index: 10;
            padding: 80px 0;
        }

        .logo-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 4px;
            width: 128px;
            margin: 0 auto 32px;
        }

        .logo-tile {
            width: 24px;
            height: 24px;
            background: linear-gradient(45deg, #22d3ee, #3b82f6);
            border-radius: 4px;
            animation: pulse 2s infinite;
        }

        .logo-tile:nth-child(odd) {
            animation-delay: 0.1s;
        }

        .logo-tile:nth-child(even) {
            animation-delay: 0.2s;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 900;
            color: white;
            margin-bottom: 16px;
            letter-spacing: -0.02em;
        }

        .hero .tagline {
            font-size: 2rem;
            color: #22d3ee;
            font-weight: 300;
            margin-bottom: 32px;
            letter-spacing: 0.05em;
        }

        .hero .description {
            font-size: 1.25rem;
            color: #cbd5e1;
            margin-bottom: 48px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-buttons {
            display: flex;
            gap: 24px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            padding: 20px 40px;
            border-radius: 12px;
            font-weight: 600;
            font-size: 1.125rem;
            text-decoration: none;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn-primary {
            background: linear-gradient(45deg, #06b6d4, #3b82f6);
            color: white;
            box-shadow: 0 20px 40px rgba(59, 130, 246, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 25px 50px rgba(59, 130, 246, 0.4);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.1);
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        /* Portfolio Section */
        .portfolio {
            padding: 80px 0;
            background: #f8fafc;
        }

        .section-title {
            text-align: center;
            margin-bottom: 64px;
        }

        .section-title h2 {
            font-size: 3.5rem;
            font-weight: 700;
            color: #0f172a;
            margin-bottom: 24px;
        }

        .gradient-text {
            background: linear-gradient(45deg, #0891b2, #3b82f6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-title p {
            font-size: 1.25rem;
            color: #64748b;
            max-width: 600px;
            margin: 0 auto;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 32px;
            margin-bottom: 48px;
        }

        .portfolio-item {
            background: white;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .portfolio-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .portfolio-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-item-content {
            padding: 24px;
        }

        .portfolio-item h3 {
            font-size: 1.25rem;
            font-weight: 700;
            color: #0f172a;
            margin-bottom: 8px;
        }

        .portfolio-item p {
            color: #64748b;
            margin-bottom: 16px;
        }

        .tags {
            display: flex;
            gap: 8px;
        }

        .tag {
            padding: 4px 12px;
            background: linear-gradient(45deg, #cffafe, #dbeafe);
            color: #0891b2;
            border-radius: 20px;
            font-size: 0.875rem;
            font-weight: 500;
        }

        /* About Section */
        .about {
            padding: 80px 0;
            background: white;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 64px;
            align-items: center;
        }

        .mission-vision {
            margin-bottom: 32px;
        }

        .mission-item, .vision-item {
            padding: 24px;
            border-radius: 16px;
            margin-bottom: 24px;
            border: 1px solid #e2e8f0;
        }

        .mission-item {
            background: linear-gradient(45deg, #f8fafc, #cffafe);
        }

        .vision-item {
            background: linear-gradient(45deg, #f8fafc, #dbeafe);
        }

        .mission-item h3, .vision-item h3 {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.25rem;
            font-weight: 700;
            color: #0f172a;
            margin-bottom: 12px;
        }

        .stats {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }

        .stat-item {
            display: flex;
            align-items: center;
            gap: 12px;
            background: white;
            padding: 16px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            border: 1px solid #e2e8f0;
        }

        .stat-number {
            font-weight: 700;
            color: #0f172a;
        }

        .stat-label {
            font-size: 0.875rem;
            color: #64748b;
        }

        .about img {
            width: 100%;
            border-radius: 16px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        /* Waitlist Section */
        .waitlist {
            padding: 80px 0;
            background: linear-gradient(45deg, #0f172a, #155e75);
            position: relative;
            overflow: hidden;
        }

        .waitlist::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 400px;
            height: 400px;
            background: rgba(6, 182, 212, 0.2);
            border-radius: 50%;
            transform: translate(200px, -200px);
        }

        .waitlist::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 300px;
            height: 300px;
            background: rgba(59, 130, 246, 0.2);
            border-radius: 50%;
            transform: translate(-150px, 150px);
        }

        .waitlist-content {
            text-align: center;
            position: relative;
            z-index: 10;
        }

        .waitlist h2 {
            font-size: 3.5rem;
            font-weight: 700;
            color: white;
            margin-bottom: 24px;
        }

        .waitlist p {
            font-size: 1.25rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 32px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .waitlist-form {
            display: flex;
            gap: 12px;
            max-width: 400px;
            margin: 0 auto;
        }

        .waitlist-form input {
            flex: 1;
            padding: 16px;
            border: none;
            border-radius: 12px;
            font-size: 1rem;
        }

        .waitlist-form button {
            padding: 16px 24px;
            background: white;
            color: #0f172a;
            border: none;
            border-radius: 12px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .waitlist-form button:hover {
            background: #f1f5f9;
        }

        /* Contact Section */
        .contact {
            padding: 80px 0;
            background: white;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 64px;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 24px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-weight: 600;
            color: #0f172a;
            margin-bottom: 8px;
        }

        .form-group input,
        .form-group textarea {
            padding: 12px 16px;
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #06b6d4;
            box-shadow: 0 0 0 3px rgba(6, 182, 212, 0.1);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .contact-info {
            background: linear-gradient(45deg, #06b6d4, #3b82f6);
            padding: 32px;
            border-radius: 16px;
            color: white;
        }

        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 24px;
        }

        .contact-info p {
            margin-bottom: 24px;
            opacity: 0.9;
        }

        .features-list {
            list-style: none;
            margin-bottom: 32px;
        }

        .features-list li {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 16px;
        }

        .phone-info {
            background: linear-gradient(45deg, #f8fafc, #cffafe);
            padding: 24px;
            border-radius: 16px;
            margin-top: 32px;
            border: 1px solid #22d3ee;
        }

        .phone-info h4 {
            color: #0f172a;
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .phone-info p {
            color: #64748b;
            margin-bottom: 16px;
        }

        .phone-number {
            font-size: 1.5rem;
            font-weight: 700;
            color: #0891b2;
            text-decoration: none;
        }

        .phone-number:hover {
            color: #3b82f6;
        }

        /* Footer */
        .footer {
            background: #0f172a;
            color: white;
            padding: 48px 0;
            text-align: center;
        }

        .footer h4 {
            font-size: 1.875rem;
            font-weight: 700;
            margin-bottom: 16px;
        }

        .footer p {
            color: #94a3b8;
            margin-bottom: 24px;
        }

        .footer-info {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 32px;
            color: #94a3b8;
            flex-wrap: wrap;
        }

        .footer-phone {
            display: flex;
            align-items: center;
            gap: 8px;
            color: #22d3ee;
            text-decoration: none;
        }

        .footer-phone:hover {
            color: white;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero .tagline {
                font-size: 1.5rem;
            }

            .section-title h2 {
                font-size: 2.5rem;
            }

            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
                gap: 32px;
            }

            .portfolio-grid {
                grid-template-columns: 1fr;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .waitlist-form {
                flex-direction: column;
            }

            .stats {
                justify-content: center;
            }

            .footer-info {
                flex-direction: column;
                gap: 16px;
            }
        }

        @keyframes pulse {
            0%, 100% {
                opacity: 0.2;
            }
            50% {
                opacity: 0.4;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="logo-grid">
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                    <div class="logo-tile"></div>
                </div>
               
                <h1>WEBSITEIN24</h1>
                <p class="tagline">YOUR WEBSITE. READY WHEN YOU ARE</p>
                <p class="description">
                    Custom websites for business owners—delivered fast, with quality and creativity that drives real results.
                </p>
               
                <div class="hero-buttons">
                    <a href="#contact" class="btn btn-primary">
                        Get Free Consultation
                        <span>→</span>
                    </a>
                    <a href="tel:651-780-7536" class="btn btn-secondary">
                        📞 651-780-7536
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>Our <span class="gradient-text">Work</span></h2>
                <p>Here are some examples of stunning websites we've built for businesses just like yours.</p>
            </div>
           
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1560472354-b33ff0c44a43?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400" alt="Professional Services">
                    <div class="portfolio-item-content">
                        <h3>Professional Services</h3>
                        <p>Modern business website with client portal and service booking</p>
                        <div class="tags">
                            <span class="tag">Services</span>
                            <span class="tag">Business</span>
                        </div>
                    </div>
                </div>
               
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400" alt="Tech Startup">
                    <div class="portfolio-item-content">
                        <h3>Tech Startup</h3>
                        <p>Innovative SaaS platform with modern user interface and analytics</p>
                        <div class="tags">
                            <span class="tag">SaaS</span>
                            <span class="tag">Technology</span>
                        </div>
                    </div>
                </div>
               
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1414235077428-338989a2e8c0?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400" alt="Restaurant Website">
                    <div class="portfolio-item-content">
                        <h3>Restaurant Website</h3>
                        <p>Elegant dining experience with menu showcase and online reservations</p>
                        <div class="tags">
                            <span class="tag">Restaurant</span>
                            <span class="tag">Hospitality</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about">
        <div class="container">
            <div class="about-grid">
                <div>
                    <div class="section-title" style="text-align: left; margin-bottom: 32px;">
                        <h2>About <span class="gradient-text">Us</span></h2>
                    </div>
                   
                    <div class="mission-vision">
                        <div class="mission-item">
                            <h3>🎯 Mission</h3>
                            <p>To empower business owners with fast, professional websites that elevate their brand and drive results.</p>
                        </div>
                       
                        <div class="vision-item">
                            <h3>👁️ Vision</h3>
                            <p>To be the go-to web design solution for entrepreneurs who value speed, style, and strategy.</p>
                        </div>
                    </div>
                   
                    <p style="font-size: 1.125rem; margin-bottom: 32px;">
                        We're a passionate team that believes beautiful, effective websites shouldn't take months to build.
                        We deliver custom-crafted sites in record time—without compromising quality.
                    </p>
                   
                    <div class="stats">
                        <div class="stat-item">
                            <span style="font-size: 2rem;">⚡</span>
                            <div>
                                <div class="stat-number">Fast</div>
                                <div class="stat-label">Delivery</div>
                            </div>
                        </div>
                        <div class="stat-item">
                            <span style="font-size: 2rem;">⭐</span>
                            <div>
                                <div class="stat-number">Premium</div>
                                <div class="stat-label">Quality</div>
                            </div>
                        </div>
                        <div class="stat-item">
                            <span style="font-size: 2rem;">👥</span>
                            <div>
                                <div class="stat-number">100+</div>
                                <div class="stat-label">Happy Clients</div>
                            </div>
                        </div>
                    </div>
                </div>
               
                <div>
                    <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&h=600" alt="Team collaboration">
                </div>
            </div>
        </div>
    </section>

    <!-- Waitlist Section -->
    <section class="waitlist">
        <div class="container">
            <div class="waitlist-content">
                <h2>Join Our Waitlist</h2>
                <p>Be the first to know about our latest projects and get exclusive access to our design resources.</p>
               
                <form class="waitlist-form" action="https://formspree.io/f/xpznvqwl" method="POST">
                    <input type="email" name="email" placeholder="Enter your email" required>
                    <input type="hidden" name="_subject" value="New Waitlist Signup - Websitein24">
                    <input type="hidden" name="form_type" value="waitlist">
                    <button type="submit">Join Now</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Let's Build Your <span class="gradient-text">Dream Website</span></h2>
                <p>Ready to transform your business with a stunning website? Let's talk about your vision and make it reality.</p>
            </div>
           
            <div class="contact-grid">
                <div>
                    <form class="contact-form" action="https://formspree.io/f/xpznvqwl" method="POST">
                        <div class="form-group">
                            <label>Your Name</label>
                            <input type="text" name="name" placeholder="Enter your full name" required>
                        </div>
                       
                        <div class="form-group">
                            <label>Email Address</label>
                            <input type="email" name="email" placeholder="your@email.com" required>
                        </div>
                       
                        <div class="form-group">
                            <label>Project Details</label>
                            <textarea name="message" placeholder="Tell us about your project, timeline, and any specific requirements..." required></textarea>
                        </div>
                       
                        <input type="hidden" name="_replyto" value="kaldan1953@gmail.com">
                        <input type="hidden" name="_subject" value="New Website Inquiry from Websitein24">
                        <input type="hidden" name="_next" value="thank-you.html">
                       
                        <button type="submit" class="btn btn-primary" style="width: 100%;">
                            📧 Send Message
                        </button>
                    </form>
                   
                    <div class="phone-info">
                        <h4>📞 Prefer to talk directly?</h4>
                        <p>Call us for immediate assistance and consultation</p>
                        <a href="tel:651-780-7536" class="phone-number">651-780-7536</a>
                    </div>
                </div>
               
                <div>
                    <div class="contact-info">
                        <h3>Schedule a Free Consultation</h3>
                        <p>Book a 30-minute call to discuss your project in detail. We'll provide insights, recommendations, and a custom quote tailored to your needs.</p>
                       
                        <ul class="features-list">
                            <li>✅ Free 30-minute consultation</li>
                            <li>✅ Custom project timeline</li>
                            <li>✅ Detailed cost breakdown</li>
                            <li>✅ Design mockup preview</li>
                        </ul>
                       
                        <a href="https://calendly.com/websitein24" target="_blank" class="btn btn-secondary" style="width: 100%; background: white; color: #06b6d4;">
                            📅 Book Your Call
                        </a>
                    </div>
                   
                    <div style="margin-top: 32px;">
                        <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400" alt="Modern workspace" style="width: 100%; border-radius: 16px;">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <h4><span class="gradient-text">Websitein24</span></h4>
            <p>Fast sites. Built right. Professional websites delivered in record time.</p>
            <div class="footer-info">
                <a href="tel:651-780-7536" class="footer-phone">
                    📞 651-780-7536
                </a>
                <span>|</span>
                <span>&copy; 2025 Websitein24. All rights reserved.</span>
            </div>
        </div>
    </footer>

    <script>
        function handleWaitlistSubmit(event) {
            event.preventDefault();
            const email = event.target.querySelector('input[type="email"]').value;
            alert(`Thank you! ${email} has been added to our waitlist.`);
            event.target.reset();
        }

        function handleContactSubmit(event) {
            event.preventDefault();
            alert('Thank you for your message! We\'ll get back to you within 24 hours.');
            event.target.reset();
        }

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>

