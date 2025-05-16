# Planer
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
