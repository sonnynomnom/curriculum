INTERMEDIATE JAVASCRIPT

# Modifying using `map()` #


Often, programmers find themselves needing to take an array and *modify* every element inside the exact same way.

For example: squaring every element in an array of numbers, retrieving the names from a database of users, etc.  

The `forEach()` method from the previous exercise iterates through an array, but it doesn't return anything. Let's learn a built-in method that does: the `map()` method!

<br />

> **Definition:** The `map()`  method calls a function on each element in the array and creates a new array with the results.

<br />

Here we have the `map()` method in action:

```javascript
var array = [1, 2, 3];

var double = array.map(function(number) {

  return number * 2;
  
});

console.log(double);
```

In the code above, we have a number array called `array` and we use the `map()` method to double each of its values. The `double` array is the modified result. So in this case, the output would be:

```javascript
[ 2 , 4,  6 ]
```

<br />

*BACKUP EXAMPLE:*

```javascript
var f = [76, 72, 73, 75, 74, 86, 83];
  
var c = f.map(function(number) {
  
    return Math.round((number - 32) * 5 / 9);
    
}); 

console.log(c);
```

In the code above, we have an array called `f` that contains next week's temperatures in Fahrenheit. To convert the degrees to Celsius, we use the `map()` method to perform the temperature conversion. The `c` array is the modified result. In this case, the output would be:

```javascript
[ 24, 22, 23, 24, 23, 30, 28 ]
```

<br />

## loop2.js ##

```javascript
// =============================
// Welcome to Sonny's Sushi Bar!
// =============================

var menu = [

  {
    'name'  : 'BBQ Eel Bowl',
    'price' : 16.00
  },
 
  {
    'name'  : 'Seaweed Salad',
    'price' : 4.50
  },
 
  {
    'name'  : 'Miso Soup',
    'price' : 2.00
  }
  
];

// 1. Type your code below:

var menuNames = [];

for (var i = 0; i < menu.length; i++) {
 
    menuNames.push(menu[i].name);
 
}



// 2. Type your code below:






// 3. Type your code below:






```

<br />

## Instructions ##

In the code editor **loop2.js**, there is an array named `menu`. Each food is an object, with its `name` and `price` properties. Suppose that we want to create a new array with *just the names* of the food menu. Using a `for` loop, we are able to loop through the `menu` and create a new array called `menuNames` with the help of the `push()` method.

<br />

**1.** Now, on line 33, print out `menuNames`. The output should look like:

```javascript
[ "BBQ Eel Bowl", "Seaweed Salad", "Miso Soup" ]
```

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use <code>console.log()</code> to output.</p>
</details>

<br />

**2.** Under the second comment, let's create a new array with *just the prices* of the food menu. Name the array `menuPrices`. This time, however, use the `forEach()` method instead of the `for` loop. When you are finished, print out the `menuPrices` array. The output should look like:

```javascript
[ 16, 4.5, 2 ]
```

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use the <code>forEach()</code> syntax given last exercise - <code>array.forEach(function(number) {  ...  });</code> as a starting point.</p>
</details>

<br />

**Annoucement: It is now Happy Hour Specials! Food and drinks are ~~10%~~ 20% off!** 

<br />

**3.** Under the third comment, let's create a new array that has the *new prices* of the food menu to reflect the change. Name the array `discountPrices`. This time, however, use the `map()` method and *return* the new array instead of using `push()`. When you are finished, print out the `discountPrices` array. The output should look like:

```javascript
[ 12.8, 3.6, 1.6 ]
```

<details>
    <summary>Stuck? Get a hint</summary>
    <p> <p>
    <p>Hint: Use the <code>map()</code> syntax given earlier - <code>result = array.map(function(number) {  return ...  });</code> as a starting point.</p>
</details>

<br />

**4.** We did it! In this exercise, we were able to get the names, prices and discount prices from the food menu using `for` loop, `forEach()` method and `map()` method.

Take a minute and make sure you understand the similarities & differences between the three.

When you are ready, click 'Next' to continue.

<br />

*Solution:*

```javascript
// 1. Type your code below:

var menuNames = [];

for (var i = 0; i < menu.length; i++) {
 
    menuNames.push(menu[i].name);
 
}

console.log(menuNames);


// 2. Type your code below:

var menuPrices = [];

menu.forEach(function(food) {
  
  menuPrices.push(food.price);
  
});

console.log(menuPrices);


// 3. Type your code below:

var discountPrices = [];

discountPrices = menu.map(function(food) {
  
  return food.price * 0.8;
  
});

console.log(discountPrices);
```

<br />

#### Community Forums ####

Get help and ask questions on the Codecademy community forums.

[Go to the forums](https://discuss.codecademy.com/c/javascript)

#### Report a Bug ####

If you see a :bug: or any other issue with this page, please report it [here](http://www1.nyc.gov/nyc-resources/categories/environment/animal-control-welfare/index.page).

---

:point_left: **[Back](exercise2.md)**
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 3/7
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
**[Next](exercise4.md)** :point_right:
