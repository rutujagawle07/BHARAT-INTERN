<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body {
            background-color: #f0f3f5;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            background-color: #ffffff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        h1 {
            color: #3498db;
        }

        .input-div {
            margin: 20px 0;
        }

        .inp {
            padding: 10px;
            font-size: 18px;
            width: 200px;
            text-align: center;
            border: 1px solid #3498db;
            border-radius: 5px;
            background-color: #ecf0f1;
            color: #3498db;
        }

        .icon {
            font-size: 40px;
            color: #3498db;
        }
    </style>
</head>

<body>
    <div class="container">
        <h1>Temperature Converter <span class="icon">&#8451;</span> <span class="icon">&#8596;</span> <span class="icon">&#8457;</span></h1>
        <div class="input-div">
            <label>Celsius</label><br>
            <input type="number" value="0" id="cel" class="inp">
        </div>
        <div class="input-div">
            <label>Fahrenheit</label><br>
            <input type="number" value="32" id="fah" class="inp">
        </div>
    </div>
    <script>
        var cel = document.getElementById("cel");
        var fah = document.getElementById("fah");
        cel.addEventListener('input', function () {
            let c = this.value;
            let f = (c * 9 / 5) + 32;
            fah.value = f.toFixed(2);
        });
        fah.addEventListener('input', function () {
            let f = this.value;
            let c = (f - 32) * 5 / 9;
            cel.value = c.toFixed(2);
        });
    </script>
</body>

</html>
