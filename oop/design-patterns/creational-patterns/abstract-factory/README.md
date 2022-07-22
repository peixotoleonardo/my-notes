# Abstract Factory

## Intent

**Abstract Factory** lets you produce families of related objects without
specifying their concrete classes.


## Problem

Imagine that you're creating a furniture shop simulator. Your code consists
of classes that represent:

1. A family of related products, say: Chair + Sofa + CoffeeTable
2. Several variants of this family. For example, products Chair + Sofa + CoffeeTable
   are available in these variants: Modern, Victorian, ArtDeco.
  
You need a way to create individual furniture objects so that they match other objects
of the same family.

Also, you don't want to change existing code when adding new products or families of
products to the program - OCP (Open/Closed Principle).

## Solution

The first thing the **Abstract Factory** pattern suggests is to explicitly
declare interfaces for each distinct product of the product family.
Then you can make all variants of products follow those interfaces. For example,
all chair variants can implement the Chair interface, all coffee table variants
can implement the CoffeeTable interface, and so on.

The next step is to declare the Abstract Factory - an interface with a list of
creation methods for all products that are part of the product family. These methods
must return abstract product types represented by the interfaces extracted
previously: Chair, Sofa, CoffeeTable and so on.

Now, how about the product variants? For each variant of a product family,
we create a separate factory class based on the AbstractFactory interface. A factory
is a class that returns products of a particular kind.

The client code has to work with both factories and products via their respective
abstract interfaces. This lets you change the type of a factory that you pass to 
the client code, as well as the product variant that the client code receives,
without breaking the actual client code.