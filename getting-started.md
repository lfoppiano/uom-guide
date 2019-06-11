# Getting Started

## Getting started with Indyria

[Indriya](https://github.com/unitsofmeasurement/indriya) is the Units of Measurement Reference Implementation. It provides both an implementation of the interfaces defined in the API, and some helpful elements which are not part of the API.

While some JSRs offer abstract base classes in their public API, many of these classes here are specialized to their target environment so having them as part of the implementation makes it easier to scale and optimize for other environments in a different implementation. 

In this chapter, we'll explain how to set up a simple Maven/Gradle project and create your first quantity. Once you've done that, you're all set to explore the rest of the functionality of Indriya.

TODO: to be reviewed!

### Setting up you project

In order to be able to use Indriya, you first have to set up your project dependencies correctly.

#### Maven 

Assuming you have a working POM file, all you should need to do is to add the following dependency to your project:

```xml
    <dependency>
      <groupId>tech.units</groupId>
      <artifactId>indriya</artifactId>
      <version>2.0-PRD</version>
    </dependency>
```

#### Gradle

Just add the dependency in your `build.gradle` file:  

```groovy
compile 'tech.units:indriya:2.0-EDR'
```

TODO: Additional dependencies??

## Examples 

Some example are available [here](https://github.com/thodorisbais/jsr385-examples).

## Your First Quantity

A first quantity can be implemented quickly. For example let's take the speed of light (*c*). Let's start by creating a new class in a package of your choice. In that class, import the following types in order to create a new speed quantity:

```java
import javax.measure.Quantity;
import javax.measure.quantity.Speed;

import tech.units.indriya.quantity.Quantities;
import tech.units.indriya.unit.Units;
```

In order to keep things simple, we'll create the quantity in the class's `main` method, and print it out immediately.

```java
  public static void main(String[] args) {
    Quantity<Speed> C = Quantities.getQuantity(1079252849, Units.KILOMETRE_PER_HOUR);
    System.out.println("The speed of light: " + C);
  }
```

Compile the class, and run it as a stand-alone Java application. The result should be like this:

```
The speed of light: 1079252849 km/h
```

That's it: you've just included Indriya as a dependency to a project, and created and printed out your first quantity!
