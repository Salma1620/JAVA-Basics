# JAVA-Basics 2

# Table of contents
- [History](#History)
- [Java jvm-jre-jdk](#Java-JDK-JRE-JVM)
- [How to run java code](#How-to-run-java-code)
- [Basics](#Basics)
  - [Packages In Java](#Packages-In-Java)
  - [Arrays In Java](#Arrays-In-Java)
- [Object Oriented Programming Language (POO)](#Object-Oriented-Programming-Language)
  - [Classes and Objects](#Classes-And-Objects)
    - [Classes](#Classes)
      - [Access Modifiers in Java](#Access-Modifiers-in-Java)
      - [Method Overloading](#Method-Overloading)
      - [Keyword Final](#Keyword-Final)
      - [Keyword Static](#Keyword-Static)
      - [Keyword Super](#Keyword-Super)
  - [Four Pillars of Object-Oriented Programming in Java](#Four-Pillars-of-Object-Oriented-Programming-in-Java)
    - [Encapsulation](#Encapsulation)
    - [Inheritance](#Inheritance)
    - [Polymorphism](#Polymorphism)
    - [Abstraction](#Abstraction)
- [Interfaces](#Interfaces)
- [Exception Handling and Assertions](#Exception-Handling-and-Assertions)
  - [Types of Exception](#Types-of-Exception)
  - [Java try and catch](#Java-try-and-catch)
  - [Java Finally keyword](#Java-Finally-keyword)
  - [The throw keyword](#The-throw-keyword)
  - [The Throws keyword](#The-Throws-keyword)
- [String APIs](#String-APIs)


# History
> Java is a high-level, class-based, object-oriented programming language that was first released by Sun Microsystems in 1995. <br/>
> The company Oracle then acquired Sun Microsystems in 2009, which explains why this language now belongs to Oracle.

# Java JDK JRE JVM

## JVM (Java Virtual Machine)
> the core of the Java programming language. It is responsible for executing Java bytecode, which is the intermediate code generated after compiling a Java program.<br/>
> The JVM makes Java platform-independent by allowing the same Java bytecode to run on any device or operating system that has a compatible JVM.
> - Loads Bytecode: The JVM loads the compiled .class files into memory.
> - Execution: It executes the bytecode line by line using an interpreter or compiles it to native machine code using the Just-In-Time (JIT) compiler for performance.
> - Memory Management: The JVM manages memory allocation and garbage collection to ensure efficient use of resources.

## JRE (Java Runtime Environment)
> provides the necessary environment to run Java applications. <br/>
  > - JVM: The core engine that executes Java bytecode.
  > - Libraries: A set of standard libraries (like java.lang, java.util, etc.) required by Java applications to run.
  > - Other Files: Configuration files, property files, etc., that support the JVM in running Java programs.

## JDK (Java Development Kit)
> full-featured software development kit used for developing Java applications.
  > - JRE: As described above, it provides the runtime environment to execute Java applications.
  > - Development Tools: These include the Java compiler (javac), debugger (jdb), archiver (jar), and other tools necessary for writing and testing Java code.
  > - Additional Libraries: The JDK includes additional libraries required for development, such as those for GUI development (AWT, Swing) and networking.

## How to run java code
**1 - Navigate to the Directory Containing Your Java File** <br/>
**2 - Compile the Java Code** <br/>
> - Before running your Java program, you need to compile it. <br/>
> - The Java compiler (javac) converts your Java source code (.java file) into bytecode (.class file), which can be run on the 
    Java Virtual Machine (JVM). <br/>
> - the JDK is used to compile your .java file into a .class file (bytecode). <br/>

```java javac HelloWorld.java ``` <br/>

**3 - Run the Java Program** <br/>
> - Once compiled, you can run your program using the Java interpreter (java command). <br/>
> - You don't need to include the .class extension when running the file. <br/>
> - The JVM interprets the bytecode and interacts with the operating system and hardware to execute your program. <br/>
> - The JVM ensures that your Java program runs consistently across different platforms.<br/>
> - The JRE provides the necessary libraries and environment to support the execution of your program <br/>
> - While the JVM does the actual work of running it. <br/>

```java java HelloWorld ``` <br/>
# Basics
## Packages In Java
> - A package in Java is a namespace that organizes a set of related classes and interfaces.<br/>
> - Conceptually you can think of packages as being similar to different folders on your computer.<br/>

## Arrays In Java
> array is a container object that holds a fixed number of values of a single type.<br/>

The declaration of an array in Java is as follows:
```java
int[] myIntArray = new int[10]; // declares an array of integers
String[] myStringArray = new String[50]; // declares an array of strings
```

# Object Oriented Programming Language
> Object-Oriented Programming is a programming paradigm centered around the concept of "objects," which are instances of "classes."
> These objects are designed to represent real-world entities and can encapsulate data and behavior (données et methodes).

## Classes and Objects
### Classes
> It defines the properties (attributes) and behaviors (methods) that the objects created from the class will have.
  _everything belongs to a class except for primitive types (byte, short, int, long)._
**Example**
```java
public class Person {
    
    // Attribute (or field) of the class
    private String name;

    // Constructor to initialize the attribute
    public Person(String name) {
        this.name = name;
    }

    // Getter for the 'name' attribute
    public String getName() {
        return name;
    }

    // Setter for the 'name' attribute
    public void setName(String name) {
        this.name = name;
    }

}
```
#### Access Modifiers in Java
> - **public :** it can be accessed from anywhere in the program. <br/>
> - **private :**  it cannot be accessed directly from any other class, even subclasses. it's accessible just y the class <br/>
> - **protected :** allows the attribute or method to be accessible within its own package and by subclasses in other packages. <br/>
> - If no access modifier is specified, the field or method is package-private by default, meaning it is accessible only by classes in the same package. <br/>

#### Method Overloading 
  > It's a feature in Java where multiple methods in the same class can have the same name but different parameter lists (i.e., different types, number, or order of parameters).<br/>
  > Purpose: It allows the same method to perform different tasks based on the type and number of arguments passed to it.<br/>
  > Key Characteristics:<br/>
    > - **Same Method Name**: All overloaded methods share the same name.<br/>
    > - **Different Parameters**: The methods must differ in their parameter lists.<br/>
    > - **Compile-Time Polymorphism**: Method overloading is an example of compile-time polymorphism, meaning the method to be called is determined at compile time.<br/>

**Example:** Method Overloading
```java
class Calculator {
    // Method to add two integers
    int add(int a, int b) {
        return a + b;
    }

    // Overloaded method to add three integers
    int add(int a, int b, int c) {
        return a + b + c;
    }

    // Overloaded method to add two doubles
    double add(double a, double b) {
        return a + b;
    }
}
```

#### Keyword Final <br/>
**final with Variables** <br/>
> When a variable is declared as final, its value cannot be changed once it has been assigned. This effectively makes the variable a constant. <br/>
> - Final Primitive Variables: Once assigned, the value cannot be changed. <br/> 
> - Final Reference Variables: The reference cannot point to a different object after assignment, but the object's internal state can still be modified. <br/>
```java
public class FinalExample {
    final int MAX_VALUE = 100;  // Constant

    public void someMethod() {
        MAX_VALUE = 200;  // Error: Cannot assign a value to final variable 'MAX_VALUE'
    }
}
```
```java
public class FinalReferenceExample {
    final StringBuilder sb = new StringBuilder("Hello");

    public void modify() {
        sb.append(" World");  // Allowed, modifying the object
        sb = new StringBuilder("New Object");  // Error: Cannot reassign a final reference
    }
}
```
**final with Methods**
> When a method is declared as final, it cannot be overridden by subclasses. This is useful when you want to prevent a specific method from being changed by subclasses. <br/>

```java
public class ParentClass {
    public final void show() {
        System.out.println("This is a final method.");
    }
}

public class ChildClass extends ParentClass {
    @Override
    public void show() {  // Error: Cannot override the final method from ParentClass
        System.out.println("Attempting to override.");
    }
}
```
**final with classes**
> When a class is declared as final, it cannot be subclassed. This is useful when you want to prevent others from extending your class. <br/>

#### Keyword Static <br/>
> indicate that a particular member (variable, method, or nested class) belongs to the class itself, rather than to instances of the class. <br/>
> This means that static members are shared among all instances of the class and can be accessed without creating an object of the class.

**static Variables**
> A static variable is shared among all instances of a class. Instead of each object having its own copy of the variable, there is only one copy, <br/>
```java static int count = 0;``` <br/>

**static Methods** <br/>
> A static methods can be called without creating an object of the class. <br/>
> Static methods can only directly access static variables and other static methods. <br/>
```java
public class MathOperations {
    public static int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int sum = MathOperations.add(5, 10);  // No need to create an object
        System.out.println("Sum: " + sum);  // Output: Sum: 15
    }
}
```

**static Blocks** <br/>
> A static block is used to initialize static variables or perform static initialization when the class is first loaded. <br/>
> Static blocks are executed only once, when the class is loaded into memory. <br/>

```java
public class StaticBlockExample {
    static int value;

    static {
        value = 42;
        System.out.println("Static block executed.");
    }

    public static void main(String[] args) {
        System.out.println("Value: " + value);  // Output: Value: 42
    }
}
```

**static Classes (Nested Static Classes)** <br/>
> A static nested class is a class that is defined within another class (known as the outer class) and is declared with the static keyword. <br/>
> Unlike non-static inner classes, a static nested class does not automatically have access to the instance variables or methods of the outer class. It can only access the static members (variables and methods) of the outer class. <br/>
> Because it doesn't require an instance of the outer class, a static nested class can be instantiated on its own, using the outer class's name. <br/>
> Static nested classes are often used to group classes that are only used in one place, increasing encapsulation. <br/>
> They are also useful when the nested class doesn't need to access the instance members of the outer class. <br/<

```java
public class OuterClass {
    static int outerStaticVar = 10;  // Static variable in the outer class
    int outerInstanceVar = 20;       // Instance variable in the outer class

    // Static nested class
    static class NestedStaticClass {
        void display() {
            // Accessing the static variable of the outer class
            System.out.println("Outer static var: " + outerStaticVar);

            // Cannot access the instance variable of the outer class
            // System.out.println("Outer instance var: " + outerInstanceVar); // This would cause an error
        }
    }

    public static void main(String[] args) {
        // Instantiating the static nested class
        OuterClass.NestedStaticClass nested = new OuterClass.NestedStaticClass();
        nested.display();  // Output: Outer static var: 10
    }
}
```

#### Keyword Super
> - The super keyword refers to superclass (parent) objects.<br/>
> - It is used to call superclass methods, and to access the superclass constructor.<br/>
> - The most common use of the super keyword is to eliminate the confusion between superclasses and subclasses that have methods with the same name.<br/>
**exampleof using super**<br/>
```java
class Animal { // Superclass (parent)
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Dog extends Animal { // Subclass (child)
  public void animalSound() {
    super.animalSound(); // Call the superclass method
    System.out.println("The dog says: bow wow");
  }
}

public class Main {
  public static void main(String args[]) {
    Animal myDog = new Dog(); // Create a Dog object
    myDog.animalSound(); // Call the method on the Dog object
  }
}
```

### Objects
> It's an instance of a class.<br/>
> It represents a specific entity in the program, with its own set of attributes and behaviors defined by the class.<br/>

**Example: Creating an instance from "Person" class**
```java
public class Main {
    public static void main(String[] args) {
        // Creating an object of the Person class
        Person person1 = new Person("Alice", 25);

        // Modifying the object's attribute using setter
        person1.setName("Bob");

        // Displaying updated attribute
        person1.getName(); 
    }
}
```


# Four Pillars of Object-Oriented Programming in Java



## Encapsulation
> - the practice of bundling data (attributes) and methods (functions) that operate on the data into a single unit, known as a class. <br/>
> - It also involves restricting access to some of the object's components, which is typically done by using access modifiers (private, protected, public). <br/>
> - you can make the attributes of a class private and provide public getter and setter methods to control access to them.

## Inheritance
> - Inheritance allows a new class to inherit the properties and methods of an existing class.<br/>
> - The new class is called a `subclass` (or derived class), and the existing class is called a `superclass` (or base class).<br/>
> - This promotes code reuse and establishes a natural hierarchy between classes. <br/>
> - In Java, the `extends` keyword is used to create a subclass.<br/>
> - **Single Inheritance:** <br/>
  > Java supports single inheritance, meaning a class can only extend one superclass. However, a class can implement multiple interfaces, which provides a way to achieve multiple            inheritance.<br/>
> - **Constructor Inheritance:** <br/>
  > A subclass does not inherit the constructors of its superclass, but it can call a superclass's constructor using `super()` in its own constructor.

**Example:** Constructor Inheritance
```java
class Dog extends Animal {
    void printMessage() {
        super.eat();  // Calls the superclass version of eat()
        System.out.println("This message is from the Dog class.");
    }
}
```
> - **Method Overriding:** <br/>
  > A subclass can provide a specific implementation for a method that is already defined in its superclass. This is known as method overriding. <br/>
  > The `@Override` annotation is often used to indicate that a method is being overridden.

**Example:** Metod Overriding
```java
class Animal {
    // Method in superclass
    void eat() {
        System.out.println("This animal eats food.");
    }

    void sleep() {
        System.out.println("This animal sleeps.");
    }
}

// Subclass
class Dog extends Animal {
    // Additional method in subclass
    void bark() {
        System.out.println("The dog barks.");
    }

    // Overriding method
    @Override
    void eat() {
        System.out.println("The dog eats dog food.");
    }
}
```


**Example:** use inheritance from animal class
```java
public class Animal {
    void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

public class Dog extends Animal {
    void walk() {
        System.out.println("Dog walks");
    }
}

Dog myDog = new Dog();
myDog.makeSound(); //output : Animal makes a sound
```

### Super keyword
> In Java, the super keyword is used to refer to members (methods, constructors, and instance variables) of the superclass (parent class) from within a subclass (child class). <br/>
> It allows the subclass to access and override features from its parent class while retaining the ability to refer to the original versions.
**Using super to Call a Superclass Method**
```Java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
    
    void callSuperMethod() {
        super.sound();  // Calls the sound() method from Animal
    }
}
```
**Using super() to Call a Superclass Constructor**
```Java
class Animal {
    Animal() {
        System.out.println("Animal constructor called");
    }
    
    Animal(String type) {
        System.out.println("Animal is a " + type);
    }
}

class Dog extends Animal {
    Dog() {
        super("Dog");  // Calls the Animal(String) constructor
        System.out.println("Dog constructor called");
    }
}
```

**Using super to Access Superclass Fields**
```Java
class Animal {
    String name = "Animal";
}

class Dog extends Animal {
    String name = "Dog";
    
    void printNames() {
        System.out.println(name);        // Prints: Dog (child class variable)
        System.out.println(super.name);  // Prints: Animal (superclass variable)
    }
}
```
## Polymorphism
> - It allows objects to be treated as instances of their parent class rather than their actual class. <br/>

### Compile-Time Polymorphism (Static Polymorphism)
> **Method Overloading:** multiple methods in the same class have the same name but different parameter lists.<br/<

### Run-Time Polymorphism (Dynamic Polymorphism)

> **Method Overriding:** a subclass provides a specific implementation of a method that is already defined in its superclass.<br/>
> The method to be called is determined at runtime based on the object's actual class.

**Example:**  Run-Time Polymorphism

```java
// Superclass
class Animal {
    void makeSound() {
        System.out.println("Some sound");
    }
}
```
```java
// Subclass
class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Bark");
    }
}
```
```java
// Another subclass
class Cat extends Animal {
    @Override
    void makeSound() {
        System.out.println("Meow");
    }
}
```
```java
public class Main {
    public static void main(String[] args) {
        Animal myAnimal;

        myAnimal = new Dog();
        myAnimal.makeSound();  // Output: Bark

        myAnimal = new Cat();
        myAnimal.makeSound();  // Output: Meow
    }
}
```

## Abstraction
> It's the process of hiding the complex implementation details and showing only the essential features of the object.<br/>
> This is achieved in Java through abstract classes and interfaces.

### Abstract Classes
> - classes that cannot be instantiated on their own and are meant to be extended by other classes.<br/>
> - They are used to provide a common definition for a group of related classes and to establish a base class with common methods and fields, some of which may be abstract (i.e.,   c 
    methods that do not have an implementation).<br/>

#### Abstract Methods 
> - Abstract classes can contain abstract methods, which are methods without an implementation. Subclasses must provide an implementation for these methods.<br/>
  > Syntax: ```java abstract void methodName(); ```<br/>


> - Abstract classes can also contain concrete (non-abstract) methods with an implementation. These methods can be used by subclasses directly.<br/>
> - **Constructors:** <br/>
>   Abstract classes can have constructors, which can be called from constructors of subclasses.<br/>
> - **Fields:** <br/>
>   Abstract classes can have fields (variables), including static and instance fields, and these can be used by subclasses.<br/>
> **Example of static field :**  ```java static int totalVehicles = 0; ```
> - **Inheritance:** <br/>
>   A concrete subclass that extends an abstract class must provide implementations for all abstract methods in the abstract class.<br/>

# Interfaces
> - Interface is a reference type, similar to a class, that can contain only abstract methods (methods without a body) and constants (public, static, and final variables).<br/> 
> - It is a way to define a contract that other classes can implement.<br/>
> - Interfaces are used to specify a set of methods that implementing classes must provide, without dictating how those methods should be implemented. <br/>

> **Abstract Methods:** <br/>
> - Interfaces can contain abstract methods, which are methods without a body (i.e., they are declared but not implemented). <br/>
> - Classes that implement the interface must provide concrete implementations of these methods. <br/>
```java
public interface Animal {
    void sound();  // Abstract method
    void eat();    // Abstract method
}
```

> **No Instance Variables:** <br/>
> - Interfaces cannot have instance variables (like: ```java private String brand; ``` ).<br/>
> - They can only have constants, which are public, static, and final by default. <br/>
```java
public interface Constants {
    // A constant variable in an interface
    int MAX_SPEED = 120;  // This is implicitly public, static, and final
}
```

> **Multiple Inheritance:**<br/>
> - A class in Java can implement multiple interfaces. This allows a class to inherit the abstract methods from multiple interfaces, providing a form of multiple inheritance. <br/>

> **Polymorphism:** <br/>
> - Interfaces enable polymorphism. You can write methods that accept interface types as parameters, allowing for flexibility and the ability to pass objects of any class that 
    implements the interface.<br/>

```java
public class Dog implements Animal {
    @Override
    public void makeSound() {
        System.out.println("The dog barks");
    }
}

// Cat.java
public class Cat implements Animal {
    @Override
    public void makeSound() {
        System.out.println("The cat meows");
    }
}
```

```java
public class Main {

    // Method that takes an Animal interface type
    public static void animalSound(Animal animal) {
        animal.makeSound();  // Polymorphic call
    }

    public static void main(String[] args) {
        // Create instances of Dog and Cat
        Animal myDog = new Dog();
        Animal myCat = new Cat();

        // Use polymorphism to call the method
        animalSound(myDog);  // Output: The dog barks
        animalSound(myCat);  // Output: The cat meows
    }
}
```

# Exception Handling and Assertions
> When executing Java code, different errors can occur, Java will throw an exception<br/>

## Types of Exception

### Built-in Exceptions
> Built-in exceptions are the exceptions that are available in Java libraries. These exceptions are suitable to explain certain error situations.<br/>
> - `Checked Exceptions` : Checked exceptions are called `compile-time exceptions` because these exceptions are checked at compile-time by the compiler.<br/>
> - `Unchecked Exceptions` : The unchecked exceptions are just opposite to the checked exceptions. they are a `runtime exceptions` The compiler will not check these exceptions at compile time. In simple words, if a program throws an unchecked exception, and even if we didn’t handle or declare it, the program would not give a compilation error.<br/>

### User-Defined Exceptions
> Sometimes, the built-in exceptions in Java are not able to describe a certain situation.<br/>
> In such cases, users can also create exceptions, which are called ‘user-defined Exceptions’. <br/>


## Java try and catch
> - The `try` statement allows you to define a block of code to be tested for errors while it is being executed.<br/>
> - The `catch` statement allows you to define a block of code to be executed, if an error occurs in the try block<br/>

## Java Finally keyword
> The finally statement lets you execute code, after try...catch, regardless of the result<br/>

**Example of try catch blok**<br/>
```java
public class Main {
  public static void main(String[] args) {
    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    } finally {
      System.out.println("The 'try catch' is finished.");
    }
  }
}
```

## The throw keyword
> The throw statement allows you to create a custom error.<br/>
```java
public class Main {
  static void checkAge(int age) {
    if (age < 18) {
      throw new ArithmeticException("Access denied - You must be at least 18 years old.");
    }
    else {
      System.out.println("Access granted - You are old enough!");
    }
  }

  public static void main(String[] args) {
    checkAge(15); // Set age to 15 (which is below 18...)
  }
}
```
## The Throws keyword
> - Used to indicate what exception type may be thrown by a method<br/>
> - It Can declare multiple exceptions<br/>
> - throws is followed by a class and used with the method signature<br/>
```java
static void checkAge(int age) throws ArithmeticException {
  if (age < 18) {
    throw new ArithmeticException("Access denied - You must be at least 18 years old.");
  }
  else {
    System.out.println("Access granted - You are old enough!");
  }
```


# String APIs
> - In Java, string is an object that represents a sequence of characters.<br/>
> - The `java.lang.String` class is used to create a string object.<br/>
> - There are two ways to create String object: <br/> `By string literal` OR `By new keyword` <br/>
> - Strings are `Immutable`: Strings in Java are immutable, meaning once created, their values cannot be changed. Any modification to a string creates a new string.<br/>
> - `String Pool`: Java maintains a special memory area called the "string pool" for string literals to optimize memory use and improve performance.<br/>

## Creating Strings
### Creating String object with String Literal
> - Each time you create a string literal, the JVM checks the "string constant pool" first.<br/>
> - If the string already exists in the pool, a reference to the pooled instance is returned.<br/>
> - If the string doesn't exist in the pool, a new string instance is created and placed in the pool.<br/>
```java
String s1="Welcome";  
String s2="Welcome";//It doesn't create a new instance  
```
> - In the above example, only one object will be created.<br/>
> - Firstly, JVM will not find any string object with the value "Welcome" in string constant pool that is why it will create a new object.<br/>
> - After that it will find the string with the value "Welcome" in the pool, it will not create a new object but will return the reference to the same instance.<br/>

### Creating String object with new keyword
> -This method creates a new String object in the heap memory, even if an identical string already exists in the string pool. <br/>

```java
 String str1 = "Hello";                // Stored in string pool
 String str2 = new String("Hello");    // New object in the heap
 String str3 = new String("Hello");    // Another new object in the heap
        
 System.out.println(str1 == str2);     // false, different memory locations
 System.out.println(str2 == str3);     // false, different objects in the heap
 System.out.println(str1.equals(str2)); // true, contents are identical
```

## Java String class methods
#### Length
```java 
int length = str.length();
```

#### Character at a Specific Index
```java 
char ch = str.charAt(0);
```

#### Extracting characters frm index to another
```java 
String sub = str.substring(1, 4); // Extracts characters from index 1 to 3
```

#### Concatenation
```java 
String newStr = str.concat(" World");
// or simply using + operator
String newStr = str + " World";
```

#### Equals and Comparison
```java
boolean isEqual = str.equals("Hello"); // checks exact match
boolean isEqualIgnoreCase = str.equalsIgnoreCase("hello"); // ignores case
```

#### Find Character or Substring Position
```java
int index = str.indexOf('e');  // Finds index of first occurrence of 'e'
int lastIndex = str.lastIndexOf("Hello");
```

#### Replacing Characters or Substrings
```java
String replacedStr = str.replace('l', 'p'); // replaces 'l' with 'p'
String replacedStrAll = str.replaceAll("Hello", "Hi");
```

#### Uppercase and Lowercase
```java
String upper = str.toUpperCase();
String lower = str.toLowerCase();
```

#### Trimming Whitespace
```java
String trimmedStr = str.trim();
```

#### Empty check 
```java
boolean isEmpty = str.isEmpty();
boolean isBlank = str.isBlank();  // Checks if it's empty or only whitespace
```

#### Starts and Ends With
```java
boolean startsWith = str.startsWith("Hello");
boolean endsWith = str.endsWith("World");
```

#### Join multiple strings with a delimiter
```java
String joined = String.join(", ", "A", "B", "C"); // "A, B, C"
```

#### Value of Other Data Types
```java
String fromInt = String.valueOf(42);      // Converts int to string
String fromChar = String.valueOf('A');    // Converts char to string
```
