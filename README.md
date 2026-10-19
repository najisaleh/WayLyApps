<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة WayLy Apps - تحميل التطبيقات والبرامج الرسمية</title>
    <style>
        :root {
            --bg-dark: #0f172a;
            --card-bg: #1e293b;
            --card-border: #334155;
            --accent-gold: #eab308;
            --accent-teal: #14b8a6;
            --accent-blue: #0284c7;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: system-ui, -apple-system, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
        }

        /* الهيدر العلوي */
        header {
            background: linear-gradient(135deg, #0f172a 0%, #1e3a8a 100%);
            border-bottom: 2px solid var(--accent-gold);
            padding: 16px 20px;
            position: sticky;
            top: 0;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 15px rgba(0,0,0,0.4);
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .site-logo {
            width: 48px;
            height: 48px;
            border-radius: 12px;
            background: var(--accent-gold);
            color: #0f172a;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 900;
            border: 2px solid #fff;
        }

        .site-title h1 {
            font-size: 1.25rem;
            color: var(--accent-gold);
            font-weight: 800;
        }

        .site-title span {
            font-size: 0.75rem;
            color: var(--text-muted);
        }

        .dev-badge {
            font-size: 0.8rem;
            color: var(--accent-gold);
            font-weight: 700;
            background: rgba(234, 179, 8, 0.1);
            padding: 6px 12px;
            border-radius: 8px;
            border: 1px solid rgba(234, 179, 8, 0.3);
        }

        /* شريط البحث البارز */
        .hero-section {
            text-align: center;
            padding: 45px 20px;
            background: radial-gradient(circle at center, #1e293b 0%, #0f172a 70%);
            border-bottom: 1px solid var(--card-border);
        }

        .hero-section h2 {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: #fff;
        }

        .hero-section p {
            color: var(--text-muted);
            margin-bottom: 25px;
            font-size: 0.95rem;
        }

        .search-box {
            max-width: 600px;
            margin: 0 auto;
            display: flex;
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 14px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
        }

        .search-input {
            flex: 1;
            background: transparent;
            border: none;
            padding: 14px 18px;
            color: #fff;
            font-size: 1rem;
            outline: none;
        }

        .search-btn {
            background: var(--accent-teal);
            color: #fff;
            border: none;
            padding: 0 24px;
            font-weight: 800;
            cursor: pointer;
            transition: background 0.2s;
        }

        .search-btn:hover {
            background: #0d9488;
        }

        /* حاوية المحتوى والأقسام */
        .container {
            max-width: 1100px;
            margin: 30px auto;
            padding: 0 20px;
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            border-right: 4px solid var(--accent-gold);
            padding-right: 10px;
        }

        .section-header h3 {
            font-size: 1.3rem;
            color: #fff;
        }

        /* شبكة عرض التطبيقات (Grid) */
        .apps-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .app-card {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 16px;
            padding: 18px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: transform 0.2s, box-shadow 0.2s, border-color 0.2s;
        }

        .app-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.4);
            border-color: var(--accent-teal);
        }

        .app-info {
            display: flex;
            gap: 12px;
            margin-bottom: 12px;
        }

        .app-icon {
            width: 60px;
            height: 60px;
            border-radius: 14px;
            object-fit: cover;
            border: 1px solid var(--card-border);
            background: #fff;
            flex-shrink: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 900;
            font-size: 1.3rem;
        }

        .app-details h4 {
            font-size: 1.05rem;
            color: #fff;
            margin-bottom: 2px;
        }

        .app-category {
            font-size: 0.75rem;
            color: var(--accent-teal);
            margin-bottom: 4px;
            display: block;
        }

        .app-meta {
            font-size: 0.78rem;
            color: var(--text-muted);
        }

        .app-desc {
            font-size: 0.85rem;
            color: #cbd5e1;
            margin-bottom: 16px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .download-btn {
            background: linear-gradient(135deg, var(--accent-blue), #1e3a8a);
            color: #fff;
            text-align: center;
            padding: 10px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 700;
            font-size: 0.9rem;
            transition: opacity 0.2s;
            display: block;
        }

        .download-btn:hover {
            opacity: 0.9;
        }

        /* رسالة عدم وجود نتائج */
        .no-results {
            text-align: center;
            color: var(--text-muted);
            grid-column: 1 / -1;
            padding: 30px;
            display: none;
            font-size: 1rem;
        }

        /* الفوتر */
        footer {
            background: #090d16;
            border-top: 2px solid var(--accent-gold);
            padding: 30px 20px;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.85rem;
        }

        footer p {
            color: var(--accent-gold);
            font-weight: 700;
            margin-bottom: 6px;
        }

        @media (max-width: 600px) {
            .hero-section h2 { font-size: 1.4rem; }
            .search-box { flex-direction: column; background: transparent; border: none; box-shadow: none; }
            .search-input { background: var(--card-bg); border: 1px solid var(--card-border); border-radius: 12px; margin-bottom: 8px; }
            .search-btn { border-radius: 12px; padding: 12px; }
        }
    </style>
</head>
<body>

    <!-- الهيدر العلوي -->
    <header>
        <div class="logo-area">
            <div class="site-logo" style="background: #1e3a8a; color: var(--accent-gold);">W</div>
            <div class="site-title">
                <h1>WayLy Apps</h1>
                <span>منصة التطبيقات الرسمية</span>
            </div>
        </div>
        <div class="dev-badge">Eng. Naji Al-Mafraji</div>
    </header>

    <!-- واجهة البحث البارزة -->
    <div class="hero-section">
        <h2>ابحث في تطبيقات وبرامج WayLy</h2>
        <p>قم بتحميل أحدث إصدارات تطبيقات الأندرويد التعليمية والتقنية بروابط مباشرة وآمنة.</p>
        <div class="search-box">
            <input type="text" id="searchInput" class="search-input" placeholder="ابحث عن اسم التطبيق (مثل: English, Sat, German)..." onkeyup="filterApps()">
            <button class="search-btn">بحث 🔍</button>
        </div>
    </div>

    <!-- محتوى الموقع الرئيسي -->
    <div class="container">
        
        <div class="section-header">
            <h3>📱 التطبيقات المتاحة للتحميل</h3>
        </div>

        <div class="apps-grid" id="appsGrid">
            
            <!-- تطبيق 1: WayLy English -->
            <div class="app-card" data-name="wayly english انجليزي لغات">
                <div>
                    <div class="app-info">
                        <div class="app-icon" style="background: #1e3a8a; color: var(--accent-gold);">EN</div>
                        <div class="app-details">
                            <h4>WayLy English</h4>
                            <span class="app-category">تعليم اللغات</span>
                            <span class="app-meta">الإصدار: 2.1 • 15 MB</span>
                        </div>
                    </div>
                    <div class="app-desc">تطبيق احترافي لتعلم قواعد والمحادثة الإنجليزية باللهجة العراقية مع مدرب ذكي وصوت مدمج.</div>
                </div>
                <a href="https://github.com/najisaleh/WayLyApp/releases/download/v2.1/wayly-english.apk" class="download-btn" download>تحميل التطبيق (15 MB) 📥</a>
            </div>

            <!-- تطبيق 2: WayLy German -->
            <div class="app-card" data-name="wayly german الالمانية الماني">
                <div>
                    <div class="app-info">
                        <div class="app-icon" style="background: #881337; color: var(--accent-gold);">DE</div>
                        <div class="app-details">
                            <h4>WayLy German</h4>
                            <span class="app-category">تعليم اللغات</span>
                            <span class="app-meta">الإصدار: 1.8 • 18 MB</span>
                        </div>
                    </div>
                    <div class="app-desc">تعلم اللغة الألمانية من الصفر، القواعد، وأبرز عبارات السفر اليومية مع نطق صوتي دقيق.</div>
                </div>
                <a href="#" class="download-btn" download>تحميل التطبيق (18 MB) 📥</a>
            </div>

            <!-- تطبيق 3: WayLySat Iraq -->
            <div class="app-card" data-name="waylysat iraq ستلايت رسيفر اقمار">
                <div>
                    <div class="app-info">
                        <div class="app-icon" style="background: #0369a1; color: var(--accent-gold);">SAT</div>
                        <div class="app-details">
                            <h4>WayLySat Iraq</h4>
                            <span class="app-category">أدوات وتقنية</span>
                            <span class="app-meta">الإصدار: 3.0 • 12 MB</span>
                        </div>
                    </div>
                    <div class="app-desc">فايندر ستلايت ذكي ومخصص لمحافظات العراق، حساب زوايا السمت والارتفاع وربط الرسيفر المحلي.</div>
                </div>
                <a href="#" class="download-btn" download>تحميل التطبيق (12 MB) 📥</a>
            </div>

            <!-- تطبيق 4: WayLy Turkish -->
            <div class="app-card" data-name="wayly turkish تركي لغات">
                <div>
                    <div class="app-info">
                        <div class="app-icon" style="background: #065f46; color: var(--accent-gold);">TR</div>
                        <div class="app-details">
                            <h4>WayLy Turkish</h4>
                            <span class="app-category">تعليم اللغات</span>
                            <span class="app-meta">الإصدار: 2.0 • 16 MB</span>
                        </div>
                    </div>
                    <div class="app-desc">تعلم اللغة التركية، القواعد وحروفها الخاصة، مع دليل شامل لعبارات السفر والأسواق.</div>
                </div>
                <a href="#" class="download-btn" download>تحميل التطبيق (16 MB) 📥</a>
            </div>

            <div class="no-results" id="noResults">عذراً، لم يتم العثور على أي تطبيق مطابق لبحثك.</div>

        </div>

    </div>

    <!-- الفوتر السفلي -->
    <footer>
        <p>جميع الحقوق محفوظة © 2026 - WayLy Apps Platform</p>
        <span>تصميم وتطوير: المهندس ناجي المفرجي (Eng. Naji Al-Mafraji)</span>
    </footer>

    <!-- جافاسكريبت للبحث الفوري -->
    <script>
        function filterApps() {
            let input = document.getElementById('searchInput').value.toLowerCase();
            let cards = document.getElementsByClassName('app-card');
            let noResults = document.getElementById('noResults');
            let foundCount = 0;

            for (let i = 0; i < cards.length; i++) {
                let card = cards[i];
                let name = card.getAttribute('data-name');
                if (name.includes(input)) {
                    card.style.display = "flex";
                    foundCount++;
                } else {
                    card.style.display = "none";
                }
            }

            if (foundCount === 0) {
                noResults.style.display = "block";
            } else {
                noResults.style.display = "none";
            }
        }
    </script>

</body>
</html>
