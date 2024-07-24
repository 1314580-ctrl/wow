body {
    margin: 0;
    padding: 0;
    background-image: url('你的圖片鏈接');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    text-align: center;
}

.channel-link, .discord-link {
    display: block;
    background-color: rgba(0, 0, 0, 0.7); /* 半透明背景 */
    color: #fff; /* 白色文字 */
    padding: 15px 30px;
    text-decoration: none;
    font-size: 24px;
    border-radius: 5px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    margin: 10px; /* 按鈕之間的間距 */
}

.channel-link:hover, .discord-link:hover {
    background-color: rgba(0, 0, 0, 0.9); /* 當鼠標懸停時改變背景顏色 */
}
