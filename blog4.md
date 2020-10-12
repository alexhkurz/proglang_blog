# Tips for Programming in Haskell

Haskell is not only a new programming language for many, but an introduction to a new type of programming. To get you along on your journey with Haskell here are a few useful tips for writing code in Haskell 

## Tips

1. **Make sure to use O instead of 0 and I instead of 1**
    
    This is a simple one but one that tripped me up personally many times and remebering this tip can save you from wasting time and pulling your hair out trying to figure out why your code isn't running
2.  **Remember your base cases**

    When builiding recursive functions that are supposed to perform operations (such as division) make sure you write your base cases. For example:
    ```
    divP O n = O
    ```
    Should be written as a base case for dividing with natural numbers as anything divided by 0 is 0
3. **Use the standard libraries avaliable to you**

    The standard libraries that Haskell provides you are useful. It is not necessary to revinvent the wheel unless you need to make critical modifications to a certain function to ensure it works 
4. **Remember that lists are not arrays**

    Remember that accesing the nth term in a list is not the same as it would be in an array. A list requires you to start from the beginning and traverse through it untill you reach the nth item on the array. It is a very ineffiecent process and so you should not do it when its not absolutely necessary to do so
5. **Think about it mathmatically**

    Remeber that Haskell is a functional programming language. This means that it was made for the purpose of writing fucntions in a simpler, more mathmaticall method. Try to ignore what you learned from other imperative programming languages and think as each line as a mathmatical function.

6. **Do not use Int when not needed**

    If you are not going to use the range of integer numbers use something less exclusive to be more efficient. For example use natural numbers if you don't need negative numbers. Use postive numbers if you don't need negatives or 1.