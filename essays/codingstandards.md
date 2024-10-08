---
layout: essay
type: essay
title: "Coding Standards"
# All dates must be YYYY-MM-DD format!
date: 2024-09-25
published: true
labels:
  - ESLint
  - TypeScript
  - New Skills
---

# Coding Standards
In the world of computer science, coding is heavy on formalities. *Every little thing matters*. I remember in my first computer science classes I was taught by my professors that coding standards focus on syntax and general formatting/spacing. For example:

- How you space out your code can affect the readability and neatness of your code.
- Naming variables helps the reader understand how the code works.
- Comments should be made to help the reader understand the code.
- Syntax should be consistent to ensure your program runs properly.
  
One of the most minor, yet debilitating standard is that spelling and case-sensitivity matters. I have found myself hundreds of times banging my head on the wall, trying to figure out why my code was not working only to figure out I forgot a letter in a variable. My code would still compile properly because technically it was syntactically correct. All my errors had to be self-checked through the vague feedback given by my current IDE until ESLint walked into my life.

Having ESLint in VSCode has been a love hate relationship for me. I appreciate the features that will provide the correct syntax, as the transition from Java to JavaScript/TypeScript slightly varies. Additionally, I appreciate how when typing it will automate similar words so when I am typing variables I can see if there was a misspelling somewhere. Sometimes I forget when assigning properties in typescript, I should be using a colon instead of the equal assignment operator and ESLint will point that out to me. When pointing out your errors, ESLint will be able to give you an explanation and choices in how to correct them. When you hover over the error, occasionally there is an option that will take you to a link that has more in-depth information.

Although helpful, I do find it tedious for the very minor problems such indentations/blank spaces. Often times when I rush through my code, I forget about spaces and to have to go back and fix them individually is a pain but, I learned that when you hover over the error, it has a “quick-fix” option and it can correct all of the occurrences of that problems. Though, I would not necessarily use that option for more complex problems because I felt like it completely changed my code, and I had no idea what was going on anymore. ESLint can be daunting at time especially when your whole code starts getting underlined with red but it is ultimately there to help you. 
