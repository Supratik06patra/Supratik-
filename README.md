<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Everything - Puchu ❤️</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Montserrat:wght@300;600&family=Pacifico&display=swap');

        :root {
            --passion-red: #ff0055;
            --rose-gold: #e0aaff;
            --gold: #f1c40f;
            --deep-space: #05051a;
            --neon-pink: #ff00ff;
            --glass: rgba(255, 255, 255, 0.1);
            --peacock-blue: #00a8cc;
            --peacock-green: #2ecc71;
        }

        body, html {
            margin: 0; padding: 0; height: 100%; width: 100%;
            overflow: hidden;
            font-family: 'Montserrat', sans-serif;
            background: var(--deep-space);
            color: white;
            display: flex; justify-content: center; align-items: center;
        }

        #bg-canvas {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            z-index: 1; pointer-events: none;
        }

        /* --- STAGE 0: HARE KRISHNA --- */
        #stage-pre {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            display: flex; flex-direction: column; justify-content: center;
            align-items: center; z-index: 1000; background: var(--deep-space);
            cursor: pointer; transition: opacity 1.5s;
        }

        .krishna-text {
            font-family: 'Great Vibes', cursive;
            font-size: 4rem;
            color: var(--gold);
            text-shadow: 0 0 20px var(--peacock-blue), 0 0 40px var(--peacock-green);
            margin-top: 20px;
            animation: textGlow 2s infinite alternate;
        }

        .feather-container {
            width: 150px;
            height: 250px;
            position: relative;
            animation: featherFloat 4s infinite ease-in-out;
            filter: drop-shadow(0 0 15px var(--peacock-blue));
        }

        @keyframes featherFloat {
            0%, 100% { transform: translateY(0) rotate(5deg); }
            50% { transform: translateY(-30px) rotate(-10deg); }
        }

        @keyframes textGlow {
            from { text-shadow: 0 0 10px var(--gold); }
            to { text-shadow: 0 0 30px var(--peacock-blue), 0 0 50px var(--peacock-green); transform: scale(1.05); }
        }

        /* --- STAGE 1: THE HEART GIFT --- */
        #stage-1 {
            display: none;
            z-index: 10; text-align: center; cursor: pointer;
            transition: opacity 1.5s, transform 1.5s;
        }

        .heart-gift {
            position: relative;
            width: 100px; height: 100px;
            background-color: var(--passion-red);
            transform: rotate(-45deg);
            margin: 0 auto 50px;
            animation: heartPulse 1.2s infinite;
            box-shadow: 0 0 50px rgba(255, 0, 85, 0.6);
        }

        .heart-gift::before, .heart-gift::after {
            content: '';
            position: absolute;
            width: 100px; height: 100px;
            background-color: var(--passion-red);
            border-radius: 50%;
        }

        .heart-gift::before { top: -50px; left: 0; }
        .heart-gift::after { top: 0; left: 50px; }

        @keyframes heartPulse {
            0% { transform: rotate(-45deg) scale(1); }
            15% { transform: rotate(-45deg) scale(1.2); }
            100% { transform: rotate(-45deg) scale(1); }
        }

        .glow-text {
            font-family: 'Great Vibes', cursive;
            font-size: 3rem;
            color: var(--rose-gold);
            text-shadow: 0 0 20px var(--passion-red);
        }

        /* --- STAGE 2: THE REVEAL --- */
        #stage-2 {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            display: none; flex-direction: column; justify-content: center;
            align-items: center; z-index: 20; text-align: center;
        }

        .puchu-title {
            font-family: 'Pacifico', cursive;
            font-size: 4rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #fff, var(--rose-gold), var(--gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: floatUI 3s infinite alternate;
        }

        @keyframes floatUI {
            from { transform: translateY(0); }
            to { transform: translateY(-15px); }
        }

        .message-bubble {
            background: var(--glass);
            backdrop-filter: blur(15px);
            padding: 20px 40px;
            border-radius: 50px;
            border: 1px solid rgba(255,255,255,0.2);
            font-size: 1.2rem;
            margin: 10px;
            opacity: 0;
            transform: translateY(20px);
            transition: 1s;
        }

        /* --- STAGE 5: THE PUZZLE BOX --- */
        #stage-puzzle {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            display: none; flex-direction: column; justify-content: center;
            align-items: center; z-index: 40;
        }

        .magic-box {
            width: 150px; height: 120px;
            background: #4a001e;
            border: 4px solid var(--gold);
            position: relative;
            box-shadow: 0 0 30px var(--gold);
            transition: transform 0.5s;
        }

        .box-lid {
            position: absolute; top: -20px; left: -10px;
            width: 170px; height: 30px;
            background: #7a0031;
            border: 2px solid var(--gold);
            transition: all 0.5s cubic-bezier(0.68, -0.55, 0.27, 1.55);
        }

        .puzzle-heart {
            position: absolute;
            font-size: 2rem;
            cursor: pointer;
            filter: drop-shadow(0 0 10px var(--gold));
            animation: keyFloat 2s infinite alternate;
            z-index: 50;
        }

        @keyframes keyFloat {
            from { transform: scale(1) translateY(0); }
            to { transform: scale(1.2) translateY(-10px); }
        }

        /* --- STAGE 6: THE LETTER --- */
        #stage-letter {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            display: none; justify-content: center; align-items: center;
            z-index: 100; background: rgba(0,0,0,0.8);
        }

        .letter-container {
            width: 300px; height: 400px;
            background: #fffafa;
            color: #333;
            padding: 40px 20px;
            border-radius: 5px;
            box-shadow: 0 0 50px rgba(255,255,255,0.3);
            font-family: 'Great Vibes', cursive;
            font-size: 2.5rem;
            text-align: center;
            transform: scale(0) rotate(-10deg);
            transition: all 1s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            display: flex; flex-direction: column; justify-content: center;
            position: relative;
            user-select: none;
        }

        /* --- GLOBAL EFFECTS --- */
        .flash {
            position: fixed; top:0; left:0; width:100%; height:100%;
            background: white; opacity: 0; z-index: 9999; pointer-events: none;
        }

        #music-btn {
            position: fixed; top: 20px; right: 20px; z-index: 1100;
            background: var(--glass); border: 1px solid white; color: white;
            width: 45px; height: 45px; border-radius: 50%; cursor: pointer;
        }

        .balloon {
            position: absolute; font-size: 2rem; pointer-events: none;
            z-index: 45; animation: balloonFloat 4s linear forwards;
        }

        @keyframes balloonFloat {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.5) rotate(20deg); opacity: 0; }
        }

        .crazy-love-text {
            position: fixed;
            pointer-events: none;
            z-index: 1001;
            font-family: 'Pacifico', cursive;
            text-shadow: 0 0 10px rgba(255,255,255,0.5);
            white-space: nowrap;
        }

    </style>
