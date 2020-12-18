# Investigating Recursive Functions Across Languages

Recursive functions are often confusing for many, and are harder to follow than iterative functions. It is especially confusing when you are doing a recursive function in a new programming language like in Haskel. In this blog we will be exploring how recursive functions are written in different languages to compare and contrast them to Haskel, and from that to hopefully better understand the Haskel version. This will be a 2 part blog. This first blog will investigate addition


### Addition

Addition is written in Haskel recursively like this

**Haskel:**
```
add :: NN -> NN -> NN
add O n = n
add (S n) m = S (add n m)
```

If you are someone new to this language it can be hard to understand with all the symbols and letters, so lets look at it in different programming languages

**Python:**

```
def recur_sum(n):
   if n <= 1:
       return n
   else:
       return n + recur_sum(n-1)

```

**Java:**
```
 public static int addNumbers(int num) {
        if (num != 0)
            return num + addNumbers(num - 1);
        else
            return num;
    }
```
**C++:**
```
int add(int n)
{
    if(n != 0)
        return n + add(n - 1);
    return 0;
}
```

Now you might be thinking, how come the recursive functions in all the other languages look similar, but they dont look similar to Haskel. Well the difference with Haskel is that is mathmatically based, however, the fucntions are closer to eachother than you might think.

**You see the first line is just defining the function.**

This line:
```
add :: NN -> NN -> NN
```

is essentially the same as these lines:

```
def recur_sum(n):
```
```
 public static int addNumbers(int num) {
```

```
int add(int n)
```

So whats with the NN->NN->NN?

Well, all that is saying is that you pass in two natural numbers, and you get a natural number out as an output.


**So what about the second line?**

Well this is essentially the same as a line in the other langauges as well.

This line:
```
add O n = n
```

is essentially the same as these lines:

```
if n <= 1:
       return n
```
```
 else
    return num;
```

```
return 0;
```

You see each of these lines are taking care of the base case. It is making sure that once the recurssion hits 0, the recursion ends so we actually get an answer and there is not an infinite loop

**Finally what about the third line?**

Same thing!

This line:
```
add (S n) m = S (add n m)
```

is essentially the same as these lines:

```
else:
       return n + recur_sum(n-1)s
```
```
 if (num != 0)
            return num + addNumbers(num - 1);
```

```
if(n != 0)
        return n + add(n - 1);
```

This is where the meat of the recursive function is for all the programs. they are simply all returning what the number is currently at and then adding n to it with the number one below it after it recursively goes through the add function


Hopefully this investigation helped you understand recurisve addition in Haskel. Check blog9 for multiplication



