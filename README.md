![101Script](https://github.com/brettderham/101Script/blob/master/resources/101script-logo.jpg "101Script")

# 101Script

A programming language for beginners.

Repo for Riley Persily, Thomas Ochsner, Simon Wroblewski, Kea Braekman, and Brett Derham

## Introduction

101Script is a simple, easy-to-read programming language intended to be used by those new to programming.  There are multiple ways to write certain operations to ease beginners into this language and others similar to it.  Thanks to 101Script's omission of extra symbols in its syntax, along with the fact that it is weakly and dynamically typed, users will be able to run code without the need to pore over tedious details of the code.

## Features

* `.IOI` file extension
* Weakly & Dynamically Typed
* Multiple names/ways to use basic operations
* Type inference
* String Interpolation
* Simple loop (`while`)
* Semi-colon not required after every line

## Examples


### Variable Declarations
```
const name = "Thomas"           const name = "Thomas"
let age = 21                    let age = 21
let sexy = true                 let sexy = true
```

### Arithmetic
```
x = (10*(3^2))/2                x = (10*((3 ** 2))/2
y = 5 + 3 - 2                   y = 5 + 3 - 2
```

### If Statements 
```
if(x > 5):                      if(x > 5) {
	print(x)		    console.log(x)
else:                           } else {
	print(z)		    console.log(z)
;                               }
```

### While Statements
```
let y = 0                   let y = 0
loopWhile(y < 8):           while(y < 8) {
    f(y)                        f(y)
;                           }
```

### Functions 
```
function multiplyByThree(x):        function multiplyByThree(x) {
    return x * 3                        return x*3
;                                   }
```

### Comments
```
-- single line					// single line
```

### Objects

```
object Shape:                   let shape = {
    name: "circle"                 name: "circle",
    radius: 3                      radius: 3
;                               }
    print(Shape.name)           console.log(Shape.name)

```

**piEstimate 101Script:**  

```
function piEstimate(precision):
    let inside = 0  // or inside gets 0
    counter = 0
    loopWhile(precision notEquals counter):
        let x = random(0,1)     //or x gets random(0,1)
        let y = random(0,1)     //or y gets random(0,1)
        if((x^2+y^2)^0.5 lessThan 1):   //or < 1
            1 addedTo inside
	;
	counter = counter + 1
    ;
    let piEstimt = 4*inside/precision
    return piEstimt
;

    // This example program shows how one may mix word and traditional operations
```

**piEstimate JS:**  

```
function piEstimate(precision) {
    let inside = 0
    for (i = 0; i < precision; i++) {
        x = Math.random()
        y = Math.random()
        if (((x**2 + y**2)**0.5) < 1) {
            inside = inside + 1
        }
    }
    return 4*inside / precision
}
```

### Alternative Operations

There are two ways to write most operations: The typical symbol and a simplified string representation of the operation.  (Shown below)

```
addedTo         +=

multipliedBy    *=

subtractedFrom  -=

dividedFrom     /=

equals          ==

notEquals       !=

gets            =

lessThan        <

greaterThan     >

lessOrEq        <=

greaterOrEq     >=
```

#### ChangeMaker Using Symbols

```
function USChangeMaker(cents):
    if(cents > 99):
        cents = 99;
    else:
        break
    ;

    let quarters = 0
    let dimes = 0
    let nickels = 0
    let pennies = 0

    loopWhile(cents >= 25):
        quarters += 1
        cents -= 25;

    loopWhile(cents >= 10):
        dimes += 1
        cents -= 10;

    loopWhile(cents >= 5):
        nickels += 1
        cents -= 5;

    loopWhile(cents >= 1):
        pennies += 1
        cents -= 1;

    return quarters + " " + dimes + " " + nickels + " " + pennies;
```

#### ChangeMaker Using String Representation

```
function USChangeMaker(cents):

    if(cents greaterThan 99):
        cents gets 99
    else:
        break
    ;

    let quarters gets 0
    let dimes gets 0
    let nickels gets 0
    let pennies gets 0

    loopWhile(cents greaterOrEq 25):
        1 addedTo quarters
        25 subtractedFrom cents
    ;

    loopWhile(cents greaterOrEq 10):
        1 addedTo dimes
        10 subtractedFrom cents
    ;

    loopWhile(cents greaterOrEq 5):
        1 addedTo nickels
        5 subtractedFrom cents
    ;

    loopWhile(cents greaterOrEq 1):
        1 addedTo pennies
        1 subtractedFrom cents
    ;

    return quarters + " " + dimes + " " + nickels + " " + pennies
;
```

### Static Semantic Errors
Examples of some static semantic errors in 101Script
```

let print = "print"
-- This will create a static semantic error because print is a keyword.

let combo = com + bo
-- Static semantic error because 101Script does not allow concatenation of strings.

function multiply(x):
    x * y
;
-- 101Script will report a static semantic error because y has not been declared yet.

let y = "string"
let x = 5
function multiply():
    x * y
;
-- 101Script will report an error because you cannot multiply a string and an int.

let function print() = function type()
-- Cannot assign two functions to each other without a static semantic error.
```
