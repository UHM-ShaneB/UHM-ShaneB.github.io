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

## About The Project

This project was my attempt in creating a sudoku puzzle game using Java. Sudoku is a puzzle game in which you are presented with a 9x9 grid of squares that are split up into groups of smaller 3x3 squares. The objective is to fill each square in with a number ranging from 1 to 9. Some squares will already have a number filled in. However, when filling in these numbers, certain conditions must be satisfied:

  - All squares must have a number
  - The same number cannot appear in the same 3x3 square, column, and row. 

This sudoku I created features four difficulties which determines the amount of numbers given to the player. The higher the difficulty then less numbers are given to help the player solve it. When the player solves a puzzle, it will check to see if the postion of the numbers satisfies the condition. It currently outputs "Congratulations" or "Try Again" to the console depending if the user completes the puzzle satisfying the conditions. 

## My Contribution

This was a solo project that I created during my freetime in a span of about a month. I pretty much wrote all the code but I did have to use the Java libraries. To make it user friendly I had to make use of GUI elements from the swing package as well as some elements from the uitl package like ArrayList. I also had to create an algorithm to determine where the given numbers are postioned. 

### *Algorithm*

My idea was to randomly fill each row with numbers from 1 to 9 that satisfies the condition of no duplicates in each 3x3 square, column and row. After all the squares were filled, randomly chosen squares would have their numbers removed. The amount of removed numbers is determined by the difficulty the user had set it too. Whatever numbers were left would be grayed out and unable to be modified by the user.

## Learning Experience

I went into this project thinking it would be as simple as creating a calculator. A lot of what I did here was similar to some of the things I did when I wrote the code for my calculator app. But it turned out to be very difficult, thus why I took aroud a month to develop a working sudoku app. Figuring out the algorithm was what took the longest since no mattter what I tried, it ended up in failure. However, I would always build off those failed ideas to come out with the current algorithm. As a matter of fact, my first idea was to just put numbers in random squares but when you try to solve it, sometimes you'll end up with a stalemate where a row, column, or 3x3 square is missing a number but no mater where you put it, it fails the conditions. I learned that sometimes you'll end up in a slump. But that doesn't mean you need to give up. You just need to walk away from it for a while, maybe even for a day, and come back with a fresh mindset which is what I did. 

[Link to repository](https://github.com/UHM-ShaneB/Shane_Sudoku)
