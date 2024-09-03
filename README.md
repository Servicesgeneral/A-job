<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Job Application Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            padding: 20px;
            direction: rtl;
        }
        .container {
            max-width: 100%;
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
        .form-header {
            text-align: center;
            margin-bottom: 20px;
        }
        .form-header img {
            max-width: 100%;
            height: auto;
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
        .lang-toggle {
            margin-bottom: 20px;
            text-align: center;
        }
        .lang-toggle button {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 4px;
            cursor: pointer;
            margin: 0 5px;
        }
        .lang-toggle button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="lang-toggle">
            <button onclick="toggleLanguage('ar')">العربية</button>
            <button onclick="toggleLanguage('en')">English</button>
        </div>
        <div id="formContent">
            <!-- Arabic content -->
            <div class="arabic">
                <div class="form-header">
                    <img src="https://www8.0zz0.com/2024/08/28/16/775349027.png" alt="Form Header Image">
                    <h2>استمارة تقديم وظيفة</h2>
                </div>
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

            <!-- English content -->
            <div class="english" style="display: none;">
                <div class="form-header">
                    <img src="https://www8.0zz0.com/2024/08/28/16/775349027.png" alt="Form Header Image">
                    <h2>Job Application Form</h2>
                </div>
                <form id="jobForm">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name" required>

                    <label for="phone">Phone Number:</label>
                    <input type="tel" id="phone" name="phone" pattern="^\d{10}$" required placeholder="XXXXXXXXXX">
                    <small>Please enter a 10-digit phone number.</small><br><br>

                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>

                    <label for="region">Region:</label>
                    <select id="region" name="region" required>
                        <option value="">Select Region</option>
                        <option value="Riyadh">Riyadh</option>
                        <option value="Mecca">Mecca</option>
                        <option value="Medina">Medina</option>
                        <option value="Qassim">Qassim</option>
                        <option value="Eastern Province">Eastern Province</option>
                        <option value="Asir">
<option value="Asir">Asir</option>
                        <option value="Tabuk">Tabuk</option>
                        <option value="Hail">Hail</option>
                        <option value="Al-Baha">Al-Baha</option>
                        <option value="Al-Jawf">Al-Jawf</option>
                        <option value="Jazan">Jazan</option>
                        <option value="Najran">Najran</option>
                    </select>

                    <label for="profession">Profession:</label>
                    <select id="profession" name="profession" required>
                        <option value="">Select Profession</option>
                        <option value="Civil Engineer">Civil Engineer</option>
                        <option value="Electrical Engineer">Electrical Engineer</option>
                        <option value="Doctor">Doctor</option>
                        <option value="Accountant">Accountant</option>
                        <option value="Teacher">Teacher</option>
                        <option value="Programmer">Programmer</option>
                        <option value="Lawyer">Lawyer</option>
                        <option value="Mechanic">Mechanic</option>
                        <option value="Driver">Driver</option>
                        <option value="Salesperson">Salesperson</option>
                        <option value="Manager">Manager</option>
                        <option value="Nurse">Nurse</option>
                        <option value="Worker">Worker</option>
                        <option value="Administrative Employee">Administrative Employee</option>
                        <option value="Electrician">Electrician</option>
                        <option value="Carpenter">Carpenter</option>
                        <option value="Plumber">Plumber</option>
                        <option value="Chef">Chef</option>
                        <option value="Blacksmith">Blacksmith</option>
                        <option value="Farmer">Farmer</option>
                        <option value="Barber">Barber</option>
                        <option value="AC Technician">AC Technician</option>
                    </select>

                    <input type="submit" value="Submit">
                </form>
                <div class="success-message" id="successMessage">
                    Your application has been submitted successfully. We will contact you if your application is accepted. Your request number is <span id="requestNumber"></span>.
                </div>

                <div class="search-container">
                    <h3>Search by Request Number</h3>
                    <input type="text" id="searchRequestNumber" placeholder="Enter Request Number">
                    <input type="button" value="Search" onclick="searchRequest()">
                </div>
                <div class="search-message" id="searchMessage">
                    Your request is still under review.
                </div>
            </div>
        </div>
    </div>

    <script>
        function generateRequestNumber() {
            return Math.floor(Math.random() * 900000) + 100000;
        }

        document.getElementById("jobForm").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevent the default form submission

            const requestNumber = generateRequestNumber();
            document.getElementById("requestNumber").textContent = requestNumber;
            document.querySelector(".success-message").style.display = "block";

            // Hide the form
            document.getElementById("jobForm").style.display = "none";
        });

        function searchRequest() {
            const searchMessage = document.getElementById("searchMessage");
            searchMessage.style.display = "block";
        }

        function toggleLanguage(lang) {
            if (lang === 'ar') {
                document.querySelector(".arabic").style.display = "block";
                document.querySelector(".english").style.display = "none";
                document.body.style.direction = "rtl";
            } else if (lang === 'en') {
                document.querySelector(".arabic").style.display = "none";
                document.querySelector(".english").style.display = "block";
                document.body.style.direction = "ltr";
            }
        }
    </script>
</body>
</html
