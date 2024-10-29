# Sudoku Solver

This project contains a simple Sudoku solver implemented in Java. The `SudokuSolver` class reads a 9x9 Sudoku board, attempts to solve it using a backtracking algorithm, and then displays the solved board or indicates if the board is unsolvable.

## Features

- Solves a 9x9 Sudoku board using a backtracking algorithm.
- Prints the board in a user-friendly format.
- Handles empty cells represented by zeros.

## Getting Started

To run the Sudoku solver:

1. Ensure you have Java installed on your machine.
2. Clone the repository or download the `SudokuSolver.java` file.
3. Compile the Java file using:
   ```bash
   javac SudokuSolver.java
   ```
4. Run the compiled class:
   ```bash
   java SudokuSolver
   ```

## Code Overview

### Main Class

```java
public class SudokuSolver {
    private static final int GRID_SIZE = 9;
    
    public static void main(String[] args) {
        // Sudoku board initialization
        int[][] board = { ... };
        
        printBoard(board);
        
        if (solveBoard(board)) {
            System.out.println("Solved successfully!");
        } else {
            System.out.println("Unsolvable board :(");
        }
        
        printBoard(board);
    }
}
```

### Methods

- **printBoard(int[][] board)**: Prints the Sudoku board in a formatted manner.
- **isNumberInRow(int[][] board, int number, int row)**: Checks if a number exists in a specific row.
- **isNumberInColumn(int[][] board, int number, int column)**: Checks if a number exists in a specific column.
- **isNumberInBox(int[][] board, int number, int row, int column)**: Checks if a number exists in the 3x3 box that the cell belongs to.
- **isValidPlacement(int[][] board, int number, int row, int column)**: Validates if a number can be placed in a specific cell.
- **solveBoard(int[][] board)**: Uses backtracking to solve the Sudoku board.

## Example Board

The provided example board in the `main` method is:

```java
int[][] board = {
    {7, 0, 2, 0, 5, 0, 6, 0, 0},
    {0, 0, 0, 0, 0, 3, 0, 0, 0},
    {1, 0, 0, 0, 0, 9, 5, 0, 0},
    {8, 0, 0, 0, 0, 0, 0, 9, 0},
    {0, 4, 3, 0, 0, 0, 7, 5, 0},
    {0, 9, 0, 0, 0, 0, 0, 0, 8},
    {0, 0, 9, 7, 0, 0, 0, 0, 5},
    {0, 0, 0, 2, 0, 0, 0, 0, 0},
    {0, 0, 7, 0, 4, 0, 2, 0, 3}
};
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any suggestions or improvements.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
