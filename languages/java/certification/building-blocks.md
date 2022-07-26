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

Java calls a word with special meaning a *keyword*.
