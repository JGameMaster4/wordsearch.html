<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Word Search Game</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }

        h1 {
            margin-bottom: 20px;
        }

        .word-search-grid {
            display: grid;
            grid-template-columns: repeat(10, 40px);
            grid-gap: 5px;
            justify-content: center;
            margin: 20px 0;
        }

        .cell {
            width: 40px;
            height: 40px;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #e0e0e0;
            cursor: pointer;
            font-size: 18px;
        }

        .cell.selected {
            background-color: #90caf9;
        }

        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #fff;
            padding: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
            text-align: center;
            z-index: 1000;
        }

        .popup button {
            padding: 10px 20px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }

        .popup button:hover {
            background-color: #0056b3;
        }

        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }
    </style>
</head>
<body>

    <h1>Word Search Game</h1>
    <p>Find the words: <strong>Filipino, Teatro, Salamisim</strong></p>
    <div class="word-search-grid" id="wordSearchGrid"></div>

    <div class="overlay" id="overlay"></div>

    <div class="popup" id="popup">
        <h2>Congratulations!</h2>
        <p>Congrats! Here is your hint: makikita moto sa page namin</p>
        <button onclick="closePopup()">SALAMAT!!!</button>
    </div>

    <script>
        const wordsToFind = ["FILIPINO", "TEATRO", "SALAMISIM",];
        const gridSize = 10; // Grid size is 10x10
        const wordSearchGrid = document.getElementById("wordSearchGrid");
        const popup = document.getElementById("popup");
        const overlay = document.getElementById("overlay");

        let selectedCells = [];
        let grid = generateGrid(gridSize, wordsToFind);

        // Render grid
        function renderGrid(grid) {
            wordSearchGrid.innerHTML = ''; // Clear the grid
            grid.forEach((row, rowIndex) => {
                row.forEach((cell, colIndex) => {
                    const div = document.createElement('div');
                    div.classList.add('cell');
                    div.textContent = cell;
                    div.addEventListener('click', () => handleCellClick(rowIndex, colIndex));
                    wordSearchGrid.appendChild(div);
                });
            });
        }

        // Generate the word search grid
        function generateGrid(size, words) {
            let grid = Array.from({ length: size }, () => Array(size).fill(''));
            words.forEach(word => placeWord(grid, word));
            fillEmptySpaces(grid);
            return grid;
        }

        // Place a word randomly in the grid
        function placeWord(grid, word) {
            const directions = [
                [0, 1],  // Horizontal
                [1, 0],  // Vertical
                [1, 1],  // Diagonal down-right
                [-1, 1]  // Diagonal up-right
            ];

            let placed = false;
            while (!placed) {
                const direction = directions[Math.floor(Math.random() * directions.length)];
                const row = Math.floor(Math.random() * grid.length);
                const col = Math.floor(Math.random() * grid[0].length);
                const endRow = row + direction[0] * (word.length - 1);
                const endCol = col + direction[1] * (word.length - 1);

                if (endRow >= 0 && endRow < grid.length && endCol >= 0 && endCol < grid[0].length) {
                    let canPlace = true;
                    for (let i = 0; i < word.length; i++) {
                        const newRow = row + direction[0] * i;
                        const newCol = col + direction[1] * i;
                        if (grid[newRow][newCol] !== '' && grid[newRow][newCol] !== word[i]) {
                            canPlace = false;
                            break;
                        }
                    }

                    if (canPlace) {
                        for (let i = 0; i < word.length; i++) {
                            const newRow = row + direction[0] * i;
                            const newCol = col + direction[1] * i;
                            grid[newRow][newCol] = word[i];
                        }
                        placed = true;
                    }
                }
            }
        }

        // Fill empty spaces with random letters
        function fillEmptySpaces(grid) {
            const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
            for (let row = 0; row < grid.length; row++) {
                for (let col = 0; col < grid[row].length; col++) {
                    if (grid[row][col] === '') {
                        grid[row][col] = alphabet.charAt(Math.floor(Math.random() * alphabet.length));
                    }
                }
            }
        }

        // Handle the click event on a grid cell
        function handleCellClick(row, col) {
            const cell = document.querySelectorAll('.cell')[row * gridSize + col];
            if (cell.classList.contains('selected')) {
                cell.classList.remove('selected');
                selectedCells = selectedCells.filter(c => c.row !== row || c.col !== col);
            } else {
                cell.classList.add('selected');
                selectedCells.push({ row, col });
            }
            checkIfWordFound();
        }

        // Check if the selected word is correct
        function checkIfWordFound() {
            let selectedWord = selectedCells.map(cell => grid[cell.row][cell.col]).join('');
            if (wordsToFind.includes(selectedWord)) {
                selectedCells.forEach(cell => {
                    document.querySelectorAll('.cell')[cell.row * gridSize + cell.col].classList.add('selected');
                });
                wordsToFind.splice(wordsToFind.indexOf(selectedWord), 1); // Remove the word from the list
                selectedCells = []; // Reset the selection
                if (wordsToFind.length === 0) {
                    showPopup();
                }
            }
        }

        // Show the prize popup
        function showPopup() {
            popup.style.display = 'block';
            overlay.style.display = 'block';
        }

        // Close the popup
        function closePopup() {
            popup.style.display = 'none';
            overlay.style.display = 'none';
        }

        // Initialize the game
        renderGrid(grid);
    </script>
</body>
</html>
