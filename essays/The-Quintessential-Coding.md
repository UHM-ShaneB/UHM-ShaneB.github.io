---
layout: essay
type: essay
title: "The Quintessential Coding"
# All dates must be YYYY-MM-DD format!
date: 2024-02-06
published: true
labels:
  - ESLint
  - IntelliJ
  - Coding Standards
---
## Coding Standards Is The Way To Go

For the past week I have been writing my Javascript code in IntelliJ. At the same time, I implemented the use of coding standards and I honestly believe it's one of the best techniques to practice when writing code. Following coding standards, in my opinion, improves the quality of the code and makes it look very professional. I believe that coding standards can help a person better understand the language they are using and can make it easier for other people to read your code. 

## A Useful Tool

<img width="150px"
     class="rounded float-start pe-4"
     src="/img/ESLint_logo.svg.png" >
     
It’s not easy for me to remember all of the coding standards. Thankfully there is a tool called ESLint that can help me. It’s my first time using this tool but I think it is very user friendly and wasn’t too difficult to set up. It’s very similar to how word or google docs checks for any grammar or spelling errors and underlines them with a squiggly line if there is one. ESLint underlines anything that violates the coding standards. You can hover over the error and it tells you exactly what’s wrong with it. Some of the violations were not clear for me and that’s probably because I’m still learning Javascript and not familiar with all the terms. One of them said Expected property shorthand which meant I had to use the shorthand syntax. But that’s okay since ESLint provides details of the violations on their website and sometimes It will give you the option to allow ESLint to fix it.

## Coding Standard Violations For Javascript

I've come across a lot of coding standard violations in my code. Some of which are due to me forgetting to go back and change the syntax, and others because I’m so used to how I wrote code in Java that its become a habit.

### Using var, let, and const
	
One coding standard violation that I’ve done, and probably will unintentionally continue doing, involves the use of var, let, and const. Using var is discouraged due to having complications with scoping. Using let and const is much more preferred but which one you use depends on how you use the variables. Using let provides the context that the variable will be reassigned but if it is never reassigned then we have a violation. In this case we should use const since this means we won’t be reassigning the variable. On the other hand, using const for a variable that is reassigned later is also a violation and will probably throw an error if you try to run it.

I never use var when declaring variables so I’m good with that. However, my mind defaults to using let since I’m usually not sure if the variable is reassigned until I finish writing my code.

### Equality And Inequality
Another violation I’ve encountered in some of the code I wrote involves the equality and inequality operators. Javascript provides two different versions for them. The regular operator for equality and inequality is == and != respectively. However the use of these is highly discouraged as it could cause problems since it ignores the datatype. Using === and !=== instead is better practice as they are much more strict since it takes the datatype into account. 

Before I would use the double equals since I’m used to it in Java. I pretty much developed the habit of using the stricter version of the operators instead so you won’t catch me using the regular ones anymore.
