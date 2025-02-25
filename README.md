HI MUSIC EVENT MANAGEMENT
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حاسبة تأخير الصوت</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 20px; }
        input, button { margin: 10px; padding: 10px; font-size: 16px; }
    </style>
</head>
<body>
    <h2>حاسبة تأخير الصوت</h2>
    <p>أدخل المسافة بين السماعات بالمتر:</p>
    <input type="number" id="distance" placeholder="المسافة بالمتر">
    <button onclick="calculateDelay()">حساب التأخير</button>
    <p id="result"></p>

    <script>
        function calculateDelay() {
            let distance = document.getElementById("distance").value;
            let speedOfSound = 343; // سرعة الصوت في الهواء بالمتر/ثانية
            let delay = (distance / speedOfSound) * 1000; // تحويل للمللي ثانية
            document.getElementById("result").innerText = "التأخير الزمني: " + delay.toFixed(2) + " مللي ثانية";
        }
    </script>
</body>
</html>
