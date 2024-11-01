---
title: "Calculations in R"
output:
  html_document: default
  pdf_document: default
  word_document: default
date: "May 14th 2022"
theme: cerulean
---

<!-- For more info on RMarkdown see http://rmarkdown.rstudio.com/ -->

## Name: Mensah Patrick-

### Calculations in R programming

### R also serves as a calculator



```{r echo=FALSE}

log(56/8.3)
```

### Each line can contain at most 8192. 
```{r echo=FALSE}
5+4+7+8+10+100+2000+400
```

### Two or more expressions can be placed on a single line as long as the are separated by semi-colons
```{r echo=FALSE}
300+34; 4*282; 30-10; 200/12
```


### For large numbers, R uses exponents
```{r echo=FALSE}
1.8e5 # 18000 because the e5 means we move the decimal point 5 places to the right 
1.5e-4 # 0.00015 because the e-4 means we move the decimal point 4 places to the left
6.9+8.5i # this is a complex number with the real part (6.9) and the imaginary part (8.5) and i is the square root of -1  

```

### Complex variables/ numbers in R. 
###. Complex numbers have the real part  and the imaginary part, which is identified by lower case (i)

```{r echo=FALSE, fig.align='center'}
z <- 7.8 - 6i
z
# Finding the real part 
Re(z)

# Finding the imaginary part
Im(z) 

# Finding the modulus (the distance from z to 0 in the complex plane by Pythagoras, assuming (x) is the real part and y is the imaginary part (square root of x^2 + y^2)
Mod(z)

# Finding the Argument (Arg(x+yi) = atan(y/x))
Arg(z)

# Finding the complex conjugate (that is changing the sign of the imaginary part)
Conj(z)

# Membership (to determine if the equation is a complex variable or not)
is.complex(z)

# Coercion (Forcing any value to be a complex variable)
as.complex(4.9)
```


### Rounding of numbers in R. Assuming we are taking 4.8 as an example

```{r echo=FALSE}
# the "greatest integer less than" function is floor 
floor(4.8) 
# the "next integer" function is ceiling 
ceiling(4.8)

# You can create a function for this by rounding to the nearest integer by adding 0.5 to the number, then using floor. Example 

rounding <- function(x) floor(x+0.5)

rounding(4.8)
rounding(2.1)

# Rounding negative numbers. Remember -2 is greater than -3
## Remember that rounding negative numbers means you are rounding towards zero
ceiling(-3.7)
ceiling(-4.4)

# with floor, remember we are staying away from zero
floor(-3.7)
floor(-4.4)

# Striping the decimal part using the trunc function 
trunc(45.77)
trunc(4.9)

```

### Using the round function 

```{r echo=FALSE}
round(x= 5.6, digits = 0)
round(6.8, 0)
round(74.2, 0)
round(-75.4, 0)
```

### Significant figures. Note that this is different from round
```{r echo=FALSE, fig.align='center'}
signif(x= 2356866542, digits = 7)
signif(2356866542,  7) # same answer 
signif(12345678, 6)
```


### Arithmetic
### The screen prompt is a calculator. Remember that R also uses BODMAS

```{r echo=FALSE}
10 + 20 - 5 * 2

```

### Powers uses the caret symbol

```{r echo=FALSE}
3^5 / 3

### The log function gives log to the base e (2.718282) for which the antilog function is exp
log(10)

exp(2)

### The old fashion. Log 3 to the base 10

log10(3)

### log to the other bases are also possible. Example log 7 to the base 4

log(7,4)

### Squre root 
sqrt(9)

### Factorial 
factorial(7)

### binomial coefficient 
choose(6,2)

### Generating n random numbers between 0 and 1 from a uniform distribution 
runif(7)

### you can change the minimum and the maximum
runif(50, min = 1, max = 100)

### sine cosine and tangent of x in radians 
sin(90)

cos(90)

round(-0.4480736)

tan(90)
tan(45)

### Inverse trigonometric transformation of real or complex numbers 
acos(-1)
asin(-1)
atan(-1)

### Inverse hyperbolic trigonometric transformation of real or complex numbers 
acosh(3)
asinh(3)
atanh(-1)

### absolute value 
abs(-199)
abs(45)

pi

sin(pi/3)

cos(pi/2)

```


### Modulo and integer quotient

```{r echo=FALSE}
### integer quotient  % / % and remainders % %
## Example .  How many 11s are in 122

135 %/% 11

### if we want to know the remainder (Modulo)
135 %% 11

## Modulos are very important to determine if a number is even or odd 
### Odd numbers have modulo 2 value 1 and even numbers have modulo 2 value 0
12%%2

55%%2


### if you want to test if a number is an exact multiple of of some other number 
### Example, if we want to find out if 1555673 is a multiple of 8
1555673 %% 8 ==0
625872 %% 8 ==0

```


```{r echo=FALSE}
### Variables and name assignment in R
### There are are three important things to remember when selecting names for your variables 

### 1. Variable names are case sensitive. Example x is not the same as X
### 2. Variable names should not begin with numbers or symbols. Example (2y) or (@x)
### 3. Variable names should not contain blank spaces (pat.men) not (pat men)


```


```{r echo=FALSE}
### Variable assignment 
x <- 100
x

## This is not the same as 
x < - 100  ## Note that there is a space between the less than sign and the minus sign
 
### this is a question. This is asking whether x is less than 100



```

```{r echo=FALSE}
### Operators 
## >=,  < , <= , ==, !=
##,  !,  & , |
### <- , ->
### $ list indexing 
### : creating a seqeuence 

```

```{r echo=FALSE}
### Integers 
x <- c(4,6,7,8,9,23,45,23)
x
is.integer(x) # is x integers 
is.numeric(x) # is x numeric


### Converting them to integer

x <- c(4,6,7,8,9,23,45,23)
x<- as.integer(x)
is.integer(x)


## the integer function also works as trunc when applied to real numbers and removes the imaginary parts

as.integer(7.8)

as.integer(-4.6)


as.integer(3.6 -3i)
```


