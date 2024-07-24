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
            padding: 0; /* Remove padding to fit video */
            text-decoration: none;
            border-radius: 5px;
            margin: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: background-color 0.3s, transform 0.3s;
            position: relative;
            width: 560px; /* Width for displaying video */
            height: 315px; /* Height for displaying video */
            overflow: hidden;
            text-align: center;
            background-color: transparent; /* Transparent background for button */
        }
        .button.youtube {
            border: 3px solid #FF0000; /* YouTube border color */
        }
        .button.discord {
            border: 3px solid #7289DA; /* Discord border color */
        }
        .button.instagram {
            border: 3px solid #C13584; /* Instagram border color */
        }
        .button-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        .video-container {
            display: flex;
            justify-content: center;
            gap: 20px; /* Space between videos */
            margin-top: 20px;
            flex-wrap: wrap;
        }
        .video-section {
            flex: 1;
            max-width: 100%; /* Full width for video buttons */
        }
        .video-section iframe {
            width: 100%;
            height: 100%;
            display: block;
            border: none; /* Remove default iframe border */
        }
        .youtube-icon {
            position: absolute;
            top: 10px;
            left: 10px;
            font-size: 40px;
            color: #fff;
            z-index: 1;
        }
    </style>
</head>
<body style="margin: 0; padding: 0; background-color: #f0f0f0; text-align: center; display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100vh;">

    <h1 style="font-size: 36px; color: #333;">歡迎來到我的網站</h1>
    <p style="font-size: 18px; color: #666;">在這裡你可以訪問我的 YouTube 頻道和加入我的 Discord 群組。</p>

    <div class="button-container">
        <a href="https://www.youtube.com/channel/UCPl1ALv9iBz0JYNtoYVB-oQ" class="button youtube">
            <i class="fab fa-youtube youtube-icon"></i> YouTube
        </a>
        <a href="https://discord.com/invite/e5cbzGFS3H" class="button discord">
            <i class="fab fa-discord"></i> Discord
        </a>
        <a href="https://www.instagram.com/ru031314580/" class="button instagram">
            <i class="fab fa-instagram"></i> ru031314580
        </a>
    </div>

    <div class="video-container">
        <div class="video-section">
            <a href="#" class="button youtube" style="display: block;">
                <iframe src="https://www.youtube.com/embed/JMNBEQ_xBi8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </a>
        </div>
        <div class="video-section">
            <a href="#" class="button instagram" style="display: block;">
                <iframe src="https://www.instagram.com/reel/C5akynxJREi/embed" frameborder="0" allowfullscreen></iframe>
            </a>
        </div>
    </div>

    <footer style="margin-top: 20px; font-size: 14px; color: #666;">
        © 2024 你的名字。保留所有权利。
    </footer>

</body>
</html>
