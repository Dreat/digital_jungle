---
title: SOLID for FP
tags: se, fp
---

<status>Status: 🌱 </status>

I have OOP brackground and used SOLID and other OOP techniques to make my code better.

Since then I switched to FP and feel like there's not enough `guidelines` for writing FP code. At the same time I have a hunch that some of the OOP wisdom can be applied here.

- **S**ingle Responsibility Principle - this one is easy and free to take. Just make sure that your methods have "one reason to change" - a single responsobility. Make them small and specialized. Anything with `and` in name can be a sign that there's too much going on
- **O**pen Close Principle - this one is trickier, but if we say that refactoring is flow of making code open to extension - this makes things easier to adapt. Basically you want to be able to add new functionalities withtout altering existing code - and this can be achieved in FP.
- **L**iskov Substitution Principle - 
- **I**nterface Segregation Principle -
- **D**ependency Inversion Principle - can be argued to go with "top level module" as main dependency, instead of more specialized ones.
