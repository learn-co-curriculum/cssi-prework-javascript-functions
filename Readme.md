# JavaScript Functions

##Objectives
* Declare a Function in JavaScript
* Invoke (or use) a JavaScript Function
* Understand the difference between Parameters and Arguments in Functions
* Understand the purpose and use of return values

## Overview
A function holds a set of actions that will run every time the function is called. This helps control the flow of our program and allows us to repeat a set of actions multiple times.

Writing functions lets us package code into blocks that we can reuse. This will prevent us from writing the same code over and over again. Understanding and using functions is one of the most important skills for a developer.

Imagine you are a cashier. Every time a customer checks out, you need to

1. Add the price of all the items
2. Apply any coupons
3. Print out the total

If you were using the JavaScript console, this set of actions might look like:
```
> 33 + 19 // add the prices of the items
52
> 52 * .15 // find the value of the 15% off coupon
7.8
> 52 - 7.8 // subtract the coupon from the price
44.2
```
That process takes time, and if you do it hundreds of times each day, you are bound to make some mistakes. Instead, we can write a function that will do all the work for us:

```
function checkout(item1, item2, coupon){
  var subtotal = item1 + item2;
  var total = subtotal - subtotal*coupon;
  console.log(total);
};
```
And then we can use the function by calling it like this:
```
> checkout(33,19,.15)
44.2
> checkout(12,9.99,.05)
20.89
```


##Function Declaration
A function is a set of instructions that we write out once and can reuse over and over. We call creating a new set of instructions **declaring a function**.

The syntax for writing JS functions is very specific. It looks like this:

```
function name() {
    // instructions here
};
```
The steps you want executed go inside the curly braces.

```
function goGetLunch() {
    console.log("Close Computer");
    console.log("Stand up");
    console.log("Walk out the door")
};
```

## Invoking a Function
Declaring a function is only the first step. In order for JavaScript to actually use the function, it has to be invoked. There are many ways to invoke a function in JavaScript, but in the scope of this prework, we will mainly stick with function calls. To call a function, you just need to write the function name followed by parenthesis.  When a function is called, all of the code between the curly brackets of that function is executed.
```
goGetLunch();
```

##Parameters & Arguments
Parameters allow you to pass values into functions - they help make functions reusable. Instead of using the same values every time you use the function, you can use the same set of instructions on different data.
```
function goGetLunch(student) {
  console.log('hey, ' + student);
  console.log('close your computer');
  console.log('stand up');
  console.log('walk out the door');
}
```
Then we can call it like this:
```
goGetLunch("Joe");
goGetLunch("Jill");
goGetLunch("Josie");
```
When you call a function with a name like "Joe", those values are called arguments. We can reuse this function, and change the name of the student we address by adding a different student argument.

To reiterate
* Parameter - the value in the function definition - `student` .
* Argument- the value in the function call - ``"Joe"``, ``"Jill"``, ``"Josie"``.


## Return Values
In order to use a value outside of the function - that is, if you want to use the output of your function - you need to **return** that value.
```
function addTwice(x,y){
    return x+x+y+y;
}
```
By using a return statement, we’re asking the function to give us back the answer.

```
> var y = addTwice(3,5);
> console.log(y)
16
```

##N.I.C.O
We can break down the creation of functions into four things that every function has:
+ **Name** - Decide an appropriate name for the function. In JavaScript, these names are camelCased.
+ **Input (Parameters)**  - Figure out which inputs, if any, are needed to accomplish what the name describes.
+ **Code** - Write instructions inside of the curly brackets to be run when it is called.
+ **Output** - Optionally return a value if needed.
