# Object-Oriented Programming (OOP) Concepts for Understanding

## Introduction



Object-oriented programming (OOP) is a programming paradigm centered on the concept of "objects." It provides a structured approach to designing and developing software systems. We can create more modular, reusable, and maintainable code by understanding and applying OOP principles.

## Core OOP Concepts

### 1. Class
* A blueprint or template for creating objects.
* **Real-world example:** A car blueprint defines a car's properties (color, model, year) and behaviors (start, stop, accelerate).
* Also take an example of a Human being who has properties like physical appearance and behaviors like speaking, running, walking, talking, etc.

```java
class Car {
    private String color;
    private String model;
    private int year;

    public Car(String color, String model, int year) {
        this.color = color;
        this.model = model;
        this.year = year;
    }

    public   
 void start() {
        System.out.println("Car started");
    }

    public void stop() {
        System.out.println("Car stopped");
    }
}
 ```

## 2. Object
An instance of a class.
#### Real-world example: A specific car, like a red 2023 Toyota Camry, is an object of the Car class.
```Java
Car car1 = new Car("red", "Camry", 2023);
Car car2 = new Car("blue", "Corolla", 2022);
```


## 3. Encapsulation
Binding data (attributes) and methods that operate on that data within a single unit (class).
Real-world example: A car's internal components (engine, transmission) are hidden from the user, who interacts only with the steering wheel, pedals, and other external controls.
 ```Java
class Car {
    // ... (same as above)

    private void startEngine() { // Private method
        // Internal logic for starting the engine
        System.out.println("Engine started");
    }
}
```

## 4. Inheritance
Creating new classes (child classes) from existing ones (parent classes).
Real-world example: A sports car inherits properties and behaviors from a general car class, but adds specific attributes like a powerful engine and aerodynamic design.

```Java
class SportsCar extends Car {
    private int horsepower;

    public SportsCar(String color, String model, int year, int horsepower) {
        super(color, model, year);
        this.horsepower = horsepower;
    }

    public void accelerate() {
        System.out.println("Sports car accelerating...");
    }
}
```


## 5. Polymorphism
The ability of objects to take on many forms.
Real-world example: Different animals may respond to the "make sound" command in different ways (dogs bark, cats meow).
```Java
class Animal {
    public void makeSound() {
        // Default implementation
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof!");
    }
}

class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Meow!");   

    }
}
```

## Abstraction in Object-Oriented Programming (OOP)
Abstraction is one of the fundamental principles of OOP. It involves simplifying complex systems by focusing on the essential features and hiding unnecessary details. In essence, abstraction allows you to model real-world entities in a way that captures their key characteristics without getting bogged down in implementation specifics.

Key Concepts in Abstraction:

* Abstract Classes:

<i>A class that cannot be instantiated directly.</i>
<i>It serves as a blueprint for other classes, defining common methods and properties.</i>
<i>Abstract classes often contain abstract methods, which have no implementation and must be overridden by subclasses.</i>
``` Java
abstract class Shape {
    abstract void draw();
}
```

### Refactoring the Codebase
<b>To refactor the codebase effectively, consider the following OOP principles:</b>

* Identify Classes and Objects:

<i>Break down the code into meaningful classes and objects.</i>
<i>Encapsulate data and behavior within classes.</i>
* Apply Inheritance:

<i>Identify commonalities between classes and create inheritance hierarchies.</i>
<i>Use inheritance to avoid code duplication.</i>
* Utilize Polymorphism:

<i>Design interfaces or abstract classes to define common behaviors.</i>
<i>Implement these behaviors in derived classes to achieve polymorphism.</i>
* Enforce Encapsulation:

<i>Make attributes private and provide public methods to access and modify them.</i>
<i>This protects data integrity and promotes code modularity.</i>

By applying the above principles, we can improve the code's readability, maintainability, and extensibility.


### References
[GFG](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)
[W3Schools](https://www.w3schools.com/java/java_oop.asp)

