# JAVA-Basics

# Table of contents
- [History](#History)
- [Java jvm, jre, jdk](#jdk-jre-jvm)
- [Object Oriented Programming Language (POO)](#Object-Oriented-Programming-Language)
  - [Classes and Objects](#Classes-Objects)
  - [Four Pillars of Object-Oriented Programming in Java](#Four-Pillars-Of-POO)
    - [Encapsulation](#Encapsulation)
    - [Inheritance](#Inheritance)
    - [Polymorphism](#Polymorphism)


# History
> Java is a high-level, class-based, object-oriented programming language that was first released by Sun Microsystems in 1995. <br/>
> The company Oracle then acquired Sun Microsystems in 2009, which explains why this language now belongs to Oracle.

# Java jvm, jre, jdk

## jvm (Java Virtual Machine)
> the core of the Java programming language. It is responsible for executing Java bytecode, which is the intermediate code generated after compiling a Java program.<br/>
> The JVM makes Java platform-independent by allowing the same Java bytecode to run on any device or operating system that has a compatible JVM.
> - Loads Bytecode: The JVM loads the compiled .class files into memory.
> - Execution: It executes the bytecode line by line using an interpreter or compiles it to native machine code using the Just-In-Time (JIT) compiler for performance.
> - Memory Management: The JVM manages memory allocation and garbage collection to ensure efficient use of resources.

## jre (Java Runtime Environment)
> provides the necessary environment to run Java applications. <br/>
  > - JVM: The core engine that executes Java bytecode.
  > - Libraries: A set of standard libraries (like java.lang, java.util, etc.) required by Java applications to run.
  > - Other Files: Configuration files, property files, etc., that support the JVM in running Java programs.

## jdk (Java Development Kit)
> full-featured software development kit used for developing Java applications.
  > - JRE: As described above, it provides the runtime environment to execute Java applications.
  > - Development Tools: These include the Java compiler (javac), debugger (jdb), archiver (jar), and other tools necessary for writing and testing Java code.
  > - Additional Libraries: The JDK includes additional libraries required for development, such as those for GUI development (AWT, Swing) and networking.



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
#### Method Overloading :
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




