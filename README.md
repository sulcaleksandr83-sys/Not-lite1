# Not-lite1
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>💰 NotCoin Lite</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>💰 NotCoin Lite</h1>
    <h2 id="tokens">Токены: 0</h2>

    <div class="buttons">
        <button onclick="collect()">🪙 Собрать токен</button>
        <button onclick="upgrade()">⬆️ Улучшить сбор (10 токенов)</button>
    </div>

    <script src="script.js"></script>
</body>
</html>body {
    background-color: #1a1a2e;
    color: #ffffff;
    text-align: center;
    font-family: Arial, sans-serif;
    margin-top: 80px;
}

h1 {
    font-size: 40px;
    color: #ffd700;
    text-shadow: 0 0 10px #ff8c00;
}

h2 {
    font-size: 30px;
    margin-bottom: 30px;
}

.buttons button {
    padding: 15px 25px;
    font-size: 20px;
    margin: 10px;
    border-radius: 10px;
    border: none;
    cursor: pointer;
    background: linear-gradient(90deg, #4caf50, #2e7d32);
    color: white;
    transition: 0.2s;
}

.buttons button:hover {
    transform: scale(1.05);
}let tokens = 0;
let power = 1;

function collect() {
    tokens += power;
    document.getElementById("tokens").innerText = "Токены: " + tokens;
}

function upgrade() {
    if(tokens >= 10) {
        tokens -= 10;
        power += 1;
        document.getElementById("tokens").innerText = "Токены: " + tokens;
        alert("⬆️ Сбор токенов увеличен! Сейчас за клик +" + power);
    } else {
        alert("Недостаточно токенов для улучшения!");
    }
}
