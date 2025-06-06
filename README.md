
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
            --border-radius: 8px;        /* نصف قطر الحواف */
            --box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* ظل العناصر */
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
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
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
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* تنسيق الشعار */
        .logo h1 {
            font-size: 2.5rem;
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
            font-weight: 600;
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

        /* شبكة بطاقات المميزات */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }

        /* بطاقة ميزة */
        .feature-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 25px;
            text-align: center;
            box-shadow: var(--box-shadow);
            transition: var(--transition);
            border-bottom: 3px solid transparent;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            border-bottom: 3px solid var(--accent-color);
        }

        .feature-card i {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 15px;
        }

        .feature-card h4 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--primary-color);
        }

        /* معلومات الاسبريد */
        .spread-info {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 30px;
            text-align: center;
            box-shadow: var(--box-shadow);
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
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }

        /* بطاقة تقييم */
        .rating-card {
            background-color: white;
            border-radius: var(--border-radius);
            padding: 25px;
            text-align: center;
            box-shadow: var(--box-shadow);
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-height: 200px;
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
            box-shadow: var(--box-shadow);
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
            box-shadow: var(--box-shadow);
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
            box-shadow: var(--box-shadow);
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

        /* أيقونات وسائل التواصل الاجتماعي */
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-icon {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: var(--primary-color);
            color: white;
            font-size: 1.5rem;
            transition: var(--transition);
        }

        .social-icon:hover {
            transform: translateY(-5px) scale(1.1);
        }

        /* ألوان مخصصة لكل منصة اجتماعية */
        .social-icon:nth-child(1) {
            background-color: #1877f2; /* فيسبوك */
        }

        .social-icon:nth-child(2) {
            background-color: #e1306c; /* انستغرام */
        }

        .social-icon:nth-child(3) {
            background-color: #000000; /* تويتر (اكس) */
        }

        .social-icon:nth-child(4) {
            background-color: #25d366; /* واتساب */
        }

        .social-icon:nth-child(5) {
            background-color: #0088cc; /* تلجرام */
        }

        /* ===== تنسيقات الفوتر ===== */
        .footer {
            background-color: var(--primary-color);
            color: white;
            padding: 20px 0;
            text-align: center;
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
            .features-grid, .ratings-grid, .apps-grid, .signals-grid, .courses-grid {
                grid-template-columns: repeat(auto-fill, minmax(100%, 1fr));
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
                padding: 20px;
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
                    <li><a href="#section7">تواصل</a></li>
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
                <h2 class="section-title" >لقد قمت بإضافة كل شيء تحتاجه في مجال التداول  إلى هذا الموقع لن تحتاج إلى شيء آخر </h2>
                <div class="register-card">
                    <h3>سجل الآن في Rannforex</h3>
                    <p>ابدأ رحلتك في عالم التداول مع شركة وساطة مالية موثوقة</p>
                    <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="btn btn-primary" target="_blank">
                        <i class="fas fa-user-plus"></i> سجل الآن
                    </a>
                </div>

                <div class="features">
                    
                    
                    
                    <h3>مميزات الشركة</h3>
                    <div class="features-grid">
                        <div class="feature-card">
                            <i class="fas fa-money-bill-wave"></i>
                            <h4>أقل إيداع</h4>
                            <p>10$ خلال 30 ثانية</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-hand-holding-usd"></i>
                            <h4>أقل سحب</h4>
                            <p>10$ خلال 30 ثانية</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-percentage"></i>
                            <h4>عمولة قليلة جداً</h4>
                            <p>أفضل العمولات في السوق</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-chart-line"></i>
                            <h4>اسبريد</h4>
                            <p>0.3~1.2</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-balance-scale"></i>
                            <h4>رافعة مالية</h4>
                            <p>1:500</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-shield-alt"></i>
                            <h4>تداول آمن</h4>
                            <p>على جميع أزواج الفوريكس والمعادن والنفط والمؤشرات والعملات المشفرة</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-users"></i>
                            <h4>أنواع الحسابات</h4>
                            <p>ميتا تريدر 5 حقيقي وبدون عمولة وكريبتو وحساب IB ويدعم الحسابات المدارة PAMM</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-tachometer-alt"></i>
                            <h4>انزلاق منخفض</h4>
                            <p>تنفيذ فوري للصفقات</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-star"></i>
                            <h4>تقييم ممتاز</h4>
                            <p>على مواقع Trust Pilot & MyFXBook & WikiFX & Forex Peace Army</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-lock"></i>
                            <h4>أمان عالي</h4>
                            <p>بسبب المصادقة الثنائية 2FA</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-passport"></i>
                            <h4>توثيق سهل</h4>
                            <p>من سورية أو أي دولة أخرى</p>
                        </div>
                        <div class="feature-card">
                            <i class="fas fa-book"></i>
                            <h4>نموذج A Book</h4>
                            <p>من أفضل مزودي السيولة</p>
                        </div>
                    </div>
                </div>

                <div class="spread-info">
                    <h3>اطلع على الاسبريد المتوسط اليومي</h3>
                    <a href="https://rannforex.com/en/trading/quotesonline/" class="btn btn-secondary" target="_blank">
                        <i class="fas fa-chart-bar"></i> عرض الاسبريد
                    </a>
                </div>
            </div>
        </section>
        
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
            padding: 20px;
        }
        .accordion {
            background-color: #007bff;
            color: white;
            cursor: pointer;
            padding: 15px;
            width: 100%;
            border: none;
            text-align: right;
            outline: none;
            font-size: 18px;
            transition: background-color 0.3s;
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
            margin-bottom: 10px;
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
</body>
</html>
        

        <!-- القسم الثاني: تقييمات الشركة -->
        <section id="section2" class="section">
            <div class="container">
                <h2 class="section-title">تقييمات الشركة</h2>
                <div class="ratings-grid">
                    <div class="rating-card">
                        <div class="rating-logo">Trustpilot</div>
                        <a href="https://fr.trustpilot.com/review/rannforex.com" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> عرض التقييمات
                        </a>
                    </div>
                    <div class="rating-card">
                        <div class="rating-logo">WikiFX</div>
                        <a href="https://www.wikifx.com/en/dealer/1141850612.html" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> عرض التقييمات
                        </a>
                    </div>
                    <div class="rating-card">
                        <div class="rating-logo">MyFXBook</div>
                        <a href="https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> عرض التقييمات
                        </a>
                    </div>
                    <div class="rating-card">
                        <div class="rating-logo">Forex Peace Army</div>
                        <a href="https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review" class="btn btn-outline" target="_blank">
                            <i class="fas fa-external-link-alt"></i> عرض التقييمات
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- القسم الثالث: تطبيقات يجب تحميلها للبدء بالتداول -->
        <section id="section3" class="section">
            <div class="container">
                <h2 class="section-title">تطبيقات يجب تحميلها للبدء بالتداول</h2>
                <div class="apps-grid">
                    <div class="app-card">
                        <div class="app-icon">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <h3>منصة ميتا تريدر 5</h3>
                        <p>المنصة الموثوقة الأفضل في مجال التداول في جميع الأسواق</p>
                        <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" class="btn btn-app" target="_blank">
                            <i class="fab fa-google-play"></i> تحميل التطبيق
                        </a>
                    </div>
                    <div class="app-card">
                        <div class="app-icon">
                            <i class="fas fa-wallet"></i>
                        </div>
                        <h3>المحفظة الإلكترونية</h3>
                        <p>محفظة إلكترونية آمنة لإدارة أموالك</p>
                        <a href="https://cwallet.com/referral/DvY6dZtS" class="btn btn-app" target="_blank">
                            <i class="fas fa-download"></i> تحميل التطبيق
                        </a>
                    </div>
                    <div class="app-card">
                        <div class="app-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3>تطبيق المصادقة الثنائية</h3>
                        <p>يلزم من أجل توثيق الحساب وتوثيق عمليات السحب والإيداع</p>
                        <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" class="btn btn-app" target="_blank">
                            <i class="fab fa-google-play"></i> تحميل التطبيق
                </a>
                    </div>
                 <div class="app-card">
                <div class="app-icon">
                    <i class="fas fa-chart-bar"></i>
                </div>
                <h3>منصة TradingView</h3>
                <p>منصة متقدمة للتحليل الفني ومتابعة الأسواق المالية العالمية</p>
                <a href="https://play.google.com/store/apps/details?id=com.tradingview.tradingviewapp" class="btn btn-app" target="_blank">
                    <i class="fab fa-google-play"></i> تحميل التطبيق
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
                    <div class="channel-card main-channel">
                        <i class="fab fa-telegram"></i>
                        <h3>قناتنا</h3>
                        <a href="https://t.me/tradewithalimahmoud" class="btn btn-telegram" target="_blank">
                            الانضمام للقناة
                        </a>
                    </div>
                    
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



        <!-- القسم السابع: وسائل التواصل -->
        <section id="section7" class="section">
            <div class="container">
                <h2 class="section-title">تواصل معنا</h2>
                <div class="contact-info">
                    <p class="contact-phone">
                        <i class="fas fa-phone"></i> +963934598967
                    </p>
                    <p class="contact-email">
                        <i class="fas fa-envelope"></i> alimahmoud001a@gmail.com
                    </p>
                </div>
                
                <div class="social-icons">
                    <a href="https://www.facebook.com/alimahmoud001" target="_blank" class="social-icon">
                        <i class="fab fa-facebook-f"></i>
                    </a>
                    <a href="https://www.instagram.com/alimahmoud001a?igsh=YzljYTk1ODg3Zg==" target="_blank" class="social-icon">
                        <i class="fab fa-instagram"></i>
                    </a>
                    <a href="https://x.com/en_alimahmoud" target="_blank" class="social-icon">
                        <i class="fab fa-x-twitter"></i>
                    </a>
                    <a href="https://wa.me/qr/AFVVUP3Z46UYM1" target="_blank" class="social-icon">
                        <i class="fab fa-whatsapp"></i>
                    </a>
                    <a href="https://t.me/Alimahmoud001" target="_blank" class="social-icon">
                        <i class="fab fa-telegram"></i>
                    </a>
                </div>
                
            </div>
        </section>
    </main>

    <!-- القسم السفلي (الفوتر) -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2025 Rannforex - جميع الحقوق محفوظة</p>
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
    </script>
</body>
</html>);
            

+++++++++++
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نافذة دردشة للموقع</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        /* زر فتح الدردشة */
        .chat-toggle-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(to right, #1E90FF, #00BFFF);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            z-index: 999;
            transition: all 0.3s ease;
        }

        .chat-toggle-btn:hover {
            transform: scale(1.1) rotate(10deg);
        }

        .chat-toggle-btn i {
            font-size: 24px;
        }

        /* نافذة الدردشة */
        .chat-container {
            position: fixed;
            bottom: 100px;
            right: 30px;
            width: 350px;
            max-height: 80vh;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            z-index: 1000;
            transform: translateY(20px);
            opacity: 0;
            transition: all 0.4s ease;
        }

        .chat-container.active {
            transform: translateY(0);
            opacity: 1;
        }

        /* رأس نافذة الدردشة */
        .chat-header {
            background: linear-gradient(to right, #1E90FF, #00BFFF);
            color: white;
            padding: 15px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .chat-header h2 {
            font-size: 18px;
            font-weight: 600;
        }

        .close-btn {
            background: none;
            border: none;
            color: white;
            font-size: 18px;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .close-btn:hover {
            transform: rotate(90deg);
        }

        /* منطقة الرسائل */
        .chat-messages {
            flex: 1;
            padding: 15px;
            overflow-y: auto;
            background: #F5F7FA;
            max-height: 250px;
            scroll-behavior: smooth;
        }

        .message {
            max-width: 80%;
            padding: 10px 12px;
            border-radius: 12px;
            line-height: 1.5;
            font-size: 14px;
            margin-bottom: 10px;
            animation: fadeIn 0.3s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .message.bot {
            background: #E6F0FA;
            color: #333;
            align-self: flex-start;
            border-bottom-left-radius: 4px;
        }

        .message.user {
            background: #1E90FF;
            color: white;
            align-self: flex-end;
            border-bottom-right-radius: 4px;
        }

        .message-info {
            font-size: 10px;
            margin-top: 5px;
            opacity: 0.7;
        }

        /* منطقة الإدخال */
        .chat-input {
            padding: 15px;
            border-top: 1px solid #E0E0E0;
            background: white;
        }

        .input-group {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        input {
            width: 100%;
            padding: 10px;
            border: 1px solid #D0D7DE;
            border-radius: 8px;
            font-size: 14px;
            transition: border-color 0.3s;
        }

        input:focus {
            outline: none;
            border-color: #1E90FF;
            box-shadow: 0 0 0 2px rgba(30, 144, 255, 0.2);
        }

        button {
            background: linear-gradient(to right, #1E90FF, #00BFFF);
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(30, 144, 255, 0.4);
        }

        /* مفتاح التواجد */
        .toggle-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-top: 10px;
        }

        .toggle-label {
            font-weight: 500;
            color: #555;
            font-size: 14px;
        }

        .toggle {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 24px;
        }

        .toggle input {
            opacity: 0;
            width: 0;
            height: 0;
        }

        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            transition: 0.4s;
            border-radius: 24px;
        }

        .slider:before {
            position: absolute;
            content: "";
            height: 16px;
            width: 16px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: 0.4s;
            border-radius: 50%;
        }

        input:checked + .slider {
            background: linear-gradient(to right, #1E90FF, #00BFFF);
        }

        input:checked + .slider:before {
            transform: translateX(26px);
        }

        /* الإخطارات */
        .notification {
            position: fixed;
            bottom: 170px;
            right: 30px;
            padding: 10px 15px;
            background: #1E90FF;
            color: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transform: translateX(120%);
            transition: transform 0.4s ease;
            z-index: 1000;
            max-width: 300px;
            font-size: 14px;
        }

        .notification.show {
            transform: translateX(0);
        }

        .notification.error {
            background: #FF4D4D;
        }

        /* التصميم للشاشات الصغيرة */
        @media (max-width: 500px) {
            .chat-container {
                width: 90%;
                right: 5%;
                bottom: 80px;
            }

            .chat-toggle-btn {
                right: 20px;
                bottom: 20px;
            }

            .notification {
                right: 5%;
                bottom: 150px;
            }
        }
    </style>
</head>
<body>
    <!-- زر فتح الدردشة -->
    <div class="chat-toggle-btn" id="chatToggle">
        <i class="fas fa-comment-dots"></i>
    </div>

    <!-- نافذة الدردشة -->
    <div class="chat-container" id="chatContainer">
        <div class="chat-header">
            <h2>دردشة العملاء</h2>
            <button class="close-btn" id="closeBtn">
                <i class="fas fa-times"></i>
            </button>
        </div>

        <div class="chat-messages" id="chatMessages">
            <div class="message bot">
                مرحبًا! يرجى إدخال اسمك وبريدك الإلكتروني للتواصل معنا.
                <div class="message-info">النظام • الآن</div>
            </div>
        </div>

        <div class="chat-input">
            <div class="input-group">
                <input type="text" id="nameInput" placeholder="الاسم والكنية" required>
                <input type="email" id="emailInput" placeholder="بريدك الإلكتروني" required>
                <button id="sendButton">
                    <i class="fas fa-paper-plane"></i>
                    إرسال
                </button>
            </div>

            <div class="toggle-container">
                <span class="toggle-label">حالة المشرف:</span>
                <label class="toggle">
                    <input type="checkbox" id="onlineToggle" checked>
                    <span class="slider"></span>
                </label>
            </div>
        </div>
    </div>

    <!-- الإخطارات -->
    <div class="notification" id="notification">تم إرسال بياناتك بنجاح!</div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const chatToggle = document.getElementById('chatToggle');
            const chatContainer = document.getElementById('chatContainer');
            const closeBtn = document.getElementById('closeBtn');
            const nameInput = document.getElementById('nameInput');
            const emailInput = document.getElementById('emailInput');
            const sendButton = document.getElementById('sendButton');
            const chatMessages = document.getElementById('chatMessages');
            const onlineToggle = document.getElementById('onlineToggle');
            const notification = document.getElementById('notification');

            // فتح وإغلاق الدردشة
            chatToggle.addEventListener('click', () => {
                chatContainer.classList.toggle('active');
            });

            closeBtn.addEventListener('click', () => {
                chatContainer.classList.remove('active');
            });

            // تحويل حالة التواجد
            onlineToggle.addEventListener('change', () => {
                if (onlineToggle.checked) {
                    showNotification('حالة المشرف: متواجد الآن');
                } else {
                    showNotification('حالة المشرف: غير متواجد حالياً', 'error');
                }
            });

            // إرسال البيانات
            sendButton.addEventListener('click', () => {
                const name = nameInput.value.trim();
                const email = emailInput.value.trim();

                if (name === '') {
                    showNotification('يرجى إدخال الاسم والكنية', 'error');
                    return;
                }

                if (!validateEmail(email)) {
                    showNotification('يرجى إدخال بريد إلكتروني صحيح', 'error');
                    return;
                }

                // محاكاة إرسال البيانات إلى بريد المشرف
                sendToAdminEmail(name, email);

                // إضافة رسالة المستخدم
                addUserMessage(name, email);

                // رد تلقائي بناءً على حالة التواجد
                setTimeout(() => {
                    if (onlineToggle.checked) {
                        addBotMessage('شكرًا لتواصلك! سأرد عليك الآن.');
                    } else {
                        addBotMessage('عملاؤنا غير متوفرين هذه اللحظة، سيتم الرد خلال دقائق قليلة، نرجو الانتظار.');
                    }
                }, 1000);

                // مسح الحقول
                nameInput.value = '';
                emailInput.value = '';
            });

            // إرسال بالضغط على Enter
            [nameInput, emailInput].forEach(input => {
                input.addEventListener('keypress', (e) => {
                    if (e.key === 'Enter') {
                        e.preventDefault();
                        sendButton.click();
                    }
                });
            });

            // وظائف مساعدة
            function validateEmail(email) {
                const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                return re.test(email);
            }

            function addUserMessage(name, email) {
                const messageDiv = document.createElement('div');
                messageDiv.classList.add('message', 'user');
                messageDiv.innerHTML = `الاسم: ${name}<br>البريد: ${email}<div class="message-info">أنت • ${getCurrentTime()}</div>`;
                chatMessages.appendChild(messageDiv);
                scrollToBottom();
            }

            function addBotMessage(text) {
                const messageDiv = document.createElement('div');
                messageDiv.classList.add('message', 'bot');
                messageDiv.innerHTML = `${text}<div class="message-info">المشرف • ${getCurrentTime()}</div>`;
                chatMessages.appendChild(messageDiv);
                scrollToBottom();
            }

            function scrollToBottom() {
                chatMessages.scrollTo({
                    top: chatMessages.scrollHeight,
                    behavior: 'smooth'
                });
            }

            function getCurrentTime() {
                const now = new Date();
                return `${now.getHours()}:${now.getMinutes().toString().padStart(2, '0')}`;
            }

            function sendToAdminEmail(name, email) {
                // محاكاة إرسال البريد الإلكتروني
                console.log('إرسال إخطار بالبريد الإلكتروني إلى المشرف:');
                console.log(`الاسم: ${name}`);
                console.log(`البريد الإلكتروني: ${email}`);
                showNotification('تم إرسال بياناتك إلى المشرف!');
            }

            function showNotification(text, type = 'success') {
                notification.textContent = text;
                notification.className = `notification show ${type === 'error' ? 'error' : ''}`;
                setTimeout(() => {
                    notification.classList.remove('show');
                }, 3000);
            }
        });
    </script>
</body>
</html>



<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>دردشة العملاء</title>
<style>
/* زر الدردشة */
#chat-btn {
  position: fixed;
  bottom: 20px;
  left: 20px;
  background-color: #007BFF;
  color: #fff;
  border: none;
  padding: 15px 20px;
  border-radius: 50px;
  cursor: pointer;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: background-color 0.3s;
  font-size: 16px;
}

#chat-btn:hover {
  background-color: #0056b3;
}

/* نافذة الدردشة */
#chat-window {
  display: none;
  position: fixed;
  bottom: 80px;
  left: 20px;
  width: 300px;
  background-color: #ffffff;
  border: 2px solid #007BFF;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
  z-index: 1000;
}

#chat-header {
  background-color: #007BFF;
  color: #ffffff;
  padding: 10px;
  border-radius: 10px 10px 0 0;
  font-size: 18px;
}

#chat-body {
  padding: 15px;
}

