# Dart Syntax and Semantics: The Building Blocks

As a programming language, Dart has a well-defined syntax and semantics that allow developers to express complex logic in a readable and maintainable manner. This chapter will explore the building blocks of Dart syntax and semantics, covering key aspects such as variables, data types, control structures, functions, classes, and more.

## Variables and Data Types

Variables are fundamental to any programming language, allowing developers to store and manipulate data. In Dart, variables are declared using the var keyword, followed by the variable name and an optional type annotation.

`var age = 30; // Inferred type is int`
`var name = 'Alice'; // Inferred type is String`

Dart supports several built-in data types, including:
* Numbers: Dart has two types of numbers: integers (whole numbers) and doubles (floating-point numbers). You can declare an integer using the int keyword and a double using the double keyword.
  
`int x = 10;
double y = 3.14;`

* Strings represent sequences of characters and can be declared using single or double quotes.

`String greeting = 'Hello, world!';`

* Booleans represent true or false values and can be declared using the bool keyword.

`bool isActive = true;`

* Lists (also known as arrays) are ordered collections of items. You can declare a list using the List keyword or the square bracket syntax in Dart.

`List<int> numbers = [1, 2, 3];`

* Maps are collections of key-value pairs, where each key is associated with a value. You can declare a map in Dart using the Map keyword or the curly bracket syntax.

`Map<String, int> ages = {'Alice': 30, 'Bob': 25};`

## Control Structures
Control structures help manage the flow of a program, allowing developers to express conditional logic and loops. Dart provides several control structures, including:
* If-Else: The if-else statement allows you to execute different code blocks based on a condition.

<code>if (age > 18) {
  print('Adult');
} else {
  print('Not an adult');
}</code>

* Switch-Case statement executes different code blocks based on the value of a variable or expression.

<code>switch (grade) {
  case 'A':
    print('Excellent');
    break;
  case 'B':
    print('Good');
    break;
  default:
    print('Not graded');
}</code>

* For loop is used to iterate over a sequence of values or a collection.

<code>for (int i = 0; i < 10; i++) {
  print(i);
}</code>

<code>for (var number in numbers) {
  print(number);
}</code>

* While and do-while loops are used to execute a block of code repeatedly as long as a condition is true.

<code>int i = 0;
while (i < 10) {
  print(i);
  i++;
}</code>

<code>do {
  print(i);
  i--;
} while (i > 0);</code>

## Functions
Functions are reusable blocks of code that accept input (parameters) and return a value. Functions in Dart can be declared using the void keyword for functions that do not return a value or by specifying the return type.

<code>void greet(String name) {
  print('Hello, $name!');
}</code>

<code>String getGreeting(String name) {
  return 'Hello, $name!';
}</code>

Dart also supports arrow syntax (=>) for short, single-expression functions.

`void greet(String name) => print('Hello, $name!');`

`String getGreeting(String name) => 'Hello, $name!';`

Functions can also have optional parameters, either positional or named. Positional parameters are enclosed in square brackets, while named parameters are enclosed in curly brackets.

<code>void greet(String name, [String salutation]) {
  print('$salutation, $name!');
}</code>

<code>void greetNamed({String name, String salutation}) {
  print('$salutation, $name!');
}</code>

## Classes and Objects
Dart is an object-oriented programming language that supports classes, objects, inheritance, and other object-oriented features. Classes define the structure and behavior of objects, while objects are instances of classes.

To declare a class in Dart, you use the class keyword, followed by the class name and a pair of curly braces enclosing the class members (fields, properties, and methods).

<code>class Person {
  String name;
  int age;
  void sayHello() {
    print('Hello, I am $name!');
  }
}</code>

To create an object (instance) of a class, you use the new keyword followed by the class name and a pair of parentheses.

<code>Person alice = new Person();
alice.name = 'Alice';
alice.age = 30;
alice.sayHello();</code>

Dart also supports constructors, special methods executed when an object is created. Constructors can be used to initialize the object's properties.

<code>class Person {
  String name;
  int age;
  Person(this.name, this.age);
  void sayHello() {
    print('Hello, I am $name!');
  }
}
Person alice = new Person('Alice', 30);
alice.sayHello();</code>

## Inheritance and Polymorphism
Inheritance is a powerful feature of object-oriented programming that allows you to create a new class based on an existing one. The new class inherits the base class members and can also add or override members.

You can use the extends keyword in Dart to create a derived class.

<code>class Employee extends Person {
  String title;
  Employee(String name, int age, this.title) : super(name, age);
  void introduce() {
    print('Hello, I am $name, and I am a $title!');
  }
}
Employee bob = new Employee('Bob', 25, 'Software Engineer');
bob.introduce();</code>

Polymorphism is another important concept in object-oriented programming that allows objects of different classes to be treated as objects of a common superclass. This enables you to write more flexible and reusable code.

<code>void sayHello(Person person) {
  person.sayHello();
}
sayHello(alice);
sayHello(bob);</code>

In summary, Dart's syntax and semantics provide developers with a powerful and flexible foundation to build web, mobile, and server applications. By understanding the building blocks of Dart, such as variables, data types, control structures, functions, and object-oriented features, you can create efficient and maintainable code for a wide range of applications.
