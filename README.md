<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>個人網頁 | 國立屏東科技大學工業管理系</title>
    <style>
        :root {
            --primary-color: #003366; /* 屏科大深藍 */
            --accent-color: #A71930;  /* Alfa Romeo 紅 (點綴用) */
            --bg-gray: #f8f9fa;
            --text-main: #333;
        }

        body {
            font-family: "PingFang TC", "Microsoft JhengHei", sans-serif;
            margin: 0;
            display: flex;
            background-color: #fff;
            color: var(--text-main);
            line-height: 1.6;
        }

        /* 左側導覽列 */
        .sidebar {
            width: 260px;
            background-color: var(--bg-gray);
            height: 100vh;
            position: fixed;
            border-right: 1px solid #e0e0e0;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 40px;
        }

        .profile-frame {
            width: 160px;
            height: 200px;
            background-color: #ddd;
            border: 4px solid #fff;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .profile-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .name-tag {
            text-align: center;
            margin: 20px 0;
        }

        .name-tag h2 {
            margin: 0;
            color: var(--primary-color);
            letter-spacing: 2px;
        }

        .sidebar nav {
            width: 100%;
            margin-top: 10px;
        }

        .sidebar nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .sidebar nav ul li a {
            display: block;
            padding: 15px 30px;
            text-decoration: none;
            color: #555;
            font-weight: 500;
            border-bottom: 1px solid #eee;
            transition: all 0.3s ease;
        }

        .sidebar nav ul li a:hover {
            background-color: var(--primary-color);
            color: #fff;
            padding-left: 40px;
        }

        /* 右側內容區 */
        .main-content {
            margin-left: 260px;
            padding: 50px 80px;
            flex: 1;
        }

        .header-title {
            border-bottom: 3px solid var(--primary-color);
            padding-bottom: 15px;
            margin-bottom: 40px;
        }

        .header-title h1 {
            font-size: 2.2rem;
            margin: 0;
            color: var(--primary-color);
        }

        section {
            margin-bottom: 50px;
            animation: fadeIn 0.8s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h3 {
            font-size: 1.4rem;
            color: var(--primary-color);
            border-left: 6px solid var(--primary-color);
            padding-left: 15px;
            margin-bottom: 20px;
            background: linear-gradient(90deg, #f0f4f8, transparent);
            padding-top: 5px;
            padding-bottom: 5px;
        }

        /* 表格樣式 */
        .data-table {
            width: 100%;
            border-collapse: collapse;
        }

        .data-table td {
            padding: 12px;
            border-bottom: 1px solid #eee;
        }

        .td-label {
            width: 120px;
            font-weight: bold;
            color: #666;
        }

        /* 專案卡片 */
        .project-item {
            background: #fff;
            border: 1px solid #e0e0e0;
            padding: 20px;
            margin-bottom: 15px;
            border-radius: 8px;
            transition: 0.3s;
        }

        .project-item:hover {
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            border-color: var(--accent-color);
        }

        .project-item strong {
            color: var(--primary-color);
            font-size: 1.1rem;
        }

        .tag {
            display: inline-block;
            background: var(--bg-gray);
            padding: 2px 10px;
            border-radius: 4px;
            font-size: 0.8rem;
            margin-right: 5px;
            color: #666;
            border: 1px solid #ddd;
        }

        /* 手機版適應 */
        @media (max-width: 900px) {
            body { flex-direction: column; }
            .sidebar { width: 100%; height: auto; position: relative; padding-bottom: 20px; }
            .main-content { margin-left: 0; padding: 30px; }
        }
    </style>
</head>
<body>

    <aside class="sidebar">
        <div class="profile-frame">
            <img src="https://via.placeholder.com/160x200?text=Photo" alt="個人照">
        </div>
        <div class="name-tag">
            <h2>你的姓名</h2>
            <p>工業管理系 | NPUST</p>
        </div>
        
        <nav>
            <ul>
                <li><a href="#about">個人首頁</a></li>
                <li><a href="#expertise">研究領域</a></li>
                <li><a href="#education">學經歷</a></li>
                <li><a href="#projects">實務專案</a></li>
                <li><a href="#contact">聯絡方式</a></li>
            </ul>
        </nav>
    </aside>

    <main class="main-content">
        <header class="header-title">
            <h1>國立屏東科技大學 工業管理系</h1>
            <p style="color: #666; margin-top: 5px;">Department of Industrial Management, NPUST</p>
        </header>

        <section id="about">
            <h3>基本資料</h3>
            <table class="data-table">
                <tr>
                    <td class="td-label">姓名</td>
                    <td>(填入你的中文姓名)</td>
                </tr>
                <tr>
                    <td class="td-label">學位</td>
                    <td>工業管理學士 (在讀)</td>
                </tr>
                <tr>
                    <td class="td-label">研究方向</td>
                    <td>生產優化、人力資源管理、高性能車輛工程實務</td>
                </tr>
                <tr>
                    <td class="td-label">技術專長</td>
                    <td>Excel VBA、車輛動態調校、零件相容性分析</td>
                </tr>
            </table>
        </section>

        <section id="expertise">
            <h3>專業領域與研究興趣</h3>
            <p>致力於將**工業管理科學**與**汽車售後市場**結合，透過標準化流程與數據分析，提升改裝維修之效能與品質。</p>
            <ul>
                <li><strong>管理科學：</strong> 工程經濟分析、工作研究 (Work Study) 與 SOP 流程建立。</li>
                <li><strong>車輛工程：</strong> BMW E46 系統維護、底盤懸吊幾何設定、Selespeed 系統診斷。</li>
                <li><strong>模擬與數位化：</strong> 運用數據進行性能車零件供應鏈優化研究。</li>
            </ul>
        </section>

        <section id="education">
            <h3>學經歷</h3>
            <table class="data-table">
                <tr>
                    <td style="width: 140px;">202X - 至今</td>
                    <td><strong>國立屏東科技大學</strong><br>工業管理系 | 學士班</td>
                </tr>
                <tr>
                    <td>202X - 202X</td>
                    <td><strong>(你的高中名稱)</strong><br>(你的科系) | 畢業</td>
                </tr>
            </table>
        </section>

        <section id="projects">
            <h3>代表性實務專案</h3>
            
            <div class="project-item">
                <span class="tag">底盤工程</span><span class="tag">數據分析</span><br>
                <strong>BMW E46 325Ci 懸吊系統參數優化與實測分析</strong>
                <p>針對 E46 自動檔車型進行 BC Racing 懸吊系統安裝，紀錄不同阻尼設定於山道駕駛中之動態回饋，並導入預防性維護概念進行 AP Racing 煞車系統配置優化。</p>
            </div>

            <div class="project-item">
                <span class="tag">SOP 建立</span><span class="tag">機械維修</span><br>
                <strong>Yamaha BW'S R 引擎改裝組件維護流程開發</strong>
                <p>針對 59mm 缸頭與傳動組件之高負載特性，建立週期性檢修 SOP，成功排除啟動盤與傳動總成之異常磨耗問題，確保動力傳遞效率。</p>
            </div>

            <div class="project-item">
                <span class="tag">工業管理</span><span class="tag">模擬應用</span><br>
                <strong>模擬賽車系統 (Sim Racing) 硬體參數調校研究</strong>
                <p>於 Assetto Corsa 及 Forza 平台，針對 Xbox 控制器之轉向線性度進行敏感度分析，達成模擬環境下最優化之操控手感設定。</p>
            </div>
        </section>

        <section id="contact">
            <h3>聯絡方式</h3>
            <div class="project-item">
                <p>📧 <strong>Email:</strong> your-email@mail.npust.edu.tw</p>
                <p>📍 <strong>研究室:</strong> 屏東縣內埔鄉學府路 1 號 (工管系館)</p>
                <p>📱 <strong>社群連結:</strong> [LinkedIn] / [GitHub] / [個人部落格]</p>
            </div>
        </section>

        <footer style="text-align: center; font-size: 0.8rem; color: #aaa; margin-top: 100px;">
            &copy; 2026 你的姓名 - 國立屏東科技大學工業管理系
        </footer>
    </main>

</body>
</html>
