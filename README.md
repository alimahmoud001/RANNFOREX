<!DOCTYPE html>
<html>
<head>
    <title>موقعي</title>
    <style>
        body {
            margin: 0; /* إزالة الهوامش الافتراضية للجسم */
            padding: 0;
        }
        .container {
            width: 50%; /* هنا نحدد العرض 50% */
            margin: 0 auto; /* توسيط أفقي */
            padding: 20px; /* هامش داخلي اختياري */
            background-color: #f0f0f0; /* لون خلفية اختياري */
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- كل محتوى الصفحة هنا -->
![Image](https://github.com/user-attachments/assets/e40ed028-8ac0-44e0-b132-03c70f1c6edf)

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
            display: flex;
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
                grid-template-columns: repeat(auto-fill, minmax(50%, 1fr));
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
 
      <div class="register-card">
                    <h3>انضم إلى قناة الإشارات المجانية الخاصة بي</h3>
                    <p> هنا الإشارات مجانية وستبقى مجانية إلى الابد </p>
                    <a href=" https://t.me/tradewithalimahmoud  " class="btn btn-primary" target="_blank">
                        <i class="fas fa-user-plus"></i> انضم الآن
                    </a>
                     </div>
                    
                </div>
                 



 <!-- القسم الثالث: تطبيقات يجب تحميلها للبدء بالتداول -->
        <sec
        <h1>مرحباً بالعالم</h1>
        <p>هذه صفحتي الشخصية.</p>
        <img src="images/my-image.jpg" alt="صورة مثال">
        <p>شرح بسيط تحت الصورة.</p>
    </div>
</body>
</html>
