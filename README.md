<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free online tool to extract and download YouTube videos in various formats and qualities. Fast, secure, and easy to use YouTube video extractor.">
    <meta name="keywords" content="YouTube extractor, video downloader, YouTube downloader, MP4 downloader, video converter">
    <meta name="author" content="YouTube Video Extractor">
    <meta name="robots" content="index, follow">
    <title>YouTube Video Extractor - Download Videos in HD Quality</title>
    <link rel="canonical" href="https://yourwebsite.com" />
    
    <!-- Open Graph / Social Media Meta Tags -->
    <meta property="og:title" content="YouTube Video Extractor">
    <meta property="og:description" content="Free online tool to extract and download YouTube videos in various formats and qualities.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://yourwebsite.com">
    <meta property="og:image" content="https://yourwebsite.com/images/thumbnail.jpg">
    
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    
    <!-- Structured Data -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebApplication",
      "name": "YouTube Video Extractor",
      "url": "https://yourwebsite.com",
      "description": "Free online tool to extract and download YouTube videos in various formats and qualities.",
      "applicationCategory": "UtilityApplication",
      "operatingSystem": "Web"
    }
    </script>
    
    <style>
        :root {
            --primary-color: #ff0000;
            --secondary-color: #282828;
            --accent-color: #606060;
            --light-color: #f9f9f9;
            --dark-color: #212121;
            --success-color: #4CAF50;
            --warning-color: #FFC107;
            --error-color: #F44336;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', Arial, sans-serif;
        }
        
        body {
            background-color: var(--light-color);
            color: var(--dark-color);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .logo img {
            height: 40px;
            margin-right: 10px;
        }
        
        .logo h1 {
            color: var(--primary-color);
            font-size: 1.5rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--primary-color);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--dark-color);
        }
        
        .hero {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 60px 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        .main-content {
            padding: 40px 0;
        }
        
        .extractor-box {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            padding: 30px;
            margin-bottom: 30px;
        }
        
        .extractor-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            border-bottom: 1px solid #eee;
            padding-bottom: 15px;
        }
        
        .extractor-header h3 {
            font-size: 1.5rem;
            color: var(--primary-color);
        }
        
        .extractor-form {
            display: flex;
            flex-direction: column;
        }
        
        .url-input-group {
            display: flex;
            margin-bottom: 20px;
        }
        
        .url-input {
            flex: 1;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: 4px 0 0 4px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .url-input:focus {
            outline: none;
            border-color: var(--primary-color);
        }
        
        .submit-btn {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: #cc0000;
        }
        
        .options-group {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .option-select {
            flex: 1;
            min-width: 200px;
            padding: 10px;
            border: 2px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        .result-container {
            display: none;
            margin-top: 30px;
            animation: fadeIn 0.5s;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .video-preview {
            width: 100%;
            margin-bottom: 20px;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }
        
        .download-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .download-card {
            background-color: white;
            border: 1px solid #eee;
            border-radius: 8px;
            padding: 15px;
            display: flex;
            flex-direction: column;
        }
        
        .download-card-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .download-quality {
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .download-size {
            color: var(--accent-color);
            font-size: 0.9rem;
        }
        
        .download-btn {
            background-color: var(--success-color);
            color: white;
            border: none;
            padding: 10px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            margin-top: auto;
            transition: background-color 0.3s;
        }
        
        .download-btn:hover {
            background-color: #3d8b40;
        }
        
        .ad-container {
            margin: 30px 0;
            text-align: center;
            background-color: #f5f5f5;
            padding: 20px;
            border-radius: 8px;
        }
        
        .ad-label {
            display: block;
            font-size: 0.8rem;
            color: var(--accent-color);
            margin-bottom: 5px;
            text-transform: uppercase;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 8px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .feature-card h3 {
            margin-bottom: 10px;
            color: var(--dark-color);
        }
        
        .feature-card p {
            color: var(--accent-color);
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 40px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            color: white;
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #aaa;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }
        
        .loading {
            display: none;
            text-align: center;
            margin: 20px 0;
        }
        
        .spinner {
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-radius: 50%;
            border-top: 4px solid var(--primary-color);
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
            margin: 0 auto 10px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .error-message {
            color: var(--error-color);
            margin-top: 10px;
            display: none;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 15px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .url-input-group {
                flex-direction: column;
            }
            
            .url-input {
                border-radius: 4px;
                margin-bottom: 10px;
            }
            
            .submit-btn {
                border-radius: 4px;
                width: 100%;
            }
            
            .download-options {
                grid-template-columns: 1fr;
            }
            
            .mobile-menu-btn {
                display: block;
                position: absolute;
                top: 15px;
                right: 15px;
            }
            
            nav {
                display: none;
                width: 100%;
                margin-top: 15px;
            }
            
            nav.active {
                display: block;
            }
            
            nav ul {
                flex-direction: column;
            }
            
            nav ul li {
                margin: 5px 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <a href="#" class="logo">
                <img src="https://via.placeholder.com/40" alt="YouTube Extractor Logo">
                <h1>YouTube Extractor</h1>
            </a>
            <button class="mobile-menu-btn">☰</button>
            <nav id="main-nav">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">How It Works</a></li>
                    <li><a href="#">Features</a></li>
                    <li><a href="#">FAQ</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <h2>Download YouTube Videos in HD Quality</h2>
            <p>Extract and save YouTube videos in MP4, WebM, 3GP and other formats. Fast, free and easy to use!</p>
        </div>
    </section>
    
    <div class="container">
        <div class="ad-container">
            <span class="ad-label">Advertisement</span>
            <!-- Replace with your AdSense code -->
            <div id="ad-top">
                <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID"
                     crossorigin="anonymous"></script>
                <!-- Responsive Ad Unit -->
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="ca-pub-YOUR_PUBLISHER_ID"
                     data-ad-slot="YOUR_AD_SLOT_ID"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
        </div>
    </div>
    
    <section class="main-content">
        <div class="container">
            <div class="extractor-box">
                <div class="extractor-header">
                    <h3>YouTube Video Extractor</h3>
                    <div class="extractor-version">v2.5</div>
                </div>
                
                <form class="extractor-form" id="extractorForm">
                    <div class="url-input-group">
                        <input type="text" class="url-input" id="videoUrl" placeholder="Paste YouTube video URL here..." required>
                        <button type="submit" class="submit-btn">Extract Video</button>
                    </div>
                    
                    <div class="options-group">
                        <select class="option-select" id="formatSelect">
                            <option value="all">All Formats</option>
                            <option value="mp4">MP4</option>
                            <option value="webm">WebM</option>
                            <option value="3gp">3GP</option>
                            <option value="audio">Audio Only</option>
                        </select>
                        
                        <select class="option-select" id="qualitySelect">
                            <option value="all">All Qualities</option>
                            <option value="hd">HD (720p-4K)</option>
                            <option value="sd">SD (480p)</option>
                            <option value="low">Low (144p-360p)</option>
                        </select>
                    </div>
                    
                    <div class="error-message" id="errorMessage">
                        Please enter a valid YouTube video URL
                    </div>
                </form>
                
                <div class="loading" id="loadingIndicator">
                    <div class="spinner"></div>
                    <p>Extracting video information...</p>
                </div>
                
                <div class="result-container" id="resultContainer">
                    <h3>Extracted Video</h3>
                    <div class="video-preview" id="videoPreview">
                        <!-- Video preview will be inserted here -->
                    </div>
                    
                    <h4>Download Options</h4>
                    <div class="download-options" id="downloadOptions">
                        <!-- Download options will be inserted here -->
                    </div>
                </div>
            </div>
            
            <div class="ad-container">
                <span class="ad-label">Advertisement</span>
                <!-- Replace with your AdSense code -->
                <div id="ad-middle">
                    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID"
                         crossorigin="anonymous"></script>
                    <!-- Responsive Ad Unit -->
                    <ins class="adsbygoogle"
                         style="display:block"
                         data-ad-client="ca-pub-YOUR_PUBLISHER_ID"
                         data-ad-slot="YOUR_AD_SLOT_ID"
                         data-ad-format="auto"
                         data-full-width-responsive="true"></ins>
                    <script>
                         (adsbygoogle = window.adsbygoogle || []).push({});
                    </script>
                </div>
            </div>
            
            <div class="features">
                <div class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3>Fast Extraction</h3>
                    <p>Our powerful servers extract YouTube videos in seconds, saving you time and bandwidth.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🔒</div>
                    <h3>Secure & Private</h3>
                    <p>We don't store your videos or track your downloads. Your privacy is our priority.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">📱</div>
                    <h3>All Devices Supported</h3>
                    <p>Download videos compatible with smartphones, tablets, computers and smart TVs.</p>
                </div>
            </div>
        </div>
    </section>
    
    <div class="container">
        <div class="ad-container">
            <span class="ad-label">Advertisement</span>
            <!-- Replace with your AdSense code -->
            <div id="ad-bottom">
                <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID"
                     crossorigin="anonymous"></script>
                <!-- Responsive Ad Unit -->
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="ca-pub-YOUR_PUBLISHER_ID"
                     data-ad-slot="YOUR_AD_SLOT_ID"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
        </div>
    </div>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>YouTube Extractor</h3>
                    <ul>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">How It Works</a></li>
                        <li><a href="#">Features</a></li>
                        <li><a href="#">Testimonials</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Help & Support</h3>
                    <ul>
                        <li><a href="#">FAQ</a></li>
                        <li><a href="#">Contact Us</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Tutorials</a></li>
                        <li><a href="#">Video Guides</a></li>
                        <li><a href="#">API Documentation</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Connect With Us</h3>
                    <ul>
                        <li><a href="#">Facebook</a></li>
                        <li><a href="#">Twitter</a></li>
                        <li><a href="#">Instagram</a></li>
                        <li><a href="#">YouTube</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 YouTube Video Extractor. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Mobile menu toggle
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            document.getElementById('main-nav').classList.toggle('active');
        });
        
        // Form submission handler
        document.getElementById('extractorForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const videoUrl = document.getElementById('videoUrl').value.trim();
            const formatSelect = document.getElementById('formatSelect').value;
            const qualitySelect = document.getElementById('qualitySelect').value;
            const errorMessage = document.getElementById('errorMessage');
            const loadingIndicator = document.getElementById('loadingIndicator');
            const resultContainer = document.getElementById('resultContainer');
            
            // Validate URL
            if (!isValidYouTubeUrl(videoUrl)) {
                errorMessage.style.display = 'block';
                return;
            }
            
            errorMessage.style.display = 'none';
            loadingIndicator.style.display = 'block';
            resultContainer.style.display = 'none';
            
            // Simulate API call (in a real app, you would call your backend here)
            setTimeout(() => {
                extractVideoInfo(videoUrl, formatSelect, qualitySelect);
                loadingIndicator.style.display = 'none';
                resultContainer.style.display = 'block';
                
                // Scroll to results
                resultContainer.scrollIntoView({ behavior: 'smooth' });
            }, 1500);
        });
        
        function isValidYouTubeUrl(url) {
            const pattern = /^(https?:\/\/)?(www\.)?(youtube\.com|youtu\.?be)\/.+$/;
            return pattern.test(url);
        }
        
        function extractVideoInfo(url, format, quality) {
            // This is a simulation - in a real app, you would call your backend API
            const videoId = extractVideoId(url);
            const videoPreview = document.getElementById('videoPreview');
            const downloadOptions = document.getElementById('downloadOptions');
            
            // Set video preview
            videoPreview.innerHTML = `
                <iframe width="100%" height="450" src="https://www.youtube.com/embed/${videoId}" 
                frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                allowfullscreen></iframe>
            `;
            
            // Generate download options based on selected filters
            let optionsHTML = '';
            const allOptions = [
                { format: 'MP4', quality: '4K', size: '120MB', url: '#' },
                { format: 'MP4', quality: '1080p', size: '85MB', url: '#' },
                { format: 'MP4', quality: '720p', size: '45MB', url: '#' },
                { format: 'MP4', quality: '480p', size: '25MB', url: '#' },
                { format: 'MP4', quality: '360p', size: '15MB', url: '#' },
                { format: 'WebM', quality: '1080p', size: '75MB', url: '#' },
                { format: 'WebM', quality: '720p', size: '40MB', url: '#' },
                { format: 'MP3', quality: '128kbps', size: '5MB', url: '#' },
                { format: 'MP3', quality: '320kbps', size: '12MB', url: '#' },
                { format: '3GP', quality: '144p', size: '8MB', url: '#' }
            ];
            
            // Filter options based on user selection
            const filteredOptions = allOptions.filter(option => {
                if (format === 'all' && quality === 'all') return true;
                
                let formatMatch = true;
                let qualityMatch = true;
                
                if (format !== 'all') {
                    if (format === 'mp4') formatMatch = option.format === 'MP4';
                    if (format === 'webm') formatMatch = option.format === 'WebM';
                    if (format === '3gp') formatMatch = option.format === '3GP';
                    if (format === 'audio') formatMatch = option.format === 'MP3';
                }
                
                if (quality !== 'all') {
                    if (quality === 'hd') {
                        qualityMatch = option.quality.includes('4K') || 
                                      option.quality.includes('1080p') || 
                                      option.quality.includes('720p');
                    }
                    if (quality === 'sd') {
                        qualityMatch = option.quality.includes('480p');
                    }
                    if (quality === 'low') {
                        qualityMatch = option.quality.includes('360p') || 
                                      option.quality.includes('144p');
                    }
                }
                
                return formatMatch && qualityMatch;
            });
            
            // Generate HTML for filtered options
            filteredOptions.forEach(option => {
                optionsHTML += `
                    <div class="download-card">
                        <div class="download-card-header">
                            <span class="download-quality">${option.format} • ${option.quality}</span>
                            <span class="download-size">${option.size}</span>
                        </div>
                        <button class="download-btn" data-url="${option.url}">Download</button>
                    </div>
                `;
            });
            
            downloadOptions.innerHTML = optionsHTML;
            
            // Add click handlers to download buttons
            document.querySelectorAll('.download-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const downloadUrl = this.getAttribute('data-url');
                    // In a real app, this would initiate the download
                    alert('Download would start for: ' + downloadUrl);
                });
            });
        }
        
        function extractVideoId(url) {
            // Extract YouTube video ID from URL
            const regExp = /^.*(youtu.be\/|v\/|u\/\w\/|embed\/|watch\?v=|&v=)([^#&?]*).*/;
            const match = url.match(regExp);
            return (match && match[2].length === 11) ? match[2] : 'dQw4w9WgXcQ'; // Default to Rick Astley if invalid
        }
        
        // Initialize AdSense ads
        function initAds() {
            // This would be handled by the AdSense script automatically
            // Included here just as a placeholder for real implementation
            console.log('AdSense ads initialized');
        }
        
        // Initialize the app
        window.addEventListener('DOMContentLoaded', function() {
            initAds();
        });
    </script>
</body>
</html>
