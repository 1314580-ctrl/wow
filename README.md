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
            padding: 15px 30px;
            text-decoration: none;
            font-size: 24px;
            border-radius: 5px;
            margin: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: background-color 0.3s, transform 0.3s;
        }
        .button.youtube {
            background-color: #FF0000; /* YouTube 颜色 */
        }
        .button.youtube:hover {
            background-color: #CC0000; /* YouTube 颜色的深一点的变体 */
        }
        .button.discord {
            background-color: #7289DA; /* Discord 颜色 */
        }
        .button.discord:hover {
            background-color: #5b6eae; /* Discord 颜色的深一点的变体 */
        }
        .button.instagram {
            background-color: #C13584; /* Instagram 颜色 */
        }
        .button.instagram:hover {
            background-color: #a02d6d; /* Instagram 颜色的深一点的变体 */
        }
        .video-container {
            margin-top: 20px;
            width: 100%;
            max-width: 800px;
            position: relative;
            padding-bottom: 56.25%; /* 16:9 aspect ratio */
            height: 0;
        }
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        .most-viewed {
            margin-top: 20px;
            width: 100%;
            max-width: 800px;
            text-align: center;
        }
        .most-viewed iframe {
            width: 100%;
            height: 315px; /* Adjust height as needed */
        }
        .most-viewed h2 {
            font-size: 24px;
            color: #333;
            margin: 10px 0;
        }
    </style>
</head>
<body style="margin: 0; padding: 0; background-color: #f0f0f0; text-align: center; display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100vh;">

    <h1 style="font-size: 36px; color: #333;">歡迎來到我的網站</h1>
    <p style="font-size: 18px; color: #666;">在這裡你可以訪問我的 YouTube 頻道和加入我的 Discord 群組。</p>

    <div>
        <a href="https://www.youtube.com/channel/UCPl1ALv9iBz0JYNtoYVB-oQ" class="button youtube">
            <i class="fab fa-youtube"></i> YouTube
        </a>
        <a href="https://discord.com/invite/e5cbzGFS3H" class="button discord">
            <i class="fab fa-discord"></i> Discord
        </a>
        <a href="https://www.instagram.com/ru031314580/" class="button instagram">
            <i class="fab fa-instagram"></i> ru031314580
        </a>
    </div>

    <div class="most-viewed">
        <h2>最多觀看量的影片</h2>
        <iframe src="https://www.youtube.com/embed/JMNBEQ_xBi8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>

    <footer style="margin-top: 20px; font-size: 14px; color: #666;">
        © 2024 你的名字。保留所有权利。
    </footer>

</body>
</html>
