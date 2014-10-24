JavaScript
-----------------

**What is JavaScript (JS) used for?**
  
- make websites respond to user interaction  
- build apps and games  
- access information on the internet  
- organize and present data


## Getting started with programming  

**EXAMPLE**  

```
	confirm('This is an example of using JS to create some interaction on a website. Click OK to continue!')
```

Makes a box in the browser with OK/Cancel buttons.  

Ask for input with `prompt`  

```
	prompt('ask a question')
```

User can then give text based input.  

### Data types  

1. *Numbers* are quantities
2. *Strings* are sequences of characters     
	- requires quotes  
3. *Booleans* are either true or false  

### Console.log  

`console.log()` will take whatever is within the parentheses and log it to the console. This is commonly called **printing out**  

**NOTE** With comparison operators *equal to* is **3** equal signs, `===` and not equal to is `!==`

### If Statements  

An `if` statement is made of the `if` keyword, a condition in parentheses and a pair of curly braces `{}`. If the condition is true then the code in the braces will run.  

	```
	if (condition)  
	{
		run.this.code
	}
	else
	{
		run.this.code
	}
	```

Adding an `else` tells what code to run if the condition is false.

### Math  

Math works in JS the same as elsewhere.  

The **modulo** is the symbol `%` and when placed between two numbers will divide the first number by the second and return the remainder. 

This can be useful with if/else statements as a condition. 

### Substrings

You can get part of a string with the `.substring(x,y)` command. Here `x` is where you start chopping and `y` is where you stop. Counting starts from 0. 

**EXAMPLE** 

``` 
// To get the 4th up to the 7th letter of the string "wonderful day" 

"wonderful day".substring(3,7)
```

### Variables  

Create a variable by assigning some value to a name;

```
var varName = data
```
Note `var` is the command that tells the computer to assign the data to varName. But it seems that this is not actually needed to assign a variable. 

Use the variable name to replace the value;

```
var varName = data

console.log(varName.length) === console.log(data.length)
```

To reassign a value to a variable;

```
// On line 2, declare a variable myName and give it your name.
var myName = "jonny"
// On line 4, use console.log to print out the myName variable.
console.log(myName)
// On line 7, change the value of myName to be just the first 2 
// letters of your name.
myName = myName.substring(0,2)
// On line 9, use console.log to print out the myName variable.
console.log(myName)
```

## Choose Your Own Adventure  
```
// Check if the user is ready to play!

confirm("Are you ready to get started?")

// Check if user is older than 13
var age = prompt("What's your age?")

if(age < 13)
{
    console.log("You can play, but we take no responsibility for you")
}
else
{
    console.log("Let's get going!")
}

console.log("You are at a Justin Bieber concert, and you hear this lyric 'Lace my shoes off, start racing.'")

console.log("Suddenly, Bieber stops and says, 'Who wants to race me?'")

var userAnswer = prompt("Do you want to race Bieber on stage?")

if(userAnswer === "yes")
{
    console.log("You and Bieber start racing. It's neck and neck! You win by a shoelace!")
}
else
{
    console.log("Oh no! Bieber shakes his head and sings 'I set a pace, so I can race without pacing.'")
}

var feedback = prompt("Please rate this game from 1 to 10")

if(feedback > 8)
{
    console.log("Thank you! We should race at the next concert!")
}
else
{
    console.log("I'll keep practicing coding and racing.")
}
```

## Introduction to Functions in JS

```
// This is what a function looks like:

var divideByThree = function (number) {
    var val = number / 3;
    console.log(val);
};
```

First declare a function with `var`, give it a name (convention is to use *lowerCamelCase*) then use the `function` keyword to tell the computer that you are making a function. The code in parentheses is the parameter, a placeholder word we give a specific value when we call the function. The block of code is written between braces, `{}`, and every line of code within this block must end with a semicolon,`;`, and a semicolon must be placed after the closing brace.  

e.g., 

```

var foodDemand = function(food){
    console.log("I want to eat" + " " + food);
}

foodDemand("pickles")

```

Good and bad examples:

```
// Nicely written function:
var calculate = function (number) {
    var val = number * 10;
    console.log(val);
};

// Badly written function with syntax errors!

greeting var func{name}(console.log(name)))} 
```

When we want to return a value from the function, we can use the `return` keyword;

```
// Parameter is a number, and we do math with that parameter
var timesTwo = function(number) {
    return number * 2;
};
```

Functions can have more than one parameter to create increased utility 

### Global vs Local variables  

A **global** variable is defined outside a function. These are accessible anywhere once they have been declared. 

Variables defined *inside* a function are **local** variables, they cannot be accessed outside of that function.  

The `var` keyword defines variables in the current scope (local if called within a function, global if outside). If a variable is assigned without the var keyword it will have global scope, such that a variable defined inside a function without var will be accessible from outside the function.  




