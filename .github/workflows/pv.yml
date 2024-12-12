<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>理想氣體方程式計算機</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }
        h1 {
            color: #333;
        }
        .input-group {
            margin-bottom: 15px;
        }
        label {
            margin-right: 10px;
        }
        input {
            padding: 5px;
            width: 150px;
        }
        button {
            padding: 10px 15px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <h1>理想氣體方程式計算機</h1>

    <div class="input-group">
        <label for="pressure">氣壓 (atm):</label>
        <input type="number" id="pressure" placeholder="輸入氣壓">
    </div>

    <div class="input-group">
        <label for="volume">體積 (L):</label>
        <input type="number" id="volume" placeholder="輸入體積">
    </div>

    <div class="input-group">
        <label for="moles">莫耳數 (n):</label>
        <input type="number" id="moles" placeholder="輸入莫耳數">
    </div>

    <div class="input-group">
        <label for="temperature">溫度 (K):</label>
        <input type="number" id="temperature" placeholder="輸入溫度">
    </div>

    <button onclick="calculate()">計算</button>

    <h2>結果:</h2>
    <p id="result"></p>

    <script>
        const R = 0.0821; // 理想氣體常數 (L·atm)/(mol·K)

        function calculate() {
            const pressure = parseFloat(document.getElementById('pressure').value);
            const volume = parseFloat(document.getElementById('volume').value);
            const moles = parseFloat(document.getElementById('moles').value);
            const temperature = parseFloat(document.getElementById('temperature').value);

            let result = "";

            if (isNaN(pressure)) {
                if (!isNaN(volume) && !isNaN(moles) && !isNaN(temperature)) {
                    // 計算氣壓
                    result = `氣壓 = ${(moles * R * temperature / volume).toFixed(2)} atm`;
                } else {
                    result = "請輸入足夠的數據來計算氣壓";
                }
            } else if (isNaN(volume)) {
                if (!isNaN(pressure) && !isNaN(moles) && !isNaN(temperature)) {
                    // 計算體積
                    result = `體積 = ${(moles * R * temperature / pressure).toFixed(2)} L`;
                } else {
                    result = "請輸入足夠的數據來計算體積";
                }
            } else if (isNaN(moles)) {
                if (!isNaN(pressure) && !isNaN(volume) && !isNaN(temperature)) {
                    // 計算莫耳數
                    result = `莫耳數 = ${(pressure * volume / (R * temperature)).toFixed(2)} mol`;
                } else {
                    result = "請輸入足夠的數據來計算莫耳數";
                }
            } else if (isNaN(temperature)) {
                if (!isNaN(pressure) && !isNaN(volume) && !isNaN(moles)) {
                    // 計算溫度
                    result = `溫度 = ${(pressure * volume / (moles * R)).toFixed(2)} K`;
                } else {
                    result = "請輸入足夠的數據來計算溫度";
                }
            } else {
                result = "請至少留下一個值未輸入進行計算";
            }

            document.getElementById('result').innerText = result;
        }
    </script>
</body>
</html>
