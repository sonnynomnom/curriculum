INTERMEDIATE JAVASCRIPT

# Basic Iteration: `for` vs. `forEach()` #

Loops are handy and there are numerous ways to loop through an array in JavaScript. The one that we learned in the *Learn JavaScript* course is the good ol' `for` loop.

- To review about **arrays**, click [here](https://www.codecademy.com/courses/learn-javascript/lessons/arrays/exercises/arrays?action=lesson_resume).
- To review about **loops**, click [here](https://www.codecademy.com/courses/learn-javascript/lessons/loops/exercises/loops?action=lesson_resume).

<br />

The code below iterates through an array of numbers and print out each number using `for` loop:

```javascript
var array = [1, 2, 3];

for (var i = 0; i < array.length; i++) {

    console.log(array[i]);

}
```

The output here would be:

```javascript
1
2
3
```

<br />

As of [ES5](https://en.wikipedia.org/wiki/ECMAScript), however, JavaScript supplies a number of vastly powerful techniques for array iteration (_35 to be exact!_).

<details>
    <summary>To learn about ES5: unfold <b>here</b>.</summary>
    <p> <p>
    <p>ECMAScript is the official name for the standardized version of JavaScript. The methods we will learn in this unit were all introduced in the version 5 and they are not supported by Internet Explorer 8 (or older).</p>
</details>

<br />

We will now get accquainted with our very first aforementioned technique: the `forEach()` built-in method; it functions the same way as the `for` loop in the code block above:

```javascript
var array = [1, 2, 3];

array.forEach(function(number) {

    console.log(number);

});
```

<br />

As you can see in the code, `forEach()` method takes a [callback function](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function) as a parameter.

<details>
    <summary>To learn about callback function: unfold <b>here</b>.</summary>
    <p> <p>
    <p>A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some action.</p>
</details>

<br />

> **Definition:** The `forEach()` method loops thorugh an array and applies the same function to every item in it.

<br />

So why use a built-in method like `forEach()` instead of `for` loop? 

- **More readable** - the choice of the method shows the intended purpose of the loop
- **Less trouble / errors** - writing `for` loops can be tiresome and it's easy to make typos
- **Less scope pollution** - each `for` loop will declare a counter (`var`); adding unnecessary values

All these reasons are why functional programming has been making quite a splash in the development world.

Now let's write some code!

<br />

## loop1.js ##

```javascript
var lastJedi = ["kylo", "rey", "finn", "luke"];  

// iterating using for loop

for (var i = 0; i < lastJedi.length; i++) {

    console.log(lastJedi[i]);
    
}
```

<br />

## Instructions ##

**1.** In **loop1.js**, there is an array named `lastJedi` and a `for` loop that prints out each of its values. Run the code to see the ouput. It should look something like this:

```javascript
kylo
rey
finn
luke
```

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Better luck looking through <a href="https://www.snapple.com/real-facts">here</a>.</p>
</details>

<br />

**2.** Change the code in lines 3 - 7 so that it uses the `forEach()` method instead of the `for` loop. The output should stay the same. 

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use the <code>forEach()</code> syntax given earlier - <code>array.forEach(function(number) {  ...  });</code> as a starting point.</p>
</details>

<br />

*Solution:*

```javascript
var lastJedi = ["kylo", "rey", "finn", "luke"];  

// iterating using forEach()

lastJedi.forEach(function(word) {
  
    console.log(word);
  
});
```

<br />

**3.** Awesome! We just used our first built-in method for array iteration: `forEach()`. We will revisit this method again in the next exercise.

Click 'Next' to continue.

<br />

#### Community Forums ####

Get help and ask questions on the Codecademy community forums.

[Go to the forums](https://discuss.codecademy.com/c/javascript)

#### Report a Bug ####

If you see a :bug: or any other issue with this page, please report it [here](http://www1.nyc.gov/nyc-resources/categories/environment/animal-control-welfare/index.page).

---

:point_left: **[Back](README.md)**
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 2/7
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
**[Next](exercise3.md)** :point_right:
