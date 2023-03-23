# Workshop
> Here are some instructions for a workshop on pair programming and TDD.

The skeleton of the tests are in the [index.html](index.html) file. To run the tests, simply open [index.html](index.html) in the browser of your choosing.

The tests use [the jasmine framework](https://jasmine.github.io/). This is because it offers the simple in browser setup. 

Please use [the jasmine documentation](https://jasmine.github.io/pages/docs_home.html) to further the tests when workshopping.
Most of what is needed for this workshop can be found in [the jasmine API documentation](https://jasmine.github.io/api/4.6/global). 
When asserting actual and expected values you should use [the matchers in the jasmine API documentation](https://jasmine.github.io/api/4.6/matchers.html).  

You don't need to follow these instructions to the point. The important thing is that you code, in a pair, using TDD.

## 1. Finish the development of the Square class. 
- Complete the Square class
  - Make the `area` property actually return the area
  - Throw and error when the Square is created without a side length
  - Add a property `perimeter` that calculates the total length of all sides
  - Allow changing the side length by setting the `area` and the `perimeter` 

```js
const square = new Square(2);
square.area = 25;
```
## 2. Continue with other geometric shapes or skip to [point 3](#3-create-a-fizzbuzz-counter)
- Create a Circle class with `area` and `perimeter` 
- Create a Rectangle class with `area` and `perimeter`
  - Use the Rectangle class to implement the Square class in [point 1](#1-finish-the-development-of-the-square-class)
- Create a Triangle class with `area` and `perimeter`
  - Maybe use Heron's formula?

## 3. Create a [FizzBuzz counter](https://en.wikipedia.org/wiki/Fizz_buzz)
FizzBuzz is a game where you count from 1 to 100 and say "Fizz", "Buzz", "FizzBuzz" or the number given a certain rules.
- Say "Fizz" when the number is dividable by 3
- Say "Buzz" when the number is dividable by 5
- Say "FizzBuzz" when the number is dividable by both 3 and 5
- Say the number when the number isn't dividable by neither 3 nor 5


---


# Additional material 

## Principles for productive pairing 

### Programming is a team sport 
This is the main principle that we apply to our work. Pairing isn't about taking turns writing code, it's about two engineers building the best software they can together. Everything gets better when we work as a team. Every part of our process stems from this principle.  

### Express yourself 
We're not mind readers. When you've got control of the keyboard, it's a good idea to vocalise your thought process so that your pair knows the direction you're taking and can provide useful feedback. 

### Give each other time
Too much interference from the off-keyboard pair can make it hard for you to make progress. Don't jump in with small corrections straight away. Instead focus on the bigger picture.

### Sit comfortably
The developer using the keyboard should be sitting with a comfortable stance. Just because we're pairing doesn't mean we should sacrifice our wellbeing. Make sure you can both see the code and don't start pairing if you're not comfortable. 

### Don't be defined by ping pong pairing
The ping pong technique is a great way to even out keyboard time, but it's nothing more than that. It's not the case that one person writes the test and one person makes it pass; you're both writing the test and you're both implementing the solution together. Ping pong just helps you decide who's driving the keyboard. Don't make a big deal of 'handing over' control when you move from test to implementation. There shouldn't be anything to hand over; the implementation is a continuation of the work you started when you wrote the test.

### It's not a competition
You're not being tested. You don't need to show that you're 'better' than your pair. We value humility and honesty. This is a team sport; work together, not in competition. 

### Take breaks 
Pairing is an intensive exercise and can easily lead to exhaustion. Use a timer to prevent extended pairing sessions. 25 minutes is a good limit. 

### Don't go solo without asking 
Sometimes it's necessary to split up. Meetings cause pairs to break apart temporarily. When this happens decide how you want to proceed together. The solo developer can either keep working or pick up something else, but agree it together. Don't go rogue. Creating a bucket of small independent tasks makes it easier for a solo developer to pick something up and remain productive. 

### Communication is key
Talk about the process. Don't go quiet on your pair. Short feedback loops are better than long ones, so talk about pairing. If something's not working, speak up. If you're stuck, ask for help. If you need a break, let your pair know.

### Pairing by default 
Most of our work is better done as a pair, but we understand there are exceptions. Writing documentation for a service is one such exception. It works better alone with a review afterwards.  

### One computer
You should only be working on one computer at a time. If you bring your own laptop to a pairing session you're not pairing; you're just working next to each other.

### Focus without disruptions 
Close any apps that might interrupt you and break your focus. The notifications from incoming email or received chat messages are good to have if there is anything urgent for you to act upon but most of the time they will only steal your focus from the task at hand. Close email and chat clients if they are not part of what you are working on. 

## Principles for TDD

### Don't do to much
Part of what makes TDD special is that you let the tests decide how you implement your code. That also means that you should only focus on getting the test to pass, and not on getting the function work as _you_ expect.

### Description is key
A good description means that you know what you are aiming for when implementing the test. The description is also part of the output when running the test, so it helps give an overview, and it also helps to give you an quick understanding of why a test has failed.

### Test often
The feedback loop is a big benefit in testing. The smaller it is, the quicker you are.

### One at a time
Only work with one failing test at a time. It might be good to write a couple of descriptions to get an plan of what tests are coming up, but only ever work on one failing test at one time. This ensures focus and clarity with the task at hand. The other tests are still there to cover you should you somehow break functionality. Remember that you can choose to run only one test.

### Isolated tests
Write tests that are independent of one another. Each test case should be independent of other tests, so that the results of one test does not affect the results of another.

### Test the functionality, not the implementation
A brittle test is a test that fails when refactoring. This means that there is a connection to the implementation. Typically, you should give input and assert the output. 

### Test your own code, not others (Unit test, at least)
When using an external API in you code always make it return an expected result by using stubs, spies or mocks. Stubs, spies and mocks are important tools when testing. They allow you to test your own code with known parameters. It's not our job to test others code and it is important to keep your tests running even if the API isn't available.

### Refactor when it has value
In certain cases it might not make sense for you to do any refactoring. But remember to always evaluate if it is worth refactoring.

