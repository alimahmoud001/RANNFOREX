
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
            padding: 0px;
            transition: all 0.4s ease;
        }
        
        .section {
            background: rgba(13, 23, 33, 0.7);
            border-radius: 15px;
            padding: 0px;
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
            padding: 5px;
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
            content: "";
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
            padding: 7px;
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
        .usdt-container iframe {
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
                padding: 1px 1px;
            }
            
            .section {
                padding: 1px;
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
                padding: 0 1px;
            }
            
            .logo h1 {
                font-size: 1.3rem;
            }
            
            .sidebar {
                width: 100%;
            }
            
            .calculator-inputs, .calculator-results {
                padding: 1px 1px;
            }
            
            .result-value {
                font-size: 1.5rem;
            }
        }
    </style>
  <!-------------------------------------------------،>
 
  ------------------------------------------------->
  <!--Start of Tawk.to Script-->
<style>
  .telegram-float {
    position: fixed;
    width: 60px;
    height: 60px;
    bottom: 30px;
    left: 30px;
    background-color: #2AABEE;
    color: #FFF;
    border-radius: 50px;
    text-align: center;
    font-size: 30px;
    box-shadow: 0 4px 16px rgba(42, 171, 238, 0.5);
    z-index: 1000;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
    animation: pulse 2s infinite;
    text-decoration: none;
  }
  
  .telegram-float:hover {
    background-color: #128BD7;
    transform: scale(1.1);
    box-shadow: 0 6px 20px rgba(42, 171, 238, 0.7);
  }
  
  @keyframes pulse {
    0% {
      box-shadow: 0 0 0 0 rgba(42, 171, 238, 0.7);
    }
    70% {
      box-shadow: 0 0 0 10px rgba(42, 171, 238, 0);
    }
    100% {
      box-shadow: 0 0 0 0 rgba(42, 171, 238, 0);
    }
  }
  
  .telegram-icon {
    width: 30px;
    height: 30px;
    fill: white;
  }
</style>

<a href="https://t.me/ali0619000" class="telegram-float" target="_blank">
  <svg class="telegram-icon" viewBox="0 0 24 24">
    <path d="M12 0c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm5.894 8.221l-1.97 9.28c-.145.658-.537.818-1.084.508l-3-2.21-1.447 1.394c-.14.141-.259.259-.374.261l.213-3.053 5.56-5.022c.24-.213-.054-.334-.373-.121l-6.869 4.326-2.96-.924c-.64-.203-.658-.64.136-.954l11.566-4.458c.538-.196 1.006.128.832.941z"/>
  </svg>
</a>
    <!-------------------------------------------------> 
    
<html>
<head>
    <style>
        /* تنسيق الأيقونة العائمة الجديدة */
        .floating-deal {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #FF5722; /* لون برتقالي جذاب */
            color: white;
            padding: 12px 24px;
            border-radius: 30px; /* حواف مستديرة */
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            font-weight: bold;
            z-index: 9999;
            transition: all 0.3s;
            border: none;
            white-space: nowrap;
        }
        
        .floating-deal:hover {
            background-color: #E64A19;
            transform: translateX(-50%) scale(1.05);
        }
        
        .deal-icon {
            margin-right: 8px;
            font-size: 20px;
        }
        
        /* تنسيق النافذة المنبثقة */
        .popup-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 10000;
        }
        
        .popup-content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 80%;
            height: 80%;
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .popup-close {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #f44336;
            color: white;
            border: none;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            cursor: pointer;
            z-index: 10001;
        }
        
        .popup-iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
    </style>
