# Kashig
Nothin
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instant Number Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
            background-color: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            margin: auto;
        }
        h1 {
            font-size: 24px;
            margin-bottom: 10px;
        }
        .number-box {
            font-size: 30px;
            font-weight: bold;
            margin: 15px 0;
            padding: 10px;
            border: 2px solid #333;
            display: inline-block;
            background: #fff;
            border-radius: 5px;
            min-width: 100px;
        }
        .btn {
            background: #28a745;
            color: white;
            padding: 10px 15px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            margin: 10px;
            border-radius: 5px;
        }
        .btn:hover {
            background: #218838;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Instant Number Generator</h1>
        <div class="number-box" id="randomNumber">000000</div>
        <br>
        <button class="btn" onclick="generateNumber()">Generate Number</button>
        <button class="btn" onclick="copyNumber()">Copy to Clipboard</button>
    </div>

    <script>
        function generateNumber() {
            let number = Math.floor(100000 + Math.random() * 900000); // 6-digit number
            document.getElementById("randomNumber").innerText = number;
        }

        function copyNumber() {
            let numberText = document.getElementById("randomNumber").innerText;
            navigator.clipboard.writeText(numberText).then(() => {
                alert("Number copied: " + numberText);
            });
        }
    </script>

</body>
</html>
