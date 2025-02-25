function calculateDelay() {
    let distance = document.getElementById("distance").value;
    if (distance && distance > 0) {
        let speedOfSound = 343; // سرعة الصوت بالأمتار في الثانية
        let delay = (distance / speedOfSound) * 1000; // التحويل إلى ميلي ثانية
        document.getElementById("result").innerText = "التأخير: " + delay.toFixed(2) + " ميلي ثانية";
    } else {
        document.getElementById("result").innerText = "الرجاء إدخال مسافة صحيحة";
    }
}