#chat-body input[type="text"],
#chat-body input[type="email"] {
  width: 100%;
  padding: 8px;
  margin: 8px 0;
  border: 1px solid #ccc;
  border-radius: 5px;
}

#chat-body button {
  background-color: #007BFF;
  color: #fff;
  border: none;
  padding: 10px;
  width: 100%;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 10px;
}

#chat-body button:hover {
  background-color: #0056b3;
}
</style>
</head>
<body>

<!-- زر فتح الدردشة -->
<button id="chat-btn">💬 دردش معنا</button>

<!-- نافذة الدردشة -->
<div id="chat-window">
  <div id="chat-header">الدردشة مع العملاء</div>
  <div id="chat-body">
    <input type="text" id="name" placeholder="الاسم والكنية" required>
    <input type="email" id="email" placeholder="البريد الإلكتروني" required>
    <button onclick="sendMessage()">إرسال</button>
    <div id="response" style="margin-top:10px; color:#007BFF;"></div>
  </div>
</div>

<script>
  // فتح وإغلاق نافذة الدردشة
  document.getElementById('chat-btn').onclick = function() {
    let chatWindow = document.getElementById('chat-window');
    chatWindow.style.display = (chatWindow.style.display === 'none' || chatWindow.style.display === '') ? 'block' : 'none';
  };

  // إرسال البيانات عبر AJAX إلى PHP
  function sendMessage() {
    let name = document.getElementById('name').value.trim();
    let email = document.getElementById('email').value.trim();
    let responseDiv = document.getElementById('response');

    if (name === '' || email === '') {
      responseDiv.textContent = 'يرجى ملء جميع الحقول.';
      return;
    }

    let formData = new FormData();
    formData.append('name', name);
    formData.append('email', email);

    fetch('chat_handler.php', { // اسم ملف PHP لمعالجة البيانات
      method: 'POST',
      body: formData
    })
    .then(response => response.text())
    .then(data => {
      responseDiv.textContent = data;
    })
    .catch(error => {
      console.error(error);
      responseDiv.textContent = 'حدث خطأ! يرجى المحاولة لاحقًا.';
    });
  }
</script>

</body>
</html>
