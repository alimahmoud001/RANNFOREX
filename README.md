<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rannforex - لقد قمت بإضافة كل شيء تحتاجه في مجال التداول  إلى هذا الموقع لن تحتاج إلى شيء آخر</title>
    <!-- مكتبة Font Awesome للأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- خطوط Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        /* ===== تنسيقات عامة ===== */
        :root {
            /* الألوان الرئيسية */
            --primary-color: #2e4057;    /* اللون الأساسي (أزرق داكن) */
            --secondary-color: #048ba8;  /* اللون الثانوي (أزرق فاتح) */
            --accent-color: #f18f01;     /* لون التمييز (برتقالي) */
            --light-color: #f5f5f5;      /* لون فاتح */
            --dark-color: #1a1a1a;       /* لون داكن */
            --success-color: #4caf50;    /* لون النجاح (أخضر) */
            --warning-color: #ff9800;    /* لون التحذير (برتقالي) */
            --danger-color: #f44336;     /* لون الخطر (أحمر) */
            
            /* قيم التصميم */
            --border-radius: 25px;        /* نصف قطر الحواف */
            --box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            --transition: all 0.3s ease; /* تأثير الانتقال */
        }

        /* إعادة تعيين التنسيقات الافتراضية */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* تنسيق التمرير السلس */
        html {
            scroll-behavior: smooth;
        }

        /* تنسيقات الجسم */
        body {
            font-family: 'Cairo', sans-serif;
            line-height: 1.6;
            color: var(--dark-color);
            background-color: #f9f9f9;
            overflow-x: hidden;
        }

        /* تنسيق الحاوية */
        .container {
            width: 100%;
            max width : 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 00px;
        }

        /* تنسيق الروابط */
        a {
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
        }

        /* تنسيق القوائم */
        ul {
            list-style: none;
        }

        /* تنسيق الصور */
        img {
            max-width: 100%;
            height: auto;
        }

        /* ===== تنسيقات الأزرار ===== */
        .btn {
            display: inline-block;
            padding: 12px 24px;
            border-radius: var(--border-radius);
            font-weight: 600;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            outline: none;
            box-shadow: var(--box-shadow);
        }

        /* زر أساسي */
        .btn-primary {
            background-color: var(--primary-color);
            color: white;
        }

        .btn-primary:hover {
            background-color: #1a2a3a;
            transform: translateY(-3px);
        }

        /* زر ثانوي */
        .btn-secondary {
            background-color: var(--secondary-color);
            color: white;
        }

        .btn-secondary:hover {
            background-color: #036d85;
            transform: translateY(-3px);
        }

        /* زر مخطط */
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
        }

        .btn-outline:hover {
            background-color: var(--primary-color);
            color: white;
            transform: translateY(-3px);
        }

        /* زر التطبيق */
        .btn-app {
            background-color: var(--accent-color);
            color: white;
            width: 100%;
            margin-top: 15px;
        }

        .btn-app:hover {
            background-color: #d97e00;
            transform: translateY(-3px);
        }

        /* زر تلجرام */
        .btn-telegram {
            background-color: #0088cc;
            color: white;
        }

        .btn-telegram:hover {
            background-color: #006699;
            transform: translateY(-3px);
        }


        /* زر الكورس */
        .btn-course {
            background-color: #ff5722;
            color: white;
            width: 100%;
            margin-top: 15px;
        }

        .btn-course:hover {
            background-color: #e64a19;
            transform: translateY(-3px);
        }

        /* ===== تنسيقات الهيدر ===== */
        .header {
            background-color: var(--primary-color);
            color: white;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-radius: 25px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* تنسيق الشعار */
        .logo h1 {
            font-size: 1rem;
            font-weight: 800;
            color: var(--accent-color);
            margin-bottom: 5px;
        }

        .logo p {
            font-size: 1rem;
            opacity: 0.8;
        }

        /* تنسيق القائمة الرئيسية */
        .main-nav ul {
            display: flex;
        }

        .main-nav ul li {
            margin-right: 20px;
        }

        .main-nav ul li:last-child {
            margin-right: 0;
        }

        .main-nav ul li a {
            color: white;
            font-weight: 200;
            padding: 10px 0;
            position: relative;
        }

        /* تأثير تحت الروابط عند التحويم */
        .main-nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent-color);
            transition: var(--transition);
        }

        .main-nav ul li a:hover::after {
            width: 100%;
        }
    /* زر القائمة للموبايل */
        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* ===== تنسيقات الأقسام ===== */
        .section {
            padding: 80px 0;
        }

        /* تلوين الأقسام بالتناوب */
        .section:nth-child(even) {
            background-color: #f0f4f8;
        }

        /* عناوين الأقسام */
        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 50px;
            color: var(--primary-color);
            position: relative;
            padding-bottom: 15px;
        }

        /* خط تحت عناوين الأقسام */
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: var(--accent-color);
            border-radius: 2px;
        }

        /* ===== تنسيقات القسم الأول ===== */
        /* بطاقة التسجيل */
        .register-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 30px;
            text-align: center;
            box-shadow: var(--box-shadow);
            margin-bottom: 50px;
            border-top: 5px solid var(--accent-color);
        }

        .register-card h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .register-card p {
            margin-bottom: 25px;
            font-size: 1.1rem;
        }

        /* قسم المميزات */
        .features {
            margin-bottom: 50px;
        }

        .features h3 {
            font-size: 1.8rem;
            text-align: center;
            margin-bottom: 30px;
            color: var(--primary-color);
        }



        /* معلومات الاسبريد */
        .spread-info {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 30px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .spread-info h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        /* ===== تنسيقات القسم الثاني ===== */
        /* شبكة بطاقات التقييمات */
        .ratings-grid {
            display: grid;
            grid-template-rows: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }

        /* بطاقة تقييم */
        .rating-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 25px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-height: 300px;
        }

        .rating-card:hover {
            transform: translateY(-10px);
        }

        .rating-card img {
            max-height: 60px;
            margin-bottom: 20px;
            object-fit: contain;
        }

        .rating-logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        /* ===== تنسيقات القسم الثالث ===== */
        /* شبكة بطاقات التطبيقات */
        .apps-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        /* بطاقة تطبيق */
        .app-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 30px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: var(--transition);
        }

        .app-card:hover {
            transform: translateY(-10px);
        }

        .app-icon {
            font-size: 3rem;
            color: var(--accent-color);
            margin-bottom: 20px;
        }

        .app-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .app-card p {
            margin-bottom: 20px;
            min-height: 50px;
        }

        /* ===== تنسيقات القسم الرابع ===== */
        /* بطاقة الدروس التعليمية */
        .tutorial-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 30px;
            box-shadow: var(--box-shadow);
        }

        .tutorial-card h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--primary-color);
            text-align: center;
        }

        /* حاوية الفيديو بنسبة 16:9 */
        .video-container {
            position: relative;
            padding-bottom: 56.25%; /* نسبة 16:9 */
            height: 0;
            overflow: hidden;
            border-radius: var(--border-radius);
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        /* ===== تنسيقات القسم الخامس ===== */
        /* قنوات تلجرام */
        .telegram-channels {
            text-align: center;
        }

        /* القناة الرئيسية */
        .main-channel {
            background-color: #0088cc;
            color: light blue;
            margin-bottom: 40px;
        }

        .main-channel i {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .main-channel h3 {
            color: blue;
        }

        /* عنوان قنوات الإشارات */
        .signals-title {
            font-size: 1.8rem;
            margin-bottom: 25px;
            color: var(--primary-color);
        }

        /* شبكة قنوات الإشارات */
        .signals-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }

        /* بطاقة قناة */
        .channel-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 20px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: var(--transition);
        }

        .channel-card:hover {
            transform: translateY(-5px);
            background-color: #f5f5f5;
        }

        .channel-card a {
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-color);
            font-weight: 600;
        }

        .channel-card a i {
            color: #0088cc;
            margin-left: 10px;
            font-size: 1.2rem;
        }

        /* ===== تنسيقات القسم السادس ===== */
        /* شبكة الكورسات */
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        /* بطاقة كورس */
        .course-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 30px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: var(--transition);
        }

        .course-card:hover {
            transform: translateY(-10px);
        }

        .course-icon {
            font-size: 3rem;
            color: #ff0000;
            margin-bottom: 20px;
        }

        .course-icon .fa-instagram {
            color: #e1306c;
        }

        .course-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .course-card p {
            margin-bottom: 20px;
            min-height: 50px;
        }

        /* ===== تنسيقات القسم السابع ===== */
        /* معلومات الاتصال */
        .contact-info {
            text-align: center;
            margin-bottom: 40px;
        }

        .contact-info p {
            font-size: 1.2rem;
            margin-bottom: 15px;
        }

        .contact-phone, .contact-email {
            font-weight: 600;
            color: var(--primary-color);
        }

       
        /* ===== تنسيقات الفوتر ===== */ 

social-icon:hover {
            transform: translateY(-5px) scale(1.1);
        }

        .footer {
            background-color: var(--primary-color);
            color: white;
            padding: 20px 0;
            text-align: center;
            border-radius: 25px; 
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
        }

        /* ===== تنسيقات التجاوب مع الشاشات المختلفة ===== */
        /* الشاشات المتوسطة (أقل من 992 بكسل) */
        @media (max-width: 992px) {
            .main-nav {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .section {
                padding: 60px 0;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* الشاشات الصغيرة (أقل من 768 بكسل) */
        @media (max-width: 768px) {
            .features-grid,  .apps-grid, .signals-grid, .courses-grid {
                grid-template-columns: repeat(auto-fill, minmax(45%, 1fr));
            }

            .section {
                padding: 40px 0;
            }

            .section-title {
                font-size: 1.8rem;
                margin-bottom: 30px;
            }

            .register-card h3, .features h3, .spread-info h3, .signals-title {
                font-size: 1.5rem;
            }

            .feature-card, .rating-card, .app-card, .channel-card, .course-card {
                padding: 4px;
                width: 100%;
                font-size: 1rem;
            }
        }

        /* الشاشات الصغيرة جداً (أقل من 576 بكسل) */
        @media (max-width: 576px) {
            .logo h1 {
                font-size: 1.8rem;
            }

            .logo p {
                font-size: 0.9rem;
            }

            .btn {
                padding: 10px 20px;
                font-size: 0.9rem;
            }

            .social-icons {
                flex-wrap: wrap;
            }
        }

        /* ===== تأثيرات إضافية ===== */
        /* تأثير الظهور التدريجي */
        .fade-in {
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* تأثير النبض */
        .pulse {
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <!-- القسم العلوي (الهيدر) -->
    <header class="header">
        <div class="container">
            <div class="logo">
                <h1>Rannforex</h1>
            </div>
            <nav class="main-nav">
                <ul>
                    <li><a href="#section1">الرئيسية</a></li>
                    <li><a href="#section2">التقييمات</a></li>
                    <li><a href="#section3">التطبيقات</a></li>
                    <li><a href="#section4">المصادقة</a></li>
                    <li><a href="#section5">قنوات تلجرام</a></li>
                    <li><a href="#section6">الكورسات</a></li>
                </ul>
            </nav>
            <div class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- القسم الرئيسي -->
    <main>
        <!-- القسم الأول: معلومات شركة الوساطة المالية -->
        <section id="section1" class="section">
            <div class="container">
                <h2 class="section-title" > يمكنك التداول بحد أدنى للايداع والسحب 10$ مع رافعة مالية 1:500 وبأقل اسبريد بدءا من 0.2-1.2 نقطة وتقييم الشركة ممتاز </h2>
                <div class="register-card">
                    <h3>سجل الآن في Rannforex</h3>
                    <p>ابدأ رحلتك في عالم التداول مع شركة وساطة مالية موثوقة</p>
                    <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="btn btn-primary" target="_blank">
                        <i class="fas fa-user-plus"></i> سجل الآن
                    </a>
                </div>
                <div class="register-card">
                    <h3>استثمر معنا في حساب مدار pamm</h3>
                    <p> لعرض تفاصيل حساب المدير </p>
                    <a href=" https://my.rannforex.com/en/pamm/details/2496/  " class="btn btn-primary" target="_blank">
                        <i class="fas fa-user-plus"></i> استثمر الآن
                    </a>
 </div>
      <div class="register-card">
                    <h3>انضم إلى قناة الإشارات الخاصة </h3>
                    <p> أعطي إشارات مجانية لمن قام بالتسجيل في الشركة حصرا</p>
                    <a href=" https://t.me/+4zjJE9uJ7Hs4MmQ0/" class="btn btn-primary" target="_blank">
                        <i class="fas fa-user-plus"></i> انضم الآن
                    </a>
                </div>
                 
                    </div>
 <!-- القسم الثالث: تطبيقات يجب تحميلها للبدء بالتداول -->
        <section id="section3" class="section">
            <div class="container">
                <h2 class="section-title">تطبيقات يجب تحميلها للبدء بالتداول</h2>
                <div class="apps-grid">
                    <div class="app-card">
                        <div class="app-icon">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" class="btn btn-app" target="_blank">
                            <i class="fab fa-google-play"></i>  ميتا تريدر 5
                        </a>
                    </div>
                    <div class="app-card">
                        <div class="app-icon">
                            <i class="fas fa-wallet"></i>
                        </div>
                        <a href="https://cwallet.com/referral/DvY6dZtS" class="btn btn-app" target="_blank">
                            <i class="fas fa-download"></i> المحفظة الالكترونية 
                        </a>
                    </div>
                    <div class="app-card">
                        <div class="app-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" class="btn btn-app" target="_blank">
                            <i class="fab fa-google-play"></i> المصادقة الثنائية
                </a>
                    </div>
                 <div class="app-card">
                <div class="app-icon">
                    <i class="fas fa-chart-bar"></i>
                </div>
                <a href="https://play.google.com/store/apps/details?id=com.tradingview.tradingviewapp" class="btn btn-app" target="_blank">
                    <i class="fab fa-google-play"></i> تريدنغ فيو
                </a>
            </div>
                </div>
           
  
               <section id="section2" class="section">
                <div class="spread-info">
                    <h3>اطلع على الاسبريد المتوسط اليومي</h3>
                    <a href="https://rannforex.com/en/trading/quotesonline/" class="btn btn-secondary" target="_blank">
                        <i class="fas fa-chart-bar"></i> عرض الاسبريد
                    </a>
                 </div> 
   <section>         
                            
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>خطوات الإيداع</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            direction: rtl;
            text-align: right;
            background-color: #f4f4f4;
            margin: 0;
            padding: 00px;
            border-radius: 20px;

        }
        .accordion {
            background-color: #f18f01;
            color: white;
            cursor: pointer;
            padding: 20px;
            width: 100%;
            border: none;
            text-align: center;
            outline: none;
            font-size: 18px;
            border-radius: 25px; 
            transition: background-color 0.3s;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
        }
        .accordion:hover {
            background-color: #0056b3;
        }
        .panel {
            padding: 0 18px;
            display: none;
            background-color: white;
            overflow: hidden;
            border: 1px solid #ddd;
            border-radius: 25px;
            margin-bottom: 10px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
        }
        .panel p, .panel ol {
            font-size: 16px;
            line-height: 1.6;
            color: #333;
        }
        .panel ol {
            padding-right: 20px;
        }
        .panel li {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
  <section id="section2" class="section">
            <div class="container">
                <h2 class="section-title">خطوات الإيداع</h2>
    <button class="accordion">خطوات الإيداع</button>
    <div class="panel">
        <ol>
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

    <script>
        const accordion = document.querySelector('.accordion');
        const panel = document.querySelector('.panel');

        accordion.addEventListener('click', function() {
            this.classList.toggle('active');
            panel.style.display = panel.style.display === 'block' ? 'none' : 'block';
        });
    </script>

        

        <!-- القسم الثاني: تقييمات الشركة -->
        <section id="section2" class="section">
            <div class="container">
                <h2 class="section-title">تقييمات الشركة</h2>
                <div class="ratings-grid">
                    <div class="rating-card">
                        <a href="https://fr.trustpilot.com/review/rannforex.com" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> Trustpilot
                        </a>
  <a href="https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> myfxbook
                        </a>
 <a href="https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> forexpeacearmy
                        </a>
  <a href="https://www.wikifx.com/en/dealer/1141850612.html" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> wikifx
                        </a>  
                    </div>
                </div>
            </div>
        </section>

           <!-- القسم الرابع: 2FA -->
        <section id="section4" class="section">
            <div class="container">
                <h2 class="section-title">2FA المصادقة</h2>
                <div class="tutorial-card">
                    <h3>فيديو بسيط حول كيفية استخدام تطبيق Google Authenticator</h3>
                    <div class="video-container">
                        <iframe src="https://www.youtube.com/embed/SlQc3Q6L3HQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                </div>
            </div>        
        </section>


        <!-- القسم الخامس: قنوات مهمة على تلجرام -->
        <section id="section5" class="section">
            <div class="container">
                <h2 class="section-title">قنوات مهمة على تلجرام</h2>
                <div class="telegram-channels">
                   
                    
                    <h3 class="signals-title">قنوات الإشارات (للتعلم وليس لنسخ الإشارات)</h3>
                    <div class="signals-grid">
                        <div class="channel-card">
                            <a href="https://t.me/FX_IRI" target="_blank">
                                <i class="fab fa-telegram"></i> FX_IRI
                            </a>
                        </div>
                        <div class="channel-card">
                            <a href="https://t.me/prosignalsfxx" target="_blank">
                                <i class="fab fa-telegram"></i> Pro Signals FX
                            </a>
                        </div>
                        <div class="channel-card">
                            <a href="https://t.me/top_tradingsignals" target="_blank">
                                <i class="fab fa-telegram"></i> Top Trading Signals
                            </a>
                        </div>
                        <div class="channel-card">
                            <a href="https://t.me/signalsfc" target="_blank">
                                <i class="fab fa-telegram"></i> Signals FC
                            </a>
                        </div>
                        <div class="channel-card">
                            <a href="https://t.me/elitetrading_signals" target="_blank">
                                <i class="fab fa-telegram"></i> Elite Trading Signals
                            </a>
                        </div>
                        <div class="channel-card">
                            <a href="https://t.me/free_signals" target="_blank">
                                <i class="fab fa-telegram"></i> Free Signals
                            </a>
                        </div>
                        <div class="channel-card">
                            <a href="https://t.me/greysuitcommunity" target="_blank">
                                <i class="fab fa-telegram"></i> Grey Suit Community
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- القسم السادس: القسم التعليمي -->
        <section id="section6" class="section">
            <div class="container">
                <h2 class="section-title">القسم التعليمي </h2>
                <div class="courses-grid">
                    <div class="course-card">
                        <div class="course-icon">
                            <i class="fab fa-youtube"></i>
                        </div>
                        <h3>TRADE WITH PATT</h3>
                        <a href="https://youtube.com/@tradewithpatarabic?si=4egOIQw15KHmRJGy" class="btn btn-course" target="_blank">
                            مشاهدة الكورس
                        </a>
                    </div>

                    <div class="course-card">
    <div class="course-icon">
        <i class="fab fa-youtube"></i>
    </div>
    <h3>Easy Trade</h3>
    <a href="https://youtube.com/@easytradingeasy?si=9sITj4F_D__TAfb5" class="btn btn-course" target="_blank">
        مشاهدة الكورس
    </a>
</div>
                    <div class="course-card">
                        <div class="course-icon">
                            <i class="fab fa-youtube"></i>
                        </div>
                        <h3>SMART RISK</h3>
                        <a href="https://youtube.com/@smart_risk?si=s0leP3OYv9GuCp3r" class="btn btn-course" target="_blank">
                            مشاهدة الكورس
                        </a>
                    </div>
                    <div class="course-card">
                        <div class="course-icon">
                            <i class="fab fa-instagram"></i>
                        </div>
                        <h3>KAMEL M5</h3>
                        <a href="https://www.instagram.com/kameel_m5/reel/DIvnWEQM_4g/" class="btn btn-course" target="_blank">
                            مشاهدة الكورس
                        </a>
                    </div>
                              <div class="course-icon">
                    </div>
                </div>
         </div>
        </section>

    <!-- القسم السفلي (الفوتر) -->
    <footer class="footer">
        <div class="container">
            <p> «Directed by Ali Mahmoud» </p>
        </div>
    </footer>

    <!-- سكريبت جافاسكريبت -->
    <script>
        // تنفيذ الكود عند اكتمال تحميل المستند
        document.addEventListener('DOMContentLoaded', function() {
            // إضافة تأثير الظهور التدريجي للأقسام
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.add('fade-in');
            });

            // إضافة تأثير النبض لزر التسجيل
            const registerBtn = document.querySelector('.register-card .btn-primary');
            if (registerBtn) {
                registerBtn.classList.add('pulse');
            }

            // التعامل مع قائمة التنقل المتحركة
            const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
            const mainNav = document.querySelector('.main-nav');
            
            if (mobileMenuBtn && mainNav) {
                mobileMenuBtn.addEventListener('click', function() {
                    mainNav.style.display = mainNav.style.display === 'block' ? 'none' : 'block';
                });
            }

            // إضافة تأثير التمرير السلس للروابط
            const navLinks = document.querySelectorAll('.main-nav a');
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        // التمرير إلى العنصر المستهدف مع تعويض ارتفاع الهيدر
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                        
                        // إغلاق القائمة المتحركة بعد النقر على رابط (للموبايل)
                        if (window.innerWidth < 992) {
                            mainNav.style.display = 'none';
                        }
                    }
                });
            });

            // تحسين تجربة المستخدم على الأجهزة المحمولة
            function handleResponsiveLayout() {
                if (window.innerWidth < 992) {
                    mainNav.style.display = 'none';
                } else {
                    mainNav.style.display = 'block';
                }
            }

            // تنفيذ عند تحميل الصفحة وتغيير حجم النافذة
            handleResponsiveLayout();
            window.addEventListener('resize', handleResponsiveLayout);

            // إضافة تأثيرات حركية للبطاقات عند التمرير
            const cards = document.querySelectorAll('.feature-card, .rating-card, .app-card, .channel-card, .course-card');
            
            // التحقق مما إذا كان العنصر مرئياً في نافذة العرض
            function isElementInViewport(el) {
                const rect = el.getBoundingClientRect();
                return (
                    rect.top >= 0 &&
                    rect.left >= 0 &&
                    rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
                    rect.right <= (window.innerWidth || document.documentElement.clientWidth)
                );
            }
            
            // معالجة تأثيرات التمرير
            function handleScroll() {
                cards.forEach(card => {
                    if (isElementInViewport(card)) {
                        card.classList.add('fade-in');
                    }
                });
            }
            
            // تنفيذ عند التمرير
            window.addEventListener('scroll', handleScroll);
            handleScroll(); // تنفيذ مرة واحدة عند تحميل الصفحة
            
            // إضافة تأثير تفاعلي لأيقونات وسائل التواصل الاجتماعي
            const socialIcons = document.querySelectorAll('.social-icon');
            socialIcons.forEach(icon => {
                icon.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-5px) scale(1.1)';
                });
                
                icon.addEventListener('mouseleave', function() {
                    this.style.transform = '';
                });
            });
        });


        
    </script><!--Start of Tawk.to Script-->
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
</a>

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





===








<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نافذة الإيداع المنعزلة</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* هذه الأنماط للعرض التوضيحي فقط - يمكن حذفها */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background: #f5f7fa;
            color: #333;
        }
        .demo-content {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        h1 {
            color: #2c3e50;
            text-align: center;
            margin-bottom: 30px;
        }
        p {
            margin-bottom: 15px;
        }
    </style>
</head>
<body>
    <div class="demo-content">
        <h1>صفحتي الرئيسية</h1>
        <p>هذه محاكاة لصفحة ويب رئيسية تحتوي على محتوى متنوع. سيتم إضافة زر الإيداع في أسفل يمين الصفحة دون التأثير على تنسيقها الحالي.</p>
        
        <p>لوريم إيبسوم دولور سيت أميت، كونسيكتيتور أديبيسسينغ إيليت. سيد دو أيوسمود تيمبور أنكايديديونتيوت لابوري أت دولور ماجنا أليكوا. يوت انيم أد مينيم فينيم، كيويس نوسترود أكسيرسيتاشيون أللامكو لابوريس نيسيوت.</p>
        
        <p>يوت أليبكيو أكس اي كومودو كونسيكويت. ديويس أيوتي أرير دولور إن ريبرهينديريت إن فوليوبتات فيليت إيسي كيواي نون بروايدينت، صن إن كولبا كيو ريبريهنيديرايت.</p>
        
        <p>فوليوبتاتي بوسكايسيوم كابرياس كيو دولوريمكيو. إست أيريور دولوريس إيوس كيوسدام إت أوفيسييس ديبايتيس. إكسسبتيور سينت أوكايكيات كيوبايدايتات نون بروفايدنت، صن إن كولبا كيو ريبريهنيديرايت فوليوبتاتي بوسكايسيوم كابرياس كيو دولوريمكيو.</p>
    </div>

    <!-- مكون الإيداع المنعزل -->
    <div id="deposit-component"></div>

    <script>
        // إنشاء مكون منعزل باستخدام Shadow DOM
        const depositComponent = document.getElementById('deposit-component');
        const shadowRoot = depositComponent.attachShadow({ mode: 'open' });
        
        // إضافة الأنماط والعناصر داخل Shadow DOM
        shadowRoot.innerHTML = `
            <style>
                :host {
                    --primary-color: #1a2a6c;
                    --secondary-color: #2a4d8e;
                    --accent-color: #ff6b6b;
                    --success-color: #00b09b;
                    --text-color: #333;
                    --light-bg: #f8f9fa;
                    --shadow: 0 5px 20px rgba(0,0,0,0.2);
                    --transition: all 0.3s ease;
                }
                
                .deposit-btn {
                    position: fixed;
                    bottom: 30px;
                    left: 30px;
                    z-index: 1000;
                    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
                    color: white;
                    padding: 16px 36px;
                    border-radius: 50px;
                    font-size: 1.1rem;
                    font-weight: 600;
                    border: none;
                    cursor: pointer;
                    box-shadow: var(--shadow);
                    transition: var(--transition);
                    display: flex;
                    align-items: center;
                    gap: 10px;
                    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
                }
                
                .deposit-btn:hover {
                    transform: translateY(-5px);
                    box-shadow: 0 8px 25px rgba(26, 42, 108, 0.4);
                }
                
                .deposit-btn:active {
                    transform: translateY(0);
                }
                
                .modal-overlay {
                    position: fixed;
                    top: 0;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    background: rgba(0,0,0,0.8);
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    z-index: 2000;
                    opacity: 0;
                    visibility: hidden;
                    transition: var(--transition);
                }
                
                .modal-overlay.active {
                    opacity: 1;
                    visibility: visible;
                }
                
                .modal {
                    background: white;
                    border-radius: 20px;
                    width: 95%;
                    max-width: 600px;
                    max-height: 90vh;
                    overflow-y: auto;
                    box-shadow: 0 25px 50px rgba(0,0,0,0.4);
                    transform: translateY(30px);
                    transition: var(--transition);
                    position: relative;
                }
                
                .modal-overlay.active .modal {
                    transform: translateY(0);
                }
                
                .modal-header {
                    background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
                    color: white;
                    padding: 25px;
                    border-radius: 20px 20px 0 0;
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    position: sticky;
                    top: 0;
                    z-index: 10;
                    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
                }
                
                .modal-header h2 {
                    font-size: 1.8rem;
                    display: flex;
                    align-items: center;
                    gap: 12px;
                    margin: 0;
                }
                
                .close-btn {
                    background: rgba(255,255,255,0.2);
                    color: white;
                    border: none;
                    width: 40px;
                    height: 40px;
                    border-radius: 50%;
                    font-size: 1.5rem;
                    cursor: pointer;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    transition: var(--transition);
                }
                
                .close-btn:hover {
                    background: rgba(255,255,255,0.3);
                    transform: rotate(90deg);
                }
                
                .modal-content {
                    padding: 30px;
                    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
                }
                
                .steps {
                    counter-reset: step-counter;
                }
                
                .step {
                    display: flex;
                    margin-bottom: 30px;
                    padding-bottom: 30px;
                    border-bottom: 1px dashed #e0e0e0;
                    position: relative;
                }
                
                .step:last-child {
                    margin-bottom: 0;
                    padding-bottom: 0;
                    border-bottom: none;
                }
                
                .step-number {
                    min-width: 40px;
                    height: 40px;
                    background: linear-gradient(to right, var(--accent-color), #ff8e53);
                    color: white;
                    border-radius: 50%;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    font-weight: bold;
                    font-size: 1.2rem;
                    margin-left: 15px;
                    flex-shrink: 0;
                }
                
                .step-content {
                    flex: 1;
                    text-align: right;
                }
                
                .step-title {
                    color: var(--primary-color);
                    font-size: 1.4rem;
                    margin-bottom: 15px;
                    display: flex;
                    align-items: center;
                    gap: 10px;
                }
                
                .step-title i {
                    color: var(--accent-color);
                }
                
                .step-details {
                    background: var(--light-bg);
                    border-radius: 12px;
                    padding: 20px;
                    margin-top: 15px;
                    box-shadow: 0 3px 10px rgba(0,0,0,0.05);
                }
                
                .step-details ul {
                    list-style-type: none;
                    padding: 0;
                }
                
                .step-details li {
                    margin-bottom: 12px;
                    padding-right: 25px;
                    position: relative;
                    font-size: 1.1rem;
                    color: var(--text-color);
                    line-height: 1.7;
                }
                
                .step-details li:before {
                    content: "•";
                    color: var(--accent-color);
                    font-size: 1.8rem;
                    position: absolute;
                    right: 0;
                    top: -7px;
                }
                
                .success {
                    text-align: center;
                    padding: 25px;
                    background: linear-gradient(to right, var(--success-color), #96c93d);
                    color: white;
                    border-radius: 0 0 20px 20px;
                    font-size: 1.4rem;
                    font-weight: bold;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    gap: 15px;
                    margin-top: 20px;
                }
                
                @media (max-width: 768px) {
                    .deposit-btn {
                        font-size: 1rem;
                        padding: 14px 30px;
                        left: 15px;
                        bottom: 15px;
                    }
                    
                    .modal-header h2 {
                        font-size: 1.4rem;
                    }
                    
                    .modal-content {
                        padding: 20px;
                    }
                    
                    .step-title {
                        font-size: 1.2rem;
                    }
                    
                    .step-details li {
                        font-size: 1rem;
                    }
                }
            </style>
            
            <button class="deposit-btn" id="showDepositSteps">
                <i class="fas fa-wallet"></i> عرض خطوات الإيداع
            </button>
            
            <div class="modal-overlay" id="depositModal">
                <div class="modal">
                    <div class="modal-header">
                        <h2><i class="fas fa-wallet"></i> خطوات إيداع الأموال في RannForex</h2>
                        <button class="close-btn" id="closeModal">&times;</button>
                    </div>
                    
                    <div class="modal-content">
                        <div class="steps">
                            <div class="step">
                                <div class="step-number">1</div>
                                <div class="step-content">
                                    <h3 class="step-title"><i class="fas fa-mouse-pointer"></i> الإيداع</h3>
                                    <div class="step-details">
                                        <ul>
                                            <li>اضغط على الثلاث شخط في موقع RannForex أعلى يمين الشاشة</li>
                                            <li>اختر Deposit</li>
                                            <li>اختر طريقة الإيداع: Crypto</li>
                                            <li>اختر حساب التداول</li>
                                            <li>اضغط على Continue</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="step">
                                <div class="step-number">2</div>
                                <div class="step-content">
                                    <h3 class="step-title"><i class="fas fa-exchange-alt"></i> تفاصيل التحويل</h3>
                                    <div class="step-details">
                                        <ul>
                                            <li>أدخل المبلغ في الفراغ الأول</li>
                                            <li>اختر USD</li>
                                            <li>اضغط على Continue</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="step">
                                <div class="step-number">3</div>
                                <div class="step-content">
                                    <h3 class="step-title"><i class="fas fa-shield-alt"></i> رمز التحقق (2FA)</h3>
                                    <div class="step-details">
                                        <ul>
                                            <li>افتح تطبيق Google Authenticator</li>
                                            <li>انسخ الكود المولد لحساب RannForex</li>
                                            <li>أدخل الكود في الفراغ المخصص</li>
                                            <li>اضغط على Continue</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="step">
                                <div class="step-number">4</div>
                                <div class="step-content">
                                    <h3 class="step-title"><i class="fab fa-bitcoin"></i> اختر TetherUS - USDT</h3>
                                    <div class="step-details">
                                        <ul>
                                            <li>اختر BUSD-T-USD (USDT)</li>
                                            <li>انسخ العنوان المقدم وهو عنوان bep20</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="step">
                                <div class="step-number">5</div>
                                <div class="step-content">
                                    <h3 class="step-title"><i class="fas fa-paper-plane"></i> إرسال من Cwallet</h3>
                                    <div class="step-details">
                                        <ul>
                                            <li>اختر USDT</li>
                                            <li>اختر شبكة BEP20</li>
                                            <li>أدخل المبلغ بالدولار</li>
                                            <li>الصق العنوان المنسوخ من RannForex</li>
                                            <li>اضغط على Send</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="success">
                        <i class="fas fa-check-circle"></i> تم الإيداع بنجاح!
                    </div>
                </div>
            </div>
        `;
        
        // إضافة سكريبت التحكم داخل Shadow DOM
        const script = document.createElement('script');
        script.textContent = `
            document.addEventListener('DOMContentLoaded', function() {
                const showBtn = this.shadowRoot.getElementById('showDepositSteps');
                const closeBtn = this.shadowRoot.getElementById('closeModal');
                const modal = this.shadowRoot.getElementById('depositModal');
                
                showBtn.addEventListener('click', function() {
                    modal.classList.add('active');
                    document.body.style.overflow = 'hidden';
                });
                
                closeBtn.addEventListener('click', function() {
                    modal.classList.remove('active');
                    document.body.style.overflow = 'auto';
                });
                
                modal.addEventListener('click', function(e) {
                    if (e.target === modal) {
                        modal.classList.remove('active');
                        document.body.style.overflow = 'auto';
                    }
                });
            });
        `;
        shadowRoot.appendChild(script);
    </script>
</body>
</html>


