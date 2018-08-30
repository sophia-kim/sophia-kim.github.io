---
layout: project
type: project
image: images/micromouse.jpg
title: Project 1
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2018-03-DD
labels:
  - Java
summary: As an assignment of the course ICS 211, I created a project...
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>

Hexadecimal sudoku is a 16x16 sudoku that solves the puzzle so that no values between 1 and 16 are used more than once on the same line going vertically, horizontally AND diagonally. If the same number repeats in any way in any direction, the puzzle solver may need to reconsider their choice of the input. When the solver completes the sudoku without the numbers conflicting, then the puzzle is considered complete and correct. 

For this assignment, I had to create a program that takes in an incomplete sudoku puzzle as an input and outputs a correct, completed conditions. The program achieves this by running numerous functions to check the values that already exist in the sudoku and finding the ultimate solution that satisfies all the conditions. One of the functions that aids in running this program is checking whether a value between 1 and 16 is valid or not. It first checks if the value is already in the given in the provided array of elements in the 16x16 sudoku. If the value already exists in the given array, then the function checks i

Here is some code that illustrates how we read values from the line sensors:

```js
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [UH Micromouse Website](http://www-ee.eng.hawaii.edu/~mmouse/about.html).



