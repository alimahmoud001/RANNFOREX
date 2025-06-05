<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>روابط التواصل الشخصية - علي محمود</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #4361ee;
            --secondary: #3f37c9;
            --accent: #4895ef;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4cc9f0;
            --card-bg: rgba(255, 255, 255, 0.9);
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #1a2a6c);
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
            margin-bottom: 40px;
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
            border: 5px solid var(--primary);
            margin: 0 auto 20px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 60px;
        }
        
        .profile-name {
            font-size: 2.2rem;
            margin-bottom: 10px;
            color: var(--secondary);
            font-weight: 700;
        }
        
        .profile-title {
            font-size: 1.2rem;
            color: var(--accent);
            margin-bottom: 20px;
            font-weight: 500;
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
        }
        
        .social-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
            background: rgba(255, 255, 255, 0.95);
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
            background: var(--success);
            border-radius: 2px;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            color: white;
            padding: 20px;
            font-size: 0.9rem;
            opacity: 0.8;
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
            .social-links {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
            
            .profile-name {
                font-size: 1.8rem;
            }
        }
        
        @media (max-width: 480px) {
            .profile-card {
                padding: 20px;
            }
            
            .social-links {
                grid-template-columns: 1fr;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-card">
                <div class="profile-img">
                    <i class="fas fa-user"></i>
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
        
        <h2 class="section-title">خدمات التداول والوساطة</h2>
        
        <div class="social-links">
            <!-- شركة الوساطة -->
            <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" class="social-card" target="_blank">
                <i class="fas fa-chart-line social-icon" style="color: #4CAF50;"></i>
                <h3 class="social-name">شركة الوساطة</h3>
                <p class="social-username">راني فوريكس - انضم الآن</p>
            </a>
            
            <!-- قناة التلجرام -->
            <a href="https://t.me/syriatradingfx" class="social-card" target="_blank">
                <i class="fab fa-telegram social-icon" style="color: #0088cc;"></i>
                <h3 class="social-name">قناتنا</h3>
                <p class="social-username">قناة التداول السورية</p>
            </a>
        </div>
        
        <footer>
            <p>© 2023 علي محمود - جميع الحقوق محفوظة</p>
            <p>صممت بحب ❤️ لتسهيل التواصل معكم</p>
        </footer>
    </div>

    <script>
        // إضافة تأثيرات تفاعلية بسيطة
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.social-card');
            
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
        });
    </script>
</body>
</html>