</head>
<body onclick="handleClick(event)">

    <canvas id="bg-canvas"></canvas>
    <div id="flash-overlay" class="flash"></div>

    <button id="music-btn" onclick="toggleMusic(event)">🎵</button>
    <audio id="bg-music" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3" type="audio/mpeg">
    </audio>

    <!-- Stage 0: Hare Krishna -->
    <div id="stage-pre" onclick="startStage1()">
        <div class="feather-container">
            <svg viewBox="0 0 100 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M50 200C50 200 50 150 50 100C50 50 80 20 50 0C20 20 50 50 50 100" stroke="#00a8cc" stroke-width="2"/>
                <circle cx="50" cy="40" r="15" fill="#00a8cc" fill-opacity="0.6"/>
                <circle cx="50" cy="40" r="10" fill="#2ecc71" fill-opacity="0.8"/>
                <circle cx="50" cy="40" r="5" fill="#f1c40f"/>
                <path d="M50 40L80 20M50 60L85 45M50 80L90 70M50 100L85 105M50 120L80 130" stroke="#00a8cc" stroke-width="1" stroke-linecap="round"/>
                <path d="M50 40L20 20M50 60L15 45M50 80L10 70M50 100L15 105M50 120L20 130" stroke="#00a8cc" stroke-width="1" stroke-linecap="round"/>
            </svg>
        </div>
        <h1 class="krishna-text">Hare Krishna 🙏</h1>
        <p style="opacity: 0.5; font-size: 0.8rem; letter-spacing: 2px; margin-top: 10px;">TAP TO START</p>
    </div>

    <!-- Stage 1 -->
    <div id="stage-1" onclick="startJourney()">
        <div class="heart-gift"></div>
        <h1 class="glow-text">Unlock My Heart, Puchu</h1>
    </div>

    <!-- Stage 2 & 3 (Messages & Vortex) -->
    <div id="stage-2">
        <h1 class="puchu-title">Hey Puchu...</h1>
        <div id="message-container"></div>
    </div>

    <!-- Stage 5: The Puzzle -->
    <div id="stage-puzzle">
        <h2 style="font-family: 'Pacifico'; color: var(--gold); margin-bottom: 50px;">Find 3 Hidden Heart Keys!</h2>
        <div class="magic-box" id="mystery-box">
            <div class="box-lid" id="box-lid"></div>
            <div style="position:absolute; top:40%; width:100%; text-align:center; font-size:0.8rem;">LOCKED</div>
        </div>
    </div>

    <!-- Stage 6: The Final Letter -->
    <div id="stage-letter">
        <div class="letter-container" id="final-letter">
            <div style="font-size: 1.2rem; font-family: 'Montserrat'; color: #ff0055; margin-bottom: 20px;">My Final Vow...</div>
            happy birthday putu putuuu
            <div style="font-size: 1rem; margin-top: 30px;">❤️ Yours Forever ❤️</div>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('bg-canvas');
        const ctx = canvas.getContext('2d');
        const audio = document.getElementById('bg-music');
        let width, height, hearts = [], particles = [];
        let currentStage = 0;
        let keysFound = 0;

        function init() {
            width = canvas.width = window.innerWidth;
            height = canvas.height = window.innerHeight;
            hearts = [];
            for(let i=0; i<50; i++) {
                hearts.push({
                    x: Math.random() * width, y: Math.random() * height,
                    size: 5 + Math.random() * 8, speed: 0.5 + Math.random(),
                    opacity: Math.random() * 0.5
                });
            }
        }
        window.addEventListener('resize', init);
        init();

        function drawHeart(x, y, size, color, alpha) {
            ctx.save();
            ctx.translate(x, y);
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.bezierCurveTo(-size / 2, -size / 2, -size, size / 3, 0, size);
            ctx.bezierCurveTo(size, size / 3, size / 2, -size / 2, 0, 0);
            ctx.fillStyle = color;
            ctx.globalAlpha = alpha;
            ctx.fill();
            ctx.restore();
        }

        function animate() {
            ctx.fillStyle = currentStage === 3 ? 'rgba(30, 0, 15, 0.2)' : 'rgba(5, 5, 26, 0.2)';
            ctx.fillRect(0, 0, width, height);

            hearts.forEach(h => {
                h.y -= h.speed;
                if(h.y < -20) h.y = height + 20;
                let color = currentStage === 0 ? 'var(--peacock-blue)' : (currentStage > 2 ? '#ff00ff' : '#ff0055');
                drawHeart(h.x, h.y, h.size, color, h.opacity);
            });

            particles.forEach((p, i) => {
                p.x += p.vx; p.y += p.vy;
                p.alpha -= 0.01;
                drawHeart(p.x, p.y, p.size, p.color || '#ff0055', p.alpha);
                if(p.alpha <= 0) particles.splice(i, 1);
            });

            requestAnimationFrame(animate);
        }
        animate();

        function triggerFlash() {
            const flash = document.getElementById('flash-overlay');
            flash.style.opacity = '1';
            setTimeout(() => flash.style.opacity = '0', 500);
        }

        function burst(x, y, count=20) {
            for(let i=0; i<count; i++) {
                const angle = Math.random() * Math.PI * 2;
                const speed = Math.random() * 5 + 2;
                particles.push({
                    x, y, vx: Math.cos(angle)*speed, vy: Math.sin(angle)*speed,
                    alpha: 1, size: Math.random()*10+5, color: currentStage === 0 ? 'var(--peacock-green)' : `hsl(${Math.random()*360}, 100%, 70%)`
                });
            }
        }

        function startStage1() {
            triggerFlash();
            currentStage = 1;
            document.getElementById('stage-pre').style.opacity = '0';
            setTimeout(() => {
                document.getElementById('stage-pre').style.display = 'none';
                document.getElementById('stage-1').style.display = 'block';
            }, 1000);
        }

        function startJourney() {
            audio.play().catch(()=>{});
            document.getElementById('stage-1').style.opacity = '0';
            setTimeout(() => {
                document.getElementById('stage-1').style.display = 'none';
                document.getElementById('stage-2').style.display = 'flex';
                currentStage = 2;
                runMessages();
            }, 1000);
        }

        async function runMessages() {
            const container = document.getElementById('message-container');
            const messages = [
                "You are the most beautiful person I know... ❤️",
                "I fall for you more every single day 💖",
                "You're not just my lover, you're my best friend 💍",
                "Now... solve the mystery of my love!"
            ];
            for(let msg of messages) {
                const b = document.createElement('div');
                b.className = 'message-bubble';
                b.innerText = msg;
                container.appendChild(b);
                setTimeout(() => b.style.opacity = '1', 100);
                await new Promise(r => setTimeout(r, 2000));
            }
            setTimeout(showPuzzle, 1000);
        }

        function showPuzzle() {
            triggerFlash();
            document.getElementById('stage-2').style.display = 'none';
            document.getElementById('stage-puzzle').style.display = 'flex';
            currentStage = 5;
            spawnKeys();
        }

        function spawnKeys() {
            for(let i=0; i<3; i++) {
                const key = document.createElement('div');
                key.className = 'puzzle-heart';
                key.innerHTML = '🔑❤️';
                key.style.left = (Math.random() * 80 + 10) + 'vw';
                key.style.top = (Math.random() * 80 + 10) + 'vh';
                key.onclick = (e) => {
                    e.stopPropagation();
                    keysFound++;
                    burst(e.clientX, e.clientY, 10);
                    key.remove();
                    if(keysFound === 3) unlockBox();
                };
                document.getElementById('stage-puzzle').appendChild(key);
            }
        }

        function unlockBox() {
            const box = document.getElementById('mystery-box');
            const lid = document.getElementById('box-lid');
            triggerFlash();
            box.style.transform = 'scale(1.2)';
            lid.style.transform = 'translateY(-100px) rotate(45deg)';
            lid.style.opacity = '0';
            for(let i=0; i<30; i++) setTimeout(createBalloon, i * 50);
            setTimeout(() => {
                document.getElementById('stage-puzzle').style.opacity = '0';
                setTimeout(showFinalLetter, 1000);
            }, 2000);
        }

        function createBalloon() {
            const b = document.createElement('div');
            b.className = 'balloon';
            b.innerText = ['🎈','💖','🎈','💝'][Math.floor(Math.random()*4)];
            b.style.left = (window.innerWidth/2 + (Math.random()*100 - 50)) + 'px';
            b.style.top = (window.innerHeight/2) + 'px';
            document.body.appendChild(b);
            setTimeout(() => b.remove(), 4000);
        }

        function showFinalLetter() {
            document.getElementById('stage-puzzle').style.display = 'none';
            document.getElementById('stage-letter').style.display = 'flex';
            currentStage = 6;
            setTimeout(() => {
                const letter = document.getElementById('final-letter');
                letter.style.transform = 'scale(1) rotate(0deg)';
                setInterval(() => burst(Math.random()*width, Math.random()*height, 5), 500);
            }, 500);
        }

        function handleClick(e) {
            if (currentStage === 0) {
                burst(e.clientX, e.clientY, 20);
                return;
            }
            burst(e.clientX, e.clientY, currentStage === 6 ? 30 : 15);
            showLoveText(e.clientX, e.clientY);
        }

        function showLoveText(x, y) {
            const txt = document.createElement('div');
            txt.className = 'crazy-love-text';
            txt.style.left = x + 'px';
            txt.style.top = y + 'px';
            const colors = ['#ff0055', '#ff00ff', '#f1c40f', '#00d2ff', '#ffffff', '#e0aaff', '#2ecc71'];
            txt.style.color = colors[Math.floor(Math.random() * colors.length)];
            const size = currentStage === 6 ? (2.5 + Math.random() * 2) : (1.5 + Math.random() * 1);
            txt.style.fontSize = size + 'rem';
            txt.innerText = "I Love You";
            document.body.appendChild(txt);
            const destX = (Math.random() - 0.5) * 400;
            const destY = -300 - Math.random() * 200;
            const rotation = (Math.random() - 0.5) * 90;
            txt.animate([
                { transform: 'translate(-50%, -50%) scale(0.5) rotate(0deg)', opacity: 1 },
                { transform: `translate(calc(-50% + ${destX}px), ${destY}px) scale(${currentStage === 6 ? 2.5 : 1.5}) rotate(${rotation}deg)`, opacity: 0 }
            ], { duration: 2000, easing: 'cubic-bezier(0.175, 0.885, 0.32, 1.275)', fill: 'forwards' });
            setTimeout(() => txt.remove(), 2000);
        }

        function toggleMusic(e) {
            e.stopPropagation();
            if(audio.paused) { audio.play(); e.target.innerText = "🎵"; }
            else { audio.pause(); e.target.innerText = "🔇"; }
        }
    </script>
</body>
</html>

