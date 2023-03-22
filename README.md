# workshop
Workshop code for Pair Programming and TDD

Here are some instructions for a workshop on pair programming and TDD.

The skeleton of the tests are in the [index.html](index.html) file. To run the tests, simply open [index.html](index.html) in the browser of your choosing.

The tests use the [jasmine framework](https://jasmine.github.io/). This is because it offers the simple in browser setup. 

Please use the [jasmine documentation](https://jasmine.github.io/pages/docs_home.html) to further the tests when workshopping.

## 1. Finish the development of the Square class. 
You don't need to follow these instructions to the point. The important thing is that you code, in a pair, using TDD.
- Complete the Square class
  - Make the `area` property actually return the area
  - Throw and error when the Square is created without a side length
  - Add a property `perimeter` that calculates the total length of all sides
  - Allow changing the side length by setting the `area` and the `perimeter` 

```js
const square = new Square(2);
square.area = 25;
```
## 2. Continue with other geometric shapes or skip to point 3
- Create a Circle class with `area` and `perimeter` 
- Create a Rectangle class with `area` and `perimeter`
  - Use the Rectangle class to implement the Square class in point 1
- Create a Triangle class with `area` and `perimeter`
  - Maybe use Heron's formula?

## 3. Create a [FizzBuzz counter](https://en.wikipedia.org/wiki/Fizz_buzz)
FizzBuzz is a game where you count from 1 to 100 and say "Fizz", "Buzz", "FizzBuzz" or the number given a certain rules.
- Say "Fizz" when the number is dividable by 3
- Say "Buzz" when the number is dividable by 5
- Say "FizzBuzz" when the number is dividable by both 3 and 5
- Say the number when the number isn't dividable by neither 3 nor 5