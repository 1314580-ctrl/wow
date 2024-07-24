<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的 YouTube 和 Discord</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            margin: 0; 
            padding: 0; 
            background-image: url('https://lh3.googleusercontent.com/drive-viewer/AKGpihb_12-nCE4alfZCi4zr8s7ThfOtYAXws4oeL220b5jPBar56cG20MY7NlknwrVY4aFOwWlXcV0TZGOV6jTulQnhFTiTPkqZrJQ=w1366-h641-rw-v1'); 
            background-size: cover; 
            background-position: center; 
            background-repeat: no-repeat; 
            text-align: center; 
            display: flex; 
            flex-direction: column; 
            justify-content: center; 
            align-items: center; 
            height: 100vh;
            overflow: hidden;
        }

        .welcome-text {
            font-size: 72px; /* Increased size */
            color: #fff;
            position: relative;
            opacity: 1;
            animation: fadeOut 5s forwards; /* Increased duration */
        }

        .confetti {
            position: absolute;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            pointer-events: none;
            overflow: hidden;
        }

        .confetti div {
            position: absolute;
            width: 15px; /* Increased size */
            height: 15px; /* Increased size */
            background: rgba(255, 255, 255, 0.7);
            border-radius: 50%;
            opacity: 0;
            animation: confettiDrop 2s infinite;
        }

        @keyframes confettiDrop {
            0% {
                opacity: 1;
            }
            100% {
                opacity: 0;
            }
        }

        @keyframes fadeOut {
            0% {
                opacity: 1;
            }
            100% {
                opacity: 0;
            }
        }

        .confetti.top-left div { animation: confettiTopLeft 3s infinite; }
        .confetti.top-right div { animation: confettiTopRight 3s infinite; }
        .confetti.bottom-left div { animation: confettiBottomLeft 3s infinite; }
        .confetti.bottom-right div { animation: confettiBottomRight 3s infinite; }

        @keyframes confettiTopLeft {
            0% { transform: translate(0, 0); }
            100% { transform: translate(-100vw, -100vh); }
        }

        @keyframes confettiTopRight {
            0% { transform: translate(0, 0); }
            100% { transform: translate(100vw, -100vh); }
        }

        @keyframes confettiBottomLeft {
            0% { transform: translate(0, 0); }
            100% { transform: translate(-100vw, 100vh); }
        }

        @keyframes confettiBottomRight {
            0% { transform: translate(0, 0); }
            100% { transform: translate(100vw, 100vh); }
        }

        .button {
            display: inline-block;
            color: #fff;
            padding: 20px;
            text-decoration: none;
            font-size: 24px;
            border-radius: 5px;
            margin: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
            position: relative;
            text-align: center;
            min-width: 250px;
            height: 150px;
            background-size: cover;
            background-position: center;
            overflow: hidden;
        }
        .button:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
        }
        .button:active {
            transform: scale(0.95);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        .button.youtube {
            background-color: #FF0000;
            background: linear-gradient(45deg, #FF0000, #CC0000);
        }
        .button.discord {
            background-color: #7289DA;
            background: linear-gradient(45deg, #7289DA, #5b6eae);
        }
        .button.instagram {
            background-color: #C13584;
            background: linear-gradient(45deg, #C13584, #a02d6d);
        }
        .button i {
            font-size: 50px;
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
        }
        .button span {
            display: block;
            font-size: 18px;
            margin-top: 60px;
        }
        .button-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        .video-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        .video-section {
            flex: 1;
            max-width: 45%;
            padding: 10px;
            border-radius: 10px;
            position: relative;
        }
        .video-section .icon {
            font-size: 40px;
            position: absolute;
            top: 10px;
            left: 10px;
            color: #fff;
        }
        .video-section .title {
            position: absolute;
            top: 10px;
            left: 60px;
            font-size: 18px;
            color: #fff;
        }
        .video-section iframe {
            width: 100%;
            height: calc(100% - 80px);
            display: block;
            border: none;
            margin-top: 60px;
        }
    </style>
</head>
<body>
    <div class="welcome-text">歡迎來到我的網站！</div>

    <div class="confetti top-left"></div>
    <div class="confetti top-right"></div>
    <div class="confetti bottom-left"></div>
    <div class="confetti bottom-right"></div>

    <h1 style="font-size: 36px; color: #333;">歡迎來到我的網站</h1>
    <p style="font-size: 18px; color: #666;">在這裡你可以訪問我的 YouTube 頻道和加入我的 Discord 群組。</p>

    <div class="button-container">
        <a href="https://www.youtube.com/channel/UCPl1ALv9iBz0JYNtoYVB-oQ" class="button youtube">
            <i class="fab fa-youtube"></i>
            <span>YouTube</span>
        </a>
        <a href="https://discord.com/invite/e5cbzGFS3H" class="button discord">
            <i class="fab fa-discord"></i>
            <span>Discord</span>
        </a>
        <a href="https://www.instagram.com/ru031314580/" class="button instagram">
            <i class="fab fa-instagram"></i>
            <span>ru031314580</span>
        </a>
    </div>

    <div class="video-container">
        <div class="video-section" style="background-color: #FF0000;">
            <i class="fab fa-youtube icon"></i>
            <span class="title">YouTube 最多觀看量</span>
            <iframe src="https://www.youtube.com/embed/JMNBEQ_xBi8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video-section" style="background-color: #C13584;">
            <i class="fab fa-instagram icon"></i>
            <span class="title">Instagram 視頻</span>
            <iframe src="https://www.instagram.com/reel/C5akynxJREi/embed" frameborder="0" allowfullscreen></iframe>
        </div>
    </div>

    <footer style="margin-top: 20px; font-size: 14px; color: #666;">
        © 2024 ru03and1314580。保留所有权利。
    </footer>

    <script>
        // Create a function to add more confetti pieces dynamically
        function generateConfetti() {
            const confettiContainers = document.querySelectorAll('.confetti');
            confettiContainers.forEach(container => {
                for (let i = 0; i < 100; i++) { // Increased number of confetti pieces
                    const confettiPiece = document.createElement('div');
                    confettiPiece.style.top = `${Math.random() * 100}vh`;
                    confettiPiece.style.left = `${Math.random() * 100}vw`;
                    confettiPiece.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 70%)`;
                    confettiPiece.style.animationDelay = `${Math.random() * 4}s`;
                    container.appendChild(confettiPiece);
                }
            });
        }

        // Generate confetti when the page loads
        window.onload = generateConfetti;
    </script>
</body>
</html>
