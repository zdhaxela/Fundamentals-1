# key concepts in c++ programing

namespaces - help organize code, prevent naming conflicts, and avoid confusion

`
#include <iostream> 
`

 library, which is necessary for input/output operations (like printing to the console)


`intmain` ()
- start of the main function.

`int`

- indicates that the main function returns an integer value
`main`

- special function name that marks the beginning of your program's execution. The operating system looks for this function when it starts your program


`return 0`;
 - This line indicates that the program has executed successfully and returns the value 0 to the operating system.
- Non-zero values often indicate an error

`using namespace std;`:

- This statement allows you to use elements from the std namespace (like cout, cin, endl) without the std:: prefix, making your code more concise

`cin`	- Standard input stream 
`cout` - Standard output stream 

####  # different types of variables in C++ -


- `int` - stores integers (whole numbers), without decimals, such as 123 or -123
- `double` - stores floating point numbers, with decimals, such as 19.99 or -19.99
- `char` - stores single characters, such as 'a' or 'B'. Char values are surrounded by - single quotes. one printbale character except blank.
- `string` - stores text, such as "Hello World". String values are surrounded by double quotes
- `bool` - stores values with two states: true or false

the syntax of an input statement usimng cin and the extraction operator >> is 
cin >> variable >> variable...;

the extraction operator >> is binary

to use pow (power), include cmath
two numeric valuse
syntax: pow(x,y) =x^y
- x and y are the arguments or parameters
- in pow (2,3), the parameters are 2 and 3

the get function
inputs the next character including whitespace
stores in memory location indicated by its argukejt
the syntax of cin and the get functioncin.get (varChar);

varChar is a char variable
it is the argument (or parameter) of the function

ignore function- discards a portion of the imput

the syntax to use the function ignore is:
cin.ignore(intExp, chExp);
intExp is an integer expression
chExp is a char expression

putback function 
places previous character extracted by the get function from an input stream back to that stream

- '`peek`' function
-returns next character from the input stream
-does not remove the character from that stream

syntax for putback
- istreamVar.putback(ch);
istreamVar: an input stream variable (such as cin)
ch is a char variable

syntax for `peek`
ch = istreamVar.peek();

in the statement 
cin.get(ch);
cin and get are two separate identifiers sperarated by a dot
- called the dot nation, thr dot separates the input stream variable name from the member, or function, name
- in C++, the dot is the member access opeerator

- syntax of cout when used with <<
cout << expression or manipulator<< expression or manipulator...l
- expression is evaluated
value is printed
manipulator is used to format the output
    - example: endl
Syntax 
setprecison(n)
- outputs decimal number with up to n decimal places
- must include the header file iomanip
    -#include <iomanip>

fixed outputs floating-point numbers in a fixed decimal format
• Example:
• Disable by using the stream member function unsetf
- Example:
• scientific manipulator outputs floating-point numbers in scientific format

showpoint forces output to show the decimal point and trailing zeros
• Examples
- cout << showpoint;
- cout << fixed << showpoint;

n C++, commas cannot be used to separate the digits of a number
• C++14 introduces digit separator ' (single-quote character)
• Example: 87523872918 can be represented as 87'523'872'918

Outputs the value of an expression in a specified number of columns
• cout << setw(5) << x<< endl;
• If number of columns exceeds the number of columns required by the
expression
• Output of the expression is right-justified
• Unused columns to the left are filled with spaces
• Must include the header file iomanip

Additional formatting tools that give you more control over your output:
• setfill manipulator
• left and right manipulators
• unsetf manipulator

Output stream variables can use setfill to fill unused columns with a
character
ostreamVar << setfill(ch);>>
• Example:
• cout << setfill('#')

left manipulator left-justifies the output
ostream << left;
diasable left by using unsetf
ostreamVar.unsetf(ios::left);
right manipulator right-justifies the output
ostreamVar << right;

Two types of manipulators
• Those with parameters
• Those without parameters
• Parameterized stream manipulators require the iomanip header
• setprecision, setw, and setfill
• Manipulators without parameters require the iostream header
• endl, fixed, scientific, showpoint, and left

 An input stream variable (such as cin) and operator can read a string into
a variable of the data type string
• The extraction operator:
• Skips any leading whitespace characters
• Stops reading at a whitespace character
• The function getline reads until end of the current line
getline(istreamVar, StrVar);>>>>

Syntax errors are reported by the compiler
• Logic errors are typically not caught by the compiler
• Spot and correct using cout statements
- Temporarily insert an output statement
• Correct the problem
• Remove output statement

A file is an area in secondary storage to hold info

file I/O is a five-step process
1. Include `fstream` header
2. Declare file stream variables
3. Associate the file stream varian=bles with the input/output sources - referred to as opening the files
4. Use the file stream variables with >>,<<, or other input/output functions
5. Close the files

stream: infinite sequence of characters from a source to a destination
- input stream: from a source to a computer
- Output stream: from a computer to a destination
- `cin`: common input
- `cout`: common output 
- to use `cin` and `cout`, include `iostream` header

- `get` reads data character-by-character
- `ignore` skips data in a line 
- `putback` puts last character retrieved by get back to the input stream
- `peek` returns next character from input stream, but does not remove it
- attempting to read invalid data into a varable causes the input stream to enter the fail statement

- The manipulators `setprecision`, `fixed`, `showpoint`, `setw`, `setfill`, `left`, and `right`, can be used for formatiing output
- include `iomanip` for the manipulators `setprecision`, `setw`, and `setfill`
- header `fstream` contains the definitions of `ifstream` and `ofstream`

chapter 4
- A computer can proceed:
in sequence
selectively (branch) making a choice
repetively looping
by calling a function

- the two most common control structures are
selection and repetition

- an expression that evaluates to true or false is called a logical expression
"8 is greater than 3" is true

- each relational operator is a binary operator (requires two operands)
- expression using these operator always evaluate to true or false

- in an expression of char values using relatonal operators
the result depends on the machines collating sequence
ASCII character set
- Logical Boolean expressions
include expressions such as 4< 6 and 'R" > "T"
return an integer value of 1 if the logical expression evaluates to true
return an integer to 0 if otherwise

- one-way selection syntax
if (expression) statement
- the statement is:
executed if the value of the expression is true
bypassed if the value is false; program goes to the next statement
- the expression is also called a decision maker
- the statement following the expression is also called the action statement

two way selection
if (expression) statement1
else statement2

-if expression is true, statement1 is executed; otherwise, statement2 is executed
- statement1 and statement2 are any C++ statements

- the data type bool has logical (boolean) values true and false- bool, true, and false are reserved words
- the identifier true has the value 1
- the identifier false has the value 0

- logical (boolean) operators enable you to combine logical expressions

- relational and dlogical operators are evaluated from left to right
- the associativity is left to right
- parentheses can override precedence

relational operators can be applied to variables of type String
- strings are compared character by character, starting with the first character
- comparison continues until either a mismatch is found or all characters are found equal
- if two strings of different lengths are compared and the comparison is equal to the last character of the shorter string 
- the shorter string is less than the larger string

A compound statement (block of statements) has this form
{
    statement_1
    statement_2
-
-
-

}
when control statement is located within another, it is said to be nested
- an else is associated with the most recent if that has not been paired with an else
- nested|chained

  short-circuit evaluation: evaluation of a logical expression stops as soon as the value of the expression is known

  comparison of floating-point numbers for equality may not behave as you would expect
- example: 
  - a solution is checking for a tolerance value / epsilon value
  example: if fabs(x-y) < 0.000001

  if an inout stream enters a fail state:
  - all subsequent input statements associated with that stream
  