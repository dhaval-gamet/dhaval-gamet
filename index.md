---
layout: none
permalink: /
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dhaval | Portfolio - Loading...</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #6366f1;
            --secondary: #8b5cf6;
            --accent: #10b981;
            --dark: #0f172a;
            --light: #f8fafc;
            --gray: #94a3b8;
            --gradient: linear-gradient(135deg, #6366f1, #8b5cf6, #10b981);
        }

        body {
            font-family: 'Space Grotesk', sans-serif;
            background-color: var(--dark);
            color: var(--light);
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            overflow: hidden;
            position: relative;
        }

        .background-animation {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: 
                radial-gradient(circle at 20% 30%, rgba(99, 102, 241, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(139, 92, 246, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 80%, rgba(16, 185, 129, 0.1) 0%, transparent 50%);
        }

        .loader-container {
            max-width: 800px;
            padding: 40px;
            background: rgba(15, 23, 42, 0.7);
            border-radius: 20px;
            border: 1px solid rgba(99, 102, 241, 0.3);
            backdrop-filter: blur(10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            margin: 20px;
        }

        .logo {
            font-family: 'Poppins', sans-serif;
            font-weight: 800;
            font-size: 3rem;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
        }

        .loading-title {
            font-size: 2.5rem;
            margin: 20px 0;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .loading-subtitle {
            color: var(--gray);
            font-size: 1.2rem;
            margin-bottom: 40px;
            max-width: 600px;
            line-height: 1.6;
        }

        .spinner {
            width: 80px;
            height: 80px;
            border: 4px solid rgba(99, 102, 241, 0.1);
            border-top: 4px solid var(--primary);
            border-right: 4px solid var(--secondary);
            border-bottom: 4px solid var(--accent);
            border-radius: 50%;
            animation: spin 1.5s linear infinite;
            margin: 30px auto;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .feature {
            padding: 20px;
            background: rgba(30, 41, 59, 0.4);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: transform 0.3s ease;
        }

        .feature:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
        }

        .feature i {
            font-size: 2rem;
            margin-bottom: 15px;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .launch-button {
            display: inline-block;
            padding: 18px 50px;
            background: var(--gradient);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.3rem;
            font-weight: 600;
            margin: 30px 0;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.3);
        }

        .launch-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(99, 102, 241, 0.4);
        }

        .launch-button i {
            margin-right: 10px;
        }

        .preview-container {
            width: 100%;
            height: 300px;
            margin-top: 40px;
            border-radius: 15px;
            overflow: hidden;
            border: 2px solid rgba(99, 102, 241, 0.3);
            position: relative;
        }

        #portfolio-frame {
            width: 100%;
            height: 100%;
            border: none;
            background: var(--dark);
        }

        .frame-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, 
                transparent 0%, 
                rgba(15, 23, 42, 0.7) 30%,
                rgba(15, 23, 42, 0.9) 100%);
            pointer-events: none;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            padding: 20px;
        }

        .mobile-warning {
            display: none;
            background: rgba(220, 38, 38, 0.1);
            border: 1px solid rgba(220, 38, 38, 0.3);
            color: #fca5a5;
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
        }

        @media (max-width: 768px) {
            .loader-container {
                margin: 10px;
                padding: 20px;
            }
            
            .loading-title {
                font-size: 1.8rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .mobile-warning {
                display: block;
            }
        }

        .loading-progress {
            width: 100%;
            height: 4px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 2px;
            margin: 20px 0;
            overflow: hidden;
        }

        .progress-bar {
            height: 100%;
            background: var(--gradient);
            width: 0%;
            animation: progress 2s ease-in-out infinite;
        }

        @keyframes progress {
            0% { width: 0%; }
            50% { width: 100%; }
            100% { width: 0%; }
        }

        .tech-icons {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .tech-icons i {
            font-size: 2rem;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            transition: transform 0.3s ease;
        }

        .tech-icons i:hover {
            transform: scale(1.2);
        }
    </style>
</head>
<body>
    <div class="background-animation"></div>
    
    <div class="loader-container">
        <div class="logo">DHAVAL</div>
        <h1 class="loading-title">Loading Interactive Portfolio</h1>
        
        <div class="spinner"></div>
        
        <div class="loading-progress">
            <div class="progress-bar"></div>
        </div>
        
        <p class="loading-subtitle">
            Preparing 3D animations, interactive elements, and immersive experience...
        </p>
        
        <div class="features-grid">
            <div class="feature">
                <i class="fas fa-cube"></i>
                <h3>3D Animations</h3>
                <p>Interactive cube with Three.js</p>
            </div>
            <div class="feature">
                <i class="fas fa-network-wired"></i>
                <h3>Dynamic Background</h3>
                <p>Vanta.js powered visuals</p>
            </div>
            <div class="feature">
                <i class="fas fa-mobile-alt"></i>
                <h3>Responsive Design</h3>
                <p>Works on all devices</p>
            </div>
            <div class="feature">
                <i class="fas fa-bolt"></i>
                <h3>Smooth Performance</h3>
                <p>Optimized animations</p>
            </div>
        </div>
        
        <div class="tech-icons">
            <i class="fab fa-html5" title="HTML5"></i>
            <i class="fab fa-css3-alt" title="CSS3"></i>
            <i class="fab fa-js" title="JavaScript"></i>
            <i class="fas fa-cube" title="Three.js"></i>
            <i class="fas fa-code" title="Vanta.js"></i>
        </div>
        
        <a href="portfolio.html" class="launch-button" id="launchBtn">
            <i class="fas fa-rocket"></i> Launch Full Portfolio
        </a>
        
        <div class="preview-container">
            <iframe id="portfolio-frame" src="portfolio.html" 
                    title="Portfolio Preview" 
                    loading="lazy"></iframe>
            <div class="frame-overlay">
                <small>Preview - Click above for full experience</small>
            </div>
        </div>
        
        <div class="mobile-warning">
            <i class="fas fa-info-circle"></i>
            For best experience on mobile, ensure you have a stable internet connection.
        </div>
        
        <p style="margin-top: 30px; color: var(--gray); font-size: 0.9rem;">
            <i class="fas fa-sync-alt"></i> Auto-redirecting in <span id="countdown">10</span> seconds
        </p>
    </div>

    <script>
        // Auto-redirect countdown
        let countdown = 10;
        const countdownElement = document.getElementById('countdown');
        const countdownInterval = setInterval(() => {
            countdown--;
            countdownElement.textContent = countdown;
            
            if (countdown <= 0) {
                clearInterval(countdownInterval);
                window.location.href = 'portfolio.html';
            }
        }, 1000);

        // Preview frame interaction
        const frame = document.getElementById('portfolio-frame');
        const launchBtn = document.getElementById('launchBtn');
        
        // Load frame content properly
        frame.onload = function() {
            console.log('Portfolio preview loaded');
            // Add some interactivity to preview
            setTimeout(() => {
                if (frame.contentWindow) {
                    try {
                        // Try to trigger some animation in iframe
                        frame.contentWindow.postMessage('playAnimation', '*');
                    } catch (e) {
                        console.log('Preview loaded successfully');
                    }
                }
            }, 1000);
        };

        // Enhanced button click
        launchBtn.addEventListener('click', function(e) {
            e.preventDefault();
            
            // Add loading effect
            this.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Launching...';
            this.style.opacity = '0.8';
            this.style.cursor = 'wait';
            
            // Redirect after short delay for UX
            setTimeout(() => {
                window.location.href = 'portfolio.html';
            }, 500);
        });

        // Handle iframe errors
        frame.onerror = function() {
            console.log('Error loading preview');
            document.querySelector('.frame-overlay').innerHTML = 
                '<div style="text-align: center; padding: 20px;">' +
                '<i class="fas fa-exclamation-triangle" style="font-size: 2rem; color: #f59e0b;"></i>' +
                '<p>Preview unavailable. Click Launch button above.</p>' +
                '</div>';
        };

        // Listen for messages from iframe
        window.addEventListener('message', function(event) {
            if (event.data === 'iframeLoaded') {
                console.log('Portfolio iframe fully loaded');
            }
        });

        // Add floating particles for loading screen
        function createParticles() {
            const particlesContainer = document.querySelector('.background-animation');
            for (let i = 0; i < 20; i++) {
                const particle = document.createElement('div');
                particle.style.position = 'absolute';
                particle.style.width = Math.random() * 5 + 2 + 'px';
                particle.style.height = particle.style.width;
                particle.style.background = `linear-gradient(135deg, 
                    rgba(${99 + Math.random() * 100}, ${102 + Math.random() * 100}, ${241}, 0.5),
                    rgba(${139}, ${92}, ${246}, 0.5))`;
                particle.style.borderRadius = '50%';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animation = `float ${3 + Math.random() * 7}s infinite ease-in-out`;
                
                particlesContainer.appendChild(particle);
            }
        }

        // Add CSS for particles
        const style = document.createElement('style');
        style.textContent = `
            @keyframes float {
                0%, 100% { transform: translate(0, 0) scale(1); }
                50% { transform: translate(${Math.random() * 50 - 25}px, ${Math.random() * 50 - 25}px) scale(1.2); }
            }
        `;
        document.head.appendChild(style);
        
        createParticles();

        // Check if user wants to stay on loading page
        launchBtn.addEventListener('mouseenter', () => {
            clearInterval(countdownInterval);
            countdownElement.textContent = 'paused';
            countdownElement.style.color = '#10b981';
        });

        launchBtn.addEventListener('mouseleave', () => {
            countdownElement.style.color = '';
        });
    </script>
</body>
</html>
