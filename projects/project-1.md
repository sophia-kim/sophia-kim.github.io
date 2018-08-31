---
layout: project
type: project
image: images/hexadecimalsudoku.jpg
title: Project 1
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2018-03-16
labels:
  - Java
summary: As an assignment of the course ICS 211, I created a project that creates a sudoku puzzle solver.
---

Hexadecimal sudoku is a 16x16 sudoku that solves the puzzle so that no values between 1 and 16 are used more than once on the same line going vertically, horizontally AND diagonally. If the same number repeats in any way in any direction, the puzzle solver may need to reconsider their choice of the input. When the solver completes the sudoku without the numbers conflicting, then the puzzle is considered complete and correct. 

For this assignment, I had to create a program that takes in an incomplete sudoku puzzle as an input and outputs a correct, completed conditions recursively. The program achieves this by running numerous functions to check the values that already exist in the sudoku and finding the ultimate solution that satisfies all the conditions. If it has found the correct solution it will print the result in the console of the user's IDE. The program scans and examines each row until reaching an empty space marked as the value -1 in the 16x16 array, and inserts a valid number and continues to repeat the same process. If it turns out that there is no value that meets the expectations of the slot, the program will use backtracking method to take a step back and find a valid value that can be used to occupy the empty slot.


Here is some code that partially demonstrates how the puzzle solver worked:

```js
private static boolean isValid(int[][] sudoku, int row, int column, int val) {
    for (int i = 0; i < 16; i++) {
      if (sudoku[i][column] == val) {
        return false;
      }
    }

    for (int j = 0; j < 16; j++) {
      if (j != column) {
        if (sudoku[row][j] == val) {
          return false;
        }
      }
    }

    int startRow = (row / 4) * 4;
    int startColumn = (column / 4) * 4;
    for (int i = startRow; i < startRow + 4; i++) {
      for (int j = startColumn; j < startColumn + 4; j++) {
        if (!(i == row && j == column) && sudoku[i][j] == val) {
          return false;
        }
      }
    }
    return true;
  }

```



