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
    </style>
</head>
<body>
    <div id="welcome-container">
        <div class="welcome-text">歡迎</div>
        <!-- Add multiple confetti divs for the effect -->
        <div class="confetti" style="background: #FF6347; left: 20%; animation-duration: 2.5s;"></div>
        <div class="confetti" style="background: #FFD700; left: 40%; animation-duration: 3s;"></div>
        <div class="confetti" style="background: #ADFF2F; left: 60%; animation-duration: 2s;"></div>
        <div class="confetti" style="background: #1E90FF; left: 80%; animation-duration: 3.5s;"></div>
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
