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
      - [Class variable](#Class-variable)
      - [Instance variable](#Instance-variable)
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
  - [Creating Strings](#Creating-Strings)
  - [Java String class methods](#Java-String-class-methods)
- [Iterators](#Iterators)
- [Collections](#Collections)
  - [List](#List)
    - [Commonly Used List Implementations](#Commonly-Used-List-Implementations)
      - [ArrayList](#ArrayList)
      - [LinkedlList](#LinkedList)
      - [Vector](#Vector)
        - [Stack](#Stack)
    - [When to use each one](#When-to-use-each-one)
  - [Queue](#Queue)
    - [Commonly Used List Implementations](#Commonly-Used-List-Implementations)
      - [PriorityQueue](#PriorityQueue)
      - [LinkedList](#LinkedList)
      - [PriorityBlockingQueue](#PriorityBlockingQueue)
    - [When to use each one](#When-to-use-each-one)
  - [Set](#Set)
  - [Commonly Used List Implementations](#Commonly-Used-List-Implementations)
    - [HashSet](#HashSet)
    - [LinkedHashSet](#LinkedHashSet)
    - [SortedSet](#SortedSet)
      - [TreeSet](#TreeSet)
    - [When to use each one](#When-to-use-each-one)
# History
> Java is a high-level, class-based, object-oriented programming language that was first released by Sun Microsystems in 1995. <br/>
> The company Oracle then acquired Sun Microsystems in 2009, which explains why this language now belongs to Oracle.

# Java JDK JRE JVM
<img src="https://github.com/user-attachments/assets/7e271bd0-0132-4e63-9b6d-cdc64dfda944" >
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
> - It is a group of related types of classes, interfaces, etc providing access to protection and namespace management.<br/>
> - Packages are used in Java in order to prevent naming conflicts, control access, and make searching/locating and usage of classes, interfaces, etc easier.<br/>
> - Packages avoid name clashes.<br/>
> - The Package provides easier access control.<br/>
> - It is easier to locate the related classes.<br/>
> - Types of packages are there in Java: **User-defined packages** and **Build In packages**.<br/>

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
#### Class variable
> - Class Variable (static variable) can be declared anywhere at the class level using the keyword static.<br/>
> - These variables can be shared by all class members.<br/>
#### Instance variable
> - Class variable can have distinct values among several objects.<br/>
> - The contents of an instance variable are completely independent of one object instance from another because they are related to a specific object instance of the class.<br/>
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

## StringBuilder
> - StringBuilder in Java is a mutable sequence of characters, meaning it can be modified without creating new objects.<br/>
> - It’s part of the `java.lang` package and is particularly useful when you need to perform many modifications on a string (e.g., appending, inserting, deleting characters).<br/>
> - StringBuilder is not synchronized, so it should only be used in single-threaded environments.<br/>

### Creating a StrinBuilder
```java
StringBuilder sb = new StringBuilder();             // Empty StringBuilder
StringBuilder sb2 = new StringBuilder("Hello");     // Initialize with "Hello"
StringBuilder sb3 = new StringBuilder(50);          // Initial capacity of 50 characters
```

## StringBuffer
> - StringBuffer is a class in Java used to create mutable (modifiable) strings, similar to StringBuilder.<br/>
> - The key difference is that StringBuffer is thread-safe because all its methods are synchronized, making it suitable for use in multithreaded environments.<br/>
```java
StringBuffer sb = new StringBuffer();               // Empty buffer
StringBuffer sb2 = new StringBuffer("Hello");       // Initialize with "Hello"
StringBuffer sb3 = new StringBuffer(50);            // Buffer with initial capacity of 50 characters
```
# Iterators
> - There are three cursors in Java : **Iterator**, **Enumeration**, and **ListIterator** <br/>

## Iterator
> - Iterators in Java are used in the **Collection framework** to retrieve elements one by one.<br/>
> - It is a universal iterator as we can apply it to any Collection object.<br/>
> - By using Iterator, we can perform both read and remove operations.<br/>
> - It is an improved version of Enumeration with the additional functionality of removing an element.<br/>
> - The iterator is the only cursor available for the entire collection framework.<br/>
> - An iterator object can be created by calling the **iterator()** method present in the Collection interface.<br/>

### Syntax
Iterator itr = c.iterator();

### Methods
**hasNext()**: Returns true if the iteration has more elements.<br/>
**next()**: Returns the next element in the iteration. It throws NoSuchElementException if no more element is present.<br/>
**remove()**: Removes the next element in the iteration. This method can be called only once per call to next().<br/>

## Enumeration
> - It is an interface used to get elements of legacy collections(Vector, Hashtable).<br/>
> - Enumeration is the first iterator present from JDK 1.0, rests are included in JDK 1.2 with more functionality.<br/>
> - Enumerations are also used to specify the input streams to a SequenceInputStream.<br/>
> - We can create an Enumeration object by calling **elements()** method of the vector class on any vector object <br/>

### Syntax

### Methods

# Collections
> - The Java Collections Framework (JCF) is part of the java.util package and includes several interfaces, classes, and methods to manage and manipulate collections of data.<br/>
> - Collections are widely used because they simplify and streamline working with groups of objects.<br/>
> - It has subinterfaces like `List`, `Set`, and `Queue`<br/>
<img src="https://github.com/user-attachments/assets/5848d904-e656-45ff-8eed-5215184ca8de" >
## List
> - List is an interface that represents an ordered collection (also known as a sequence) of elements.<br/>
> - It is part of the Java Collections Framework and provides a way to store and manipulate a sequence of objects.<br/>
> - The List interface provides various methods for adding, removing, and accessing elements.<br/>

### Commonly Used List Implementations

#### ArrayList
> - Uses a resizable array to store elements.<br/>
> - Allows fast random access (get/set) due to array-based structure.<br/>
> - Slower at insertions and deletions in the middle, as elements need to be shifted.<br/>
> - Not synchronized, meaning it's not thread-safe.<br/>

```java
// Creating an ArrayList of String type
ArrayList<String> fruits = new ArrayList<>();

// Adding elements to the ArrayList
fruits.add("Apple");
fruits.add("Banana");
fruits.add("Cherry");

// Adding an element at a specific index
fruits.add(1, "Mango");  // Now, "Mango" is at index 1

// Accessing an element by index
String firstFruit = fruits.get(0);
System.out.println("First fruit: " + firstFruit);  // Output: Apple

// Updating an element at a specific index
fruits.set(2, "Orange");  // Changes "Banana" to "Orange" at index 2

// Removing an element by index
fruits.remove(3);  // Removes the element at index 3 ("Cherry")

// Checking if a specific element is in the ArrayList
boolean hasMango = fruits.contains("Mango");
System.out.println("Does the list contain Mango? " + hasMango);  // Output: true

// Getting the size of the ArrayList
int size = fruits.size();
System.out.println("Size of the list: " + size);  // Output: 3

// Iterating over the ArrayList and printing each element
System.out.println("Fruits in the list:");
for (String fruit : fruits) {
  System.out.println(fruit);
}

// Clearing all elements in the ArrayList
fruits.clear();
```

#### LinkedList
> - It is an implementation of the List and Deque interfaces.<br/>
> - Doubly Linked Structure: The LinkedList is implemented as a doubly linked list, meaning each element (node) contains a link to both the previous and the next node.<br/>
> - Sequential Access: Unlike arrays or ArrayList, accessing a specific element in a LinkedList requires traversing the list from the beginning or the end.<br/>
> - Fast Insertion and Removal: LinkedList provides efficient insertion and deletion when adding or removing elements from the beginning, end, or middle of the list.<br/>
> - It is not synchronised that means it is not Thread safe.<br/>
> - We can create a synchronised LinkedList using Collections.synchronizedList() method.<br/>

```java
LinkedList<Integer> list = new LinkedList<>();
// Adding elements
list.add("A");
list.addFirst("Start");
list.addLast("End");
list.add(3, "Salma");

// Accessing elements
System.out.println("First element: " + list.getFirst());
System.out.println("Last element: " + list.getLast());

// Removing elements
list.removeFirst();
list.removeLast();
//from LinkedList to Array
Integer[] numbers = new Integer[numbersList.size()];		
numbers = numbersList.toArray(numbers);
```

#### Vector
> - Thread Safety: All methods of Vector are synchronized, making it safe for use in multi-threaded applications.<br/>
> - Indexed Access: You can access elements by their index.<br/>

```java
Vector<String> fruits = new Vector<>();
// Adding elements to the Vector
fruits.add("Apple");
fruits.add(1, "Grapes"); // Insert "Grapes" at index 1

// Accessing elements
System.out.println("First fruit: " + fruits.get(0));

// Removing an element
fruits.remove("Apple");
```
##### Stack
> - Stack is a subclass of Vector. This means Stack inherits all the properties and methods of Vector, including those for manipulating elements and managing capacity.<br/>
> - data structure that follows the Last-In-First-Out (LIFO) principle, where the last element added is the first to be removed.<br/>
> - This structure is useful for scenarios where you need to process items in reverse order of their arrival.<br/>

```java
Stack<Integer> stack = new Stack<>();
// Push elements onto the stack
stack.push(10);
stack.push(20);
stack.push(30);

// Peek at the top element
System.out.println("Top element is: " + stack.peek()); // Output: 30

// Pop elements from the stack
System.out.println("Popped: " + stack.pop()); // Output: 30
System.out.println("Popped: " + stack.pop()); // Output: 20

// Check if the stack is empty
System.out.println("Is the stack empty? " + stack.isEmpty()); // Output: false
```

### When to use each one
#### ArrayList
> - Allows fast random access using indices (O(1) complexity for get and set operations).<br/>
> - Slower for insertion and deletion, especially in the middle of the list, as elements may need to be shifted (O(n) complexity).<br/>
> - Not synchronized, so it’s not thread-safe but faster in single-threaded contexts.<br/>

When to Use: <br/>

> - You primarily need fast access to elements by index.<br/>
> - Your list operations are mostly get and set.<br/>
> - Thread safety is not required.<br/>
> - Examples: Maintaining a list of items, where you often retrieve elements but rarely modify the list.<br/>

#### LinkedList
> - Implemented as a doubly linked list.<br/>
> - Insertion and deletion at both ends are fast (O(1) complexity at head and tail).<br/>
> - Slower random access (O(n) complexity) as it requires traversal from the beginning.<br/>
> - Not synchronized, so it’s not thread-safe.<br/>

When to Use:

> - You need to frequently add or remove elements at the beginning, end, or middle of the list.<br/>
> - Accessing elements by index is not a frequent operation.<br/>
> - Thread safety is not a concern.<br/>
> - Examples: Implementing queues or deques, where elements are frequently added or removed from both ends.<br/>

#### Vector
> -Backed by a dynamically resizing array.<br/>
> Similar to ArrayList in terms of fast access and slower insertion/deletion in the middle.<br/>
> Synchronized by default, which makes it thread-safe but can lead to performance bottlenecks due to synchronization overhead.<br/>

When to Use:

> - You need a thread-safe list for a multi-threaded environment.<br/>
> - Alternatives like Collections.synchronizedList(new ArrayList<>()) or CopyOnWriteArrayList are unsuitable.<br/>
> - Examples: Legacy applications requiring thread safety, or when migrating older codebases that rely on Vector.<br/>


## Queue
> - Queue interface is a subtype of the Collection interface and represents a collection of elements in a specific order.<br/>
> - The Queue is used to insert elements at the end of the queue and removes from the beginning of the queue. It follows FIFO concept.<br/>
> - The Queue interface is implemented by several classes in Java, including LinkedList, ArrayDeque, and PriorityQueue.<br/>
> - **add(element)** : Adds an element to the rear of the queue. If the queue is full, it throws an exception.<br/>
> - **offer(element)** : Adds an element to the rear of the queue. If the queue is full, it returns false.<br/>
> - **remove()** : Removes and returns the element at the front of the queue. If the queue is empty, it throws an exception., we can add the index of element to remove. <br/>
> - **poll()** : Removes and returns the element at the front of the queue. If the queue is empty, it returns null.<br/>
> - **element()** : Returns the element at the front of the queue without removing it. If the queue is empty, it throws an exception.<br/>
> - **peek()** : Returns the element at the front of the queue without removing it. If the queue is empty, it returns null.<br/>
> - **size()** : This method is used to return the size of the queue.<br/>

### Commonly Used List Implementations

#### PriorityQueue
> - PriorityQueue orders elements based on priority <br/>
> - **Natural Ordering** : If elements are Comparable, PriorityQueue will order them in their natural order (e.g., integers in ascending order).
> - **Custom Comparator** : You can specify a custom Comparator at the time of PriorityQueue creation to define custom ordering, such as descending or based on a specific field in a custom class.<br/>
> - It’s based on a heap data structure, making insertion and removal efficient <br/>

```java
//Creating a PriorityQueue
PriorityQueue<Integer> queue = new PriorityQueue<>(); // Natural ordering (ascending)
//Adding elements to the queue
queue.add(30);
queue.add(10);
queue.add(20);
//It will order them (10 then 20 then 30) automatiqly
while (!queue.isEmpty()) {
  System.out.println(queue.poll()); // Output: 10, 20, 30
}
//return and remove the firt element
System.out.println(queue.poll());
//return without removing it
System.out.println(queue.peek());
//Removing element
queue.remove(10);
//Iterator
Iterator iterator = pq.iterator();
while (iterator.hasNext()) {
  System.out.print(iterator.next() + " ");
}
```

#### LinkedList

> - With a Queue, you generally interact with elements only at the head (for removal) or the tail (for addition) without accessing elements by index.<br/>
> - LinkedList is not thread-safe.<br/>

```java
Queue<String> queue = new LinkedList<>();
queue.offer("first");
queue.offer("second");
queue.offer("third");
System.out.println(queue.poll());  // Output: first (FIFO)
System.out.println(queue.peek());  // Output: second
```

#### PriorityBlockingQueue

> - The elements are ordered based on their priority, with the smallest (or highest priority) elements appearing at the head of the queue.<br/>
> - You can specify a custom ordering by passing a Comparator when creating the queue.<br/>
> - PriorityBlockingQueue is technically **unbounded**, meaning it does not have a maximum size, unlike other blocking queues like ArrayBlockingQueue.<br/>
> - PriorityBlockingQueue is designed for concurrent access, so multiple threads can safely add or remove elements from the queue without explicit synchronization.<br/>

```java
// blocking queue
Queue<Integer> pbq = new PriorityBlockingQueue<Integer>();
// Adding items to the pbq
pbq.add(10);
pbq.add(20);
pbq.add(15);
// Printing the top element
System.out.println(pbq.peek());
// Printing the top element and removing it
System.out.println(pbq.poll());
// Printing the top element again
System.out.println(pbq.peek());
```

### When to use each one

> - Use LinkedList when simple queue or list behavior is needed without concurrent access.<br/>
> - Use PriorityQueue in single-threaded contexts for tasks with varying priorities.<br/>
> - Use PriorityBlockingQueue in multi-threaded applications where priority ordering and safe concurrent access are required.<br/>

### Deque




## Set
> - The Set Interface is present in java.util package and extends the Collection interface.<br/>
> - It is an unordered collection of objects in which duplicate values cannot be stored.<br/>
> - This interface contains the methods inherited from the Collection interface and adds a feature that restricts the insertion of the duplicate elements.<br/>
> - There are two interfaces that extend the set implementation namely .<br/>
> - Commun implementations of Set: `HashSet`, `LinkedHashSet`.<br/>
> - Interface that extends from Set: `SortedSet`, and the implementation of SortedSet: `TreeSet`.<br/>


### Commonly Used List Implementations

#### HashSet 
> - The objects are inserted based on their hashcode.<br/>
> - This class also allows the insertion of NULL elements.<br/> 

```java
// Creating object of Set of type String
Set<String> h = new HashSet<String>();
// Adding elements into the HashSet
h.add("India");
h.add("Australia");
h.add("South Africa");
// Adding the duplicate element
h.add("India");
// Displaying the HashSet
System.out.println(h);
// --> [South Africa, Australia, India]
// Removing items from HashSet
h.remove("Australia");
// Iterating over hash set items
Iterator<String> i = h.iterator();
// It holds true till there is a single element remaining in the object
while (i.hasNext())
  System.out.println(i.next());
}
```

#### LinkedHashSet
> - No Duplicates: Like other Set implementations, LinkedHashSet does not allow duplicate elements.<br/>
> - Insertion Order: Maintains the order in which elements are added to the set.<br/>
> - Faster Access: Has similar performance to HashSet for most operations, with O(1) average complexity for adding, removing, and checking for elements.<br/>

```java
Set<String> lh = new LinkedHashSet<String>();
// Adding elements into the LinkedHashSet
lh.add("India");
lh.add("Australia");
lh.add("South Africa");
// Adding the duplicate element
lh.add("India");
// Displaying the LinkedHashSet
System.out.println(lh);
// --> [India, Australia, South Africa]
// Removing items from LinkedHashSet
// using remove()
lh.remove("Australia");
// Iterating over linked hash set items
Iterator<String> i = lh.iterator();
while (i.hasNext())  System.out.println(i.next());
```

#### SortedSet
> - The SortedSet interface is present in java.util package extends the Set interface present in the collection framework.<br/>
> - This interface contains the methods inherited from the Set interface and adds a feature that stores all the elements in this interface to be stored in a sorted manner (ascending order).<br/>
> - the implementation of SortedSet: `TreeSet`.<br/>

##### TreeList
```java
Set<String> ts = new TreeSet<String>();
// Adding elements into the TreeSet
ts.add("India");
ts.add("Australia");
ts.add("South Africa");
// Adding the duplicate element
ts.add("India");
// Displaying the TreeSet
System.out.println(ts);
// --> [Australia, India, South Africa]
// Removing items from TreeSet
ts.remove("Australia");
// Iterating over Tree set items
Iterator<String> i = ts.iterator();
while (i.hasNext())
  System.out.println(i.next());
}
```

### When to use each one
> - HashSet: when you need a list with unique values and with a hashcode order.<br/>
> - LinkeHashSet: when you need a list with unique values and wiht the same order that inserted in.<br/>
> - TreeSet: when you need a list with unique value and an order (ascending/ descending).<br/>










