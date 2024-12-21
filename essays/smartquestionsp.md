---
layout: essay
type: essay
title: "Getting The Help You Need"
# All dates must be YYYY-MM-DD format!
date: 2024-09-11
published: false
labels:
  - Questions
  - Answers
  - StackOverflow
---

How does one go about getting the help they need as a software engineer? In a time where a multitude of resources are readily available with a simple search, knowing how to get the answer you need is crucial. When troubleshooting and/or looking for more information on a problem, its best to be as concise as possible and ensure that you are trying to exhaust any and all information that is already available to you. 

Try different approaches to your problem and check your syntax to make sure its not a small overlooked error.
Do not hesitate to reach out to a friend who may know how to solve your problem. 
Make sure the question has not already been asked.

By doing so, you can save yourself time and get the help you need to get your project done.

After looking at some questions on StackOverflow, here are two that stuck out to me.

[What is the '-->' operator in C/C++?](https://stackoverflow.com/questions/1642028/what-is-the-operator-in-c-c)
After reading Hidden Features and Dark Corners of C++/STL on comp.lang.c++.moderated, I was completely surprised that the following snippet compiled and worked in both Visual Studio 2008 and G++ 4.4. I would assume this is also valid C since it works in GCC as well.

Here's the code:
```
#include <stdio.h>
int main()
{
    int x = 10;
    while (x --> 0) // x goes to 0
    {
        printf("%d ", x);
    }
}
Output:

9 8 7 6 5 4 3 2 1 0
```
Where is this defined in the standard, and where has it come from?


After looking through this thread, I have noticed that some of the answers are sarcastic and unhelpful. Others, who have tried to help agrees on the basic claim that it counts down to 0 in this situation, which is already stated as commented in the code. The rest of the discourse is other users arguing about why is does that, what is an equivalent code, and whether it is or is not ethical to use it. Overall, the original poster has gotten many answers but I do not believe they got the exact answer they were looking for either. 

The second question that stuck out to me was: 
Why do certain random strings produce colors when entered as background colors in HTML?

For example, bgcolor="chucknorris" produces a red background:
```
<body bgcolor="chucknorris"> test </body>

Conversely, bgcolor="chucknorr" produces a yellow background:

<body bgcolor="chucknorr"> test </body>

```
This holds true across various browsers and platforms. What’s going on here?
[Why does HTML think “chucknorris” is a color?](https://stackoverflow.com/questions/8318911/why-does-html-think-chucknorris-is-a-color)

In this question’s thread, the answers given are concise and in-depth explanations, while many agree on the same reasoning. Each answer may vary in the way they explain via their visuals but are all still helpful in answering the question. They state that when converting 'chucknorris', the system only recognizes the c in the string and converts the rest to 0's which will give you c00c0000000. Then, it tries to convert it to RGB format where the values are then R: c00c, G: 0000, B: 0000. After, the first two numbers of each value are taken resulting in R: c0, G: 00, B: 00. Finally you are given the value #C00000 or (192, 00, 00), resulting in a red hue.
Not only did the responses answer the users question in their specific example, but they could also apply what they learned to related questions on how strings are converted into a RGB color on HTML.

