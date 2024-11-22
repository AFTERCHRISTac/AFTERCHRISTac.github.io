<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2048 Game</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="game-container">
        <h1>2048</h1>
        <div class="grid-container" id="grid-container">
            <!-- Cells will be generated here -->
        </div>
        <div class="score-container">
            <span>Score: <span id="score">0</span></span>
        </div>
        <button id="restart-button">Restart</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
