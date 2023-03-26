<html>
<head>
    <title>New Puzzle Game</title>
    <style>
        body {
            background-color: #FFC0CB;
        }

        #gameCanvas {
            width: 500px;
            height: 500px;
            border: 1px solid #000000;
            background-color: #FFF;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <h1>New Puzzle Game</h1>
    <div id="gameCanvas"></div>
    <script>
        // Setup the game canvas
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');

        // Set the game size
        const blockSize = 20;
        const widthInBlocks = 25;
        const heightInBlocks = 25;

        // Set the starting position and direction of the snake
        let snakeX = 10;
        let snakeY = 10;
        let direction = "right";

        // Draw the snake on the canvas
        const drawSnake = () => {
            ctx.fillStyle = "#000000";
            ctx.fillRect(snakeX * blockSize, snakeY * blockSize, blockSize, blockSize);
        }

        // Draw the canvas border
        const drawBorder = () => {
            ctx.fillStyle = "#000000";
            ctx.fillRect(0, 0, widthInBlocks * blockSize, heightInBlocks * blockSize);
        }

        // Draw the game on the canvas
        const draw = () => {
            drawBorder();
            drawSnake();
        };

        // Update the game state
        const update = () => {
            snakeX += 1;
        };

        // Main game loop
        const loop = () => {
            update();
            draw();
            setTimeout(loop, 1000 / 15);
        };

        // Start the game....
        loop();
        // Update the game state
        const update = () => {
            // Move the snake
            if (direction === "right") {
                snakeX += 1;
            } else if (direction === "left") {
                snakeX -= 1;
            } else if (direction === "up") {
                snakeY -= 1;
            } else if (
    </script>
</body>
</html>
