# javascript

JavaScript programming guidelines will help you to deliver error free code and it follows on the Google JavaScript guideline documentation.



File Name:
The file name must be all lower case. It may include dashes(-) or underscores(_) but no other punctuation allowed. 
File encoding type must be UTF-8.
Package Name:
Package names are all lowerCamelCase.
example: com.nodeSimplified.exampleCode.
Class Name:
Class names, interface names, typedef, and record names are all UpperCamelCase.
These names are always nouns or noun phrases.
example: ImmutableList.
Method Name:
Method names must be lowerCamelCase.
The private Method name must end with a trailing underscore.
These names are typically verbs or verb phrases.
example: sendMessage().
Enum Name:
Enum names should be written in UpperCamelCase.
These names are typically singular nouns.
Constant Name:
Constant names should be all Upper case, separated by underscores.
example: CONSTANT_NAME.
Non-constant Name:
Non-constant field names (static) should be written in lowerCamelCase and private variable should end with a trailing underscore.
Parameters are well written in lowerCamelCase. It holds good for constructor parameters.
one character parameter should not be used in public methods.
local variable names are written in lowerCamelCase.
Local Variable Declaration:
Declare the local variables with either let or const keyword. Use const by default if the variable doesn't need to be reassigned. 
The Var keyword must not be used.
One variable per declaration. for example: let i = 1 , j =2 is not a good practice. 
Array Literals:
Whenever there is a line break between closing bracket and the final element, Include a trailing comma.
ex:      const values = [
             'first value',
             'second value',
        ];
Do not use the variadic constructor.
Illegal : const a3 = new Array(x1); // if x1 is undefined, then exception will be thrown.
Legal  : const a3 = [x1];
Do not use non-numeric properties on an array except length. Use an Object or Map instead.
String Literals:
Ordinary string literals should be delimited with single quotes('). single quotes(') should be preferred over double quotes(").
should not use line continuations(\).  
Illegal:
const lineString = 'Lorem Ipsum is simply dummy text of the printing \
        and typesetting industry. Lorem Ipsum has been the industry\
        standard dummy text ever since the 1500';

Legal:
const lineString = 'Lorem Ipsum is simply dummy text of the printing ' +
        'and typesetting industry. Lorem Ipsum has been the industry ' +
        'standard dummy text ever since the 1500';

For Loops:
There are three different types of for loop available with ES6 Standards.  for...of statement should be preferred when ever possible.
for...in statement includes few unwanted prototypes properties so it should not be used for looping.
Prefer for...of and Objects.key over for...in when ever possible.
Exception:
Exceptions are an important part of the javascript programming language.
When ever exceptional case occurs, it must be used. Always should throw an Error or subclass of an Error.
new keyword must be used while constructing an error.
Never throw a string or any other object as an Error in your code.
Switch Statement:
Must be enclosed in braces. Switch statements must contain default cases, even through the code is not present.
Switch cases will either terminate abruptly (with the break, or return statement) or will be marked with the comment stating execution will continue in next statement group. "// Fall through" comment should be used to mention the idea of fall-through.
this Keyword:
this keyword must be used only inside class constructor and methods or in the arrow function inside a class constructor and methods.

Some General Guidelines:
With keyword should not be used.
Eval function should not be used.
Always terminate a statement with a semicolon.
Mark deprecated methods, classes, and interfaces with @deprecated annotation.
Set compiler warning level to verbose.
Use of "Strict mode" is highly encouraged.

