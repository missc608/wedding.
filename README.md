<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>政儒 & 怡靜 婚禮邀請函 | Our Wedding Invitation</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Noto+Serif+TC:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary-warm: #d4a373;
            --secondary-sage: #8da399;
            --bg-light: #fbf9f6;
            --text-dark: #333333;
            --text-muted: #777777;
            --white-glow: rgba(255, 255, 255, 0.85);
            --shadow-soft: 0 10px 30px rgba(0, 0, 0, 0.05);
            --shadow-card: 0 4px 20px rgba(212, 163, 115, 0.15);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Noto Serif TC', serif;
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.8;
            overflow-x: hidden;
        }

        .en-font {
            font-family: 'Cormorant Garamond', serif;
        }

        .no-wrap {
            white-space: nowrap;
        }

        /* 1. 導覽列 (毛玻璃) */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(251, 249, 246, 0.75);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(212, 163, 115, 0.2);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-logo {
            font-size: 1.2rem;
            font-weight: 600;
            color: var(--primary-warm);
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            gap: 1.5rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-warm);
        }

        /* 3. 質感配置 - 全螢幕首頁 */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.25), rgba(0,0,0,0.25)), 
                        url('https://i.postimg.cc/tgMnz6H1/0J7A8207.jpg') center/cover no-repeat;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #ffffff;
            padding: 0 1rem;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 400;
            letter-spacing: 4px;
            margin-bottom: 0.5rem;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.2rem;
            letter-spacing: 2px;
            margin-bottom: 2rem;
            font-weight: 300;
        }

        /* 2. 計時器視覺 (獨立白色微光卡片) */
        .countdown-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .time-card {
            background: var(--white-glow);
            padding: 1rem 1.2rem;
            border-radius: 12px;
            box-shadow: var(--shadow-soft);
            min-width: 75px;
            text-align: center;
            backdrop-filter: blur(5px);
        }

        .time-card .number {
            font-size: 2rem;
            font-weight: 600;
            color: var(--primary-warm);
            line-height: 1;
        }

        .time-card .label {
            font-size: 0.75rem;
            color: var(--text-muted);
            margin-top: 4px;
            text-transform: uppercase;
        }

        .divider {
            width: 1px;
            height: 35px;
            background-color: rgba(255, 255, 255, 0.5);
            margin: 0 4px;
        }

        /* 容器通用 */
        .section-padding {
            padding: 5rem 1.5rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2rem;
            color: var(--primary-warm);
            letter-spacing: 2px;
            font-weight: 400;
        }

        .section-title span {
            display: block;
            font-size: 0.9rem;
            color: var(--secondary-sage);
            letter-spacing: 3px;
        }

        /* 3. V-Card 垂直卡片設計 */
        .v-card {
            background: #ffffff;
            border-radius: 16px;
            padding: 2.5rem;
            box-shadow: var(--shadow-card);
            margin-bottom: 2rem;
            border: 1px solid rgba(212, 163, 115, 0.1);
        }

        .v-card-item {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            text-align: center;
        }

        .info-group h3 {
            color: var(--secondary-sage);
            font-size: 1.1rem;
            margin-bottom: 0.3rem;
        }

        .gallery {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
            margin: 2rem 0;
        }

        .gallery img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 12px;
        }

        /* 7. 摺疊式面板 (Accordion) */
        .accordion {
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid rgba(141, 163, 153, 0.3);
            margin-top: 1rem;
        }

        .accordion-header {
            background-color: #fff;
            padding: 1.2rem 1.5rem;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
            color: var(--text-dark);
            transition: background 0.3s;
        }

        .accordion-header:hover {
            background-color: #f4efe9;
        }

        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            background-color: #faf8f5;
            padding: 0 1.5rem;
        }

        .accordion-content p {
            padding: 1.2rem 0;
            color: var(--text-muted);
            font-size: 0.95rem;
            border-top: 1px dashed rgba(0,0,0,0.05);
        }

        /* 4. & 8. 表單樣式與動態邏輯 */
        .form-group {
            margin-bottom: 1.5rem;
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        /* 4. 中英雙語標籤 */
        label {
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--text-dark);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        label .en-label {
            font-family: 'Cormorant Garamond', serif;
            font-size: 0.85rem;
            color: var(--secondary-sage);
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        input[type="text"], input[type="email"], input[type="number"], select, textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-family: inherit;
            font-size: 1rem;
            background-color: #fcfbf9;
            transition: border-color 0.3s;
        }

        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: var(--primary-warm);
        }

        /* 8. 條件隱藏區塊 */
        .conditional-field {
            display: none;
            animation: fadeIn 0.4s ease-in-out forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-5px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .submit-btn {
            width: 100%;
            background-color: var(--primary-warm);
            color: white;
            padding: 1rem;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            margin-top: 1rem;
        }

        .submit-btn:hover {
            background-color: #c08d5e;
        }

        .submit-btn:active {
            transform: scale(0.99);
        }

        /* 隱藏式 Iframe */
        #hidden_iframe {
            display: none;
        }

        footer {
            text-align: center;
            padding: 2rem;
            font-size: 0.85rem;
            color: var(--text-muted);
            border-top: 1px solid rgba(0,0,0,0.05);
        }

        /* RWD 調整 */
        @media (max-width: 600px) {
            .hero h1 { font-size: 2.2rem; }
            .countdown-container { gap: 0.2rem; }
            .time-card { min-width: 60px; padding: 0.8rem 0.5rem; }
            .time-card .number { font-size: 1.5rem; }
            .gallery { grid-template-columns: 1fr; }
            .v-card { padding: 1.5rem; }
        }
    </style>
