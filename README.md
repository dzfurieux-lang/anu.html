<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>ANUKSHIKA - LA BOSS DU GAMING</title>
    <style>
        /* LE PIRE DESIGN DU MONDE (VOLONTAIRE) */
        body {
            background-color: #ff00ff; /* Rose flashy qui pique les yeux */
            background-image: url('https://www.transparenttextures.com/patterns/cubes.png');
            font-family: "Comic Sans MS", "Comic Sans", cursive; /* La police la plus troll */
            color: #00ff00; /* Vert fluo */
            text-align: center;
            overflow-x: hidden;
        }

        .container {
            border: 10px dashed yellow;
            margin: 20px;
            padding: 20px;
            background: rgba(0,0,0,0.7);
        }

        marquee {
            font-size: 30px;
            font-weight: bold;
            background: yellow;
            color: black;
        }

        .jul-zone {
            border: 5px solid #00A3E0;
            padding: 20px;
            margin: 20px;
            animation: shake 0.5s infinite; /* Jul qui tremble de puissance */
        }

        @keyframes shake {
            0% { transform: translate(1px, 1px) rotate(0deg); }
            10px { transform: translate(-1px, -2px) rotate(-1deg); }
            20px { transform: translate(-3px, 0px) rotate(1deg); }
            100% { transform: translate(1px, -1px) rotate(0deg); }
        }

        .roblox-noob {
            width: 150px;
            cursor: pointer;
            transition: 0.2s;
        }

        .roblox-noob:active {
            transform: scale(1.5) rotate(360deg);
        }

        .btn-troll {
            background: red;
            color: white;
            font-size: 25px;
            padding: 20px;
            border: 5px outset white;
            cursor: pointer;
        }

        .btn-troll:hover {
            position: absolute;
            top: Math.random();
            left: Math.random();
        }

        .sri-lanka-power {
            font-size: 50px;
            text-shadow: 5px 5px #8D153A;
        }

        .date-anniv {
            font-size: 100px;
            color: gold;
            -webkit-text-stroke: 2px black;
        }

        #secret-msg {
            display: none;
            font-size: 50px;
            color: white;
            background: black;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: 9999;
            padding-top: 200px;
        }
    </style>
</head>
<body>

    <marquee scrollamount="20">⚠️ ALERTE : ANUKSHIKA EST DANS LE SECTEUR ⚠️ C'EST PAS DES LOL ⚠️ TEAM JUL EN FORCE ⚠️</marquee>

    <div class="container">
        <h1 class="sri-lanka-power">🇱🇰 REINE DU SRI LANKA 🇱🇰</h1>
        <p>Née le 13 Juillet 2010 pour dominer le monde (et Roblox)</p>
        
        <div class="date-anniv">13/07/2010</div>

        <div class="jul-zone">
            <h2>🤘 SECTION "LE J C'EST LE S" 🤘</h2>
            <p>"En bande organisée, personne peut nous canaliser !"</p>
            <p>Anukshika quand elle entend Jul : 💃🕺✨</p>
            <button onclick="jouerSon()">CLIQUE POUR LE SIGNE JUL</button>
        </div>

        <div class="roblox-zone">
            <h2>🎮 ROBLOX ADDICT 🎮</h2>
            <p>Clique sur le Noob pour entendre son cri de guerre :</p>
            <img src="https://upload.wikimedia.org/wikipedia/commons/3/3a/Roblox_player_icon_black.svg" class="roblox-noob" onclick="oof()" alt="Noob">
            <p>(C'est Anukshika quand elle perd contre son frère ça 😂)</p>
        </div>

        <div class="call-zone">
            <h2>📱 LES APPELS DE 3H DU MATIN 📱</h2>
            <p>Statut actuel : En train de raconter des bêtises au téléphone.</p>
            <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHJqbmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/3o7TKMGpxas34AnT7W/giphy.gif" width="200">
        </div>

        <br>
        <button class="btn-troll" id="moveBtn">CLIQUE ICI POUR UN CADEAU</button>
    </div>

    <div id="secret-msg" onclick="this.style.display='none'">
        TU AS RÉUSSI À CLIQUER ! <br>
        ANUKSHIKA T'ES LA MEILLEURE SŒUR <br>
        MÊME SI TU ES UNE NOOB À ROBLOX ! ❤️
    </div>

    <script>
        // Le bouton qui s'enfuit (TROLL)
        const btn = document.getElementById('moveBtn');
        btn.addEventListener('mouseover', () => {
            btn.style.position = 'absolute';
            btn.style.top = Math.random() * 80 + 'vh';
            btn.style.left = Math.random() * 80 + 'vw';
        });

        btn.addEventListener('click', () => {
            document.getElementById('secret-msg').style.display = 'block';
        });

        function oof() {
            alert("OOF! (Bruit de mort Roblox)");
        }

        function jouerSon() {
            alert("JUL DIT : MERCEEEE MA TEAM ! 🤘💙");
        }
    </script>

    <marquee direction="right" scrollamount="15">
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHJqbmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/126Atuf8ZpQsQE/giphy.gif" width="100">
        JE T'AIME ENORMEMENT MA SOEUR D'AMOUR ! 🤘🇱🇰🎮
    </marquee>

</body>
</html>
