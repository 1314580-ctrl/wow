<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的 YouTube 和 Discord</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
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
            height: auto;
            vertical-align: middle;
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
            font-size: 40px;
            position: absolute;
            top: 10px;
            left: 10px;
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
            max-width: 100%;
            padding: 10px;
            border-radius: 10px;
        }
        .video-section iframe {
            width: 100%;
            height: 300px;
            display: block;
            border: none;
        }
        .video-section .youtube-icon {
            top: 10px;
            left: 10px;
        }
    </style>
</head>
<body style="margin: 0; padding: 0; background-color: #f0f0f0; text-align: center; display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100vh;">

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
        <div class="video-section">
            <div class="button youtube" style="display: block; position: relative;">
                <i class="fab fa-youtube"></i>
                <span style="position: absolute; top: 10px; left: 50%; transform: translateX(-50%);">YouTube 最多觀看量</span>
                <iframe src="https://www.youtube.com/embed/JMNBEQ_xBi8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
        </div>
        <div class="video-section">
            <div class="button instagram" style="display: block; position: relative;">
                <i class="fab fa-instagram"></i>
                <span style="position: absolute; top: 10px; left: 50%; transform: translateX(-50%);">Instagram 視頻</span>
                <iframe src="https://www.instagram.com/reel/C5akynxJREi/embed" frameborder="0" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <footer style="margin-top: 20px; font-size: 14px; color: #666;">
        © 2024 你的名字。保留所有权利。
    </footer>

</body>
</html>
