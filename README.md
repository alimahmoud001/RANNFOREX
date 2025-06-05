<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>راني فوريكس - خدمات التداول والوساطة المالية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
        }
        
        :root {
            --primary: #2c3e50;
            --secondary: #1a237e;
            --accent: #3498db;
            --gold: #f1c40f;
            --success: #2ecc71;
            --light: #f8f9fa;
            --dark: #212529;
            --card-bg: rgba(255, 255, 255, 0.95);
            --gradient: linear-gradient(135deg, #1a2a6c, #2c3e50, #1a237e);
        }
        
        body {
            background: var(--gradient);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            color: var(--dark);
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .container {
            max-width: 1200px;
            width: 100%;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            animation: fadeInDown 1s ease;
        }
        
        .logo-header {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }
        
        .logo-icon {
            font-size: 3rem;
            color: var(--gold);
            margin-left: 15px;
        }
        
        .logo-text {
            font-size: 2.5rem;
            font-weight: 700;
            color: white;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }
        
        .section {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 30px;
            margin: 25px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }
        
        .section-title {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 3px solid var(--accent);
        }
        
        .section-icon {
            font-size: 2rem;
            color: var(--accent);
            margin-left: 15px;
        }
        
        .section-header {
            font-size: 1.8rem;
            color: var(--secondary);
            font-weight: 700;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .feature-card {
            background: rgba(52, 152, 219, 0.1);
            border-radius: 15px;
            padding: 20px;
            border-left: 4px solid var(--accent);
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            background: rgba(52, 152, 219, 0.2);
            transform: translateY(-3px);
        }
        
        .feature-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-bottom: 15px;
        }
        
        .feature-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .feature-desc {
            font-size: 0.95rem;
            color: #555;
            line-height: 1.6;
        }
        
        .links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .link-card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(52, 152, 219, 0.2);
            cursor: pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 120px;
        }
        
        .link-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
            border-color: var(--accent);
        }
        
        .link-icon {
            font-size: 2rem;
            margin-bottom: 15px;
        }
        
        .link-title {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--secondary);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            margin: 40px 0;
        }
        
        .social-card {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--card-bg);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            font-size: 1.8rem;
        }
        
        .social-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.3), transparent);
            transform: translateX(-100%);
            transition: transform 0.5s ease;
        }
        
        .social-card:hover {
            transform: translateY(-8px) rotate(5deg);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }
        
        .social-card:hover:before {
            transform: translateX(100%);
        }
        
        .social-card.facebook { color: #1877F2; }
        .social-card.instagram { color: #E1306C; background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%); }
        .social-card.twitter { color: #1DA1F2; }
        .social-card.whatsapp { color: #25D366; }
        .social-card.telegram { color: #0088CC; }
        .social-card.mobile { color: #34B7F1; }
        .social-card.email { color: #EA4335; }
        
        .deposit-steps {
            padding: 20px;
            background: rgba(52, 152, 219, 0.1);
            border-radius: 15px;
            margin-top: 20px;
            border-left: 4px solid var(--success);
        }
        
        .step {
            display: flex;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px dashed #ccc;
        }
        
        .step-number {
            width: 35px;
            height: 35px;
            background: var(--accent);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-left: 15px;
            flex-shrink: 0;
        }
        
        .step-content {
            flex-grow: 1;
        }
        
        .step-title {
            font-weight: 600;
            margin-bottom: 5px;
            color: var(--secondary);
        }
        
        .step-desc {
            color: #555;
            line-height: 1.6;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            color: white;
            padding: 20px;
            font-size: 0.9rem;
            opacity: 0.8;
            width: 100%;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 10px;
            flex-wrap: wrap;
        }
        
        .footer-link {
            color: var(--gold);
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        .footer-link:hover {
            color: white;
            text-decoration: underline;
        }
        
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        @media (max-width: 768px) {
            .links-grid {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
            
            .section-header {
                font-size: 1.5rem;
            }
            
            .logo-text {
                font-size: 2rem;
            }
            
            .social-card {
                width: 60px;
                height: 60px;
                font-size: 1.6rem;
            }
        }
        
        @media (max-width: 480px) {
            .section {
                padding: 20px;
            }
            
            .links-grid {
                grid-template-columns: 1fr;
            }
            
            .section-header {
                font-size: 1.3rem;
            }
            
            .logo-text {
                font-size: 1.7rem;
            }
            
            .logo-icon {
                font-size: 2.5rem;
            }
            
            .social-links {
                gap: 15px;
            }
            
            .social-card {
                width: 55px;
                height: 55px;
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo-header">
                <i class="fas fa-chart-line logo-icon"></i>
                <h1 class="logo-text">راني فوريكس</h1>
            </div>
            <p style="color: white; font-size: 1.2rem; max-width: 800px; margin: 0 auto;">
                خدمات الوساطة المالية المتكاملة لتداول الفوركس والمعادن والنفط والمؤشرات والعملات المشفرة
            </p>
        </header>
        
        <!-- القسم الأول: شركة الوساطة المالية -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-building section-icon"></i>
                <h2 class="section-header">شركة الوساطة المالية</h2>
            </div>
            
            <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="link-card" target="_blank" style="animation: pulse 2s infinite; background: linear-gradient(135deg, #2ecc71, #3498db); color: white;">
                <i class="fas fa-user-plus link-icon"></i>
                <h3 class="link-title">التسجيل في راني فوريكس</h3>
                <p>انضم الآن واستفد من المزايا الحصرية</p>
            </a>
            
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-dollar-sign"></i>
                    </div>
                    <h3 class="feature-title">شروط تداول مميزة</h3>
                    <p class="feature-desc">
                        ★ اقل إيداع 10$ خلال 30 ثانية<br>
                        ★ أقل سحب 10$ خلال 30 ثانية<br>
                        ★ عمولة قليلة جداً<br>
                        ★ اسبريد 0.3~1.2<br>
                        ★ رافعة مالية 1:500
                    </p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3 class="feature-title">الأمان والموثوقية</h3>
                    <p class="feature-desc">
                        ★ تداول آمن على جميع الأصول<br>
                        ★ تقييم ممتاز على مواقع عالمية<br>
                        ★ الأمان العالي باستخدام 2FA<br>
                        ★ توثيق من سورية وأي دولة أخرى
                    </p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-wallet"></i>
                    </div>
                    <h3 class="feature-title">أنواع الحسابات</h3>
                    <p class="feature-desc">
                        ★ أربع أنواع من الحسابات<br>
                        ★ ميتا تريدر 5 حقيقي<br>
                        ★ بدون عمولة<br>
                        ★ كريبتو<br>
                        ★ حساب IB<br>
                        ★ يدعم الحسابات المدارة PAMM
                    </p>
                </div>
            </div>
            
            <div class="links-grid">
                <a href="https://rannforex.com/en/trading/quotesonline/" class="link-card" target="_blank">
                    <i class="fas fa-chart-bar link-icon" style="color: #3498db;"></i>
                    <h3 class="link-title">متوسط الأسبريد اليومي</h3>
                    <p>تابع الأسبريد المتوسط لراني فوريكس</p>
                </a>
            </div>
        </div>
        
        <!-- القسم الثاني: تقييمات الشركة -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-star section-icon"></i>
                <h2 class="section-header">تقييمات الشركة</h2>
            </div>
            
            <div class="links-grid">
                <a href="https://fr.trustpilot.com/review/rannforex.com" class="link-card" target="_blank">
                    <i class="fab fa-trustpilot link-icon" style="color: #00b67a;"></i>
                    <h3 class="link-title">Trust Pilot</h3>
                    <p>شهادات المستخدمين</p>
                </a>
                
                <a href="https://www.wikifx.com/en/dealer/1141850612.html" class="link-card" target="_blank">
                    <i class="fas fa-star-half-alt link-icon" style="color: #3498db;"></i>
                    <h3 class="link-title">WikiFX</h3>
                    <p>تقييمات الخبراء</p>
                </a>
                
                <a href="https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1" class="link-card" target="_blank">
                    <i class="fas fa-chart-pie link-icon" style="color: #f39c12;"></i>
                    <h3 class="link-title">MyFxBook</h3>
                    <p>مراجعات المتداولين</p>
                </a>
                
                <a href="https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review" class="link-card" target="_blank">
                    <i class="fas fa-shield-alt link-icon" style="color: #27ae60;"></i>
                    <h3 class="link-title">Forex Peace Army</h3>
                    <p>تقييمات موثوقة</p>
                </a>
            </div>
        </div>
        
        <!-- القسم الثالث: التطبيقات المطلوبة -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-mobile-alt section-icon"></i>
                <h2 class="section-header">التطبيقات المطلوبة للبدء بالتداول</h2>
            </div>
            
            <div class="links-grid">
                <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" class="link-card" target="_blank">
                    <i class="fas fa-chart-line link-icon" style="color: #3498db;"></i>
                    <h3 class="link-title">منصة ميتا تريدر 5</h3>
                    <p>المنصة الأفضل للتداول</p>
                </a>
                
                <a href="https://cwallet.com/referral/DvY6dZtS" class="link-card" target="_blank">
                    <i class="fas fa-wallet link-icon" style="color: #9b59b6;"></i>
                    <h3 class="link-title">المحفظة الإلكترونية</h3>
                    <p>CWallet - محفظة آمنة</p>
                </a>
                
                <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" class="link-card" target="_blank">
                    <i class="fas fa-lock link-icon" style="color: #2c3e50;"></i>
                    <h3 class="link-title">تطبيق المصادقة الثنائية</h3>
                    <p>لتعزيز أمان حسابك</p>
                </a>
            </div>
        </div>
        
        <!-- القسم الرابع: قسم تعليمي -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-graduation-cap section-icon"></i>
                <h2 class="section-header">فيديو تعليمي</h2>
            </div>
            
            <div class="links-grid">
                <a href="https://youtube.com/shorts/SlQc3Q6L3HQ?si=Q5sdG7_lxANoykBs" class="link-card" target="_blank">
                    <i class="fab fa-youtube link-icon" style="color: #e74c3c;"></i>
                    <h3 class="link-title">فيديو تعليمي للمصادقة</h3>
                    <p>كيفية استخدام تطبيق Google Authenticator</p>
                </a>
            </div>
        </div>
        
        <!-- القسم الخامس: قنوات تلجرام -->
        <div class="section">
            <div class="section-title">
                <i class="fab fa-telegram section-icon"></i>
                <h2 class="section-header">قنوات تلجرام</h2>
            </div>
            
            <div class="links-grid">
                <a href="https://t.me/tradewithalimahmoud" class="link-card" target="_blank">
                    <i class="fab fa-telegram link-icon" style="color: #0088cc;"></i>
                    <h3 class="link-title">قناتنا الرئيسية</h3>
                    <p>Trade With Ali Mahmoud</p>
                </a>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fab fa-telegram"></i>
                    </div>
                    <h3 class="feature-title">قنوات الإشارات (للتعلم فقط)</h3>
                    <p class="feature-desc">
                        💯https://t.me/FX_IRI<br>
                        💯https://t.me/prosignalsfxx<br>
                        💯https://t.me/top_tradingsignals<br>
                        💯https://t.me/signalsfc<br>
                        💯https://t.me/elitetrading_signals<br>
                        💯https://t.me/free_signals<br>
                        💯https://t.me/greysuitcommunity
                    </p>
                </div>
            </div>
        </div>
        
        <!-- القسم السادس: القسم التعليمي -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-book section-icon"></i>
                <h2 class="section-header">موارد تعليمية</h2>
            </div>
            
            <div class="links-grid">
                <a href="https://youtube.com/@tradewithpatarabic?si=4egOIQw15KHmRJGy" class="link-card" target="_blank">
                    <i class="fab fa-youtube link-icon" style="color: #e74c3c;"></i>
                    <h3 class="link-title">كورس تعلم التداول</h3>
                    <p>مع باتك - أشهر ملياردير في التداول</p>
                </a>
                
                <a href="https://youtube.com/@smart_risk?si=s0leP3OYv9GuCp3r" class="link-card" target="_blank">
                    <i class="fab fa-youtube link-icon" style="color: #e74c3c;"></i>
                    <h3 class="link-title">قناة Smart Risk</h3>
                    <p>محتوى تعليمي متقدم</p>
                </a>
                
                <a href="https://www.instagram.com/kameel_m5/reel/DIvnWEQM_4g/" class="link-card" target="_blank">
                    <i class="fab fa-instagram link-icon" style="color: #E1306C;"></i>
                    <h3 class="link-title">كورس على انستغرام</h3>
                    <p>محتوى تعليمي من كامل</p>
                </a>
            </div>
        </div>
        
        <!-- القسم السابع: تعليمات الإيداع -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-money-bill-wave section-icon"></i>
                <h2 class="section-header">طريقة الإيداع</h2>
            </div>
            
            <div class="deposit-steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <div class="step-content">
                        <h3 class="step-title">الانتقال لقسم الإيداع</h3>
                        <p class="step-desc">نضغط على الثلاث خطوط في موقع rannforex أعلى يمين الشاشة ثم Deposit</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <div class="step-content">
                        <h3 class="step-title">اختيار طريقة الدفع</h3>
                        <p class="step-desc">Select deposit method: crypto ثم اختر حساب التداول ثم Continue</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <div class="step-content">
                        <h3 class="step-title">إدخال المبلغ</h3>
                        <p class="step-desc">أدخل المبلغ في الفراغ الأول، اختر USD ثم Continue</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">4</div>
                    <div class="step-content">
                        <h3 class="step-title">كود المصادقة</h3>
                        <p class="step-desc">أدخل كود 2FA من تطبيق Google Authenticator ثم Continue</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">5</div>
                    <div class="step-content">
                        <h3 class="step-title">إتمام العملية</h3>
                        <p class="step-desc">نسخ العنوان الظاهر، ثم في CWallet نختار Send، نلصق العنوان ثم Send</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- روابط التواصل الاجتماعي -->
        <div class="social-links">
            <a href="https://www.facebook.com/alimahmoud001" class="social-card facebook" target="_blank">
                <i class="fab fa-facebook-f"></i>
            </a>
            
            <a href="https://www.instagram.com/alimahmoud001a?igsh=YzljYTk1ODg3Zg==" class="social-card instagram" target="_blank">
                <i class="fab fa-instagram"></i>
            </a>
            
            <a href="https://x.com/en_alimahmoud" class="social-card twitter" target="_blank">
                <i class="fab fa-x-twitter"></i>
            </a>
            
            <a href="https://wa.me/qr/AFVVUP3Z46UYM1" class="social-card whatsapp" target="_blank">
                <i class="fab fa-whatsapp"></i>
            </a>
            
            <a href="https://t.me/Alimahmoud001" class="social-card telegram" target="_blank">
                <i class="fab fa-telegram"></i>
            </a>
            
            <a href="tel:+963934598967" class="social-card mobile">
                <i class="fas fa-mobile-alt"></i>
            </a>
            
            <a href="mailto:alimahmoud001a@gmail.com" class="social-card email">
                <i class="fas fa-envelope"></i>
            </a>
        </div>
        
        <footer>
            <p>© 2023 علي محمود - جميع الحقوق محفوظة</p>
            <div class="footer-links">
                <a href="tel:+963934598967" class="footer-link">+963 934 598 967</a>
                <a href="mailto:alimahmoud001a@gmail.com" class="footer-link">alimahmoud001a@gmail.com</a>
                <a href="https://t.me/tradewithalimahmoud" class="footer-link">قناة التلجرام</a>
            </div>
            <p style="margin-top: 15px;">صممت بحب ❤️ لتسهيل رحلتك في عالم التداول</p>
        </footer>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.link-card, .social-card');
            
            cards.forEach(card => {
                card.addEventListener('click', function(e) {
                    e.preventDefault();
                    const link = this.getAttribute('href');
                    
                    // تأثير النقر
                    this.style.transform = 'scale(0.95)';
                    setTimeout(() => {
                        this.style.transform = '';
                        if(link) window.open(link, '_blank');
                    }, 200);
                });
            });
            
            // تأثيرات الظهور التدريجي للبطاقات
            const animateCards = () => {
                const cards = document.querySelectorAll('.section, .social-card');
                cards.forEach((card, index) => {
                    setTimeout(() => {
                        card.style.opacity = '0';
                        card.style.transform = 'translateY(20px)';
                        card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
                        
                        setTimeout(() => {
                            card.style.opacity = '1';
                            card.style.transform = 'translateY(0)';
                        }, 50);
                    }, index * 150);
                });
            };
            
            setTimeout(animateCards, 500);
        });
    </script>
</body>
</html>
