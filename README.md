<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sire & Shield | Specialty Horse & Dog Insurance</title>
    <style>
        :root {
            --primary: #1a1a2e;
            --accent: #8B0000;
            --gold: #DAA520;
            --light: #f8f9fa;
            --text: #333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text);
            overflow-x: hidden;
        }
        
        /* Navigation */
        nav {
            background: rgba(26, 26, 46, 0.98);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }
        
        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        nav .logo {
            font-size: 28px;
            font-weight: bold;
            color: white;
            text-decoration: none;
            letter-spacing: 1px;
        }
        
        nav .logo span {
            color: var(--gold);
        }
        
        nav ul {
            list-style: none;
            display: flex;
            gap: 30px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }
        
        nav a:hover {
            color: var(--gold);
        }
        
        .cta-button {
            background: var(--accent);
            color: white;
            padding: 12px 30px;
            border-radius: 25px;
            text-decoration: none;
            transition: all 0.3s;
            font-weight: 600;
        }
        
        .cta-button:hover {
            background: #B22222;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(139, 0, 0, 0.3);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%);
            color: white;
            padding: 180px 20px 100px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><path d="M0,300 Q300,200 600,300 T1200,300 L1200,600 L0,600 Z" fill="rgba(255,255,255,0.05)"/></svg>') no-repeat bottom;
            opacity: 0.3;
        }
        
        .hero .container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 64px;
            margin-bottom: 20px;
            letter-spacing: 2px;
            animation: fadeInUp 1s ease-out;
        }
        
        .hero .tagline {
            font-size: 28px;
            margin-bottom: 15px;
            opacity: 0.95;
            font-style: italic;
            animation: fadeInUp 1s ease-out 0.2s both;
        }
        
        .hero .subtitle {
            font-size: 20px;
            max-width: 800px;
            margin: 0 auto 40px;
            opacity: 0.9;
            animation: fadeInUp 1s ease-out 0.4s both;
        }
        
        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 60px;
            margin-top: 50px;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease-out 0.6s both;
        }
        
        .stat {
            text-align: center;
        }
        
        .stat-number {
            font-size: 48px;
            font-weight: bold;
            color: var(--gold);
            margin-bottom: 5px;
        }
        
        .stat-label {
            font-size: 16px;
            opacity: 0.9;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Section Styles */
        .section {
            padding: 80px 20px;
        }
        
        .section-light {
            background: var(--light);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-header h2 {
            font-size: 42px;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .section-header p {
            font-size: 20px;
            color: #666;
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* Coverage Cards */
        .coverage-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .coverage-card {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s;
            border: 2px solid transparent;
        }
        
        .coverage-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(139, 0, 0, 0.2);
            border-color: var(--accent);
        }
        
        .coverage-icon {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .coverage-card h3 {
            font-size: 24px;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .coverage-card p {
            color: #666;
            margin-bottom: 20px;
        }
        
        .coverage-features {
            list-style: none;
            margin-top: 20px;
        }
        
        .coverage-features li {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
            color: #555;
        }
        
        .coverage-features li:last-child {
            border-bottom: none;
        }
        
        .coverage-features li::before {
            content: "✓ ";
            color: var(--accent);
            font-weight: bold;
            margin-right: 10px;
        }
        
        /* Advantages Section */
        .advantages {
            background: var(--primary);
            color: white;
            padding: 80px 20px;
        }
        
        .advantages h2 {
            color: white;
        }
        
        .advantages-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }
        
        .advantage-item {
            text-align: center;
            padding: 30px;
        }
        
        .advantage-icon {
            font-size: 56px;
            margin-bottom: 20px;
            color: var(--gold);
        }
        
        .advantage-item h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--gold);
        }
        
        .advantage-item p {
            font-size: 16px;
            opacity: 0.9;
            line-height: 1.8;
        }
        
        /* Process Section */
        .process-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .process-step {
            text-align: center;
            padding: 30px 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            position: relative;
        }
        
        .step-number {
            width: 60px;
            height: 60px;
            background: var(--accent);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            font-weight: bold;
            margin: 0 auto 20px;
        }
        
        .process-step h3 {
            font-size: 20px;
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .process-step p {
            color: #666;
        }
        
        /* Testimonials */
        .testimonials {
            background: var(--light);
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .testimonial {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            border-left: 4px solid var(--accent);
        }
        
        .testimonial-text {
            font-style: italic;
            color: #555;
            margin-bottom: 20px;
            line-height: 1.8;
        }
        
        .testimonial-author {
            font-weight: bold;
            color: var(--primary);
        }
        
        .testimonial-role {
            color: #888;
            font-size: 14px;
        }
        
        /* CTA Section */
        .cta-section {
            background: linear-gradient(135deg, var(--accent), #B22222);
            color: white;
            padding: 80px 20px;
            text-align: center;
        }
        
        .cta-section h2 {
            font-size: 42px;
            margin-bottom: 20px;
        }
        
        .cta-section p {
            font-size: 20px;
            margin-bottom: 40px;
            opacity: 0.95;
        }
        
        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .btn-primary {
            background: white;
            color: var(--accent);
            padding: 15px 40px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            transition: all 0.3s;
            display: inline-block;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        
        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
            padding: 15px 40px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            transition: all 0.3s;
            display: inline-block;
        }
        
        .btn-secondary:hover {
            background: white;
            color: var(--accent);
            transform: translateY(-3px);
        }
        
        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 60px 20px 30px;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-section h3 {
            color: var(--gold);
            margin-bottom: 20px;
            font-size: 20px;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section li {
            margin-bottom: 10px;
        }
        
        .footer-section a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-section a:hover {
            color: var(--gold);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.6);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            nav ul {
                display: none;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero .tagline {
                font-size: 20px;
            }
            
            .hero-stats {
                gap: 30px;
            }
            
            .stat-number {
                font-size: 32px;
            }
            
            .section-header h2 {
                font-size: 32px;
            }
            
            .coverage-grid,
            .advantages-grid,
            .process-steps {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <a href="#" class="logo">SIRE & <span>SHIELD</span></a>
            <ul>
                <li><a href="#coverage">Coverage</a></li>
                <li><a href="#advantages">Why Us</a></li>
                <li><a href="#process">Process</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="#contact" class="cta-button">Get a Quote</a>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>SIRE & SHIELD</h1>
            <p class="tagline">Specialty Horse & Dog Insurance</p>
            <p class="subtitle">Protecting elite animals through data-driven insurance solutions with genetic risk assessment for superior coverage and pricing</p>
            
            <div class="hero-stats">
                <div class="stat">
                    <div class="stat-number">15-30%</div>
                    <div class="stat-label">Better Premiums</div>
                </div>
                <div class="stat">
                    <div class="stat-number">85%</div>
                    <div class="stat-label">Customer Retention</div>
                </div>
                <div class="stat">
                    <div class="stat-number">24/7</div>
                    <div class="stat-label">Claims Support</div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Coverage Section -->
    <section id="coverage" class="section">
        <div class="container">
            <div class="section-header">
                <h2>Comprehensive Coverage Options</h2>
                <p>From mortality to major medical, we protect your investment with specialized policies tailored to elite animals</p>
            </div>
            
            <div class="coverage-grid">
                <div class="coverage-card">
                    <div class="coverage-icon">🐴</div>
                    <h3>Equine Mortality</h3>
                    <p>Full coverage for death from any cause, protecting horses valued from $50,000 to $10,000,000</p>
                    <ul class="coverage-features">
                        <li>2.5-4.5% annual premium</li>
                        <li>Death from accident or illness</li>
                        <li>Humane destruction coverage</li>
                        <li>Worldwide protection</li>
                    </ul>
                </div>
                
                <div class="coverage-card">
                    <div class="coverage-icon">🏆</div>
                    <h3>Loss of Use</h3>
                    <p>Critical protection when your horse can no longer perform racing, showing, or breeding duties</p>
                    <ul class="coverage-features">
                        <li>Performance horse focus</li>
                        <li>Competition & racing coverage</li>
                        <li>Breeding stock protection</li>
                        <li>Permanent disability</li>
                    </ul>
                </div>
                
                <div class="coverage-card">
                    <div class="coverage-icon">⚕️</div>
                    <h3>Major Medical</h3>
                    <p>Comprehensive coverage for surgical procedures and major medical expenses up to $25,000 per incident</p>
                    <ul class="coverage-features">
                        <li>Colic surgery coverage</li>
                        <li>Emergency procedures</li>
                        <li>Diagnostic imaging</li>
                        <li>Specialist consultations</li>
                    </ul>
                </div>
                
                <div class="coverage-card">
                    <div class="coverage-icon">🛡️</div>
                    <h3>Liability Insurance</h3>
                    <p>Protect your business from lawsuits and accidents at your training facility or events</p>
                    <ul class="coverage-features">
                        <li>Trainer/facility coverage</li>
                        <li>$1M-$5M limits available</li>
                        <li>Competition venue required</li>
                        <li>Property damage protection</li>
                    </ul>
                </div>
                
                <div class="coverage-card">
                    <div class="coverage-icon">🐕</div>
                    <h3>Canine Performance</h3>
                    <p>Specialized insurance for show dogs, service dogs, and valuable breeding animals</p>
                    <ul class="coverage-features">
                        <li>Show dog protection</li>
                        <li>Service dog coverage</li>
                        <li>Breeding stock insurance</li>
                        <li>Working dog policies</li>
                    </ul>
                </div>
                
                <div class="coverage-card">
                    <div class="coverage-icon">🧬</div>
                    <h3>Genetic-Based Pricing</h3>
                    <p>Unique advantage: leverage genetic health data for superior premium rates on healthy animals</p>
                    <ul class="coverage-features">
                        <li>EquiGenix integration</li>
                        <li>Risk profile analysis</li>
                        <li>Personalized pricing</li>
                        <li>Health optimization</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Advantages Section -->
    <section id="advantages" class="advantages">
        <div class="container">
            <div class="section-header">
                <h2>Why Choose Sire & Shield?</h2>
                <p style="color: rgba(255,255,255,0.9);">We're not just another insurance broker - we're your partner in protecting elite animals with cutting-edge technology</p>
            </div>
            
            <div class="advantages-grid">
                <div class="advantage-item">
                    <div class="advantage-icon">🧬</div>
                    <h3>Genetic Risk Data</h3>
                    <p>Exclusive access to comprehensive genetic profiles through EquiGenix Performance Pro. Better pricing for healthy animals, superior risk assessment, reduced claims.</p>
                </div>
                
                <div class="advantage-item">
                    <div class="advantage-icon">🏇</div>
                    <h3>WEC Presence</h3>
                    <p>Office at World Equestrian Center provides direct access to elite horse owners. Convenient consultations during major events and competitions.</p>
                </div>
                
                <div class="advantage-item">
                    <div class="advantage-icon">🔗</div>
                    <h3>Integrated Ecosystem</h3>
                    <p>Part of Ocala Innovation Partners with genetic testing, nutrition, and wellness services. Complete solution for elite animal care.</p>
                </div>
                
                <div class="advantage-item">
                    <div class="advantage-icon">💰</div>
                    <h3>Better Pricing</h3>
                    <p>Genetic data enables 15-30% premium discounts for healthy animals. Exclusive carrier programs you can't get elsewhere.</p>
                </div>
                
                <div class="advantage-item">
                    <div class="advantage-icon">🎯</div>
                    <h3>Specialist Focus</h3>
                    <p>Elite animals only - we understand high-value horses and dogs. Deep expertise in racing, showing, and breeding insurance.</p>
                </div>
                
                <div class="advantage-item">
                    <div class="advantage-icon">🤝</div>
                    <h3>Claims Advocacy</h3>
                    <p>We fight for you during claims. Fast processing, maximum payouts, expert guidance through difficult situations.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Process Section -->
    <section id="process" class="section section-light">
        <div class="container">
            <div class="section-header">
                <h2>Simple Insurance Process</h2>
                <p>From consultation to coverage in 5 easy steps</p>
            </div>
            
            <div class="process-steps">
                <div class="process-step">
                    <div class="step-number">1</div>
                    <h3>Free Consultation</h3>
                    <p>Discuss your needs, review animal value and genetic profile if available</p>
                </div>
                
                <div class="process-step">
                    <div class="step-number">2</div>
                    <h3>Get Quotes</h3>
                    <p>We shop 5-8 carriers to find best rates and coverage for your situation</p>
                </div>
                
                <div class="process-step">
                    <div class="step-number">3</div>
                    <h3>Application</h3>
                    <p>Complete simple application, coordinate veterinary exam if needed</p>
                </div>
                
                <div class="process-step">
                    <div class="step-number">4</div>
                    <h3>Underwriting</h3>
                    <p>Submit to carrier with genetic data supporting favorable risk profile</p>
                </div>
                
                <div class="process-step">
                    <div class="step-number">5</div>
                    <h3>Coverage Active</h3>
                    <p>Policy bound, protection in place, ongoing service and support provided</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Testimonials -->
    <section class="testimonials">
        <div class="container">
            <div class="section-header">
                <h2>What Our Clients Say</h2>
                <p>Trusted by elite horse owners and breeders throughout Ocala</p>
            </div>
            
            <div class="testimonial-grid">
                <div class="testimonial">
                    <p class="testimonial-text">"Sire & Shield saved me $12,000 annually on mortality coverage by using my horse's genetic data. The genetic screening showed low disease risk, and they negotiated amazing rates with the carrier."</p>
                    <p class="testimonial-author">Sarah Johnson</p>
                    <p class="testimonial-role">Racing Stable Owner, Ocala</p>
                </div>
                
                <div class="testimonial">
                    <p class="testimonial-text">"When my stallion needed emergency colic surgery, Sire & Shield handled everything. They got the claim approved in 48 hours and ensured I received maximum coverage. Outstanding service."</p>
                    <p class="testimonial-author">Michael Chen</p>
                    <p class="testimonial-role">Thoroughbred Breeder</p>
                </div>
                
                <div class="testimonial">
                    <p class="testimonial-text">"As a trainer with 45 horses, insurance is critical. Sire & Shield provides comprehensive coverage for my entire operation at competitive rates. Their genetic-based approach is revolutionary."</p>
                    <p class="testimonial-author">Jennifer Martinez</p>
                    <p class="testimonial-role">Professional Trainer, WEC</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section id="contact" class="cta-section">
        <div class="container">
            <h2>Protect Your Investment Today</h2>
            <p>Get a free consultation and quote from our insurance specialists. Discover how genetic data can save you 15-30% on premiums.</p>
            
            <div class="cta-buttons">
                <a href="#" class="btn-primary">Get Free Quote</a>
                <a href="#" class="btn-secondary">Schedule Consultation</a>
            </div>
            
            <div style="margin-top: 50px; font-size: 18px;">
                <p><strong>Visit Our Office:</strong></p>
                <p>World Equestrian Center<br>
                Ocala, Florida</p>
                <p style="margin-top: 20px;"><strong>Contact:</strong></p>
                <p>[Phone] | [Email]</p>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>About Sire & Shield</h3>
                <p style="color: rgba(255,255,255,0.8);">Specialty insurance brokerage serving elite horse and dog owners with genetic data-powered risk assessment and superior coverage options.</p>
            </div>
            
            <div class="footer-section">
                <h3>Coverage Options</h3>
                <ul>
                    <li><a href="#coverage">Equine Mortality</a></li>
                    <li><a href="#coverage">Loss of Use</a></li>
                    <li><a href="#coverage">Major Medical</a></li>
                    <li><a href="#coverage">Liability Insurance</a></li>
                    <li><a href="#coverage">Canine Performance</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Resources</h3>
                <ul>
                    <li><a href="#">Insurance Guide</a></li>
                    <li><a href="#">Claims Process</a></li>
                    <li><a href="#">FAQ</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Genetic Testing Info</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Ocala Innovation Partners</h3>
                <ul>
                    <li><a href="#">EquiGenix Performance Pro</a></li>
                    <li><a href="#">Pinnacle Equine</a></li>
                    <li><a href="#">Horse Capital Nutrition</a></li>
                    <li><a href="#">Ocala Elite Experiences</a></li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2025 Sire & Shield | A Division of Ocala Innovation Partners</p>
            <p style="margin-top: 10px; font-size: 12px;">Licensed Insurance Broker | All Rights Reserved | Privacy Policy | Terms of Service</p>
        </div>
    </footer>
</body>
</html>
