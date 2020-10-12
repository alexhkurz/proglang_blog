# Troubleshooting Haskell Installation 

When installing Haskell there tends tobe many issues that can arrise. This  will go over how to troubleshoot through these issues on Mac. I will also go over my experinece and the issues I faced when installing haskell.

## Installation Process

For Mac OS the installation is quite simple. There are only two commands you need 

```
curl -sSL https://get.haskellstack.org/ | sh
```

and 
```
stack exec ghci
```

There arent really many issuses I faced when installing Haskell on my Mac computer. It was quite straightforward 

 <br><br>
### A few problems you might encounter:

**Homebrew Not Installed** 
You may need homebrew to sucesfully install ghci. you can do this by typing this in: 
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

**Comand Line Tools Not Downloaded**
You may need to update or download your command line tools to be able to install Haskell. You can do this by going to this website on apple 

https://developer.apple.com/download/more/

![image](/appleimage.png)

<br><br>

## How do I know GHCI is working?

Simple! just type ghci in your terminal and check if you see something similar to this

```
an-macair:~ donaldsheng$ ghci
GHCi, version 8.8.2: https://www.haskell.org/ghc/  :? for help
Prelude> pi
3.141592653589793
Prelude> exp 1
2.718281828459045
Prelude> :q
Leaving GHCi.
an-macair:~ donaldsheng$e
```


