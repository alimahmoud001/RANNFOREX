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
                <h2 class="section-title" >هذه فرصة عمل جيدة للجميع تحقيق أرباح جيدة ابدأ التداول هنا نقبل السوريين أو اي بلد آخر لقد قمت بإضافة كل شيء تحتاجه إلى هذا الموقع من قنوات يوتيوب تعليمية وقنوات إشارات مجانية بالإضافة إلى قناتي على تلجرام</h2>
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
 ====
 
    <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نظام إدارة الصور</title>
    <style>
        :root {
            --primary: #4361ee;
            --secondary: #3f37c9;
            --success: #4cc9f0;
            --light: #f8f9fa;
            --dark: #212529;
            --gray: #6c757d;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 30px 0;
            margin-bottom: 30px;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .app-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 30px;
        }
        
        @media (min-width: 992px) {
            .app-container {
                grid-template-columns: 1fr 2fr;
            }
        }
        
        .upload-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .gallery-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--success);
            display: flex;
            align-items: center;
        }
        
        .section-title i {
            margin-left: 10px;
        }
        
        .upload-area {
            border: 3px dashed rgba(255, 255, 255, 0.4);
            border-radius: 15px;
            padding: 40px 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 25px;
            position: relative;
        }
        
        .upload-area:hover {
            background: rgba(255, 255, 255, 0.15);
        }
        
        .upload-icon {
            font-size: 4rem;
            margin-bottom: 15px;
            color: var(--success);
        }
        
        .upload-text {
            font-size: 1.3rem;
            margin-bottom: 15px;
        }
        
        .browse-btn {
            background: var(--success);
            border: none;
            color: var(--dark);
            padding: 12px 30px;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            display: inline-block;
            margin-top: 10px;
        }
        
        .browse-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        input[type="file"] {
            display: none;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }
        
        .form-control {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.15);
            color: white;
            font-size: 1.1rem;
            outline: none;
        }
        
        .form-control::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }
        
        .btn {
            background: linear-gradient(to right, #00b09b, #96c93d);
            border: none;
            color: white;
            padding: 15px 0;
            font-size: 1.2rem;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
            font-weight: 600;
            margin-top: 10px;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .preview-container {
            display: none;
            margin: 25px 0;
            text-align: center;
        }
        
        #imagePreview {
            max-width: 100%;
            max-height: 250px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .image-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .image-card:hover {
            transform: translateY(-10px);
        }
        
        .card-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            display: block;
        }
        
        .card-body {
            padding: 15px;
        }
        
        .card-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .card-date {
            font-size: 0.9rem;
            color: var(--success);
            margin-bottom: 15px;
        }
        
        .card-actions {
            display: flex;
            justify-content: space-between;
        }
        
        .action-btn {
            padding: 8px 15px;
            border-radius: 50px;
            border: none;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .download-btn {
            background: var(--success);
            color: var(--dark);
        }
        
        .delete-btn {
            background: #e63946;
            color: white;
        }
        
        .action-btn:hover {
            opacity: 0.9;
            transform: scale(1.05);
        }
        
        .empty-gallery {
            text-align: center;
            padding: 40px 20px;
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.7);
        }
        
        .empty-gallery i {
            font-size: 3rem;
            display: block;
            margin-bottom: 20px;
            color: var(--success);
        }
        
        .status-message {
            padding: 15px;
            border-radius: 10px;
            margin: 20px 0;
            text-align: center;
            display: none;
        }
        
        .success-message {
            background: rgba(76, 201, 240, 0.3);
            border: 1px solid var(--success);
        }
        
        .error-message {
            background: rgba(230, 57, 70, 0.3);
            border: 1px solid #e63946;
        }
        
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.7);
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>نظام إدارة الصور</h1>
            <p class="subtitle">حمّل صورك من هاتفك، احفظها في الموقع، وادرها بسهولة</p>
        </header>
        
        <div class="app-container">
            <section class="upload-section">
                <h2 class="section-title">
                    <i>📤</i> رفع صورة جديدة
                </h2>
                
                <div class="upload-area" id="uploadArea">
                    <div class="upload-icon">📁</div>
                    <div class="upload-text">اضغط لاختيار صورة من هاتفك</div>
                    <button class="browse-btn">تصفح معرض الصور</button>
                    <input type="file" id="imageInput" accept="image/*">
                </div>
                
                <div id="uploadStatus" class="status-message"></div>
                
                <div class="preview-container" id="previewContainer">
                    <img id="imagePreview" alt="معاينة الصورة">
                </div>
                
                <div class="form-group">
                    <label for="imageTitle">عنوان الصورة:</label>
                    <input type="text" class="form-control" id="imageTitle" placeholder="أدخل عنوانًا وصفى للصورة">
                </div>
                
                <div class="form-group">
                    <label for="imageDescription">وصف الصورة (اختياري):</label>
                    <textarea class="form-control" id="imageDescription" rows="3" placeholder="أضف وصفًا للصورة"></textarea>
                </div>
                
                <button class="btn" id="saveBtn">حفظ الصورة في الموقع</button>
            </section>
            
            <section class="gallery-section">
                <h2 class="section-title">
                    <i>🖼️</i> معرض الصور المحفوظة
                </h2>
                
                <div id="galleryStatus" class="status-message"></div>
                
                <div class="gallery-container" id="imageGallery">
                    <!-- سيتم ملؤها بالصور المخزنة -->
                    <div class="empty-gallery">
                        <i>📷</i>
                        <p>لا توجد صور مخزنة بعد</p>
                        <p>قم برفع صورة لتبدأ</p>
                    </div>
                </div>
            </section>
        </div>
        
        <footer>
            <p>تم التطوير خصيصًا للعمل على أجهزة الهاتف المحمول | نظام إدارة الصور © 2023</p>
        </footer>
    </div>

    <script>
        // عناصر DOM
        const uploadArea = document.getElementById('uploadArea');
        const imageInput = document.getElementById('imageInput');
        const imagePreview = document.getElementById('imagePreview');
        const previewContainer = document.getElementById('previewContainer');
        const imageTitle = document.getElementById('imageTitle');
        const imageDescription = document.getElementById('imageDescription');
        const saveBtn = document.getElementById('saveBtn');
        const imageGallery = document.getElementById('imageGallery');
        const uploadStatus = document.getElementById('uploadStatus');
        const galleryStatus = document.getElementById('galleryStatus');
        
        // متغيرات التطبيق
        let uploadedImage = null;
        let storedImages = JSON.parse(localStorage.getItem('savedImages')) || [];
        
        // تهيئة التطبيق
        function initApp() {
            renderGallery();
            setupEventListeners();
        }
        
        // إعداد مستمعي الأحداث
        function setupEventListeners() {
            // اختيار الصورة
            uploadArea.addEventListener('click', () => imageInput.click());
            imageInput.addEventListener('change', handleImageSelect);
            
            // حفظ الصورة
            saveBtn.addEventListener('click', saveImage);
        }
        
        // معالجة اختيار الصورة
        function handleImageSelect(e) {
            const file = e.target.files[0];
            
            if (!file) return;
            
            if (!file.type.match('image.*')) {
                showMessage(uploadStatus, 'الرجاء اختيار ملف صورة فقط', 'error');
                return;
            }
            
            uploadedImage = file;
            
            // عرض معاينة الصورة
            const reader = new FileReader();
            reader.onload = (e) => {
                imagePreview.src = e.target.result;
                previewContainer.style.display = 'block';
                
                // استخدام اسم الملف كعنوان افتراضي
                if (!imageTitle.value) {
                    const fileName = file.name.replace(/\.[^/.]+$/, "");
                    imageTitle.value = fileName;
                }
            };
            reader.readAsDataURL(file);
        }
        
        // حفظ الصورة في التخزين المحلي
        function saveImage() {
            if (!uploadedImage) {
                showMessage(uploadStatus, 'الرجاء اختيار صورة أولاً', 'error');
                return;
            }
            
            if (!imageTitle.value.trim()) {
                showMessage(uploadStatus, 'الرجاء إدخال عنوان للصورة', 'error');
                return;
            }
            
            const reader = new FileReader();
            reader.onload = (e) => {
                const imageData = {
                    id: Date.now(),
                    title: imageTitle.value,
                    description: imageDescription.value,
                    image: e.target.result,
                    date: new Date().toLocaleString(),
                    filename: uploadedImage.name
                };
                
                // إضافة الصورة إلى القائمة
                storedImages.push(imageData);
                
                // حفظ في التخزين المحلي
                localStorage.setItem('savedImages', JSON.stringify(storedImages));
                
                // إظهار رسالة النجاح
                showMessage(uploadStatus, 'تم حفظ الصورة في الموقع بنجاح!', 'success');
                
                // إعادة تعيين النموذج
                resetForm();
                
                // تحديث المعرض
                renderGallery();
            };
            
            reader.readAsDataURL(uploadedImage);
        }
        
        // عرض المعرض
        function renderGallery() {
            if (storedImages.length === 0) {
                imageGallery.innerHTML = `
                    <div class="empty-gallery">
                        <i>📷</i>
                        <p>لا توجد صور مخزنة بعد</p>
                        <p>قم برفع صورة لتبدأ</p>
                    </div>
                `;
                return;
            }
            
            imageGallery.innerHTML = storedImages.map(image => `
                <div class="image-card">
                    <img src="${image.image}" alt="${image.title}" class="card-image">
                    <div class="card-body">
                        <h3 class="card-title">${image.title}</h3>
                        <div class="card-date">${image.date}</div>
                        <div class="card-actions">
                            <button class="action-btn download-btn" onclick="downloadImage('${image.id}')">
                                تنزيل
                            </button>
                            <button class="action-btn delete-btn" onclick="deleteImage('${image.id}')">
                                حذف
                            </button>
                        </div>
                    </div>
                </div>
            `).join('');
        }
        
        // تنزيل الصورة
        function downloadImage(imageId) {
            const image = storedImages.find(img => img.id == imageId);
            if (!image) return;
            
            const link = document.createElement('a');
            link.href = image.image;
            
            // الحصول على امتداد الملف
            const fileExtension = image.filename.split('.').pop().toLowerCase();
            
            // استخدام عنوان الصورة كاسم الملف
            link.download = `${image.title}.${fileExtension}`;
            
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
            
            showMessage(galleryStatus, 'جاري تنزيل الصورة...', 'success');
            setTimeout(() => {
                galleryStatus.style.display = 'none';
            }, 2000);
        }
        
        // حذف الصورة
        function deleteImage(imageId) {
            if (confirm('هل أنت متأكد من رغبتك في حذف هذه الصورة؟')) {
                storedImages = storedImages.filter(img => img.id != imageId);
                localStorage.setItem('savedImages', JSON.stringify(storedImages));
                renderGallery();
                showMessage(galleryStatus, 'تم حذف الصورة بنجاح', 'success');
            }
        }
        
        // إعادة تعيين النموذج
        function resetForm() {
            imageInput.value = '';
            imageTitle.value = '';
            imageDescription.value = '';
            previewContainer.style.display = 'none';
            uploadedImage = null;
        }
        
        // عرض الرسائل
        function showMessage(element, message, type) {
            element.textContent = message;
            element.className = `status-message ${type}-message`;
            element.style.display = 'block';
            
            setTimeout(() => {
                element.style.display = 'none';
            }, 3000);
        }
        
        // بدء التطبيق
        initApp();
    </script>
