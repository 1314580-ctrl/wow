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
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
            position: relative;
        }

        /* Welcome animation container */
        #welcome-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.9);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            opacity: 1;
            transition: opacity 1s ease-in-out;
            overflow: hidden;
        }
        .welcome-text {
            font-size: 50px;
            color: #333; /* Keep the text color black */
            text-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
            animation: welcome-animation 3s ease forwards;
            position: relative;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 30px;
            background: #ff0;
            opacity: 0.8;
            animation: confetti-fall 4s infinite;
        }
        @keyframes confetti-fall {
            0% {
                transform: translateY(-100vh) rotate(0deg);
            }
            100% {
                transform: translateY(100vh) rotate(720deg);
            }
        }
        /* Additional confetti colors and positions */
        .confetti:nth-child(1) { background: #FF6347; left: 5%; animation-duration: 2.5s; }
        .confetti:nth-child(2) { background: #FFD700; left: 15%; animation-duration: 3s; }
        .confetti:nth-child(3) { background: #ADFF2F; left: 25%; animation-duration: 2s; }
        .confetti:nth-child(4) { background: #1E90FF; left: 35%; animation-duration: 3.5s; }
        .confetti:nth-child(5) { background: #FF1493; left: 45%; animation-duration: 2.8s; }
        .confetti:nth-child(6) { background: #FF4500; left: 55%; animation-duration: 3.2s; }
        .confetti:nth-child(7) { background: #32CD32; left: 65%; animation-duration: 2.6s; }
        .confetti:nth-child(8) { background: #00BFFF; left: 75%; animation-duration: 3.4s; }
        .confetti:nth-child(9) { background: #FF8C00; left: 85%; animation-duration: 2.7s; }
        .confetti:nth-child(10) { background: #DA70D6; left: 95%; animation-duration: 3s; }
        
        /* Buttons and other styles */
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
        footer {
            margin-top: 20px;
            font-size: 14px;
            color: #666;
        }

        @keyframes welcome-animation {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.1); opacity: 0.8; }
            100% { transform: scale(1); opacity: 0; }
        }
    </style>
</head>
<body>
    <div id="welcome-container">
        <div class="welcome-text">歡迎</div>
        <!-- Add multiple confetti divs for the effect -->
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
        <div class="confetti"></div>
    </div>

    <h1>歡迎來到我的網站</h1>
    <p>在這裡你可以訪問我的 YouTube 頻道和加入我的 Discord 群組。</p>

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

    <footer>© 2024 ru03and1314580。保留所有权利。</footer>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            setTimeout(function() {
                var welcomeContainer = document.getElementById('welcome-container');
                welcomeContainer.style.opacity = '0';
                setTimeout(function() {
                    welcomeContainer.style.display = 'none';
                }, 1000); // Delay to match the transition duration
            }, 3000); // Duration to show the welcome message
        });
    </script>
</body>
</html>
