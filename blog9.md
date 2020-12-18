# Investigating Recursive Functions Across Languages pt 2

Here is the second part of this blog series. Lets investigate multiplication now!


### Multiplication

Multiplication is written in Haskel recursively like this

**Haskel:**
```
mult :: NN -> NN -> NN
mult O n = O
mult (S O) n = n
mult (S n) m = add m (mult n m)
```

Now lets look at it in different programming languages

**Python:**

```
def product( x , y ): 
    # if x is less than y swap 
    # the numbers 
    if x < y: 
        return product(y, x) 
      
    # iteratively calculate y 
    # times sum of x 
    elif y != 0: 
        return (x + product(x, y - 1)) 
      
    # if any of the two numbers is 
    # zero return zero 
    else: 
        return 0

```

**Java:**
```
    static int product(int x, int y) 
    { 
        // if x is less than  
        // y swap the numbers 
        if (x < y) 
            return product(y, x); 
      
        // iteratively calculate  
        // y times sum of x 
        else if (y != 0) 
            return (x + product(x, y - 1)); 
      
        // if any of the two numbers is  
        // zero return zero 
        else
            return 0; 
    } 
```
**C++:**
```
int product(int x, int y) 
{ 
    // if x is less than  
    // y swap the numbers 
    if (x < y) 
        return product(y, x); 
  
    // iteratively calculate  
    // y times sum of x 
    else if (y != 0) 
        return (x + product(x, y - 1)); 
  
    // if any of the two numbers is  
    // zero return zero 
    else
        return 0; 
} 
```

*Note code taken from:* https://www.geeksforgeeks.org/product-2-numbers-using-recursion/

Now, unlike addition, the two solutions here are a bit different as we can see. If anything it looks like the answers in other languages might be mor complicated than in Haskel.

Lets examine whats the same and different

In this function in Haskel we can see we have to base functions:

```
mult O n = O
mult (S O) n = n
```

The first one is for if you are multplying by 0 in which case we  know that the answer will be 0

The second is if you are multiplying n by 1 in which case we always know the answer will be just n

Then in the final line:
```
mult (S n) m = add m (mult n m)
```

We basically use the add function we defined before alone with the mult function recursivelt to go through essentially this equation recursively

x + (x * (y - 1))

The other programming languages, go about doing multipiclation recursively a little differently.

What they do is make sure that the number that is greater is inserted first as seen here in C++:

```
 if x < y:
        return product(y, x)
```

Then if neither of the numbers is 0 then it will finally use the same equation to calculate recursion:

x + (x * (y - 1))




