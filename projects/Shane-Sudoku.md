---
layout: project
type: project
image: img/Shane_Sudoku_Img.png
title: "Shane Sudoku"
date: 2023-02-04
published: true
labels:
  - Java
  - Sudoku
summary: "A sudoku puzzle app"
---

This project was my attempt in creating a sudoku puzzle game using Java. Sudoku is a puzzle game in which you are presented with a 9x9 grid of squares that are split up into groups of smaller 3x3 squares. Some of the squares will already be filled out with numbers ranging between 1 and 9, and the player must fill the rest of the squares making sure that it follows the condition where same number does no appear in the same 3x3 square, column, and row. This sudoku I created features four difficulties which determines the amount of numbers given to the player. The higher the difficulty then less numbers are given to help the player solve it. When the player solves a puzzle, it will check to see if the postion of the numbers satisfies the condition.

This was a solo project that I created during my freetime in a span of a few weeks. I pretty much wrote all the code but I did have to use the Java libraries. To make it user friendly I had to make use of GUI elements from the swing package as well as some elements from the uitl package like ArrayList. I also had to create an algorithm to determine where the given numbers are postioned. My idea was to randomly fill each row with numbers from 1 to 9 that satisfies the condition of no duplicates in each 3x3 square, column and row.

From this project I expanded my knowledge of GUIs as well as using the extends keyword which allows me to create multiple classes that uses the same functions. This allowed me to keep things a little more organized.

[Link to repository](https://github.com/UHM-ShaneB/Shane_Sudoku)