</body>
</html>     
 ====
      <div class="register-card">
                    <h3>انضم إلى قناة الإشارات المجانية الخاصة بي</h3>
                    <p> هنا الإشارات مجانية وستبقى مجانية إلى الابد </p>
                    <a href=" https://t.me/tradewithalimahmoud  " class="btn btn-primary" target="_blank">
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
                            <i class="fab fa-google-play"></i> النصادقة الثنائية
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

<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بطاقة ميزات المتداول</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
      
        
        .card {
            background: rgba(255, 255, 255, 0.95);
            width: 100%;
            max-width: 100%;
            max-width: 900px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            border: 1px solid rgba(255, 255, 255, 0.3);
            position: relative;
        }
        
        .card-header {
            background: linear-gradient(90deg, #3498db, #2ecc71);
            color: white;
            padding: 25px 40px;
            text-align: center;
        }
        
        .card-header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            font-weight: 700;
            letter-spacing: -0.5px;
        }
        
        .card-header p {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .card-body {
            display: flex;
            flex-wrap: wrap;
            padding: 30px;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
            gap: 25px;
            width: 100%;
        }
        
        .feature {
            display: flex;
            align-items: flex-start;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 15px;
            transition: all 0.3s ease;
            border-left: 4px solid #3498db;
        }
        
        .feature:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            background: #fff;
            border-left: 4px solid #e74c3c;
        }
        
        .feature-icon {
            background: #3498db;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            margin-left: 15px;
            flex-shrink: 0;
        }
        
        .feature-content h3 {
            color: #2c3e50;
            margin-bottom: 8px;
            font-weight: 600;
        }
        
        .feature-content p {
            color: #7f8c8d;
            line-height: 1.6;
            font-size: 1.05rem;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            padding: 30px;
            background: #f8f9fa;
            border-top: 1px solid #eee;
        }
        
        .badge {
            background: #e74c3c;
            color: white;
            padding: 10px 25px;
            border-radius: 50px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 1rem;
        }
        
        .security-badge {
            background: #27ae60;
        }
        
        @media (max-width: 768px) {
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .card-header h1 {
                font-size: 2rem;
            }
            
            .feature {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .feature-icon {
                margin-left: 0;
                margin-bottom: 15px;
            }
        }
        
        .star {
            color: #f1c40f;
            margin-left: 3px;
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="card-header">
            <h1>مزايا التداول معنا</h1>
            <p>نقدم لك أفضل شروط التداول في السوق مع تنفيذ فوري وأعلى درجات الأمان</p>
        </div>
        
        <div class="card-body">
            <div class="features-grid">
                <div class="feature">
                    <div class="feature-icon">
                        <i class="fas fa-wallet"></i>
                    </div>
                    <div class="feature-content">
                        <h3>عمليات الإيداع والسحب</h3>
                        <p>
                            <span class="star">★</span> أقل إيداع 10$ خلال 30 ثانية فقط<br>
                            <span class="star">★</span> أقل سحب 10$ خلال 30 ثانية
                        </p>
                    </div>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">
                        <i class="fas fa-percentage"></i>
                    </div>
                    <div class="feature-content">
                        <h3>تكاليف تنافسية</h3>
                        <p>
                            <span class="star">★</span> عمولة قليلة جداً<br>
                            <span class="star">★</span> اسبريد منخفض 0.3~1.2
                        </p>
                    </div>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div class="feature-content">
                        <h3>شروط تداول ممتازة</h3>
                        <p>
                            <span class="star">★</span> رافعة مالية عالية 1:500<br>
                            <span class="star">★</span> انزلاق منخفض وتنفيذ فوري للصفقات
                        </p>
                    </div>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">
                        <i class="fas fa-globe"></i>
                    </div>
                    <div class="feature-content">
                        <h3>أدوات تداول متنوعة</h3>
                        <p>
                            <span class="star">★</span> تداول أمن على جميع أزواج الفوركس والمعادن والنفط<br>
                            <span class="star">★</span> المؤشرات والعملات المشفرة
                        </p>
                    </div>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">
                        <i class="fas fa-user-circle"></i>
                    </div>
                    <div class="feature-content">
                        <h3>أنواع الحسابات</h3>
                        <p>
                            <span class="star">★</span> أربع أنواع من الحسابات: ميتاتريدر 5 حقيقي<br>
                            <span class="star">★</span> بدون عمولة، كريبتو، وحساب IB<br>
                            <span class="star">★</span> يدعم الحسابات المدارة PAMM
                        </p>
                    </div>
                </div>
                
                <div class="feature">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <div class="feature-content">
                        <h3>الأمان والمصداقية</h3>
                        <p>
                            <span class="star">★</span> تقييم ممتاز على TrustPilot و MyFxBook<br>
                            <span class="star">★</span> Wikifx و Forex Peace Army<br>
                            <span class="star">★</span> الأمان عالي جداً بسبب 2FA<br>
                            <span class="star">★</span> توثيق من سورية وأي دولة أخرى
                        </p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="badges">
            <div class="badge">
                <i class="fas fa-lock"></i> نموذج A-Book
            </div>
            <div class="badge security-badge">
                <i class="fas fa-shield-alt"></i> أفضل مزودي السيولة
            </div>
        </div>
    </div>
  </body>                  
                    
                  
  
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
            padding: 20px;
            border-radius: 20px;

        }
        .accordion {
            background-color: #007bff;
            color: white;
            cursor: pointer;
            padding: 15px;
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

=====