</head>
<body>

    <!-- 1. 固定的毛玻璃導航列 -->
    <nav>
        <div class="nav-logo en-font">J & J</div>
        <ul class="nav-links">
            <li><a href="#about">關於我們</a></li>
            <li><a href="#details">婚禮詳情</a></li>
            <li><a href="#rsvp">出席回函</a></li>
        </ul>
    </nav>

    <!-- 3. 全螢幕封面圖 -->
    <header class="hero">
        <p class="en-font">WELCOME TO OUR WEDDING</p>
        <h1>政儒 & 怡靜</h1>
        <p>我們的婚禮邀請</p>

        <!-- 2. 白色微光卡片倒數計時器 -->
        <div class="countdown-container" id="countdown">
            <div class="time-card">
                <div class="number en-font" id="days">00</div>
                <div class="label en-font">Days</div>
            </div>
            <div class="divider"></div>
            <div class="time-card">
                <div class="number en-font" id="hours">00</div>
                <div class="label en-font">Hours</div>
            </div>
            <div class="divider"></div>
            <div class="time-card">
                <div class="number en-font" id="minutes">00</div>
                <div class="label en-font">Mins</div>
            </div>
            <div class="divider"></div>
            <div class="time-card">
                <div class="number en-font" id="seconds">00</div>
                <div class="label en-font">Secs</div>
            </div>
        </div>
    </header>

    <!-- 關於我們區塊 -->
    <section id="about" class="section-padding">
        <div class="section-title">
            <span>ABOUT US</span>
            <h2>關於我們</h2>
        </div>
        <div class="v-card">
            <p style="text-align: center; color: var(--text-muted); margin-bottom: 1.5rem;">
                兩顆心的交匯，一段美好的旅程。<br>誠摯邀請您來到現場，與我們一同分享這份喜悅與愛。
            </p>
            <div class="gallery">
                <img src="https://i.postimg.cc/9FY4nKhq/0J7A8218.jpg" alt="政儒與怡靜婚紗照 1">
                <img src="https://i.postimg.cc/2SjqRGkn/0J7A8225.jpg" alt="政儒與怡靜婚紗照 2">
            </div>
        </div>
    </section>

    <!-- 3. 婚禮詳情區塊 (垂直 V-Card 設計) -->
    <section id="details" class="section-padding">
        <div class="section-title">
            <span>LOCATION & TIME</span>
            <h2>婚禮詳情</h2>
        </div>

        <div class="v-card v-card-item">
            <div class="info-group">
                <h3>婚禮日期 DATE</h3>
                <p>2027 年 3 月 6 日 星期六</p>
            </div>
            <div class="info-group">
                <h3>宴席時間 TIME</h3>
                <p>午宴 11:30 入席 / 12:00 開席</p>
            </div>
            <div class="info-group">
                <h3>地點 VENUE</h3>
                <p class="no-wrap">台北君悅酒店 3樓宴會廳</p>
                <p style="font-size: 0.9rem; color: var(--text-muted);" class="no-wrap">台北市信義區松壽路2號</p>
            </div>
        </div>

        <!-- 7. & 6. 交通指引 (摺疊式面板 Accordion + no-wrap 防斷行) -->
        <div class="accordion">
            <div class="accordion-header" onclick="toggleAccordion()">
                <span>交通指引 & 停車資訊</span>
                <span id="accordion-icon">+</span>
            </div>
            <div class="accordion-content" id="accordion-content">
                <p>
                    <strong>【捷運資訊】</strong><br>
                    搭乘至<span class="no-wrap">捷運台北101/世貿站</span> 5號出口，步行約 3 分鐘即可抵達。<br><br>
                    <strong>【公車資訊】</strong><br>
                    搭乘至<span class="no-wrap">台北君悅酒店站</span>或<span class="no-wrap">市府轉運站</span>。<br><br>
                    <strong>【停車資訊】</strong><br>
                    飯店設有地下停車場，賓客可享有免費停車折抵，請於離開前告知櫃檯。
                </p>
            </div>
        </div>
    </section>

    <!-- 4. & 5. & 8. 出席回函表單 -->
    <section id="rsvp" class="section-padding">
        <div class="section-title">
            <span>RSVP</span>
            <h2>出席回函</h2>
        </div>

        <div class="v-card">
            <!-- 5. 隱藏式 Iframe 提交技術 (使用指定 Google Form 欄位 ID) -->
            <iframe name="hidden_iframe" id="hidden_iframe" onload="if(submitted){showSuccessMessage();}"></iframe>
            
            <form action="https://docs.google.com/forms/d/e/1FAIpQLScNtYfmOBcb8rM_W8GayVsepZQXkl-csftjMGl_Z58cEx-ofw/formResponse" 
                  method="POST" 
                  target="hidden_iframe" 
                  onsubmit="submitted=true;">

                <!-- 4. 中英雙語標籤 + 清空預填值 (ID: entry.238723909) -->
                <div class="form-group">
                    <label for="name">姓名 <span class="en-label">NAME</span></label>
                    <input type="text" id="name" name="entry.238723909" placeholder="請輸入您的姓名" required>
                </div>

                <!-- 4. 雙語標籤 + 純中文選單 (ID: entry.756719319) -->
                <div class="form-group">
                    <label for="relation">關係 <span class="en-label">RELATIONSHIP</span></label>
                    <select id="relation" name="entry.756719319" required>
                        <option value="" disabled selected>請選擇您的身分</option>
                        <option value="男方親友">男方親友</option>
                        <option value="女方親友">女方親友</option>
                        <option value="共同朋友">共同朋友</option>
                    </select>
                </div>

                <!-- (ID: entry.1508122991) -->
                <div class="form-group">
                    <label for="email">電子郵件 <span class="en-label">EMAIL</span></label>
                    <input type="email" id="email" name="entry.1508122991" placeholder="example@mail.com" required>
                </div>

                <!-- (ID: entry.2064784402) -->
                <div class="form-group">
                    <label for="phone">聯絡電話 <span class="en-label">PHONE</span></label>
                    <input type="text" id="phone" name="entry.2064784402" placeholder="0912345678" required>
                </div>

                <!-- 8. 智能邏輯判斷欄位 (ID: entry.1723381945) -->
                <div class="form-group">
                    <label for="attendCount">參加午宴人數 <span class="en-label">ATTENDEES</span></label>
                    <input type="number" id="attendCount" name="entry.1723381945" min="0" value="0" required onchange="toggleConditionalFields()" oninput="toggleConditionalFields()">
                </div>

                <!-- 8. 只有當參加人數 > 0 時才會顯示的欄位 -->
                <div id="conditionalSection" class="conditional-field">
                    <!-- (ID: entry.1578009372) -->
                    <div class="form-group">
                        <label for="chairs">需要兒童椅數量 <span class="en-label">HIGH CHAIRS</span></label>
                        <input type="number" id="chairs" name="entry.1578009372" min="0" value="0">
                    </div>

                    <!-- (ID: entry.372078878) -->
                    <div class="form-group">
                        <label for="diet">飲食需求 <span class="en-label">DIET</span></label>
                        <select id="diet" name="entry.372078878">
                            <option value="葷食">葷食</option>
                            <option value="素食">素食</option>
                        </select>
                    </div>
                </div>

                <button type="submit" class="submit-btn">確認送出 SUBMIT</button>
            </form>
        </div>
    </section>

    <footer>
        <p class="en-font">Cheng-Ru & Yi-Ching Wedding | 2027</p>
    </footer>

    <script>
        var submitted = false;

        // 2. 倒數計時器邏輯 (設定目標時間為 2027年3月6日 11:30 AM)
        const weddingDate = new Date("March 6, 2027 11:30:00").getTime();

        function updateCountdown() {
            const now = new Date().getTime();
            const distance = weddingDate - now;

            if (distance < 0) {
                document.getElementById("countdown").innerHTML = "<p style='color: white;'>婚禮隆重登場中！</p>";
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById("days").innerText = days < 10 ? '0' + days : days;
            document.getElementById("hours").innerText = hours < 10 ? '0' + hours : hours;
            document.getElementById("minutes").innerText = minutes < 10 ? '0' + minutes : minutes;
            document.getElementById("seconds").innerText = seconds < 10 ? '0' + seconds : seconds;
        }

        setInterval(updateCountdown, 1000);
        updateCountdown();

        // 7. 交通指引 Accordion 切換
        function toggleAccordion() {
            const content = document.getElementById("accordion-content");
            const icon = document.getElementById("accordion-icon");
            if (content.style.maxHeight) {
                content.style.maxHeight = null;
                icon.innerText = "+";
            } else {
                content.style.maxHeight = content.scrollHeight + "px";
                icon.innerText = "-";
            }
        }

        // 8. 智能表單邏輯：人數大於 0 才顯示飲食與兒童椅需求
        function toggleConditionalFields() {
            const count = parseInt(document.getElementById("attendCount").value, 10);
            const conditionalSection = document.getElementById("conditionalSection");

            if (count > 0) {
                conditionalSection.style.display = "block";
            } else {
                conditionalSection.style.display = "none";
            }
        }

        // 5. 提交成功回饋
        function showSuccessMessage() {
            alert("感謝您的回覆！我們期待在婚禮當天見到您。");
            document.querySelector("form").reset();
            toggleConditionalFields();
        }
    </script>
</body>
</html>
