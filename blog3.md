# Guide to Abstract Syntax 

Abstract syntax is a useful way of writing in Haskel and in functional programming languages. Lets go over what it is, how to write could with abstract syntax, and go over some examples 
<br>

## What is abstract syntax?

**Abstract Syntax** is a process in which numbers are represented not in the tradional 1,2,3,4,5 format but rather in terms of sucesssors. For example the number 2 is not written as 2 when using positive numbers. Its written as the sucessor as 1.

To really understand how this is used in Haskell lets look at a couple of examples:

**Ex1.** Adding two natural numbers
```
add :: NN -> NN -> NN
add O n = n
add (S n) m = S (add n m)
```
As you can see here we are defining addition in a different way than we normally would do. We are setting the base case as 0 n = n (as this is natural numbers). We do this because we know that adding anything 0 must be n.

 *We then, in the next line, recursively calculate the addition of all other numbers in terms of sucessors from 0*

**Ex2.** Dividing a natural number by a positive number
```
-- use recursion over NN
divP :: NN -> PN -> NN
divP O n = O
divP n I = n
divP n m = add (S(O)) (divP (subtrNP n m) m)
```
In this case we have two base cases becaue we are dividing a natural number by a posotive number. 

For the natural number base case we have *O n = O* because natural numbers start at 0 and anything multiplied by 0 = 0

In the posotive number vase we have *n I= n* because posotive numbers start at 1 and anything multiplied by 1 is just that number

The final line calculates the division by recursively calling the function for all the subsequent cases based of these base cases