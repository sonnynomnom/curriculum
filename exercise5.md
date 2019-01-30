INTERMEDIATE JAVASCRIPT

# Discover More! #

We have learned three important built-in functions: `forEach()`, `map()`, and `filter()`, but what about the other 32?

It is very important for programmers to be able to identify the use cases of the most important iteration methods, but also able to find new ones. In this exercise, we will dig around the array methods documentation.

<br />

**The documentation for the complete list of array methods:**  

[www.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

Take a few minutes and read through all the methods. Make sure to bookmark the page. 

<br />

Suppose we were given the task to sort an array of authors alphabetically:

```javascript
var authors = [ "Tolkien", "Rowling", "Martin"];
```

If we don't know where to start, then the steps would be:

- Find a suitable method
- Understand its syntax / description 
- Test the examples
- (Repeat)

In this case, after scrolling down the left tab for methods, we found the `sort()` method towards the bottom of the list.
Following the link would lead to the syntax, description and examples [page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort). Some testing would reveal that `sort()` would in fact be the perfect candidate:

```javascript
var authors = [ "Tolkien", "Rowling", "Martin"];

authors.sort();

console.log(authors);
```

The output shows that `author` is now sorted:

```javascript
[ 'Martin', 'Rowling', 'Tolkien' ]
```

<br />

> **Definition:** The `sort()` method sorts the elements of an array in place and returns the array.

<br />

## loop4.js ##

```javascript
// "Talk is cheap. Show me the code." - Linus Torvalds, Creator of Linux kernel and Git

var array = [1, 2, 3, 4, 5];

var sum = [];

// 1. Code your answer below:



// 2. Code your answer below:



// 3. Code your answer below:



```

<br />

## Instructions ##

Inside the code editor **loop4.js**, there is a number array called `array`. For this example, let's try to find the sum of the array's numbers by iterating, and there is one catch: you can *not* use `for` loop, `forEach()` method, `map()` method, `filter()` method or `sort()` method! 

**1.** Go back to the Mozilla documentation page and scroll through the 35 methods. Try to find a method that we haven't learned that can solve the problem. Once you think you have found the one, under comment 1, print out the name of the method.

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint 1: Use the <code>console.log()</code> to print out.</p>
    <p>Hint 2: The name of the method might be deceiving so make sure to read through all 35 methods</p>
</details>

<br />

*Solution:* 

```javascript
// 1. Code your answer below:

console.log("reduce()");
```

<br />

**2.** Under comment 2, print out the description of the method you have found, as given on the documenation.

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use the <code>console.log()</code> to print out.</p>
</details>

<br />

*Solution:*

```javascript
// 2. Code your answer below:

console.log("Apply a function against an accumulator and each value of the array (from left-to-right) as to reduce it to a single value.");
```
<br />

**3.** Under comment 3, use the method you have found to reduce (!) `array` down to a single value: the sum of its numbers. When you are finished, print out `sum`. The ouput should look like this:

```javascript
15
```

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use the syntax given in the documentation as a starting point.</p>
</details>

<br />

*Solution:*

```javascript
// 3. Code your answer below:

sum = array.reduce(function(accumulator, current) {
  
    return accumulator + current;
    
});

console.log(sum);
```

<br />

**4.** If you have used the `reduce()` method, you have done your research properly!

<br />

> **Definition:** The `reduce()` method applies a function (comparison function) against an accumulator and each element in the array (from left to right) as to reduce it to a single value.

<br />

To see how this work, let's check out another example. The code below is for combining DNA sequence from groups of three bases to a whole sequence using `for` loop:

```javascript
var DNA = ["AAT", "CGC", "ATA"];

var sequence = "";

for ( var i = 0; i < DNA.length; i++ ) {
  
  sequence += DNA[i];
  
}

console.log(sequence);
```
<br />

The code above is self-explanary; we loop through the `DNA` array and add each of its Strings to the `sequence`. Now let's solve the same problem with the `reduce()` method:

```javascript
sequence = DNA.reduce(function(accumulator, current) { 
  
  return accumulator + current;
  
});

console.log(sequence);
```

<br />

That's it! We have learned how to navigate around the documentation page and also learned two new methods: `sort()` and `reduce()`! Click 'Next' to review the things we learned in this unit.

<br />

#### Community Forums ####
Get help and ask questions on the Codecademy community forums.

[Go to the forums](https://discuss.codecademy.com/c/javascript)

#### Report a Bug ####
If you see a :bug: or any other issue with this page, please report it [here](http://www1.nyc.gov/nyc-resources/categories/environment/animal-control-welfare/index.page).

---

:point_left: **[Back](exercise4.md)**
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 5/7
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
**[Next](exercise6.md)** :point_right:
