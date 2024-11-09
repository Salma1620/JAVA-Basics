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
  - [StringBuilder](#StringBuilder)
    - [Creating a StrinBuilder](#Creating-a-StrinBuilder)
  - [StringBuffer](#StringBuffer)
    - [Creating a StrinBuilder](#Creating-a-StrinBuilder)
- [Iterators](#Iterators)
  - [Iterator](#Iterator)
  - [Enumeration](#Enumeration)
- [Collections](#Collections)
  - [List](#List)
    - [Commonly Used List Implementations](#Commonly-Used-List-Implementations)
      - [ArrayList](#ArrayList)
      - [LinkedlList](#LinkedList)
      - [Vector](#Vector)
        - [Stack](#Stack)
    - [When to use List Implementations](#When-to-use-List-Implementations)
  - [Queue](#Queue)
    - [Commonly Used Queue Implementations](#Commonly-Used-Queue-Implementations)
      - [PriorityQueue](#PriorityQueue)
      - [LinkedList](#LinkedList)
      - [PriorityBlockingQueue](#PriorityBlockingQueue)
    - [When to use Queue Implementations](#When-to-use-Queue-Implementations)
  - [Set](#Set)
    - [Commonly Used Set Implementations](#Commonly-Used-Set-Implementations)
      - [HashSet](#HashSet)
      - [LinkedHashSet](#LinkedHashSet)
      - [SortedSet](#SortedSet)
        - [TreeSet](#TreeSet)
    - [When to use Set Implementations](#When-to-use-Set-Implementations)
  - [Map](#Map)
    - [Commonly Used Map Implementations](#Commonly-Used-Map-Implementations)
      - [HashMap](#HashMap)
      - [LinkedHashMap](#LinkedHashMap)
      - [SortedMap](#SortedMap)
        - [TreeMap](#TreeMap)
    - [When to use Map Implementations](#When-to-use-Map-Implementations)
- [Threads](#Threads)
  - [The Concept Of Multitasking](#The-Concept-Of-Multitasking)
    - [Process-Based Multitasking (Multiprocessing)](#Process-Based-Multitasking-(Multiprocessing))
    - [thread-Based Multitasking (Multithreading)](#thread-Based-Multitasking-(Multithreading))
      - [Life Cycle Of Thread](#Life-Cycle-Of-Thread)
- [JDBC (Java Database Connectivity)](#JDBC (Java Database-Connectivity))
- [Streams API](#Streams-API)
  - [Create Java Stream](#Create-Java-Stream)
  - [Different Operations On Streams](#Different-Operations-On-Streams)
    - [Intermediate Operations](#Intermediate-Operations)
    - [Terminal operations](#Terminal-operations)
- [LTS versions](#LTS-versions)
# History
> Java is a high-level, class-based, object-oriented programming language that was first released by Sun Microsystems in 1995. <br/>
> The company Oracle then acquired Sun Microsystems in 2009, which explains why this language now belongs to Oracle.

# Java JDK JRE JVM
<img src="https://github.com/user-attachments/assets/7e271bd0-0132-4e63-9b6d-cdc64dfda944" >

## JVM (Java Virtual Machine)
> - the core of the Java programming language. It is responsible for executing Java bytecode, which is the intermediate code generated after compiling a Java program.<br/>
> - The JVM makes Java platform-independent by allowing the same Java bytecode to run on any device or operating system that has a compatible JVM.<br/>
> - Loads Bytecode: The JVM loads the compiled .class files into memory.<br/>
> - The ClassLoader in Java is a component of the JVM responsible for dynamically loading classes at runtime. It converts .class files (compiled bytecode) into usable Java objects within the program.<br/>
> - Execution: It executes the bytecode line by line using an interpreter or compiles it to native machine code using the Just-In-Time (JIT) compiler for performance.<br/>
> - Memory Management: The JVM manages memory allocation and garbage collection to ensure efficient use of resources.<br/>

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
<img src="https://github.com/user-attachments/assets/dd6d2e3f-0591-4d37-a0ca-a132d562b8df" > <br/>
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

#### Keyword Final
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

#### Keyword Static
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

### Example
```java
// creating a linkedlist
List<String> cities = new LinkedList<>(); 
// adding elements to the list
cities.add("G-1"); 
cities.add("G-2"); 
cities.add("G-3"); 
// creating iterator for the list
Iterator<String> citiesIterator = cities.iterator();
// is it a element next to the iterator
citiesIterator.hasNext();
// moving the iterator to the next element
citiesIterator.next();
```

## Enumeration
> - It is an interface used to get elements of legacy collections(Vector, Hashtable).<br/>
> - Enumeration is the first iterator present from JDK 1.0, rests are included in JDK 1.2 with more functionality.<br/>
> - Enumerations are also used to specify the input streams to a SequenceInputStream.<br/>
> - We can create an Enumeration object by calling **elements()** method of the vector class on any vector object <br/>

### Syntax
```java
Enumeration e = v.elements();
```

### Methods
**hasMoreElements()**: This method tests if this enumeration contains more elements or not.<br/>
**nextElement()**: This method returns the next element of this enumeration. It throws NoSuchElementException if no more element is present<br/>

### Example
```java
// Creating a vector object
Vector v = new Vector();
// Iterating over vector object
for (int i = 0; i < 10; i++)   v.addElement(i);
// Printing elements in vector object
System.out.println(v);
// At beginning e(cursor) will point to index just before the first element in v
Enumeration e = v.elements();
// Checking the next element availability where condition holds true till there is a single element remaining in the List
while (e.hasMoreElements()) {
  // Moving cursor to next element
  int i = (Integer)e.nextElement();
  // Print above elements in object
  System.out.print(i + " ");
}
```

### limitations of enumeration
> - Enumeration is for legacy classes(Vector, Hashtable) only. Hence it is not a universal iterator.<br/>
> - Remove operations can’t be performed using Enumeration.<br/>
> - Only forward direction iterating is possible.<br/>

## ListIterator
> - It is only applicable for List collection implemented classes like ArrayList, LinkedList, etc.<br/>
> - It provides bi-directional iteration.<br/>
> - ListIterator must be used when we want to enumerate elements of List.<br/>
> - This cursor has more functionality(methods) than iterator.<br/>
> - ListIterator object can be created by calling listIterator() method present in the List interface.<br/>

### Syntax
```java
ListIterator ltr = l.listIterator();
```

### Methods

**Forward direction:** <br/>
> - hasNext(): Returns true if the iteration has more elements<br/>
> - next(): Same as next() method of Iterator. Returns the next element in the iteration.<br/>
> - nextIndex(): Returns the next element index or list size if the list iterator is at the end of the list.<br/>

**Backward direction:** <br/>
> - hasPrevious(): Returns true if the iteration has more elements while traversing backward.<br/>
> - previous(): Returns the previous element in the iteration and can throw NoSuchElementException if no more element present.<br/>
> - previousIndex(): Returns the previous element index or -1 if the list iterator is at the beginning of the list.<br/>

**Other metods:** <br/>
> - remove(): Same as remove() method of Iterator. Removes the next element in the iteration.<br/>
> - set(Object obj): Replaces the last element returned by next() or previous() with the specified element.<br/>
> - add(Object obj): Inserts the specified element into the list at the position before the element that would be returned by next(). <br/>

### Example
```
// Creating an object of ArrayList class
ArrayList al = new ArrayList();
// Iterating over Arraylist object
for (int i = 0; i < 10; i++)
// Adding elements to the Arraylist object
al.add(i);
// Print and display all elements inside object created above
System.out.println(al);
// At beginning ltr(cursor) will point to index just before the first element in al
ListIterator ltr = al.listIterator();
// Checking the next element availability
while (ltr.hasNext()) {
  //  Moving cursor to next element
  int i = (Integer)ltr.next();
  // Getting even elements one by one
  System.out.print(i + " ");
}
```



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

### When to Use List Implementations

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

### Commonly Used Queue Implementations

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

### When to use Queue Implementations

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


### Commonly Used Set Implementations

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

### When to use Set Implementations
> - HashSet: when you need a list with unique values and with a hashcode order.<br/>
> - LinkeHashSet: when you need a list with unique values and wiht the same order that inserted in.<br/>
> - TreeSet: when you need a list with unique value and an order (ascending/ descending).<br/>


## Map
> - Map Interface is present in java.util package represents a mapping between a key and a value.<br/>
> - Java Map interface is not a subtype of the Collection interface.<br/>
> - Therefore it behaves a bit differently from the rest of the collection types. A map contains unique keys.<br/>
> - Maps are perfect to use for key-value association mapping such as dictionaries.<br/>
> - The maps are used to perform lookups by keys or when someone wants to retrieve and update elements by keys.<br/>
> - A Map cannot contain duplicate keys and each key can map to at most one value.
> - Some implementations allow null key and null values like the `HashMap` and `LinkedHashMap`, but some do not like the `TreeMap`.
> - The order of a map depends on the specific implementations. For example, `TreeMap` and `LinkedHashMap` have predictable orders, while `HashMap` does not.
> - There are two interfaces for implementing Map in Java. They are `Map` and `SortedMap`, and three classes: `HashMap`, `TreeMap`, and `LinkedHashMap`.

### Commonly Used Map Implementations
####  HashMap 
> - This class uses a technique called Hashing.<br/>
> - Hashing is a technique of converting a large String to a small String that represents the same String.<br/>
> - A shorter value helps in indexing and faster searches. Let’s see how to create a map object using this class.<br/>

```java
// Creating an empty HashMap
Map<String, Integer> map = new HashMap<>();
// Inserting entries in the Map using put() method
map.put("vishal", 10);
map.put("sachin", 30);
map.put("vaibhav", 20);
// Iterating over Map
for (Map.Entry<String, Integer> e : map.entrySet())
// Printing key-value pairs
System.out.println(e.getKey() + " " + e.getValue());
```

#### LinkedHashMap
> - LinkedHashMap is just like HashMap with the additional feature of maintaining an order of elements inserted into it.<br/>
> - HashMap provided the advantage of quick insertion, search, and deletion but it never maintained the track and order of insertion which the LinkedHashMap provides where the elements can be accessed in their insertion order.<br/>

```java
Map<String, Integer> map = new LinkedHashMap<>();
// Inserting pair entries in above Map using put() method
map.put("vishal", 10);
map.put("sachin", 30);
map.put("vaibhav", 20);
// Iterating over Map
for (Map.Entry<String, Integer> e : map.entrySet())
// Printing key-value pairs
System.out.println(e.getKey() + " " + e.getValue());
```

### SortedMap
> - SortedMap is an interface that extends Map and guarantees that the map is sorted in ascending order by key.<br/>
> - `TreeMap` is the most commonly used implementation of SortedMap.<br/>


#### TreeMap 
> - TreeMap automatically sorts entries by their natural ordering (if keys implement Comparable) or by a specified comparator (if one is provided).<br/>
> - Null Keys: TreeMap does not allow null keys but does allow null values.<br/>

```java
// Creating a TreeMap which is an implementation of SortedMap
SortedMap<String, Integer> sortedMap = new TreeMap<>();

// Adding key-value pairs to the TreeMap
sortedMap.put("Apple", 10);
sortedMap.put("Banana", 20);
sortedMap.put("Cherry", 15);
sortedMap.put("Date", 25);
sortedMap.put("Fig", 30);

// Displaying the whole map (automatically sorted by key)
System.out.println("Full SortedMap: " + sortedMap);
// --> Full SortedMap: {Apple=10, Banana=20, Cherry=15, Date=25, Fig=30}

// Accessing the first and last keys
System.out.println("First Key: " + sortedMap.firstKey());
System.out.println("Last Key: " + sortedMap.lastKey());
// --> First Key: Apple
       Last Key: Fig

// Getting a head map (all keys less than "Cherry")
SortedMap<String, Integer> headMap = sortedMap.headMap("Cherry");
System.out.println("HeadMap (keys less than 'Cherry'): " + headMap);
// --> HeadMap (keys less than 'Cherry'): {Apple=10, Banana=20}

// Getting a tail map (all keys greater than or equal to "Cherry")
SortedMap<String, Integer> tailMap = sortedMap.tailMap("Cherry");
System.out.println("TailMap (keys greater than or equal to 'Cherry'): " + tailMap);
// --> TailMap (keys greater than or equal to 'Cherry'): {Cherry=15, Date=25, Fig=30}

// Getting a submap (keys from "Banana" to "Fig", excluding "Fig")
SortedMap<String, Integer> subMap = sortedMap.subMap("Banana", "Fig");
System.out.println("SubMap (keys from 'Banana' to 'Fig'): " + subMap);
// --> SubMap (keys from 'Banana' to 'Fig'): {Banana=20, Cherry=15, Date=25}
```

### When to use Map Implementations
> - HasMap: when you don’t need any ordering of keys or values. Ideal for quick lookups and inserts when the order doesn’t matter. <br/>
> - LinkedHashMap: when you need predictable iteration order (insertion order or access order.<br/>
> - TreeMap: when you need a sorted map, either by natural ordering of keys or by a custom comparator. <br>




# Threads

## The Concept Of Multitasking
> - To help users Operating System accommodates users the privilege of multitasking, where users can perform multiple actions simultaneously on the machine.<br/>
> - This Multitasking can be enabled in two ways: `Process-Based Multitasking` and `Thread-Based Multitasking`.<br/>
<img src="https://github.com/user-attachments/assets/84950d32-f71b-4806-a551-f2c99b8dec21" >

### Process-Based Multitasking (Multiprocessing)
> - A process is an independent program in execution with its own memory space and resources, isolated from other processes.<br/>
> - In this type of Multitasking, processes are heavyweight and each process was allocated by a separate memory area.<br/>
> - And as the process is heavyweight the cost of communication between processes is high and it takes a long time for switching between processes as it involves actions such as loading, saving in registers, updating maps, lists, etc. <br/>

### thread-Based Multitasking (Multithreading)
> - Thread: The smallest unit of execution within a process.<br/>
> - Each thread has its own execution path but shares resources like memory with other threads in the same process.<br/>
> - Threads are provided with lightweight nature, and the cost of communication between threads is also low.<br/>
> - Concurrency: The ability of the program to manage multiple threads at the same time, which can improve performance by allowing tasks to run in parallel.<br/>

#### Life Cycle Of Thread
<img src="https://github.com/user-attachments/assets/c938fc54-c8fe-41ee-a805-659599d91c72" >

**1. New State** <br/>
> - By default, a Thread will be in a new state.<br/> 
> - In this state, code has not yet been run and the execution process is not yet initiated. <br/>

**2. Active State** <br/>
> - A Thread that is a new state by default gets transferred to Active state when it invokes the start() method, his Active state contains two sub-states namely: <br/>
> - **Runnable State:**<br/>
> - In This State, The Thread is ready to run at any given time and it’s the job of the Thread Scheduler to provide the thread time for the runnable state preserved threads.<br/>
> - **Running State:**<br/>
> - When The Thread Receives CPU allocated by Thread Scheduler, it transfers from the “Runnable” state to the “Running” state.<br/>
> - And after the expiry of its given time slice session, it again moves back to the “Runnable” state and waits for its next time slice.<br/>

**3. Waiting/Blocked State** <br/>
> - If a Thread is inactive but on a temporary time, then either it is a waiting or blocked state.<br/>
> - For example, if there are two threads, T1 and T2 where T1 needs to communicate to the camera and the other thread T2 already using a camera to scan then T1 waits until T2 Thread completes its work.<br/>
> - At this state T1 is parked in waiting for the state, and in another scenario, the user called two Threads T2 and T3 with the same functionality and both had same time slice given by Thread Scheduler then both Threads T1, T2 is in a blocked state.<br/>
> - When there are multiple threads parked in a Blocked/Waiting state, Thread Scheduler clears Queue by rejecting unwanted Threads and allocating CPU on a priority basis. <br/>

**4. Timed Waiting State** <br/>

> - Sometimes the longer duration of waiting for threads causes starvation.<br/>
> - If we take an example like there are two threads T1, T2 waiting for CPU and T1 is undergoing a Critical Coding operation and if it does not exist the CPU until its operation gets executed then T2 will be exposed to longer waiting with undetermined certainty.<br/>
> - In order to avoid this starvation situation, we had Timed Waiting for the state to avoid that kind of scenario as in Timed Waiting, each thread has a time period for which sleep() method is invoked and after the time expires the Threads starts executing its task. <br/>

**5. Terminated State** <br/>
> - A thread will be in Terminated State, due to the below reasons: <br/>
> - Termination is achieved by a Thread when it finishes its task Normally.<br/>
> - Sometimes Threads may be terminated due to unusual events like segmentation faults, exceptions…etc. and such kind of Termination can be called Abnormal Termination.<br/>
> - A terminated Thread means it is dead and no longer available.<br/>


# JDBC (Java Database Connectivity)
> -JDBC is an API(Application programming interface) used in Java programming to interact with databases.
> The classes and interfaces of JDBC allow the application to send requests made by users to the specified database.

## Components of JDBC
1. **JDBC API:**
> - It provides various methods and interfaces for easy communication with the database.
> - It provides two packages as follows, which contain the java SE and Java EE platforms to exhibit WORA(write once run anywhere) capabilities.
> - The java.sql package contains interfaces and classes of JDBC API.

3. **JDBC Driver manager:**
> - It loads a database-specific driver in an application to establish a connection with a database.
> - It is used to make a database-specific call to the database to process the user request.

4. **JDBC Test suite:**
> - It is used to test the operation(such as insertion, deletion, updation) being performed by JDBC Drivers.

6. **JDBC-ODBC Bridge Drivers:**
> - It connects database drivers to the database.
> - This bridge translates the JDBC method call to the ODBC function call.
> - It makes use of the sun.jdbc.odbc package which includes a native library to access ODBC characteristics.



# Streams API
> - Streams represent a pipeline of data processing steps, designed to operate on sequences of elements.<br/>
> - A Stream doesn’t store data; it provides a way to operate on data sequentially or in parallel.<br/>
> - Streams are immutable. Once a Stream is created, it cannot be modified, and each operation produces a new Stream.<br/>
> - Streams built for processing pipelines, like filtering, mapping, and reducing, through methods like filter, map, and reduce.<br/>

## Create Java Stream
### From a Collection
```java
List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
Stream<String> namesStream = names.stream();
```
`In this example, names is immutable (constant)` <br/>
### From an Array
```java
String[] array = {"A", "B", "C"};
Stream<String> arrayStream = Arrays.stream(array);
```
### Using Stream.of()
```java
Stream<Integer> numberStream = Stream.of(1, 2, 3, 4, 5);
```
### Using Stream.generate()
```java
Stream<Double> randomNumbers = Stream.generate(Math::random);
```
### Using Stream.iterate()
```java
Stream<Integer> evenNumbers = Stream.iterate(0, n -> n + 2).limit(5);
```
### Using Stream.builder()
```java
Stream.Builder<String> builder = Stream.builder();
builder.add("first");
builder.add("second");
builder.add("third");
Stream<String> builtStream = builder.build();
```
### From Primitives (IntStream, LongStream, DoubleStream)
```java
IntStream intStream = IntStream.of(1, 2, 3, 4);
LongStream longStream = LongStream.range(1, 10); // Range 1 to 9
DoubleStream doubleStream = DoubleStream.generate(() -> Math.random());
```


## Different Operations On Streams

### Intermediate Operations
> - Intermediate operations (like filter, map, sorted) are evaluated lazily, meaning they only execute when a terminal operation (like collect, forEach, count) is invoked.<br/>
> - This can improve performance by processing only the necessary elements.<br/>

#### filter()
> Filters elements based on a given condition.<br/>
**Example** <br/>
```java
Stream<Integer> stream = Stream.of(1,2,3,4,5);
Stream<Integer> stream1 = stream.filter(i-> i%2 == 0);
stream1.forEach(System.out::println);
```

#### map()
> Transforms each element of the stream using the provided function. This can be used for mapping values from one type to another. <br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
Stream<Integer> squares = numbers.map(n -> n * n);
squares.forEach(System.out::println); // Output: 1, 4, 9, 16, 25
```

#### sorted()
> Sorts the elements in natural order or based on a custom comparator. <br/>
```java
Stream<Integer> numbers = Stream.of(5, 1, 3, 4, 2);
Stream<Integer> sortedNumbers = numbers.sorted();
sortedNumbers.forEach(System.out::println); // Output: 1, 2, 3, 4, 5
```

#### flatMap()
> it "flattens" the results into a single stream, removing any nested structures that may result from applying the function. <br/>
```java
List<List<Integer>> listOfLists = Arrays.asList(
    Arrays.asList(1, 2),
    Arrays.asList(3, 4),
    Arrays.asList(5, 6)
);
List<Integer> result = listOfLists.stream()
                                  .flatMap(list -> list.stream())  // flatten the List into a single Stream
                                  .collect(Collectors.toList());
// other example
List<String> list = Arrays.asList("hello", "world");
List<String> result = list.stream()
                          .flatMap(s -> Arrays.stream(s.split("")))  // Split each string and flatten it
                          .collect(Collectors.toList());
```

#### peek()
> Allows you to perform an action on each element of the stream without modifying the stream. It's often used for debugging or logging purposes.<br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
numbers.peek(n -> System.out.println("Processing: " + n))
       .filter(n -> n % 2 == 0)
       .forEach(System.out::println); // Output: Processing: 1, 2, Processing: 2, 4
```

#### distinct()
> Removes duplicate elements from the stream. <br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 2, 3, 3, 3, 4);
Stream<Integer> distinctNumbers = numbers.distinct();
distinctNumbers.forEach(System.out::println); // Output: 1, 2, 3, 4
```

#### limit()
> Limits the number of elements in the stream. <br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
Stream<Integer> firstThree = numbers.limit(3);
firstThree.forEach(System.out::println); // Output: 1, 2, 3
```

### Terminal operations
> - terminal operation consumes the stream and produces an outcome (e.g., a value, a collection, or a side-effect).<br/>
> - Once a terminal operation is invoked, the stream is considered consumed, and no further operations can be performed on it.<br/>

#### forEach()
> Used to perform an action for each element of the stream. <br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
numbers.forEach(System.out::println);  // Prints each number
```

#### collect()
> accumulate the elements of the stream into a collection, such as a List, Set, or a Map. <br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
List<Integer> result = numbers.collect(Collectors.toList());  // Collects into a List
System.out.println(result);  // Output: [1, 2, 3, 4, 5]
```
> Other common Collectors are:<br/>
> - Collectors.toSet() – collects into a Set. <br/>
> - Collectors.joining() – concatenates elements into a string.<br/>

#### count()
>  Returns the number of elements in the stream. <br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
long count = numbers.count();  // Counts the number of elements in the stream
System.out.println(count);  // Output: 5
```

#### anyMatch() and allMatch()
> - The anyMatch operation checks if any element of a stream matches a given condition. <br/>
> - The allMatch operation checks if all elements satisfy the given condition. <br/>
> - They return a boolean value indicating the result. <br/>
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);  
// Check if any element is greater than 3  
boolean anyMatch = numbers.stream()  
                                  .anyMatch(n -> n > 3);  
// Check if all elements are greater than 0  
boolean allMatch = numbers.stream()  
                                  .allMatch(n -> n > 0);  
```

#### reduce()
> Combines elements of a stream to produce a single result.<br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4);
int product = numbers.reduce(1, (a, b) -> a * b);
System.out.println(product);  // Output: 24
```

### findFirst() and findAny()
> Returns the first element of the stream or any element. <br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
Optional<Integer> first = numbers.findFirst();  // Finds the first element
first.ifPresent(System.out::println);  // Output: 1
```

#### toArray()
> Collects the elements of the stream into an array.<br/>
```java
Stream<Integer> numbers = Stream.of(1, 2, 3, 4, 5);
Integer[] array = numbers.toArray(Integer[]::new);  // Collects into an array
System.out.println(Arrays.toString(array));  // Output: [1, 2, 3, 4, 5]
``` 

# LTS versions
> Java Long-Term Support (LTS) versions are stable releases that Oracle and other vendors support for an extended period, making them ideal for production environments.<br/>

## Java 8
### Functionnal Interface
> - Functional interfaces are interfaces that have exactly one abstract method. <br/>
> - They are annotated with `@FunctionalInterface`. <br/>

**Example : Functionnal Interface**
```Java
@FunctionalInterface
interface MyInterface {
    void myAbstractMethod(); // This is the single abstract method
}
```

### Lamdba Expression
> - Lambda expression is a powerful feature in Java 8 that allows you to implement the functional interfaces.<br/>
> - They make your code more readable and expressive, especially when working with collections, streams, and functional programming constructs.<br/>

**Example : Lambda Expression**
```Java
// Before Java 8
public class BeforeJava8Example {
    public static void main(String[] args) {
        MyInterface implementation = new MyInterface() {
            @Override
            public void myAbstractMethod() {
                System.out.println("Hello from myAbstractMethod!");
            }
        };

        implementation.myAbstractMethod(); // Call the implemented method
    }
}

// Java 8: Using lambda expression
public class Java8Example {
    public static void main(String[] args) {
        MyInterface implementation = () -> {
            System.out.println("Hello from myAbstractMethod!");
        };

        implementation.myAbstractMethod(); // Call the implemented method
    }
}
```

### Method Reference
>  - A method reference in Java is a shorthand notation of a lambda expression that calls an existing method.<br/>
>  - It's a way to refer to a method without invoking it.<br/>

#### Reference to a Static Method

```Java
public class MethodReferenceExample {
    public static void main(String[] args) {
        String[] stringArray = { "Tom", "Jerry", "Mickey", "Donald" };
        
        // Using a method reference to a static method
        Arrays.sort(stringArray, MethodReferenceExample::compareStrings);

        // Print sorted array
        for (String s : stringArray) {
            System.out.println(s);
        }
    }

    // Static method to compare strings
    public static int compareStrings(String s1, String s2) {
        return s1.compareToIgnoreCase(s2);
    }
}
```

#### Reference to an Instance Method of a Particular Object

```Java
class Printer {
    public void print(String message) {
        System.out.println(message);
    }
}

public class MethodReferenceExample {
    public static void main(String[] args) {
        Printer printer = new Printer();
        
        // Using method reference to an instance method of a particular object
        MyInterface ref = printer::print;
        
        // Calling the method through the reference
        ref.display("Hello from method reference!");
    }
}

@FunctionalInterface
interface MyInterface {
    void display(String message);
}
```

#### Reference to an Instance Method of an Arbitrary Object of a Particular Type
```Java
public class MethodReferenceExample {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Tom", "Jerry", "Mickey");

        // Using method reference to an instance method of an arbitrary object
        names.forEach(System.out::println);
    }
}
```

#### Reference to a Constructor
```Java
class Dog {
    public Dog() {
        System.out.println("Dog created");
    }
}

public class MethodReferenceExample {
    public static void main(String[] args) {
        // Using method reference to a constructor
        Supplier<Dog> dogSupplier = Dog::new;
        
        // Create a new Dog instance
        Dog dog = dogSupplier.get();
    }
}
```

### Default and Static Methods in Interfaces
> - Interfaces could now have methods with implementations, allowing backward compatibility and the addition of new methods to interfaces without breaking existing implementations.<br/>

```java
interface Outil {
    static void afficherMessage() {
        System.out.println("Message de l'interface Outil.");
    }
}

public class Main {
    public static void main(String[] args) {
        // Appel de la méthode statique sans implémenter l'interface
        Outil.afficherMessage(); // Output: Message de l'interface Outil.
    }
}
```

```java
interface Vehicle {
    // Abstract method (must be implemented by any class that implements this interface)
    void drive();

    // Default method
    default void startEngine() {
        System.out.println("Engine started.");
    }
}

class Car implements Vehicle {
    @Override
    public void drive() {
        System.out.println("Car is driving.");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        
        // Calling the abstract method
        myCar.drive(); // Output: Car is driving.

        // Calling the static method
        Vehicle.checkBattery(); // Output: Battery is good.
    }
}
```
### Optional Class
> Optional class was introduced to handle values that may or may not be present, helping to avoid the common NullPointerException issues. <br/>

#### isPresent() and isEmpty()
> - isPresent() checks if a value is present.<br/>
> - isEmpty() checks if a value is absent.<br/>
```java
Optional<String> opt = Optional.of("Hello");
if (opt.isPresent()) {
    System.out.println("Value is present: " + opt.get());
}
```

#### ifPresent()
> Executes a function if a value is present.<br/>
```java
opt.ifPresent(value -> System.out.println("Value: " + value));
```

#### orElse(), orElseGet() and orElseThrow()
> - orElse(): Returns the value if present; otherwise, it returns a specified default value.<br/>
> - orElseGet(): Returns the value if present; otherwise, it calls a Supplier function to provide a default value.<br/>
> - orElseThrow(): Returns the value if present; otherwise, it throws an exception.<br/>
```java
String result = opt.orElse("Default Value");
String result2 = opt.orElseGet(() -> "Computed Default Value");
String value = opt.orElseThrow(() -> new IllegalArgumentException("Value is absent"));
```

## Java 11

### Running Java Files Directly
> With Java 11, you can run a Java file directly without compiling it first, making it easier to quickly test code snippets.<br/>
```java
java HelloWorld.java
```

### New String Methods
> Java 11 adds a few new methods to the String class: isBlank, lines, strip, stripLeading, stripTrailing, and repeat.<br/>

```java
" ".isBlank();          // true - Checks if a string is empty or contains only white space
"Hello\nWorld".lines(); // Stream<String> - Splits a string into lines
" Java ".strip();       // "Java" - Removes leading and trailing whitespace
"Hello".repeat(3);      // "HelloHelloHello" - Repeats the string
```

```java
String multilineString = "Baeldung helps \n \n developers \n explore Java.";
List<String> lines = multilineString.lines()
  .filter(line -> !line.isBlank())
  .map(String::strip)
  .collect(Collectors.toList());
assertThat(lines).containsExactly("Baeldung helps", "developers", "explore Java.");
```

### Optionnal new method isEmpty
```java
Optional<String> optional = Optional.empty();
System.out.println(optional.isEmpty());    // Output: true
```

### Collection to an Array
> The java.util.Collection interface contains a new default toArray method which takes an IntFunction argument.<br/>
```java
List<String> sampleList = Arrays.asList("Java", "Kotlin");
String[] sampleArray = sampleList.toArray(String[]::new);
```

### using the local variable syntax (var keyword) in lambda parameters
```java
List<String> names = List.of("Alice", "Bob", "Charlie");
names.stream()
     .filter((@NotNull var name) -> name.startsWith("A"))
     .forEach(System.out::println);
```



