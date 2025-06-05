<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>علي محمود - روابط التواصل وخدمات الوساطة المالية</title>
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
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #2c3e50, #1a237e);
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
        
        .profile-card {
            background: var(--card-bg);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            padding: 30px;
            max-width: 500px;
            margin: 0 auto 30px;
            text-align: center;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .profile-card:before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transform: rotate(45deg);
            z-index: 0;
        }
        
        .profile-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--accent);
            margin: 0 auto 20px;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 60px;
            position: relative;
            z-index: 1;
        }
        
        .profile-name {
            font-size: 2.2rem;
            margin-bottom: 10px;
            color: var(--secondary);
            font-weight: 700;
            position: relative;
            z-index: 1;
        }
        
        .profile-title {
            font-size: 1.2rem;
            color: var(--accent);
            margin-bottom: 20px;
            font-weight: 500;
            position: relative;
            z-index: 1;
        }
        
        .social-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            width: 100%;
            margin-top: 20px;
        }
        
        .social-card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            cursor: pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 150px;
            position: relative;
            overflow: hidden;
        }
        
        .social-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--accent);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }
        
        .social-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
            background: rgba(255, 255, 255, 0.98);
        }
        
        .social-card:hover:before {
            transform: scaleX(1);
        }
        
        .social-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            transition: transform 0.3s ease;
        }
        
        .social-card:hover .social-icon {
            transform: scale(1.2);
        }
        
        .social-name {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--dark);
        }
        
        .social-username {
            font-size: 0.9rem;
            color: #666;
            overflow: hidden;
            text-overflow: ellipsis;
            width: 100%;
        }
        
        .facebook { color: #1877F2; }
        .instagram { color: #E1306C; }
        .twitter { color: #1DA1F2; }
        .whatsapp { color: #25D366; }
        .telegram { color: #0088CC; }
        .mobile { color: #34B7F1; }
        .email { color: #EA4335; }
        .broker { color: #2ecc71; }
        .review { color: #f39c12; }
        .platform { color: #3498db; }
        .wallet { color: #9b59b6; }
        
        .section-title {
            text-align: center;
            font-size: 1.8rem;
            color: white;
            margin: 40px 0 20px;
            padding: 10px 0;
            position: relative;
            font-weight: 700;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: var(--gold);
            border-radius: 2px;
        }
        
        .broker-features {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 30px;
            margin: 30px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .broker-header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .broker-logo {
            font-size: 3rem;
            color: var(--gold);
            margin-bottom: 15px;
        }
        
        .broker-title {
            font-size: 2rem;
            color: var(--secondary);
            margin-bottom: 10px;
        }
        
        .broker-subtitle {
            font-size: 1.2rem;
            color: var(--accent);
            margin-bottom: 20px;
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
        
        .broker-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .broker-link-card {
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
        
        .broker-link-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
            border-color: var(--accent);
        }
        
        .broker-link-icon {
            font-size: 2rem;
            margin-bottom: 15px;
        }
        
        .broker-link-title {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--secondary);
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
        }
        
        .footer-link {
            color: var(--gold);
            text-decoration: none;
            transition: all 0.3s ease;
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
        
        @media (max-width: 768px) {
            .social-links, .broker-links {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
            
            .profile-name {
                font-size: 1.8rem;
            }
            
            .broker-title {
                font-size: 1.7rem;
            }
        }
        
        @media (max-width: 480px) {
            .profile-card {
                padding: 20px;
            }
            
            .social-links, .broker-links {
                grid-template-columns: 1fr;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-card">
                <div class="profile-img">
                    <i class="fas fa-user-tie"></i>
                </div>
                <h1 class="profile-name">علي محمود</h1>
                <p class="profile-title">متخصص في الفوركس والوساطة المالية</p>
            </div>
        </header>
        
        <h2 class="section-title">روابط التواصل الشخصي</h2>
        
        <div class="social-links">
            <!-- فيس بوك -->
            <a href="https://www.facebook.com/alimahmoud001" class="social-card" target="_blank">
                <i class="fab fa-facebook social-icon facebook"></i>
                <h3 class="social-name">فيسبوك</h3>
                <p class="social-username">علي محمود</p>
            </a>
            
            <!-- انستغرام -->
            <a href="https://www.instagram.com/alimahmoud001a?igsh=YzljYTk1ODg3Zg==" class="social-card" target="_blank">
                <i class="fab fa-instagram social-icon instagram"></i>
                <h3 class="social-name">انستغرام</h3>
                <p class="social-username">alimahmoud001a</p>
            </a>
            
            <!-- تويتر (X) -->
            <a href="https://x.com/en_alimahmoud" class="social-card" target="_blank">
                <i class="fab fa-x-twitter social-icon twitter"></i>
                <h3 class="social-name">تويتر (X)</h3>
                <p class="social-username">en_alimahmoud</p>
            </a>
            
            <!-- واتساب -->
            <a href="https://wa.me/qr/AFVVUP3Z46UYM1" class="social-card" target="_blank">
                <i class="fab fa-whatsapp social-icon whatsapp"></i>
                <h3 class="social-name">واتساب</h3>
                <p class="social-username">تواصل مباشر</p>
            </a>
            
            <!-- تلجرام -->
            <a href="https://t.me/ali0619000" class="social-card" target="_blank">
                <i class="fab fa-telegram social-icon telegram"></i>
                <h3 class="social-name">تلجرام</h3>
                <p class="social-username">@ali0619000</p>
            </a>
            
            <!-- موبايل -->
            <a href="tel:+963934598967" class="social-card">
                <i class="fas fa-mobile-alt social-icon mobile"></i>
                <h3 class="social-name">اتصال هاتفي</h3>
                <p class="social-username">+963 934 598 967</p>
            </a>
            
            <!-- ايميل -->
            <a href="mailto:alimahmoud001a@gmail.com" class="social-card">
                <i class="fas fa-envelope social-icon email"></i>
                <h3 class="social-name">البريد الإلكتروني</h3>
                <p class="social-username">alimahmoud001a@gmail.com</p>
            </a>
        </div>
        
        <h2 class="section-title">خدمات الوساطة المالية - راني فوريكس</h2>
        
        <div class="broker-features">
            <div class="broker-header">
                <div class="broker-logo">
                    <i class="fas fa-chart-line"></i>
                </div>
                <h2 class="broker-title">راني فوريكس - Rann Forex</h2>
                <p class="broker-subtitle">شركة وساطة مالية موثوقة لتداول الفوركس والمعادن والنفط والمؤشرات والعملات المشفرة</p>
            </div>
            
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
                        ★ رافعة مالية 1:500<br>
                        ★ انزلاق منخفض<br>
                        ★ تنفيذ فوري للصفقات
                    </p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3 class="feature-title">الأمان والموثوقية</h3>
                    <p class="feature-desc">
                        ★ تداول آمن على جميع الأصول<br>
                        ★ تقييم ممتاز على مواقع:<br>
                        &nbsp;&nbsp;- Trust Pilot<br>
                        &nbsp;&nbsp;- MyFxBook<br>
                        &nbsp;&nbsp;- WikiFX<br>
                        &nbsp;&nbsp;- Forex Peace Army<br>
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
                        ★ أربع أنواع من الحسابات:<br>
                        &nbsp;&nbsp;- ميتا تريدر 5 حقيقي<br>
                        &nbsp;&nbsp;- بدون عمولة<br>
                        &nbsp;&nbsp;- كريبتو<br>
                        &nbsp;&nbsp;- حساب IB<br>
                        ★ يدعم الحسابات المدارة PAMM<br>
                        ★ نموذج A-Book من أفضل مزودي السيولة
                    </p>
                </div>
            </div>
            
            <div class="broker-links">
                <!-- رابط التسجيل -->
                <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="broker-link-card" target="_blank">
                    <i class="fas fa-user-plus broker-link-icon" style="color: #2ecc71;"></i>
                    <h3 class="broker-link-title">التسجيل في شركة الوساطة</h3>
                    <p class="social-username">انضم الآن واستفد من المزايا</p>
                </a>
                
                <!-- قناة التلجرام -->
                <a href="https://t.me/syriatradingfx" class="broker-link-card" target="_blank">
                    <i class="fab fa-telegram broker-link-icon" style="color: #0088cc;"></i>
                    <h3 class="broker-link-title">قناتنا على تلجرام</h3>
                    <p class="social-username">قناة التداول السورية</p>
                </a>
                
                <!-- اسبريد اليومي -->
                <a href="https://rannforex.com/en/trading/quotesonline/" class="broker-link-card" target="_blank">
                    <i class="fas fa-chart-bar broker-link-icon" style="color: #3498db;"></i>
                    <h3 class="broker-link-title">متوسط الأسبريد اليومي</h3>
                    <p class="social-username">تابع الأسبريد المتوسط</p>
                </a>
                
                <!-- تقييمات الشركة -->
                <a href="https://fr.trustpilot.com/review/rannforex.com" class="broker-link-card" target="_blank">
                    <i class="fas fa-star broker-link-icon" style="color: #f1c40f;"></i>
                    <h3 class="broker-link-title">تقييم Trust Pilot</h3>
                    <p class="social-username">شهادات المستخدمين</p>
                </a>
                
                <!-- منصة ميتا تريدر 5 -->
                <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" class="broker-link-card" target="_blank">
                    <i class="fas fa-mobile-alt broker-link-icon" style="color: #9b59b6;"></i>
                    <h3 class="broker-link-title">منصة ميتا تريدر 5</h3>
                    <p class="social-username">المنصة الأفضل للتداول</p>
                </a>
                
                <!-- المحفظة الإلكترونية -->
                <a href="https://cwallet.com/referral/DvY6dZtS" class="broker-link-card" target="_blank">
                    <i class="fas fa-wallet broker-link-icon" style="color: #e74c3c;"></i>
                    <h3 class="broker-link-title">المحفظة الإلكترونية</h3>
                    <p class="social-username">CWallet - محفظة آمنة</p>
                </a>
                
                <!-- تطبيق المصادقة الثنائية -->
                <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" class="broker-link-card" target="_blank">
                    <i class="fas fa-lock broker-link-icon" style="color: #2c3e50;"></i>
                    <h3 class="broker-link-title">تطبيق المصادقة الثنائية</h3>
                    <p class="social-username">لتعزيز أمان حسابك</p>
                </a>
                
                <!-- فيديو المصادقة الثنائية -->
                <a href="https://youtube.com/shorts/SlQc3Q6L3HQ?si=Q5sdG7_lxANoykBs" class="broker-link-card" target="_blank">
                    <i class="fab fa-youtube broker-link-icon" style="color: #e74c3c;"></i>
                    <h3 class="broker-link-title">فيديو تعليمي للمصادقة</h3>
                    <p class="social-username">كيفية استخدام 2FA</p>
                </a>
                
                <!-- تقييمات إضافية -->
                <a href="https://www.wikifx.com/en/dealer/1141850612.html" class="broker-link-card" target="_blank">
                    <i class="fas fa-star-half-alt broker-link-icon" style="color: #3498db;"></i>
                    <h3 class="broker-link-title">تقييم WikiFX</h3>
                    <p class="social-username">تقييمات الخبراء</p>
                </a>
                
                <a href="https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1" class="broker-link-card" target="_blank">
                    <i class="fas fa-chart-pie broker-link-icon" style="color: #f39c12;"></i>
                    <h3 class="broker-link-title">تقييم MyFxBook</h3>
                    <p class="social-username">مراجعات المتداولين</p>
                </a>
                
                <a href="https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review" class="broker-link-card" target="_blank">
                    <i class="fas fa-shield-alt broker-link-icon" style="color: #27ae60;"></i>
                    <h3 class="broker-link-title">تقييم Forex Peace Army</h3>
                    <p class="social-username">تقييمات موثوقة</p>
                </a>
            </div>
        </div>
        
        <footer>
            <p>© 2023 علي محمود - جميع الحقوق محفوظة</p>
            <div class="footer-links">
                <a href="tel:+963934598967" class="footer-link">+963 934 598 967</a>
                <a href="mailto:alimahmoud001a@gmail.com" class="footer-link">alimahmoud001a@gmail.com</a>
                <a href="https://t.me/syriatradingfx" class="footer-link">قناة التداول السورية</a>
            </div>
            <p style="margin-top: 15px;">صممت بحب ❤️ لتسهيل التواصل معكم وتقديم أفضل خدمات الوساطة المالية</p>
        </footer>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.social-card, .broker-link-card');
            
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
                const cards = document.querySelectorAll('.social-card, .feature-card, .broker-link-card');
                cards.forEach((card, index) => {
                    setTimeout(() => {
                        card.style.opacity = '0';
                        card.style.transform = 'translateY(20px)';
                        card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
                        
                        setTimeout(() => {
                            card.style.opacity = '1';
                            card.style.transform = 'translateY(0)';
                        }, 50);
                    }, index * 100);
                });
            };
            
            setTimeout(animateCards, 500);
        });
    </script>
</body>
</html>
