<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pour Anukshika 💖</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Playfair+Display:ital,wght@1,700&display=swap" rel="stylesheet">
    <style>
        /* Variables de couleurs et style de base */
        :root {
            --primary: #ff7eb3;
            --secondary: #ff758c;
            --dark: #2b2d42;
            --light: #edf2f4;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body, html {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #2b2d42, #8d99ae);
            color: var(--light);
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* Effet d'arrière-plan animé */
        .background-blobs {
            position: fixed;
            top: 0; left: 0; width: 100vw; height: 100vh;
            z-index: -1;
            overflow: hidden;
        }
        .blob {
            position: absolute;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 50%;
            filter: blur(80px);
            opacity: 0.6;
            animation: float 10s infinite alternate ease-in-out;
        }
        .blob1 { width: 400px; height: 400px; top: -100px; left: -100px; }
        .blob2 { width: 300px; height: 300px; bottom: -50px; right: -50px; animation-duration: 12s; }

        @keyframes float {
            0% { transform: translateY(0px) scale(1); }
            100% { transform: translateY(50px) scale(1.1); }
        }

        /* En-tête (Hero Section) */
        header {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 5rem;
            background: -webkit-linear-gradient(var(--primary), #ffd166);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
            text-shadow: 0px 10px 20px rgba(0,0,0,0.2);
            animation: fadeInDown 1.5s ease;
        }
        p.subtitle {
            font-size: 1.5rem;
            font-weight: 300;
            letter-spacing: 2px;
            margin-bottom: 40px;
            animation: fadeInUp 1.5s ease 0.5s both;
        }

        /* Bouton interactif */
        .btn-love {
            padding: 15px 40px;
            font-size: 1.2rem;
            font-weight: 600;
            color: white;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            border: none;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 10px 20px rgba(255, 117, 140, 0.4);
            transition: transform 0.3s, box-shadow 0.3s;
            animation: fadeInUp 1.5s ease 1s both;
        }
        .btn-love:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 25px rgba(255, 117, 140, 0.6);
        }

        /* Section Contenu (Glassmorphism) */
        .content-section {
            padding: 100px 20px;
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        .glass-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
        }
        .glass-card h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: #ffd166;
        }

        /* Animations d'apparition */
        @keyframes fadeInDown { from { opacity: 0; transform: translateY(-30px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }

        /* Cœurs volants générés par JS */
        .floating-heart {
            position: fixed;
            bottom: -50px;
            font-size: 2rem;
            animation: flyUp 3s linear forwards;
            pointer-events: none;
        }
        @keyframes flyUp {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.5) rotate(45deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <!-- Arrière-plan animé -->
    <div class="background-blobs">
        <div class="blob blob1"></div>
        <div class="blob blob2"></div>
    </div>

    <!-- En-tête -->
    <header>
        <h1>Anukshika</h1>
        <p class="subtitle">La meilleure des sœurs au monde ✨</p>
        <button class="btn-love" onclick="sendLove()">Clique pour une dose d'amour</button>
    </header>

    <!-- Cartes d'informations (Glassmorphism) -->
    <section class="content-section">
        <div class="glass-card">
            <h3>💖 Une âme en or</h3>
            <p>Tu as un cœur immense. Ta bienveillance et ta façon de prendre soin des autres font de toi une personne irremplaçable dans ma vie.</p>
        </div>
        <div class="glass-card">
            <h3>🌟 Une force incroyable</h3>
            <p>Rien ne t'arrête. Ton courage et ta détermination m'inspirent au quotidien. Ne doute jamais de ce que tu es capable d'accomplir.</p>
        </div>
        <div class="glass-card">
            <h3>✨ Notre lien unique</h3>
            <p>Plus qu'une sœur, tu es ma moitié. Les fous rires, les confidences... Aucun mot ne suffit pour décrire à quel point je t'aime.</p>
        </div>
    </section>

    <script>
        // Fonction JavaScript pour créer des cœurs qui volent
        function sendLove() {
            const colors = ['#ff7eb3', '#ff758c', '#ffd166', '#ffb5a7'];
            
            for(let i = 0; i < 15; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.innerHTML = '❤️';
                    heart.classList.add('floating-heart');
                    
                    // Positionnement et style aléatoires
                    heart.style.left = Math.random() * 100 + 'vw';
                    heart.style.color = colors[Math.floor(Math.random() * colors.length)];
                    heart.style.fontSize = (Math.random() * 2 + 1) + 'rem';
                    heart.style.animationDuration = (Math.random() * 2 + 2) + 's';
                    
                    document.body.appendChild(heart);
                    
                    // Supprimer le cœur après l'animation
                    setTimeout(() => {
                        heart.remove();
                    }, 4000);
                }, i * 100); // Décalage pour un effet d'explosion en rafale
            }
        }
    </script>
</body>
</html>
