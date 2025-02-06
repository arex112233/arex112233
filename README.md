<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine? 💖</title>
    <style>
        body {
            background-color: #ffccdc;
            text-align: center;
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .card {
            background: white;
            width: 350px;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            position: relative;
        }
        .heart {
            font-size: 50px;
            color: red;
            animation: heartbeat 1s infinite;
        }
        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.3); }
            100% { transform: scale(1); }
        }
        .teddy {
            font-size: 80px;
        }
        .buttons button {
            background: pink;
            border: none;
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 10px;
            margin: 10px;
            transition: 0.3s;
        }
        .buttons button:hover {
            background: red;
            color: white;
        }
        #response {
            font-size: 20px;
            margin-top: 20px;
            font-weight: bold;
        }
        .fullscreen-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 204, 220, 0.95);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }
        .fullscreen-content {
            text-align: center;
        }
        .fullscreen-content img {
            max-width: 90%;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        .fullscreen-content h2 {
            font-size: 32px;
            color: #ff1493;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <!-- Valentine's Question Card -->
    <div class="card" id="valentineQuestion">
        <div class="heart">❤️</div>
        <h1>Will you be my Valentine? 💖</h1>
        <div class="teddy">🐻</div>
        <div class="buttons">
            <button onclick="sayYes()">Yes! 😍</button>
            <button onclick="sayNo()">No 🙈</button>
        </div>
        <div id="response"></div>
    </div>

    <!-- Fullscreen Image Popup -->
    <div class="fullscreen-overlay" id="fullscreenOverlay">
        <div class="fullscreen-content">
            <img src="me.jpg" alt="Valentine's Image">
            <h2>Thank you for choosing me! 💖<br>You made my day!</h2>
        </div>
    </div>

    <script>
        function sayYes() {
            // Show the fullscreen overlay
            document.getElementById("fullscreenOverlay").style.display = "flex";
        }

        function sayNo() {
            // Display a playful message
            document.getElementById("response").innerHTML = "Oh Ana! But you're still amazing! 💖";
        }
    </script>
</body>
</html>
