---
title: Final Year University Project
description: A mobile game that I developed, inspired by the after-image that application windows leave behind on a slow computer.
skills: "Operations Research, Java, CPLEX"
thumbnail: assets/img/SnakeGameEditor.PNG
thumbnail-alt: Task Graph
action: Repo
action-dest: https://github.com/ThatRandomCoderNZ/task-scheduling
---

I genuinely thought to myself at one point that this may be the hardest thing I’ve ever done. If the title makes sense to you then please understand that I had never been exposed to any proper form of operations research or optimisation before starting this project. On the other hand, if you have no idea what column generation is, then we’ve got a lot in common. Unlike Chen & Powell [referece] however, I’ll try and take it easy on you.

This project is based a theoretical problem where we have an input graph of tasks that take x amount of time to complete that are to be scheduled across multiple processors. Just to complicate things further, tasks much be completed in a certain order and there are additional communication costs on tasks depending on what processor they are scheduled on.

Throughout the whole of 2022 this project has demanded intense research deep into optimisation theory and required me to really brush up on my linear programming skills. I experimented with a range of different languages and linear program solvers such as Gurobi with Python or GLPK with Julia. Eventually however, I couldn’t deny my comfort with Java and settled with Java in concert with the CPLEX API.

The solution for this problem involves formulating a mathematical representation of the various constraints that describe the situation. These constraints are then manipulated into a form where they can be broken down into subproblems which is referred to in the literature as Dantzig-Wolfe decomposition. From there the subproblems can be solved iteratively where the solution of the previous subproblem will inform the input of the next, or in other words, what columns will be generated for the next iteration.

Despite the difficulty I had translating mathematical concepts into my OOP mind, I’m grateful for this project as it helped me grow my research skills to new heights and made me consider new approaches to problem solving. I’ve left out a lot of the technical details here but if you’d like to read further, feel free to leaf through my final year report [Coming October 2022].