<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的 YouTube 和 Discord</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            overflow-x: hidden;
            background-color: #f0f0f0;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        #welcome-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 1s ease;
        }

        .welcome-text {
            font-size: 48px;
            color: #fff;
            margin: 0;
        }

        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: #FF0;
            border-radius: 50%;
            pointer-events: none;
            animation: confetti 3s infinite;
        }

        @keyframes confetti {
            0% { transform: translateY(-100vh) rotate(0); opacity: 1; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
        }

        /* 多个彩带 */
        .confetti:nth-child(1) { background: #FF5733; left: 10%; animation-duration: 2.5s; }
        .confetti:nth-child(2) { background: #33FF57; left: 20%; animation-duration: 3s; }
        .confetti:nth-child(3) { background: #3357FF; left: 30%; animation-duration: 2.8s; }
        .confetti:nth-child(4) { background: #FF33A1; left: 40%; animation-duration: 3.2s; }
        .confetti:nth-child(5) { background: #FFD433; left: 50%; animation-duration: 3.4s; }
        .confetti:nth-child(6) { background: #33FFD4; left: 60%; animation-duration: 2.7s; }
        .confetti:nth-child(7) { background: #FF6F33; left: 70%; animation-duration: 3s; }
        .confetti:nth-child(8) { background: #A133FF; left: 80%; animation-duration: 2.9s; }
        .confetti:nth-child(9) { background: #33FF6F; left: 90%; animation-duration: 3.1s; }
        .confetti:nth-child(10) { background: #FF33F6; left: 100%; animation-duration: 2.8s; }

        /* 动画 */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.5s, transform 0.5s;
        }

        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
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

    <footer>
        © 2024 ru03and1314580。保留所有权利。
    </footer>

    <script>
        // 滚动动画
        document.addEventListener('scroll', function() {
            var elements = document.querySelectorAll('.animate-on-scroll');
            elements.forEach(function(element) {
                var elementPosition = element.getBoundingClientRect();
                if (elementPosition.top < window.innerHeight && elementPosition.bottom > 0) {
                    element.classList.add('visible');
                }
            });
        });

        // 隐藏欢迎界面
        setTimeout(function() {
            document.getElementById('welcome-container').style.opacity = 0;
            setTimeout(function() {
                document.getElementById('welcome-container').style.display = 'none';
            }, 1000);
        }, 5000);
    </script>
</body>
</html>
