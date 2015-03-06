# Clean Code 

## Meaningful Names

* Use intention revealing names. 
* Long names are better than names that don't make sense or acronyms.
* A Comment must not be necessary to understand what a variable does.
* Avoid mental mapping. &#x2192; `l, m, n, k, j, z, p`
* Avoid using `l`(Simple L), `O`(Capital O) as names.
* Don’t encode additional details in names. &#x2192; Hungarian Notation is bad.
* Make meaningful distinctions. &#x2192; Don't misspell to make two names distinct. class vs. klass.
* Number series naming is wrong. &#x2192; Avoid names such as `a1, a2, a3, a4`. (variadic or meaningful names should be used)
* Use searchable names. &#x2192; `MAX_CLASSES_PER_STUDENT` instead of `7`.

## Functions

* A function should be able to read as a TO paragraph. And a set of functions should be read as set of TO paragraphs. (Readable from top to bottom)
    * TO `calculateFibonacci()` we need to do get `N` as input...
* A function should remain at constant level of abstraction. A function shouldn’t deal with both low level and high level stuff.
* Bury the switch statement in an abstract factory. &#x2192; Use polymorphism, and avoid switches.
* Number of arguments to a function, It should be zero (niladic), one (monadic) or two (dyadic). Three (triadic) arguments are OK but should be avoided. (Argument lists are considered as a single argument)
* Instead of using Boolean-s as arguments split the function in two. Avoid flag arguments.
* Don’t have side effects for functions. 
    * `checkPassword()` function should not initialize the session. 
* Avoid output arguments, Pass by reference for the purpose of modification is bad. 
    * `appendFooter(StringBuffer report)` &#x2192; `report.appendFooter()`
* Command query separation. A function can be a command or query but not both.
    * `setAttribute()` should not return an `attribute_exists==True`. 
* Throw Exceptions instead of returning error codes.
* Error Handling is one thing. Functions that handle errors should only do that. They should start with try and end with catch or finally. 
* Functions should be small 3-5(good) - 10-15(max) lines.

## Comments

* Logs in comments are clutter, use a source code control system.
* Avoid redundant comments. 
* Comments doesn't make up for bad code.
* Only use documentation comments if it is in a public API.
* Avoid closing braces comments. Make functions shorter instead.
* Don't comment code. Delete them completely or keep them.
* Don't add markup to comments. Ex: HTML, RST
* Avoid too much information. Ex: History of an algorithm
* Avoid function headers. You don't need a comment if function name already makes sense.
* Don't mark sections of file with banner comments.

## Formatting 

* Use an automated tool for formatting.
* Whole team should agree to a certain formatting practice.
* Put high-level code first in a file. And it should be followed by low level code. Caller should be above the callee.
* Vertical Openness. &#x2192; Separate each concepts.
* Vertical Density. &#x2192; Keep related things closer.
* Vertical Distance. &#x2192; Variables should be declared closer to their usage. Instance variables should be in either top of the class (Java) or the bottom of the class (C++).


##  Objects and Data Structures

* Law of Demeter. &#x2192; Avoid method chaining to access unknown data. A function will know too much. Don't talk to strangers.
* Procedural code makes it harder to add new data structures because all the functions should change. However you can add new functions easily without changing the data structures.
* OO code makes it harder to add new functions because all the classes must change. Easier to add new classes without changing functions.
* Feature Envy. &#x2192; Don't create data structure + object hybrids. Example: Data transfer objects + Business Rule methods.
* An Object exposes behaviour and hides data.
* A data structure exposes data and has no behaviour.

## Error Handling

* Error handling should not obscure logic. &#x2192; High level functions can handle errors thrown by low level functions.
* Raise exceptions instead of returning error codes.
* Do not use checked exceptions. (Checked exceptions violate open/closed principle.)
* Provide context with exceptions.
* Write tests that forces exceptions.
* Special Case Pattern. &#x2192; Encapsulate special cases of business logic in a class. 
* Don't return null. &#x2192; Return a special case object or throw an exception.
* Don't pass null. &#x2192; If you need to pass null to something it is a problem.
* Write try-catch-finally statement first. &#x2192; If you are using TDD write a test that expects exceptions first.

## Boundaries 

* When using third party code instead of depending on their implementations directly, depend on wrapper classes with limited features.
* Learn boundaries through *learning tests*.
* Learning tests can be used to verify newer releases.
* Adapter pattern is useful when dealing with things that doesn't exist.
    * Create an interface, use it. When the API is completed create an *Adapter*.
    * When the API changes only the adapter needs to change. 

## Unit Tests

* Unit Tests should be written with same care as the production code.
    * Easier to change when the production code is refactored or changed.
    * However tests don't need to be as efficient as production code. (Memory efficient, Size efficient...)
* Three Laws of TDD
    * You may not write production code until you have written a failing unit test.
    * You may not write more of unit test than is sufficient to fail, and not compiling is failing.
    * You may not write more of production code that is sufficient to pass current failing test.
* Test a single concept in a single test.
* Test function should have `BUILD-OPERATE-CHECK` sections.
* Create a domain specific testing language based on the assertions you need to make. Example: `assertHtmlEquals()`, `assertResponseIsXml()`
    * Possible to use `GIVEN-WHEN-THEN` approach for naming.
* Use *Template* Pattern to avoid duplication.
* F.I.R.S.T.
    * **F**ast. &#x2192; Fast unit tests can be executed often. Find problems early.
    * **I**ndependent. &#x2192; Test should not depend on each other.
    * **R**epeatable. &#x2192; Tests should be repeatable in any environment.
    * **S**elf-Validating. &#x2192; You should be able to easily identify which tests passed and which failed.
    * **T**imely. &#x2192; Tests should be written in a timely manner. Unit tests should be written just before the production code that makes them fast. 


