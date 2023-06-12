# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

A. Is a feature of object-oriented programming (OOP) that allows you to use the same code to work with different types of objects. For example, you  can have a method that takes an object as a parameter, and the method will work with any type of object that is passed to it.

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

A. Polymorphism in OO design refers to the ability of objects to respond to messages in different ways, depending on their specific type. This is achieved by defining methods with the same name in different classes, and then overriding those methods in the child classes to provide a specific implementation.

class Animal {
    public void makeSound() {
        System.out.println("Generic animal sound");
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

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        animal.makeSound(); // Prints "Woof!"

        animal = new Cat();
        animal.makeSound(); // Prints "Meow!"
    }
}

In this example, the makeSound() method is defined in the Animal class. However, it is overridden in the Dog and Cat classes. This means that the makeSound() method will behave differently depending on the type of object that it is called on.

In this example, we are creating a Main class that has a main() method. In the main() method, we are creating an Animal object and then assigning it to a variable called animal. We are then calling the makeSound() method on the animal object. The makeSound() method will print "Generic animal sound" because it is defined in the Animal class.

We are then creating a Dog object and assigning it to the animal variable. We are then calling the makeSound() method on the animal object. The makeSound() method will now print "Woof!" because it has been overridden in the Dog class.

We are then creating a Cat object and assigning it to the animal variable. We are then calling the makeSound() method on the animal object. The makeSound() method will now print "Meow!" because it has been overridden in the Cat class.

This is a simple example of how polymorphism can be used in OO design. Polymorphism can be used to make code more concise, reusable, and readable.

3. What can we use to implement polymorphism in Java?

A. Method overloading: Method overloading is when a class has multiple methods with the same name, but different parameters. The compiler will choose the correct method to call based on the types and number of arguments that are passed to the method.

Method overriding: Method overriding is when a subclass has a method with the same name, parameters, and return type as a method in its superclass. The method in the subclass will override the method in the superclass, and will be called when the method is invoked on an object of the subclass.


4. How many 'forms' can an object take when using polymorphism?

A. It can take many forms.

5. Give an example of when you could use polymorphism.

A. When you need to work with objects of different types. For example, you might need to write code that can work with both animals and vehicles. By using polymorphism, you can write code that is generic and can work with any type of object.

When you need to reuse code. If you have a method that works with a particular type of object, you can use polymorphism to make that method work with any type of object. This can save you time and effort, and it can also make your code more reusable.

When you need to make your code more readable and maintainable. Polymorphism can help you to make your code more readable and maintainable by making it clear what type of object is being used. This can make it easier to understand and update your code.



# Composition and Aggregation

6. What do we mean by 'composition' in reference to object-oriented programming?

A. Composition is a way of creating objects by combining other objects. In object-oriented programming, objects are like little boxes that contain data and methods. When you compose objects, you are creating a new object that contains the data and methods of the other objects.

7. When would you use composition? Provide a simple example in Java.

A. When you need to create complex objects. For example, you might need to create an object that represents a car. This object would need to contain data about the car's engine, wheels, body, and seats. You could use composition to create this object by composing objects that represent the car's engine, wheels, body, and seats.

When you need to reuse code. If you have code that represents a particular part of an object, you can use composition to reuse that code in different objects. For example, you might have code that represents a car's engine. You could use composition to reuse this code in different objects that represent different types of cars.

When you need to make your code more readable and maintainable. Composition can help you to make your code more readable and maintainable by making it clear what parts of an object are related. This can make it easier to understand and update your code.
Here is a simple example of how composition can be used in Java. Let's say you are writing a program that needs to be able to represent a car. You could create a Car class that contains data about the car's engine, wheels, body, and seats.

Code snippet
class Car {

    private Engine engine;
    private Wheels wheels;
    private Body body;
    private Seats seats;

    public Car() {
        engine = new Engine();
        wheels = new Wheels();
        body = new Body();
        seats = new Seats();
    }

    public void drive() {
        engine.start();
        wheels.turn();
        body.move();
    }
}
Use code with caution. Learn more
The Car class would then have methods for driving the car, changing the car's engine, wheels, body, and seats.

This would allow you to create a Car object without having to duplicate the code for the car's engine, wheels, body, and seats.

8. Give a difference between composition and aggregation?

A. Composition is a strong relationship between two objects, where the child object cannot exist without the parent object. For example, a House object can be composed of Door objects, Window objects, and Roof objects. The Door objects, Window objects, and Roof objects cannot exist without the House object.

Aggregation is a weak relationship between two objects, where the child object can exist without the parent object. For example, a University object can be aggregated by Department objects. The Department objects can exist without the University object.

9. What is/are the advantage(s) of using composition/aggregation?

A. Reusability: Composition and aggregation allow you to reuse code by creating objects that contain other objects. This can save you time and effort when you are developing software.

Flexibility: Composition and aggregation allow you to create flexible designs that can be easily changed. This is because the child objects in a composition or aggregation relationship are not tightly coupled to the parent object.

Maintainability: Composition and aggregation can help to improve the maintainability of your code by making it easier to understand and update. This is because composition and aggregation make it clear which objects are related to each other.

10. When using composition, when an object is destroyed, what happens to all the objects it is composed of?

A. When an object is destroyed in composition, all of the objects it is composed of are also destroyed. This is because the objects that are composed of are considered to be part of the parent object. When the parent object is destroyed, all of its child objects are also destroyed.

11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?

A. When using aggregation, when an object is destroyed, the objects it is aggregated by are not destroyed. This is because the objects that are aggregated by are not considered to be part of the parent object. When the parent object is destroyed, the objects it is aggregated by are not affected.