# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of the array (list in some programming languages) data structure? Name some methods of it!
Array can store multiple items in a single variable. Arrays are also useful data structures because they are iterable and mutable.
Methods:
    - append() --> add a single item the the end of the array - arr.append(item)
    - remove() --> remove item from the array - arr.remove(item)
    - insert() --> insert item to the array - arr.insert(item)
    - extend() --> add elements of an array to another array  - arr1.extend(arr2)

#### What are the differences between a list/array and a set?
A set is a collection which is unordered, unchangeable*, and unindexed, doesn't allow duplicate values, and can only contain immutable data types. While list items are ordered, changeable/mutable, allow duplicate values, and can contain any data types.
*can't change the items' value in a set, however can add or remove from a set

#### What are the purpose and some methods of a dictionary/map data structure (simple data objects in JavaScript)?
The dictionary is a mutable data type. Dictionaries are indexed by keys, which can be any immutable type. Strings and numbers can always be keys. Tuples can be used as keys if they contain only strings, numbers or tuples; if a tuple contains any mutable object either directly or indirectly, it cannot be used as a key. A dictionary is a set of key-value pairs, with the requirement that the keys are unique (within one dictionary). The main operations on a dictionary are storing a value with some key and extracting the value given the key. It is also possible to delete a key-value pair with the del statement. If you store a value using a key that is already in use, the old value associated with that key is forgotten

### Algorithms

#### Write a method (or pseudocode) that generates the Fibonacci sequence.
```
var i;
var fib = [0, 1]; // Initialize array!

for (i = 2; i <= 10; i++) {
  // Next fibonacci number = previous + one before previous
  // Translated to JavaScript:
  fib[i] = fib[i - 2] + fib[i - 1];
  console.log(fib[i]);
}
```

#### How do you find a max value in a list/array if you can’t use any built-in functions or methods?
```
function findMax(arr) {
	let max = 0;
	for (let i = 0; i < arr.length; i++) {
		if (arr[i] > max) {
			max = arr[i];
		}
	} return max;
}
console.log(findMax([1, 4, 2, 15, 3]));
```
    
#### How do you find the average of values in a list/array if you can’t use any built-in functions or methods?
```
function average(arr) {
	let sum = 0;
	for (let i = 0; i < arr.length; i++) {
		sum += arr[i]; 
	}
	return sum/arr.length;
}
console.log(average([1, 4, 2, 3]));
```

#### What do we call an in-place sort?
Sorting a list, in-place. Meaning not giving it's sorted outcome to any other variable at all, only modifying the order of the elements within the list.
list.sort()

#### Explain an algorithm which sorts a list!
Bubblesort: The algorithm iterates through the list, the number of times of the list's length. each time it chaecks adjacent elements
and if the next element is lower, it swaps them. This way it sorts the list into ascending order.
```
function bubbleSort(array){
	
    for(var i = 0; i <= array.length-1; i++){
        // Last i elements are already in place
        for(var j = 0; j < ( array.length - i -1); j++){

            // Comparing two adjacent numbers 
            // and see if first is greater than second
            if(array[j] > array[j+1]){

            // Swap them if the condition is true 
            var temp = array[j]
            array[j] = array[j + 1]
            array[j+1] = temp
            }
        }
    }
    // Print the sorted array
    console.log(array);
}

var array = [23, 43, 12, 56, 35];
bubbleSort(array);
Output:
[ 12, 23, 35, 43, 56 ] //sorted array
```
### Programming paradigms - procedural

#### Explain the characteristics of the procedural programming paradigm.
You specify exactly how to do something, not just the desired outcome.
Variables, pointers, and stored procedures are commonplace, and data is often considered mutable variables (changeable).
Inheritance is commonplace and typically used as an example of reusable, clean code that helps future developers.

#### What is the call stack?
The call stack is a stack data structure that stores information about the active subroutines of a program. 
It keeps track of the point to which each active subroutine (or method call) should return control when it finishes executing.
Subroutines may be nested to any level (recursive as a special case), hence the stack structure.

#### What is "stack overflow"?
Stack overflow is an error which occurs when a program attempts to use more space than is available on the call stack.

