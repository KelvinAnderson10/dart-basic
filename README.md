# Dart Programming Language

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
print("I Love $language"); // Output: I Love Flutter

String upperCase = '${"hello".toUpperCase()}';
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

## Type Conversion
