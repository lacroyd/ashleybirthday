# ashleybirthday
suprise
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Cake Animation</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f1c40f;
            overflow: hidden;
        }
        #cakeContainer {
            position: relative;
            width: 300px;
            height: 200px;
            perspective: 1000px;
        }
        #cake {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 100%;
            background-color: #bd8554;
            border-radius: 50% 50% 0 0;
            animation: spin 10s infinite linear;
        }
        .candle {
            position: absolute;
            width: 10px;
            height: 30px;
            background-color: #e74c3c;
            top: -30px;
            animation: fall 3s infinite;
        }
        .flame {
            position: absolute;
            width: 6px;
            height: 6px;
            background-color: #f39c12;
            border-radius: 50%;
            animation: flicker 1s infinite;
        }
        @keyframes fall {
            0% { transform: translateY(-100vh); }
            100% { transform: translateY(100vh); }
        }
        @keyframes flicker {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.2); opacity: 0.5; }
            100% { transform: scale(1); opacity: 1; }
        }
        @keyframes spin {
            from { transform: rotateY(0deg); }
            to { transform: rotateY(360deg); }
        }
        .drippingFrosting {
            position: absolute;
            width: 100%;
            height: 10px;
            background-color: #ffffff;
            bottom: 10px;
            animation: drip 4s infinite;
        }
        @keyframes drip {
            0% { transform: translateY(0); }
            50% { transform: translateY(5px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div id="cakeContainer">
        <div id="cake">
            <div class="candle" style="left: 20%; animation-delay: 0s;"><div class="flame" style="top: -6px;"></div></div>
            <div class="candle" style="left: 50%; animation-delay: 1s;"><div class="flame" style="top: -6px;"></div></div>
            <div class="candle" style="left: 80%; animation-delay: 2s;"><div class="flame" style="top: -6px;"></div></div>
            <div class="drippingFrosting"></div>
        </div>
    </div>
    <script>
        // Additional glitter/ribbon effects can be implemented here
        // For simplicity, we focus on cake animation in this demo
    </script>
</body>
</html>
