<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>استمارة تقديم وظيفة</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            direction: rtl;
            padding: 20px;
        }
        .container {
            max-width: 500px;
            margin: 0 auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h2 {
            text-align: center;
            color: #007bff;
        }
        label {
            font-weight: bold;
            margin-bottom: 5px;
            display: block;
        }
        input[type="text"],
        input[type="tel"],
        input[type="email"],
        select {
            width: 100%;
            padding: 10px;
            margin: 5px 0 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        input[type="submit"] {
            background-color: #007bff;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
        .success-message, .search-message {
            display: none;
            margin-top: 20px;
            padding: 10px;
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
            border-radius: 4px;
            text-align: center;
        }
        .search-container {
            margin-top: 30px;
            text-align: center;
        }
        .search-container input[type="text"] {
            width: 70%;
            display: inline-block;
        }
        .search-container input[type="button"] {
            width: 25%;
            display: inline-block;
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 4px;
            cursor: pointer;
        }
        .search-container input[type="button"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>استمارة تقديم وظيفة</h2>
        <form id="jobForm">
            <label for="name">الاسم:</label>
            <input type="text" id="name" name="name" required>

            <label for="phone">رقم الجوال:</label>
            <input type="tel" id="phone" name="phone" pattern="^05\d{8}$" required placeholder="05XXXXXXXX">
            <small>يرجى إدخال رقم جوال سعودي يبدأ بـ 05 ويتكون من 10 أرقام.</small><br><br>

            <label for="email">البريد الإلكتروني:</label>
            <input type="email" id="email" name="email" required>

            <label for="region">المنطقة:</label>
            <select id="region" name="region" required>
                <option value="">اختر المنطقة</option>
                <option value="الرياض">الرياض</option>
                <option value="مكة المكرمة">مكة المكرمة</option>
                <option value="المدينة المنورة">المدينة المنورة</option>
                <option value="القصيم">القصيم</option>
                <option value="الشرقية">الشرقية</option>
                <option value="عسير">عسير</option>
                <option value="تبوك">تبوك</option>
                <option value="حائل">حائل</option>
                <option value="الباحة">الباحة</option>
                <option value="الجوف">الجوف</option>
                <option value="جازان">جازان</option>
                <option value="نجران">نجران</option>
            </select>

            <label for="profession">المهنة:</label>
            <select id="profession" name="profession" required>
                <option value="">اختر المهنة</option>
                <option value="مهندس مدني">مهندس مدني</option>
                <option value="مهندس كهربائي">مهندس كهربائي</option>
                <option value="طبيب">طبيب</option>
                <option value="محاسب">محاسب</option>
                <option value="مدرس">مدرس</option>
                <option value="مبرمج">مبرمج</option>
                <option value="محامي">محامي</option>
                <option value="ميكانيكي">ميكانيكي</option>
                <option value="سائق">سائق</option>
                <option value="بائع">بائع</option>
                <option value="مدير">مدير</option>
                <option value="ممرض">ممرض</option>
                <option value="عامل">عامل</option>
                <option value="موظف إداري">موظف إداري</option>
                <option value="فني كهرباء">فني كهرباء</option>
                <option value="نجار">نجار</option>
                <option value="سباك">سباك</option>
                <option value="طاهٍ">طاهٍ</option>
                <option value="حداد">حداد</option>
                <option value="مزارع">مزارع</option>
                <option value="حلاق">حلاق</option>
                <option value="فني تبريد وتكييف">فني تبريد وتكييف</option>
            </select>

            <input type="submit" value="إرسال">
        </form>
        <div class="success-message" id="successMessage">
            تم تقديم الطلب بنجاح. سيتم التواصل معك في حال قبول طلبك. رقم طلبك هو <span id="requestNumber"></span>.
        </div>

        <div class="search-container">
            <h3>البحث برقم الطلب</h3>
            <input type="text" id="searchRequestNumber" placeholder="أدخل رقم الطلب">
            <input type="button" value="بحث" onclick="searchRequest()">
        </div>
        <div class="search-message" id="searchMessage">
            ما زال طلبك قيد المراجعة.
        </div>
    </div>

    <script>
        function generateRequestNumber() {
            return Math.floor(Math.random() * 900000) + 100000;
        }

        document.getElementById("jobForm").addEventListener("submit", function(event) {
            event.preventDefault(); // لمنع الإرسال الفعلي للنموذج

            const requestNumber = generateRequestNumber();
            document.getElementById("requestNumber").textContent = requestNumber;
            document.getElementById("successMessage").style.display = "block";

            // إخفاء النموذج
            document.getElementById("jobForm").style.display = "none";
        });

        function searchRequest() {
            const searchMessage = document.getElementById("searchMessage");
            searchMessage.style.display = "block";
        }
    </script>
</body>
</html>
