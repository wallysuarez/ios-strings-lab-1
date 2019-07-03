# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)

```
for i in 1...10 {
print(String(i), terminator: " ")
}
```
***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.
```
for i in 5...51 where i % 2 == 0 {
print(String(i), terminator: " ")
}
```
***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.
```
for i in 1...60 where i == 4 {
for j in stride(from: i, to: 60, by: 10) {
print(String(j), terminator: " ")
}
}
```

***
## Question 4

Print each character in the string `"Hello world!"`

```
var string = "Hello, world!"

for i in string {
print(i)
}
```
***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

```
print(myStringSeven[myStringSeven.index(myStringSeven.endIndex, offsetBy: -2)])
```

***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

```

```

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

```
var singleCharacter = Character("a")
print(singleCharacter)
```
***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`
```
var helloUni = ("\u{0022}\u{0048}\u{0045}\u{004c}\u{004c}\u{004f} \u{0057}\u{004f}\u{0052}\u{004c}\u{0044}\u{0021}\u{0022}")
print(helloUni)
```
***
## Question 10

**Using only Unicode**, print out your name.

```
var myName = ("\u{0057}\u{0041}\u{004c}\u{004c}\u{0059} \u{0053}\u{0055}\u{0041}\u{0052}\u{0045}\u{005a}")
print(myName)
```
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

```
var helloSpanish = ("\u{0022}\u{0048}\u{004f}\u{004c}\u{0041} \u{004d}\u{0055}\u{004e}\u{0044}\u{004f}\u{0021}\u{0022}")

print(helloSpanish)
```

***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```
```
var flower = "\u{2698}"
var verticalSymbol = "\u{007c}"
var horizontalSymbol = "\u{005f}"

for _ in 1...11 {
print(horizontalSymbol, terminator: " ")
}
print()
print()
for _ in 1...7 {
print("\(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol)")
}
for _ in 1...11 {
print(horizontalSymbol, terminator: " ")
}
```
***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

var aString = "this string has 29 characters"
var reverse = String(aString.reversed())
print(reverse)
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

let aString = "anutforajaroftuna"
let palindrome = String(aString.reversed())

if aString == palindrome {
print(true)
} else {
print(false)
}
```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

var split = problem.split(separator: " ")

for i in split {
print(i)
}
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

***
