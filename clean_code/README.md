# Clean Code 

## Meaningful Names

* Use intention revealing names. 
* Long names are better than names that don't make sense or acronyms.
* A Comment must not be necessary to understand what a variable does.
* Avoid mental mapping. &#x2192; l, m, n, k, j, z, p
* Don’t encode additional details in names. &#x2192; Hungarian Notation is bad.
* Make meaningful distinctions. &#x2192; Don't misspell to make two names distinct. class vs. klass.
* Number series naming is wrong. &#x2192; Avoid names such as a1, a2, a3, a4. (variadic or meaningful names should be used)
* Use searchable names. &#x2192; MAX_CLASSES_PER_STUDENT instead of 7.

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


