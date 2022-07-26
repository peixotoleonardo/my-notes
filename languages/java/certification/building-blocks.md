# Building Blocks

## Major Components of Java

The JDK contains the minimum software you need to do Java development.
Key commands include:

- javac: Converts .java source files into .class bytecode
- java: Executes the program
- jar: Packages files together
- javadoc: Generates documentation

The javac program generates instructions in a special format called *bytecode*
that the java command can run. Then java launches the JVM before running the code.
The JVM knows how to run bytecode on the actual machine it is on. You can think of
the JVM as a special magic box on your machine that knows how to run your .class
file within your particular operating system and hardware.

## Understanding the Class Structure

In Java programs, classes are the basic building blocks. When defining a class,
you describe all the parts and characteristics of one of those building blocks.

To Use mos classes, you have to create objects. An *object* is a runtime instance
of a class in memory. An object is often referred to as an *instance* since it
represents a single representation of the class. All the various objects of all
the different classes represent the state of your program. A reference is a 
variable that points to an object.

### Fields and Methods

Java classes have two primary elements: *method*, often called functions or
procedures in other languages, and *fields*, more generally known as variables.
Together these are called the *members* of the class. Variables hold the state
of the program, and methods operate on that state. If the change is important to
remember, a variable stores that change.

### Comments

Another common part of the code is called a *comment*. Because comments aren't
executable code, you can place them in many places. There are **three types** of
comments in Java.

1. single-line comment - //...

2. multiple-line comment - /*...*/, we cannot have nested multiple-line comment

3. Javadoc comment - /**...*/ has a specific structure that the Javadoc tool
  knows how to read

### Classes and Sources Files

A top-level class is often public, which means any code can call it.
Interestingly, Java does not require that the type be public. A top-level is
a data structure that can be defined independently within a source file.

You can even put two types in the same file. When you do so, at most one of
top-level types in the file is allowed to be public.

If you have a public type, it needs to match the filename.

## Writing a main() Method

A Java program begins execution with its **main()** method. The **main()**
method is often called an entry point into the program, because it is the
starting point that the JVM looks for when it begins running a new program.

### Creating a main() Method

The **main()** method lets the JVM call our code. The simplest possible class
with a main() method looks like this:

```java
public class Zoo {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

This code prints *Hello World*. To compile and execute this code, type
it into a file called Zoo.java and execute the following:

```
$ javac Zoo.java
$ java Zoo
```

To compile Java code with the javac command, the file must have the
extension .java. the name of the file must match the name of the public class.
The result is a file of bytecode with the same name but with a .class filename
extension. 

Some rules for a Java file:

- Each file can contain only one public class.

- The filename must match the class name, including case, and have a
  .java extension

- If the Java class is an entry point for the program, it must contain a valid
  main() method.

### Passing Parameters to a Java Program

```java
public class Zoo {
  public static void main(String[] args) {
    System.out.println(args[0]);
    System.out.println(args[1]);
  }
}
```

```sh
$ javac Zoo.java && java Zoo Foo Bar
```