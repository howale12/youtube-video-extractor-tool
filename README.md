<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTube Video Extractor - Download Videos in HD Quality</title>
    <meta name="description" content="Free online tool to extract and download YouTube videos in MP4, WebM, 3GP formats. Fast, secure, and easy to use YouTube video downloader.">
    <meta name="keywords" content="YouTube downloader, video extractor, MP4 download, YouTube to MP3, HD video download">
    <meta name="author" content="YouTube Video Extractor">
    
    <!-- Open Graph / Social Media Meta Tags -->
    <meta property="og:title" content="YouTube Video Extractor">
    <meta property="og:description" content="Free online tool to extract and download YouTube videos in various formats and qualities.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://yourwebsite.com">
    <meta property="og:image" content="https://yourwebsite.com/images/thumbnail.jpg">
    
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary: #FF0000;
            --primary-dark: #CC0000;
            --secondary: #282828;
            --light: #FFFFFF;
            --dark: #212121;
            --gray: #F1F1F1;
            --dark-gray: #606060;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background-color: var(--gray);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background-color: var(--light);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .logo i {
            color: var(--primary);
            font-size: 2rem;
            margin-right: 10px;
        }
        
        .logo h1 {
            color: var(--dark);
            font-size: 1.5rem;
        }
        
        .logo span {
            color: var(--primary);
        }
        
        /* Ad Container Styles */
        .ad-container {
            background-color: #f8f8f8;
            padding: 20px;
            border-radius: 8px;
            margin: 30px 0;
            text-align: center;
            border: 1px dashed #ccc;
        }
        
        .ad-label {
            font-size: 0.8rem;
            color: var(--dark-gray);
            text-transform: uppercase;
            margin-bottom: 5px;
        }
        
        /* Extractor Box */
        .extractor-box {
            background-color: var(--light);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            padding: 30px;
            margin-top: 30px;
        }
        
        .extractor-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }
        
        .extractor-header h2 {
            color: var(--primary);
        }
        
        .extractor-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .input-group {
            display: flex;
        }
        
        .url-input {
            flex: 1;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: 4px 0 0 4px;
            font-size: 1rem;
        }
        
        .url-input:focus {
            outline: none;
            border-color: var(--primary);
        }
        
        .submit-btn {
            background-color: var(--primary);
            color: var(--light);
            border: none;
            padding: 0 25px;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: var(--primary-dark);
        }
        
        .options-group {
            display: flex;
            gap: 15px;
        }
        
        .option-select {
            flex: 1;
            padding: 10px;
            border: 2px solid #ddd;
            border-radius: 4px;
        }
        
        /* Results Section */
        .result-container {
            display: none;
            margin-top: 30px;
            animation: fadeIn 0.5s;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .video-info {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .video-thumbnail {
            width: 200px;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .video-thumbnail img {
            width: 100%;
            height: auto;
        }
        
        .video-details h3 {
            margin-bottom: 10px;
        }
        
        .download-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .download-card {
            background-color: var(--light);
            border: 1px solid #eee;
            border-radius: 8px;
            padding: 15px;
        }
        
        .download-card-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .download-quality {
            font-weight: bold;
            color: var(--primary);
        }
        
        .download-btn {
            display: block;
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 10px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            margin-top: 10px;
            transition: background-color 0.3s;
        }
        
        .download-btn:hover {
            background-color: var(--primary-dark);
        }
        
        /* Loading State */
        .loading {
            display: none;
            text-align: center;
            margin: 20px 0;
        }
        
        .spinner {
            border: 4px solid rgba(0,0,0,0.1);
            border-radius: 50%;
            border-top: 4px solid var(--primary);
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
            margin: 0 auto 10px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .options-group {
                flex-direction: column;
            }
            
            .input-group {
                flex-direction: column;
            }
            
            .url-input {
                border-radius: 4px;
                margin-bottom: 10px;
            }
            
            .submit-btn {
                border-radius: 4px;
                padding: 12px;
            }
            
            .video-info {
                flex-direction: column;
            }
            
            .video-thumbnail {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <a href="#" class="logo">
                <i class="fab fa-youtube"></i>
                <h1>YouTube <span>Extractor</span></h1>
            </a>
        </div>
    </header>
    
    <main class="container">
        <!-- Top Ad Unit -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <!-- Replace with your AdSense code -->
            <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID"
                crossorigin="anonymous"></script>
            <!-- Responsive Ad -->
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
        
        <div class="extractor-box">
            <div class="extractor-header">
                <h2>YouTube Video Extractor</h2>
                <div class="extractor-version">v2.5</div>
            </div>
            
            <form class="extractor-form" id="downloadForm">
                <div class="input-group">
                    <input type="text" class="url-input" id="videoUrl" placeholder="Paste YouTube video URL here..." required>
                    <button type="submit" class="submit-btn">Extract</button>
                </div>
                
                <div class="options-group">
                    <select class="option-select" id="formatSelect">
                        <option value="mp4">MP4 Video</option>
                        <option value="webm">WebM Video</option>
                        <option value="mp3">MP3 Audio</option>
                    </select>
                    
                    <select class="option-select" id="qualitySelect">
                        <option value="high">High Quality</option>
                        <option value="medium">Medium Quality</option>
                        <option value="low">Low Quality</option>
                    </select>
                </div>
                
                <div class="error-message" id="errorMessage"></div>
            </form>
            
            <div class="loading" id="loadingIndicator">
                <div class="spinner"></div>
                <p>Processing video...</p>
            </div>
            
            <div class="result-container" id="resultContainer">
                <div class="video-info" id="videoInfo">
                    <div class="video-thumbnail">
                        <img id="videoThumbnail" src="" alt="Video thumbnail">
                    </div>
                    <div class="video-details">
                        <h3 id="videoTitle"></h3>
                        <p id="videoDuration"></p>
                    </div>
                </div>
                
                <h3>Download Options</h3>
                <div class="download-options" id="downloadOptions"></div>
            </div>
        </div>
        
        <!-- Middle Ad Unit -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <!-- Replace with your AdSense code -->
            <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID"
                crossorigin="anonymous"></script>
            <!-- Responsive Ad -->
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
    </main>
    
    <script>
        document.getElementById('downloadForm').addEventListener('submit', async function(e) {
            e.preventDefault();
            
            const videoUrl = document.getElementById('videoUrl').value;
            const format = document.getElementById('formatSelect').value;
            const quality = document.getElementById('qualitySelect').value;
            const errorElement = document.getElementById('errorMessage');
            const loadingElement = document.getElementById('loadingIndicator');
            const resultElement = document.getElementById('resultContainer');
            
            // Reset UI
            errorElement.style.display = 'none';
            resultElement.style.display = 'none';
            loadingElement.style.display = 'block';
            
            try {
                // Validate URL
                if (!isValidYouTubeUrl(videoUrl)) {
                    throw new Error('Please enter a valid YouTube URL');
                }
                
                // Extract video ID
                const videoId = extractVideoId(videoUrl);
                if (!videoId) {
                    throw new Error('Could not extract video ID from URL');
                }
                
                // Simulate API call (in a real app, call your backend here)
                const videoInfo = await simulateDownloadRequest(videoId, format, quality);
                
                // Display video info
                document.getElementById('videoTitle').textContent = videoInfo.title;
                document.getElementById('videoThumbnail').src = videoInfo.thumbnail;
                document.getElementById('videoDuration').textContent = videoInfo.duration;
                
                // Display download options
                displayDownloadOptions(videoInfo.formats);
                
                // Show results
                resultElement.style.display = 'block';
                
            } catch (error) {
                errorElement.textContent = error.message;
                errorElement.style.display = 'block';
            } finally {
                loadingElement.style.display = 'none';
            }
        });
        
        function isValidYouTubeUrl(url) {
            const pattern = /^(https?:\/\/)?(www\.)?(youtube\.com|youtu\.?be)\/.+$/;
            return pattern.test(url);
        }
        
        function extractVideoId(url) {
            const regExp = /^.*(youtu.be\/|v\/|u\/\w\/|embed\/|watch\?v=|&v=)([^#&?]*).*/;
            const match = url.match(regExp);
            return (match && match[2].length === 11) ? match[2] : null;
        }
        
        // Simulated API response
        async function simulateDownloadRequest(videoId, format, quality) {
            return new Promise((resolve) => {
                setTimeout(() => {
                    resolve({
                        title: `YouTube Video ${videoId}`,
                        thumbnail: `https://img.youtube.com/vi/${videoId}/mqdefault.jpg`,
                        duration: '10:30',
                        formats: {
                            [format]: {
                                quality: quality === 'high' ? '1080p' : 
                                       quality === 'medium' ? '720p' : '480p',
                                size: quality === 'high' ? '85MB' : 
                                     quality === 'medium' ? '45MB' : '25MB',
                                url: `https://example.com/download/${videoId}/${format}/${quality}`
                            }
                        }
                    });
                }, 2000);
            });
        }
        
        function displayDownloadOptions(formats) {
            const optionsElement = document.getElementById('downloadOptions');
            optionsElement.innerHTML = '';
            
            for (const [format, info] of Object.entries(formats)) {
                const card = document.createElement('div');
                card.className = 'download-card';
                card.innerHTML = `
                    <div class="download-card-header">
                        <span class="download-quality">${format.toUpperCase()} • ${info.quality}</span>
                        <span class="download-size">${info.size}</span>
                    </div>
                    <a href="${info.url}" class="download-btn" download>Download Now</a>
                `;
                optionsElement.appendChild(card);
            }
        }
        
        // Initialize ads
        document.addEventListener('DOMContentLoaded', function() {
            // Load additional ad scripts if needed
        });
    </script>
</body>
</html>
