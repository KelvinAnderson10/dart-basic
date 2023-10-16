# Dart Programming Language 💙

## Table of Contents
1. [Chapter 1: Built-in Data Type](#chapter-1-built-in-data-type)
2. [Chapter 2: Variable Declaration](#chapter-2-variable-declaration)
3. [Chapter 3: Type Conversion](#chapter-2-type-conversion)
4. [Chapter 4: Conditions](#chapter-3-conditions)
5. [Chapter 5: Loops](#chapter-4-loops)
6. [Chapter 6: Functions](#chapter-5-functions)
   
## Chapter 1: Built-in Data Type
The Dart language has special support for the following:
#### 1. Integer
```dart
int age = 20;
```
#### 2. Double
```dart
double pi = 3.14;
```
#### 3. String
```dart
String name = 'Kelvin';

// String Interpolation
var language = 'Flutter';
print('I Love $language'); // Output: I Love Flutter

String upperCase = '${'hello'.toUpperCase()}';
print(uppercase); // Output:HELLO
```
#### 4. Boolean
```dart
bool isAlive = true;
```
#### 5. List
```dart
var numbers = [1,2,3,4,5];
```
#### 6. Map (Key-Value) 
```dart
var profile = {'name':'Kelvin','age':23}
```
#### 7. Set -> unique
```dart
var halogens = {'fluorine', 'chlorine', 'bromine', 'iodine', 'astatine'};
var luckyNumbers = [7, 9, 10];
```

---

## Chapter 2: Variable Declaration
#### 1. Type Inference
```dart
var name = 'Kelvin';
```
#### 2. Predefined data type
```dart
int age = 20;
```
#### 3. Nullable
```dart
int a = null; // INVALID in null-safe Dart.

int? a = null; // Valid in null-safe Dart.

int? a; // The initial value of a is null.
```
#### 4. `late`
Better late than never, declare variables that will be initialized later
```dart
late int marriedAge;
marriedAge = 30;
```
#### 5. `dynamic`
Can store any data type
```dart
dynamic goal = false;
goal = "SIUUUUUUU";
```
#### 6. `const`
const keyword used to make a variable to store a compile time constant value. Compile time constant value is a value which will be constant while compiling. const is used to make the object immutable.
```dart
const a = 5;
const a = 69; // **ERROR**

const b;
b = 6; // **ERROR** (Must be 1 LINE)

const languages = ['Dart', 'Golang'];
languages = ['Java', 'Kotlin']; // **ERROR**

const languages = ['Dart', 'Golang'];
languages.add('Cindo'); // **ERROR**
languages[0] = 'Cindo'; // **ERROR**
```
#### 7. `final`
final keyword also used to make the variable to hold a constant value. Once initialized we can't change the value.
```dart
final myAnimeList = ['Naruto', 'AOT'];
myAnimeList.add('Barbie'); // **SUCCESS**
myAnimeList[0] = 'Barbie'; // **SUCCESS**
```
---

## Chapter 3: Type Conversion
```dart
// String to int
var one = int.parse('1');
print(one); // Output: 1

// String to double
var onePointOne = double.parse('1.1');
print(onePointOne); // Output: 1.1

// int to String
var twenty = 20.toString();
print(twenty); // Output: 20

// double to String
var pi = 3.14316.toStringAsFixed(2);
print(pi); // Output: 3.14
```
---

## Chapter 4: Conditions
#### 1. Ternary Operator
```dart
int num = 5;
String res = (num % 2) == 0 ? 'Even' : 'Odd';
print(res); // Output: Even
```

#### 2. Null Safety Operator
```dart
String? favoriteFood;
print(favoriteFood ?? 'Cannot be null'); // Output: Cannot be null
print(favoriteFood!) // Use bang operator (!) to tell the compiler that the value won't be null

int? num = null;
num ?? = 1; // num will be assigned by 1 if it's null
```

#### 3, If-Else
```dart
int noOfMonth = 5;
if (noOfMonth == 1) {
  print("The month is jan");
} else if (noOfMonth == 2) {
  print("The month is feb");
} else {
  print("Invalid option given.");
}
```

#### 4, Switch Case
```dart
var dayOfWeek = 5;
switch (dayOfWeek) {
  case 1:
      print("Day is Sunday.");
      break;
  case 2:
      print("Day is Monday.");
    break;
  default:
      print("Invalid Weekday.");
    break;
}
```
---

## Chapter 5: Loops
#### 1. For
```dart
for (int i = 0; i < 10; i++) {
  print(i);
}
// Output: 0 1 2 3 4 5 6 7 8 9
```

#### 2. For in
```dart
List<String> vocal = ['a', 'i', 'e', 'o'];
for (String v in vocal) {
  print(v);
}
// Output: a i u e o
```

#### 3. While
```dart
var i = 1;
while (i < 5) {
  print(i);
  i++;
}
// Output: 1 2 3 4
```

#### 4. Do-While
`do` scope will be executed before checking the `while` statement, meaning do-while will always be executed at least once
```dart
var i = 1;
do {
  print(i);
  i++;
} while (i < 5);
// Output: 1 2 3 4
```
---

## Chapter 6: Functions
```dart
// We use void if our function doesn't return anything
void greet(String name) {
  print('Hello $name');
}

// Function with return value
int add(int number1, int number2) {
  return number1 + number2;
}

// Optional Positioned Parameter Function
void optionalPositionedParam(int g1, [ var g2 ]) {
  print("g1 is $g1");
  print("g2 is $g2");
}
optionalPositionedParam(1)

// Optional Named Parameter Function
void optionalNamedParam(int g1, { var g2, var g3 }) {
  print("g1 is $g1");
  print("g2 is $g2");
  print("g3 is $g3");
}
optionalNamedParam(1, g3 : 12)

// Function with default param
void defaultParam(int g1, { int g2 : 12 }) {
  print("g1 is $g1");
  print("g2 is $g2");
}
defaultParam(1)
```
