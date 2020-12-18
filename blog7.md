# Exploring Abstract Reduction Systems

Abstract Reduction Systems can be confusing at first to get the hang of. As the name suggests, its very abstract and so when things are not concrete there is a lot of things you can get lost in. I think what was most helpful for me was going through some examples of Abstract Reduction Systems so thats what we are going to do here going step by step

### So lets do the example

Lets say the abstract reduction system is defined by these rules:

a -> b
bf -> d
bb -> b
de -> f
df -> g
ga -> b


and you want to reduce the string "aaadefacc" to its normal form

How would we approach this?

Well its quite simple, do not get confused by the letters just start replacing things!

*Note: every change will be hilighted in bold from step to step*

First lets try replacing the 'de' to 'f'

aaaadefacc
aaaa**f**fac

Next lets try replacing the a's to 'bb's

aaaaffac
**bbbb**ffab

Next lets try replacing the bb's to 'b's

bbbbffab
**bb**ffab

Oh look we can do it again! lets replace the final 'bb'to 'b'

bbffab
**b**ffab

Now we can replace bf!

bffab
**d**fab

We are getting close to the end now lets replace 'df' with 'g'

dfab
**g**ab

Lets replace 'ga' with 'b'

gab
**b**b

And finally we can reduce 'bb' to 'b'

bb
**b**

And we are done! We know this because the string we have ended with can no longer be reduced with the rules to the ARS! See, if you take it step by step, and bold what changes you make it is very easy to keep track of things and eventually get to the normal form. Hope this step through step walkthrough helped your understanding of ARSs!