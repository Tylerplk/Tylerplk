<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>เกมเศรษฐีจีน</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>เกมเศรษฐีจีน</h1>
    </header>
    <main>
        <div class="game-board">
            <div class="player-info">
                <p>ผู้เล่น: <span id="player-name">ผู้เล่น 1</span></p>
                <p>เงินในบัญชี: <span id="player-money">1000</span> บาท</p>
            </div>
            <button id="roll-dice">ทอยลูกเต๋า</button>
            <div id="dice-result"></div>
        </div>
    </main>
    <footer>
        <p>© 2024 เกมเศรษฐีจีน</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: 'Arial', sans-serif;
    background-color: #b22222; /* สีแดงเข้ม */
    color: #ffd700; /* สีทอง */
    text-align: center;
}

header {
    background-color: #8b0000; /* สีแดงเข้ม */
    padding: 20px;
}

h1 {
    margin: 0;
}

.main {
    margin: 20px;
}

.game-board {
    border: 2px solid #ffd700; /* ขอบทอง */
    padding: 20px;
    background-color: #fff8dc; /* สีครีม */
}

button {
    background-color: #ffd700; /* สีทอง */
    color: #000; /* สีดำ */
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background-color: #ffcc00; /* สีทองเข้มเมื่อhover */
}

footer {
    margin-top: 20px;
}
document.getElementById('roll-dice').addEventListener('click', function() {
    const diceValue = Math.floor(Math.random() * 6) + 1; // สุ่มเลข 1-6
    document.getElementById('dice-result').innerText = `คุณทอยได้: ${diceValue}`;
    
    // อัพเดตเงินของผู้เล่น (สมมุติว่าเพิ่ม 100 บาทต่อการทอย)
    let playerMoney = parseInt(document.getElementById('player-money').innerText);
    playerMoney += 100; // เพิ่มเงิน
    document.getElementById('player-money').innerText = playerMoney;
});
