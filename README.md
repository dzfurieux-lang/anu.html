<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ANUKSHIKA | Premium Edition</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;700&family=Syncopate:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* ================= VARIABLES & RESET ================= */
        :root {
            --bg: #050505;
            --text: #ffffff;
            --gold: #D4AF37;
            --jul-cyan: #00f0ff;
            --roblox-red: #ff0055;
            --sri-lanka: #8D153A;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; cursor: none; /* Cache le curseur de base */ }
        
        body {
            background-color: var(--bg);
            color: var(--text);
            font-family: 'Space Grotesk', sans-serif;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* ================= CUSTOM CURSOR ================= */
        .cursor {
            width: 20px; height: 20px;
            border: 2px solid var(--gold);
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            transform: translate(-50%, -50%);
            transition: width 0.2s, height 0.2s, background-color 0.2s;
        }
        .cursor-dot {
            width: 4px; height: 4px;
            background: var(--jul-cyan);
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 10000;
            transform: translate(-50%, -50%);
        }

        /* ================= BACKGROUND CANVAS ================= */
        #canvas-bg {
            position: fixed;
            top: 0; left: 0;
            width: 100vw; height: 100vh;
            z-index: -1;
            opacity: 0.6;
        }

        /* ================= HERO SECTION ================= */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
        }

        .birth-date {
            font-family: 'Space Grotesk';
            font-size: 1rem;
            letter-spacing: 10px;
            color: rgba(255, 255, 255, 0.5);
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .glitch-title {
            font-family: 'Syncopate', sans-serif;
            font-size: clamp(3rem, 8vw, 7rem);
            font-weight: 700;
            text-transform: uppercase;
            position: relative;
            text-shadow: 0 0 20px rgba(212, 175, 55, 0.5);
        }

        .subtitle {
            margin-top: 20px;
            font-size: 1.2rem;
            letter-spacing: 5px;
            background: linear-gradient(90deg, var(--gold), var(--jul-cyan));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .scroll-indicator {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            animation: bounce 2s infinite;
            opacity: 0.5;
        }

        @keyframes bounce {
            0%, 100% { transform: translate(-50%, 0); }
            50% { transform: translate(-50%, 15px); }
        }

        /* ================= PREMIUM BENTO GRID ================= */
        .grid-container {
            max-width: 1400px;
            margin: 100px auto;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .tilt-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 40px;
            backdrop-filter: blur(10px);
            transform-style: preserve-3d;
            transition: border 0.3s;
            opacity: 0;
            transform: translateY(50px);
        }

        .tilt-card.visible {
            opacity: 1;
            transform: translateY(0);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        .tilt-card:hover {
            border-color: rgba(255, 255, 255, 0.2);
        }

        .card-content {
            transform: translateZ(30px); /* Effet 3D du texte */
        }

        h2 {
            font-family: 'Syncopate', sans-serif;
            font-size: 1.5rem;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        p { line-height: 1.6; color: #a0a0a0; font-size: 1.1rem; }

        /* Specific Cards */
        .card-sri-lanka { grid-column: span 2; border-top: 2px solid var(--gold); }
        .card-jul { border-top: 2px solid var(--jul-cyan); }
        .card-roblox { border-top: 2px solid var(--roblox-red); }
        .card-calls { grid-column: span 2; border-top: 2px solid #8A2BE2; }

        /* ================= FOOTER ================= */
        footer {
            text-align: center;
            padding: 100px 20px 50px;
            font-family: 'Syncopate';
            font-size: 0.8rem;
            letter-spacing: 3px;
            color: rgba(255, 255, 255, 0.3);
        }

        @media (max-width: 1024px) {
            .grid-container { grid-template-columns: 1fr; }
            .card-sri-lanka, .card-calls { grid-column: span 1; }
        }
    </style>
</head>
<body>

    <!-- Curseur Custom -->
    <div class="cursor" id="cursor"></div>
    <div class="cursor-dot" id="cursor-dot"></div>

    <!-- Fond Particules 3D -->
    <canvas id="canvas-bg"></canvas>

    <section class="hero">
        <div class="birth-date">Est. 13 Juillet 2010</div>
        <h1 class="glitch-title">ANUKSHIKA</h1>
        <div class="subtitle">THE ULTIMATE SISTER</div>
        <div class="scroll-indicator"><i class="fa-solid fa-chevron-down"></i></div>
    </section>

    <section class="grid-container" id="grid">
        
        <!-- SRI LANKA -->
        <div class="tilt-card card-sri-lanka">
            <div class="card-content">
                <h2 style="color: var(--gold);"><i class="fa-solid fa-crown"></i> Héritage Sri Lankais</h2>
                <p>Le sang royal du Sri Lanka coule dans ses veines. Une force de caractère, une élégance naturelle et un cœur immense. Elle n'est pas seulement ma sœur, elle est ma fierté absolue.</p>
            </div>
        </div>

        <!-- JUL -->
        <div class="tilt-card card-jul">
            <div class="card-content">
                <h2 style="color: var(--jul-cyan);">👽 LA ZONE</h2>
                <p>Team Jul validée. D'or et de platine au quotidien. Personne n'écoute le J avec autant de style qu'elle. C'est pas des LOL, c'est le sang.</p>
            </div>
        </div>

        <!-- ROBLOX -->
        <div class="tilt-card card-roblox">
            <div class="card-content">
                <h2 style="color: var(--roblox-red);"><i class="fa-solid fa-gamepad"></i> ROBLOX</h2>
                <p>Notre terrain d'entente. Nos sessions de jeu interminables, les fous rires sur les serveurs, et cette complicité de malade qu'on ne retrouve nulle part ailleurs.</p>
            </div>
        </div>

        <!-- NIGHT CALLS -->
        <div class="tilt-card card-calls">
            <div class="card-content">
                <h2 style="color: #8A2BE2;"><i class="fa-solid fa-phone-volume"></i> Appels Nocturnes</h2>
                <p>Quand tout le monde dort, on refait le monde. Ces appels le soir, nos discussions sans fin... ce sont mes moments préférés. Un lien fraternel que rien ni personne ne pourra jamais briser. Je t'aime énormément.</p>
            </div>
        </div>

    </section>

    <footer>
        DÉDIÉ À ANUKSHIKA • LA MEILLEURE SŒUR DE L'UNIVERS
    </footer>

    <script>
        // 1. CUSTOM CURSOR LOGIC
        const cursor = document.getElementById('cursor');
        const cursorDot = document.getElementById('cursor-dot');
        
        window.addEventListener('mousemove', (e) => {
            cursor.style.left = e.clientX + 'px';
            cursor.style.top = e.clientY + 'px';
            cursorDot.style.left = e.clientX + 'px';
            cursorDot.style.top = e.clientY + 'px';
        });

        document.querySelectorAll('.tilt-card').forEach(el => {
            el.addEventListener('mouseenter', () => {
                cursor.style.transform = 'translate(-50%, -50%) scale(2)';
                cursor.style.backgroundColor = 'rgba(255, 255, 255, 0.1)';
            });
            el.addEventListener('mouseleave', () => {
                cursor.style.transform = 'translate(-50%, -50%) scale(1)';
                cursor.style.backgroundColor = 'transparent';
                // Reset tilt
                el.style.transform = `perspective(1000px) rotateX(0deg) rotateY(0deg)`;
            });
        });

        // 2. 3D TILT EFFECT ON CARDS
        const cards = document.querySelectorAll('.tilt-card');
        cards.forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                const centerX = rect.width / 2;
                const centerY = rect.height / 2;
                
                const rotateX = ((y - centerY) / centerY) * -10; // Max 10 deg
                const rotateY = ((x - centerX) / centerX) * 10;
                
                card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
            });
        });

        // 3. SCROLL REVEAL ANIMATION
        const observerOptions = { threshold: 0.1 };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        cards.forEach(card => observer.observe(card));

        // 4. PARTICLES BACKGROUND ANIMATION (CANVAS)
        const canvas = document.getElementById('canvas-bg');
        const ctx = canvas.getContext('2d');
        let particlesArray;

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        class Particle {
            constructor(x, y, directionX, directionY, size, color) {
                this.x = x; this.y = y;
                this.directionX = directionX; this.directionY = directionY;
                this.size = size; this.color = color;
            }
            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2, false);
                ctx.fillStyle = this.color;
                ctx.fill();
            }
            update() {
                if (this.x > canvas.width || this.x < 0) this.directionX = -this.directionX;
                if (this.y > canvas.height || this.y < 0) this.directionY = -this.directionY;
                this.x += this.directionX;
                this.y += this.directionY;
                this.draw();
            }
        }

        function initParticles() {
            particlesArray = [];
            let numberOfParticles = (canvas.height * canvas.width) / 9000;
            for (let i = 0; i < numberOfParticles; i++) {
                let size = (Math.random() * 2) + 1;
                let x = (Math.random() * ((innerWidth - size * 2) - (size * 2)) + size * 2);
                let y = (Math.random() * ((innerHeight - size * 2) - (size * 2)) + size * 2);
                let directionX = (Math.random() * 1) - 0.5;
                let directionY = (Math.random() * 1) - 0.5;
                let color = '#ffffff';
                particlesArray.push(new Particle(x, y, directionX, directionY, size, color));
            }
        }

        function animateParticles() {
            requestAnimationFrame(animateParticles);
            ctx.clearRect(0, 0, innerWidth, innerHeight);
            for (let i = 0; i < particlesArray.length; i++) {
                particlesArray[i].update();
            }
        }

        window.addEventListener('resize', () => {
            canvas.width = innerWidth;
            canvas.height = innerHeight;
            initParticles();
        });

        initParticles();
        animateParticles();
    </script>
</body>
</html>
