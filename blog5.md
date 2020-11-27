# Lamda Calculus Evaluation Guide

It took me a while to grasp how to evaluate lamda calculation functions. This guide is meant to be a collection of information that I found and researched that help me to finally understand how to evaluate these functions

**First you must understand the three porgramming constructs of Lambda Calculus**

### 1. Abstraction
Lets look at this function

    λx.e

The program is *e* and that program could contain a variable known as *x* We refer to this as abstraction because *e* does not depend on *x*

##### Free vs Bound Variables

Its important to note that if you see this function

λx.x

*x* is considered bound because it is both the body of the function and a paramater. However if the function is like one we've seen previously:

λx.e

*e* is considered free because as you can see it wasn't declared before, or in the body of the function


### 2. Application
Lets look at these two programs

e<sub>1</sub>e<sub>2</sub>

This is a progarm (function) that uses the first listed function e<sub>1</sub> as the **function** to e<sub>2</sub> the **argument**

### 3. Variables 

Anything that is considered a basic program is now considered the variables

*Note: the three constructs above are taken largely from the notes here,* https://hackmd.io/@alexhkurz/S1D0yP8Bw
*I added more depth using these websites:* 
https://learnxinyminutes.com/docs/lambda-calculus/

** Now lets look at evaluation of these functins**

##Evaluation
Now that we know the constructs, lets look at how to evaluate using β-Reduction.
To do this we should replace any occruence of an *x* variable with a variable. Lets use *a*

(λx.x)a evaluates to: a
(λx.e)a evaluates to: e

When we combine multiple lambda functions to allow for multi-paramater functions we call that **currying**

Lets look at a more complicated example and how we would simplify it

(λf.λx.f(fx))λx.x
λx.(λx.x)((λx.x)x)
λx.((λx.x)x)
λx.x

This is a classic example of a multi-paramater function and how you would simplify the function. As you can swee we are using the β-Reduction rule in each step to reduce the function. Note that often the function before a reduction is known as the redex and the function after reduction is often referred to as the contractum

Another importnat note is that you can only substitue if a variabel is *free* not if they are bound.

*Sources:* https://cs.stackexchange.com/questions/4990/lambda-calculus-simplification

https://learnxinyminutes.com/docs/lambda-calculus/
