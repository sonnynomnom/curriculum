INTERMEDIATE JAVASCRIPT

# The Water `filter()` #

Next up on the list of powerful built-in methods: `filter()`! Yep, `filter()` does exactly what it sounds like: it takes in an array and filters out unwanted elements. It allows you to create a subset of data that meets a certain criteria.

<br />

> **Definition:** The `filter()` method iterates through an array and returns a new array of elements that returned [`truthy`](https://developer.mozilla.org/en-US/docs/Glossary/Truthy) from the callback function.

<br />

<details>
    <summary>To learn about truthy: unfold <b>here</b>.</summary>
    <p> <p>
    <p>In JavaScript, a truthy value is a value that is considered true when evaluated in a Boolean context.</p>
</details>

<br />

In the code below, we are looping through the `year` array using the `filter()` method and returning a new array called `superSenior` that only contains numbers greater than 4.

```javascript
var year = [1, 2, 3, 4, 5, 6];

var superSenior = year.filter(function(number) {

  return number > 4;

});

console.log(superSenior);
```

The output in this case would be:

```javascript
[ 5, 6 ]
```

<br />

*BACKUP EXAMPLE*

In the code below, we have a `frequency` array with five different frequencies in Hz. We then have a :microphone: filter where the cutoff frequency is set at 120 Hz. The cutoff is where the filter begins to eliminate lower frequencies.

```javascript
var frequency = [808, 120, 78, 909, 3750];

var micFilter = frequency.filter(function(number) {

  return number > 120;

});

console.log(micFilter);
```

The output in this case would be:

```javascript
[ 808, 909, 3750 ];
```

<br />

## loop3.js ##

```javascript
var water = ["lead", "copper", "chlorine", "pesticides", "minerals"];  

// 1. Write your code below:



// 2. Write your code below:



```

<br />

## Instructions ##

**1.** Inside the code editor **loop3.js**, we have an array called `water` with five different items. Starting on line 4 and under the first comment, iterate through the array with a `filter()` method and return a new array called `metals` that only has words with length less than 7. Then, print out the `metals` array.

The output should look like:

```javascript
[ 'lead', 'copper' ]
```

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use the <code>filter()</code> syntax given above - <code>result = array.filter(function(number) {  return ...  });</code> as a starting point.</p>
</details>

<br />

**2.** Next, under the second comment, loop through the `water` array again using the `filter()` method and return a new array called `bad` that has everything but "minerals". Then, print out the `bad` array.

The output should look like:

```javascript
[ 'lead', 'copper', 'chlorine', 'pesticides' ]
```

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use the <code>filter()</code> syntax given above - <code>result = array.filter(function(element) {  return ...  });</code> as a starting point.</p>
</details>

<br />

**3.** Pat yourself in the back. Besides the `for` loop, you now know three additionals ways to iterate / manipulate an array:

- `forEach()` method
- `map()` method
- `filter()` method

Let's learn how to discover more methods. Click 'Next' to continue.

<br />

*Solution*:

```javascript
var water = ["lead", "copper", "chlorine", "pesticides", "minerals"];  

// 1. Write your code below:

var metals = water.filter(function(word) {
  
  return word.length < 7;
  
});

console.log(metals);

// 2. Write your code below:

var bad = water.filter(function(word) {
  
  return word != "minerals";
  
});

console.log(bad);
```

<br />


#### Community Forums ####
Get help and ask questions on the Codecademy community forums.

[Go to the forums](https://discuss.codecademy.com/c/javascript)

#### Report a Bug ####
If you see a :bug: or any other issue with this page, please report it [here](http://www1.nyc.gov/nyc-resources/categories/environment/animal-control-welfare/index.page).

---

:point_left: **[Back](exercise3.md)**
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 4/7
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
**[Next](exercise5.md)** :point_right:
