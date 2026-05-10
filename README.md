<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ANUKSHIKA | OS Premium</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;700&family=Syncopate:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg: #050505;
            --text: #ffffff;
            --gold: #FFD700;
            --hindu-saffron: #FF671F;
            --jul-alien: #00f0ff;
            --roblox-red: #ff0055;
            --night-purple: #8A2BE2;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            background-color: var(--bg);
            color: var(--text);
            font-family: 'Space Grotesk', sans-serif;
            overflow-x: hidden;
        }

        /* --- BACKGROUND --- */
        #canvas-bg {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            z-index: -1; opacity: 0.5;
        }

        /* --- HERO SECTION --- */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            background: radial-gradient(circle at center, rgba(255, 103, 31, 0.15) 0%, transparent 60%);
        }

        .date-badge {
            font-family: 'Syncopate', sans-serif;
            background: rgba(255, 215, 0, 0.1);
            color: var(--gold);
            padding: 10px 20px;
            border: 1px solid var(--gold);
            border-radius: 50px;
            margin-bottom: 20px;
            letter-spacing: 3px;
            font-weight: bold;
        }

        .title-glitch {
            font-family: 'Syncopate', sans-serif;
            font-size: clamp(3rem, 10vw, 8rem);
            font-weight: 700;
            background: linear-gradient(to right, #fff, var(--gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 40px rgba(255, 215, 0, 0.3);
            margin-bottom: 10px;
        }

        .subtitle {
            font-size: 1.5rem;
            color: #aaa;
            letter-spacing: 2px;
        }

        /* --- GRID LAYOUT --- */
        .container {
            max-width: 1400px;
            margin: 0 auto 100px;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            gap: 25px;
        }

        .card {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 40px;
            backdrop-filter: blur(10px);
            transition: 0.4s;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 255, 255, 0.2);
            box-shadow: 0 15px 30px rgba(0,0,0,0.5);
        }

        .card h2 {
            font-family: 'Syncopate', sans-serif;
            font-size: 1.5rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        /* --- SPECIFIC CARDS --- */
        .hindu-card { grid-column: span 12; border-top: 3px solid var(--hindu-saffron); }
        .jul-card { grid-column: span 6; border-top: 3px solid var(--jul-alien); }
        .roblox-card { grid-column: span 6; border-top: 3px solid var(--roblox-red); }
        .calls-card { grid-column: span 12; border: 1px solid var(--night-purple); background: linear-gradient(135deg, rgba(138, 43, 226, 0.1), transparent); }

        /* --- STATS BARS (TROLL) --- */
        .stat-group { margin-top: 20px; }
        .stat-label { font-size: 0.9rem; color: #888; margin-bottom: 5px; display: flex; justify-content: space-between; }
        .stat-bar { width: 100%; height: 8px; background: #222; border-radius: 10px; overflow: hidden; }
        .stat-fill { height: 100%; border-radius: 10px; }

        /* --- TROLL BUTTON --- */
        .troll-btn {
            margin-top: 30px;
            padding: 15px 30px;
            background: transparent;
            border: 2px solid var(--roblox-red);
            color: var(--roblox-red);
            font-family: 'Syncopate';
            font-weight: bold;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }
        .troll-btn:hover {
            background: var(--roblox-red);
            color: white;
            box-shadow: 0 0 20px rgba(255, 0, 85, 0.5);
        }

        @media (max-width: 900px) {
            .jul-card, .roblox-card { grid-column: span 12; }
        }
    </style>
</head>
<body>

    <canvas id="canvas-bg"></canvas>

    <section class="hero">
        <div class="date-badge">13 JUILLET 2010</div>
        <h1 class="title-glitch">ANUKSHIKA</h1>
        <p class="subtitle">Déesse Sri-Lankaise • Boss de la Zone • Noob sur Roblox</p>
    </section>

    <div class="container">
        
        <!-- HINDOUISME & SRI LANKA -->
        <div class="card hindu-card">
            <h2 style="color: var(--hindu-saffron);"><i class="fa-solid fa-om"></i> SANG SRI-LANKAIS & FORCE COSMIQUE</h2>
            <p style="color: #bbb; line-height: 1.8; font-size: 1.1rem; max-width: 900px;">
                Anukshika ne marche pas, elle lévite. Guidée par la sagesse et l'énergie cosmique, son karma est absolument inatteignable. Héritière d'une culture sri-lankaise millénaire, elle combine la grâce d'une divinité avec le caractère bien trempé de quelqu'un à qui il ne faut surtout pas manquer de respect. 
            </p>
            <div class="stat-group" style="max-width: 500px;">
                <div class="stat-label"><span>Niveau de Karma</span><span>Infini 🕉️</span></div>
                <div class="stat-bar"><div class="stat-fill" style="width: 100%; background: var(--hindu-saffron);"></div></div>
            </div>
            <div class="stat-group" style="max-width: 500px;">
                <div class="stat-label"><span>Tolérance aux épices</span><span>Détruit des estomacs normaux</span></div>
                <div class="stat-bar"><div class="stat-fill" style="width: 100%; background: #ff3300;"></div></div>
            </div>
        </div>

        <!-- JUL -->
        <div class="card jul-card">
            <h2 style="color: var(--jul-alien);"><i class="fa-solid fa-music"></i> D'OR ET DE PLATINE</h2>
            <p style="color: #bbb; line-height: 1.7;">
                Il y a l'Hindouisme, et puis il y a l'autre religion d'Anukshika : JUL. Le sang, la zone, les aliens. Si tu cherches Anukshika, elle est sûrement en train de faire le signe avec les mains en écoutant un vieux son de l'OVNI. Personne ne teste sa playlist.
            </p>
            <div class="stat-group">
                <div class="stat-label"><span>Signes JUL faits par jour</span><span>4 502</span></div>
                <div class="stat-bar"><div class="stat-fill" style="width: 95%; background: var(--jul-alien);"></div></div>
            </div>
        </div>

        <!-- ROBLOX (LE TROLL) -->
        <div class="card roblox-card">
            <h2 style="color: var(--roblox-red);"><i class="fa-solid fa-gamepad"></i> DOSSIER ROBLOX</h2>
            <p style="color: #bbb; line-height: 1.7;">
                Jouer avec elle = garantie de fous rires. Mais on va rétablir la vérité ici : son talent sur Roblox est proche du néant absolu. Elle passe plus de temps à mourir et à faire le bruit "OOF" qu'à gagner. Mais bon, c'est mon duo préféré.
            </p>
            <div class="stat-group">
                <div class="stat-label"><span>Skill / Aim</span><span>Erreur 404 - Introuvable</span></div>
                <div class="stat-bar"><div class="stat-fill" style="width: 5%; background: var(--roblox-red);"></div></div>
            </div>
            <button class="troll-btn" onclick="alert('OOF ! Anukshika est tombée de la map. Encore.')">VOIR SES STATS RÉELLES</button>
        </div>

        <!-- APPELS NOCTURNES -->
        <div class="card calls-card" style="text-align: center; display: flex; flex-direction: column; align-items: center;">
            <h2 style="color: var(--night-purple); justify-content: center;"><i class="fa-solid fa-phone-volume"></i> LES APPELS DE 3H DU MATIN</h2>
            <p style="color: #bbb; line-height: 1.8; max-width: 800px; font-size: 1.1rem; margin-bottom: 20px;">
                C'est notre rituel sacré. Quand la ville dort, nous on refait le monde. On critique tout, on raconte nos vies, on pleure de rire jusqu'à ne plus avoir de voix. Ces moments valent de l'or. T'es bien plus qu'une sœur, t'es ma meilleure pote. Je t'aime de fou. ❤️
            </p>
            <div style="font-size: 3rem; color: var(--night-purple); animation: pulse 2s infinite;">
                <i class="fa-solid fa-heart"></i>
            </div>
        </div>

    </div>

    <script>
        // --- ANIMATION DU FOND ---
        const canvas = document.getElementById('canvas-bg');
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        let particles = [];
        for (let i = 0; i < 80; i++) {
            particles.push({
                x: Math.random() * canvas.width,
                y: Math.random() * canvas.height,
                size: Math.random() * 2,
                speedX: (Math.random() - 0.5) * 0.5,
                speedY: (Math.random() - 0.5) * 0.5,
                color: Math.random() > 0.5 ? '#FFD700' : '#FF671F' // Or et Safran Hindou
            });
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach(p => {
                p.x += p.speedX; p.y += p.speedY;
                if (p.x < 0 || p.x > canvas.width) p.speedX *= -1;
                if (p.y < 0 || p.y > canvas.height) p.speedY *= -1;
                ctx.fillStyle = p.color;
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
                ctx.fill();
            });
            requestAnimationFrame(animate);
        }
        animate();

        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });
    </script>
</body>
</html>
