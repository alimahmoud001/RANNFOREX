<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل المتداول - دليلك الشامل للتداول</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --success-color: #27ae60;
            --warning-color: #f39c12;
            --text-color: #333;
            --bg-color: #f9f9f9;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', Arial, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            display: flex;
            min-height: 100vh;
        }

        /* Sidebar Styles */
        .sidebar {
            width: 280px;
            background-color: var(--primary-color);
            color: white;
            position: fixed;
            height: 100vh;
            overflow-y: auto;
            transition: all 0.3s;
            z-index: 1000;
            transform: translateX(-100%);
        }

        .sidebar.active {
            transform: translateX(0);
        }

        .sidebar-header {
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.2);
            text-align: center;
        }

        .sidebar-header h2 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        .sidebar-menu {
            padding: 0;
            list-style: none;
        }

        .sidebar-menu li {
            position: relative;
        }

        .sidebar-menu li a {
            display: block;
            padding: 15px 20px;
            color: white;
            text-decoration: none;
            font-size: 1.1rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s;
        }

        .sidebar-menu li a:hover {
            background-color: rgba(255, 255, 255, 0.1);
            padding-right: 25px;
        }

        .sidebar-menu li a i {
            margin-left: 10px;
        }

        .submenu {
            display: none;
            background-color: rgba(0, 0, 0, 0.2);
            padding: 0;
            list-style: none;
        }

        .submenu.active {
            display: block;
        }

        .submenu li a {
            padding: 12px 20px 12px 40px;
            font-size: 1rem;
        }

        /* Main Content Styles */
        .main-content {
            flex: 1;
            padding: 20px;
            margin-right: 0;
            transition: all 0.3s;
        }

        .main-content.active {
            margin-right: 280px;
        }

        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--secondary-color);
        }

        .header h1 {
            color: var(--primary-color);
            font-size: 2rem;
            font-weight: 700;
        }

        .menu-toggle {
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--primary-color);
        }

        .section {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 30px;
            display: none;
        }

        .section.active {
            display: block;
            animation: fadeIn 0.5s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section h2 {
            color: var(--secondary-color);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #eee;
            font-size: 1.8rem;
        }

        .section h3 {
            color: var(--primary-color);
            margin: 20px 0 15px;
            font-size: 1.4rem;
        }

        .link-box {
            background-color: var(--light-color);
            border-left: 4px solid var(--secondary-color);
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 4px;
        }

        .link-box a {
            color: var(--secondary-color);
            font-weight: bold;
            text-decoration: none;
            display: block;
            margin-bottom: 10px;
            word-break: break-all;
        }

        .link-box a:hover {
            text-decoration: underline;
        }

        .link-box p {
            margin-bottom: 5px;
        }

        .feature-list {
            list-style-type: none;
        }

        .feature-list li {
            padding: 8px 0;
            position: relative;
            padding-right: 25px;
        }

        .feature-list li:before {
            content: "★";
            color: var(--warning-color);
            position: absolute;
            right: 0;
        }

        /* Calculator Styles */
        .calculator-form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: var(--dark-color);
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }

        .form-group input:focus, .form-group select:focus {
            border-color: var(--secondary-color);
            outline: none;
        }

        .calculator-results {
            margin-top: 30px;
        }

        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .result-box {
            background-color: var(--light-color);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
        }

        .result-box h4 {
            color: var(--primary-color);
            margin-bottom: 10px;
        }

        .result-box p {
            font-size: 1.2rem;
            font-weight: bold;
            color: var(--secondary-color);
        }

        .capital-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        .capital-table th, .capital-table td {
            padding: 12px;
            text-align: center;
            border: 1px solid #ddd;
        }

        .capital-table th {
            background-color: var(--primary-color);
            color: white;
        }

        .capital-table tr:nth-child(even) {
            background-color: #f2f2f2;
        }

        .chart-container {
            position: relative;
            height: 400px;
            margin-top: 40px;
        }

        /* USDT Exchange Styles */
        .usdt-form {
            max-width: 800px;
            margin: 0 auto;
        }

        .form-step {
            display: none;
        }

        .form-step.active {
            display: block;
        }

        .form-row {
            display: flex;
            flex-wrap: wrap;
            margin: 0 -10px;
        }

        .form-col {
            flex: 1;
            min-width: 250px;
            padding: 0 10px;
        }

        .btn {
            display: inline-block;
            padding: 12px 25px;
            background-color: var(--secondary-color);
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            text-align: center;
            transition: all 0.3s;
            margin-top: 10px;
        }

        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }

        .btn-block {
            display: block;
            width: 100%;
        }

        .btn-next {
            background-color: var(--success-color);
        }

        .btn-back {
            background-color: var(--warning-color);
        }

        .btn-submit {
            background-color: var(--accent-color);
        }

        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .payment-method {
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s;
            text-align: center;
        }

        .payment-method:hover {
            border-color: var(--secondary-color);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .payment-method.active {
            border-color: var(--success-color);
            background-color: rgba(39, 174, 96, 0.1);
        }

        .payment-method i {
            font-size: 2rem;
            margin-bottom: 10px;
            color: var(--secondary-color);
        }

        .copy-btn {
            background-color: var(--light-color);
            border: none;
            padding: 5px 10px;
            border-radius: 4px;
            cursor: pointer;
            margin-right: 10px;
            transition: all 0.3s;
        }

        .copy-btn:hover {
            background-color: #ddd;
        }

        .order-summary {
            background-color: var(--light-color);
            padding: 20px;
            border-radius: 8px;
            margin-top: 30px;
        }

        .order-summary h3 {
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .order-details {
            margin-bottom: 20px;
        }

        .order-details p {
            margin-bottom: 8px;
        }

        .order-details strong {
            color: var(--dark-color);
        }

        /* Footer & Social */
        .footer {
            text-align: center;
            padding: 20px;
            background-color: var(--primary-color);
            color: white;
            margin-top: 50px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .social-link {
            display: inline-block;
            width: 50px;
            height: 50px;
            background-color: white;
            color: var(--primary-color);
            border-radius: 50%;
            text-align: center;
            line-height: 50px;
            font-size: 1.5rem;
            transition: all 0.3s;
        }

        .social-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .social-link.email {
            background-color: var(--accent-color);
            color: white;
        }

        .social-link.telegram {
            background-color: #0088cc;
            color: white;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .calculator-form {
                grid-template-columns: 1fr;
            }
            
            .main-content.active {
                margin-right: 0;
            }
            
            .sidebar {
                width: 250px;
            }
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 1.5rem;
            }
            
            .section {
                padding: 20px 15px;
            }
            
            .form-row {
                flex-direction: column;
            }
            
            .form-col {
                padding: 0;
                margin-bottom: 15px;
            }
        }

        @media (max-width: 576px) {
            .results-grid {
                grid-template-columns: 1fr;
            }
            
            .payment-methods {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Sidebar -->
        <div class="sidebar" id="sidebar">
            <div class="sidebar-header">
                <h2>دليل المتداول</h2>
                <p>القائمة الرئيسية</p>
            </div>
            <ul class="sidebar-menu">
                <li><a href="#" data-section="broker-section"><i class="fas fa-building"></i>شركة الوساطة</a></li>
                <li>
                    <a href="#" class="has-submenu"><i class="fas fa-mobile-alt"></i>تطبيقات التداول <i class="fas fa-chevron-down"></i></a>
                    <ul class="submenu">
                        <li><a href="#" data-section="apps-section">جميع التطبيقات</a></li>
                        <li><a href="#" data-section="mt5-section">ميتا تريدر 5</a></li>
                        <li><a href="#" data-section="binance-section">محفظة باينانس</a></li>
                        <li><a href="#" data-section="auth-section">المصادقة الثنائية</a></li>
                        <li><a href="#" data-section="tradingview-section">تطبيق التحليل</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#" class="has-submenu"><i class="fab fa-telegram"></i>قنوات التلجرام <i class="fas fa-chevron-down"></i></a>
                    <ul class="submenu">
                        <li><a href="#" data-section="telegram-section">جميع القنوات</a></li>
                        <li><a href="#" data-section="signals-section">قناة الإشارات</a></li>
                        <li><a href="#" data-section="course-section">قناة الكورس</a></li>
                        <li><a href="#" data-section="community-section">المجتمع</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#" class="has-submenu"><i class="fas fa-graduation-cap"></i>التعليم <i class="fas fa-chevron-down"></i></a>
                    <ul class="submenu">
                        <li><a href="#" data-section="education-section">جميع المصادر</a></li>
                        <li><a href="#" data-section="patar-course">كورس باتك</a></li>
                        <li><a href="#" data-section="smart-risk">سمارت ريسك</a></li>
                        <li><a href="#" data-section="instagram-course">كورس انستغرام</a></li>
                    </ul>
                </li>
                <li><a href="#" data-section="calculator-section"><i class="fas fa-calculator"></i>حاسبة رأس المال</a></li>
                <li><a href="#" data-section="usdt-section"><i class="fas fa-exchange-alt"></i>شراء وبيع USDT</a></li>
            </ul>
        </div>

        <!-- Main Content -->
        <div class="main-content" id="main-content">
            <div class="header">
                <h1>دليل المتداول - دليلك الشامل للتداول</h1>
                <div class="menu-toggle" id="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
            </div>

            <!-- Broker Section -->
            <div class="section active" id="broker-section">
                <h2>شركة الوساطة المالية</h2>
                <div class="link-box">
                    <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" target="_blank">رابط التسجيل في شركة الوساطة</a>
                    <h3>ميزات الشركة:</h3>
                    <ul class="feature-list">
                        <li>اقل ايداع او سحب 10$ خلال 30 ثانية</li>
                        <li>اسبريد 0.2~1.2 ورافعة مالية 500:1</li>
                        <li>تداول أمن على جميع ازواج الفوريكس والمعادن والنفط والمؤشرات والعملات المشفرة</li>
                        <li>حسابات إسلامية خالية من العمولة</li>
                        <li>حسابات احترافي اسبريد قليل جدا</li>
                        <li>انزلاق منخفض وتنفيذ فوري للصفقات</li>
                        <li>تقييم ممتاز على موقع trust pilot & myfxbook & wikifx & Forex peace army يمكنك الاطلاع بنفسك</li>
                        <li>الأمان عالي جدا بسبب 2FA</li>
                        <li>توثيق سريع وسهل</li>
                        <li>نموذج A Book من افضل مزودي السيولة</li>
                    </ul>
                </div>
                <div class="link-box">
                    <a href="https://rannforex.com/en/trading/quotesonline/" target="_blank">رابط الاطلاع على الاسبريد المتوسط اليومي</a>
                    <p>هذا الرابط يوضح متوسط الأسبريد اليومي لجميع الأزواج والعملات</p>
                </div>
            </div>

            <!-- Apps Section -->
            <div class="section" id="apps-section">
                <h2>تطبيقات يجب تحميلها للبدء بالتداول</h2>
                
                <div class="link-box" id="mt5-section">
                    <h3>منصة ميتا تريدر 5</h3>
                    <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" target="_blank">رابط تحميل ميتا تريدر 5</a>
                    <p>ملاحظة: هي المنصة الموثوقة الافضل في مجال التداول في جميع الاسواق</p>
                </div>
                
                <div class="link-box" id="binance-section">
                    <h3>المحفظة الاكترونية باينانس</h3>
                    <a href="https://www.binance.com/activity/referral-entry/CPA?ref=CPA_004C6HBMJS" target="_blank">رابط تحميل باينانس</a>
                </div>
                
                <div class="link-box" id="auth-section">
                    <h3>تطبيق المصادقة الثنائية</h3>
                    <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" target="_blank">رابط تحميل Google Authenticator</a>
                </div>
                
                <div class="link-box" id="tradingview-section">
                    <h3>تطبيق التحليل TradingView</h3>
                    <a href="https://play.google.com/store/apps/details?id=com.tradingview.tradingviewapp" target="_blank">رابط تحميل TradingView</a>
                </div>
            </div>

            <!-- Telegram Section -->
            <div class="section" id="telegram-section">
                <h2>قنوات التلجرام</h2>
                <p>باشتراك شهري 30 دولار يمكنك الدخول الى القنوات الخاصة بي التالية</p>
                
                <div class="link-box" id="signals-section">
                    <h3>قناة الإشارات</h3>
                    <a href="https://t.me/tradewithali002" target="_blank">https://t.me/tradewithali002</a>
                </div>
                
                <div class="link-box" id="course-section">
                    <h3>قناة الكورس</h3>
                    <a href="https://t.me/tradewithali003" target="_blank">https://t.me/tradewithali003</a>
                </div>
                
                <div class="link-box">
                    <h3>قناتي العامة (إشارات مجانية بدون اشتراك)</h3>
                    <a href="https://t.me/Tradewithali001" target="_blank">https://t.me/Tradewithali001</a>
                </div>
                
                <div class="link-box" id="community-section">
                    <h3>مجتمعنا</h3>
                    <a href="https://t.me/SyriaTradingFXg" target="_blank">https://t.me/SyriaTradingFXg</a>
                </div>
            </div>

            <!-- Education Section -->
            <div class="section" id="education-section">
                <h2>القسم التعليمي</h2>
                
                <div class="link-box" id="patar-course">
                    <h3>كورس كامل لتعلم التداول مع باتك</h3>
                    <a href="https://youtube.com/@tradewithpatarabic?si=4egOIQw15KHmRJGy" target="_blank">https://youtube.com/@tradewithpatarabic</a>
                </div>
                
                <div class="link-box" id="smart-risk">
                    <h3>قناة أخرى على يوتيوب</h3>
                    <a href="https://youtube.com/@smart_risk?si=s0leP3OYv9GuCp3r" target="_blank">https://youtube.com/@smart_risk</a>
                </div>
                
                <div class="link-box" id="instagram-course">
                    <h3>كورس على انستغرام</h3>
                    <a href="https://www.instagram.com/kameel_m5?igsh=YzljYTk1ODg3Zg==" target="_blank">https://www.instagram.com/kameel_m5</a>
                </div>
                
                <div class="link-box">
                    <h3>كورس على يوتيوب - Smart risk</h3>
                    <a href="https://youtube.com/@smart_risk?si=8VLFIUyBN-9rm7L6" target="_blank">https://youtube.com/@smart_risk</a>
                </div>
            </div>

            <!-- Calculator Section -->
            <div class="section" id="calculator-section">
                <h2>حاسبة تطور رأس المال</h2>
                
                <form id="capital-calculator" class="calculator-form">
                    <div class="form-group">
                        <label for="initial-capital">رأس المال الأولي ($)</label>
                        <input type="number" id="initial-capital" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="win-rate">نسبة الصفقات الرابحة (%)</label>
                        <input type="number" id="win-rate" min="0" max="100" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="profit-per-trade">معدل الربح لكل صفقة (%)</label>
                        <input type="number" id="profit-per-trade" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="loss-per-trade">معدل الخسارة لكل صفقة (%)</label>
                        <input type="number" id="loss-per-trade" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="trades-interval">عدد الصفقات في كل تحديث</label>
                        <input type="number" id="trades-interval" value="10" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="target-capital">الهدف النهائي ($)</label>
                        <input type="number" id="target-capital" required>
                    </div>
                    
                    <button type="submit" class="btn btn-block">حساب النتائج</button>
                </form>
                
                <div class="calculator-results" id="calculator-results" style="display: none;">
                    <h3>النتائج</h3>
                    
                    <div class="results-grid">
                        <div class="result-box">
                            <h4>متوسط العائد لكل صفقة</h4>
                            <p id="avg-return">0%</p>
                        </div>
                        
                        <div class="result-box">
                            <h4>عدد الصفقات المطلوبة</h4>
                            <p id="required-trades">0</p>
                        </div>
                        
                        <div class="result-box">
                            <h4>معدل النمو الإجمالي</h4>
                            <p id="total-growth">0%</p>
                        </div>
                    </div>
                    
                    <h3>تطور رأس المال</h3>
                    <div class="chart-container">
                        <canvas id="capital-chart"></canvas>
                    </div>
                    
                    <h3>جدول تطور رأس المال</h3>
                    <div class="table-responsive">
                        <table class="capital-table">
                            <thead>
                                <tr>
                                    <th>عدد الصفقات</th>
                                    <th>رأس المال ($)</th>
                                    <th>معدل النمو</th>
                                </tr>
                            </thead>
                            <tbody id="capital-table-body">
                                <!-- Will be filled by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>

            <!-- USDT Exchange Section -->
            <div class="section" id="usdt-section">
                <h2>شراء وبيع USDT</h2>
                
                <form id="usdt-form" class="usdt-form">
                    <!-- Step 1: Personal Info -->
                    <div class="form-step active" id="step1">
                        <h3>المعلومات الشخصية</h3>
                        
                        <div class="form-row">
                            <div class="form-col">
                                <div class="form-group">
                                    <label for="full-name">الاسم الثلاثي</label>
                                    <input type="text" id="full-name" required>
                                </div>
                            </div>
                            
                            <div class="form-col">
                                <div class="form-group">
                                    <label for="phone">رقم الهاتف</label>
                                    <input type="tel" id="phone" required>
                                </div>
                            </div>
                        </div>
                        
                        <div class="form-group">
                            <label for="city">المدينة</label>
                            <input type="text" id="city" required>
                        </div>
                        
                        <button type="button" class="btn btn-next" onclick="nextStep(1)">التالي</button>
                    </div>
                    
                    <!-- Step 2: Transaction Type -->
                    <div class="form-step" id="step2">
                        <h3>نوع العملية</h3>
                        
                        <div class="form-group">
                            <label>ماذا تريد أن تفعل؟</label>
                            <div class="payment-methods">
                                <div class="payment-method" onclick="selectTransactionType('buy')">
                                    <i class="fas fa-shopping-cart"></i>
                                    <h4>شراء USDT</h4>
                                    <p>شراء عملة USDT</p>
                                </div>
                                
                                <div class="payment-method" onclick="selectTransactionType('sell')">
                                    <i class="fas fa-money-bill-wave"></i>
                                    <h4>بيع USDT</h4>
                                    <p>بيع عملة USDT</p>
                                </div>
                            </div>
                            <input type="hidden" id="transaction-type">
                        </div>
                        
                        <div class="form-row">
                            <button type="button" class="btn btn-back" onclick="prevStep(2)">السابق</button>
                            <button type="button" class="btn btn-next" onclick="nextStep(2)" disabled id="step2-next">التالي</button>
                        </div>
                    </div>
                    
                    <!-- Step 3: Buy Details -->
                    <div class="form-step" id="step3-buy">
                        <h3>تفاصيل الشراء</h3>
                        
                        <div class="form-group">
                            <label for="buy-amount">الكمية المطلوبة (USDT)</label>
                            <input type="number" id="buy-amount" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="buy-network">اختر الشبكة</label>
                            <select id="buy-network" required>
                                <option value="">-- اختر الشبكة --</option>
                                <option value="bep20">BEP20</option>
                                <option value="trc20">TRC20</option>
                                <option value="erc20">ERC20</option>
                                <option value="binance-pay">Binance Pay</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="buy-address">عنوان المحفظة (سيتم إرسال USDT إليه)</label>
                            <input type="text" id="buy-address" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="buy-notes">ملاحظات (اختياري)</label>
                            <textarea id="buy-notes" rows="3"></textarea>
                        </div>
                        
                        <div class="form-row">
                            <button type="button" class="btn btn-back" onclick="prevStep(3)">السابق</button>
                            <button type="button" class="btn btn-next" onclick="nextStep(3)">التالي</button>
                        </div>
                    </div>
                    
                    <!-- Step 3: Sell Details -->
                    <div class="form-step" id="step3-sell">
                        <h3>تفاصيل البيع</h3>
                        
                        <div class="form-group">
                            <label for="sell-amount">الكمية المراد بيعها (USDT)</label>
                            <input type="number" id="sell-amount" required>
                        </div>
                        
                        <div class="form-group">
                            <label>طريقة الاستلام</label>
                            <div class="payment-methods">
                                <div class="payment-method" onclick="selectPaymentMethod('syriatel')">
                                    <i class="fas fa-mobile-alt"></i>
                                    <h4>سيريتل كاش</h4>
                                </div>
                                
                                <div class="payment-method" onclick="selectPaymentMethod('haram')">
                                    <i class="fas fa-university"></i>
                                    <h4>حوالة هرم</h4>
                                </div>
                                
                                <div class="payment-method" onclick="selectPaymentMethod('bemo')">
                                    <i class="fas fa-credit-card"></i>
                                    <h4>بنك بيمو</h4>
                                </div>
                                
                                <div class="payment-method" onclick="selectPaymentMethod('sham')">
                                    <i class="fas fa-wallet"></i>
                                    <h4>شام كاش</h4>
                                </div>
                            </div>
                            <input type="hidden" id="payment-method">
                        </div>
                        
                        <div class="form-group" id="payment-details-container" style="display: none;">
                            <label id="payment-details-label">تفاصيل الحساب</label>
                            <input type="text" id="payment-details" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="sell-network">شبكة USDT المراد بيعها</label>
                            <select id="sell-network" required>
                                <option value="">-- اختر الشبكة --</option>
                                <option value="bep20">BEP20</option>
                                <option value="trc20">TRC20</option>
                                <option value="erc20">ERC20</option>
                                <option value="binance-pay">Binance Pay</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="sell-notes">ملاحظات (اختياري)</label>
                            <textarea id="sell-notes" rows="3"></textarea>
                        </div>
                        
                        <div class="form-row">
                            <button type="button" class="btn btn-back" onclick="prevStep(3)">السابق</button>
                            <button type="button" class="btn btn-next" onclick="nextStep(3)">التالي</button>
                        </div>
                    </div>
                    
                    <!-- Step 4: Payment Info -->
                    <div class="form-step" id="step4-buy">
                        <h3>تفاصيل الدفع</h3>
                        
                        <div class="form-group">
                            <label>طريقة الدفع</label>
                            <div class="payment-methods">
                                <div class="payment-method" onclick="selectBuyPaymentMethod('syriatel')">
                                    <i class="fas fa-mobile-alt"></i>
                                    <h4>سيريتل كاش</h4>
                                </div>
                                
                                <div class="payment-method" onclick="selectBuyPaymentMethod('haram')">
                                    <i class="fas fa-university"></i>
                                    <h4>حوالة هرم</h4>
                                </div>
                                
                                <div class="payment-method" onclick="selectBuyPaymentMethod('bemo')">
                                    <i class="fas fa-credit-card"></i>
                                    <h4>بنك بيمو</h4>
                                </div>
                                
                                <div class="payment-method" onclick="selectBuyPaymentMethod('sham')">
                                    <i class="fas fa-wallet"></i>
                                    <h4>شام كاش</h4>
                                </div>
                            </div>
                            <input type="hidden" id="buy-payment-method">
                        </div>
                        
                        <div id="buy-payment-details" style="display: none;">
                            <h4>تفاصيل الدفع:</h4>
                            <div id="syriatel-details" class="payment-details" style="display: none;">
                                <p>عنواني: <span>0934598967</span> <button class="copy-btn" onclick="copyToClipboard('0934598967')">نسخ</button></p>
                            </div>
                            
                            <div id="haram-details" class="payment-details" style="display: none;">
                                <p>الاسم: <span>علي ابراهيم محمود</span> <button class="copy-btn" onclick="copyToClipboard('علي ابراهيم محمود')">نسخ</button></p>
                                <p>رقم الهاتف: <span>0934598967</span> <button class="copy-btn" onclick="copyToClipboard('0934598967')">نسخ</button></p>
                                <p>المدينة: <span>اللاذقية</span> <button class="copy-btn" onclick="copyToClipboard('اللاذقية')">نسخ</button></p>
                            </div>
                            
                            <div id="bemo-details" class="payment-details" style="display: none;">
                                <p>الاسم: <span>علي ابراهيم محمود</span> <button class="copy-btn" onclick="copyToClipboard('علي ابراهيم محمود')">نسخ</button></p>
                                <p>رقم الحساب: <span>060104947910013000000</span> <button class="copy-btn" onclick="copyToClipboard('060104947910013000000')">نسخ</button></p>
                            </div>
                            
                            <div id="sham-details" class="payment-details" style="display: none;">
                                <p>العنوان: <span>be456e0ea9392db4d68a7093ee317bc8</span> <button class="copy-btn" onclick="copyToClipboard('be456e0ea9392db4d68a7093ee317bc8')">نسخ</button></p>
                                <p>رقم الحساب: <span>5991161126028260</span> <button class="copy-btn" onclick="copyToClipboard('5991161126028260')">نسخ</button></p>
                            </div>
                        </div>
                        
                        <div class="form-row">
                            <button type="button" class="btn btn-back" onclick="prevStep(4)">السابق</button>
                            <button type="button" class="btn btn-next" onclick="nextStep(4)">التالي</button>
                        </div>
                    </div>
                    
                    <!-- Step 4: Sell Address -->
                    <div class="form-step" id="step4-sell">
                        <h3>عنوان المحفظة</h3>
                        
                        <div class="form-group">
                            <label>اختر شبكة USDT المراد بيعها</label>
                            <div class="payment-methods">
                                <div class="payment-method" onclick="selectSellNetwork('bep20')">
                                    <i class="fab fa-ethereum"></i>
                                    <h4>BEP20</h4>
                                    <p>0x21802218d8d661d66F2C7959347a6382E1cc614F</p>
                                </div>
                                
                                <div class="payment-method" onclick="selectSellNetwork('trc20')">
                                    <i class="fas fa-coins"></i>
                                    <h4>TRC20</h4>
                                    <p>TD2LoErPRkVPBxDk72ZErtiyi6agirZQjX</p>
                                </div>
                                
                                <div class="payment-method" onclick="selectSellNetwork('erc20')">
                                    <i class="fab fa-ethereum"></i>
                                    <h4>ERC20</h4>
                                    <p>0x21802218d8d661d66F2C7959347a6382E1cc614F</p>
                                </div>
                                
                                <div class="payment-method" onclick="selectSellNetwork('binance-pay')">
                                    <i class="fab fa-bitcoin"></i>
                                    <h4>Binance Pay</h4>
                                    <p>969755964</p>
                                </div>
                            </div>
                            <input type="hidden" id="sell-network-final">
                        </div>
                        
                        <div class="form-group">
                            <label for="sell-address-final">أو أدخل العنوان يدوياً</label>
                            <input type="text" id="sell-address-final">
                        </div>
                        
                        <div class="form-row">
                            <button type="button" class="btn btn-back" onclick="prevStep(4)">السابق</button>
                            <button type="button" class="btn btn-next" onclick="nextStep(4)">التالي</button>
                        </div>
                    </div>
                    
                    <!-- Step 5: Summary -->
                    <div class="form-step" id="step5">
                        <h3>ملخص الطلب</h3>
                        
                        <div class="order-summary" id="order-summary">
                            <!-- Will be filled by JavaScript -->
                        </div>
                        
                        <div class="form-group">
                            <label for="confirmation">أقر بأن جميع المعلومات المقدمة صحيحة</label>
                            <input type="checkbox" id="confirmation" required>
                        </div>
                        
                        <div class="form-row">
                            <button type="button" class="btn btn-back" onclick="prevStep(5)">السابق</button>
                            <button type="submit" class="btn btn-submit">إرسال الطلب</button>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        <p>جميع الحقوق محفوظة &copy; دليل المتداول 2023</p>
        <div class="social-links">
            <a href="https://t.me/ali0619000" class="social-link telegram" target="_blank">
                <i class="fab fa-telegram"></i>
            </a>
            <a href="mailto:alimahmoud001a@gmail.com" class="social-link email">
                <i class="fas fa-envelope"></i>
            </a>
        </div>
    </div>

    <script>
        // Menu Toggle
        document.getElementById('menu-toggle').addEventListener('click', function() {
            document.getElementById('sidebar').classList.toggle('active');
            document.getElementById('main-content').classList.toggle('active');
        });

        // Section Navigation
        document.querySelectorAll('[data-section]').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const sectionId = this.getAttribute('data-section');
                
                // Hide all sections
                document.querySelectorAll('.section').forEach(section => {
                    section.classList.remove('active');
                });
                
                // Show selected section
                document.getElementById(sectionId).classList.add('active');
                
                // Close sidebar on mobile
                if (window.innerWidth < 992) {
                    document.getElementById('sidebar').classList.remove('active');
                    document.getElementById('main-content').classList.remove('active');
                }
            });
        });

        // Submenu Toggle
        document.querySelectorAll('.has-submenu').forEach(item => {
            item.addEventListener('click', function(e) {
                if (e.target === this) {
                    e.preventDefault();
                    const submenu = this.nextElementSibling;
                    submenu.classList.toggle('active');
                    
                    const icon = this.querySelector('.fa-chevron-down');
                    icon.classList.toggle('fa-rotate-180');
                }
            });
        });

        // Capital Calculator
        document.getElementById('capital-calculator').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get input values
            const initialCapital = parseFloat(document.getElementById('initial-capital').value);
            const winRate = parseFloat(document.getElementById('win-rate').value) / 100;
            const profitPerTrade = parseFloat(document.getElementById('profit-per-trade').value) / 100;
            const lossPerTrade = parseFloat(document.getElementById('loss-per-trade').value) / 100;
            const tradesInterval = parseInt(document.getElementById('trades-interval').value);
            const targetCapital = parseFloat(document.getElementById('target-capital').value);
            
            // Calculate results
            const avgReturn = (winRate * profitPerTrade) - ((1 - winRate) * lossPerTrade);
            const requiredTrades = Math.ceil(Math.log(targetCapital / initialCapital) / Math.log(1 + avgReturn));
            const totalGrowth = ((targetCapital - initialCapital) / initialCapital) * 100;
            
            // Display results
            document.getElementById('avg-return').textContent = (avgReturn * 100).toFixed(2) + '%';
            document.getElementById('required-trades').textContent = requiredTrades;
            document.getElementById('total-growth').textContent = totalGrowth.toFixed(2) + '%';
            
            // Generate capital growth data
            const capitalData = [];
            const labels = [];
            const tableBody = document.getElementById('capital-table-body');
            tableBody.innerHTML = '';
            
            let currentCapital = initialCapital;
            for (let i = 0; i <= requiredTrades; i += tradesInterval) {
                if (i > 0) {
                    for (let j = 0; j < tradesInterval; j++) {
                        if (Math.random() < winRate) {
                            currentCapital *= (1 + profitPerTrade);
                        } else {
                            currentCapital *= (1 - lossPerTrade);
                        }
                    }
                }
                
                capitalData.push(currentCapital);
                labels.push(i);
                
                // Add to table
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${i}</td>
                    <td>${currentCapital.toFixed(2)}</td>
                    <td>${((currentCapital / initialCapital - 1) * 100).toFixed(2)}%</td>
                `;
                tableBody.appendChild(row);
            }
            
            // Create chart
            const ctx = document.getElementById('capital-chart').getContext('2d');
            if (window.capitalChart) {
                window.capitalChart.destroy();
            }
            
            window.capitalChart = new Chart(ctx, {
                type: 'line',
                data: {
                    labels: labels,
                    datasets: [{
                        label: 'رأس المال ($)',
                        data: capitalData,
                        borderColor: '#3498db',
                        backgroundColor: 'rgba(52, 152, 219, 0.1)',
                        borderWidth: 2,
                        fill: true,
                        tension: 0.4
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        title: {
                            display: true,
                            text: 'تطور رأس المال مع عدد الصفقات',
                            font: {
                                size: 16
                            }
                        },
                        legend: {
                            position: 'top',
                            rtl: true
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return 'رأس المال: $' + context.parsed.y.toFixed(2);
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            title: {
                                display: true,
                                text: 'عدد الصفقات'
                            }
                        },
                        y: {
                            title: {
                                display: true,
                                text: 'رأس المال ($)'
                            },
                            beginAtZero: false
                        }
                    }
                }
            });
            
            // Show results
            document.getElementById('calculator-results').style.display = 'block';
        });

        // USDT Exchange Form
        let currentStep = 1;
        let transactionType = '';
        let paymentMethod = '';
        let buyPaymentMethod = '';
        let sellNetwork = '';
        
        function nextStep(step) {
            // Validate current step before proceeding
            if (step === 1) {
                if (!document.getElementById('full-name').value || 
                    !document.getElementById('phone').value || 
                    !document.getElementById('city').value) {
                    alert('الرجاء ملء جميع الحقول المطلوبة');
                    return;
                }
            } else if (step === 2) {
                if (!transactionType) {
                    alert('الرجاء اختيار نوع العملية');
                    return;
                }
            } else if (step === 3) {
                if (transactionType === 'buy') {
                    if (!document.getElementById('buy-amount').value || 
                        !document.getElementById('buy-network').value || 
                        !document.getElementById('buy-address').value) {
                        alert('الرجاء ملء جميع الحقول المطلوبة');
                        return;
                    }
                } else {
                    if (!document.getElementById('sell-amount').value || 
                        !paymentMethod || 
                        !document.getElementById('sell-network').value) {
                        alert('الرجاء ملء جميع الحقول المطلوبة');
                        return;
                    }
                    
                    if (paymentMethod && !document.getElementById('payment-details').value) {
                        alert('الرجاء إدخال تفاصيل الحساب');
                        return;
                    }
                }
            } else if (step === 4) {
                if (transactionType === 'buy' && !buyPaymentMethod) {
                    alert('الرجاء اختيار طريقة الدفع');
                    return;
                } else if (transactionType === 'sell' && !sellNetwork) {
                    alert('الرجاء اختيار شبكة USDT');
                    return;
                }
            } else if (step === 5) {
                if (!document.getElementById('confirmation').checked) {
                    alert('الرجاء تأكيد أن المعلومات صحيحة');
                    return;
                }
                
                // Prepare order summary
                prepareOrderSummary();
            }
            
            // Hide current step
            if (transactionType === 'buy') {
                document.getElementById(`step${step}-buy`).classList.remove('active');
            } else {
                document.getElementById(`step${step}-sell`).classList.remove('active');
            }
            
            // Show next step
            currentStep = step + 1;
            
            if (currentStep === 3) {
                if (transactionType === 'buy') {
                    document.getElementById('step3-buy').classList.add('active');
                } else {
                    document.getElementById('step3-sell').classList.add('active');
                }
            } else if (currentStep === 4) {
                if (transactionType === 'buy') {
                    document.getElementById('step4-buy').classList.add('active');
                } else {
                    document.getElementById('step4-sell').classList.add('active');
                }
            } else if (currentStep === 5) {
                document.getElementById('step5').classList.add('active');
            } else {
                document.getElementById(`step${currentStep}`).classList.add('active');
            }
        }
        
        function prevStep(step) {
            // Hide current step
            if (step === 3 && transactionType === 'buy') {
                document.getElementById('step3-buy').classList.remove('active');
            } else if (step === 3 && transactionType === 'sell') {
                document.getElementById('step3-sell').classList.remove('active');
            } else if (step === 4 && transactionType === 'buy') {
                document.getElementById('step4-buy').classList.remove('active');
            } else if (step === 4 && transactionType === 'sell') {
                document.getElementById('step4-sell').classList.remove('active');
            } else if (step === 5) {
                document.getElementById('step5').classList.remove('active');
            } else {
                document.getElementById(`step${step}`).classList.remove('active');
            }
            
            // Show previous step
            currentStep = step - 1;
            
            if (currentStep === 3) {
                if (transactionType === 'buy') {
                    document.getElementById('step3-buy').classList.add('active');
                } else {
                    document.getElementById('step3-sell').classList.add('active');
                }
            } else if (currentStep === 4) {
                if (transactionType === 'buy') {
                    document.getElementById('step4-buy').classList.add('active');
                } else {
                    document.getElementById('step4-sell').classList.add('active');
                }
            } else {
                document.getElementById(`step${currentStep}`).classList.add('active');
            }
        }
        
        function selectTransactionType(type) {
            transactionType = type;
            document.getElementById('transaction-type').value = type;
            
            // Update UI
            document.querySelectorAll('#step2 .payment-method').forEach(method => {
                method.classList.remove('active');
            });
            
            if (type === 'buy') {
                document.querySelector('#step2 .payment-method:nth-child(1)').classList.add('active');
            } else {
                document.querySelector('#step2 .payment-method:nth-child(2)').classList.add('active');
            }
            
            document.getElementById('step2-next').disabled = false;
        }
        
        function selectPaymentMethod(method) {
            paymentMethod = method;
            document.getElementById('payment-method').value = method;
            
            // Update UI
            document.querySelectorAll('#step3-sell .payment-method').forEach(m => {
                m.classList.remove('active');
            });
            
            document.querySelector(`#step3-sell .payment-method[onclick="selectPaymentMethod('${method}')"]`).classList.add('active');
            
            // Show payment details field
            document.getElementById('payment-details-container').style.display = 'block';
            
            // Update label
            let labelText = '';
            if (method === 'syriatel') {
                labelText = 'رقم هاتف سيريتل كاش';
            } else if (method === 'haram') {
                labelText = 'رقم هاتف حوالة الهرم';
            } else if (method === 'bemo') {
                labelText = 'رقم الحساب البنكي';
            } else if (method === 'sham') {
                labelText = 'رقم حساب شام كاش';
            }
            
            document.getElementById('payment-details-label').textContent = labelText;
        }
        
        function selectBuyPaymentMethod(method) {
            buyPaymentMethod = method;
            document.getElementById('buy-payment-method').value = method;
            
            // Update UI
            document.querySelectorAll('#step4-buy .payment-method').forEach(m => {
                m.classList.remove('active');
            });
            
            document.querySelector(`#step4-buy .payment-method[onclick="selectBuyPaymentMethod('${method}')"]`).classList.add('active');
            
            // Show payment details
            document.getElementById('buy-payment-details').style.display = 'block';
            document.querySelectorAll('.payment-details').forEach(d => {
                d.style.display = 'none';
            });
            
            document.getElementById(`${method}-details`).style.display = 'block';
        }
        
        function selectSellNetwork(network) {
            sellNetwork = network;
            document.getElementById('sell-network-final').value = network;
            
            // Update UI
            document.querySelectorAll('#step4-sell .payment-method').forEach(m => {
                m.classList.remove('active');
            });
            
            document.querySelector(`#step4-sell .payment-method[onclick="selectSellNetwork('${network}')"]`).classList.add('
