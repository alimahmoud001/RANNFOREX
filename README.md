<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>راني فوريكس - بوابة التداول الشاملة</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #1a3a6c;
            --secondary-color: #2a5a9c;
            --accent-color: #ff9800;
            --light-color: #f5f8ff;
            --dark-color: #0d1b2a;
            --success-color: #4caf50;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1b2a, #1a3a6c);
            color: #fff;
            min-height: 100vh;
            position: relative;
            padding-bottom: 50px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
            background: rgba(13, 27, 42, 0.9);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo i {
            font-size: 2rem;
            color: var(--accent-color);
        }
        
        .logo h1 {
            font-size: 1.5rem;
            background: linear-gradient(to right, var(--accent-color), #ffcc80);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .menu-toggle {
            background: var(--secondary-color);
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
            color: white;
            font-size: 1.5rem;
        }
        
        .menu-toggle:hover {
            background: var(--accent-color);
            transform: rotate(90deg);
        }
        
        /* Sidebar Styles */
        .sidebar {
            position: fixed;
            top: 0;
            right: -320px;
            width: 320px;
            height: 100%;
            background: var(--dark-color);
            box-shadow: -5px 0 15px rgba(0, 0, 0, 0.3);
            z-index: 200;
            transition: var(--transition);
            padding: 20px 0;
            overflow-y: auto;
        }
        
        .sidebar.active {
            right: 0;
        }
        
        .sidebar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .close-btn {
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .close-btn:hover {
            color: var(--accent-color);
            transform: scale(1.1);
        }
        
        .menu-items {
            list-style: none;
            padding: 20px 0;
        }
        
        .menu-item {
            padding: 12px 30px;
            cursor: pointer;
            transition: var(--transition);
            border-left: 3px solid transparent;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .menu-item:hover, .menu-item.active {
            background: rgba(42, 90, 156, 0.3);
            border-left: 3px solid var(--accent-color);
        }
        
        .menu-item i {
            width: 25px;
            text-align: center;
            color: var(--accent-color);
        }
        
        /* Main Content Styles */
        .content {
            padding: 20px;
            margin-top: 20px;
            background: rgba(13, 27, 42, 0.7);
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .section {
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .section.active {
            display: block;
        }
        
        .section-title {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--accent-color);
        }
        
        .section-title i {
            font-size: 1.8rem;
            color: var(--accent-color);
        }
        
        .section-title h2 {
            font-size: 1.8rem;
            font-weight: 600;
        }
        
        .card {
            background: rgba(26, 58, 108, 0.5);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .card-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 15px;
        }
        
        .card-header i {
            font-size: 1.5rem;
            color: var(--accent-color);
        }
        
        .card-header h3 {
            font-size: 1.3rem;
            font-weight: 600;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin: 15px 0;
        }
        
        .feature {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 8px 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
        }
        
        .feature i {
            color: var(--accent-color);
        }
        
        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(135deg, var(--accent-color), #ffab40);
            color: var(--dark-color);
            border: none;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: var(--transition);
            text-align: center;
            margin: 10px 5px;
            box-shadow: 0 4px 15px rgba(255, 152, 0, 0.3);
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 152, 0, 0.4);
        }
        
        .btn-secondary {
            background: linear-gradient(135deg, var(--secondary-color), #3a7bd5);
            box-shadow: 0 4px 15px rgba(42, 90, 156, 0.3);
        }
        
        .btn-secondary:hover {
            box-shadow: 0 8px 20px rgba(42, 90, 156, 0.4);
        }
        
        .link-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .link-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 15px;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .link-item:hover {
            background: rgba(42, 90, 156, 0.3);
            transform: translateX(5px);
        }
        
        .link-item h4 {
            margin-bottom: 10px;
            color: var(--accent-color);
        }
        
        .link-item a {
            color: #64b5f6;
            text-decoration: none;
            word-break: break-all;
        }
        
        .link-item a:hover {
            text-decoration: underline;
        }
        
        .step-list {
            counter-reset: step-counter;
            margin: 20px 0;
        }
        
        .step {
            position: relative;
            padding: 15px 15px 15px 60px;
            margin-bottom: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            border-left: 3px solid var(--accent-color);
        }
        
        .step:before {
            counter-increment: step-counter;
            content: counter(step-counter);
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            width: 35px;
            height: 35px;
            background: var(--accent-color);
            color: var(--dark-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.1rem;
        }
        
        .note {
            background: rgba(255, 152, 0, 0.15);
            border-left: 4px solid var(--accent-color);
            padding: 15px;
            margin: 15px 0;
            border-radius: 0 8px 8px 0;
        }
        
        .note i {
            color: var(--accent-color);
            margin-left: 5px;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 30px;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .sidebar {
                width: 280px;
                right: -280px;
            }
            
            .logo h1 {
                font-size: 1.2rem;
            }
            
            .section-title h2 {
                font-size: 1.5rem;
            }
            
            .btn {
                padding: 10px 20px;
                font-size: 0.9rem;
            }
        }
        
        @media (max-width: 480px) {
            .sidebar {
                width: 100%;
                right: -100%;
            }
            
            .features {
                grid-template-columns: 1fr;
            }
            
            .link-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="logo">
            <i class="fas fa-chart-line"></i>
            <h1>rannforex</h1>
        </div>
        <button class="menu-toggle" id="menuToggle">
            <i class="fas fa-bars"></i>
        </button>
    </header>
    
    <!-- Sidebar Navigation -->
    <nav class="sidebar" id="sidebar">
        <div class="sidebar-header">
            <h2>الأقسام الرئيسية</h2>
            <button class="close-btn" id="closeSidebar">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <ul class="menu-items">
            <li class="menu-item active" data-target="section1">
                <i class="fas fa-link"></i>
                <span>رابط الشركة</span>
            </li>
            <li class="menu-item" data-target="section2">
                <i class="fas fa-star"></i>
                <span>تقييمات الشركة</span>
            </li>
            <li class="menu-item" data-target="section3">
                <i class="fas fa-mobile-alt"></i>
                <span>تطبيقات التداول</span>
            </li>
            <li class="menu-item" data-target="section4">
                <i class="fas fa-lock"></i>
                <span>المصادقة الثنائية</span>
            </li>
            <li class="menu-item" data-target="section5">
                <i class="fab fa-telegram"></i>
                <span>قنوات التلجرام</span>
            </li>
            <li class="menu-item" data-target="section6">
                <i class="fas fa-graduation-cap"></i>
                <span>القسم التعليمي</span>
            </li>
            <li class="menu-item" data-target="section7">
                <i class="fas fa-chart-pie"></i>
                <span>قسم الاستثمار</span>
            </li>
            <li class="menu-item" data-target="section8">
                <i class="fas fa-money-bill-wave"></i>
                <span>طريقة الإيداع</span>
            </li>
        </ul>
    </nav>
    
    <!-- Main Content -->
    <div class="container">
        <div class="content">
            <!-- Section 1: Broker Link -->
            <section id="section1" class="section active">
                <div class="section-title">
                    <i class="fas fa-link"></i>
                    <h2>رابط شركة الوساطة المالية</h2>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-external-link-alt"></i>
                        <h3>رابط التسجيل في راني فوريكس</h3>
                    </div>
                    <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="btn" target="_blank">
                        <i class="fas fa-user-plus"></i> سجل الآن
                    </a>
                    
                    <div class="note">
                        <i class="fas fa-info-circle"></i>
                        <strong>ملاحظة:</strong> ★ اقل ايداع 10$ خلال 30 ثانية ★ أقل سحب 10$ خلال 30 ثانية ★ عمولة قليلة جدا
                    </div>
                    
                    <div class="features">
                        <div class="feature">
                            <i class="fas fa-chart-line"></i>
                            <span>اسبريد 0.3~1.2</span>
                        </div>
                        <div class="feature">
                            <i class="fas fa-balance-scale"></i>
                            <span>رافعة مالية 1:500</span>
                        </div>
                        <div class="feature">
                            <i class="fas fa-shield-alt"></i>
                            <span>تداول آمن</span>
                        </div>
                        <div class="feature">
                            <i class="fas fa-wallet"></i>
                            <span>أربع أنواع من الحسابات</span>
                        </div>
                        <div class="feature">
                            <i class="fas fa-tachometer-alt"></i>
                            <span>انزلاق منخفض</span>
                        </div>
                        <div class="feature">
                            <i class="fas fa-bolt"></i>
                            <span>تنفيذ فوري للصفقات</span>
                        </div>
                        <div class="feature">
                            <i class="fas fa-star"></i>
                            <span>تقييم ممتاز على مواقع التقييم</span>
                        </div>
                        <div class="feature">
                            <i class="fas fa-lock"></i>
                            <span>الأمان عالي جداً بسبب 2FA</span>
                        </div>
                    </div>
                    
                    <div class="note">
                        <i class="fas fa-lightbulb"></i>
                        <strong>معلومات إضافية:</strong> ★ توثيق من سورية أو أي دولة أخرى ★ نموذج A-Book من أفضل مزودي السيولة
                    </div>
                    
                    <div class="card-header" style="margin-top: 20px;">
                        <i class="fas fa-table"></i>
                        <h3>الإسبريد المتوسط اليومي</h3>
                    </div>
                    <a href="https://rannforex.com/en/trading/quotesonline/" class="btn btn-secondary" target="_blank">
                        <i class="fas fa-external-link-alt"></i> عرض الإسبريد
                    </a>
                </div>
            </section>
            
            <!-- Section 2: Company Reviews -->
            <section id="section2" class="section">
                <div class="section-title">
                    <i class="fas fa-star"></i>
                    <h2>تقييمات الشركة</h2>
                </div>
                
                <div class="link-grid">
                    <div class="link-item">
                        <h4><i class="fas fa-star-half-alt"></i> Trust Pilot</h4>
                        <a href="https://fr.trustpilot.com/review/rannforex.com" target="_blank">https://fr.trustpilot.com/review/rannforex.com</a>
                    </div>
                    
                    <div class="link-item">
                        <h4><i class="fas fa-globe"></i> WikiFX</h4>
                        <a href="https://www.wikifx.com/en/dealer/1141850612.html" target="_blank">https://www.wikifx.com/en/dealer/1141850612.html</a>
                    </div>
                    
                    <div class="link-item">
                        <h4><i class="fas fa-book"></i> MyFXBook</h4>
                        <a href="https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1" target="_blank">https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1</a>
                    </div>
                    
                    <div class="link-item">
                        <h4><i class="fas fa-shield-alt"></i> Forex Peace Army</h4>
                        <a href="https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review" target="_blank">https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review</a>
                    </div>
                </div>
            </section>
            
            <!-- Section 3: Trading Apps -->
            <section id="section3" class="section">
                <div class="section-title">
                    <i class="fas fa-mobile-alt"></i>
                    <h2>تطبيقات التداول</h2>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-chart-bar"></i>
                        <h3>منصة ميتا تريدر 5</h3>
                    </div>
                    <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" class="btn" target="_blank">
                        <i class="fab fa-android"></i> تحميل للتداول
                    </a>
                    <div class="note">
                        <i class="fas fa-info-circle"></i>
                        <strong>ملاحظة:</strong> هي المنصة الموثوقة الأفضل في مجال التداول في جميع الأسواق
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-wallet"></i>
                        <h3>المحفظة الإلكترونية</h3>
                    </div>
                    <a href="https://cwallet.com/referral/DvY6dZtS" class="btn btn-secondary" target="_blank">
                        <i class="fas fa-download"></i> تحميل المحفظة
                    </a>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-lock"></i>
                        <h3>تطبيق المصادقة الثنائية</h3>
                    </div>
                    <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" class="btn" target="_blank">
                        <i class="fab fa-google-play"></i> تحميل التطبيق
                    </a>
                    <div class="note">
                        <i class="fas fa-info-circle"></i>
                        <strong>ملاحظة:</strong> يلزم من أجل توثيق الحساب وتوثيق عمليات السحب والإيداع
                    </div>
                </div>
            </section>
            
            <!-- Section 4: Authentication -->
            <section id="section4" class="section">
                <div class="section-title">
                    <i class="fas fa-lock"></i>
                    <h2>المصادقة الثنائية</h2>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-video"></i>
                        <h3>فيديو تعليمي</h3>
                    </div>
                    <p>فيديو بسيط حول كيفية استخدام تطبيق Google Authenticator</p>
                    <a href="https://youtube.com/shorts/SlQc3Q6L3HQ?si=Q5sdG7_lxANoykBs" class="btn" target="_blank">
                        <i class="fab fa-youtube"></i> مشاهدة الفيديو
                    </a>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-key"></i>
                        <h3>نصائح هامة للمصادقة الثنائية</h3>
                    </div>
                    <ul style="padding: 15px 30px; line-height: 2;">
                        <li>احفظ رمز الاسترداد في مكان آمن</li>
                        <li>لا تشارك رمز المصادقة مع أي شخص</li>
                        <li>تأكد من ضبط الوقت الصحيح على جهازك</li>
                        <li>استخدم تطبيق المصادقة على جهازك الشخصي فقط</li>
                    </ul>
                </div>
            </section>
            
            <!-- Section 5: Telegram Channels -->
            <section id="section5" class="section">
                <div class="section-title">
                    <i class="fab fa-telegram"></i>
                    <h2>قنوات التلجرام</h2>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-bullhorn"></i>
                        <h3>قناتنا الرئيسية</h3>
                    </div>
                    <a href="https://t.me/tradewithalimahmoud" class="btn" target="_blank">
                        <i class="fab fa-telegram"></i> انضم إلى قناتنا
                    </a>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-signal"></i>
                        <h3>قنوات الإشارات (للتعلم فقط)</h3>
                    </div>
                    <div class="link-grid">
                        <div class="link-item">
                            <h4>FX IRI</h4>
                            <a href="https://t.me/FX_IRI" target="_blank">https://t.me/FX_IRI</a>
                        </div>
                        <div class="link-item">
                            <h4>Pro Signals FX</h4>
                            <a href="https://t.me/prosignalsfxx" target="_blank">https://t.me/prosignalsfxx</a>
                        </div>
                        <div class="link-item">
                            <h4>Top Trading Signals</h4>
                            <a href="https://t.me/top_tradingsignals" target="_blank">https://t.me/top_tradingsignals</a>
                        </div>
                        <div class="link-item">
                            <h4>Signals FC</h4>
                            <a href="https://t.me/signalsfc" target="_blank">https://t.me/signalsfc</a>
                        </div>
                        <div class="link-item">
                            <h4>Elite Trading Signals</h4>
                            <a href="https://t.me/elitetrading_signals" target="_blank">https://t.me/elitetrading_signals</a>
                        </div>
                        <div class="link-item">
                            <h4>Free Signals</h4>
                            <a href="https://t.me/free_signals" target="_blank">https://t.me/free_signals</a>
                        </div>
                        <div class="link-item">
                            <h4>Grey Suit Community</h4>
                            <a href="https://t.me/greysuitcommunity" target="_blank">https://t.me/greysuitcommunity</a>
                        </div>
                    </div>
                    <div class="note">
                        <i class="fas fa-exclamation-triangle"></i>
                        <strong>تنويه:</strong> هذه القنوات للتعلم وليس لنسخ الإشارات
                    </div>
                </div>
            </section>
            
            <!-- Section 6: Educational Content -->
            <section id="section6" class="section">
                <div class="section-title">
                    <i class="fas fa-graduation-cap"></i>
                    <h2>القسم التعليمي</h2>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-play-circle"></i>
                        <h3>كورس كامل مع باتك</h3>
                    </div>
                    <p>تعلم التداول مع أشهر ملياردير عبقري التداول باتك</p>
                    <a href="https://youtube.com/@tradewithpatarabic?si=4egOIQw15KHmRJGy" class="btn" target="_blank">
                        <i class="fab fa-youtube"></i> مشاهدة الكورس
                    </a>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-chalkboard-teacher"></i>
                        <h3>قناة Smart Risk على يوتيوب</h3>
                    </div>
                    <a href="https://youtube.com/@smart_risk?si=s0leP3OYv9GuCp3r" class="btn btn-secondary" target="_blank">
                        <i class="fab fa-youtube"></i> زيارة القناة
                    </a>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fab fa-instagram"></i>
                        <h3>كورس على انستغرام</h3>
                    </div>
                    <a href="https://www.instagram.com/kameel_m5?igsh=YzljYTk1ODg3Zg==" class="btn" target="_blank">
                        <i class="fab fa-instagram"></i> زيارة الكورس
                    </a>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-book"></i>
                        <h3>كورس Smart Risk على يوتيوب</h3>
                    </div>
                    <a href="https://youtube.com/@smart_risk?si=8VLFIUyBN-9rm7L6" class="btn btn-secondary" target="_blank">
                        <i class="fab fa-youtube"></i> مشاهدة الكورس
                    </a>
                </div>
            </section>
            
            <!-- Section 7: Investment -->
            <section id="section7" class="section">
                <div class="section-title">
                    <i class="fas fa-chart-pie"></i>
                    <h2>قسم الاستثمار</h2>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-user-tie"></i>
                        <h3>حسابي الاستثماري</h3>
                    </div>
                    <p>للاطلاع على تفاصيل حسابي الاستثماري في شركة راني فوريكس</p>
                    <div style="background: rgba(255,255,255,0.1); padding: 20px; border-radius: 10px; margin: 20px 0; text-align: center;">
                        <p>سأقوم بإدراج رابط وصورة لاحقاً</p>
                        <p style="margin-top: 10px; color: var(--accent-color);">
                            <i class="fas fa-exclamation-circle"></i> سيتم تحديث هذا القسم قريباً
                        </p>
                    </div>
                </div>
            </section>
            
            <!-- Section 8: Deposit Method -->
            <section id="section8" class="section">
                <div class="section-title">
                    <i class="fas fa-money-bill-wave"></i>
                    <h2>طريقة الإيداع</h2>
                </div>
                
                <div class="card">
                    <div class="card-header">
                        <i class="fas fa-wallet"></i>
                        <h3>خطوات الإيداع</h3>
                    </div>
                    
                    <div class="step-list">
                        <div class="step">
                            <p>نضغط على الثلاث خطوط في موقع RannForex أعلى يمين الشاشة</p>
                            <p>1️⃣ Deposit</p>
                            <p>Select deposit method: crypto</p>
                            <p>Select trading account: اختر حساب التداول</p>
                            <p>Continue</p>
                        </div>
                        
                        <div class="step">
                            <p>2️⃣ Transfer details</p>
                            <p>أدخل المبلغ في الفراغ الأول</p>
                            <p>اختر USD</p>
                            <p>Continue</p>
                        </div>
                        
                        <div class="step">
                            <p>3️⃣ 2FA Code</p>
                            <p>نذهب إلى تطبيق Google Authenticator</p>
                            <p>نقوم بأخذ الكود الذي ولده من أجل حساب RannForex وإدخاله في الفراغ الموجود</p>
                            <p>Continue</p>
                        </div>
                        
                        <div class="step">
                            <p>4️⃣ TetherUS - USDT</p>
                            <p>BUSD-T-USDT</p>
                            <p>نسخ العنوان</p>
                        </div>
                        
                        <div class="step">
                            <p>5️⃣ CWallet Send</p>
                            <p>USDT</p>
                            <p>BEP20</p>
                            <p>Amount: ... $</p>
                            <p>لصق العنوان (من RannForex)</p>
                            <p>Send</p>
                        </div>
                    </div>
                    
                    <div class="note">
                        <i class="fas fa-check-circle"></i>
                        <strong>انتهى الإيداع بنجاح!</strong>
                    </div>
                </div>
            </section>
        </div>
    </div>
    
    <footer>
        <p>© 2025 راني فوريكس - جميع الحقوق محفوظة | تم التصميم بعناية لخدمة المتداولين</p>
    </footer>
    
    <script>
        // Menu Toggle Functionality
        const menuToggle = document.getElementById('menuToggle');
        const sidebar = document.getElementById('sidebar');
        const closeSidebar = document.getElementById('closeSidebar');
        const menuItems = document.querySelectorAll('.menu-item');
        const sections = document.querySelectorAll('.section');
        
        // Toggle sidebar
        menuToggle.addEventListener('click', () => {
            sidebar.classList.add('active');
        });
        
        closeSidebar.addEventListener('click', () => {
            sidebar.classList.remove('active');
        });
        
        // Menu items click functionality
        menuItems.forEach(item => {
            item.addEventListener('click', () => {
                // Remove active class from all items
                menuItems.forEach(i => i.classList.remove('active'));
                // Add active class to clicked item
                item.classList.add('active');
                
                // Get target section id
                const target = item.getAttribute('data-target');
                
                // Hide all sections
                sections.forEach(section => {
                    section.classList.remove('active');
                });
                
                // Show target section
                document.getElementById(target).classList.add('active');
                
                // Close sidebar on mobile
                if (window.innerWidth <= 768) {
                    sidebar.classList.remove('active');
                }
            });
        });
        
        // Close sidebar when clicking outside
        document.addEventListener('click', (e) => {
            if (!sidebar.contains(e.target) && !menuToggle.contains(e.target)) {
                sidebar.classList.remove('active');
            }
        });
        
        // Prevent closing when clicking inside sidebar
        sidebar.addEventListener('click', (e) => {
            e.stopPropagation();
        });
    </script>
</body>
</html>
