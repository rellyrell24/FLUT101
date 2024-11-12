# Variables, Types, and Operators: Managing Data

In Dart, managing data is essential for creating efficient and maintainable applications. This article will explore variables, types, and operators, focusing on declaring, initializing, and manipulating data in Dart.

## Variables

Variables store data, which can be manipulated and used throughout your program. In Dart, you can declare a variable using the `var` keyword, followed by the variable name and an optional type annotation.

<code>var age = 30; // Inferred type is int
var name = 'Alice'; // Inferred type is String</code>

When declaring a variable without an initial value, you can use the `late` keyword to indicate that the variable will be initialized later.

<code>late String address;
address = '123 Main St';</code>

You can also declare a constant value using the `const` or `final` keywords. The `const` keyword is used for compile-time constants, while the `final` keyword is used for runtime constants.

<code>const int speedOfLight = 299792458; // Compile-time constant
final DateTime now = DateTime.now(); // Runtime constant </code>

## Data Types

Dart has several built-in data types, including:

* Dart has two types of numbers: integers (whole numbers) and doubles (floating-point numbers). You can declare an integer using the int keyword and a double using the double keyword.

<code>int x = 10;
double y = 3.14;</code>

* Strings represent sequences of characters and can be declared using single or double quotes.

`String greeting = 'Hello, world!';`

* Booleans represent true or false values and can be declared using the bool keyword.
  
`bool isActive = true;`

* Lists: Lists (also known as arrays) are ordered collections of items. You can declare a list using the List keyword or the square bracket syntax in Dart.

`List<int> numbers = [1, 2, 3];`

* Sets: Sets are unordered collections of unique items. In Dart, you can declare a set using the Set keyword or the curly bracket syntax.

`Set<int> uniqueNumbers = {1, 2, 3, 3};`

* Maps: Maps are collections of key-value pairs, where each key is associated with a value. In Dart, you can declare a map using the Map keyword or by using the curly bracket syntax.

`Map<String, int> ages = {'Alice': 30, 'Bob': 25};`

## Operators

Operators are symbols that perform specific operations on operands, such as arithmetic, comparison, and logical operations. Dart supports a wide range of operators, including:
* Arithmetic Operators: These operators perform operations like addition, subtraction, multiplication, and division.

<code>int sum = 10 + 20; // 30
int difference = 10 - 20; // -10
int product = 10 * 20; // 200
int quotient = 20 ~/ 10; // 2
int remainder = 20 % 10; // 0</code>

* Increment and Decrement Operators: These operators are used to increment or decrement a variable by 1.

<code>int counter = 0;
counter++; // 1
counter--; // 0</code>

* Relational Operators: These operators compare two values and return a boolean result.
  
<code>bool isEqual = 10 == 20; // false 
bool isNotEqual = 10 != 20; // true 
bool isGreater = 10 > 20; // false 
bool isLess = 10 < 20; // true 
bool isGreaterOrEqual = 10 >= 20; // false 
bool isLessOrEqual = 10 <= 20; // true</code>

* Logical Operators: These operators perform logical operations like AND, OR, and NOT.

<code>bool result1 = true && false; // false
bool result2 = true || false; // true
bool result3 = !true; // false</code>

* Assignment Operators: These operators assign a value to a variable.
  
<code>int x = 10;
x += 5; // 15 (equivalent to x = x + 5)
x -= 5; // 10 (equivalent to x = x - 5)
x *= 2; // 20 (equivalent to x = x * 2)
x ~/= 2; // 10 (equivalent to x = x ~/ 2)
x %= 3; // 1 (equivalent to x = x % 3)</code>

* Conditional Operator: This operator is a shorthand way of writing an if-else statement. It is also called the ternary operator.

`String result = 10 > 20 ? 'Greater' : 'Less'; // 'Less'`

* Null Coalescing Operator: This operator returns the first non-null value.

<code>String? name;
String username = name ?? 'Anonymous'; // 'Anonymous'</code>

## Type Conversion

Sometimes, you may need to convert data from one type to another. Dart provides several methods for type conversion, including:
* String to Number: Use the `int.parse()` and `double.parse()` methods to convert a string to an integer or a double, respectively.

<code>String strInt = '42';
int intValue = int.parse(strInt); // 42
String strDouble = '3.14';
double doubleValue = double.parse(strDouble); // 3.14</code>

* Number to String: You can use the toString() method to convert a number to a string.

<code>int intValue = 42;
String strInt = intValue.toString(); // '42'
double doubleValue = 3.14;
String strDouble = doubleValue.toString(); // '3.14'</code>

* Type Checking: You can use the is and is! operators to check if an object is of a specific type.

<code>Object obj = 42;
bool isInt = obj is int; // true
bool isNotInt = obj is! int; // false</code>

Understanding how to manage data in Dart is crucial for creating efficient and maintainable applications. Learning about variables, types, and operators allows you to effectively declare, initialize, and manipulate data to suit your program's requirements. These fundamental concepts will be the foundation for more advanced Dart programming techniques and applications.