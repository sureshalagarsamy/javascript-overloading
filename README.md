### What is function overloading in JavaScript?

There is no real function overloading in JavaScript and it allows to pass any number of parameters of any type.

You have to check inside the function how many arguments have been passed and what is the type arguments using typeof.

> How to create function overloading in JavaScript?

The example for ```function overloading not supporting``` in JavaScript as ```given below```.

```javascript
function sum(a, b) {
    alert(a + b);
}

function sum(c) {
    alert(c);
}

sum(3);		// The output is 3.
sum(2, 4);	// The output is 2 only.
```
In the JavaScript, when we write more than one functions with same name that time JavaScript consider the last define function and override the previous functions. You can see the above example output for the same.

We can achieve using the several different techniques as give below.

* You can check the declared argument name value is undefined.
* We can check the total arguments with arguments.length.
* Checking the type of passing arguments.
* Using number of arguments
* Using optional arguments like x=x || 'default'
* Using different name in the first place
* We can use the arguments array to access any given argument by using arguments[i]

### Solution

```javascript
function sum() {
   if (arguments.length==1) {
	return sum(arguments[0]);
   } else if (arguments.length==2){
	return funcTwo(arguments[0],  arguments[1]);
   }
}
function funcTwo(a,b) {
   alert(a+b);
}
function sum(c) {
   alert(c);
}
```

But better to use different functions unless if you don't feel any difficulties on the above solution.
