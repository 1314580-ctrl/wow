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
            position: relative;
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

        .confetti:nth-child(odd) {
            background: #FF6347;
            left: calc(100% * var(--i) / 50);
            animation-duration: calc(2.5s + (var(--i) * 0.1s));
        }

        .confetti:nth-child(even) {
            background: #FFD700;
            left: calc(100% * var(--i) / 50);
            animation-duration: calc(2.5s + (var(--i) * 0.1s));
        }

        .confetti:nth-child(3n) {
            background: #ADFF2F;
            left: calc(100% * var(--i) / 50);
            animation-duration: calc(2.5s + (var(--i) * 0.1s));
        }

        .confetti:nth-child(4n) {
            background: #1E90FF;
            left: calc(100% * var(--i) / 50);
            animation-duration: calc(2.5s + (var(--i) * 0.1s));
        }

        #confetti-line {
            position: absolute;
            top: 50%;
            left: 0;
            width: 100%;
            height: 10px;
            overflow: hidden;
            pointer-events: none;
        }

        .confetti-line {
            position: absolute;
            top: 0;
            width: 100%;
            height: 10px;
            background: rgba(0, 0, 0, 0);
            display: flex;
            justify-content: space-between;
            align-items: center;
            pointer-events: none;
        }

        .confetti-line .confetti {
            position: relative;
            width: 10px;
            height: 30px;
            background: #FF6347;
            animation: confetti-line-fall 2s infinite;
        }

        @keyframes confetti-line-fall {
            0% {
                transform: translateY(-100%);
            }
            100% {
                transform: translateY(100%);
            }
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
    </div>

    <div id="confetti-line">
        <div class="confetti-line">
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