</head>
<body>
    <!-- الأيقونة العائمة الجديدة -->
    <button class="floating-deal" id="floatingDeal">
        <span class="deal-icon">🎁</span>
        <span>عرض خاص!</span>
    </button>
    
    <!-- النافذة المنبثقة -->
    <div class="popup-overlay" id="popupOverlay">
        <button class="popup-close" id="popupClose">×</button>
        <div class="popup-content">
            <iframe class="popup-iframe" id="popupIframe" src="about:blank"></iframe>
        </div>
    </div>
    
    <script>
        // عناصر DOM
        const floatingDeal = document.getElementById('floatingDeal');
        const popupOverlay = document.getElementById('popupOverlay');
        const popupClose = document.getElementById('popupClose');
        const popupIframe = document.getElementById('popupIframe');
        
        // الرابط المطلوب
        const formUrl = 'https://docs.google.com/forms/d/e/1FAIpQLSfJPgS_xgOyzY9k2HBBvBBu5fl4Zhg-VK7VjETkfRh7hZzWPw/viewform?usp=dialog';
        
        // حدث النقر على الأيقونة العائمة
        floatingDeal.addEventListener('click', function() {
            popupIframe.src = formUrl;
            popupOverlay.style.display = 'block';
            document.body.style.overflow = 'hidden';
        });
        
        // حدث النقر على زر الإغلاق
        popupClose.addEventListener('click', function() {
            popupOverlay.style.display = 'none';
            popupIframe.src = 'about:blank';
            document.body.style.overflow = 'auto';
        });
        
        // إغلاق النافذة عند النقر خارجها
        popupOverlay.addEventListener('click', function(e) {
            if (e.target === popupOverlay) {
                popupOverlay.style.display = 'none';
                popupIframe.src = 'about:blank';
                document.body.style.overflow = 'auto';
            }
        });
    </script>
</body>
</html>
    <!------------------------------------------------->

</head>
<body>
    <!-- الشريط العلوي -->
    <div class="header">
        <div class="logo">
            <h1>Rannforex</h1>
        </div>
        <button class="menu-btn" id="menuBtn">
            <i class="fas fa-bars"></i>
        </button>
    </div>
    
    <!-- القائمة الجانبية -->
    <div class="sidebar" id="sidebar">
        <div class="sidebar-item active" data-section="broker">
            <i class="fas fa-building"></i>
            <span>Rannforex</span>
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
          <div class="sidebar-item" data-section="education">
            <i class="fas fa-graduation-cap"></i>
            <span>الدورات التعليمية</span>
        </div>
        <div class="sidebar-item" data-section="investment">
            <i class="fas fa-chart-line"></i>
            <span>حساب الاستثمار</span>
        </div>
      <div class="sidebar-item" data-section="usdt">
            <i class="fas fa-money-bill-wave"></i>
            <span>شراء وبيع usdt</span>
        </div>
        <div class="sidebar-item" data-section="deposit">
            <i class="fas fa-money-bill-wave"></i>
            <span>طريقة الإيداع</span>
        </div>
         <!-- <div class="sidebar-item" data-section="telegram">
            <i class="fab fa-telegram"></i>
            <span>قنوات تلجرام</span>
        </div>-->
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
                <p>انضم الآن إلى واحدة من أفضل شركات الوساطة المالية في العالم واستمتع بمزايا تداول فريدة أنأ أتداول معهم ولديهم بيئة تداول آمنة ومستقرة</p>
                <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="btn" target="_blank">
                    <i class="fas fa-user-plus"></i> سجل حساب جديد الآن
                </a>
            </div>
            
            <div class="card">
                <h3 class="card-title">
                    <i class="fas fa-medal"></i> ميزات شركة Rannforex
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
                    <p>محفظة باينانس الآمنة لإدارة أموالك وعمليات الإيداع والسحب</p>
                    <a href="https://www.binance.com/activity/referral-entry/CPA?ref=CPA_004C6HBMJS" class="btn" target="_blank">
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
            </div>
        </div>


  
