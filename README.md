# JavaScript course

# JavaScript

# .......................................................................

# Lesson 1

# What is JavaScript?
    JavaScript is a technology that we used to create websites.
    ex: youtube.com
        amazone.com

usually we use mainly 3 technologies to create a website.
- HTML
- CSS
- JavaScript

HTML creates the content of a website. (buttons, images, texts)
CSS changes the appearences of the website. to make the website looks nice.
JavaScript makes the website interactive.

before work on the JavaScript, we need to have setup as,
a web browser.

To learn JavaScript, give instructions to the computer.
then the computer follows the instructions.

# Terminology (Naming)

JavaScript is a programming language. Used to code.
To test the JS code, we can use web browser's console.

JS can do many things,
- create alerts
- do math etc..

alert('Hello');
4 + 4

* JavaScript is case sensistive.

document.body.innerHTML = 'Hello';
this removes everything on the webpage and replaces with 'Hello'. This is used to odify the web page.
it is one of the most important feature in Java Script.

# Basics of JavaScript--

- Giving instructions to a computer. (Code)
- The computer follows our instructions. (running the code)

# Syntax

- Syntax are the rules that we have to follow when using a programming language.
- Similar to English. (grammar)
But the difference between english grammar and syntax is, we don't necessarily follow the grammar to get an understand. 
But in programming, we have to follow the rules of syntax exactly. otherwise the computer will not understand our code.

Ex : alert'Hello');
Uncaught SyntaxError: Unexpected string

# .......................................................................

# Lesson 2

# Numbers and Math

Syntax for math in JavaScript is like normal math. + - / *
JS can handle decimal numbers too. (Ex: 2.58)

Order of Operations: (Operator Precedence)
 2 + 2
 2 - 2
 10 * 3
 10 / 2

+ - * / are called operators.

* / are done first. & have the same priority.
+ - are done after. & have the same priority.

2 * 3 / 5 
 -> calculate from left to right

2 + 3 - 5 
 -> calculate from left to right

For order of operations, we can use brackets also. To control which part gets done first.

(1 + 1) * 3
first do inside the brackets addition and then multiply.

brackets have the highest priority in the order of operations.
1. (.....)
2. * /
3. + -

1. Weired behavior of math in JavaScript

In programming,
2, 3, 4 = Integers
2.2, 2.5 = floating point numbers (floats)

computers have a problem working with floats.

ex: 0.1 + 0.2 
=> 0.30000000000000004

computers can only store numbers 0 and 1.
but humans can count from 0,1,2......9

Human           Computer
2                10
99               1100011
0.2              ??

How the computer stores 0.2
0.0011001100110011........

but this doesn't happen with all the floats. so this issue happens with some of the floats.

When calculating money, we want to avoid any inaccuracies.

* Remember,
In programming, Calculations with floats are sometimes innacurate.

when working with money, the best practice is,
1. Do the calculation in cents.
2. Convert back to dollars.

* How to round a number in JavaScript,

Math.round(2.2);
=> 2

Math.round(2.8);
=> 3

Ex: first calculate the money in cents, then round it to the nearest cents, and then convert back to dollar.

((2095 + 799) * 0.1 ) / 100
=> 2.89

# .......................................................................

# Lesson 3

# Strings
String represents a text.

Syntax rules for String.

can add two strings together by +
Ex: 
'some' + 'text'
=> 'sometext'

can add more than 2 strings also.
Ex: 
'some' +  'more' + 'text'
=> 'somemoretext'

This is called concatenation. (combining multiple strings together.)

Numbers & Strings are two different types of values in JavaScript.
we can check the type of the value by,

typeof 2
=> 'number'

typeof 'hello'
=> 'string'

when we add a string and a number, JavaScript automatically converts the number into a string and combines them together.
This is called,
# Type coercion
(automatic type conversion - automatically convert the values from one data type to another.)

'hello' + 3
=> 'hello3'

Strings also follow the order of operations.

'$' + (2095 + 799)/100
=> '$28.94'

[brackets are always calculated first, then + and the / ]
then adding the value to the $ sign is the final step.

'Items (' + (1 + 1) + '): $' + (2095 + 799) / 100
=> 'Items (2): $28.94'

alert('Items (' + (1 + 1) + '): $' + (2095 + 799) / 100);

In JavaScript, there are 2 ways to create strings.
1. single quotes. '......'   'Hello'
2. double quotes. "......"   "Hello"
3. backtick. `.......`

which one to use,
In JS, it is recommend to use single quotes.

# Escape Character

character = 1 letter/number/symbol

character:
1. letter (a,b,c)
2. number (1,2,3)
3. symbol (!,@,#)
4. escape character \'

Ex:
" I'm learning JavaScript "
' I\'m learning JavaScript '

\" = double quote that is just text
This doesn't start or end string.

\n = newline character
This creates a new line of texts.

alert('some\nwork');
=> some
   work

backtick
`hello`
'hello'

Strings created with backticks have a name. we called it "template strings"

# Interpolation = insert value directly into a string.

how to write below code using backticks,
'Items (' + (1 + 1) + '): $' + (2095 + 799) / 100
=> 'Items (2): $28.94'

`Items (${1 + 1}): $${(2095 + 799) /100}` 
=> 'Items (2): $28.94'

# Multi-line Strings

`some
text`
    
=> 'some\ntext'

So, what should we use to create a String?
'....' vs `....`

=> use single quotes '....' by default.

=> If we need interpolation, multi-line strings use `....`

# .......................................................................

# Lesson 4

# HTML , CSS , JavaScript together.
# Basics of HTML & CSS

# HTML - Hyper Text Markup Language
- Giving instructions to a computer.

unlike JS, we can't use the console to write and test the HTML code.
we have to use a file to do HTML code.

Just like JS, HTML is also giving instructions to the computer.

HTML Syntax:

HTML elements:
<p></p>
<button></button>

nested elements:
<p><button>Hello</button></p>

multiple spaces are combined into 1 sppace in HTML.
<p>This is            <button>Hello</button>a paragraph.</p>

new lines also count as spaces.
<p>This is           
    <button>Hello</button>a paragraph.</p>

web page =  a single page (on a website) 
Ex: home page, cart page etc.. (Together all these, we call it a website)


# CSS - Cascading Style Sheets
- Changes the appearance.

<style></style>
Style tag is not visible on the web page.

CSS Syntax:

<style>
    button{
        background-color: red;
        color: white;
        border: none;
    }
</style>

button <--- CSS Selectior.
-> It tells the computer, which element we want to change.
-> Selects which elements to change.

CSS Styles :

background-color: red;
color: white;
border: none;

-> This tells the computer, how to change the appearance.

background-color: <--- CSS property.
-> It tells the computer, what we are changing.

red <--- CSS Value.
-> It tells the computer, what we are changing the property to.

; ---> is the end of the style. 


HTML Attributes:


































