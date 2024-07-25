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
        }

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
            color: #333;
            text-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .confetti {
            position: absolute;
            width: 10px;
            height: 30px;
            background: #ff0;
            opacity: 0.8;
            animation: confetti-fall 3s infinite;
        }

        @keyframes confetti-fall {
            0% {
                transform: translateY(-100vh) rotate(0deg);
            }
            100% {
                transform: translateY(100vh) rotate(720deg);
            }
        }

        .confetti:nth-child(1) { background: #FF6347; left: 2%; animation-duration: 2.5s; }
        .confetti:nth-child(2) { background: #FFD700; left: 4%; animation-duration: 3s; }
        .confetti:nth-child(3) { background: #ADFF2F; left: 6%; animation-duration: 2s; }
        .confetti:nth-child(4) { background: #1E90FF; left: 8%; animation-duration: 3.5s; }
        .confetti:nth-child(5) { background: #FF1493; left: 10%; animation-duration: 2.8s; }
        .confetti:nth-child(6) { background: #FF4500; left: 12%; animation-duration: 3.2s; }
        .confetti:nth-child(7) { background: #32CD32; left: 14%; animation-duration: 2.6s; }
        .confetti:nth-child(8) { background: #00BFFF; left: 16%; animation-duration: 3.4s; }
        .confetti:nth-child(9) { background: #FF8C00; left: 18%; animation-duration: 2.7s; }
        .confetti:nth-child(10) { background: #DA70D6; left: 20%; animation-duration: 3s; }
        .confetti:nth-child(11) { background: #FF6347; left: 22%; animation-duration: 2.5s; }
        .confetti:nth-child(12) { background: #FFD700; left: 24%; animation-duration: 3s; }
        .confetti:nth-child(13) { background: #ADFF2F; left: 26%; animation-duration: 2s; }
        .confetti:nth-child(14) { background: #1E90FF; left: 28%; animation-duration: 3.5s; }
        .confetti:nth-child(15) { background: #FF1493; left: 30%; animation-duration: 2.8s; }
        .confetti:nth-child(16) { background: #FF4500; left: 32%; animation-duration: 3.2s; }
        .confetti:nth-child(17) { background: #32CD32; left: 34%; animation-duration: 2.6s; }
        .confetti:nth-child(18) { background: #00BFFF; left: 36%; animation-duration: 3.4s; }
        .confetti:nth-child(19) { background: #FF8C00; left: 38%; animation-duration: 2.7s; }
        .confetti:nth-child(20) { background: #DA70D6; left: 40%; animation-duration: 3s; }
        .confetti:nth-child(21) { background: #FF6347; left: 42%; animation-duration: 2.5s; }
        .confetti:nth-child(22) { background: #FFD700; left: 44%; animation-duration: 3s; }
        .confetti:nth-child(23) { background: #ADFF2F; left: 46%; animation-duration: 2s; }
        .confetti:nth-child(24) { background: #1E90FF; left: 48%; animation-duration: 3.5s; }
        .confetti:nth-child(25) { background: #FF1493; left: 50%; animation-duration: 2.8s; }
        .confetti:nth-child(26) { background: #FF4500; left: 52%; animation-duration: 3.2s; }
        .confetti:nth-child(27) { background: #32CD32; left: 54%; animation-duration: 2.6s; }
        .confetti:nth-child(28) { background: #00BFFF; left: 56%; animation-duration: 3.4s; }
        .confetti:nth-child(29) { background: #FF8C00; left: 58%; animation-duration: 2.7s; }
        .confetti:nth-child(30) { background: #DA70D6; left: 60%; animation-duration: 3s; }
        .confetti:nth-child(31) { background: #FF6347; left: 62%; animation-duration: 2.5s; }
        .confetti:nth-child(32) { background: #FFD700; left: 64%; animation-duration: 3s; }
        .confetti:nth-child(33) { background: #ADFF2F; left: 66%; animation-duration: 2s; }
        .confetti:nth-child(34) { background: #1E90FF; left: 68%; animation-duration: 3.5s; }
        .confetti:nth-child(35) { background: #FF1493; left: 70%; animation-duration: 2.8s; }
        .confetti:nth-child(36) { background: #FF4500; left: 72%; animation-duration: 3.2s; }
        .confetti:nth-child(37) { background: #32CD32; left: 74%; animation-duration: 2.6s; }
        .confetti:nth-child(38) { background: #00BFFF; left: 76%; animation-duration: 3.4s; }
        .confetti:nth-child(39) { background: #FF8C00; left: 78%; animation-duration: 2.7s; }
        .confetti:nth-child(40) { background: #DA70D6; left: 80%; animation-duration: 3s; }
        .confetti:nth-child(41) { background: #FF6347; left: 82%; animation-duration: 2.5s; }
        .confetti:nth-child(42) { background: #FFD700; left: 84%; animation-duration: 3s; }
        .confetti:nth-child(43) { background: #ADFF2F; left: 86%; animation-duration: 2s; }
        .confetti:nth-child(44) { background: #1E90FF; left: 88%; animation-duration: 3.5s; }
        .confetti:nth-child(45) { background: #FF1493; left: 90%; animation-duration: 2.8s; }
        .confetti:nth-child(46) { background: #FF4500; left: 92%; animation-duration: 3.2s; }
        .confetti:nth-child(47) { background: #32CD32; left: 94%; animation-duration: 2.6s; }
        .confetti:nth-child(48) { background: #00BFFF; left: 96%; animation-duration: 3.4s; }
        .confetti:nth-child(49) { background: #FF8C00; left: 98%; animation-duration: 2.7s; }
        .confetti:nth-child(50) { background: #DA70D6; left: 100%; animation-duration: 3s; }

        .button {
            display: inline-block;
            color: #fff;
            padding: 20px;
            text-decoration: none;
            font-size: 24px;
            border-radius: 5px;
            margin: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: background-color 0.3s, transform 0.3s;
            position: relative;
            text-align: center;
            min-width: 250px;
            height: 150px;
            vertical-align: middle;
            background-size: cover;
            background-position: center;
            overflow: hidden;
        }

        .button:hover::after {
            content: attr(data-tooltip);
            position: absolute;
            bottom: 100%;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(0, 0, 0, 0.7);
            color: #fff;
            padding: 5px 10px;
            border-radius: 5px;
            white-space: nowrap;
            opacity: 0;
            animation: showTooltip 0.3s forwards;
        }

        @keyframes showTooltip {
            0% {
                opacity: 0;
                transform: translateX(-50%) translateY(10px);
            }
            100% {
                opacity: 1;
                transform: translateX(-50%) translateY(0);
            }
        }

        .button.youtube {
            background-color: #FF0000;
        }

        .button.youtube:hover {
            background-color: #CC0000;
        }

        .button.discord {
            background-color: #7289DA;
        }

        .button.discord:hover {
            background-color: #5b6eae;
        }

        .button.instagram {
            background-color: #C13584;
        }

        .button.instagram:hover {
            background-color: #a02d6d;
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

        /* 添加滚动动画 */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.5s, transform 0.5s;
        }

        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <div id="welcome-container">
        <div class="welcome-text">歡迎來到我的網站</div>
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
        <div class="confetti"></div>
        <div class="confetti"></div>
    </div>

    <audio id="background-music" src="your-music-file.mp3" autoplay loop></audio>

    <h1 class="animate-on-scroll">歡迎來到我的網站</h1>
    <p class="animate-on-scroll">在這裡你可以訪問我的 YouTube 頻道和加入我的 Discord 群組。</p>

    <div class="button-container animate-on-scroll">
        <a href="https://www.youtube.com/channel/UCPl1ALv9iBz0JYNtoYVB-oQ" class="button youtube" data-tooltip="訪問我的 YouTube 頻道">
            <i class="fab fa-youtube"></i>
            <span>YouTube</span>
        </a>
        <a href="https://discord.com/invite/e5cbzGFS3H" class="button discord" data-tooltip="加入我的 Discord 群組">
            <i class="fab fa-discord"></i>
            <span>Discord</span>
        </a>
        <a href="https://www.instagram.com/ru031314580/" class="button instagram" data-tooltip="訪問我的 Instagram">
            <i class="fab fa-instagram"></i>
            <span>ru031314580</span>
        </a>
    </div>

    <div class="video-container animate-on-scroll">
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

    <footer class="animate-on-scroll">
        &copy; 2024 我的網站. 版權所有.
    </footer>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const confettiElements = document.querySelectorAll(".confetti");

            confettiElements.forEach((confetti, index) => {
                confetti.style.left = `${Math.random() * 100}%`;
                confetti.style.animationDelay = `${Math.random() * 2}s`;
            });

            setTimeout(() => {
                document.getElementById('welcome-container').style.opacity = '0';
                setTimeout(() => {
                    document.getElementById('welcome-container').style.display = 'none';
                }, 1000);
            }, 3000);

            const elements = document.querySelectorAll(".animate-on-scroll");
            elements.forEach(element => {
                element.classList.add("visible");
            });
        });
    </script>
</body>
</html>
