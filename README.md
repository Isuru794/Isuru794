<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Isuru Sumedha | Fullstack Developer & SE Undergraduate</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0a0a0f 0%, #0d1117 100%);
            color: #ffffff;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }

        /* Animated Background Grid */
        .grid-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 255, 204, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 204, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            pointer-events: none;
            animation: gridMove 20s linear infinite;
            z-index: 0;
        }

        @keyframes gridMove {
            0% {
                transform: translate(0, 0);
            }
            100% {
                transform: translate(50px, 50px);
            }
        }

        /* Floating Orbs */
        .orb {
            position: fixed;
            border-radius: 50%;
            filter: blur(80px);
            opacity: 0.3;
            pointer-events: none;
            z-index: 0;
            animation: floatOrb 15s ease-in-out infinite;
        }

        @keyframes floatOrb {
            0%, 100% {
                transform: translate(0, 0) scale(1);
            }
            50% {
                transform: translate(50px, -50px) scale(1.1);
            }
        }

        .orb-1 {
            width: 400px;
            height: 400px;
            background: #00ffcc;
            top: -200px;
            right: -200px;
            animation-delay: 0s;
        }

        .orb-2 {
            width: 300px;
            height: 300px;
            background: #ff3366;
            bottom: -150px;
            left: -150px;
            animation-delay: 5s;
        }

        .orb-3 {
            width: 250px;
            height: 250px;
            background: #6633ff;
            top: 50%;
            left: 50%;
            animation-delay: 10s;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        /* About Me Card */
        .about-card {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(0, 255, 204, 0.2);
            padding: 40px;
            margin-bottom: 30px;
            transition: all 0.3s ease;
            animation: slideIn 0.8s ease-out;
        }

        .about-card:hover {
            border-color: rgba(0, 255, 204, 0.5);
            box-shadow: 0 0 30px rgba(0, 255, 204, 0.1);
            transform: translateY(-5px);
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .profile-header {
            display: flex;
            align-items: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }

        .avatar {
            width: 130px;
            height: 130px;
            background: linear-gradient(135deg, #00ffcc, #ff3366);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: rotate 10s linear infinite;
            box-shadow: 0 0 30px rgba(0, 255, 204, 0.3);
        }

        @keyframes rotate {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        .avatar-inner {
            width: 120px;
            height: 120px;
            background: #0d1117;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            font-weight: bold;
            background: linear-gradient(135deg, #00ffcc, #ff3366);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }

        .name-section h1 {
            font-size: 48px;
            background: linear-gradient(135deg, #00ffcc, #ff3366, #6633ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 10px;
        }

        .badge {
            display: inline-block;
            padding: 5px 15px;
            background: rgba(0, 255, 204, 0.1);
            border: 1px solid rgba(0, 255, 204, 0.3);
            border-radius: 20px;
            color: #00ffcc;
            font-size: 14px;
            margin-right: 10px;
            margin-top: 10px;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .info-item {
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            border-left: 3px solid #00ffcc;
            transition: all 0.3s ease;
        }

        .info-item:hover {
            transform: translateX(10px);
            background: rgba(0, 255, 204, 0.1);
        }

        .info-label {
            color: #00ffcc;
            font-weight: bold;
            margin-bottom: 5px;
        }

        /* Typing Animation */
        .typing-container {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            text-align: center;
            border: 1px solid rgba(0, 255, 204, 0.2);
            animation: slideIn 0.8s ease-out 0.2s backwards;
        }

        .typing-text {
            font-size: 28px;
            font-weight: bold;
            color: #00ffcc;
            font-family: monospace;
        }

        .cursor {
            display: inline-block;
            width: 3px;
            height: 32px;
            background: #00ffcc;
            animation: blink 1s infinite;
            margin-left: 5px;
            vertical-align: middle;
        }

        @keyframes blink {
            0%, 50% {
                opacity: 1;
            }
            51%, 100% {
                opacity: 0;
            }
        }

        /* Stats Cards */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            border: 1px solid rgba(0, 255, 204, 0.2);
            transition: all 0.3s ease;
            animation: slideIn 0.8s ease-out 0.4s backwards;
        }

        .stat-card:hover {
            transform: translateY(-5px) scale(1.02);
            border-color: #00ffcc;
            box-shadow: 0 5px 25px rgba(0, 255, 204, 0.2);
        }

        .stat-number {
            font-size: 48px;
            font-weight: bold;
            color: #00ffcc;
            margin-bottom: 10px;
        }

        /* Tech Stack */
        .tech-section {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 40px;
            margin-bottom: 30px;
            border: 1px solid rgba(0, 255, 204, 0.2);
            animation: slideIn 0.8s ease-out 0.6s backwards;
        }

        .section-title {
            font-size: 32px;
            text-align: center;
            margin-bottom: 30px;
            background: linear-gradient(135deg, #00ffcc, #ff3366);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 20px;
        }

        .tech-item {
            text-align: center;
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tech-item:hover {
            transform: translateY(-5px);
            background: rgba(0, 255, 204, 0.1);
            box-shadow: 0 5px 15px rgba(0, 255, 204, 0.2);
        }

        .tech-icon {
            font-size: 48px;
            margin-bottom: 10px;
        }

        /* 3D Cube */
        .cube-container {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 40px;
            margin-bottom: 30px;
            text-align: center;
            border: 1px solid rgba(0, 255, 204, 0.2);
            animation: slideIn 0.8s ease-out 0.8s backwards;
        }

        .canvas-container {
            display: inline-block;
            margin: 0 auto;
        }

        canvas {
            border-radius: 10px;
            box-shadow: 0 0 30px rgba(0, 255, 204, 0.3);
        }

        /* Focus Cards */
        .focus-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }

        .focus-card {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(0, 255, 204, 0.2);
            transition: all 0.3s ease;
            animation: slideIn 0.8s ease-out 1s backwards;
        }

        .focus-card:hover {
            transform: translateY(-5px);
            border-color: #00ffcc;
            box-shadow: 0 0 20px rgba(0, 255, 204, 0.1);
        }

        .focus-icon {
            font-size: 48px;
            margin-bottom: 15px;
        }

        /* Connect Section */
        .connect-section {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 40px;
            text-align: center;
            border: 1px solid rgba(0, 255, 204, 0.2);
            animation: slideIn 0.8s ease-out 1.2s backwards;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .social-btn {
            padding: 12px 30px;
            background: rgba(0, 255, 204, 0.1);
            border: 1px solid rgba(0, 255, 204, 0.3);
            border-radius: 25px;
            color: #00ffcc;
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: bold;
        }

        .social-btn:hover {
            background: #00ffcc;
            color: #0d1117;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 255, 204, 0.3);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 30px;
            color: rgba(255, 255, 255, 0.5);
        }
    </style>
</head>
<body>
    <div class="grid-bg"></div>
    <div class="orb orb-1"></div>
    <div class="orb orb-2"></div>
    <div class="orb orb-3"></div>

    <div class="container">
        <!-- About Me Section - TOP -->
        <div class="about-card">
            <div class="profile-header">
                <div class="avatar">
                    <div class="avatar-inner">IS</div>
                </div>
                <div class="name-section">
                    <h1>Isuru Sumedha</h1>
                    <div>
                        <span class="badge">Fullstack Developer</span>
                        <span class="badge">SE Undergraduate</span>
                        <span class="badge">3D Web Enthusiast</span>
                    </div>
                </div>
            </div>
            
            <div class="info-grid">
                <div class="info-item">
                    <div class="info-label">🎓 Education</div>
                    <div>Software Engineering Undergraduate</div>
                    <div style="font-size: 14px; color: #888;">University of Sri Lanka</div>
                </div>
                <div class="info-item">
                    <div class="info-label">💼 Current Role</div>
                    <div>Fullstack Developer</div>
                    <div style="font-size: 14px; color: #888;">MERN | Next.js | Three.js</div>
                </div>
                <div class="info-item">
                    <div class="info-label">📍 Location</div>
                    <div>Sri Lanka</div>
                    <div style="font-size: 14px; color: #888;">Asia/Colombo</div>
                </div>
                <div class="info-item">
                    <div class="info-label">🚀 Passion</div>
                    <div>Creative Coding & 3D Web</div>
                    <div style="font-size: 14px; color: #888;">WebGL | Three.js | Interactive Design</div>
                </div>
            </div>
        </div>

        <!-- Typing Animation -->
        <div class="typing-container">
            <div class="typing-text">
                <span id="typed-text"></span><span class="cursor"></span>
            </div>
        </div>

        <!-- Stats -->
        <div class="stats-grid">
            <div class="stat-card">
                <div class="stat-number" id="years-exp">3+</div>
                <div>Years of Coding</div>
                <div style="font-size: 12px; color: #888;">Fullstack Development</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="projects">20+</div>
                <div>Projects Completed</div>
                <div style="font-size: 12px; color: #888;">Production Ready</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="tech-stack">15+</div>
                <div>Technologies</div>
                <div style="font-size: 12px; color: #888;">And Growing</div>
            </div>
        </div>

        <!-- Tech Stack -->
        <div class="tech-section">
            <h2 class="section-title">⚡ Tech Universe</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-icon">⚛️</div>
                    <div>React</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🟢</div>
                    <div>Node.js</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">▲</div>
                    <div>Next.js</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📘</div>
                    <div>TypeScript</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🎨</div>
                    <div>Three.js</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🎯</div>
                    <div>Tailwind</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🍃</div>
                    <div>MongoDB</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐘</div>
                    <div>PostgreSQL</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐳</div>
                    <div>Docker</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📦</div>
                    <div>Git</div>
                </div>
            </div>
        </div>

        <!-- 3D Cube -->
        <div class="cube-container">
            <h2 class="section-title">🔄 3D Interactive Cube</h2>
            <div class="canvas-container">
                <canvas id="cubeCanvas" width="300" height="300"></canvas>
            </div>
            <p style="margin-top: 15px; color: #888;">✨ Rotating in 3D Space</p>
        </div>

        <!-- Current Focus -->
        <div class="focus-grid">
            <div class="focus-card">
                <div class="focus-icon">🔭</div>
                <h3 style="color: #00ffcc; margin-bottom: 10px;">Currently Building</h3>
                <p>Fullstack SaaS platform with Next.js + Three.js 3D dashboards</p>
            </div>
            <div class="focus-card">
                <div class="focus-icon">🌱</div>
                <h3 style="color: #00ffcc; margin-bottom: 10px;">Learning</h3>
                <p>WebGL Shaders, System Design, AWS Architecture</p>
            </div>
            <div class="focus-card">
                <div class="focus-icon">🤝</div>
                <h3 style="color: #00ffcc; margin-bottom: 10px;">Open To</h3>
                <p>3D web projects, Hackathons, Creative collaborations</p>
            </div>
        </div>

        <!-- Connect -->
        <div class="connect-section">
            <h2 class="section-title">🌐 Let's Connect</h2>
            <div class="social-links">
                <a href="#" class="social-btn">💼 LinkedIn</a>
                <a href="#" class="social-btn">🐦 Twitter</a>
                <a href="#" class="social-btn">💻 GitHub</a>
                <a href="#" class="social-btn">📧 Email</a>
                <a href="#" class="social-btn">🎨 Portfolio</a>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>⚡ 3D Animated Profile | Built with 💚 by Isuru Sumedha</p>
            <p style="font-size: 12px; margin-top: 10px;">Fullstack Developer | SE Undergraduate | 3D Web Enthusiast</p>
        </div>
    </div>

    <script>
        // Typing Animation
        const phrases = [
            "Fullstack Developer",
            "3D Web Enthusiast", 
            "Creative Problem Solver",
            "MERN Stack Expert",
            "Always Learning..."
        ];
        
        let phraseIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typedTextElement = document.getElementById('typed-text');
        
        function typeEffect() {
            const currentPhrase = phrases[phraseIndex];
            
            if (isDeleting) {
                typedTextElement.textContent = currentPhrase.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typedTextElement.textContent = currentPhrase.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === currentPhrase.length) {
                isDeleting = true;
                setTimeout(typeEffect, 2000);
                return;
            }
            
            if (isDeleting && charIndex === 0) {
                isDeleting = false;
                phraseIndex = (phraseIndex + 1) % phrases.length;
                setTimeout(typeEffect, 500);
                return;
            }
            
            const speed = isDeleting ? 50 : 100;
            setTimeout(typeEffect, speed);
        }
        
        typeEffect();

        // 3D Cube with Three.js
        function initCube() {
            const canvas = document.getElementById('cubeCanvas');
            const scene = new THREE.Scene();
            scene.background = new THREE.Color(0x0d1117);
            
            const camera = new THREE.PerspectiveCamera(75, 1, 0.1, 1000);
            camera.position.z = 2.5;
            
            const renderer = new THREE.WebGLRenderer({ canvas, alpha: false });
            renderer.setSize(300, 300);
            renderer.setClearColor(0x0d1117);
            
            // Create cube with different colors for each face
            const materials = [
                new THREE.MeshStandardMaterial({ color: 0x00ffcc, metalness: 0.7, roughness: 0.2 }), // right
                new THREE.MeshStandardMaterial({ color: 0xff3366, metalness: 0.7, roughness: 0.2 }), // left
                new THREE.MeshStandardMaterial({ color: 0x6633ff, metalness: 0.7, roughness: 0.2 }), // top
                new THREE.MeshStandardMaterial({ color: 0xffcc00, metalness: 0.7, roughness: 0.2 }), // bottom
                new THREE.MeshStandardMaterial({ color: 0x33ff66, metalness: 0.7, roughness: 0.2 }), // front
                new THREE.MeshStandardMaterial({ color: 0xff6633, metalness: 0.7, roughness: 0.2 })  // back
            ];
            
            const geometry = new THREE.BoxGeometry(1.2, 1.2, 1.2);
            const cube = new THREE.Mesh(geometry, materials);
            scene.add(cube);
            
            // Lighting
            const ambientLight = new THREE.AmbientLight(0x404040);
            scene.add(ambientLight);
            
            const directionalLight = new THREE.DirectionalLight(0xffffff, 1);
            directionalLight.position.set(2, 2, 2);
            scene.add(directionalLight);
            
            const backLight = new THREE.PointLight(0x00ffcc, 0.5);
            backLight.position.set(-1, -1, -1);
            scene.add(backLight);
            
            // Animation
            function animate() {
                requestAnimationFrame(animate);
                cube.rotation.x += 0.01;
                cube.rotation.y += 0.015;
                cube.rotation.z += 0.005;
                renderer.render(scene, camera);
            }
            
            animate();
        }
        
        // Load Three.js and init cube
        const script = document.createElement('script');
        script.src = 'https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js';
        script.onload = initCube;
        document.head.appendChild(script);
        
        // Animate numbers counting up
        function animateNumber(element, target, suffix = '') {
            let current = 0;
            const increment = target / 50;
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    element.textContent = target + suffix;
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(current) + suffix;
                }
            }, 20);
        }
        
        // Trigger number animations when in viewport
        const observerOptions = {
            threshold: 0.5
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    if (entry.target.id === 'years-exp') animateNumber(entry.target, 3, '+');
                    if (entry.target.id === 'projects') animateNumber(entry.target, 20, '+');
                    if (entry.target.id === 'tech-stack') animateNumber(entry.target, 15, '+');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);
        
        observer.observe(document.getElementById('years-exp'));
        observer.observe(document.getElementById('projects'));
        observer.observe(document.getElementById('tech-stack'));
        
        // Smooth scroll reveal animation
        const revealElements = document.querySelectorAll('.about-card, .typing-container, .stat-card, .tech-section, .cube-container, .focus-card, .connect-section');
        
        const revealObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });
        
        revealElements.forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'all 0.6s ease-out';
            revealObserver.observe(el);
        });
    </script>
</body>
</html>
