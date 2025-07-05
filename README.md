
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل التداول الشامل | راني فوريكس</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/chart.js">
    <style>
        :root {
            --primary: #1a2a3a;
            --secondary: #3498db;
            --accent: #27ae60;
            --dark: #0d1721;
            --light: #ecf0f1;
            --gold: #f1c40f;
            --sidebar-width: 280px;
            --header-height: 70px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1721, #1a2a3a);
            color: var(--light);
            min-height: 100vh;
            overflow-x: hidden;
            line-height: 1.6;
        }
        
        /* الشريط العلوي */
        .header {
            background: rgba(13, 23, 33, 0.9);
            height: var(--header-height);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.4);
            border-bottom: 1px solid rgba(52, 152, 219, 0.3);
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo img {
            height: 40px;
        }
        
        .logo h1 {
            font-size: 1.5rem;
            background: linear-gradient(to right, var(--gold), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }
        
        .menu-btn {
            background: var(--secondary);
            color: white;
            border: none;
            border-radius: 50%;
            width: 45px;
            height: 45px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-size: 1.3rem;
            transition: all 0.3s ease;
        }
        
        .menu-btn:hover {
            background: #2980b9;
            transform: rotate(90deg);
        }
        
        /* القائمة الجانبية */
        .sidebar {
            position: fixed;
            top: var(--header-height);
            left: 0;
            width: var(--sidebar-width);
            height: calc(100vh - var(--header-height));
            background: rgba(13, 23, 33, 0.95);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            overflow-y: auto;
            transform: translateX(-100%);
            transition: transform 0.4s ease;
            z-index: 900;
            border-right: 1px solid rgba(52, 152, 219, 0.2);
        }
        
        .sidebar.active {
            transform: translateX(0);
        }
        
        .sidebar-item {
            padding: 15px 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-left: 3px solid transparent;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .sidebar-item:hover, .sidebar-item.active {
            background: rgba(52, 152, 219, 0.15);
            border-left: 3px solid var(--accent);
        }
        
        .sidebar-item i {
            font-size: 1.2rem;
            color: var(--gold);
            width: 25px;
            text-align: center;
        }
        
        .sidebar-item span {
            font-size: 1.1rem;
            font-weight: 500;
        }
        
        /* المحتوى الرئيسي */
        .main-content {
            margin-top: var(--header-height);
            padding: 30px;
            transition: all 0.4s ease;
        }
        
        .section {
            background: rgba(13, 23, 33, 0.7);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(52, 152, 219, 0.2);
            display: none;
        }
        
        .section.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--accent);
            color: var(--gold);
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .section-title i {
            color: var(--accent);
        }
        
        /* بطاقات المحتوى */
        .card {
            background: rgba(26, 42, 58, 0.7);
            border-radius: 12px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(52, 152, 219, 0.15);
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--secondary);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .card-title i {
            color: var(--gold);
        }
        
        .feature-list {
            list-style-type: none;
            margin: 15px 0;
        }
        
        .feature-list li {
            padding: 10px 0;
            padding-left: 30px;
            position: relative;
            border-bottom: 1px dashed rgba(255, 255, 255, 0.1);
        }
        
        .feature-list li:last-child {
            border-bottom: none;
        }
        
        .feature-list li::before {
            content: "★";
            color: var(--accent);
            position: absolute;
            left: 0;
            font-size: 1.2rem;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, var(--accent), var(--secondary));
            color: white;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            margin-top: 15px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            text-align: center;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(39, 174, 96, 0.4);
        }
        
        .btn-secondary {
            background: linear-gradient(135deg, #3498db, #2c3e50);
        }
        
        .btn-gold {
            background: linear-gradient(135deg, var(--gold), #e67e22);
        }
        
        /* التقييمات */
        .rating-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .rating-card {
            background: rgba(26, 42, 58, 0.8);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .rating-card:hover {
            transform: scale(1.03);
        }
        
        .rating-stars {
            color: var(--gold);
            font-size: 1.5rem;
            margin: 10px 0;
        }
        
        /* حاسبة رأس المال */
        .calculator-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        
        .calculator-inputs, .calculator-results {
            background: rgba(26, 42, 58, 0.8);
            border-radius: 12px;
            padding: 25px;
        }
        
        .input-group {
            margin-bottom: 20px;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: #bdc3c7;
        }
        
        .input-group input {
            width: 100%;
            padding: 12px 15px;
            border: none;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .input-group input:focus {
            outline: none;
            border-color: var(--secondary);
            background: rgba(255, 255, 255, 0.15);
        }
        
        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .result-box {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .result-value {
            font-size: 1.8rem;
            font-weight: 700;
            margin: 10px 0;
            color: var(--accent);
        }
        
        .result-label {
            font-size: 1.1rem;
            color: #bdc3c7;
        }
        
        .chart-container {
            height: 300px;
            margin-top: 30px;
        }
        
        /* قسم الفيديو */
        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            border-radius: 12px;
            margin: 25px 0;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* روابط التطبيقات */
        .apps-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }
        
        .app-card {
            background: rgba(26, 42, 58, 0.8);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .app-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .app-icon {
            font-size: 3.5rem;
            margin-bottom: 15px;
            color: var(--secondary);
        }
        
        /* التكيف مع الشاشات الصغيرة */
        @media (max-width: 992px) {
            .calculator-container {
                grid-template-columns: 1fr;
            }
            
            .sidebar {
                width: 250px;
            }
        }
        
        @media (max-width: 768px) {
            .main-content {
                padding: 20px 15px;
            }
            
            .section {
                padding: 20px;
            }
            
            .section-title {
                font-size: 1.6rem;
            }
            
            .rating-grid, .apps-grid {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 480px) {
            .header {
                padding: 0 15px;
            }
            
            .logo h1 {
                font-size: 1.3rem;
            }
            
            .sidebar {
                width: 100%;
            }
            
            .calculator-inputs, .calculator-results {
                padding: 20px 15px;
            }
            
            .result-value {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- الشريط العلوي -->
    <div class="header">
        <div class="logo">
            <h1>دليل التداول الشامل</h1>
        </div>
        <button class="menu-btn" id="menuBtn">
            <i class="fas fa-bars"></i>
        </button>
    </div>
    
    <!-- القائمة الجانبية -->
    <div class="sidebar" id="sidebar">
        <div class="sidebar-item active" data-section="broker">
            <i class="fas fa-building"></i>
            <span>شركة الوساطة</span>
        </div>
        <div class="sidebar-item" data-section="ratings">
            <i class="fas fa-star"></i>
            <span>تقييمات الشركة</span>
        </div>
        <div class="sidebar-item" data-section="apps">
            <i class="fas fa-mobile-alt"></i>
            <span>تطبيقات التداول</span>
        </div>
        <div class="sidebar-item" data-section="authentication">
            <i class="fas fa-shield-alt"></i>
            <span>المصادقة الثنائية</span>
        </div>
        <div class="sidebar-item" data-section="telegram">
            <i class="fab fa-telegram"></i>
            <span>قنوات تلجرام</span>
        </div>
        <div class="sidebar-item" data-section="education">
            <i class="fas fa-graduation-cap"></i>
            <span>الدورات التعليمية</span>
        </div>
        <div class="sidebar-item" data-section="investment">
            <i class="fas fa-chart-line"></i>
            <span>حساب الاستثمار</span>
        </div>
        <div class="sidebar-item" data-section="deposit">
            <i class="fas fa-money-bill-wave"></i>
            <span>طريقة الإيداع</span>
        </div>
        <div class="sidebar-item" data-section="calculator">
            <i class="fas fa-calculator"></i>
            <span>حاسبة رأس المال</span>
        </div>
    </div>
    
    <!-- المحتوى الرئيسي -->
    <div class="main-content" id="mainContent">
        <!-- قسم شركة الوساطة -->
        <div class="section active" id="broker">
            <h2 class="section-title">
                <i class="fas fa-building"></i> شركة الوساطة المالية
            </h2>
            
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-link"></i> Rannforex    
                </h3>
                <p>انضم الآن إلى واحدة من أفضل شركات الوساطة المالية في العالم واستمتع بمزايا تداول فريدة أنأ أتداول معهم ولديهم بيئة تداول آمنة ومستقرة:</p>
                <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="btn" target="_blank">
                    <i class="fas fa-user-plus"></i> سجل حساب جديد الآن
                </a>
            </div>
            
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-medal"></i> ميزات شركة راني فوريكس
                </h3>
                <ul class="feature-list">
                    <li>أقل إيداع وسحب 10$ بدون انتظار</li>
                    <li>عمولة تداول قليلة جدا  2$ على كل 1 لوت في الاتجاهين</li>
                    <li>اسبريد منخفض يبدأ من 0.2~1</li>
                    <li>رافعة مالية عالية تصل إلى 1:500</li>
                    <li>تداول آمن على جميع أزواج الفوركس والمعادن والنفط والمؤشرات والعملات المشفرة</li>
                    <li>يدعم حساب خالي من العمولة وحساب تداولكريبتو وحسابات استثمارية</li>
                    <li>يدعم حسابات الشراكة IB والحسابات المدارة  PAMM</li>
                    <li>انزلاق منخفض جداً وتنفيذ فوري للصفقات</li>
                    <li>تقييم ممتاز على مواقع TrustPilot, MyFxbook, WikiFX, Forex Peace Army</li>
                    <li>أمان عالي بسبب خاصية المصادقة الثنائية (2FA)</li>
                    <li>توثيق الحساب من سوريا وأي دولة أخرى</li>
                    <li>نموذج A-Book من أفضل مزودي السيولة</li>
                </ul>
            </div>
            
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-chart-bar"></i> اسبريد راني فوريكس
                </h3>
                <p>يمكنك الاطلاع على متوسط الأسبريد اليومي لجميع أزواج التداول:</p>
                <a href="https://rannforex.com/en/trading/quotesonline/" class="btn btn-secondary" target="_blank">
                    <i class="fas fa-external-link-alt"></i> عرض الأسبريد المتوسط اليومي
                </a>
            </div>
        </div>
        
        <!-- قسم التقييمات -->
        <div class="section" id="ratings">
            <h2 class="section-title">
                <i class="fas fa-star"></i> تقييمات الشركة
            </h2>
            
            <p>شركة RANNFOREX تحصل على تقييمات ممتازة من أفضل المواقع المتخصصة في تقييم شركات الفوركس:</p>
            
            <div class="rating-grid">
                <div class="rating-card">
                    <i class="fas fa-star"></i>
                    <h3>Trust Pilot</h3>
                    <div class="rating-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                    <p>تقييم 4.5/5 من آلاف المستخدمين</p>
                    <a href="https://fr.trustpilot.com/review/rannforex.com" class="btn btn-gold" target="_blank">
                        <i class="fas fa-external-link-alt"></i> زيارة الموقع
                    </a>
                </div>
                
                <div class="rating-card">
                    <i class="fas fa-star"></i>
                    <h3>WikiFX</h3>
                    <div class="rating-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p>تقييم 5/5 مع شهادة موثوقية</p>
                    <a href="https://www.wikifx.com/en/dealer/1141850612.html" class="btn btn-gold" target="_blank">
                        <i class="fas fa-external-link-alt"></i> زيارة الموقع
                    </a>
                </div>
                
                <div class="rating-card">
                    <i class="fas fa-star"></i>
                    <h3>MyFxBook</h3>
                    <div class="rating-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="far fa-star"></i>
                    </div>
                    <p>تقييم 4/5 من المتداولين المحترفين</p>
                    <a href="https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1" class="btn btn-gold" target="_blank">
                        <i class="fas fa-external-link-alt"></i> زيارة الموقع
                    </a>
                </div>
                
                <div class="rating-card">
                    <i class="fas fa-star"></i>
                    <h3>Forex Peace Army</h3>
                    <div class="rating-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                    <p>تقييم 4.4/5 من الجيش السلمي للفوركس</p>
                    <a href="https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review" class="btn btn-gold" target="_blank">
                        <i class="fas fa-external-link-alt"></i> زيارة الموقع
                    </a>
                </div>
            </div>
        </div>
        
        <!-- قسم تطبيقات التداول -->
        <div class="section" id="apps">
            <h2 class="section-title">
                <i class="fas fa-mobile-alt"></i> تطبيقات التداول
            </h2>
            
            <p>هذه التطبيقات الأساسية التي تحتاجها للبدء في رحلتك للتداول:</p>
            
            <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>منصة ميتاتريدر 5</h3>
                    <p>المنصة الأفضل والأكثر موثوقية للتداول في جميع الأسواق المالية</p>
                    <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" class="btn" target="_blank">
                        <i class="fab fa-android"></i> تحميل التطبيق
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-wallet"></i>
                    </div>
                    <h3>المحفظة الإلكترونية</h3>
                    <p>محفظة CWallet الآمنة لإدارة أموالك وعمليات الإيداع والسحب</p>
                    <a href="https://cwallet.com/referral/DvY6dZtS" class="btn" target="_blank">
                        <i class="fas fa-download"></i> تحميل التطبيق
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>المصادقة الثنائية</h3>
                    <p>تطبيق Google Authenticator لحماية حسابك بطبقة أمان إضافية</p>
                    <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" class="btn" target="_blank">
                        <i class="fab fa-android"></i> تحميل التطبيق
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-chart-pie"></i>
                    </div>
                    <h3>تطبيق TradingView</h3>
                    <p>منصة التحليل الفني الأفضل لمتابعة الأسواق واتخاذ قرارات التداول</p>
                    <a href="https://play.google.com/store/apps/details?id=com.tradingview.tradingviewapp" class="btn" target="_blank">
                        <i class="fab fa-android"></i> تحميل التطبيق
                    </a>
                </div>
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3> my fx book</h3>
                    <p>لمعرفة الأخبار</p>
                    <a href="https://play.google.com/store/apps/details?id=com.myfxbook.forex" class="btn" target="_blank">
                        <i class="fab fa-android"></i> تحميل التطبيق
                    </a>
                </div>
            </div>
        </div>


  
﻿
           
        <!-- القسم التعليمي -->
        <div class="section" id="education">
            <h2 class="section-title">
                <i class="fas fa-mobile-alt"></i> كورسات مجانية
            </h2>
            
            <p>هذه الكورسات الأساسية التي تحتاجها للبدء في رحلتك للتداول:</p>
            
            <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>TRADE WITH PATT</h3>
                    <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" class="btn" target="_blank">
                        <i class="fab fa-youtube"></i> مشاهدة الكورس
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-wallet"></i>
                    </div>
                    <h3>Easy Trade</h3>
                    <a href="https://youtube.com/@easytradingeasy?si=9sITj4F_D__TAfb5" class="btn" target="_blank">
                        <i class="fas fa-youtube"></i> مشاهدة الكورس
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>SMART RISK</h3>
                    <a href="https://youtube.com/@smart_risk?si=s0leP3OYv9GuCp3r" class="btn" target="_blank">
                        <i class="fab fa-android"></i> مشاهدة الكورس
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                        <i class="fas fa-chart-pie"></i>
                    </div>
                    <h3>KAMEL M5(instagram)</h3>
                    <a href="https://www.instagram.com/kameel_m5" class="btn" target="_blank">
                     <i class="fab fa-android"></i> مشاهدة الكورس
                    </a>
                </div>
            </div>
        </div>
   





<div class="section" id="investment">
            <h2 class="section-title">
                <i class="fas fa-chart-line"></i> حساب الاستثمار
            </h2>
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-link"></i> Rannforex    
                </h3>
                <p>يمكنك التداول معي بحساب استثمار بحد أدنى للايداع 10$ سأحصل على نسبة 50% من الارباح يمكنك الاطلاع على تفاصيل حسابي الاستثماري هنا</p>
                <a href="https://my.rannforex.com/en/pamm/details/2534/" class="btn" target="_blank">
                    <i class="fas fa-user-plus"></i> استثمر الآن   
                </a>
            </div>
        </div>



              



        <div class="section" id="deposit">
            <h2 class="section-title">
                <i class="fas fa-money-bill-wave"></i> طريقة الإيداع
            </h2> <ol>
            <li><strong>الإيداع:</strong>
                <ul>
                    <li>اضغط على الثلاث شخط في موقع RannForex أعلى يمين الشاشة.</li>
                    <li>اختر <strong>Deposit</strong>.</li>
                    <li>اختر طريقة الإيداع: <strong>Crypto</strong>.</li>
                    <li>اختر حساب التداول.</li>
                    <li>اضغط على <strong>Continue</strong>.</li>
                </ul>
            </li>
            <li><strong>تفاصيل التحويل:</strong>
                <ul>
                    <li>أدخل المبلغ في الفراغ الأول.</li>
                    <li>اختر <strong>USD</strong>.</li>
                    <li>اضغط على <strong>Continue</strong>.</li>
                </ul>
            </li>
            <li><strong>رمز التحقق (2FA):</strong>
                <ul>
                    <li>افتح تطبيق <strong>Google Authenticator</strong>.</li>
                    <li>انسخ الكود المولد لحساب RannForex.</li>
                    <li>أدخل الكود في الفراغ المخصص.</li>
                    <li>اضغط على <strong>Continue</strong>.</li>
                </ul>
            </li>
            <li><strong> اختر TetherUS - USDT:</strong>
                <ul>
                    <li>اختر <strong>BUSD-T-USD (USDT)</strong>.</li>
                    <li>انسخ العنوان المقدم وهو عنوان bep20.</li>
                </ul>
            </li>
            <li><strong>إرسال من Cwallet:</strong>
                <ul>
                    <li>اختر <strong>USDT</strong>.</li>
                    <li>اختر شبكة <strong>BEP20</strong>.</li>
                    <li>أدخل المبلغ بالدولار.</li>
                    <li>الصق العنوان المنسوخ من RannForex.</li>
                    <li>اضغط على <strong>Send</strong>.</li>
                </ul>
            </li>
            <li><strong>تم الإيداع بنجاح!</strong></li>
        </ol>
        </div>















<!-- tlegram section --> 
        <div class="section" id="telegram">
            <h2 class="section-title">
                <i class="fas fa-mobile-alt"></i> قنوات خاصة بي على تلجرام
            </h2>
            
            <p>هذه القنوات الأساسية التي تحتاجها للبدء في رحلتك للتداول:</p>
            
            <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3> قناة الكورس الاساسي</h3>
                    <p>هذه القناة تحوي على كورس متضمن كل شيء لن تحتاج الى كورس غيره </p>
                    <a href="https://t.me/tradewithali003" class="btn" target="_blank">
                        <i class="fab fa-telegram"></i> انضم الآن
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3>القناة </h3>
                    <p> Trade with Ali</p>
                    <a href="https://t.me/Tradewithali001" class="btn" target="_blank">
                        <i class="fab fa-telegram"></i> انضم الآن
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3> حقق الأرباح </h3>
                    <p> سوف أقوم بإرسال إشارات لجميع الاعضاء </p>
                    <a href="https://t.me/tradewithali002" class="btn" target="_blank">
                        <i class="fab fa-telegram"></i> انضم الآن
                    </a>
                </div>
                
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3>للحصول على usdt</h3>
                    <p> هذا البوت يمكن من حلاله الحصول على usdt عن طريق ظوسائل دفع مختلفة في سوريا  </p>
                    <a href="https://t.me/Syria_usdtbot" class="btn" target="_blank">
                        <i class="fab fa-telegram"></i> انضم الآن
                    </a>
                </div>
            </div>
        </div>

        
        <!-- قسم المصادقة الثنائية -->
        <div class="section" id="authentication">
            <h2 class="section-title">
                <i class="fas fa-shield-alt"></i> المصادقة الثنائية
            </h2>
            
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-lock"></i> حماية حسابك بطبقة أمان إضافية
                </h3>
                <p>المصادقة الثنائية (2FA) هي طريقة أمان تطلب من المستخدمين تقديم شكلين مختلفين من الهوية للتحقق من أنفسهم. وهي ضرورية لحماية حساب التداول الخاص بك من الاختراق.</p>
                
                <h4 style="margin: 20px 0 15px; color: var(--accent);">كيفية إعداد المصادقة الثنائية:</h4>
                <ol style="padding-right: 20px; margin-bottom: 20px;">
                    <li style="margin-bottom: 10px;">قم بتنزيل تطبيق Google Authenticator</li>
                    <li style="margin-bottom: 10px;">اضغط السهم الموجود في الشريط العلوي في صفحة الموقع</li>
                    <li style="margin-bottom: 10px;">امسح رمز QR باستخدام التطبيق أو انسخ المفتاح السري</li>
                     <li style="margin-bottom: 10px;">اختر إدخال مفتاح الإعداد  اسم الرمز Rannforex والصق المفتاح السري واختر بالإستناد إلى الوقت</li>
                    <li style="margin-bottom: 10px;">عودة ثم انسخ الرمز من مولد الرموز بالضغط مطولا عليه ثم الصقه في خانة 2fa code </li>
                    <li>يمكنك الآن السحب والإيداع بسهولة وأمان</li>
                </ol>
            </div>
            
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-video"></i> شرح استخدام تطبيق Google Authenticator
                </h3>
                <p>شاهد هذا الفيديو القصير لتعرف كيفية استخدام تطبيق المصادقة الثنائية:</p>
                
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/SlQc3Q6L3HQ" allowfullscreen></iframe>
                </div>
            </div>
        </div>








        
        <!-- قسم حاسبة رأس المال -->
        <div class="section" id="calculator">
            <h2 class="section-title">
                <i class="fas fa-calculator"></i> حاسبة تطور رأس المال
            </h2>
            
            <div class="calculator-container">
                <div class="calculator-inputs">
                    <h3 style="margin-bottom: 20px; color: var(--secondary);">أدخل بيانات التداول</h3>
                    
                    <div class="input-group">
                        <label for="initialCapital">رأس المال الأولي ($)</label>
                        <input type="number" id="initialCapital" value="10000" min="1">
                    </div>
                    
                    <div class="input-group">
                        <label for="winRate">نسبة الصفقات الرابحة (%)</label>
                        <input type="number" id="winRate" value="60" min="0" max="100" step="1">
                    </div>
                    
                    <div class="input-group">
                        <label for="profitRate">معدل الربح لكل صفقة (% من رأس المال)</label>
                        <input type="number" id="profitRate" value="2" min="0" step="0.1">
                    </div>
                    
                    <div class="input-group">
                        <label for="lossRate">معدل الخسارة لكل صفقة (% من رأس المال)</label>
                        <input type="number" id="lossRate" value="1" min="0" step="0.1">
                    </div>
                    
                    <div class="input-group">
                        <label for="updateInterval">عدد الصفقات في كل تحديث</label>
                        <input type="number" id="updateInterval" value="10" min="1">
                    </div>
                    
                    <div class="input-group">
                        <label for="targetCapital">الهدف النهائي ($)</label>
                        <input type="number" id="targetCapital" value="15000" min="1">
                    </div>
                    
                    <button class="btn" id="calculateBtn">
                        <i class="fas fa-calculator"></i> حساب تطور رأس المال
                    </button>
                </div>
                
                <div class="calculator-results">
                    <h3 style="margin-bottom: 20px; color: var(--accent);">نتائج الحساب</h3>
                    
                    <div class="results-grid">
                        <div class="result-box">
                            <div class="result-label">متوسط العائد لكل صفقة</div>
                            <div id="avgReturn" class="result-value">0.80%</div>
                        </div>
                        
                        <div class="result-box">
                            <div class="result-label">عدد الصفقات المطلوبة</div>
                            <div id="tradesRequired" class="result-value">52</div>
                        </div>
                        
                        <div class="result-box">
                            <div class="result-label">معدل النمو الإجمالي</div>
                            <div id="overallGrowth" class="result-value">50.00%</div>
                        </div>
                    </div>
                    
                    <div class="chart-container">
                        <canvas id="growthChart"></canvas>
                    </div>
                </div>
            </div>
        </div>
        
        
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script>
        // التحكم في القائمة الجانبية
        const menuBtn = document.getElementById('menuBtn');
        const sidebar = document.getElementById('sidebar');
        const sidebarItems = document.querySelectorAll('.sidebar-item');
        const sections = document.querySelectorAll('.section');
        const mainContent = document.getElementById('mainContent');
        
        menuBtn.addEventListener('click', () => {
            sidebar.classList.toggle('active');
        });
        
        // تغيير القسم عند النقر على عنصر القائمة
        sidebarItems.forEach(item => {
            item.addEventListener('click', () => {
                const sectionId = item.getAttribute('data-section');
                
                // تحديث العنصر النشط في القائمة
                sidebarItems.forEach(i => i.classList.remove('active'));
                item.classList.add('active');
                
                // إظهار القسم المحدد وإخفاء الآخرين
                sections.forEach(section => {
                    section.classList.remove('active');
                    if (section.id === sectionId) {
                        setTimeout(() => {
                            section.classList.add('active');
                        }, 100);
                    }
                });
                
                // إغلاق القائمة على الأجهزة المحمولة
                if (window.innerWidth < 992) {
                    sidebar.classList.remove('active');
                }
            });
        });
        
        // حاسبة تطور رأس المال
        const calculateBtn = document.getElementById('calculateBtn');
        const ctx = document.getElementById('growthChart').getContext('2d');
        
        let growthChart = new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['0', '10', '20', '30', '40', '50'],
                datasets: [{
                    label: 'رأس المال',
                    data: [10000, 10830, 11730, 12708, 13764, 14913],
                    borderColor: '#3498db',
                    backgroundColor: 'rgba(52, 152, 219, 0.1)',
                    borderWidth: 3,
                    pointBackgroundColor: '#fff',
                    pointRadius: 5,
                    pointHoverRadius: 7,
                    fill: true,
                    tension: 0.3
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        labels: {
                            color: '#ecf0f1',
                            font: {
                                size: 14
                            }
                        }
                    },
                    tooltip: {
                        backgroundColor: 'rgba(44, 62, 80, 0.9)',
                        titleColor: '#ecf0f1',
                        bodyColor: '#ecf0f1',
                        titleFont: {
                            size: 16
                        },
                        bodyFont: {
                            size: 14
                        },
                        padding: 12,
                        displayColors: false,
                        callbacks: {
                            label: function(context) {
                                return '$' + context.parsed.y.toLocaleString();
                            }
                        }
                    }
                },
                scales: {
                    x: {
                        title: {
                            display: true,
                            text: 'عدد الصفقات',
                            color: '#bdc3c7',
                            font: {
                                size: 14,
                                weight: 'bold'
                            }
                        },
                        grid: {
                            color: 'rgba(255, 255, 255, 0.1)'
                        },
                        ticks: {
                            color: '#ecf0f1'
                        }
                    },
                    y: {
                        title: {
                            display: true,
                            text: 'رأس المال ($)',
                            color: '#bdc3c7',
                            font: {
                                size: 14,
                                weight: 'bold'
                            }
                        },
                        grid: {
                            color: 'rgba(255, 255, 255, 0.1)'
                        },
                        ticks: {
                            color: '#ecf0f1',
                            callback: function(value) {
                                return '$' + value.toLocaleString();
                            }
                        }
                    }
                }
            }
        });
        
        calculateBtn.addEventListener('click', calculate);
        
        function calculate() {
            const initialCapital = parseFloat(document.getElementById('initialCapital').value) || 10000;
            const winRate = parseFloat(document.getElementById('winRate').value) || 60;
            const profitRate = parseFloat(document.getElementById('profitRate').value) || 2;
            const lossRate = parseFloat(document.getElementById('lossRate').value) || 1;
            const updateInterval = parseInt(document.getElementById('updateInterval').value) || 10;
            const targetCapital = parseFloat(document.getElementById('targetCapital').value) || 15000;
            
            const winRateDecimal = winRate / 100;
            const profitRateDecimal = profitRate / 100;
            const lossRateDecimal = lossRate / 100;
            
            const expectedReturn = (winRateDecimal * profitRateDecimal) - ((1 - winRateDecimal) * lossRateDecimal);
            document.getElementById('avgReturn').textContent = (expectedReturn * 100).toFixed(2) + '%';
            
            let nTrades;
            if (expectedReturn <= 0) {
                nTrades = '∞';
            } else {
                nTrades = Math.ceil(Math.log(targetCapital / initialCapital) / Math.log(1 + expectedReturn));
            }
            document.getElementById('tradesRequired').textContent = nTrades;
            
            const overallGrowth = ((targetCapital - initialCapital) / initialCapital) * 100;
            document.getElementById('overallGrowth').textContent = overallGrowth.toFixed(2) + '%';
            
            const results = [];
            let tradeCount = 0;
            let currentCapital = initialCapital;
            
            while (tradeCount <= (typeof nTrades === 'number' ? nTrades : 1000)) {
                results.push({
                    trades: tradeCount,
                    capital: currentCapital
                });
                
                if (currentCapital >= targetCapital || tradeCount > 1000) break;
                
                tradeCount += updateInterval;
                currentCapital = initialCapital * Math.pow(1 + expectedReturn, tradeCount);
            }
            
            updateChart(results);
        }
        
        function updateChart(results) {
            const labels = results.map(r => r.trades);
            const data = results.map(r => r.capital);
            
            growthChart.data.labels = labels;
            growthChart.data.datasets[0].data = data;
            growthChart.update();
        }
        
        // حساب أولي عند تحميل الصفحة
        calculate();
        
        // إغلاق القائمة عند النقر خارجها
        document.addEventListener('click', (e) => {
            if (!sidebar.contains(e.target) && !menuBtn.contains(e.target) && window.innerWidth < 992) {
                sidebar.classList.remove('active');
            }
        });
    </script>




====
<div class="section" id="telegram">

    
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نظام تحويل العملات الرقمية في سورية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1a365d;
            --secondary: #2c5282;
            --accent: #38a169;
            --light: #f7fafc;
            --dark: #1a202c;
            --danger: #e53e3e;
            --warning: #dd6b20;
            --light-blue: #e3f2fd;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f0f4f8, #d6e4f0);
            color: var(--dark);
            min-height: 100vh;
            padding: 20px;
            line-height: 1.7;
        }
        
        .container {
            max-width: 400px;
            margin: 0 auto;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.18);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 30px 25px;
            text-align: center;
            position: relative;
        }
        
        header h1 {
            font-size: 2.1rem;
            margin-bottom: 12px;
            font-weight: 800; /* زيادة سمك خط العنوان */
            letter-spacing: -0.5px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
        header p {
            font-size: 1.1rem;
            opacity: 0.9;
            font-weight: 500; /* زيادة سمك خط الوصف */
        }
        
        .logo {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 18px;
            margin-bottom: 15px;
        }
        
        .logo i {
            font-size: 3rem;
            background: rgba(255, 255, 255, 0.15);
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 8px rgba(0,0,0,0.15);
        }
        
        .form-container {
            padding: 30px;
        }
        
        .section {
            margin-bottom: 35px;
            padding-bottom: 25px;
            border-bottom: 1px solid #e2e8f0;
        }
        
        .section-title {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 15px;
            font-weight: 700; /* زيادة سمك خط العنوان */
            padding-bottom: 10px;
            border-bottom: 2px solid var(--light-blue);
        }
        
        .section-title i {
            background-color: #ebf8ff;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.3rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.08);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600; /* زيادة سمك خط التسميات */
            color: var(--dark);
            font-size: 1.05rem;
        }
        
        input, select, textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid #cbd5e0;
            border-radius: 10px;
            font-size: 1.05rem;
            transition: all 0.3s;
            background-color: #f7fafc;
            font-weight: 500; /* زيادة سمك خط الإدخال */
        }
        
        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 4px rgba(66, 153, 225, 0.2);
            background-color: white;
        }
        
        .radio-group {
            display: flex;
            flex-wrap: wrap;
            gap: 18px;
            margin-top: 10px;
        }
        
        .radio-option {
            flex: 1;
            min-width: 140px;
        }
        
        .radio-option input {
            display: none;
        }
        
        .radio-option label {
            display: block;
            padding: 18px 15px;
            border: 2px solid #cbd5e0;
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            background-color: #f7fafc;
            font-size: 1.1rem;
            font-weight: 600; /* زيادة سمك خط الخيارات */
        }
        
        .radio-option input:checked + label {
            border-color: var(--accent);
            background-color: #e6fffa;
            font-weight: 700; /* زيادة سمك الخط عند التحديد */
            box-shadow: 0 4px 10px rgba(56, 161, 105, 0.15);
            transform: translateY(-3px);
        }
        
        .info-box {
            background-color: #ebf8ff;
            border-left: 5px solid var(--secondary);
            padding: 20px;
            border-radius: 10px;
            margin-top: 25px;
            display: none;
        }
        
        .info-box.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        .info-box p {
            margin-bottom: 12px;
            line-height: 1.7;
            font-size: 1.05rem;
            font-weight: 500; /* زيادة سمك خط المعلومات */
        }
        
        .copy-field {
            background-color: white;
            border: 1px solid #cbd5e0;
            border-radius: 10px;
            padding: 14px;
            margin: 12px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        
        .copy-field span {
            font-family: 'Courier New', monospace;
            word-break: break-all;
            font-size: 1.05rem;
            font-weight: 500; /* زيادة سمك خط النص القابل للنسخ */
        }
        
        .copy-btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 10px 18px;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.3s;
            font-weight: 600; /* زيادة سمك نص زر النسخ */
            font-size: 1rem;
            min-width: 90px;
        }
        
        .copy-btn:hover {
            background: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 3px 8px rgba(0,0,0,0.15);
        }
        
        .btn {
            display: block;
            width: 100%;
            padding: 18px;
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1.15rem;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 25px;
            font-weight: 700; /* زيادة سمك نص الأزرار */
            letter-spacing: 0.5px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.15);
        }
        
        .review-btn {
            background: linear-gradient(to right, var(--warning), #e67e22);
        }
        
        .submit-btn {
            background: linear-gradient(to right, var(--accent), #2ecc71);
            display: none;
        }
        
        .btn:hover {
            opacity: 0.95;
            transform: translateY(-3px);
            box-shadow: 0 7px 18px rgba(0,0,0,0.2);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .summary {
            display: none;
            background: #f0f7ff;
            border-radius: 12px;
            padding: 25px;
            margin-top: 25px;
            border: 2px solid #c5defa;
        }
        
        .summary-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 18px;
            padding-bottom: 18px;
            border-bottom: 1px dashed #cbd5e0;
            font-size: 1.1rem;
            font-weight: 500; /* زيادة سمك خط العناصر */
        }
        
        .summary-item span:first-child {
            font-weight: 600; /* زيادة سمك نص التصنيفات */
            color: var(--primary);
        }
        
        .summary-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
            font-weight: 700; /* زيادة سمك خط المجموع */
            font-size: 1.3rem;
            color: var(--primary);
            margin-top: 10px;
            padding-top: 10px;
            border-top: 2px dashed #cbd5e0;
        }
        
        .success-message {
            text-align: center;
            padding: 40px 30px;
            display: none;
            background: #f8fff8;
            border-radius: 12px;
            border: 2px solid #c5fad5;
            margin-top: 20px;
        }
        
        .success-message i {
            font-size: 4.5rem;
            color: var(--accent);
            margin-bottom: 25px;
        }
        
        .success-message h2 {
            color: var(--accent);
            margin-bottom: 25px;
            font-size: 2.2rem;
            font-weight: 800; /* زيادة سمك خط عنوان النجاح */
        }
        
        .success-message p {
            font-size: 1.15rem;
            margin-bottom: 25px;
            font-weight: 500; /* زيادة سمك خط النص */
            line-height: 1.8;
        }
        
        .fee-info {
            background: #fff8e1;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            border-left: 5px solid var(--warning);
            font-size: 1.1rem;
            font-weight: 600; /* زيادة سمك خط معلومات العمولة */
            box-shadow: 0 3px 8px rgba(0,0,0,0.05);
        }
        
        .fee-info i {
            color: var(--warning);
            margin-left: 8px;
        }
        
        #finalSummary {
            background: white;
            padding: 25px;
            border-radius: 12px;
            text-align: right;
            border: 1px solid #e2e8f0;
            margin-top: 20px;
            font-size: 1.1rem;
        }
        
        #finalSummary p {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
            font-weight: 500; /* زيادة سمك خط الملخص النهائي */
        }
        
        #finalSummary p:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        #finalSummary strong {
            font-weight: 700; /* زيادة سمك الخط للكلمات البارزة */
            color: var(--primary);
            min-width: 160px;
            display: inline-block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @media (max-width: 768px) {
            .radio-group {
                flex-direction: column;
            }
            
            .radio-option {
                min-width: 100%;
            }
            
            .container {
                border-radius: 12px;
            }
            
            header {
                padding: 25px 20px;
            }
            
            header h1 {
                font-size: 1.8rem;
            }
            
            .form-container {
                padding: 20px;
            }
            
            .section-title {
                font-size: 1.35rem;
            }
            
            .btn {
                padding: 16px;
                font-size: 1.1rem;
            }
        }
        
        @media (max-width: 480px) {
            body {
                padding: 10px;
            }
            
            header {
                padding: 20px 15px;
            }
            
            header h1 {
                font-size: 1.6rem;
            }
            
            .logo i {
                width: 65px;
                height: 65px;
                font-size: 2.5rem;
            }
            
            .form-container {
                padding: 15px;
            }
            
            .section-title {
                font-size: 1.25rem;
            }
            
            .copy-btn {
                padding: 8px 12px;
                font-size: 0.9rem;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <i class="fas fa-coins"></i>
                <div>
                    <h1>نظام تحويل العملات الرقمية في سورية</h1>
                    <p>تحويل USDT بوسائل الدفع المحلية</p>
                </div>
            </div>
        </header>
        
        <div class="form-container">
            <div class="section">
                <h2 class="section-title"><i class="fas fa-user"></i> المعلومات الشخصية</h2>
                <div class="form-group">
                    <label for="fullname">الاسم الثلاثي</label>
                    <input type="text" id="fullname" placeholder="الاسم الكامل">
                </div>
                
                <div class="form-group">
                    <label for="phone">رقم الهاتف</label>
                    <input type="tel" id="phone" placeholder="09xxxxxxxx">
                </div>
                
                <div class="form-group">
                    <label for="city">المدينة</label>
                    <input type="text" id="city" placeholder="المدينة">
                </div>
            </div>
            
            <div class="fee-info">
                <i class="fas fa-info-circle"></i>
                <strong>نظام العمولة المحدث:</strong> 1 دولار ثابت + 0.5% من المبلغ الكامل
            </div>
            
            <div class="section">
                <h2 class="section-title"><i class="fas fa-exchange-alt"></i> نوع العملية</h2>
                <div class="radio-group">
                    <div class="radio-option">
                        <input type="radio" id="buy" name="transactionType" value="buy" checked>
                        <label for="buy">شراء USDT</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="sell" name="transactionType" value="sell">
                        <label for="sell">بيع USDT</label>
                    </div>
                </div>
            </div>
            
            <!-- Buy Section -->
            <div id="buySection">
                <div class="section">
                    <h2 class="section-title"><i class="fas fa-shopping-cart"></i> تفاصيل الشراء</h2>
                    
                    <div class="form-group">
                        <label for="buyAmount">الكمية المطلوبة (USDT)</label>
                        <input type="number" id="buyAmount" placeholder="أدخل الكمية">
                    </div>
                    
                    <div class="form-group">
                        <label for="buyNetwork">اختر الشبكة</label>
                        <select id="buyNetwork">
                            <option value="bep20">BEP20</option>
                            <option value="trc20">TRC20</option>
                            <option value="erc20">ERC20</option>
                            <option value="binance">Binance Pay</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="buyAddress">العنوان (لإرسال USDT)</label>
                        <input type="text" id="buyAddress" placeholder="أدخل عنوان المحفظة">
                    </div>
                    
                    <div class="form-group">
                        <label for="buyNotes">ملاحظات (اختياري)</label>
                        <textarea id="buyNotes" rows="2" placeholder="أي ملاحظات إضافية"></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="paymentMethod">طريقة الدفع</label>
                        <select id="paymentMethod">
                            <option value="">اختر طريقة الدفع</option>
                            <option value="sham">شام كاش</option>
                            <option value="syriatel">سيريتل كاش</option>
                            <option value="hawala">حوالة الهرم</option>
                            <option value="bimo">بنك بيمو</option>
                        </select>
                    </div>
                    
                    <div class="info-box" id="shamInfo">
                        <p>الدفع عبر شام كاش:</p>
                        <div class="copy-field">
                            <span>be456e0ea9392db4d68a7093ee317bc8</span>
                            <button class="copy-btn" data-clipboard-text="be456e0ea9392db4d68a7093ee317bc8">نسخ</button>
                        </div>
                        <p>رقم الحساب: 5991161126028260</p>
                    </div>
                    
                    <div class="info-box" id="syriatelInfo">
                        <p>الدفع عبر سيريتل كاش:</p>
                        <div class="copy-field">
                            <span>0934598967</span>
                            <button class="copy-btn" data-clipboard-text="0934598967">نسخ</button>
                        </div>
                    </div>
                    
                    <div class="info-box" id="hawalaInfo">
                        <p>الدفع عبر حوالة الهرم:</p>
                        <p>الاسم: علي ابراهيم محمود</p>
                        <p>رقم الهاتف: 0934598967</p>
                        <p>المدينة: اللاذقية</p>
                    </div>
                    
                    <div class="info-box" id="bimoInfo">
                        <p>الدفع عبر بنك بيمو:</p>
                        <div class="copy-field">
                            <span>060104947910013000000</span>
                            <button class="copy-btn" data-clipboard-text="060104947910013000000">نسخ</button>
                        </div>
                        <p>الاسم: علي ابراهيم محمود</p>
                    </div>
                </div>
            </div>
            
            <!-- Sell Section -->
            <div id="sellSection" style="display: none;">
                <div class="section">
                    <h2 class="section-title"><i class="fas fa-money-bill-wave"></i> تفاصيل البيع</h2>
                    
                    <div class="form-group">
                        <label for="sellAmount">الكمية المعروضة (USDT)</label>
                        <input type="number" id="sellAmount" placeholder="أدخل الكمية">
                    </div>
                    
                    <div class="form-group">
                        <label for="receiveMethod">طريقة الاستلام</label>
                        <select id="receiveMethod">
                            <option value="">اختر طريقة الاستلام</option>
                            <option value="syriatel">سيريتل كاش</option>
                            <option value="hawala">حوالة الهرم</option>
                            <option value="bimo">بنك بيمو</option>
                            <option value="sham">شام كاش</option>
                        </select>
                    </div>
                    
                    <div class="form-group" id="bimoAccountGroup" style="display: none;">
                        <label for="bimoAccount">رقم الحساب البنكي</label>
                        <input type="text" id="bimoAccount" placeholder="رقم الحساب">
                    </div>
                    
                    <div class="form-group" id="shamAccountGroup" style="display: none;">
                        <label for="shamAccount">رقم الحساب أو العنوان</label>
                        <input type="text" id="shamAccount" placeholder="رقم الحساب أو العنوان">
                    </div>
                    
                    <div class="form-group">
                        <label for="sellNotes">ملاحظات (اختياري)</label>
                        <textarea id="sellNotes" rows="2" placeholder="أي ملاحظات إضافية"></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="sellNetwork">اختر الشبكة</label>
                        <select id="sellNetwork">
                            <option value="">اختر شبكة الاستلام</option>
                            <option value="bep20">BEP20</option>
                            <option value="trc20">TRC20</option>
                            <option value="erc20">ERC20</option>
                            <option value="binance">Binance Pay</option>
                        </select>
                    </div>
                    
                    <div class="info-box" id="bep20Info">
                        <p>العنوان BEP20:</p>
                        <div class="copy-field">
                            <span>0x21802218d8d661d66F2C7959347a6382E1cc614F</span>
                            <button class="copy-btn" data-clipboard-text="0x21802218d8d661d66F2C7959347a6382E1cc614F">نسخ</button>
                        </div>
                    </div>
                    
                    <div class="info-box" id="trc20Info">
                        <p>العنوان TRC20:</p>
                        <div class="copy-field">
                            <span>TD2LoErPRkVPBxDk72ZErtiyi6agirZQjX</span>
                            <button class="copy-btn" data-clipboard-text="TD2LoErPRkVPBxDk72ZErtiyi6agirZQjX">نسخ</button>
                        </div>
                    </div>
                    
                    <div class="info-box" id="erc20Info">
                        <p>العنوان ERC20:</p>
                        <div class="copy-field">
                            <span>0x21802218d8d661d66F2C7959347a6382E1cc614F</span>
                            <button class="copy-btn" data-clipboard-text="0x21802218d8d661d66F2C7959347a6382E1cc614F">نسخ</button>
                        </div>
                    </div>
                    
                    <div class="info-box" id="binanceInfo">
                        <p>Binance Pay:</p>
                        <div class="copy-field">
                            <span>969755964</span>
                            <button class="copy-btn" data-clipboard-text="969755964">نسخ</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <button id="reviewBtn" class="btn review-btn">مراجعة الطلب</button>
            
            <div class="summary" id="summarySection">
                <h2 class="section-title"><i class="fas fa-file-invoice"></i> ملخص الطلب</h2>
                <div class="summary-item">
                    <span>الاسم:</span>
                    <span id="summaryName"></span>
                </div>
                <div class="summary-item">
                    <span>رقم الهاتف:</span>
                    <span id="summaryPhone"></span>
                </div>
                <div class="summary-item">
                    <span>نوع العملية:</span>
                    <span id="summaryType"></span>
                </div>
                <div class="summary-item">
                    <span>الكمية (USDT):</span>
                    <span id="summaryAmount"></span>
                </div>
                <div class="summary-item">
                    <span>عمولة التحويل (1 دولار + 0.5%):</span>
                    <span id="summaryFee"></span>
                </div>
                <div class="summary-item">
                    <span>عمولة الشبكة:</span>
                    <span id="summaryNetworkFee"></span>
                </div>
                <div class="summary-item">
                    <span>المبلغ الإجمالي (SYP):</span>
                    <span id="summaryTotal"></span>
                </div>
                <div class="summary-item">
                    <span>ملاحظات:</span>
                    <span id="summaryNotes"></span>
                </div>
                <p style="margin-top: 20px; padding: 15px; background: #fff8f8; border-radius: 8px; font-weight: 600;">
                    <i class="fas fa-info-circle"></i> عمولة التسديد على طرق التحويل المختلفة بالليرة السورية تقع على المستخدم كما تحددها هذه الجهات
                </p>
            </div>
            
            <button id="submitBtn" class="btn submit-btn">إرسال الطلب</button>
            
            <div class="success-message" id="successMessage">
                <i class="fas fa-check-circle"></i>
                <h2>تم إرسال الطلب بنجاح!</h2>
                <p>تم إرسال تفاصيل طلبك إلى بريدنا الإلكتروني وسنتواصل معك قريبًا.</p>
                <p>تفاصيل الطلب:</p>
                <div id="finalSummary"></div>
            </div>
        </div>
    </div>
    
    <script>
        // Constants
        const EXCHANGE_RATE = 9850; // SYP per USD
        const NETWORK_FEES = {
            'bep20': 0.15,
            'trc20': 2,
            'erc20': 0.3,
            'binance': 0
        };
        
        // DOM Elements
        const buySection = document.getElementById('buySection');
        const sellSection = document.getElementById('sellSection');
        const transactionTypeRadios = document.querySelectorAll('input[name="transactionType"]');
        const paymentMethod = document.getElementById('paymentMethod');
        const receiveMethod = document.getElementById('receiveMethod');
        const reviewBtn = document.getElementById('reviewBtn');
        const submitBtn = document.getElementById('submitBtn');
        const summarySection = document.getElementById('summarySection');
        const successMessage = document.getElementById('successMessage');
        
        // Toggle sections based on transaction type
        transactionTypeRadios.forEach(radio => {
            radio.addEventListener('change', () => {
                if (radio.value === 'buy') {
                    buySection.style.display = 'block';
                    sellSection.style.display = 'none';
                } else {
                    buySection.style.display = 'none';
                    sellSection.style.display = 'block';
                }
            });
        });
        
        // Show payment info based on selected method
        paymentMethod.addEventListener('change', () => {
            // Hide all info boxes first
            document.querySelectorAll('#buySection .info-box').forEach(box => {
                box.classList.remove('active');
            });
            
            // Show selected info box
            if (paymentMethod.value === 'sham') {
                document.getElementById('shamInfo').classList.add('active');
            } else if (paymentMethod.value === 'syriatel') {
                document.getElementById('syriatelInfo').classList.add('active');
            } else if (paymentMethod.value === 'hawala') {
                document.getElementById('hawalaInfo').classList.add('active');
            } else if (paymentMethod.value === 'bimo') {
                document.getElementById('bimoInfo').classList.add('active');
            }
        });
        
        // Show account fields for sell section
        receiveMethod.addEventListener('change', () => {
            document.getElementById('bimoAccountGroup').style.display = 'none';
            document.getElementById('shamAccountGroup').style.display = 'none';
            
            if (receiveMethod.value === 'bimo') {
                document.getElementById('bimoAccountGroup').style.display = 'block';
            } else if (receiveMethod.value === 'sham') {
                document.getElementById('shamAccountGroup').style.display = 'block';
            }
        });
        
        // Show network info for sell section
        document.getElementById('sellNetwork').addEventListener('change', function() {
            // Hide all info boxes first
            document.querySelectorAll('#sellSection .info-box').forEach(box => {
                box.classList.remove('active');
            });
            
            // Show selected info box
            if (this.value === 'bep20') {
                document.getElementById('bep20Info').classList.add('active');
            } else if (this.value === 'trc20') {
                document.getElementById('trc20Info').classList.add('active');
            } else if (this.value === 'erc20') {
                document.getElementById('erc20Info').classList.add('active');
            } else if (this.value === 'binance') {
                document.getElementById('binanceInfo').classList.add('active');
            }
        });
        
        // Copy functionality
        document.querySelectorAll('.copy-btn').forEach(button => {
            button.addEventListener('click', function() {
                const text = this.getAttribute('data-clipboard-text');
                navigator.clipboard.writeText(text).then(() => {
                    const originalText = this.textContent;
                    this.textContent = 'تم النسخ!';
                    setTimeout(() => {
                        this.textContent = originalText;
                    }, 2000);
                });
            });
        });
        
        // Calculate fees with new structure: $1 + 0.5% of total amount
        function calculateFees(amount, network) {
            // العمولة الجديدة: 1 دولار ثابت + 0.5% من المبلغ
            const transactionFee = 1 + (amount * 0.005);
            
            const networkFee = NETWORK_FEES[network] || 0;
            const totalFeeUSD = transactionFee + networkFee;
            const totalFeeSYP = totalFeeUSD * EXCHANGE_RATE;
            
            return {
                transactionFee,
                networkFee,
                totalFeeUSD,
                totalFeeSYP
            };
        }
        
        // Review button handler
        reviewBtn.addEventListener('click', function(e) {
            e.preventDefault();
            
            // Get basic user info
            const fullName = document.getElementById('fullname').value;
            const phone = document.getElementById('phone').value;
            const city = document.getElementById('city').value;
            
            // Validate required fields
            if (!fullName || !phone || !city) {
                alert('الرجاء ملء جميع الحقول الإلزامية');
                return;
            }
            
            const transactionType = document.querySelector('input[name="transactionType"]:checked').value;
            
            // Transaction specific data
            let amount, network, notes;
            let methodDetails = '';
            
            if (transactionType === 'buy') {
                amount = parseFloat(document.getElementById('buyAmount').value);
                network = document.getElementById('buyNetwork').value;
                notes = document.getElementById('buyNotes').value;
                const method = document.getElementById('paymentMethod').value;
                
                if (!amount || amount <= 0 || !network || !method) {
                    alert('الرجاء ملء جميع الحقول الإلزامية في قسم الشراء');
                    return;
                }
                
                // Get method details
                switch(method) {
                    case 'sham':
                        methodDetails = 'شام كاش: be456e0ea9392db4d68a7093ee317bc8';
                        break;
                    case 'syriatel':
                        methodDetails = 'سيريتل كاش: 0934598967';
                        break;
                    case 'hawala':
                        methodDetails = 'حوالة الهرم: علي ابراهيم محمود - 0934598967 - اللاذقية';
                        break;
                    case 'bimo':
                        methodDetails = 'بنك بيمو: 060104947910013000000';
                        break;
                }
            } else {
                amount = parseFloat(document.getElementById('sellAmount').value);
                network = document.getElementById('sellNetwork').value;
                notes = document.getElementById('sellNotes').value;
                const method = document.getElementById('receiveMethod').value;
                
                if (!amount || amount <= 0 || !network || !method) {
                    alert('الرجاء ملء جميع الحقول الإلزامية في قسم البيع');
                    return;
                }
                
                // Get method details
                let accountInfo = '';
                if (method === 'bimo') {
                    accountInfo = document.getElementById('bimoAccount').value;
                } else if (method === 'sham') {
                    accountInfo = document.getElementById('shamAccount').value;
                }
                
                switch(method) {
                    case 'syriatel':
                        methodDetails = 'سيريتل كاش: ' + phone;
                        break;
                    case 'hawala':
                        methodDetails = 'حوالة الهرم: ' + fullName + ' - ' + phone + ' - ' + city;
                        break;
                    case 'bimo':
                        methodDetails = 'بنك بيمو: ' + accountInfo;
                        break;
                    case 'sham':
                        methodDetails = 'شام كاش: ' + accountInfo;
                        break;
                }
            }
            
            // Calculate fees
            const fees = calculateFees(amount, network);
            const totalAmountSYP = transactionType === 'buy' ? 
                (amount + fees.totalFeeUSD) * EXCHANGE_RATE : 
                (amount - fees.totalFeeUSD) * EXCHANGE_RATE;
            
            // Update summary
            document.getElementById('summaryName').textContent = fullName;
            document.getElementById('summaryPhone').textContent = phone;
            document.getElementById('summaryType').textContent = transactionType === 'buy' ? 'شراء' : 'بيع';
            document.getElementById('summaryAmount').textContent = amount + ' USDT';
            document.getElementById('summaryFee').textContent = fees.transactionFee.toFixed(2) + ' USD (' + (fees.transactionFee * EXCHANGE_RATE).toLocaleString() + ' SYP)';
            document.getElementById('summaryNetworkFee').textContent = fees.networkFee.toFixed(2) + ' USD (' + (fees.networkFee * EXCHANGE_RATE).toLocaleString() + ' SYP)';
            document.getElementById('summaryTotal').textContent = totalAmountSYP.toLocaleString() + ' SYP';
            document.getElementById('summaryNotes').textContent = notes || 'لا يوجد';
            
            // Store data for submission
            window.transactionData = {
                fullName,
                phone,
                city,
                transactionType,
                amount,
                network,
                notes,
                methodDetails,
                fees,
                totalAmountSYP
            };
            
            // Show summary and submit button
            summarySection.style.display = 'block';
            submitBtn.style.display = 'block';
            reviewBtn.style.display = 'none';
            
            // Scroll to summary
            summarySection.scrollIntoView({ behavior: 'smooth' });
        });
        
        // Submit button handler
        submitBtn.addEventListener('click', function(e) {
            e.preventDefault();
            
            const data = window.transactionData;
            
            // Prepare final summary for email
            const finalSummary = `
                <p><strong>الاسم:</strong> ${data.fullName}</p>
                <p><strong>رقم الهاتف:</strong> ${data.phone}</p>
                <p><strong>المدينة:</strong> ${data.city}</p>
                <p><strong>نوع العملية:</strong> ${data.transactionType === 'buy' ? 'شراء' : 'بيع'}</p>
                <p><strong>الكمية:</strong> ${data.amount} USDT</p>
                <p><strong>عمولة التحويل:</strong> ${data.fees.transactionFee.toFixed(2)} USD</p>
                <p><strong>عمولة الشبكة:</strong> ${data.fees.networkFee.toFixed(2)} USD</p>
                <p><strong>المبلغ الإجمالي:</strong> ${data.totalAmountSYP.toLocaleString()} SYP</p>
                <p><strong>تفاصيل الدفع/الاستلام:</strong> ${data.methodDetails}</p>
                <p><strong>ملاحظات:</strong> ${data.notes || 'لا يوجد'}</p>
            `;
            
            document.getElementById('finalSummary').innerHTML = finalSummary;
            
            // Prepare email content
            const subject = `طلب جديد: ${data.transactionType === 'buy' ? 'شراء' : 'بيع'} USDT`;
            const body = `تفاصيل الطلب الجديد:%0D%0A%0D%0A${finalSummary.replace(/<[^>]*>/g, '')}`;
            
            // Show success message
            summarySection.style.display = 'none';
            submitBtn.style.display = 'none';
            successMessage.style.display = 'block';
            
            // Create mailto link
            const mailtoLink = `mailto:alimahmoud001a@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
            
            // Open email client
            window.location.href = mailtoLink;
        });
    </script>
</section>


====



<!--Start of Tawk.to Script-->
<script type="text/javascript">
var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
(function(){
var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
s1.async=true;
s1.src='https://embed.tawk.to/6843680cc265e21908a097c7/1it3kssj8';
s1.charset='UTF-8';
s1.setAttribute('crossorigin','*');
s0.parentNode.insertBefore(s1,s0);
})();
</script>
<!--End of Tawk.to Script-->
<!--End of Tawk.to Script-->




<!-- HTML: ?? ?????? -->
<a href="https://t.me/ali0619000" target="_blank" id="telegram-float" aria-label="????? ??? ??????">
  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="#ffffff" viewBox="0 0 24 24">
    <path d="M9.99999 17.3333L19.8333 6.49996C20.3333 5.99996 19.6667 5.16663 18.8333 5.49996L3.33332 11.5C2.66666 11.8333 2.66666 12.6666 3.33332 12.8333L7.66666 13.8333L15.5 8.33329C15.8333 8.16663 16 8.33329 15.8333 8.66663L10.3333 16.5L9.99999 17.3333Z"></path>
  </svg>

<!-- CSS: ????? ???? ?????? -->
<style>
#telegram-float {
  position: fixed;
  right: 20px;
  bottom: 120px;
  background: linear-gradient(45deg, #0088cc, #00bfff);
  width: 55px;
  height: 55px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  z-index: 9999;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

#telegram-float:hover {
  transform: scale(1.1);
  box-shadow: 0 6px 20px rgba(0,0,0,0.3);
}

#telegram-float svg {
  width: 28px;
  height: 28px;
}
</style>

