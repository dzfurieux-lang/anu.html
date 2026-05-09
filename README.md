<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ANUKSHIKA OS | The Queen</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;700&family=Syncopate:wght@400;700&family=VT323&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg: #0a0a0a;
            --text: #ffffff;
            --gold: #FFD700;
            --sri-lanka-red: #8D153A;
            --jul-alien: #00f0ff;
            --roblox-oof: #ff0055;
            --buddha-orange: #FF9933;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            background-color: var(--bg);
            color: var(--text);
            font-family: 'Space Grotesk', sans-serif;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* --- BOOT SCREEN (TROLL HACKING EFFECT) --- */
        #boot-screen {
            position: fixed;
            top: 0; left: 0; width: 100vw; height: 100vh;
            background: #000;
            color: #0f0;
            font-family: 'VT323', monospace;
            font-size: 1.5rem;
            padding: 20px;
            z-index: 10000;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
        }
        .boot-text { margin-bottom: 10px; opacity: 0; }

        /* --- MAIN CONTENT --- */
        #main-content {
            display: none; /* Hidden until boot finishes */
            opacity: 0;
            transition: opacity 2s ease-in;
        }

        /* --- BACKGROUND --- */
        #canvas-bg {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            z-index: -1; opacity: 0.4;
        }

        /* --- HERO --- */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            background: radial-gradient(circle at center, rgba(141, 21, 58, 0.2) 0%, transparent 70%);
        }

        .title-glitch {
            font-family: 'Syncopate', sans-serif;
            font-size: clamp(3rem, 8vw, 7rem);
            font-weight: 700;
            color: var(--gold);
            text-shadow: 0 0 30px rgba(255, 215, 0, 0.4);
            animation: pulse 2s infinite;
        }

        /* --- BENTO GRID SYSTEM --- */
        .grid-container {
            max-width: 1400px;
            margin: 0 auto 100px;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            gap: 20px;
        }

        .card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 30px;
            backdrop-filter: blur(10px);
            transition: transform 0.3s, border-color 0.3s;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: rgba(255, 255, 255, 0.2);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .card h2 {
            font-family: 'Syncopate', sans-serif;
            font-size: 1.3rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* --- SECTIONS SPÉCIFIQUES --- */
        .sri-lanka-card { grid-column: span 8; border-top: 3px solid var(--sri-lanka-red); }
        .religion-card { grid-column: span 4; border-top: 3px solid var(--buddha-orange); }
        .jul-card { grid-column: span 6; border-top: 3px solid var(--jul-alien); }
        .roblox-card { grid-column: span 6; border-top: 3px solid var(--roblox-oof); }
        .calls-card { grid-column: span 12; background: linear-gradient(135deg, rgba(20,20,40,0.8), rgba(0,0,0,0.9)); border: 1px solid #8A2BE2; }

        /* --- STATS TROLL --- */
        .stat-bar { margin-top: 15px; }
        .stat-bar span { display: block; font-size: 0.9rem; margin-bottom: 5px; color: #aaa; }
        .bar-bg { width: 100%; height: 10px; background: rgba(255,255,255,0.1); border-radius: 5px; overflow: hidden; }
        .bar-fill { height: 100%; border-radius: 5px; }

        .btn-troll {
            margin-top: 30px;
            padding: 15px 30px;
            font-family: 'Syncopate';
            font-weight: bold;
            background: red;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 0 20px rgba(255,0,0,0.5);
            transition: 0.2s;
        }
        .btn-troll:hover { background: darkred; transform: scale(1.05); }

        @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.8; } }

        @media (max-width: 900px) {
            .sri-lanka-card, .religion-card, .jul-card, .roblox-card { grid-column: span 12; }
        }
    </style>
</head>
<body>

    <!-- BOOT SCREEN (TROLL) -->
    <div id="boot-screen">
        <div class="boot-text" id="line1">INITIALISATION DE L'OS ANUKSHIKA...</div>
        <div class="boot-text" id="line2">CHARGEMENT DU PROFIL : SŒUR D'AMOUR... [OK]</div>
        <div class="boot-text" id="line3">VERIFICATION DE L'ADN SRI LANKAIS... [100% PUR]</div>
        <div class="boot-text" id="line4">CONNEXION AUX SERVEURS JUL (LA ZONE)... [D'OR ET DE PLATINE]</div>
        <div class="boot-text" id="line5">ANALYSE DU NIVEAU ROBLOX... [ERREUR: NIVEAU NOOB DÉTECTÉ... ON L'AIME QUAND MÊME]</div>
        <div class="boot-text" id="line6" style="color: yellow; margin-top: 20px;">DÉVERROUILLAGE DU SYSTÈME DANS 3... 2... 1...</div>
    </div>

    <div id="main-content">
        <canvas id="canvas-bg"></canvas>

        <header class="hero">
            <div style="color: var(--gold); font-size: 1.2rem; margin-bottom: 10px; letter-spacing: 5px;">EST. 13 JUILLET 2010</div>
            <h1 class="title-glitch">ANUKSHIKA</h1>
            <p style="font-size: 1.5rem; color: #ccc; margin-top: 10px;">L'Élue du Sri Lanka • Princesse de la Nuit • OOF Master</p>
        </header>

        <div class="grid-container">
            
            <!-- ORIGINES SRI LANKA (DÉTAILLÉ) -->
            <div class="card sri-lanka-card">
                <h2 style="color: var(--sri-lanka-red);"><i class="fa-solid fa-earth-asia"></i> HÉRITAGE SRI LANKAIS</h2>
                <p style="color: #bbb; line-height: 1.6; margin-bottom: 20px;">
                    Née avec la puissance du Lion de Ceylan. Anukshika représente l'élite absolue. Dans ses veines coule la force des ancêtres, et sur sa langue, une tolérance aux épices qui ferait pleurer un dragon. Un Kottu Roti supplément piment ? C'est juste son petit-déjeuner.
                </p>
                <div class="stat-bar">
                    <span>Tolérance au piment (Échelle de Scoville)</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 100%; background: red;"></div></div>
                </div>
                <div class="stat-bar">
                    <span>Charisme Royal</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 95%; background: var(--gold);"></div></div>
                </div>
            </div>

            <!-- RELIGION ET KARMA -->
            <div class="card religion-card">
                <h2 style="color: var(--buddha-orange);"><i class="fa-solid fa-yin-yang"></i> SPIRITUALITÉ</h2>
                <p style="color: #bbb; line-height: 1.6;">
                    L'île de l'émeraude est sacrée, tout comme elle. Que ce soit sous la protection des temples bouddhistes ou avec les bénédictions des divinités hindoues (Ganesha veille sur ses games Roblox), elle possède un Karma niveau légendaire. 
                </p>
                <div style="margin-top: 20px; font-weight: bold; color: var(--gold); text-align: center; font-size: 1.5rem;">
                    KARMA: OVER 9000 🕉️
                </div>
            </div>

            <!-- JUL -->
            <div class="card jul-card">
                <h2 style="color: var(--jul-alien);">👽 LA ZONE (RELIGION SECONDAIRE)</h2>
                <p style="color: #bbb; line-height: 1.6;">
                    Si le Sri Lanka est sa patrie, "La Zone" est sa deuxième maison. Elle connaît les sons de Jul mieux que ses leçons d'histoire. Quand elle fait le signe Jul, même les aliens de l'espace la respectent.
                </p>
                <div class="stat-bar">
                    <span>Heures passées à écouter Jul</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 100%; background: var(--jul-alien);"></div></div>
                </div>
            </div>

            <!-- ROBLOX (TROLL) -->
            <div class="card roblox-card">
                <h2 style="color: var(--roblox-oof);"><i class="fa-solid fa-gamepad"></i> DOSSIER ROBLOX</h2>
                <p style="color: #bbb; line-height: 1.6;">
                    Notre QG virtuel. On y joue des heures. Par contre, il faut qu'on parle de son niveau... Officiellement elle est très forte, officieusement, le son "OOF" est la bande originale de ses parties. Mais c'est pour ça que c'est ma joueuse préférée.
                </p>
                <div class="stat-bar">
                    <span>Skill Réel</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 15%; background: orange;"></div></div>
                </div>
                <div class="stat-bar">
                    <span>Fous rires générés</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 100%; background: #00ff00;"></div></div>
                </div>
            </div>

            <!-- APPELS NOCTURNES -->
            <div class="card calls-card" style="text-align: center;">
                <h2 style="color: #8A2BE2; justify-content: center;"><i class="fa-solid fa-moon"></i> LE SYNDICAT DE LA NUIT</h2>
                <p style="color: #bbb; line-height: 1.6; max-width: 800px; margin: 0 auto 20px;">
                    C'est la nuit que la magie opère. Nos appels le soir sont légendaires. On refait le monde, on juge les gens, on pleure de rire jusqu'à ne plus avoir de souffle. C'est dans ces moments-là que je me rends compte que je n'ai pas juste une sœur, j'ai une meilleure amie pour la vie. Je t'aime de fou Anukshika. ❤️
                </p>
                <button class="btn-troll" onclick="alert('Bip Bip Bip... Le serveur de Jul a crashé suite à un excès de love. Mais Anukshika est certifiée Boss Finale de la famille !')">
                    ACTIVER LE PROTOCOLE D'AMOUR
                </button>
            </div>

        </div>
    </div>

    <script>
        // --- BOOT SEQUENCE LOGIC ---
        const lines = document.querySelectorAll('.boot-text');
        const bootScreen = document.getElementById('boot-screen');
        const mainContent = document.getElementById('main-content');

        let delay = 500;
        lines.forEach((line, index) => {
            setTimeout(() => {
                line.style.opacity = '1';
            }, delay);
            delay += 800; // Delay between lines
        });

        // Hide boot screen and show main content
        setTimeout(() => {
            bootScreen.style.display = 'none';
            mainContent.style.display = 'block';
            setTimeout(() => { mainContent.style.opacity = '1'; }, 100);
        }, delay + 1000);

        // --- PARTICLES BACKGROUND (PREMIUM VIBE) ---
        const canvas = document.getElementById('canvas-bg');
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        let particles = [];
        for (let i = 0; i < 100; i++) {
            particles.push({
                x: Math.random() * canvas.width,
                y: Math.random() * canvas.height,
                size: Math.random() * 2,
                speedX: (Math.random() - 0.5) * 0.5,
                speedY: (Math.random() - 0.5) * 0.5
            });
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = "rgba(255, 215, 0, 0.5)"; // Gold particles
            particles.forEach(p => {
                p.x += p.speedX; p.y += p.speedY;
                if (p.x < 0 || p.x > canvas.width) p.speedX *= -1;
                if (p.y < 0 || p.y > canvas.height) p.speedY *= -1;
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
                ctx.fill();
            });
            requestAnimationFrame(animate);
        }
        animate();
    </script>
</body>
</html>
