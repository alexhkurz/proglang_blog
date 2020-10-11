# Imperative vs Functional Programming Guide

Imperative and Functional Programming languages, while both being programming languages, were made, and are used for very different things. It is important for a programmer to understand both these types of programming and have both of them as tools in your arsenal that you can use in the appropriate situation. 

## First lets define them...

### **Imperative Programming**
This is the type of programming that many people are used to using. It is essentially a sequence of lines (statements), that are executed in turn when the program is run.

**Ex.** Java, Python, C++ are all examples of imperative languages 

```
int num1 = 2;
int num2 = 5
int num3 = 3
int avg = (num1 + num2 + num3) / 3
```
In this example written in Java, each line is executed in sequence. Three variables are stored and then the average is calculated last 

### **Functional Programming**
Functional Programming is a type of declaritive programming language. It was made for a mathmatical approach to programming. The way you write things mathmatically is often the way you write them in a functional programming languages. This type of programming language bring about certain advantages like readability.

**Ex.** WolfraLanguage, Ocaml, and Haskell are all examples of functional programming languages

```
less :: NN -> NN -> Bool
less O O = False
less n m = if ((subtr n m) == O) && ((subtr m n) == O) -- checks if they are equal
    then False
    else if ((subtr n m) == O) && ((subtr m n) /= O) then True 
    -- if n - m = 0 but at the same time m - n is not equal to 0 then n < m must be true
    else False
```
This is an example written in Haskell, you can see that it is written in terms of function rather than statements. This method determines wether or not a natural number is less than another natural number 

## So when do I use one over the other?

Use **Imperative** languages when you have a primary function for your code and you want a blueprint, object-oriented design to your code. Then from that you primarly add new items to the program.

Use **Functional** languages when you have a fixed set of things that your vode does. When you only want to add new operations on exisiting data that often stays constant in the program.