<!-- investment section --> 
        <div class="section" id="investment">
            <h2 class="section-title">
                <i class="fas fa-mobile-alt"></i> اطلع على تفاصيل حساب الإستثمار الحاص بي
            </h2>
            
            <p>اطلع على تفاصيل حساب الإستثمار الحاص بي</p>
            
            <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3> حساب الشراكة pamm</h3>
                    <p>يمكنك أن تستثمر معي وأن نتقاسم 50% من الأرباح</p>
                  <a href="https://my.rannforex.com/en/pamm/details/2534/" class="btn" target="_blank">
                     <i class="fab fa-telegram"></i> استثمر الآن
                    </a>
                </div>
            </div>
        </div>
        

<!------------------- usdt --> 
        <div class="section" id="usdt">
            <h2 class="section-title">
                <i class="fas fa-mobile-alt"></i>شراء وبيع usdt
            </h2>
            
            <p>من أجل شحن المحفظة الخاصة بك أو الإيداع في حساب التداول</p>
            
            <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3> أرسل الطلب الآن</h3>
                    <p>يمكنك شراء usdt عن طريق سيريتل كاش او شام كاش أو بنك بيمو أو حوالة الهرم</p>
               <a href="https://alimahmoud001.github.io/usdt//" class="open-link-button">                <i class="fab fa-telegram"></i> شراء/بيع
                    </a>
                </div>
            </div>
        </div>
                            
              
﻿
           
<!-- ---------------------> 

     <!-- القسم التعليمي -->
<!-- investment section --> 
        <div class="section" id="education">
            <h2 class="section-title">
                <i class="fas fa-mobile-alt"></i> دورات مجانية
            </h2>
            
            
            <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3>قناة الكورس الخاصة بي على تلجرام</h3>
                  <a href="https://t.me/tradewithali003/" class="btn" target="_blank">
                     <i class="fab fa-telegram"></i> شاهد الكورس
                    </a>
                </div>
            </div> <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3>  KAMEL M5(instagram)</h3>
                  <a href="https://www.instagram.com/kameel_m5/" class="btn" target="_blank">
                     <i class="fab fa-telegram"></i> شاهد الكورس
                    </a>
                </div>
            </div> <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3> Easy Trade</h3>
                  <a href="https://youtube.com/@easytradingeasy?si=9sITj4F_D__TAfb5/" class="btn" target="_blank">
                     <i class="fab fa-telegram"></i> شاهد الكورس
                    </a>
                </div>
            </div> <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3> TRADE WITH PATT</h3>
                  <a href="http://www.youtube.com/@tradewithpatarabic/" class="btn" target="_blank">
                     <i class="fab fa-telegram"></i> شاهد الكورس
                    </a>
                </div>
            </div> <div class="apps-grid">
                <div class="app-card">
                    <div class="app-icon">
                    </div>
                    <h3> SMART RISK</h3>
                  <a href="https://youtube.com/@smart_risk?si=s0leP3OYv9GuCp3r/" class="btn" target="_blank">
                     <i class="fab fa-telegram"></i> شاهد الكورس
                    </a>
                </div>
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


<!-- tlegram section -
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
                    <a href="https://t.me/+D_3xl17gg6M5OWRk" class="btn" target="_blank">
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
                    <h3> قناة التداول p2p</h3>
                    <p> لقد قمت بانشاء هذه المجموعة بين الاعضاء لمن يود بيع وشراء العملات المشفرة</p>
                    <a href="https://t.me/tradewithali004" class="btn" target="_blank">
                        <i class="fab fa-telegram"></i> انضم الآن
                    </a>
                </div>
            </div>
        </div>-> 

        
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
                    <li style="margin-bottom: 10px;">في إعدادات حساب التداول الخاص بك، قم بتمكين المصادقة الثنائية</li>
                    <li style="margin-bottom: 10px;">امسح رمز QR باستخدام التطبيق</li>
                    <li style="margin-bottom: 10px;">احفظ رمز الاسترداد في مكان آمن</li>
                    <li>استخدم الرمز الذي يظهر في التطبيق عند تسجيل الدخول</li>
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


