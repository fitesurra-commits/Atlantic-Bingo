# Atlantic-Bingo
Enjoy Bingo
function generateColumn(min, max) {
    const numbers = [];
    while (numbers.length < 5) {
        let num = Math.floor(Math.random() * (max - min + 1)) + min;
        if (!numbers.includes(num)) numbers.push(num);
    }
    return numbers;
}

// Example: Generate all 5 columns
const board = {
    B: generateColumn(1, 15),
    I: generateColumn(16, 30),
    N: generateColumn(31, 45), // Replace N[2] with "FREE" later
    G: generateColumn(46, 60),
    O: generateColumn(61, 75)
};
