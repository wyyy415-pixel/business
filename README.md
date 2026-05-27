<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Index.html 測試頁面</title>
    <style>
        /* 基礎樣式重設 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif, "Microsoft JhengHei";
        }

        body {
            background-color: #f4f7f6;
            color: #333;
            line-height: 1.6;
        }

        /* 導覽列 */
        header {
            background-color: #2c3e50;
            color: #fff;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        header .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #1abc9c;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            margin-left: 1.5rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #1abc9c;
        }

        /* 英雄區 (Hero Section) */
        .hero {
            background: linear-gradient(135deg, #1abc9c, #2c3e50);
            color: white;
            text-align: center;
            padding: 5rem 1rem;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            background-color: #e74c3c;
            color: white;
            padding: 0.7rem 2rem;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s, transform 0.2s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #c0392b;
            transform: translateY(-2px);
        }

        /* 主要內容區 */
        .container {
            max-width: 1200px;
            margin: 3rem auto;
            padding: 0 1rem;
        }

        .section-title {
            text-align: center;
            margin-bottom: 2rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            background-color: #1abc9c;
            margin: 0.5rem auto 0;
        }

        /* 卡片佈局 (Grid) */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }

        .card {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            text-align: center;
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card-icon {
            font-size: 2.5rem;
            color: #1abc9c;
            margin-bottom: 1rem;
        }

        .card h3 {
            margin-bottom: 1rem;
        }

        /* 測試互動表單區 */
        .form-section {
            background: white;
            padding: 2.5rem;
            border-radius: 8px;
            max-width: 600px;
            margin: 0 auto;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: #1abc9c;
        }

        /* 頁尾 */
        footer {
            background-color: #2c3e50;
            color: #bdc3c7;
            text-align: center;
            padding: 2rem 1rem;
            margin-top: 5rem;
            font-size: 0.9rem;
        }

        /* 響應式調整 */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                gap: 1rem;
            }
            nav a {
                margin: 0 0.75rem;
            }
            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">TestLab 🧪</div>
        <nav>
            <a href="#home">首頁</a>
            <a href="#features">功能測試</a>
            <a href="#contact">聯絡我們</a>
        </nav>
    </header>

    <section class="hero" id="home">
        <h1>歡迎來到 HTML 測試網頁</h1>
        <p>這是一個用來測試 CSS 樣式、JavaScript 腳本與瀏覽器相容性的環境。</p>
        <button class="btn" onclick="alert('恭喜！JavaScript 按鈕觸發成功！')">點擊測試 JS</button>
    </section>

    <main class="container">
        
        <section id="features">
            <h2 class="section-title">核心測試項目</h2>
            <div class="grid">
                <div class="card">
                    <div class="card-icon">🎨</div>
                    <h3>CSS Grid & Flexbox</h3>
                    <p>測試區塊在不同螢幕尺寸下的排版流暢度與回應式（RWD）表現。</p>
                </div>
                <div class="card">
                    <div class="card-icon">⚡</div>
                    <h3>DOM 互動</h3>
                    <p>點擊上方按鈕可測試簡單的 JavaScript 彈窗功能是否正常運作。</p>
                </div>
                <div class="card">
                    <div class="card-icon">📱</div>
                    <h3>行動裝置優化</h3>
                    <p>支援行動裝置視口（Viewport）設定，確保手機瀏覽不破版。</p>
                </div>
            </div>
        </section>

        <hr style="border: 0; height: 1px; background: #ddd; margin: 4rem 0;">

        <section id="contact">
            <h2 class="section-title">表單與輸入測試</h2>
            <div class="form-section">
                <form onsubmit="event.preventDefault(); alert('表單送出成功！（已攔截預設跳轉）');">
                    <div class="form-group">
                        <label for="name">測試姓名</label>
                        <input type="text" id="name" placeholder="請輸入姓名" required>
                    </div>
                    <div class="form-group">
                        <label for="email">電子郵件</label>
                        <input type="email" id="email" placeholder="example@email.com" required>
                    </div>
                    <div class="form-group">
                        <label for="message">測試留言</label>
                        <textarea id="message" rows="4" placeholder="請輸入任意文字..."></textarea>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">送出測試</button>
                </form>
            </div>
        </section>

    </main>

    <footer>
        <p>&copy; 2026 TestLab. 僅供前端開發與環境測試使用。</p>
    </footer>

</body>
</html>
