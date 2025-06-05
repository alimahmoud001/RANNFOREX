# RANNFOREX

<html dir="rtl" lang="ar">
  <head>
    <meta charset="UTF-8">
    <meta content="width=device-width, initial-scale=1.0" name="viewport">
    <title>Rann Forex - الوساطة المالية الموثوقة
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&amp;display=swap" rel="stylesheet"></link>
    <style>
      :root {
          --primary: #0a3d62;
          --secondary: #1e88e5;
          --accent: #00b894;
          --accent-light: #55efc4;
          --light: #ffffff;
          --dark: #2d3436;
          --gray: #f5f6fa;
          --warning: #fdcb6e;
          --danger: #e17055;
          --success: #00b894;
          --border: #e0e0e0;
          --shadow: rgba(0, 0, 0, 0.1);
      }

      * {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
      }

      body {
          font-family: 'Tajawal', sans-serif;
          background-color: var(--gray);
          color: var(--dark);
          line-height: 1.8;
      }

      .container {
          max-width: 1200px;
          margin: 0 auto;
          padding: 20px;
      }

      /* Header Styles */
      header {
          background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
          color: var(--light);
          text-align: center;
          padding: 50px 20px;
          border-radius: 0 0 20px 20px;
          margin-bottom: 30px;
          box-shadow: 0 5px 15px var(--shadow);
      }

      .logo {
          font-size: 2.8rem;
          margin-bottom: 20px;
          display: flex;
          justify-content: center;
          align-items: center;
          gap: 15px;
      }

      .logo i {
          color: var(--warning);
          background: rgba(255, 255, 255, 0.1);
          width: 80px;
          height: 80px;
          border-radius: 50%;
          display: flex;
          justify-content: center;
          align-items: center;
          padding: 15px;
      }

      .tagline {
          font-size: 1.3rem;
          max-width: 800px;
          margin: 0 auto 30px;
          opacity: 0.9;
      }

      /* Main Button */
      .main-btn {
          display: inline-block;
          background: var(--accent);
          color: white;
          padding: 18px 45px;
          border-radius: 12px;
          text-decoration: none;
          font-weight: bold;
          margin: 30px 0;
          transition: all 0.3s ease;
          box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
          font-size: 1.2rem;
          border: none;
          cursor: pointer;
      }

      .main-btn:hover {
          background: var(--accent-light);
          transform: translateY(-3px);
          box-shadow: 0 8px 20px rgba(0, 0, 0, 0.25);
      }

      .main-btn:active {
          transform: translateY(1px);
      }

      /* Card Styles */
      .card {
          background: var(--light);
          border-radius: 16px;
          padding: 30px;
          margin-bottom: 30px;
          border: 1px solid var(--border);
          box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
          transition: transform 0.3s ease, box-shadow 0.3s ease;
      }

      .card:hover {
          transform: translateY(-5px);
          box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
      }

      .card-header {
          display: flex;
          align-items: center;
          margin-bottom: 25px;
          color: var(--primary);
          padding-bottom: 15px;
          border-bottom: 2px solid var(--accent);
      }

      .card-header i {
          margin-left: 15px;
          font-size: 1.8rem;
          background: var(--accent);
          color: white;
          width: 50px;
          height: 50px;
          border-radius: 12px;
          display: flex;
          justify-content: center;
          align-items: center;
      }

      .card-title {
          font-size: 1.8rem;
          font-weight: 800;
      }

      /* Feature List */
      .features-grid {
          display: grid;
          grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
          gap: 25px;
          margin: 30px 0;
      }

      .feature-item {
          background: var(--gray);
          padding: 25px;
          border-radius: 16px;
          display: flex;
          align-items: center;
          transition: all 0.3s ease;
          border: 1px solid var(--border);
      }

      .feature-item:hover {
          background: var(--light);
          transform: translateY(-3px);
          box-shadow: 0 8px 15px var(--shadow);
          border-color: var(--accent);
      }

      .feature-icon {
          background: var(--secondary);
          width: 60px;
          height: 60px;
          border-radius: 16px;
          display: flex;
          justify-content: center;
          align-items: center;
          margin-left: 20px;
          flex-shrink: 0;
          color: white;
          font-size: 1.5rem;
      }

      .feature-content h3 {
          font-size: 1.3rem;
          margin-bottom: 8px;
          color: var(--primary);
      }

      .feature-content p {
          color: #666;
      }

      /* Review Section */
      .reviews-container {
          display: grid;
          grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
          gap: 25px;
      }

      .review-item {
          background: var(--light);
          padding: 25px;
          border-radius: 16px;
          text-align: center;
          transition: all 0.3s ease;
          border: 1px solid var(--border);
      }

      .review-item:hover {
          transform: translateY(-5px);
          box-shadow: 0 10px 20px var(--shadow);
          border-color: var(--accent);
      }

      .review-logo {
          font-size: 2.5rem;
          margin-bottom: 20px;
          color: var(--secondary);
      }

      .review-item h3 {
          font-size: 1.4rem;
          margin-bottom: 15px;
          color: var(--primary);
      }

      /* Steps Section - Modified Layout */
      .steps-container {
          counter-reset: step-counter;
      }

      .step-item {
          display: flex;
          align-items: flex-start;
          gap: 25px;
          padding: 30px;
          margin-bottom: 25px;
          background: var(--gray);
          border-radius: 16px;
          transition: all 0.3s ease;
          border: 1px solid var(--border);
      }

      .step-item:hover {
          background: var(--light);
          transform: translateY(-3px);
          box-shadow: 0 8px 15px var(--shadow);
      }

      .step-number {
          background: var(--accent);
          color: white;
          width: 50px;
          height: 50px;
          border-radius: 50%;
          display: flex;
          justify-content: center;
          align-items: center;
          font-weight: bold;
          font-size: 1.5rem;
          flex-shrink: 0;
      }

      .step-number::before {
          counter-increment: step-counter;
          content: counter(step-counter);
      }

      .step-content {
          flex: 1;
      }

      .step-content h3 {
          font-size: 1.3rem;
          margin-bottom: 10px;
          color: var(--primary);
      }

      .divider {
          text-align: center;
          margin: 20px 0;
          position: relative;
      }

      .divider::before {
          content: '';
          position: absolute;
          top: 50%;
          right: 0;
          left: 0;
          height: 1px;
          background: linear-gradient(to right, transparent, var(--accent), transparent);
          z-index: 1;
      }

      .divider i {
          background: var(--gray);
          padding: 0 20px;
          position: relative;
          z-index: 2;
          color: var(--accent);
          font-size: 1.5rem;
      }

      /* Links Section */
      .links-grid {
          display: grid;
          grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
          gap: 20px;
      }

      .link-item {
          background: var(--gray);
          padding: 20px;
          border-radius: 16px;
          text-align: center;
          transition: all 0.3s ease;
          border: 1px solid var(--border);
      }

      .link-item:hover {
          background: var(--light);
          transform: translateY(-3px);
          box-shadow: 0 8px 15px var(--shadow);
          border-color: var(--accent);
      }

      .link-item a {
          color: var(--dark);
          text-decoration: none;
          display: flex;
          flex-direction: column;
          align-items: center;
          gap: 15px;
          font-size: 1.1rem;
      }

      .link-item i {
          font-size: 2.5rem;
          color: var(--secondary);
      }

      /* Contact Section */
      .contact-info {
          display: flex;
          flex-wrap: wrap;
          gap: 25px;
          justify-content: center;
          margin-top: 20px;
      }

      .contact-item {
          display: flex;
          align-items: center;
          padding: 20px 30px;
          background: var(--gray);
          border-radius: 16px;
          transition: all 0.3s ease;
          border: 1px solid var(--border);
          gap: 15px;
          cursor: pointer;
      }

      .contact-item:hover {
          background: var(--light);
          transform: translateY(-3px);
          box-shadow: 0 8px 15px var(--shadow);
          border-color: var(--accent);
      }

      .contact-item i {
          color: var(--accent);
          font-size: 2rem;
      }

      .contact-content h3 {
          font-size: 1.3rem;
          color: var(--primary);
      }

      .contact-content p {
          color: #666;
      }

      /* Footer */
      footer {
          background: var(--primary);
          color: var(--light);
          text-align: center;
          padding: 40px 20px;
          margin-top: 50px;
          border-radius: 20px 20px 0 0;
      }

      .footer-links {
          display: flex;
          justify-content: center;
          gap: 25px;
          margin-bottom: 30px;
      }

      .footer-links a {
          color: var(--light);
          font-size: 1.8rem;
          transition: all 0.3s ease;
          display: flex;
          justify-content: center;
          align-items: center;
          width: 60px;
          height: 60px;
          border-radius: 50%;
          background: rgba(255, 255, 255, 0.1);
      }

      .footer-links a:hover {
          color: var(--accent-light);
          transform: translateY(-5px);
          background: rgba(255, 255, 255, 0.2);
      }

      .footer-text {
          max-width: 800px;
          margin: 0 auto;
          opacity: 0.8;
      }

      /* Responsive */
      @media (max-width: 768px) {
          .features-grid {
              grid-template-columns: 1fr;
          }

          .step-item {
              flex-direction: column;
              align-items: center;
              text-align: center;
              padding: 25px;
          }

          .step-number {
              margin-bottom: 15px;
          }

          .contact-info {
              flex-direction: column;
          }

          .logo {
              font-size: 2rem;
          }

          .logo i {
              width: 60px;
              height: 60px;
          }
      }
    </style>
  </head>
  <body>
    <header>
      <div class="container">
        <div class="logo">
          <i class="fas fa-chart-line"></i>
          <h1>RannForex</h1>
        </div>
        <p class="tagline">
          وسيطك المالي الموثوق لتداول الفوركس والمعادن والنفط والمؤشرات والعملات
          المشفرة بأفضل الشروط والأمان لقد قمت بتضمين روابط لكل ما تحتاجه في
          مجال التداول ضمن هذه الصفحة من تطبيقات وبرامج تحليل فني ومحفظة
          إلكترونية ومنصة ميتا تريدر ووسيط التداول الذي اعمل معه وقناتي على
          تلجرام ❤️
        </p>
        <a class="main-btn" href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1">
          <i class="fas fa-user-plus"></i> سجل حساب جديد الآن
        </a>
      </div>
    </header>

    <div class="container">
      <!-- Main Features -->
      <div class="card">
        <div class="card-header">
          <i class="fas fa-star"></i>
          <h2 class="card-title">مميزات شركة Rann Forex</h2>
        </div>

        <div class="features-grid">
          <div class="feature-item">
            <div class="feature-icon">
              <i class="fas fa-dollar-sign"></i>
            </div>
            <div class="feature-content">
              <h3>أقل إيداع وسحب</h3>
              <p>10$ خلال 30 ثانية فقط</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <i class="fas fa-percentage"></i>
            </div>
            <div class="feature-content">
              <h3>عمولات قليلة جداً</h3>
              <p>اسبريد يبدأ من 0.3~1.2</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <i class="fas fa-sliders-h"></i>
            </div>
            <div class="feature-content">
              <h3>رافعة مالية عالية</h3>
              <p>تصل إلى 1:500</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <i class="fas fa-shield-alt"></i>
            </div>
            <div class="feature-content">
              <h3>أمان عالي</h3>
              <p>نظام المصادقة الثنائية (2FA)</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <i class="fas fa-bolt"></i>
            </div>
            <div class="feature-content">
              <h3>تنفيذ فوري</h3>
              <p>للصفقات مع انزلاق منخفض</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <i class="fas fa-wallet"></i>
            </div>
            <div class="feature-content">
              <h3>أنواع متعددة من الحسابات</h3>
              <p>حقيقي، بدون عمولة، كريبتو، IB و PAMM</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Important Links -->
      <div class="card">
        <div class="card-header">
          <i class="fas fa-link"></i>
          <h2 class="card-title">روابط هامة</h2>
        </div>

        <div class="links-grid">
          <div class="link-item">
            <a href="https://rannforex.com/en/trading/quotesonline/">
              <i class="fas fa-chart-bar"></i>
              <span>متوسط الاسبريد اليومي لشركة rannforex </span>
            </a>
          </div>

          <div class="link-item">
            <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5">
              <i class="fas fa-mobile-alt"></i>
              <span>المنصة الموثوقة منصة ميتاتريدر 5</span>
            </a>
          </div>

          <div class="link-item">
            <a href="https://cwallet.com/referral/DvY6dZtS">
              <i class="fas fa-wallet"></i>
              <span> المحفظة الالكترونية cwallet تعمل في سورية وتوثق على الهوية السورية</span>
            </a>
          </div>

          <div class="link-item">
            <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2">
              <i class="fas fa-lock"></i>
              <span>تطبيق المصادقة الثنائية يجب عليك تنزيله من اجل توثيق عمليات السحب والايداع</span>
            </a>
          </div>
        </div>
      </div>

      <!-- Reviews -->
      <div class="card">
        <div class="card-header">
          <i class="fas fa-medal"></i>
          <h2 class="card-title">تقييمات الشركة</h2>
        </div>

        <div class="reviews-container">
          <div class="review-item">
            <div class="review-logo">
              <i class="fas fa-award"></i>
            </div>
            <h3>Trust Pilot</h3>
            <p>تقييم ممتاز من منصة الثقة العالمية</p>
            <a class="main-btn" href="https://fr.trustpilot.com/review/rannforex.com" style="font-size: 1rem; margin-top: 20px; padding: 12px 25px;">
              زيارة التقييم
            </a>
          </div>

          <div class="review-item">
            <div class="review-logo">
              <i class="fas fa-star"></i>
            </div>
            <h3>WikiFX</h3>
            <p>معلومات شاملة عن الوسيط المالي</p>
            <a class="main-btn" href="https://www.wikifx.com/en/dealer/1141850612.html" style="font-size: 1rem; margin-top: 20px; padding: 12px 25px;">
              زيارة التقييم
            </a>
          </div>

          <div class="review-item">
            <div class="review-logo">
              <i class="fas fa-book"></i>
            </div>
            <h3>My FX Book</h3>
            <p>مراجعة شاملة لأداء الوسيط</p>
            <a class="main-btn" href="https://www.myfxbook.com/reviews/brokers/rannforex/1933426,1" style="font-size: 1rem; margin-top: 20px; padding: 12px 25px;">
              زيارة التقييم
            </a>
          </div>

          <div class="review-item">
            <div class="review-logo">
              <i class="fas fa-shield-alt"></i>
            </div>
            <h3>Forex Peace Army</h3>
            <p>تقييمات من مجتمع المتداولين</p>
            <a class="main-btn" href="https://www.forexpeacearmy.com/forex-reviews/15906/rannforex-review" style="font-size: 1rem; margin-top: 20px; padding: 12px 25px;">
              زيارة التقييم
            </a>
          </div>
        </div>
      </div>
      <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مراجعة شاملة لـ RannForex - تداول العملات والعقود الآجلة</tit

      <!-- Deposit Steps - Modified Layout -->
      <div class="card">
        <div class="card-header">
          <i class="fas fa-money-bill-wave"></i>
          <h2 class="card-title">خطوات الإيداع</h2>
        </div>

        <div class="steps-container">
          <div class="step-item">
            <div class="step-number"></div>
            <div class="step-content">
              <h3>الدخول إلى موقع Rann Forex</h3>
              <p>اضغط على الثلاث خطوط في أعلى يمين الشاشة ثم اختر Deposit</p>
            </div>
          </div>

          <div class="divider">
            <i class="fas fa-arrow-down"></i>
          </div>

          <div class="step-item">
            <div class="step-number"></div>
            <div class="step-content">
              <h3>طريقة الإيداع</h3>
              <p>اختر crypto ثم اختر حساب التداول واضغط Continue</p>
            </div>
          </div>

          <div class="divider">
            <i class="fas fa-arrow-down"></i>
          </div>

          <div class="step-item">
            <div class="step-number"></div>
            <div class="step-content">
              <h3>المبلغ</h3>
              <p>أدخل المبلغ في الفراغ الأول واختر USD ثم اضغط Continue</p>
            </div>
          </div>

          <div class="divider">
            <i class="fas fa-arrow-down"></i>
          </div>

          <div class="step-item">
            <div class="step-number"></div>
            <div class="step-content">
              <h3>المصادقة الثنائية</h3>
              <p>
                ادخل الكود من تطبيق Google Authenticator في الفراغ المخصص ثم
                اضغط Continue
              </p>
            </div>
          </div>

          <div class="divider">
            <i class="fas fa-arrow-down"></i>
          </div>

          <div class="step-item">
            <div class="step-number"></div>
            <div class="step-content">
              <h3>العنوان</h3>
              <p>
                عندما تظهر منصة الدفع ابحث عن tetherus (usdt) ثم bsc-t-usd
                (usdt) ثم انسخ العنوان الذي ظهر لك
              </p>
            </div>
          </div>

          <div class="divider">
            <i class="fas fa-arrow-down"></i>
          </div>

          <div class="step-item">
            <div class="step-number"></div>
            <div class="step-content">
              <h3>من المحفظة</h3>
              <p>
                اذهب إلى Cwallet وأرسل USDT عبر شبكة BEP-20 إلى العنوان الذي
                نسخته
              </p>
            </div>
          </div>
        </div>
      </div>
      
      
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فيديو المصادقة الثنائية - Rann Forex</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            font-family: 'Tajawal', sans-serif;
            background-color: #f5f6fa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }
        
        .video-container {
            text-align: center;
            padding: 30px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            max-width: 500px;
            width: 100%;
            border: 1px solid #e0e0e0;
        }
        
        .video-btn {
            display: inline-block;
            background: linear-gradient(135deg, #FF0000 0%, #CC0000 100%);
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            margin: 20px 0;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(204, 0, 0, 0.2);
            border: none;
            cursor: pointer;
        }
        
        .video-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(204, 0, 0, 0.3);
            background: linear-gradient(135deg, #CC0000 0%, #FF0000 100%);
        }
        
        .video-btn i {
            margin-left: 10px;
        }
        
        h2 {
            color: #0a3d62;
            margin-bottom: 15px;
        }
        
        .video-thumbnail {
            width: 100%;
            border-radius: 10px;
            margin: 15px 0;
            border: 3px solid #f0f0f0;
            transition: transform 0.3s;
            cursor: pointer;
        }
        
        .video-thumbnail:hover {
            transform: scale(1.02);
        }
        
        .video-info {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            margin: 20px 0;
            text-align: right;
        }
    </style>
</head>
<body>
    <div class="video-container">
        <h2><i class="fas fa-lock"></i> فيديو تعليمي</h2>
        <p>شاهد كيفية استخدام تطبيق المصادقة الثنائية (2FA)</p>
        
        <!-- صورة مصغرة للفيديو قابلة للنقر -->
        <a href="https://youtube.com/shorts/SlQc3Q6L3HQ?si=Q5sdG7_lxANoykBs" target="_blank">
            <img src="https://img.youtube.com/vi/SlQc3Q6L3HQ/maxresdefault.jpg" alt="فيديو المصادقة الثنائية" class="video-thumbnail">
        </a>
        
        <!-- زر تشغيل الفيديو -->
        <a href="https://youtube.com/shorts/SlQc3Q6L3HQ?si=Q5sdG7_lxANoykBs" target="_blank" class="video-btn">
            <i class="fab fa-youtube"></i> تشغيل الفيديو
        </a>
        
      
    </div>
</body>
      </html>

      <!-- Contact Section -->
      <div class="card">
        <div class="card-header">
          <i class="fas fa-headset"></i>
          <h2 class="card-title">تواصل معنا</h2>
     

        <div class="contact-info">
          <div class="contact-item" onclick="window.open('https://t.me/ali0619000', '_blank')">
            <i class="fab fa-telegram"></i>
            <div class="contact-content">
              <h3>Telegram</h3>
              <p>@ali0619000</p>
            </div>
          </div>

          <div class="contact-item" onclick="window.open('https://t.me/syriatradingfx', '_blank')">
            <i class="fab fa-telegram"></i>
            <div class="contact-content">
              <h3>قناتنا</h3>
              <p>syriatradingfx</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <footer>
      <div class="container">
        <div class="footer-links">
          <a href="https://t.me/syriatradingfx" target="_blank"><i class="fab fa-telegram"></i></a>
          <a href="https://wa.me/qr/AFVVUP3Z46UYM1" target="_blank"><i class="fab fa-whatsapp"></i></a>
          <a href="https://www.facebook.com/alimahmoud326" target="_blank"><i class="fab fa-facebook"></i></a>
        </div>
        <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اتصل بنا - Rann Forex</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            font-family: 'Tajawal', sans-serif;
            background-color: #f5f6fa;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }
        
        .email-container {
            text-align: center;
            padding: 30px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            max-width: 500px;
            width: 100%;
            border: 1px solid #e0e0e0;
        }
        
        .email-btn {
            display: inline-block;
            background: linear-gradient(135deg, #0a3d62 0%, #1e88e5 100%);
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            margin: 20px 0;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(10, 61, 98, 0.2);
            border: none;
            cursor: pointer;
        }
        
        .email-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(10, 61, 98, 0.3);
            background: linear-gradient(135deg, #1e88e5 0%, #0a3d62 100%);
        }
        
        .email-btn i {
            margin-left: 10px;
        }
        
        h2 {
            color: #0a3d62;
            margin-bottom: 15px;
        }
        
        .email-info {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            margin: 20px 0;
            text-align: right;
            direction: ltr;
        }
        
        .email-info span {
            font-weight: bold;
            color: #1e88e5;
            display: block;
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <div class="email-container">
        <h2><i class="fas fa-envelope-open-text"></i> تواصل مباشر</h2>
        
        
        <!-- الزر الرئيسي مع تحديد البريد في خاصية mailto -->
        <a href="mailto:alimahmoud001a@gmail.com?cc=&bcc=&subject=استفسار عن خدمات Rann Forex&body=السلام عليكم،%0D%0A%0D%0Aأود الاستفسار عن:" class="email-btn">
            <i class="fas fa-paper-plane"></i> إرسال بريد الآن
        </a>
        
        <p style="color: #666; font-size: 0.9rem;">
        راسلني : alimahmoud001a@gmail.com ❤️
        </p>
    </div>
</body>
        </html>
    </div>
</body>
</html>
      
</a>

<style>
.email-button {
  display: inline-block;
  background: #0a3d62;
  color: white;
  padding: 12px 25px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  margin: 10px 0;
  transition: all 0.3s ease;
  font-family: 'Tajawal', sans-serif;
}

.email-button:hover {
  background: #1e88e5;
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

.email-button i {
  margin-left: 8px;
}
</style>
        <p class="footer-text">
          © 2025 Rann Forex. جميع الحقوق محفوظة. التداول في الأسواق المالية
          ينطوي على مخاطر
        </p>
      </div>
    </footer>

    <script>
      // Add animations to elements when they come into view
      document.addEventListener('DOMContentLoaded', function() {
          const animateItems = document.querySelectorAll('.card, .feature-item, .review-item, .step-item, .link-item');

          const observer = new IntersectionObserver((entries) => {
              entries.forEach(entry => {
                  if (entry.isIntersecting) {
                      entry.target.style.opacity = '1';
                      entry.target.style.transform = 'translateY(0)';
                  }
              });
          }, { threshold: 0.1 });

          animateItems.forEach(item => {
              item.style.opacity = '0';
              item.style.transform = 'translateY(20px)';
              item.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
              observer.observe(item);
          });

          // Button pulse animation
          const mainBtn = document.querySelector('.main-btn');
          if (mainBtn) {
              setInterval(() => {
                  mainBtn.style.boxShadow = '0 0 0 0 rgba(0, 184, 148, 0.7)';
                  setTimeout(() => {
                      mainBtn.style.boxShadow = '0 0 0 10px rgba(0, 184, 148, 0)';
                  }, 500);
              }, 2000);
          }
      });
    </script>
  </body>
</html>
