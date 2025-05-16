<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>چک‌لیست تحلیل بازار</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            background-color: #f4f4f4;
            text-align: right;
        }
        h1 {
            color: #333;
            text-align: center;
        }
        .checklist {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .checklist label {
            display: block;
            margin: 10px 0;
            font-size: 16px;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 20px;
        }
        button:hover {
            background-color: #218838;
        }
        #result {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            text-align: center;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>چک‌لیست تحلیل بازار</h1>
    <div class="checklist">
        <label><input type="checkbox" name="checklist" value="competitors"> تحلیل رقبا و شناسایی نقاط قوت و ضعف آن‌ها</label>
        <label><input type="checkbox" name="checklist" value="demand"> بررسی تقاضای بازار و نیازهای مشتریان</label>
        <label><input type="checkbox" name="checklist" value="trends"> شناسایی روندهای اقتصادی و فناوری</label>
        <label><input type="checkbox" name="checklist" value="regulations"> بررسی قوانین و مقررات مرتبط</label>
        <label><input type="checkbox" name="checklist" value="swot"> انجام تحلیل SWOT (نقاط قوت، ضعف، فرصت‌ها، تهدیدها)</label>
        <label><input type="checkbox" name="checklist" value="target"> تعریف دقیق بازار هدف و مشتریان</label>
        <label><input type="checkbox" name="checklist" value="pricing"> تحلیل استراتژی‌های قیمت‌گذاری</label>
        <label><input type="checkbox" name="checklist" value="supply"> بررسی زنجیره تأمین و منابع</label>
        <button onclick="calculateRisk()">محاسبه ریسک</button>
    </div>
    <div id="result"></div>

    <script>
        function calculateRisk() {
            const checkboxes = document.querySelectorAll('input[name="checklist"]:checked');
            const count = checkboxes.length;
            const total = document.querySelectorAll('input[name="checklist"]').length;
            const riskLevel = count >= 6 ? "پایین" : count >= 3 ? "متوسط" : "بالا";
            document.getElementById("result").innerHTML = 
                `تعداد تاییدیه‌ها: ${count} از ${total}<br>` +
                `سطح ریسک: ${riskLevel}`;
        }
    </script>
</body>
</html>
