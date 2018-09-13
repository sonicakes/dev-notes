# Slides for my TDD with RSPEC talk

## slide 1
Hi everyone, my name is Sonia, and I have recently graduated from GA WDI. This is my first technical talk, so apologies for potential slips and falls. This talk is aimed at beginners in Ruby and RSPEC, and serves as an introduction to a wider topic of Testing Software.

## slide 2
### About Me

Moved to Sydney from Russia
Past: International Economics and Linguistics
Taught myself to code via freeCodeCamp
Currently: BA of Digital Design at Curtin University
WDi-28 at General Assembly, Sydney
Anime, Languages and Sci-Fi books

## slide 3
### What is Testing?

 Software testing is used to gain valuable information about a program's quality and can be used to uncover problems.
 In my own words, testing is writing code and running it in your local environment to make sure the code does what is supposed to do, but it doesn't get executed in production.

## slide 4
### Types of Testing

1. Unit testing
Unit testing involves breaking your program into pieces, and subjecting each piece to a series of tests.

Example in Ruby/Rails: password field should not be empty for User model

2. Functional Testing


Functional testing is a type of testing which verifies that each function of the software application operates in conformance with the requirement specification.
- Mainline functions:  Testing the main functions of an application
- Basic Usability: It involves basic usability testing of the system. It checks whether an user can freely navigate through the screens without any difficulties.
- Accessibility:  Checks the accessibility of the system for the user
- Error Conditions: Usage of testing techniques to check for error conditions.  It checks whether suitable error messages are displayed.

Example in Ruby/Rails: check that appropriate flash message is displayed if the booking could not be processed

 3. Integration Testing

 is a software development process which program units are combined and tested as groups in multiple ways. Checks interaction between units.

 Example in ruby/rails: acceptance test framework Capybara (used with Minitest) checks for integration tests. e.g. multiple units together.

## Slide 5
### What is TDD?
Approach to development which combines test-first development where you write a test before you write just enough production code to fulfill that test and refactoring. Explain the chart

## Slide 6
Why TDD?
- thinking before doing: what do we want from code?
- fast feedback
- cleaner, simplified code
- no pseudocode: tests provide detailed specificaiton
- less debugging

## Slide 7
### Testing with RSPEC
- DSL testing tool for Ruby
- Behaviour-Driven Framework (incl. TDD, Domain-Driven Design, Object Oriented Design)
- Mocking Framework (dummy objects)
- Simplicity in Syntax

## Slide 8
### My journey with TDD

- Was aware of Testing for JS (Mocha, Jasmine), but was a bit scared to tackle it
- Writing test statements (example from MTA console logs) - like to test code in different scenarios before write more code for it
- RSPEC was introduced during GA
- Decided to explore it and use if for my final project

## Slide 9
### Overview of final project

- Unit and functional testing
- Test coverage
- Example of the screenshots
This slide talks about Unit tests example

## Slide 10
### Overview - p2, Functional
Ran out of time - 1 week only for the project

## Slide 11
### Overview - p3, simplecov
Test coverage

## SLide 12
### Demo
The great thing about TDD is it works very well with dealing with customer requirements.
Example here demonstrates e-commerce customer.
We’ll be testing the shopping cart and models (unit tests)

## Slide 13
### demo
E.g. we have a following requirement from the customer:
Example is online bookstore, some books have pricing and some are free(e.g. free tourist maps)
You can only order 1 copy of each free map. If you order more than 5 paid books with prices, then you get free shipping. Otherwise, shipping will always cost $20.

## Slide 14
### demo
Converting those business rules we know that we require Shopping Cart model, doing all the business logic about price and shipping etc.
A basic Product Model, which will just have a name and price.
Now we can open RSPEC file and describe what we think the operation should be without writing test code or application code.

## Slide 15
### demo
writing tests in rspec and they all show as pending

## Slide 16
### demo
Now writing expectations for my specified conditions

## Slide 17
### demo
All 4 tests fail since there is no class of 'Shopping Cart'

## slide 18
### demo
So I create the class, with the functions empty and re-run my tests
Still fails, but now the error messages make more sense
This makes sense.
The function returns nil (because it doesn’t do anything)
But we expect zero.

So we need this function to loop over the products
property and return the sum of the product quantity

## slide 19
### demo
writing a method that checks product quantity, test passes!

## slide 20
### How testing changed my attitude to code:

- Failure is not the end of the world: its a part of success!
- Errors mean something is happening and there is room for improvement!!
- Makes you think about code in a deeper way (engineering mindset)

## slide 21
### Resources

## slide 22
## Thankyous
