# Clean Code 

## Meaningful Names

## Functions

* A function should be able to read as a TO paragraph. And a set of functions should be read as set of TO paragraphs. (Readable from top to bottom)
    * TO `calculateFibonacci()` we need to do get `N` as input...
* A function should remain at constant level of abstraction. A function shouldn’t deal with both low level and high level stuff.
* Bury the switch statement in an abstract factory. (Use polymorphism, and avoid switches).
* Number of arguments to a function, It should be zero (niladic), one (monadic) or two (dyadic). Three (triadic) arguments are OK but should be avoided. (Argument lists are considered as a single argument)
* Instead of using Boolean-s as arguments split the function in two. Avoid flag arguments.
* Don’t have side effects for functions. 
    * checkPassword() function should not initialize the session. 
* Avoid output arguments, Pass by reference for the purpose of modification is bad. 
    * `appendFooter(StringBuffer report)?report.appendFooter()`
* Command query separation. A function can be a command or query but not both.
    * `setAttribute()` should not return an `attribute_exists==True`. 
* Throw Exceptions instead of returning error codes.
* Error Handling is one thing. Functions that handle errors should only do that. They should start with try and end with catch or finally. 
* Functions should be small 3-5(good) - 10-15(max) lines.
