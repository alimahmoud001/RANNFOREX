<!DOCTYPE html>
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
                    <i class="fas fa-link"></i> رابط التسجيل في شركة راني فوريكس
                </h3>
                <p>انضم الآن إلى واحدة من أفضل شركات الوساطة المالية في العالم واستمتع بمزايا تداول فريدة:</p>
                <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="btn" target="_blank">
                    <i class="fas fa-user-plus"></i> سجل حساب جديد الآن
                </a>
            </div>
            
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-medal"></i> ميزات شركة راني فوريكس
                </h3>
                <ul class="feature-list">
                    <li>أقل إيداع 10$ خلال 30 ثانية فقط</li>
                    <li>أقل سحب 10$ خلال 30 ثانية</li>
                    <li>عمولة تداول قليلة جداً</li>
                    <li>اسبريد منخفض يبدأ من 0.3~1.2</li>
                    <li>رافعة مالية عالية تصل إلى 1:500</li>
                    <li>تداول آمن على جميع أزواج الفوركس والمعادن والنفط والمؤشرات والعملات المشفرة</li>
                    <li>أربع أنواع من الحسابات: ميتاتريدر 5 حقيقي، بدون عمولة، كريبتو، وحساب IB</li>
                    <li>يدعم الحسابات المدارة PAMM</li>
                    <li>انزلاق منخفض جداً</li>
                    <li>تنفيذ فوري للصفقات</li>
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
            
            <p>شركة راني فوريكس تحصل على تقييمات ممتازة من أفضل المواقع المتخصصة في تقييم شركات الفوركس:</p>
            
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
                    <a href="https://www.forexpeacearmy.com/forex-reviews/15
