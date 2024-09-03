<script type='text/javascript' src='//embitterlorrycar.com/07/d5/ac/07d5acabcbfb0e843f499e904565f063.js'></script>
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
            font-family: 'Amiri', serif;
            font-size: 24px;
        }
        .form-header {
            text-align: center;
            margin-bottom: 20px;
        }
        .form-header h2 {
            font-family: 'Amiri', serif;
            font-size: 36px;
            margin: 0;
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
        .success-message,
        .loading-popup {
            display: none;
            position: fixed;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            z-index: 1000;
        }
        .success-message {
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }
        .loading-popup {
            background-color: #fff3cd;
            color: #856404;
            border: 1px solid #ffeeba;
        }
        .loading-popup::before {
            content: '';
            display: inline-block;
            width: 24px;
            height: 24px;
            border: 3px solid #007bff;
            border-radius: 50%;
            border-top: 3px solid transparent;
            animation: spin 1s linear infinite;
            vertical-align: middle;
            margin-right: 10px;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
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
                    <h2>المتحدة للمقاولات</h2>
                </div>
                <form id="jobForm">
                    <label for="name">الاسم:</label>
                    <input type="text" id="name" name="name" required>

                    <label for="phone">رقم الجوال:</label>
                    <input type="tel" id="phone" name="phone" required placeholder="أدخل رقم الجوال">

                    <label for="email">البريد الإلكتروني:</label>
                    <input type="email" id="email" name="email" required>

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
                <div class="loading-popup" id="loadingPopup">
                    <div>يرجى الانتظار...</div>
                </div>
                <div class="success-message" id="successMessage">
                    تم تقديم الطلب بنجاح. سيتم التواصل معك في حال قبول طلبك. رقم طلبك هو <span id="requestNumber"></span>.
                </div>
            </div>

            <!-- English content -->
            <div class="english" style="display: none;">
                <div class="form-header">
                    <h2>Al-Mutahida for Contracting</h2>
                </div>
                <form id="jobFormEn">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name" required>

                    <label for="phone">Phone Number:</label>
                    <input type="tel" id="phone" name="phone" required placeholder="Enter phone number">

                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>

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
                <div class="loading-popup" id="loadingPopupEn">
                    <div>Please wait...</div>
                </div>
                <div class="success-message" id="<div class="success-message" id="successMessageEn">
                    Your application has been submitted successfully. We will contact you if your application is accepted. Your request number is <span id="requestNumberEn"></span>.
                </div>
            </div>
        </div>
    </div>

    <script>
        function generateRequestNumber() {
            return Math.floor(Math.random() * 900000) + 100000;
        }

        function showLoadingPopup() {
            const lang = document.body.getAttribute('data-lang');
            if (lang === 'ar') {
                document.getElementById("loadingPopup").style.display = "block";
            } else if (lang === 'en') {
                document.getElementById("loadingPopupEn").style.display = "block";
            }
        }

        function hideLoadingPopup() {
            const lang = document.body.getAttribute('data-lang');
            if (lang === 'ar') {
                document.getElementById("loadingPopup").style.display = "none";
            } else if (lang === 'en') {
                document.getElementById("loadingPopupEn").style.display = "none";
            }
        }

        function showSuccessMessage() {
            const lang = document.body.getAttribute('data-lang');
            if (lang === 'ar') {
                document.getElementById("successMessage").style.display = "block";
            } else if (lang === 'en') {
                document.getElementById("successMessageEn").style.display = "block";
            }
        }

        document.getElementById("jobForm").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevent the default form submission

            showLoadingPopup();

            // Simulate a delay (e.g., an AJAX request)
            setTimeout(function() {
                const requestNumber = generateRequestNumber();
                document.getElementById("requestNumber").textContent = requestNumber;
                
                hideLoadingPopup();
                showSuccessMessage();
                
                // Hide the form
                document.getElementById("jobForm").style.display = "none";
            }, 2000); // Adjust the delay as needed
        });

        document.getElementById("jobFormEn").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevent the default form submission

            showLoadingPopup();

            // Simulate a delay (e.g., an AJAX request)
            setTimeout(function() {
                const requestNumber = generateRequestNumber();
                document.getElementById("requestNumberEn").textContent = requestNumber;
                
                hideLoadingPopup();
                showSuccessMessage();
                
                // Hide the form
                document.getElementById("jobFormEn").style.display = "none";
            }, 2000); // Adjust the delay as needed
        });

        function toggleLanguage(lang) {
            if (lang === 'ar') {
                document.querySelector(".arabic").style.display = "block";
                document.querySelector(".english").style.display = "none";
                document.body.style.direction = "rtl";
                document.body.setAttribute('data-lang', 'ar');
            } else if (lang === 'en') {
                document.querySelector(".arabic").style.display = "none";
                document.querySelector(".english").style.display = "block";
                document.body.style.direction = "ltr";
                document.body.setAttribute('data-lang', 'en');
            }
        }

        // Initial language setup
        toggleLanguage('ar'); // Default to Arabic
    </script>
</body>
</html>