#### What are the main parts of a function?
function_name(parameter1, parameter2): # function definition name and parameters
    multiply = parameter1 * parameter2 # function body describing the routine
    return multiply # return value

function_name(argument1, argument2) # calling the function with arguments

#### What is the difference between parameters and arguments?
Function parameters are the names listed in the function's definition. Function arguments are the real values passed to the function. Parameters are initialized to the values of the arguments supplied.
```
function add(x, y){
	return x + y
}

add(2, 3)
```
We have introduced x and y here and changed the location of the 2 and 3. x and y are the parameters while 2 and 3 are the arguments here.

### Programming languages - JavaScript

#### What does it mean that a type is immutable? Tell examples.
In JavaScript, primitive values (string, number, bigint, boolean, undefined, symbol, null) are immutable — once a primitive value is created, it cannot be changed, although the variable that holds it may be reassigned another value.
It can be beneficial to use immutable objects for several reasons:
 - To improve performance (no planning for the object's future changes)
 - To reduce memory use (make object references instead of cloning the whole object)
 - Thread-safety (multiple threads can reference the same object without interfering with one other)
 - Lower developer mental burden (the object's state won't change and its behavior is always consistent)
 
 Object.freeze() is a language-level method to make an object immutable in JavaScript.
 
#### What does it mean that an object is mutable? Tell examples.
A mutable value is one that can be changed without creating an entirely new value. In JavaScript, objects and arrays are mutable by default.

#### What is a conditional expression?
A conditional expression, then, is condensed syntax that will return one expression if a particular expression is true, and another if that condition is false. The most basic such expression makes use of the ?: notation. For instance, let’s say that if the tempC (temperature in Celsius) value is below
```
const tempC = 12;
const t1 = (tempC>0)?"hot":"cold";
> t1: "hot"
```
This expression allows you to replace and if/then/else block with a single line of code, assigning the value ‘hot’ to the corresponding t1 variable.
```
const t2 = (tempC  > 30) ? "hot": (tempC >20) ? "warm": (tempC >10) ? "mild": (tempC >0)?"cool":"cold"
> t2: "mild"
```

#### What are different types of arguments?
The arguments object is a local variable available within all non-arrow functions. You can refer to a function's arguments inside that function by using its arguments object. It has entries for each argument the function was called with, with the first entry's index at 0.
Arguments is an Array-like object accessible inside functions that contains the values of the arguments passed to that function.

#### What is variable shadowing?
Variable shadowing occurs when a variable of an inner scope is defined with the same name as a variable in the outer scope. In the inner scope, both variables’ scope overlap. According to variable scoping rules, the inner scope should always be able to access a variable defined in the outer scope, but in practice, shadowing will prevent that from happening.
```
let points = 10;

function displayDouble() {
  let number = 2;
  number = points * number; // variable 'points' is accessible in the inner scope
  console.log(number); //=> 20
}
displayDouble();
```
```
let number = 10;

function displayDouble() {
  //a new variable is defined with the same name as variable on line 1 - outer scope
  let number = 3;
  number *= 2;
  console.log(number); //=> 6
}

displayDouble();
console.log(number); //=> 10
```
In this case, both variables on line 1 and 5 are defined with the same name — number.This has a significant result: the variable defined in the outer scope is ‘shadowed’ by the variable defined in the inner scope. It might be useful to think of ‘variable shadowing’ as a sort of protection mechanism that has two effects:
 - Firstly, it prevents inner scope to access variables defined in the outer scope.
 - Secondly, it prevents inner scope to modify or reassign variables defined in the outer scope.

#### What can happen if you try to delete/add an item from/to a list, while you are iterating over it?
This is the problem with changing a for-loop's count AS it's counting: it loses its place. Removing items can cause the loop to skip elements of the list without meaning to. Adding items may cause the loop to view the same list item more than once. Of course this depends on the index of the item that you're removing, but in general the more you change the list, the more you throw off the loop's count. The problems this creates can be subtle, and therefore difficult to track down.

#### If you need to access the iterator variable after a for loop, how would you do it?
If you need it after a loop, you store it in another variable, INSIDE the foor loop. When it ends you can use the new variable afterwards.

#### What type of elements can a list contain?
Each item in a javascript  list can be of any data type. fe: string, numbers, list, tuple, dict

#### What can the + operator be used for?
To format a string is by using the + operator. This is done by concatenating the string with the variables.
```
let name = "John";
let age = 30;
let food = "pizza";

// String formatting using plus operator
let sentence = name + ' is ' + age + ' years old and likes ' + food;

console.log(sentence); // John is 30 years old and likes pizza
```

#### What is string formatting?
```let name = "John";
let age = 30;
let food = "pizza";
```
 -> backtick:
```
let sentence = `${name} is ${age} years old and likes ${food}`;
```
 -> + operator:
 ```
 let sentence = name + ' is ' + age + ' years old and likes ' + food;
 ```

#### Name 4 iterable types.
strings, arrays, maps and sets.

#### Does the order of the function definitions matter? Why?
It won't change the result of the program. It can help the understanding of a code if it's ordered well. The calling of the functions is what matters.

#### What is spread/rest syntax for?
Spread syntax (...) allows an iterable, such as an array or string, to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected. In an object literal, the spread syntax enumerates the properties of an object and adds the key-value pairs to the object being created.
Spread syntax looks exactly like rest syntax. In a way, spread syntax is the opposite of rest syntax. Spread syntax "expands" an array into its elements, while rest syntax collects multiple elements and "condenses" them into a single element.
```
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
// expected output: 6

console.log(sum.apply(null, numbers));
// expected output: 6
```
#### What does a destructuring assignment mean?
Destructuring Assignment is a JavaScript expression that allows to unpack values from arrays, or properties from objects, into distinct variables data can be extracted from arrays, objects, nested objects and assigning to variables. In Destructuring Assignment on the left-hand side defined that which value should be unpacked from the sourced variable. In general way implementation of the extraction of the array is as shown below: Example: 
```
var names = ["alpha", "beta", "gamma", "delta"];
 
var firstName = names[0];
var secondName = names[1];
 
console.log(firstName);//"alpha"
console.log(secondName);//"beta"
```
```
[x, y, ...restof] = [10, 20, 30, 40, 50];
console.log(x); // 10
console.log(y); // 20
console.log(restof); // [30, 40, 50]
```

#### What happens when you try to assign the result of a function which has no return statement to a variable?
When a function has no return value;, it returns undefined. There's generally no need to use such a return result. When you declare a variable by having a var a statement in a block, but haven't yet assigned a value to it, it is undefined.

1. When you call a function with fewer arguments than the arguments list in the function statement lists, the unpassed arguments are set to undefined. You can test for that with eg.:
```
function dosomething(arg1, arg2) {
    if (arg2===undefined)
    arg2= DEFAULT_VALUE_FOR_ARG2;
    ...
}
```
With this method you can't tell the difference between dosomething(1) and dosomething(1, undefined); arg2 will be the same value in both. If you need to tell the difference you can look at arguments.length, but doing optional arguments like that isn't generally very readable.
2. When a function has no return value;, it returns undefined. There's generally no need to use such a return result.
3. When you declare a variable by having a var a statement in a block, but haven't yet assigned a value to it, it is undefined. Again, you shouldn't really ever need to rely on that.

## Software engineering

### Debugging

#### What techniques can you use while debugging a program?
print
debugger
rubberduck

#### What does step over, step into and step out mean when using the debugger?
step over: skip functions
step into: by default the debugger skips over managed properties and fields, but the Step Into Specific command allows you to override this behavior.
step out: to step out the specific

#### How can you start to debug a program from a certain line using the debugger?
1. Create breakpoint on desired line (with red dot)
2. Run the debugger

### Version control

#### What are the advantages of using a version control system?
1. Collaboration
2. Storing versions (Properly)
3. Restoring previous versions
4. Understanding what happened (commits)
5. Backup

#### What is the difference between the working directory, the staging area and the repository in git?
working directory: the directory where you are working on your computer (which is checked by git if the repository is created)
staging area: where the added changes can be checked before they are commited (they can be still deleted from staging)
git repository: storage of commited changes, which can be restored or merged later if needed (can be pushed to github)
![image](https://user-images.githubusercontent.com/113178205/200187799-c2d2b82f-5b8e-4bc1-a56a-bfacbff6352f.png)

#### What are remote repositories in git?
The remote repository is an online storage of the git repositories. 
It can be used to share code with colleagues by git push/pull commands and to manage multiple branches and merges between the versions. 

#### Why does a merge conflict occur?
A conflict arises when two separate branches have made edits to the same line in a file, or when a file has been deleted in one branch but edited in the other.

#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
git add - add file to staging
git commit - create a commit with a message and add it to the local repo
git push - push the changes to the remote repository (github

#### What does it mean atomic commits and descriptive commit messages?
Atomic commit means every commit pertains to one fix or feature.
Descriptive commit means the purpose of the commit is clear from commit messages and description.

#### What’s the difference between Git and GitHub?
Git is a distributed **version control tool** that can manage a development project's source code history, while GitHub is a **cloud based platform** built around the Git tool.

## Software design

### Clean code

#### What does clean code mean?
Code is clean if it can be understood easily, understandability comes readability, changeability, extensibility and maintainability.
No duplications, no dead code, meaningful variable names, proper indentation, functional structure and no magic numbers.

#### What steps do we usually do during a clean code refactoring?
1. Fix bad naming
2. Fix badly formatted code
3. Clear repetitive code
4. Refactor long methods
5. Fix wrong comment usage
6. Delete dead code

### Error handling

#### What is error/exception handling?
An exception is an error that happens during execution of a program. When that error occurs, Javascript generate an exception that can be handled, which avoids your program to crash.
An exception signifies the presence of an abnormal condition which requires special operable techniques. In programming terms, an exception is the anomalous code that breaks the normal flow of the code.

While coding, there can be three types of errors in the code:
 - Syntax Error: When a user makes a mistake in the pre-defined syntax of a programming language, a syntax error may appear.
 - Runtime Error: When an error occurs during the execution of the program, such an error is known as Runtime error. The codes which create runtime errors are known as Exceptions. Thus, exception handlers are used for handling runtime errors.
 - Logical Error: An error which occurs when there is any logical mistake in the program that may not produce the desired output, and may terminate abnormally. Such an error is known as Logical error.

#### What are the basics of exception handling in JavaScript?
The try...catch...finally statements combo handles errors without stopping JavaScript.
The try statement defines the code block to run (to try).
The catch statement defines a code block to handle any error.
The finally statement defines a code block to run regardless of the result.
The throw statement defines a custom error.
Both catch and finally are optional, but you must use one of them.


#### In which case should we catch an exception? Why?
Exceptions are convenient in many ways for handling errors and special conditions in a program. When you think that you have a code which can produce an error then you can use exception handling.

#### What can/should we do with an exception in the `catch` block?
- printing the problem in an elegant way
- quit the program if need it
- The catch statement defines a code block to handle any error

#### What does the `finally` statement do in a `try-catch` block in JavaScript?
The try...catch...finally statements combo handles errors without stopping JavaScript.
The finally statement defines a code block to run regardless of the result.

```
Syntax
try {
  tryCode - Code block to run
}
catch(err) {
  catchCode - Code block to handle errors
}
finally {
  finallyCode - Code block to be executed regardless of the try result
}
```
```
<p>Please input a number between 5 and 10:</p>

<input id="demo" type="text">
<button type="button" onclick="myFunction()">Test Input</button>
<p id="message"></p>
<script>
function myFunction()
  const message = document.getElementById("message");
  message.innerHTML = "";
  let x = document.getElementById("demo").value;
  try {
    if(x == "") throw "Empty";
    if(isNaN(x)) throw "Not a number";
    if(x > 10) throw "Too high";
    if(x < 5) throw "Too low";
  }
  catch(err) {
    message.innerHTML = "Error: " + err + ".";
  }
  finally {
    document.getElementById("demo").value = "";
  }
}
</script>
```
