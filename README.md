<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anukshika | La Légende</title>
    <link href="https://fonts.googleapis.com/css2?family=Syncopate:wght@400;700&family=Montserrat:wght@300;400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        :root {
            --gold: #D4AF37;
            --sri-lanka-red: #8D153A;
            --jul-blue: #00A3E0;
            --dark: #0a0a0a;
            --glass: rgba(255, 255, 255, 0.05);
            --accent: #ff007a;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--dark);
            color: white;
            font-family: 'Montserrat', sans-serif;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* --- BACKGROUND ANIMATION --- */
        .bg-glow {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 50% 50%, #1a1a2e 0%, #0a0a0a 100%);
            z-index: -2;
        }

        .orbit {
            position: fixed;
            top: 50%; left: 50%;
            width: 600px; height: 600px;
            border: 1px solid rgba(212, 175, 55, 0.1);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            z-index: -1;
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate { from { transform: translate(-50%, -50%) rotate(0deg); } to { transform: translate(-50%, -50%) rotate(360deg); } }

        /* --- HERO SECTION --- */
        header {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }

        .badge-date {
            background: var(--gold);
            color: black;
            padding: 5px 15px;
            font-weight: 700;
            border-radius: 20px;
            font-size: 0.9rem;
            margin-bottom: 20px;
            letter-spacing: 2px;
            animation: fadeIn 1s ease;
        }

        h1 {
            font-family: 'Syncopate', sans-serif;
            font-size: clamp(3rem, 10vw, 8rem);
            text-transform: uppercase;
            line-height: 0.9;
            background: linear-gradient(to bottom, #fff 30%, var(--gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
        }

        .slogan {
            font-size: 1.2rem;
            letter-spacing: 5px;
            color: var(--jul-blue);
            text-transform: uppercase;
            font-weight: 300;
        }

        /* --- SECTION GRID --- */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 100px 20px;
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            gap: 25px;
        }

        .card {
            background: var(--glass);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 30px;
            padding: 40px;
            transition: 0.4s;
        }

        .card:hover {
            border-color: var(--gold);
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.5);
        }

        /* Profile Card */
        .profile { grid-column: span 7; position: relative; overflow: hidden; }
        .origin-tag { color: var(--gold); font-weight: 700; display: flex; align-items: center; gap: 10px; margin-bottom: 15px;}
        
        /* Jul Card */
        .jul-card { 
            grid-column: span 5; 
            background: linear-gradient(135deg, rgba(0, 163, 224, 0.2), rgba(0,0,0,0.5));
            display: flex; flex-direction: column; align-items: center; justify-content: center;
        }
        .signe-jul { font-size: 5rem; color: var(--jul-blue); margin-bottom: 15px; animation: pulse 2s infinite; }

        /* Roblox Card */
        .roblox-card { 
            grid-column: span 6; 
            background: linear-gradient(135deg, rgba(255, 0, 0, 0.1), rgba(0,0,0,0.5));
        }
        .stat-grid { display: flex; gap: 20px; margin-top: 20px; }
        .stat-item { background: rgba(0,0,0,0.3); padding: 15px; border-radius: 15px; flex: 1; text-align: center; }

        /* Night Call Card */
        .call-card { 
            grid-column: span 6; 
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            border-left: 5px solid var(--accent);
        }

        /* --- BUTTONS & INTERACTION --- */
        .btn-action {
            margin-top: 50px;
            padding: 20px 40px;
            background: none;
            border: 1px solid var(--gold);
            color: var(--gold);
            font-family: 'Syncopate';
            cursor: pointer;
            border-radius: 50px;
            transition: 0.3s;
            overflow: hidden;
            position: relative;
        }

        .btn-action:hover {
            background: var(--gold);
            color: black;
        }

        /* --- ANIMATIONS --- */
        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.1); opacity: 1; }
            100% { transform: scale(1); opacity: 0.8; }
        }

        .flying-emoji {
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            animation: fly 3s forwards ease-out;
        }

        @keyframes fly {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-500px) rotate(360deg); opacity: 0; }
        }

        footer {
            text-align: center;
            padding: 50px;
            font-size: 0.8rem;
            letter-spacing: 2px;
            opacity: 0.5;
        }

        /* Mobile */
        @media (max-width: 900px) {
            .profile, .jul-card, .roblox-card, .call-card { grid-column: span 12; }
        }
    </style>
