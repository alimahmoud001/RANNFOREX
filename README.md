
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل المتداول</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #2c3e50; /* Dark Blue/Grey */
            --secondary-color: #34495e; /* Slightly Lighter Dark Blue/Grey */
            --accent-color: #3498db; /* Bright Blue */
            --text-color: #ecf0f1; /* Light Grey */
            --light-bg: #ecf0f1; /* Very Light Grey */
            --dark-text: #2c3e50; /* Dark text for light backgrounds */
            --border-color: #7f8c8d; /* Grey border */
        }

        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--primary-color);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        header {
            background-color: var(--secondary-color);
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            position: relative;
        }

        h1 {
            color: var(--accent-color);
            font-size: 2.5em;
            margin: 0;
            font-weight: 700;
        }

        .menu-button {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 10px 15px;
            font-size: 1.2em;
            cursor: pointer;
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1001;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }

        .sidebar {
            height: 100%;
            width: 0;
            position: fixed;
            z-index: 1000;
            top: 0;
            right: 0;
            background-color: var(--secondary-color);
            overflow-x: hidden;
            transition: 0.5s;
            padding-top: 60px;
            box-shadow: -2px 0 5px rgba(0, 0, 0, 0.2);
        }

        .sidebar a {
            padding: 15px 25px;
            text-decoration: none;
            font-size: 1.2em;
            color: var(--text-color);
            display: block;
            transition: 0.3s;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .sidebar a:hover {
            background-color: var(--accent-color);
            color: white;
        }

        .sidebar .closebtn {
            position: absolute;
            top: 0;
            left: 25px;
            font-size: 36px;
            margin-left: 50px;
            color: var(--text-color);
        }

        .main-content {
            margin-right: 0;
            padding: 20px;
            transition: margin-right .5s;
        }

        section {
            background-color: var(--secondary-color);
            margin: 20px 0;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }

        h2 {
            color: var(--accent-color);
            font-size: 2em;
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 10px;
            margin-bottom: 20px;
            font-weight: 700;
        }

        h3 {
            color: var(--accent-color);
            font-size: 1.5em;
            margin-top: 25px;
            margin-bottom: 15px;
        }

        ul {
            list-style: none;
            padding: 0;
        }

        li {
            margin-bottom: 10px;
        }

        a {
            color: var(--accent-color);
            text-decoration: none;
            transition: color 0.3s;
        }

        a:hover {
            color: #61dafb; /* Lighter accent on hover */
        }

        .feature-list li {
            position: relative;
            padding-right: 25px;
            margin-bottom: 10px;
            font-size: 1.1em;
        }

        .feature-list li::before {
            content: '★';
            color: var(--accent-color);
            position: absolute;
            right: 0;
            font-size: 1.2em;
            line-height: 1;
        }

        .note {
            background-color: #f39c12; /* Orange */
            color: white;
            padding: 10px;
            border-radius: 5px;
            margin-top: 15px;
            font-weight: bold;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: var(--text-color);
        }

        .form-group input[type="text"],
        .form-group input[type="number"],
        .form-group textarea,
        .form-group select {
            width: calc(100% - 20px);
            padding: 10px;
            border: 1px solid var(--border-color);
            border-radius: 5px;
            background-color: var(--light-bg);
            color: var(--dark-text);
            font-size: 1em;
            box-sizing: border-box;
        }

        .form-group input[type="radio"] {
            margin-left: 10px;
        }

        .button {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1em;
            transition: background-color 0.3s;
            margin-top: 10px;
        }

        .button:hover {
            background-color: #2980b9; /* Darker blue on hover */
        }

        .result-box {
            background-color: var(--primary-color);
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            border: 1px solid var(--accent-color);
        }

        .result-box p {
            margin: 5px 0;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            color: var(--dark-text);
        }

        table th, table td {
            border: 1px solid var(--border-color);
            padding: 10px;
            text-align: right;
            background-color: var(--light-bg);
        }

        table th {
            background-color: var(--accent-color);
            color: white;
            font-weight: bold;
        }

        .copy-address {
            cursor: pointer;
            color: var(--accent-color);
            text-decoration: underline;
            font-weight: bold;
        }

        .copy-address:hover {
            color: #61dafb;
        }

        .floating-icons {
            position: fixed;
            bottom: 20px;
            left: 20px;
            display: flex;
            flex-direction: column;
            gap: 15px;
            z-index: 999;
        }

        .floating-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background-color: var(--accent-color);
            border-radius: 50%;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s, background-color 0.3s;
        }

        .floating-icons a:hover {
            transform: scale(1.1);
            background-color: #2980b9;
        }

        .floating-icons img {
            width: 30px;
            height: 30px;
            filter: invert(100%); /* Make icons white */
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }
            h2 {
                font-size: 1.8em;
            }
            .sidebar {
                width: 250px; /* Full width for mobile */
            }
            .main-content {
                margin-right: 0; /* No push for mobile */
            }
            .menu-button {
                top: 15px;
                right: 15px;
                padding: 8px 12px;
                font-size: 1em;
            }
        }

        @media (min-width: 769px) {
            .sidebar {
                width: 300px;
            }
            .main-content.shifted {
                margin-right: 300px;
            }
        }
    </style>
