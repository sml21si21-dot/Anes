# Anes
Amigo
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anes t7abni? 💕</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ffeef8 0%, #ffd6e7 50%, #ffcccb 100%);
            height: 100vh;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            touch-action: manipulation; /* Prevents zooming when tapping fast */
        }

        .heart {
            position: absolute;
            color: #ff69b4;
            animation: float 6s infinite linear;
            font-size: 20px;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }

        .container {
            text-align: center;
            background: rgba(255, 255, 255, 0.85);
            padding: 40px 20px;
            border-radius: 30px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            backdrop-filter: blur(10px);
            z-index: 10;
            width: 90%;
            max-width: 400px;
        }

        h1 {
            color: #d81b60;
            font-size: 1.8rem;
            margin-bottom: 30px;
        }

        .buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            height: 60px;
        }

        button {
            padding: 12px 30px;
            font-size: 1.1rem;
            font-weight: bold;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.1s;
        }

        #yesBtn {
            background-color: #ff4081;
            color: white;
        }

        #noBtn {
            background-color: #9e9e9e;
            color: white;
            position: absolute; /* Needed for jumping */
        }
    </style>
</head>
<body>

    <div class="heart" style="left: 10%; animation-delay: 0s;">❤️</div>
    <div class="heart" style="left: 40%; animation-delay: 2s;">💖</div>
    <div class="heart" style="left: 70%; animation-delay: 1s;">💗</div>
    <div class="heart" style="left: 90%; animation-delay: 3s;">❤️</div>

    <div class="container">
        <h1>Anes t7abni wla lala ?</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">Iyih</button>
            <button id="noBtn" onpointerover="moveButton(this)" onpointerdown="moveButton(this)">Lala</button>
        </div>
    </div>

    <script>
        function moveButton(btn) {
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        function celebrate() {
            document.querySelector('.container').innerHTML = `
                <h1 style="font-size: 2.5rem;">❤️</h1>
                <h2 style="color: #d81b60;">I knew it! Sahit Anes!</h2>
            `;
        }
    </script>
</body>
</html>
