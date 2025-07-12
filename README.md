<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>قائمة جانبية متكاملة</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f5f5f5;
            overflow-x: hidden;
        }
        
        /* هيكل الصفحة الرئيسي */
        .page-wrapper {
            display: flex;
            min-height: 100vh;
            transition: all 0.3s ease;
        }
        
        /* تصميم القائمة الجانبية */
        .sidebar {
            width: 280px;
            background-color: #2c3e50;
            color: white;
            height: 100vh;
            position: fixed;
            right: 0;
            top: 0;
            transition: all 0.3s ease;
            z-index: 1000;
            box-shadow: -2px 0 15px rgba(0,0,0,0.1);
        }
        
        .sidebar-header {
            padding: 20px;
            background-color: #1a252f;
            text-align: center;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #34495e;
        }
        
        .sidebar-toggle {
            background: none;
            border: none;
            color: white;
            font-size: 24px;
            cursor: pointer;
            padding: 5px;
            transition: all 0.3s;
        }
        
        .sidebar-toggle:hover {
            transform: scale(1.1);
        }
        
        .sidebar-menu {
            padding: 0;
            list-style: none;
            overflow-y: auto;
            height: calc(100vh - 70px);
        }
        
        .menu-item {
            border-bottom: 1px solid #34495e;
            transition: all 0.3s;
        }
        
        .menu-item:hover {
            background-color: #34495e;
        }
        
        .menu-link {
            padding: 16px 25px;
            display: block;
            color: white;
            text-decoration: none;
            transition: all 0.3s;
            cursor: pointer;
            font-size: 16px;
        }
        
        .menu-link.active {
            background-color: #3498db;
            border-right: 4px solid #2980b9;
        }
        
        /* تصميم حاوية المحتوى */
        .content-container {
            flex: 1;
            padding: 25px;
            margin-right: 280px;
            transition: all 0.3s ease;
            min-height: 100vh;
        }
        
        .content-iframe {
            width: 100%;
            height: calc(100vh - 50px);
            border: none;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        
        /* حالة القائمة المغلقة */
        .sidebar.collapsed {
            right: -280px;
        }
        
        .sidebar.collapsed + .content-container {
            margin-right: 0;
        }
        
        /* زر القائمة للجوال */
        .mobile-menu-btn {
            position: fixed;
            right: 20px;
            top: 20px;
            background-color: #2c3e50;
            color: white;
            border: none;
            padding: 12px;
            cursor: pointer;
            border-radius: 5px;
            z-index: 999;
            display: none;
            font-size: 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            transition: all 0.3s;
        }
        
        .mobile-menu-btn:hover {
            background-color: #34495e;
        }
        
        /* تصميم متجاوب للشاشات الصغيرة */
        @media (max-width: 992px) {
            .sidebar {
                width: 250px;
            }
            
            .content-container {
                margin-right: 0;
                padding: 20px;
            }
        }
        
        @media (max-width: 768px) {
            .sidebar {
                right: -250px;
                width: 250px;
            }
            
            .sidebar.active {
                right: 0;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .content-container {
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- زر القائمة للجوال -->
    <button class="mobile-menu-btn" id="mobileMenuBtn">☰</button>
    
    <div class="page-wrapper">
        <!-- القائمة الجانبية -->
        <div class="sidebar" id="sidebar">
            <div class="sidebar-header">
                <h2 style="margin: 0; font-size: 20px;">قائمة الموقع</h2>
                <button class="sidebar-toggle" id="sidebarToggle">×</button>
            </div>
            <ul class="sidebar-menu" id="sidebarMenu">
                <!-- ********** هنا ضع روابطك الخاصة ********** -->
                <!-- مثال: -->
                <li class="menu-item">
                    <a class="menu-link" data-link="index.html">الصفحة الرئيسية</a>
                </li>
                <li class="menu-item">
                    <a class="menu-link" data-link="about.html">من نحن</a>
                </li>
                <li class="menu-item">
                    <a class="menu-link" data-link="services.html">خدماتنا</a>
                </li>
                <li class="menu-item">
                    <a class="menu-link" data-link="products.html">منتجاتنا</a>
                </li>
                <li class="menu-item">
                    <a class="menu-link" data-link="contact.html">اتصل بنا</a>
                </li>
                <!-- يمكنك إضافة المزيد من الروابط هنا -->
            </ul>
        </div>
        
        <!-- حاوية المحتوى -->
        <div class="content-container">
            <iframe class="content-iframe" id="contentFrame" src="about:blank" title="محتوى الموقع"></iframe>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const menuLinks = document.querySelectorAll('.menu-link');
            const sidebar = document.getElementById('sidebar');
            const sidebarToggle = document.getElementById('sidebarToggle');
            const mobileMenuBtn = document.getElementById('mobileMenuBtn');
            const contentFrame = document.getElementById('contentFrame');
            
            // فتح الرابط في الحاوية عند النقر على عنصر القائمة
            menuLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const linkUrl = this.getAttribute('data-link');
                    if (linkUrl) {
                        contentFrame.src = linkUrl;
                    }
                    
                    // إزالة التنشيط من جميع العناصر وإضافته للعنصر الحالي
                    menuLinks.forEach(item => item.classList.remove('active'));
                    this.classList.add('active');
                    
                    // إغلاق القائمة تلقائياً على الجوال
                    if (window.innerWidth <= 768) {
                        sidebar.classList.remove('active');
                    }
                });
            });
            
            // زر إغلاق/فتح القائمة (في الشريط الجانبي)
            sidebarToggle.addEventListener('click', function() {
                if (window.innerWidth > 768) {
                    sidebar.classList.toggle('collapsed');
                } else {
                    sidebar.classList.remove('active');
                }
            });
            
            // زر القائمة للجوال
            mobileMenuBtn.addEventListener('click', function() {
                sidebar.classList.toggle('active');
            });
            
            // فتح أول رابط افتراضياً عند تحميل الصفحة
            if (menuLinks.length > 0) {
                const firstLink = menuLinks[0].getAttribute('data-link');
                if (firstLink) {
                    contentFrame.src = firstLink;
                    menuLinks[0].classList.add('active');
                }
            }
            
            // إغلاق القائمة عند النقر خارجها على الجوال
            document.addEventListener('click', function(e) {
                if (window.innerWidth <= 768 && 
                    !sidebar.contains(e.target) && 
                    e.target !== mobileMenuBtn) {
                    sidebar.classList.remove('active');
                }
            });
            
            // تعديل الحجم عند تغيير حجم النافذة
            window.addEventListener('resize', function() {
                if (window.innerWidth > 768) {
                    sidebar.classList.remove('active');
                    sidebar.classList.remove('collapsed');
                } else {
                    if (!sidebar.classList.contains('active')) {
                        sidebar.classList.add('collapsed');
                    }
                }
            });

            // تهيئة أولية للزر حسب حجم الشاشة
            if (window.innerWidth <= 768) {
                mobileMenuBtn.style.display = 'block';
                sidebar.classList.add('collapsed');
            }
        });
    </script>
</body>
</html>
