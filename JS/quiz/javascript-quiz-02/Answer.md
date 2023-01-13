###### Question 1: What's the output?

```js
function greeting() {
console.log(name);
console.log(age);
var name = "Hana";
let age = 21;
}

greeting();
// A: Hana and undefined
// B: Hana and ReferenceError
// C: ReferenceError and 21
// D: undefined and ReferenceError

// Ans: D
// Short explanation: The variable declared by "var" behaves as hoisting, so the variable can be used before it has been declared, but the default value "undefined" is shown in this case, because the declaration is executed before using automatically but the value is assigned at the point of the sentence. In the other side, the variable declared by "let" can't be used before it is declared, it cause reference error.

```
###### Question 2: What's the output?

```js
+true;
!"Lydia";

// A: 1 and false
// B: false and NaN
// C: false and false

// Ans: A
// Short explanation: These output shows results by calculating or compared to a default value. "+true" means "default value 0 plus true (1) = 1", '!"Lydia"' means 'the result comparing "undefined" to "Lydia"'.

```
###### Question 3: What's the output?

```js
function sum(a, b) {
return a + b;
}

sum(1, "2");

// A: NaN
// B: TypeError
// C: "12"
// D: 3

// Ans: C
// Short explanation: The "+" operator deal with operands as String when one of them is String type, so these operands are merged as String.

```
###### Question 4: What's the output?

```js
let number = 0;
console.log(number++);
console.log(++number);
console.log(number);

// A: 1 1 2
// B: 1 2 2
// C: 0 2 2
// D: 0 1 2

// Ans: C
// Short explanation: At first declared value 0 is shown on console then increment is executed, so number become 1. Secondly, increment is executed before the number variable is shown in console, so 2 is shown on console. At last, the number variable doesn't change and 2 is shown on console again.

```

###### Question 5: What's the output?

```js
!!null;
!!"";
!!1;

// A: false true false
// B: false false true
// C: false true true
// D: true true false

// Ans: B
// Short explanation: "!!" means that "not" is repeated twice, which means the result doesn't change from original value. These original values are 'null' and '""' is false, '1' is true.

```
###### Question 6: What's the output?

```js
console.log(3 + 4 + "5");

// A: "345"
// B: "75"
// C: 12
// D: "12"

// Ans: B
// Short explanation: The sentence is read from the start, so firstly "3 + 4" is executed, which means 7 because 2 characters are number and they are calculated as number. Then '7 + "5"' is executed, but "5" is String type, so these operands are deal with String, which merge 2 values as String.

```
###### Question 7: What's the value of num?

```js
const num = parseInt("7*6", 10);

// A: 42
// B: "42"
// C: 7
// D: NaN

// Ans: C
// Short explanation: This parseInt function try to change String "7*6" to a decimal number. But in purseInt function, if there is non numerical character, it is ignored and following characters are also ignored. In this case, first character "7" is changed to a number, but non numerical number (*) and following "6" are ignored.

```

###### Question 8:

Write a function indexOfIgnoreCase taking two strings
and determining the first occurrence of the second
string in the first string. The function should be
case insensitive.

Example: indexOfIgnoreCase('bit','it') and
indexOfIgnoreCase('bit','IT') should return 1.

```js
//Hint
function indexOfIgnoreCase(s1, s2) {
// Change s1 and s2
// first to lowercase.
// Then use the
// indexOf method.
    return s1.toLowerCase().indexOf(s2.toLowerCase());
}

```

###### Question 9:
Write a function firstChar, which returns the
first character that is not a space when a string
is passed.

Example: firstChar(' Rosa Parks ') should return 'R'.

```js
//Hint:
function firstChar(text) {
// Trim first.
// Then use the
// charAt method.
    return text.trim().charAt(0);
}
```

###### Question 10:
Write a function normalize, that replaces '-'
with '/' in a date string.

Example: normalize('20-05-2017') should return
'20/05/2017'.

```js
function normalize(date) {
    return date.replaceAll('-', '/');
}
```