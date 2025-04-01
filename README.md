<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Compress images online for free. Reduce JPG, PNG, WebP file size without losing quality. Fast, secure, and browser-based.">
    <title>ImageCompress | Free Online Image Compression Tool</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_ADSENSE_ID" crossorigin="anonymous"></script>
    <style>
        :root {
            --primary: #4361ee;
            --primary-light: #eef2ff;
            --secondary: #3a0ca3;
            --accent: #f72585;
            --dark: #1a1a2e;
            --light: #f8f9fa;
            --gray: #6c757d;
            --border: #e9ecef;
            --success: #4cc9f0;
            --shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
            --radius: 12px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }

        /* Header */
        header {
            background: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .logo i {
            color: var(--accent);
        }

        /* Navigation */
        nav ul {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }

        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
            padding: 0.5rem 0;
            position: relative;
        }

        nav a:hover {
            color: var(--primary);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }

        nav a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--dark);
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 4rem 0 3rem;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto 2rem;
        }

        /* Main Tool Container */
        .tool-container {
            background: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            padding: 2.5rem;
            margin-bottom: 3rem;
            position: relative;
            overflow: hidden;
        }

        .tool-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 6px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
        }

        .tool-header {
            text-align: center;
            margin-bottom: 2.5rem;
        }

        .tool-header h2 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .tool-header p {
            color: var(--gray);
        }

        /* Upload Area */
        .upload-area {
            border: 2px dashed var(--border);
            border-radius: var(--radius);
            padding: 3rem 1rem;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            margin-bottom: 2rem;
            background: var(--primary-light);
            position: relative;
        }

        .upload-area:hover {
            border-color: var(--primary);
            background: rgba(67, 97, 238, 0.05);
        }

        .upload-area.active {
            border-color: var(--success);
            background: rgba(76, 201, 240, 0.05);
        }

        .upload-area i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1rem;
            transition: var(--transition);
        }

        .upload-area:hover i {
            transform: translateY(-5px);
        }

        .upload-area p {
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .upload-area span {
            font-size: 0.9rem;
            color: var(--gray);
        }

        #file-input {
            display: none;
        }

        /* Controls */
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .control-group {
            flex: 1;
            min-width: 280px;
        }

        .control-group h3 {
            margin-bottom: 1rem;
            font-size: 1.1rem;
            color: var(--dark);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .control-group h3 i {
            color: var(--primary);
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        input[type="range"] {
            flex: 1;
            height: 8px;
            border-radius: 4px;
            background: #ddd;
            outline: none;
            -webkit-appearance: none;
            transition: var(--transition);
        }

        input[type="range"]:hover {
            background: #ccc;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: var(--primary);
            cursor: pointer;
            transition: var(--transition);
        }

        input[type="range"]::-webkit-slider-thumb:hover {
            transform: scale(1.2);
        }

        .slider-value {
            width: 50px;
            text-align: center;
            font-weight: bold;
            color: var(--primary);
        }

        /* Format Options */
        .format-options {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }

        .format-option {
            padding: 0.6rem 1.2rem;
            border: 1px solid var(--border);
            border-radius: 6px;
            cursor: pointer;
            transition: var(--transition);
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .format-option:hover {
            border-color: var(--primary);
            color: var(--primary);
        }

        .format-option.selected {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        /* Buttons */
        .btn {
            padding: 0.9rem 1.8rem;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .btn i {
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
            box-shadow: 0 4px 14px rgba(67, 97, 238, 0.3);
        }

        .btn-primary:hover {
            background: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(67, 97, 238, 0.4);
        }

        .btn-secondary {
            background: white;
            color: var(--primary);
            border: 1px solid var(--border);
        }

        .btn-secondary:hover {
            background: var(--primary-light);
            border-color: var(--primary);
        }

        .action-buttons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }

        /* Results Section */
        .results {
            display: none;
            margin-top: 2rem;
            animation: fadeIn 0.5s;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .comparison {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .image-box {
            flex: 1;
            min-width: 300px;
            background: white;
            border-radius: var(--radius);
            padding: 1.5rem;
            box-shadow: var(--shadow);
        }

        .image-box h4 {
            margin-bottom: 1rem;
            font-size: 1.2rem;
            color: var(--dark);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .image-box h4 i {
            color: var(--primary);
        }

        .image-box img {
            width: 100%;
            height: auto;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
        }

        .image-box img:hover {
            transform: scale(1.02);
        }

        .image-info {
            background: var(--primary-light);
            padding: 1rem;
            border-radius: 8px;
            margin-bottom: 1rem;
        }

        .image-info p {
            margin-bottom: 0.5rem;
            font-size: 0.95rem;
        }

        .download-btn {
            width: 100%;
        }

        /* Stats */
        .stats {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .stat-item {
            background: white;
            padding: 1.5rem;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            text-align: center;
            min-width: 160px;
            transition: var(--transition);
        }

        .stat-item:hover {
            transform: translateY(-5px);
        }

        .stat-item .value {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .stat-item .label {
            font-size: 0.9rem;
            color: var(--gray);
        }

        /* Loading Spinner */
        .spinner {
            display: none;
            width: 50px;
            height: 50px;
            margin: 2rem auto;
            border: 5px solid rgba(0, 0, 0, 0.1);
            border-radius: 50%;
            border-top-color: var(--primary);
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Ad Containers */
        .ad-container {
            margin: 3rem 0;
            text-align: center;
            padding: 1.5rem;
            background: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        .ad-label {
            font-size: 0.8rem;
            color: var(--gray);
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Features Section */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 4rem 0;
        }

        .section-title {
            grid-column: 1 / -1;
            text-align: center;
            margin-bottom: 1rem;
            font-size: 2rem;
            color: var(--dark);
        }

        .section-subtitle {
            grid-column: 1 / -1;
            text-align: center;
            margin-bottom: 2rem;
            color: var(--gray);
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .feature-card {
            background: white;
            border-radius: var(--radius);
            padding: 2rem;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .feature-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            background: var(--primary-light);
            width: 70px;
            height: 70px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }

        .feature-card h3 {
            margin-bottom: 1rem;
            font-size: 1.3rem;
            color: var(--dark);
        }

        .feature-card p {
            color: var(--gray);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 4rem 0 2rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            color: white;
            position: relative;
            padding-bottom: 0.8rem;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--primary);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 0.8rem;
        }

        .footer-column ul li a {
            color: #adb5bd;
            text-decoration: none;
            transition: var(--transition);
            display: inline-block;
        }

        .footer-column ul li a:hover {
            color: white;
            transform: translateX(5px);
        }

        .footer-column p {
            color: #adb5bd;
            margin-bottom: 1.5rem;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            color: white;
            background: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #adb5bd;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .tool-container {
                padding: 2rem;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                justify-content: center;
                flex-wrap: wrap;
            }
            
            .hero {
                padding: 3rem 0 2rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .tool-header h2 {
                font-size: 1.6rem;
            }
            
            .comparison {
                flex-direction: column;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
            }
        }

        @media (max-width: 576px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav {
                display: none;
                width: 100%;
                margin-top: 1rem;
            }
            
            nav.active {
                display: block;
            }
            
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
                text-align: center;
            }
            
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .tool-container {
                padding: 1.5rem;
            }
            
            .controls {
                flex-direction: column;
                gap: 1.5rem;
            }
            
            .format-options {
                justify-content: center;
            }
            
            .stat-item {
                min-width: 120px;
                padding: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <a href="#" class="logo">
                <i class="fas fa-compress-alt"></i>
                ImageCompress
            </a>
            <button class="mobile-menu-btn" id="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
            <nav id="main-nav">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Features</a></li>
                    <li><a href="#">How It Works</a></li>
                    <li><a href="#">FAQ</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container">
        <!-- Hero Section -->
        <section class="hero">
            <h1>Optimize Your Images in Seconds</h1>
            <p>Reduce file size without sacrificing quality. Perfect for websites, social media, and storage.</p>
        </section>

        <!-- Ad Container -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_ADSENSE_ID"
                 data-ad-slot="YOUR_AD_SLOT_ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>

        <!-- Compression Tool -->
        <section class="tool-container">
            <div class="tool-header">
                <h2>Image Compression Tool</h2>
                <p>Upload your image and adjust settings for optimal results</p>
            </div>

            <!-- Upload Area -->
            <div class="upload-area" id="upload-area">
                <i class="fas fa-cloud-upload-alt"></i>
                <p>Drag & drop your image here</p>
                <span>or click to browse files (JPG, PNG, WebP - Max 10MB)</span>
                <input type="file" id="file-input" accept="image/jpeg, image/png, image/webp">
            </div>

            <!-- Controls -->
            <div class="controls">
                <div class="control-group">
                    <h3><i class="fas fa-sliders-h"></i> Compression Level</h3>
                    <div class="slider-container">
                        <input type="range" id="compression-slider" min="0" max="100" value="70">
                        <span class="slider-value" id="compression-value">70%</span>
                    </div>
                </div>

                <div class="control-group">
                    <h3><i class="fas fa-file-image"></i> Output Format</h3>
                    <div class="format-options">
                        <div class="format-option selected" data-format="original">
                            <i class="fas fa-file"></i> Original
                        </div>
                        <div class="format-option" data-format="jpeg">
                            <i class="fas fa-file-image"></i> JPG
                        </div>
                        <div class="format-option" data-format="png">
                            <i class="fas fa-file-image"></i> PNG
                        </div>
                        <div class="format-option" data-format="webp">
                            <i class="fas fa-file-image"></i> WebP
                        </div>
                    </div>
                </div>
            </div>

            <!-- Action Buttons -->
            <div class="action-buttons">
                <button class="btn btn-primary" id="compress-btn" disabled>
                    <i class="fas fa-compress-alt"></i> Compress Image
                </button>
                <button class="btn btn-secondary" id="reset-btn">
                    <i class="fas fa-redo"></i> Reset
                </button>
            </div>

            <!-- Loading Spinner -->
            <div class="spinner" id="loading-spinner"></div>

            <!-- Results Section -->
            <div class="results" id="results">
                <h3 style="text-align: center; margin-bottom: 2rem;">Compression Results</h3>
                
                <div class="comparison">
                    <div class="image-box">
                        <h4><i class="fas fa-image"></i> Original Image</h4>
                        <img id="original-image" src="" alt="Original image">
                        <div class="image-info">
                            <p id="original-size"><i class="fas fa-weight-hanging"></i> Size: 0 KB</p>
                            <p id="original-dimensions"><i class="fas fa-ruler-combined"></i> Dimensions: 0 × 0 px</p>
                        </div>
                    </div>
                    
                    <div class="image-box">
                        <h4><i class="fas fa-compress-alt"></i> Compressed Image</h4>
                        <img id="compressed-image" src="" alt="Compressed image">
                        <div class="image-info">
                            <p id="compressed-size"><i class="fas fa-weight-hanging"></i> Size: 0 KB</p>
                            <p id="compressed-dimensions"><i class="fas fa-ruler-combined"></i> Dimensions: 0 × 0 px</p>
                        </div>
                        <button class="btn btn-primary download-btn" id="download-btn">
                            <i class="fas fa-download"></i> Download
                        </button>
                    </div>
                </div>

                <!-- Stats -->
                <div class="stats">
                    <div class="stat-item">
                        <div class="value" id="savings-percent">0%</div>
                        <div class="label">Size Reduced</div>
                    </div>
                    <div class="stat-item">
                        <div class="value" id="savings-kb">0 KB</div>
                        <div class="label">File Savings</div>
                    </div>
                    <div class="stat-item">
                        <div class="value" id="quality-retained">100%</div>
                        <div class="label">Quality Retained</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Ad Container -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_ADSENSE_ID"
                 data-ad-slot="YOUR_AD_SLOT_ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>

        <!-- Features Section -->
        <section class="features">
            <h2 class="section-title">Why Choose Our Image Compressor?</h2>
            <p class="section-subtitle">We provide the fastest and most efficient way to optimize your images without compromising quality</p>
            
            <div class="feature-card">
                <i class="fas fa-bolt"></i>
                <h3>Lightning Fast</h3>
                <p>Compress images in seconds with our optimized browser-based engine.</p>
            </div>
            
            <div class="feature-card">
                <i class="fas fa-lock"></i>
                <h3>100% Private</h3>
                <p>Your images never leave your device. No uploads, no server processing.</p>
            </div>
            
            <div class="feature-card">
                <i class="fas fa-chart-line"></i>
                <h3>Smart Optimization</h3>
                <p>Advanced algorithms maximize quality while minimizing file size.</p>
            </div>
        </section>

        <!-- Ad Container -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_ADSENSE_ID"
                 data-ad-slot="YOUR_AD_SLOT_ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>ImageCompress</h3>
                    <p>Free online tool to optimize your images for web and mobile.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Features</a></li>
                        <li><a href="#">How It Works</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#">Image Optimization Guide</a></li>
                        <li><a href="#">Web Performance Tips</a></li>
                        <li><a href="#">File Format Comparison</a></li>
                        <li><a href="#">API Documentation</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Company</h3>
                    <ul>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Contact</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; <span id="current-year"></span> ImageCompress. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Mobile Menu Toggle
        document.getElementById('mobile-menu-btn').addEventListener('click', function() {
            document.getElementById('main-nav').classList.toggle('active');
        });

        // Set Current Year in Footer
        document.getElementById('current-year').textContent = new Date().getFullYear();

        // Compression Slider
        const compressionSlider = document.getElementById('compression-slider');
        const compressionValue = document.getElementById('compression-value');
        
        compressionSlider.addEventListener('input', function() {
            compressionValue.textContent = this.value + '%';
        });

        // Format Selection
        const formatOptions = document.querySelectorAll('.format-option');
        formatOptions.forEach(option => {
            option.addEventListener('click', function() {
                formatOptions.forEach(opt => opt.classList.remove('selected'));
                this.classList.add('selected');
            });
        });

        // File Upload Handling
        const uploadArea = document.getElementById('upload-area');
        const fileInput = document.getElementById('file-input');
        const compressBtn = document.getElementById('compress-btn');
        const resetBtn = document.getElementById('reset-btn');
        const resultsSection = document.getElementById('results');
        const loadingSpinner = document.getElementById('loading-spinner');
        
        let selectedFile = null;
        let originalImageData = null;
        let compressedImageData = null;

        // Drag and Drop
        ['dragover', 'dragenter'].forEach(event => {
            uploadArea.addEventListener(event, (e) => {
                e.preventDefault();
                uploadArea.classList.add('active');
            });
        });

        ['dragleave', 'dragend'].forEach(event => {
            uploadArea.addEventListener(event, () => {
                uploadArea.classList.remove('active');
            });
        });

        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.classList.remove('active');
            
            if (e.dataTransfer.files.length) {
                handleFileSelection(e.dataTransfer.files[0]);
            }
        });

        uploadArea.addEventListener('click', () => {
            fileInput.click();
        });

        fileInput.addEventListener('change', () => {
            if (fileInput.files.length) {
                handleFileSelection(fileInput.files[0]);
            }
        });

        // Handle Selected File
        function handleFileSelection(file) {
            // Validate file type
            const validTypes = ['image/jpeg', 'image/png', 'image/webp'];
            if (!validTypes.includes(file.type)) {
                alert('Please upload a JPG, PNG, or WebP image.');
                return;
            }
            
            // Validate file size (10MB max)
            if (file.size > 10 * 1024 * 1024) {
                alert('File size exceeds 10MB limit.');
                return;
            }
            
            selectedFile = file;
            compressBtn.disabled = false;
            
            // Update UI
            uploadArea.querySelector('p').textContent = file.name;
            uploadArea.querySelector('span').textContent = formatFileSize(file.size);
            
            // Preview original image
            const reader = new FileReader();
            reader.onload = function(e) {
                const img = new Image();
                img.onload = function() {
                    document.getElementById('original-image').src = e.target.result;
                    document.getElementById('original-dimensions').textContent = 
                        `Dimensions: ${img.width} × ${img.height} px`;
                    originalImageData = {
                        src: e.target.result,
                        width: img.width,
                        height: img.height,
                        size: file.size
                    };
                    document.getElementById('original-size').textContent = 
                        `Size: ${formatFileSize(file.size)}`;
                };
                img.src = e.target.result;
            };
            reader.readAsDataURL(file);
        }

        // Compress Image
        compressBtn.addEventListener('click', function() {
            if (!selectedFile) return;
            
            // Show loading spinner
            loadingSpinner.style.display = 'block';
            resultsSection.style.display = 'none';
            
            // Get selected format
            const selectedFormat = document.querySelector('.format-option.selected').dataset.format;
            const format = selectedFormat === 'original' ? selectedFile.type.split('/')[1] : selectedFormat;
            
            // Get quality (0-1)
            const quality = 1 - (compressionSlider.value / 100);
            
            // Simulate compression delay
            setTimeout(() => {
                compressImage(selectedFile, quality, format);
                loadingSpinner.style.display = 'none';
            }, 800);
        });

        // Image Compression Logic
        function compressImage(file, quality, format) {
            const reader = new FileReader();
            reader.onload = function(e) {
                const img = new Image();
                img.onload = function() {
                    // Create canvas
                    const canvas = document.createElement('canvas');
                    const ctx = canvas.getContext('2d');
                    canvas.width = img.width;
                    canvas.height = img.height;
                    ctx.drawImage(img, 0, 0);
                    
                    // Determine MIME type
                    let mimeType;
                    switch (format) {
                        case 'jpeg': mimeType = 'image/jpeg'; break;
                        case 'png': mimeType = 'image/png'; break;
                        case 'webp': mimeType = 'image/webp'; break;
                        default: mimeType = file.type;
                    }
                    
                    // Convert to data URL with quality
                    const compressedDataURL = canvas.toDataURL(mimeType, quality);
                    const compressedSize = Math.round(compressedDataURL.length * 0.75); // Approximate size
                    
                    // Display compressed image
                    document.getElementById('compressed-image').src = compressedDataURL;
                    document.getElementById('compressed-dimensions').textContent = 
                        `Dimensions: ${img.width} × ${img.height} px`;
                    document.getElementById('compressed-size').textContent = 
                        `Size: ${formatFileSize(compressedSize)}`;
                    
                    // Calculate savings
                    const savingsPercent = Math.round(((file.size - compressedSize) / file.size) * 100);
                    const savingsKB = Math.round((file.size - compressedSize) / 1024);
                    const qualityRetained = 100 - Math.round(quality * 100);
                    
                    document.getElementById('savings-percent').textContent = savingsPercent + '%';
                    document.getElementById('savings-kb').textContent = savingsKB + ' KB';
                    document.getElementById('quality-retained').textContent = qualityRetained + '%';
                    
                    // Store compressed data for download
                    compressedImageData = {
                        dataURL: compressedDataURL,
                        format: format,
                        size: compressedSize
                    };
                    
                    // Show results
                    resultsSection.style.display = 'block';
                };
                img.src = e.target.result;
            };
            reader.readAsDataURL(file);
        }

        // Download Compressed Image
        document.getElementById('download-btn').addEventListener('click', function() {
            if (!compressedImageData) return;
            
            const link = document.createElement('a');
            link.href = compressedImageData.dataURL;
            link.download = `compressed.${compressedImageData.format}`;
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        });

        // Reset Tool
        resetBtn.addEventListener('click', function() {
            // Reset file input
            fileInput.value = '';
            selectedFile = null;
            originalImageData = null;
            compressedImageData = null;
            
            // Reset UI
            uploadArea.querySelector('p').textContent = 'Drag & drop your image here';
            uploadArea.querySelector('span').textContent = 'or click to browse files (JPG, PNG, WebP - Max 10MB)';
            compressBtn.disabled = true;
            resultsSection.style.display = 'none';
            
            // Reset compression settings
            compressionSlider.value = 70;
            compressionValue.textContent = '70%';
            
            // Reset format selection
            formatOptions.forEach(opt => opt.classList.remove('selected'));
            document.querySelector('.format-option[data-format="original"]').classList.add('selected');
        });

        // Helper: Format File Size
        function formatFileSize(bytes) {
            if (bytes === 0) return '0 Bytes';
            const k = 1024;
            const sizes = ['Bytes', 'KB', 'MB', 'GB'];
            const i = Math.floor(Math.log(bytes) / Math.log(k));
            return parseFloat((bytes / Math.pow(k, i)).toFixed(2) + ' ' + sizes[i];
        }
    </script>
</body>
</html>