</head>
<body>

    <button class="menu-button" onclick="toggleSidebar()">☰ القائمة</button>

    <div id="mySidebar" class="sidebar">
        <a href="javascript:void(0)" class="closebtn" onclick="closeSidebar()">×</a>
        <a href="#home" onclick="navigateTo('home')">دليل المتداول</a>
        <a href="#brokerage" onclick="navigateTo('brokerage')">شركة الوساطة المالية</a>
        <a href="#apps" onclick="navigateTo('apps')">تطبيقات يجب تحميلها</a>
        <a href="#telegram" onclick="navigateTo('telegram')">قسم التلجرام</a>
        <a href="#education" onclick="navigateTo('education')">القسم التعليمي</a>
        <a href="#capital-calculator" onclick="navigateTo('capital-calculator')">حاسبة تطور رأس المال</a>
        <a href="#usdt-exchange" onclick="navigateTo('usdt-exchange')">شراء وبيع USDT</a>
    </div>

    <div id="main" class="main-content">
        <header>
            <h1 id="home">دليل المتداول</h1>
        </header>

        <section id="brokerage">
            <h2>شركة الوساطة المالية</h2>
            <p>⬅️ <a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1" target="_blank">رابط شركة الوساطة المالية</a></p>
            <h3>ميزاتها:</h3>
            <ul class="feature-list">
                <li>اقل ايداع او سحب 10$ خلال 30 ثانية</li>
                <li>اسبريد 0.2~1.2 ورافعة مالية 500:1</li>
                <li>تداول آمن على جميع ازواج الفوريكس والمعادن والنفط والمؤشرات والعملات المشفرة</li>
                <li>حسابات إسلامية خالية من العمولة</li>
                <li>حسابات احترافية اسبريد قليل جدا</li>
                <li>انزلاق منخفض وتنفيذ فوري للصفقات</li>
                <li>تقييم ممتاز على موقع trust pilot & myfxbook & wikifx & Forex peace army يمكنك الاطلاع بنفسك</li>
                <li>الأمان عالي جدا بسبب 2FA</li>
                <li>توثيق سريع وسهل</li>
                <li>نموذج A Book من افضل مزودي السيولة</li>
            </ul>
            <p>⬅️ <a href="https://rannforex.com/en/trading/quotesonline/" target="_blank">rannforex اسبريد للاطلاع على الاسبريد المتوسط اليومي</a></p>
        </section>

        <section id="apps">
            <h2>تطبيقات يجب تحميلها للبدء بالتداول</h2>
            <h3>منصة ميتا تريدر 5</h3>
            <p>⬅️ <a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5" target="_blank">رابط تحميل ميتا تريدر 5</a></p>
            <div class="note">ملاحظة: هي المنصة الموثوقة الأفضل في مجال التداول في جميع الأسواق.</div>

            <h3>المحفظة الإلكترونية</h3>
            <p>⬅️ <a href="https://www.binance.com/activity/referral-entry/CPA?ref=CPA_004C6HBMJS" target="_blank">باينانس</a></p>

            <h3>تطبيق المصادقة الثنائية</h3>
            <p>⬅️ <a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2" target="_blank">Google Authenticator</a></p>

            <h3>تطبيق التحليل</h3>
            <p>⬅️ <a href="https://play.google.com/store/apps/details?id=com.tradingview.tradingviewapp" target="_blank">TradingView</a></p>
        </section>

        <section id="telegram">
            <h2>قسم التلجرام</h2>
            <p>باشتراك شهري 30 دولار يمكنك الدخول الى القنوات الخاصة بي التالية:</p>
            <ul>
                <li>قناة الإشارات: <a href="https://t.me/tradewithali002" target="_blank">https://t.me/tradewithali002</a></li>
                <li>قناة الكورس: <a href="https://t.me/tradewithali003" target="_blank">https://t.me/tradewithali003</a></li>
            </ul>
            <h3>قناتي العامة إشارات مجانية بدون اشتراك:</h3>
            <ul>
                <li><a href="https://t.me/Tradewithali001" target="_blank">https://t.me/Tradewithali001</a></li>
            </ul>
            <h3>مجتمعنا:</h3>
            <ul>
                <li><a href="https://t.me/SyriaTradingFXg" target="_blank">https://t.me/SyriaTradingFXg</a></li>
            </ul>
        </section>

        <section id="education">
            <h2>القسم التعليمي</h2>
            <ul>
                <li>⬅️ كورس كامل لتعلم التداول مع اشهر ملياردير عبقري التداول باتك: <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">رابط الكورس (مثال)</a></li>
                <li>⬅️ قناة أخرى على يوتيوب: <a href="https://www.youtube.com/channel/UC-x_y_z_a_b_c_d" target="_blank">رابط القناة (مثال)</a></li>
                <li>⬅️ كورس اخر على انستغرام: <a href="https://www.instagram.com/kameel_m5?igsh=YzljYTk1ODg3Zg==" target="_blank">Kameel M5</a></li>
                <li>كورس على يوتيوب Smart Risk: <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">رابط الكورس (مثال)</a></li>
            </ul>
        </section>

        <section id="capital-calculator">
            <h2>حاسبة تطور رأس المال</h2>
            <p>صمم كود يحسب معدل تطور رأس المال في التداول.</p>
            <div class="form-group">
                <label for="initialCapital">رأس المال الأولي ($):</label>
                <input type="number" id="initialCapital" value="1000" min="1" step="0.01">
            </div>
            <div class="form-group">
                <label for="winRate">نسبة الصفقات الرابحة (%):</label>
                <input type="number" id="winRate" value="50" min="0" max="100" step="0.1">
            </div>
            <div class="form-group">
                <label for="profitPerTrade">معدل الربح لكل صفقة (% من رأس المال):</label>
                <input type="number" id="profitPerTrade" value="2" min="0.01" step="0.01">
            </div>
            <div class="form-group">
                <label for="lossPerTrade">معدل الخسارة في كل صفقة (% من رأس المال):</label>
                <input type="number" id="lossPerTrade" value="1" min="0.01" step="0.01">
            </div>
            <div class="form-group">
                <label for="tradesPerUpdate">عدد الصفقات لكل تحديث عرض (X):</label>
                <input type="number" id="tradesPerUpdate" value="10" min="1" step="1">
            </div>
            <div class="form-group">
                <label for="targetCapital">الهدف النهائي لرأس المال ($):</label>
                <input type="number" id="targetCapital" value="10000" min="1" step="0.01">
            </div>
            <button class="button" onclick="calculateCapitalGrowth()">حساب تطور رأس المال</button>

            <div class="result-box" id="capitalGrowthResults" style="display:none;">
                <h3>النتائج المحسوبة:</h3>
                <p><strong>متوسط العائد لكل صفقة:</strong> <span id="avgReturnPerTrade"></span>%</p>
                <p><strong>عدد الصفقات المطلوبة للهدف:</strong> <span id="tradesNeeded"></span> صفقة</p>
                <p><strong>معدل النمو الإجمالي (تقديري):</strong> <span id="totalGrowthRate"></span>%</p>

                <h3>جدول تطور رأس المال:</h3>
                <table id="capitalGrowthTable">
                    <thead>
                        <tr>
                            <th>عدد الصفقات</th>
                            <th>رأس المال</th>
                        </tr>
                    </thead>
                    <tbody>
                        </tbody>
                </table>

                <h3>مخطط تطور رأس المال:</h3>
                <p>للحصول على مخطط بياني تفاعلي، يمكنك استخدام مكتبات JavaScript مثل Chart.js. البيانات أدناه جاهزة للاستخدام:</p>
                <pre id="chartData"></pre>
                <canvas id="capitalChart" style="background-color: white; border-radius: 5px; margin-top: 15px;"></canvas>
                <p style="font-size: 0.8em; color: var(--dark-text); background-color: var(--light-bg); padding: 10px; border-radius: 5px;">
                    <strong>ملاحظة:</strong> لعرض المخطط البياني بشكل تفاعلي وجميل، ستحتاج إلى تضمين مكتبة Chart.js في صفحتك وإضافة كود JavaScript لإنشاء المخطط باستخدام البيانات المولدة.
                </p>
            </div>
        </section>

        <section id="usdt-exchange">
            <h2>شراء وبيع USDT</h2>
            <p>تحويل USDT بوسائل الدفع المتاحة في سوريا.</p>
            <div class="form-group">
                <label for="fullName">الاسم الثلاثي:</label>
                <input type="text" id="fullName" placeholder="الاسم الثلاثي" required>
            </div>
            <div class="form-group">
                <label for="phoneNumber">رقم الهاتف:</label>
                <input type="text" id="phoneNumber" placeholder="رقم الهاتف" required>
            </div>
            <div class="form-group">
                <label for="city">المدينة:</label>
                <input type="text" id="city" placeholder="المدينة" required>
            </div>

            <div class="form-group">
                <label>ماذا تريد؟</label><br>
                <input type="radio" id="buyUSDT" name="transactionType" value="buy" onchange="showTransactionFields()">
                <label for="buyUSDT">شراء USDT</label><br>
                <input type="radio" id="sellUSDT" name="transactionType" value="sell" onchange="showTransactionFields()">
                <label for="sellUSDT">بيع USDT</label>
            </div>

            <div id="buyFields" style="display:none;">
                <h3>شراء USDT</h3>
                <div class="form-group">
                    <label for="buyAmount">الكمية المطلوبة من USDT:</label>
                    <input type="number" id="buyAmount" min="1" step="0.01" oninput="calculateBuyAmount()">
                </div>
                <div class="form-group">
                    <label for="buyNetwork">اختر الشبكة:</label>
                    <select id="buyNetwork" onchange="calculateBuyAmount()">
                        <option value="">اختر شبكة</option>
                        <option value="bep20">BEP20</option>
                        <option value="trc20">TRC20</option>
                        <option value="erc20">ERC20</option>
                        <option value="binance_pay">Binance Pay</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="buyAddress">عنوان المحفظة (يكتبه المستخدم):</label>
                    <input type="text" id="buyAddress" placeholder="عنوان محفظة USDT" required>
                </div>
                <div class="form-group">
                    <label for="buyNote">ملاحظة (اختياري):</label>
                    <textarea id="buyNote" rows="3" placeholder="أضف أي ملاحظات هنا"></textarea>
                </div>
                <div class="form-group">
                    <label for="paymentMethodBuy">طريقة الدفع (الليرة السورية):</label>
                    <select id="paymentMethodBuy" onchange="showPaymentDetails()">
                        <option value="">اختر طريقة الدفع</option>
                        <option value="sham_cash">شام كاش</option>
                        <option value="bemo_bank">بنك بيمو</option>
                        <option value="syriatel_cash">سيريتل كاش</option>
                        <option value="harram_transfer">حوالة الهرم</option>
                    </select>
                </div>
                <div id="paymentDetails" class="result-box" style="display:none; background-color: var(--light-bg); color: var(--dark-text);">
                    <h3>تفاصيل الدفع:</h3>
                    <p id="paymentDetailsContent"></p>
                    <p class="note" style="background-color: #f1c40f; color: var(--dark-text);">
                        عمولة التسديد على طرق التحويل المختلفة بالليرة السورية تقع على المستخدم كما تحددها هذه الجهات.
                    </p>
                </div>
                <div id="buySummary" class="result-box" style="display:none;">
                    <h3>مراجعة الطلب (شراء USDT):</h3>
                    <p>الكمية المطلوبة: <span id="summaryBuyAmount"></span> USDT</p>
                    <p>الشبكة: <span id="summaryBuyNetwork"></span></p>
                    <p>عمولة التحويل: <span id="summaryBuyFee"></span> $</p>
                    <p id="summaryTrc20Fee" style="display:none;">عمولة شبكة TRC20 إضافية: 2$</p>
                    <p><strong>المبلغ الإجمالي المستحق بالدولار:</strong> <span id="summaryBuyTotalUSD"></span> $</p>
                    <p><strong>المبلغ الإجمالي المستحق بالليرة السورية:</strong> <span id="summaryBuyTotalSYP"></span> ل.س</p>
                </div>
                <button class="button" onclick="submitUSDTRequest('buy')">إرسال طلب الشراء</button>
            </div>

            <div id="sellFields" style="display:none;">
                <h3>بيع USDT</h3>
                <div class="form-group">
                    <label for="sellAmount">الكمية المراد بيعها من USDT:</label>
                    <input type="number" id="sellAmount" min="1" step="0.01" oninput="calculateSellAmount()">
                </div>
                <div class="form-group">
                    <label for="sellNetwork">اختر الشبكة التي ستبيع منها:</label>
                    <select id="sellNetwork" onchange="showSellAddress()">
                        <option value="">اختر شبكة</option>
                        <option value="bep20">BEP20</option>
                        <option value="trc20">TRC20</option>
                        <option value="erc20">ERC20</option>
                        <option value="binance_pay">Binance Pay</option>
                    </select>
                </div>
                <div id="sellCryptoAddress" class="result-box" style="display:none; background-color: var(--light-bg); color: var(--dark-text);">
                    <h3>عنوان محفظتنا لاستلام USDT:</h3>
                    <p id="sellAddressContent"></p>
                </div>
                <div class="form-group">
                    <label for="sellNote">ملاحظة (اختياري):</label>
                    <textarea id="sellNote" rows="3" placeholder="أضف أي ملاحظات هنا"></textarea>
                </div>
                <div class="form-group">
                    <label for="paymentMethodSell">طريقة الاستلام (الليرة السورية):</label>
                    <select id="paymentMethodSell">
                        <option value="">اختر طريقة الاستلام</option>
                        <option value="syriatel_cash">سيريتل كاش</option>
                        <option value="harram_transfer">حوالة الهرم</option>
                        <option value="bemo_bank">بنك بيمو</option>
                        <option value="sham_cash">شام كاش</option>
                    </select>
                </div>
                <div id="additionalSellDetails" class="form-group" style="display:none;">
                    <label for="bankAccountNum">رقم الحساب البنكي / عنوان الحساب (لـ بنك بيمو / شام كاش):</label>
                    <input type="text" id="bankAccountNum" placeholder="رقم الحساب أو عنوان الحساب">
                </div>
                <div id="sellSummary" class="result-box" style="display:none;">
                    <h3>مراجعة الطلب (بيع USDT):</h3>
                    <p>الكمية المراد بيعها: <span id="summarySellAmount"></span> USDT</p>
                    <p>الشبكة: <span id="summarySellNetwork"></span></p>
                    <p>عمولة التحويل: <span id="summarySellFee"></span> $</p>
                    <p id="summarySellTrc20Fee" style="display:none;">عمولة شبكة TRC20 إضافية: 2$</p>
                    <p><strong>المبلغ الإجمالي المستحق بالدولار:</strong> <span id="summarySellTotalUSD"></span> $</p>
                    <p><strong>المبلغ الإجمالي المستحق بالليرة السورية:</strong> <span id="summarySellTotalSYP"></span> ل.س</p>
                </div>
                <button class="button" onclick="submitUSDTRequest('sell')">إرسال طلب البيع</button>
            </div>
            <div id="requestStatus" class="result-box" style="display:none;"></div>
        </section>
    </div>

    <div class="floating-icons">
        <a href="https://t.me/ali0619000" target="_blank" title="تواصل عبر التلجرام">
            <img src="https://upload.wikimedia.org/wikipedia/commons/8/82/Telegram_logo.svg" alt="Telegram">
        </a>
        <a href="mailto:alimahmoud001a@gmail.com" title="تواصل عبر البريد الإلكتروني">
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Gmail_icon_%282020%29.svg" alt="Email">
        </a>
    </div>

    <script>
        const EXCHANGE_RATE = 10000; // سعر الصرف الحالي 1 دولار = 10000 ليرة سورية
        const BASE_FEE_USD = 1; // عمولة التحويل الثابتة بالدولار
        const PERCENTAGE_FEE_RATE = 0.005; // 0.5% عمولة نسبة مئوية
        const TRC20_NETWORK_FEE = 2; // عمولة شبكة TRC20 الإضافية

        function toggleSidebar() {
            const sidebar = document.getElementById("mySidebar");
            const mainContent = document.getElementById("main");
            if (sidebar.style.width === "0px" || sidebar.style.width === "") {
                sidebar.style.width = "300px";
                if (window.innerWidth > 768) {
                    mainContent.classList.add('shifted');
                }
            } else {
                sidebar.style.width = "0";
                if (window.innerWidth > 768) {
                    mainContent.classList.remove('shifted');
                }
            }
        }

        function closeSidebar() {
            document.getElementById("mySidebar").style.width = "0";
            if (window.innerWidth > 768) {
                document.getElementById("main").classList.remove('shifted');
            }
        }

        function navigateTo(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: 'smooth' });
                closeSidebar();
            }
        }

        // Capital Growth Calculator Functions
        function calculateCapitalGrowth() {
            const initialCapital = parseFloat(document.getElementById('initialCapital').value);
            const winRate = parseFloat(document.getElementById('winRate').value) / 100;
            const profitPerTrade = parseFloat(document.getElementById('profitPerTrade').value) / 100;
            const lossPerTrade = parseFloat(document.getElementById('lossPerTrade').value) / 100;
            const tradesPerUpdate = parseInt(document.getElementById('tradesPerUpdate').value);
            const targetCapital = parseFloat(document.getElementById('targetCapital').value);

            if (isNaN(initialCapital) || isNaN(winRate) || isNaN(profitPerTrade) || isNaN(lossPerTrade) || isNaN(tradesPerUpdate) || isNaN(targetCapital) || initialCapital <= 0 || tradesPerUpdate <= 0 || targetCapital <= 0) {
                alert('الرجاء إدخال قيم صحيحة لجميع الحقول.');
                return;
            }

            let currentCapital = initialCapital;
            let totalTrades = 0;
            const capitalHistory = [{ trades: 0, capital: initialCapital }];
            let maxIterations = 10000; // Prevent infinite loops

            // Calculate average return per trade
            const avgReturnPerTrade = (winRate * profitPerTrade) - ((1 - winRate) * lossPerTrade);
            document.getElementById('avgReturnPerTrade').textContent = (avgReturnPerTrade * 100).toFixed(2);

            // Simulate growth
            while (currentCapital < targetCapital && totalTrades < maxIterations) {
                totalTrades++;
                const isWin = Math.random() < winRate;
                if (isWin) {
                    currentCapital += currentCapital * profitPerTrade;
                } else {
                    currentCapital -= currentCapital * lossPerTrade;
                }

                if (currentCapital <= 0) { // Capital depleted
                    currentCapital = 0;
                    break;
                }

                if (totalTrades % tradesPerUpdate === 0) {
                    capitalHistory.push({ trades: totalTrades, capital: currentCapital });
                }
            }

            // Ensure the target or final state is included if not already
            if (capitalHistory[capitalHistory.length - 1].trades !== totalTrades || capitalHistory[capitalHistory.length - 1].capital !== currentCapital) {
                capitalHistory.push({ trades: totalTrades, capital: currentCapital });
            }


            document.getElementById('tradesNeeded').textContent = totalTrades >= maxIterations ? 'أكثر من ' + maxIterations : totalTrades;
            document.getElementById('totalGrowthRate').textContent = ((currentCapital / initialCapital - 1) * 100).toFixed(2);

            // Populate table
            const tableBody = document.getElementById('capitalGrowthTable').getElementsByTagName('tbody')[0];
            tableBody.innerHTML = '';
            capitalHistory.forEach(data => {
                const row = tableBody.insertRow();
                const cell1 = row.insertCell(0);
                const cell2 = row.insertCell(1);
                cell1.textContent = data.trades;
                cell2.textContent = data.capital.toFixed(2) + '$';
            });

            // Prepare chart data (for Chart.js if integrated)
            const chartLabels = capitalHistory.map(data => data.trades);
            const chartDataPoints = capitalHistory.map(data => data.capital.toFixed(2));
            document.getElementById('chartData').textContent = JSON.stringify({ labels: chartLabels, data: chartDataPoints }, null, 2);

            document.getElementById('capitalGrowthResults').style.display = 'block';

            // Placeholder for Chart.js integration (example, requires Chart.js library)
            /*
            const ctx = document.getElementById('capitalChart').getContext('2d');
            if (window.myCapitalChart) {
                window.myCapitalChart.destroy();
            }
            window.myCapitalChart = new Chart(ctx, {
                type: 'line',
                data: {
                    labels: chartLabels,
                    datasets: [{
                        label: 'تطور رأس المال',
                        data: chartDataPoints,
                        borderColor: '#3498db',
                        backgroundColor: 'rgba(52, 152, 219, 0.2)',
                        borderWidth: 2,
                        fill: true,
                        tension: 0.1
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    scales: {
                        x: {
                            title: {
                                display: true,
                                text: 'عدد الصفقات',
                                color: 'var(--dark-text)'
                            },
                            ticks: { color: 'var(--dark-text)' }
                        },
                        y: {
                            title: {
                                display: true,
                                text: 'رأس المال ($)',
                                color: 'var(--dark-text)'
                            },
                            ticks: { color: 'var(--dark-text)' }
                        }
                    },
                    plugins: {
                        legend: {
                            labels: {
                                color: 'var(--dark-text)'
                            }
                        }
                    }
                }
            });
            */
        }


        // USDT Buy/Sell Functions
        function showTransactionFields() {
            const buyFields = document.getElementById('buyFields');
            const sellFields = document.getElementById('sellFields');
            const requestStatus = document.getElementById('requestStatus');

            buyFields.style.display = 'none';
            sellFields.style.display = 'none';
            requestStatus.style.display = 'none';

            if (document.getElementById('buyUSDT').checked) {
                buyFields.style.display = 'block';
                document.getElementById('buySummary').style.display = 'none';
                document.getElementById('paymentDetails').style.display = 'none';
            } else if (document.getElementById('sellUSDT').checked) {
                sellFields.style.display = 'block';
                document.getElementById('sellSummary').style.display = 'none';
                document.getElementById('sellCryptoAddress').style.display = 'none';
                document.getElementById('additionalSellDetails').style.display = 'none';
            }
        }

        function calculateBuyAmount() {
            const amount = parseFloat(document.getElementById('buyAmount').value);
            const network = document.getElementById('buyNetwork').value;
            const summaryDiv = document.getElementById('buySummary');
            const trc20FeeSpan = document.getElementById('summaryTrc20Fee');

            if (isNaN(amount) || amount <= 0) {
                summaryDiv.style.display = 'none';
                return;
            }

            let totalFeeUSD = BASE_FEE_USD + (amount * PERCENTAGE_FEE_RATE);
            if (network === 'trc20') {
                totalFeeUSD += TRC20_NETWORK_FEE;
                trc20FeeSpan.style.display = 'block';
            } else {
                trc20FeeSpan.style.display = 'none';
            }

            const totalUSD = amount + totalFeeUSD;
            const totalSYP = totalUSD * EXCHANGE_RATE;

            document.getElementById('summaryBuyAmount').textContent = amount.toFixed(2);
            document.getElementById('summaryBuyNetwork').textContent = network.toUpperCase().replace('_', ' ');
            document.getElementById('summaryBuyFee').textContent = totalFeeUSD.toFixed(2);
            document.getElementById('summaryBuyTotalUSD').textContent = totalUSD.toFixed(2);
            document.getElementById('summaryBuyTotalSYP').textContent = totalSYP.toFixed(2);
            summaryDiv.style.display = 'block';
        }

        function showPaymentDetails() {
            const method = document.getElementById('paymentMethodBuy').value;
            const detailsDiv = document.getElementById('paymentDetails');
            const detailsContent = document.getElementById('paymentDetailsContent');

            detailsDiv.style.display = 'block';
            detailsContent.innerHTML = '';

            let addressToCopy = '';

            switch (method) {
                case 'sham_cash':
                    detailsContent.innerHTML = `
                        <p><strong>عنوان المحفظة:</strong> <span class="copy-address" data-copy="be456e0ea9392db4d68a7093ee317bc8">be456e0ea9392db4d68a7093ee317bc8</span></p>
                        <p><strong>رقم الحساب:</strong> <span class="copy-address" data-copy="5991161126028260">5991161126028260</span></p>
                    `;
                    break;
                case 'syriatel_cash':
                    detailsContent.innerHTML = `<p><strong>عنواني:</strong> <span class="copy-address" data-copy="0934598967">0934598967</span></p>`;
                    break;
                case 'harram_transfer':
                    detailsContent.innerHTML = `
                        <p><strong>الاسم:</strong> علي ابراهيم محمود</p>
                        <p><strong>رقم الهاتف:</strong> <span class="copy-address" data-copy="0934598967">0934598967</span></p>
                        <p><strong>المدينة:</strong> اللاذقية</p>
                    `;
                    break;
                case 'bemo_bank':
                    detailsContent.innerHTML = `
                        <p><strong>الاسم:</strong> علي ابراهيم محمود</p>
                        <p><strong>رقم الحساب البنكي:</strong> <span class="copy-address" data-copy="060104947910013000000">060104947910013000000</span></p>
                    `;
                    break;
                default:
                    detailsDiv.style.display = 'none';
                    break;
            }
            addCopyListeners();
        }

        function calculateSellAmount() {
            const amount = parseFloat(document.getElementById('sellAmount').value);
            const network = document.getElementById('sellNetwork').value;
            const summaryDiv = document.getElementById('sellSummary');
            const trc20FeeSpan = document.getElementById('summarySellTrc20Fee');

            if (isNaN(amount) || amount <= 0) {
                summaryDiv.style.display = 'none';
                return;
            }

            let totalFeeUSD = BASE_FEE_USD + (amount * PERCENTAGE_FEE_RATE);
            if (network === 'trc20') {
                totalFeeUSD += TRC20_NETWORK_FEE;
                trc20FeeSpan.style.display = 'block';
            } else {
                trc20FeeSpan.style.display = 'none';
            }

            const totalUSD = amount - totalFeeUSD; // User receives amount - fees
            const totalSYP = totalUSD * EXCHANGE_RATE;

            document.getElementById('summarySellAmount').textContent = amount.toFixed(2);
            document.getElementById('summarySellNetwork').textContent = network.toUpperCase().replace('_', ' ');
            document.getElementById('summarySellFee').textContent = totalFeeUSD.toFixed(2);
            document.getElementById('summarySellTotalUSD').textContent = totalUSD.toFixed(2);
            document.getElementById('summarySellTotalSYP').textContent = totalSYP.toFixed(2);
            summaryDiv.style.display = 'block';
        }

        function showSellAddress() {
            const network = document.getElementById('sellNetwork').value;
            const addressDiv = document.getElementById('sellCryptoAddress');
            const addressContent = document.getElementById('sellAddressContent');

            addressDiv.style.display = 'block';
            addressContent.innerHTML = '';

            let address = '';
            switch (network) {
                case 'bep20':
                    address = '0x21802218d8d661d66F2C7959347a6382E1cc614F';
                    break;
                case 'trc20':
                    address = 'TD2LoErPRkVPBxDk72ZErtiyi6agirZQjX';
                    break;
                case 'erc20':
                    address = '0x21802218d8d661d66F2C7959347a6382E1cc614F';
                    break;
                case 'binance_pay':
                    address = '969755964';
                    break;
                default:
                    addressDiv.style.display = 'none';
                    break;
            }
            if (address) {
                addressContent.innerHTML = `<span class="copy-address" data-copy="${address}">${address}</span>`;
            }
            addCopyListeners();
            calculateSellAmount(); // Recalculate fees if network changes
        }

        function addCopyListeners() {
            document.querySelectorAll('.copy-address').forEach(element => {
                element.onclick = function() {
                    const textToCopy = this.getAttribute('data-copy');
                    navigator.clipboard.writeText(textToCopy).then(() => {
                        alert('تم نسخ العنوان: ' + textToCopy);
                    }).catch(err => {
                        console.error('فشل النسخ: ', err);
                    });
                };
            });
        }

        function submitUSDTRequest(type) {
            const fullName = document.getElementById('fullName').value;
            const phoneNumber = document.getElementById('phoneNumber').value;
            const city = document.getElementById('city').value;
            const requestStatusDiv = document.getElementById('requestStatus');

            if (!fullName || !phoneNumber || !city) {
                alert('الرجاء تعبئة الاسم الثلاثي ورقم الهاتف والمدينة.');
                return;
            }

            let subject = '';
            let body = `تفاصيل الطلب:\n`;
            body += `الاسم الثلاثي: ${fullName}\n`;
            body += `رقم الهاتف: ${phoneNumber}\n`;
            body += `المدينة: ${city}\n\n`;

            let totalAmountUSD = 0;
            let totalAmountSYP = 0;
            let transactionFeeUSD = 0;
            let networkFeeText = '';

            if (type === 'buy') {
                const amount = parseFloat(document.getElementById('buyAmount').value);
                const network = document.getElementById('buyNetwork').value;
                const address = document.getElementById('buyAddress').value;
                const note = document.getElementById('buyNote').value;
                const paymentMethod = document.getElementById('paymentMethodBuy').value;

                if (isNaN(amount) || amount <= 0 || !network || !address || !paymentMethod) {
                    alert('الرجاء تعبئة جميع حقول الشراء المطلوبة.');
                    return;
                }

                transactionFeeUSD = BASE_FEE_USD + (amount * PERCENTAGE_FEE_RATE);
                if (network === 'trc20') {
                    transactionFeeUSD += TRC20_NETWORK_FEE;
                    networkFeeText = ` (بما في ذلك عمولة شبكة TRC20 بقيمة ${TRC20_NETWORK_FEE}$)`;
                }
                totalAmountUSD = amount + transactionFeeUSD;
                totalAmountSYP = totalAmountUSD * EXCHANGE_RATE;

                subject = `طلب شراء USDT - ${fullName}`;
                body += `نوع العملية: شراء USDT\n`;
                body += `الكمية المطلوبة: ${amount.toFixed(2)} USDT\n`;
                body += `الشبكة: ${network.toUpperCase().replace('_', ' ')}\n`;
                body += `عنوان المحفظة: ${address}\n`;
                body += `طريقة الدفع: ${paymentMethod}\n`;
                body += `ملاحظة: ${note || 'لا توجد'}\n\n`;
                body += `عمولة التحويل: ${transactionFeeUSD.toFixed(2)}$ ${networkFeeText}\n`;
                body += `المبلغ الإجمالي المستحق بالدولار: ${totalAmountUSD.toFixed(2)}$\n`;
                body += `المبلغ الإجمالي المستحق بالليرة السورية: ${totalAmountSYP.toFixed(2)} ل.س\n`;

            } else if (type === 'sell') {
                const amount = parseFloat(document.getElementById('sellAmount').value);
                const network = document.getElementById('sellNetwork').value;
                const note = document.getElementById('sellNote').value;
                const paymentMethod = document.getElementById('paymentMethodSell').value;
                const bankAccountNum = document.getElementById('bankAccountNum').value;

                if (isNaN(amount) || amount <= 0 || !network || !paymentMethod) {
                    alert('الرجاء تعبئة جميع حقول البيع المطلوبة.');
                    return;
                }
                if ((paymentMethod === 'bemo_bank' || paymentMethod === 'sham_cash') && !bankAccountNum) {
                    alert('الرجاء إدخال رقم الحساب البنكي أو عنوان الحساب لطريقة الدفع المختارة.');
                    return;
                }

                transactionFeeUSD = BASE_FEE_USD + (amount * PERCENTAGE_FEE_RATE);
                if (network === 'trc20') {
                    transactionFeeUSD += TRC20_NETWORK_FEE;
                    networkFeeText = ` (بما في ذلك عمولة شبكة TRC20 بقيمة ${TRC20_NETWORK_FEE}$)`;
                }
                totalAmountUSD = amount - transactionFeeUSD; // User receives amount - fees
                totalAmountSYP = totalAmountUSD * EXCHANGE_RATE;

                subject = `طلب بيع USDT - ${fullName}`;
                body += `نوع العملية: بيع USDT\n`;
                body += `الكمية المراد بيعها: ${amount.toFixed(2)} USDT\n`;
                body += `الشبكة: ${network.toUpperCase().replace('_', ' ')}\n`;
                body += `طريقة الاستلام: ${paymentMethod}\n`;
                if (bankAccountNum) {
                    body += `تفاصيل الاستلام (رقم/عنوان الحساب): ${bankAccountNum}\n`;
                }
                body += `ملاحظة: ${note || 'لا توجد'}\n\n`;
                body += `عمولة التحويل: ${transactionFeeUSD.toFixed(2)}$ ${networkFeeText}\n`;
                body += `المبلغ الإجمالي المستحق بالدولار: ${totalAmountUSD.toFixed(2)}$\n`;
                body += `المبلغ الإجمالي المستحق بالليرة السورية: ${totalAmountSYP.toFixed(2)} ل.س\n`;
            }

            const mailtoLink = `mailto:alimahmoud001a@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;

            requestStatusDiv.style.display = 'block';
            requestStatusDiv.innerHTML = `
                <h3>تم إرسال الطلب بنجاح!</h3>
                <p><strong>تفاصيل العمولة:</strong></p>
                <ul>
                    <li>عمولة ثابتة: ${BASE_FEE_USD}$</li>
                    <li>عمولة نسبة مئوية: ${PERCENTAGE_FEE_RATE * 100}% من المبلغ الإجمالي</li>
                    ${networkFeeText ? `<li>${networkFeeText.replace(' (بما في ذلك ', '').replace(')', '')}</li>` : ''}
                </ul>
                <p><strong>المبلغ الإجمالي المستحق ${type === 'buy' ? 'للدفع' : 'للاستلام'} بالدولار:</strong> ${totalAmountUSD.toFixed(2)}$</p>
                <p><strong>المبلغ الإجمالي المستحق ${type === 'buy' ? 'للدفع' : 'للاستلام'} بالليرة السورية:</strong> ${totalAmountSYP.toFixed(2)} ل.س</p>
                <p class="note">عمولة التسديد على طرق التحويل المختلفة بالليرة السورية تقع على المستخدم كما تحددها هذه الجهات.</p>
                <p><strong>تم تجهيز بريد إلكتروني بتفاصيل طلبك. يرجى إرساله لإتمام العملية.</strong></p>
                <a href="${mailtoLink}" class="button">إرسال البريد الإلكتروني الآن</a>
            `;

            // Open the mail client
            window.location.href = mailtoLink;
        }

        // Event listener for additional sell details (bank account/address)
        document.getElementById('paymentMethodSell').addEventListener('change', function() {
            const method = this.value;
            const additionalDetailsDiv = document.getElementById('additionalSellDetails');
            if (method === 'bemo_bank' || method === 'sham_cash') {
                additionalDetailsDiv.style.display = 'block';
            } else {
                additionalDetailsDiv.style.display = 'none';
            }
        });

        // Initial setup for sidebar on load if screen is large enough
        window.onload = function() {
            if (window.innerWidth > 768) {
                document.getElementById("mySidebar").style.width = "300px";
                document.getElementById("main").classList.add('shifted');
            }
            addCopyListeners(); // Add listeners on load for any static copy elements
        };

        window.onresize = function() {
            const sidebar = document.getElementById("mySidebar");
            const mainContent = document.getElementById("main");
            if (window.innerWidth > 768) {
                sidebar.style.width = "300px";
                mainContent.classList.add('shifted');
            } else {
                if (sidebar.style.width === "300px") { // If sidebar was open due to large screen
                    sidebar.style.width = "0"; // Close it for mobile view
                }
                mainContent.classList.remove('shifted');
            }
        };
    </script>
</body>
</html>
