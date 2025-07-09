<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل المتداول</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
        }

        body {
            background-color: #f4f7fa;
            color: #333;
            line-height: 1.6;
        }

        /* Header */
        header {
            background: linear-gradient(90deg, #1a3c6e, #2a5b9e);
            color: #fff;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            font-size: 2.5rem;
            font-weight: 700;
        }

        /* Sidebar */
        .sidebar {
            position: fixed;
            top: 0;
            right: -250px;
            width: 250px;
            height: 100%;
            background-color: #1a3c6e;
            color: #fff;
            transition: right 0.3s ease;
            z-index: 1000;
            padding: 20px;
        }

        .sidebar.active {
            right: 0;
        }

        .sidebar ul {
            list-style: none;
            margin-top: 20px;
        }

        .sidebar ul li {
            margin: 15px 0;
        }

        .sidebar ul li a {
            color: #fff;
            text-decoration: none;
            font-size: 1.1rem;
            display: block;
            padding: 10px;
            border-radius: 5px;
        }

        .sidebar ul li a:hover {
            background-color: #2a5b9e;
        }

        .menu-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            font-size: 1.5rem;
            background-color: #1a3c6e;
            color: #fff;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            z-index: 1001;
        }

        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 0 20px;
        }

        .section {
            display: none;
            background-color: #fff;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .section.active {
            display: block;
        }

        .section h2 {
            font-size: 1.8rem;
            color: #1a3c6e;
            margin-bottom: 15px;
        }

        .section p, .section ul {
            font-size: 1rem;
            margin-bottom: 10px;
        }

        .section ul li {
            margin-bottom: 10px;
        }

        .section a {
            color: #2a5b9e;
            text-decoration: none;
        }

        .section a:hover {
            text-decoration: underline;
        }

        /* Calculator Section */
        .calculator form {
            display: grid;
            gap: 10px;
            margin-bottom: 20px;
        }

        .calculator input {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 100%;
        }

        .calculator button {
            background-color: #1a3c6e;
            color: #fff;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .calculator button:hover {
            background-color: #2a5b9e;
        }

        #capitalChart {
            width: 100%;
            height: 400px;
        }

        /* USDT Section */
        .usdt-form select, .usdt-form input, .usdt-form textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .usdt-form .copyable {
            cursor: pointer;
            background-color: #f4f7fa;
            padding: 10px;
            border-radius: 5px;
        }

        .usdt-form .copyable:hover {
            background-color: #e0e6ed;
        }

        /* Floating Contact Icons */
        .contact-icons {
            position: fixed;
            bottom: 20px;
            left: 20px;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .contact-icons a {
            display: block;
            width: 50px;
            height: 50px;
            background-color: #1a3c6e;
            color: #fff;
            border-radius: 50%;
            text-align: center;
            line-height: 50px;
            font-size: 1.5rem;
            text-decoration: none;
        }

        .contact-icons a:hover {
            background-color: #2a5b9e;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.8rem;
            }

            .sidebar {
                width: 200px;
            }

            .container {
                padding: 0 10px;
            }

            .section h2 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <h1>دليل المتداول</h1>
    </header>

    <!-- Sidebar Toggle Button -->
    <div class="menu-toggle" onclick="toggleSidebar()">☰</div>

    <!-- Sidebar -->
    <nav class="sidebar" id="sidebar">
        <ul>
            <li><a href="#" onclick="showSection('home')">الصفحة الرئيسية</a></li>
            <li><a href="#" onclick="showSection('apps')">تطبيقات التداول</a></li>
            <li><a href="#" onclick="showSection('telegram')">قنوات التلجرام</a></li>
            <li><a href="#" onclick="showSection('education')">التعليم</a></li>
            <li><a href="#" onclick="showSection('calculator')">حاسبة تطور رأس المال</a></li>
            <li><a href="#" onclick="showSection('usdt')">شراء وبيع USDT</a></li>
        </ul>
    </nav>

    <!-- Main Content -->
    <div class="container">
        <!-- Home Section -->
        <div class="section active" id="home">
            <h2>شركة الوساطة المالية</h2>
            <p><a href="https://my.rannforex.com/en/auth/register/?fprc=cf22v1">رابط التسجيل في شركة RannForex</a></p>
            <h3>ميزات الشركة:</h3>
            <ul>
                <li>أقل إيداع أو سحب: 10$ خلال 30 ثانية</li>
                <li>سبريد: 0.2~1.2، رافعة مالية: 500:1</li>
                <li>تداول آمن على جميع أزواج الفوركس، المعادن، النفط، المؤشرات، والعملات المشفرة</li>
                <li>حسابات إسلامية خالية من العمولة وحسابات احترافية بأسبريد منخفض جدًا</li>
                <li>انزلاق منخفض وتنفيذ فوري للصفقات</li>
                <li>تقييم ممتاز على مواقع Trust Pilot, Myfxbook, WikiFX, Forex Peace Army</li>
                <li>أمان عالي بفضل التوثيق الثنائي (2FA)</li>
                <li>توثيق سريع وسهل</li>
                <li>نموذج A-Book من أفضل مزودي السيولة</li>
            </ul>
            <p><a href="https://rannforex.com/en/trading/quotesonline/">الاطلاع على السبريد المتوسط اليومي</a></p>
        </div>

        <!-- Apps Section -->
        <div class="section" id="apps">
            <h2>تطبيقات يجب تحميلها للبدء بالتداول</h2>
            <ul>
                <li><a href="https://play.google.com/store/apps/details?id=net.metaquotes.metatrader5">منصة ميتا تريدر 5</a> - المنصة الموثوقة الأفضل في مجال التداول</li>
                <li><a href="https://www.binance.com/activity/referral-entry/CPA?ref=CPA_004C6HBMJS">باينانس</a> - المحفظة الإلكترونية</li>
                <li><a href="https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2">Google Authenticator</a> - تطبيق المصادقة الثنائية</li>
                <li><a href="https://play.google.com/store/apps/details?id=com.tradingview.tradingviewapp">TradingView</a> - تطبيق التحليل</li>
            </ul>
        </div>

        <!-- Telegram Section -->
        <div class="section" id="telegram">
            <h2>قنوات التلجرام</h2>
            <p> باشتراك شهري 30 دولار يمكنك الدخول إلى القنوات الخاصة التالية:</p>
            <ul>
                <li><a href="https://t.me/tradewithali002">قناة الإشارات</a></li>
                <li><a href="https://t.me/tradewithali003">قناة الكورس</a></li>
            </ul>
            <p>قناة عامة تقدم إشارات مجانية بدون اشتراك:</p>
            <ul>
                <li><a href="https://t.me/Tradewithali001">قناة الإشارات المجانية</a></li>
            </ul>
            <p>مجتمعنا:</p>
            <ul>
                <li><a href="https://t.me/SyriaTradingFXg">مجتمع SyriaTradingFX</a></li>
            </ul>
        </div>

        <!-- Education Section -->
        <div class="section" id="education">
            <h2>التعليم</h2>
            <ul>
                <li><a href="https://youtube.com/@tradewithpatarabic?si=4egOIQw15KHmRJGy">كورس كامل لتعلم التداول مع باتك</a></li>
                <li><a href="https://youtube.com/@smart_risk?si=s0leP3OYv9GuCp3r">قناة Smart Risk على يوتيوب</a></li>
                <li><a href="https://www.instagram.com/kameel_m5?igsh=YzljYTk1ODg3Zg==">كورس على إنستغرام</a></li>
                <li><a href="https://youtube.com/@smart_risk?si=8VLFIUyBN-9rm7L6">كورس Smart Risk على يوتيوب</a></li>
            </ul>
        </div>

        <!-- Calculator Section -->
        <div class="section" id="calculator">
            <h2>حاسبة تطور رأس المال</h2>
            <form id="capitalForm">
                <label>رأس المال الأولي:</label>
                <input type="number" id="initialCapital" required>
                <label>نسبة الصفقات الرابحة (%):</label>
                <input type="number" id="winRate" required>
                <label>معدل الربح لكل صفقة (%):</label>
                <input type="number" id="profitPerTrade" required>
                <label>معدل الخسارة لكل صفقة (%):</label>
                <input type="number" id="lossPerTrade" required>
                <label>عدد الصفقات في كل تحديث:</label>
                <input type="number" id="tradesPerUpdate" required>
                <label>الهدف النهائي:</label>
                <input type="number" id="targetCapital" required>
                <button type="submit">احسب</button>
            </form>
            <h3>النتائج:</h3>
            <p id="avgReturn">متوسط العائد لكل صفقة: </p>
            <p id="tradesRequired">عدد الصفقات المطلوبة: </p>
            <p id="growthRate">معدل النمو الإجمالي: </p>
            <h3>جدول تطور رأس المال:</h3>
            <table id="capitalTable" border="1">
                <thead>
                    <tr>
                        <th>عدد الصفقات</th>
                        <th>رأس المال</th>
                    </tr>
                </thead>
                <tbody></tbody>
            </table>
            <h3>مخطط تطور رأس المال:</h3>
            <canvas id="capitalChart"></canvas>
        </div>

        <!-- USDT Buy/Sell Section -->
        <div class="section" id="usdt">
            <h2>شراء وبيع USDT</h2>
            <form id="usdtForm">
                <label>الاسم الثلاثي:</label>
                <input type="text" id="fullName" required>
                <label>رقم الهاتف:</label>
                <input type="text" id="phone" required>
                <label>المدينة:</label>
                <input type="text" id="city" required>
                <label>الإجراء:</label>
                <select id="action" onchange="toggleActionFields()">
                    <option value="buy">شراء USDT</option>
                    <option value="sell">بيع USDT</option>
                </select>

                <!-- Buy Fields -->
                <div id="buyFields">
                    <label>الكمية المطلوبة (USDT):</label>
                    <input type="number" id="buyAmount" required>
                    <label>الشبكة:</label>
                    <select id="buyNetwork">
                        <option value="bep20">BEP20</option>
                        <option value="trc20">TRC20</option>
                        <option value="erc20">ERC20</option>
                        <option value="binance_pay">Binance Pay</option>
                    </select>
                    <label>عنوان المحفظة:</label>
                    <input type="text" id="buyAddress" required>
                    <label>طريقة الدفع:</label>
                    <select id="paymentMethod" onchange="showPaymentDetails()">
                        <option value="sham_cash">شام كاش</option>
                        <option value="syriatel_cash">سيريتل كاش</option>
                        <option value="haram_transfer">حوالة الهرم</option>
                        <option value="bemo_bank">بنك بيمو</option>
                    </select>
                    <div id="paymentDetails"></div>
                    <label>ملاحظة (اختياري):</label>
                    <textarea id="buyNote"></textarea>
                </div>

                <!-- Sell Fields -->
                <div id="sellFields" style="display: none;">
                    <label>الكمية المراد بيعها (USDT):</label>
                    <input type="number" id="sellAmount" required>
                    <label>طريقة الاستلام:</label>
                    <select id="receiveMethod" onchange="showReceiveDetails()">
                        <option value="syriatel_cash">سيريتل كاش</option>
                        <option value="haram_transfer">حوالة الهرم</option>
                        <option value="bemo_bank">بنك بيمو</option>
                        <option value="sham_cash">شام كاش</option>
                    </select>
                    <div id="receiveDetails"></div>
                    <label>الشبكة:</label>
                    <select id="sellNetwork" onchange="showCryptoDetails()">
                        <option value="bep20">BEP20</option>
                        <option value="trc20">TRC20</option>
                        <option value="erc20">ERC20</option>
                        <option value="binance_pay">Binance Pay</option>
                    </select>
                    <div id="cryptoDetails"></div>
                    <label>ملاحظة (اختياري):</label>
                    <textarea id="sellNote"></textarea>
                </div>

                <button type="submit">إرسال الطلب</button>
            </form>
            <div id="orderSummary"></div>
        </div>
    </div>

    <!-- Floating Contact Icons -->
    <div class="contact-icons">
        <a href="https://t.me/ali0619000" target="_blank"><i>📱</i></a>
        <a href="mailto:alimahmoud001a@gmail.com"><i>✉️</i></a>
    </div>

    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script>
        // Sidebar Toggle
        function toggleSidebar() {
            document.getElementById('sidebar').classList.toggle('active');
        }

        // Show Section
        function showSection(sectionId) {
            document.querySelectorAll('.section').forEach(section => {
                section.classList.remove('active');
            });
            document.getElementById(sectionId).classList.add('active');
            toggleSidebar();
        }

        // Capital Calculator
        document.getElementById('capitalForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const initialCapital = parseFloat(document.getElementById('initialCapital').value);
            const winRate = parseFloat(document.getElementById('winRate').value) / 100;
            const profitPerTrade = parseFloat(document.getElementById('profitPerTrade').value) / 100;
            const lossPerTrade = parseFloat(document.getElementById('lossPerTrade').value) / 100;
            const tradesPerUpdate = parseInt(document.getElementById('tradesPerUpdate').value);
            const targetCapital = parseFloat(document.getElementById('targetCapital').value);

            const avgReturn = (winRate * profitPerTrade) - ((1 - winRate) * lossPerTrade);
            let currentCapital = initialCapital;
            let trades = 0;
            const tableData = [];
            const chartData = { labels: [], data: [] };

            while (currentCapital < targetCapital && trades < 10000) {
                currentCapital *= (1 + avgReturn);
                trades++;
                if (trades % tradesPerUpdate === 0) {
                    tableData.push({ trades, capital: currentCapital.toFixed(2) });
                    chartData.labels.push(trades);
                    chartData.data.push(currentCapital);
                }
            }

            const growthRate = ((currentCapital - initialCapital) / initialCapital * 100).toFixed(2);
            document.getElementById('avgReturn').textContent = `متوسط العائد لكل صفقة: ${(avgReturn * 100).toFixed(2)}%`;
            document.getElementById('tradesRequired').textContent = `عدد الصفقات المطلوبة: ${trades}`;
            document.getElementById('growthRate').textContent = `معدل النمو الإجمالي: ${growthRate}%`;

            // Update Table
            const tbody = document.querySelector('#capitalTable tbody');
            tbody.innerHTML = '';
            tableData.forEach(row => {
                tbody.innerHTML += `<tr><td>${row.trades}</td><td>${row.capital}</td></tr>`;
            });

            // Update Chart
            const ctx = document.getElementById('capitalChart').getContext('2d');
            new Chart(ctx, {
                type: 'line',
                data: {
                    labels: chartData.labels,
                    datasets: [{
                        label: 'تطور رأس المال',
                        data: chartData.data,
                        borderColor: '#1a3c6e',
                        fill: false
                    }]
                },
                options: { responsive: true }
            });
        });

        // USDT Form Logic
        const exchangeRate = 10000; // SYP per USD
        document.getElementById('usdtForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const fullName = document.getElementById('fullName').value;
            const phone = document.getElementById('phone').value;
            const city = document.getElementById('city').value;
            const action = document.getElementById('action').value;

            let summary = `الاسم: ${fullName}<br>رقم الهاتف: ${phone}<br>المدينة: ${city}<br>الإجراء: ${action === 'buy' ? 'شراء' : 'بيع'}<br>`;

            if (action === 'buy') {
                const amount = parseFloat(document.getElementById('buyAmount').value);
                const network = document.getElementById('buyNetwork').value;
                const address = document.getElementById('buyAddress').value;
                const paymentMethod = document.getElementById('paymentMethod').value;
                const note = document.getElementById('buyNote').value;

                let commission = 1 + (amount * 0.005);
                if (network === 'trc20') commission += 2;
                const totalSYP = (amount + commission) * exchangeRate;

                summary += `الكمية: ${amount} USDT<br>الشبكة: ${network}<br>عنوان المحفظة: ${address}<br>طريقة الدفع: ${paymentMethod}<br>العمولة: ${commission.toFixed(2)} USDT<br>المبلغ المستحق: ${totalSYP.toFixed(2)} ل.س<br>`;
                if (note) summary += `ملاحظة: ${note}<br>`;
                summary += `ملاحظة: عمولة التسديد على طرق التحويل المختلفة بالليرة السورية تقع على المستخدم كما تحددها هذه الجهات.`;
            } else {
                const amount = parseFloat(document.getElementById('sellAmount').value);
                const network = document.getElementById('sellNetwork').value;
                const receiveMethod = document.getElementById('receiveMethod').value;
                const note = document.getElementById('sellNote').value;

                let commission = 1 + (amount * 0.005);
                if (network === 'trc20') commission += 2;
                const totalSYP = (amount - commission) * exchangeRate;

                summary += `الكمية: ${amount} USDT<br>الشبكة: ${network}<br>طريقة الاستلام: ${receiveMethod}<br>العمولة: ${commission.toFixed(2)} USDT<br>المبلغ المستحق: ${totalSYP.toFixed(2)} ل.س<br>`;
                if (note) summary += `ملاحظة: ${note}<br>`;
                summary += `ملاحظة: عمولة التسديد على طرق التحويل المختلفة بالليرة السورية تقع على المستخدم كما تحددها هذه الجهات.`;
            }

            document.getElementById('orderSummary').innerHTML = `<h3>تم إرسال الطلب بنجاح</h3><p>${summary}</p>`;
            const mailtoLink = `mailto:alimahmoud001a@gmail.com?subject=طلب ${action === 'buy' ? 'شراء' : 'بيع'} USDT&body=${encodeURIComponent(summary.replace(/<br>/g, '\n'))}`;
            window.location.href = mailtoLink;
        });

        function toggleActionFields() {
            const action = document.getElementById('action').value;
            document.getElementById('buyFields').style.display = action === 'buy' ? 'block' : 'none';
            document.getElementById('sellFields').style.display = action === 'sell' ? 'block' : 'none';
        }

        function showPaymentDetails() {
            const method = document.getElementById('paymentMethod').value;
            let details = '';
            if (method === 'sham_cash') {
                details = `<p class="copyable" onclick="copyText(this)">عنوان شام كاش: be456e0ea9392db4d68a7093ee317bc8</p><p class="copyable" onclick="copyText(this)">رقم الحساب: 5991161126028260</p>`;
            } else if (method === 'syriatel_cash') {
                details = `<p class="copyable" onclick="copyText(this)">عنوان سيريتل كاش: 0934598967</p>`;
            } else if (method === 'haram_transfer') {
                details = `<p>تفاصيل حوالة الهرم:<br>الاسم: علي ابراهيم محمود<br>رقم الهاتف: 0934598967<br>المدينة: اللاذقية</p>`;
            } else if (method === 'bemo_bank') {
                details = `<p>تفاصيل بنك بيمو:<br>الاسم: علي ابراهيم محمود<br>رقم الحساب: 060104947910013000000</p>`;
            }
            document.getElementById('paymentDetails').innerHTML = details;
        }

        function showReceiveDetails() {
            const method = document.getElementById('receiveMethod').value;
            let details = '';
            if (method === 'bemo_bank' || method === 'sham_cash') {
                details = `<label>رقم الحساب أو عنوان الحساب:</label><input type="text" id="receiveAccount" required>`;
            }
            document.getElementById('receiveDetails').innerHTML = details;
        }

        function showCryptoDetails() {
            const network = document.getElementById('sellNetwork').value;
            let details = '';
            if (network === 'bep20') {
                details = `<p class="copyable" onclick="copyText(this)">BEP20: 0x21802218d8d661d66F2C7959347a6382E1cc614F</p>`;
            } else if (network === 'trc20') {
                details = `<p class="copyable" onclick="copyText(this)">TRC20: TD2LoErPRkVPBxDk72ZErtiyi6agirZQjX</p>`;
            } else if (network === 'erc20') {
                details = `<p class="copyable" onclick="copyText(this)">ERC20: 0x21802218d8d661d66F2C7959347a6382E1cc614F</p>`;
            } else if (network === 'binance_pay') {
                details = `<p class="copyable" onclick="copyText(this)">Binance Pay: 969755964</p>`;
            }
            document.getElementById('cryptoDetails').innerHTML = details;
        }

        function copyText(element) {
            const text = element.textContent.split(': ')[1];
            navigator.clipboard.writeText(text).then(() => alert('تم نسخ العنوان!'));
        }
    </script>
</body>
</html>