</head>
<body>

    <div class="bg-glow"></div>
    <div class="orbit"></div>

    <header>
        <div class="badge-date">13 JUILLET 2010</div>
        <h1>ANUKSHIKA</h1>
        <p class="slogan">Sri Lankan Queen • Team Jul • Roblox Pro</p>
        <button class="btn-action" onclick="megaBoost()">ACTIVER LE MODE HAGOUN</button>
    </header>

    <div class="container">
        <div class="card profile">
            <div class="origin-tag"><i class="fas fa-gem"></i> L'ÉLITE DU SRI LANKA</div>
            <h2>Identité Royale</h2>
            <p style="margin-top: 20px; line-height: 1.8; opacity: 0.8;">
                Originaire du pays de l'or et du thé, Anukshika porte en elle la force de ses racines. 
                Une personnalité rare, un mélange de douceur et de caractère qui impose le respect. 
                Elle n'est pas juste une sœur, c'est un trésor national.
            </p>
            <div style="margin-top: 30px; font-weight: 700; color: var(--gold);">
                STATUT : IRREMPLAÇABLE
            </div>
        </div>

        <div class="card jul-card">
            <div class="signe-jul">🤘</div>
            <h2 style="color: var(--jul-blue);">D'OR ET DE PLATINE</h2>
            <p style="text-align: center; margin-top: 10px;">"C'est pas des LOL", Anukshika est la fan n°1. Le J c'est la famille, le sang, la zone.</p>
            <div style="margin-top: 20px; font-family: 'Syncopate'; font-size: 0.7rem; color: var(--jul-blue);">PLAYLIST : 100% OVNI</div>
        </div>

        <div class="card roblox-card">
            <h2><i class="fas fa-gamepad"></i> ROBLOX GAMING</h2>
            <p>Notre terrain de jeu, nos délires, nos victoires. Personne ne nous teste sur les serveurs.</p>
            <div class="stat-grid">
                <div class="stat-item">
                    <div style="color: var(--gold); font-weight: 700;">DUO</div>
                    <div style="font-size: 0.8rem;">Invaincu</div>
                </div>
                <div class="stat-item">
                    <div style="color: var(--gold); font-weight: 700;">SKILL</div>
                    <div style="font-size: 0.8rem;">Maximum</div>
                </div>
                <div class="stat-item">
                    <div style="color: var(--gold); font-weight: 700;">FUN</div>
                    <div style="font-size: 0.8rem;">Infini</div>
                </div>
            </div>
        </div>

        <div class="card call-card">
            <h2><i class="fas fa-moon"></i> LES APPELS DU SOIR</h2>
            <p style="margin-top: 15px; font-style: italic; opacity: 0.9;">
                "Quand le monde s'endort, nos discussions commencent."
            </p>
            <p style="margin-top: 10px; font-size: 0.9rem;">
                C'est là que les secrets se partagent, que les fous rires éclatent et que notre lien devient indestructible. 
                Des heures au téléphone à refaire le monde, c'est notre rituel sacré.
            </p>
        </div>
    </div>

    <footer>
        DÉVELOPPÉ AVEC UN AMOUR INFINI POUR LA MEILLEURE DES SŒURS <br>
        ANUKSHIKA © 2024 - ÉDITION LIMITÉE
    </footer>

    <script>
        function megaBoost() {
            const emojis = ['👑', '💎', '🤘', '💙', '🇱🇰', '🎮', '✨'];
            for(let i=0; i<30; i++) {
                setTimeout(() => {
                    const e = document.createElement('div');
                    e.className = 'flying-emoji';
                    e.innerHTML = emojis[Math.floor(Math.random() * emojis.length)];
                    e.style.left = Math.random() * 100 + 'vw';
                    e.style.top = '100vh';
                    e.style.fontSize = (Math.random() * 30 + 20) + 'px';
                    document.body.appendChild(e);
                    
                    setTimeout(() => e.remove(), 3000);
                }, i * 100);
            }
            alert("MODE HAGOUN ACTIVÉ : Anukshika est officiellement la boss du site !");
        }
    </script>
</body>
</html>
