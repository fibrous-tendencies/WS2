## Homework 1 | Coding for Design II | Due February 11 @ 11:59 PM | 20 Points

Welcome to Homework 1! In this assignment you will be further exploring some of the topics covered in the **Introduction to Optimization** module. We will not cover everything you need to complete the assignment in the first class but you should be able to get started. You will need to develop your own .ipynb for part of this assignment. 

You should feel free to copy and modify code from the in class workshops to complete the assignment. All responses and plots should be collected into a single pdf file that has letter sized (8.5" x 11") pages. 

### 1 | Designing an Optimization Problem

In the first section of this assignment you will be designing (but not implementing) a design optimization problem. In your problem you should have multiple variables that control various aspects of your design. 

#### 1.1 | Describe the optimization problem

In this section you should describe, with words and/or diagrams, the design space that you would like to optimize. 

This problem needs to be a realistic problem that you are interested in solving. It should not be a toy problem. For example, just trying to maximize the area of a quadrilateral subject to corner coordinate constraints is not a suitable problem to solve. You must define a problem with some real context. You can invent a scenario or use a real one you have encountered where having a process for automatically updating the parameters of your design problem to achieve a particular objective (aka goal) would have accelerated your design process or led to a higher performing result.

You do not need to be able to solve this problem with the algorithms we have covered in class so far, but you may need to revise your problem statement if you read through the following questions and find that you are not able to define the parameters, constraints, constants, and objective function in a concrete way.

- `What is your optimization problem?`
- `Why is this problem suitable to be solved with an optimization process?`
- `If you develop a method for optimizing this problem, what would this enable you to do?`

#### 1.2 | Describe the optimization parameters (aka variables)

In this section you will more specifically define all of the design variables for your optimization problem. 

The design parameters could be something like number of legs on a table, positions of the vertices of a mesh, ratio of stiffness between two materials, etc... The important thing about these variables is that they have some *numerical value* associated with them. 

Something like 'sustainability' or 'visual softness' are not immediately quantifiable with numerical values although you may come up with a proxy for these properties of a design such as 'amount of embodied carbon' or 'curve radius' that stands in for these more abstract variables.

- `How many design parameters do you have?`

For each of your parameters you should answer the following questions. If you have repeated parameters that do the same thing, just with multiple instances, you only need to describe it once. I.e. if you are optimizing the color of all of the pixels in an image and all the pixels are treated equally during the optimization then you only need to answer the following questions for a single pixel. 

- `What is this parameter controlling?`
- `Is this parameter continuous or discrete?`

#### 1.3 | Describe any constraints on your parameters

Not every parameter should be allowed to take any value. In this section you must answer the following questions for each parameter:

- `Is there any constraint on this parameter? I.e. can it range all the way from -infinity to infinity or does it have limits?`
- `If the parameter does have a constraint, what is it?`
- `Why are there (or are there not) constraints on this parameter?`

#### 1.4 | Describe any constants in your problem

In this section you will address any values that are important for evaluating your objective function, but will remain constant throughout the optimization problem.

It is important to distinguish here between constants and parameter bounds. 

These constants can be things such as the Young's modulus of a material required for an FEA simulation, the maximum height of a final solution, etc. 

#### 1.4 Describe your objective function

In this section you should describe how you plan to evaluate the design resulting from a particular combination of parameters. An *objective function* (sometimes called a loss function in ML/AI or a cost function) is evaluated to give a score to a particular design. 

During the optimization process you will generally try to minimize (or maximize) the score of this objective function. The combination of parameters that produce the lowest (or highest) score will correspond to the best solution found in the design space.

- `What is the objective you are trying to minimize (or maximize)?`
- `How do you think your variables should contribute to the objective score?`

> Note: If you objective is not convex (most design spaces are not convex) then it is very possible that you may end up in a local minimum instead of at a global minimum. There are different ways of trying to find a global minimum, but in general this is a very hard problem to solve. 

## 2
