# Day 52: Multiple Inheritance & MRO

## Concept
Multiple inheritance means a class can inherit from **more than one parent class**.

Python allows this, so a child class can use attributes and methods from multiple base classes.

For example, if we have:
- a `Vehicle` class
- a `Flyable` class

Then a class like `FlyingCar` can inherit from both.

## Why Use Multiple Inheritance?
Multiple inheritance is used when a class needs features from more than one parent class.

It helps when:
- one parent provides one type of behavior
- another parent provides a different type of behavior
- and the child class needs both

For example:
- `Vehicle` can provide movement-related behavior
- `Flyable` can provide flying-related behavior
- `FlyingCar` can use both

This makes code more reusable and organized.

## What is MRO?
MRO stands for **Method Resolution Order**.

It is the order in which Python searches for a method or attribute in parent classes.

When a class inherits from multiple classes, Python needs rules to decide:
- which parent class method to call first
- where to search next if the method is not found

Python follows a specific order called **MRO**.

You can check it using:
```python
ClassName.__mro__
```
### Diamond Problem
The diamond problem happens when multiple inheritance creates a shape like this:
```python
        A
       / \
      B   C
       \ /
        D
```
Here:

* B and C both inherit from A
* D inherits from both B and C

Now if D calls a method that exists in all parents, Python must decide:

* should it take the method from B?
* or from C?
* or from A?

Python solves this using MRO.

### Key Points

* A class can inherit from more than one class.
* Python uses MRO to decide method lookup order.
* MRO prevents confusion in multiple inheritance.
* The diamond problem is handled safely in Python through MRO.
* super() also works according to MRO.

### Example Scenario

We have:

* Vehicle class with a start() method
* Flyable class with a fly() method
* FlyingCar class that inherits from both

This allows FlyingCar to use behavior from both parent classes.

## Conclusion
Multiple inheritance is powerful when used properly. It helps combine features from different classes into one child class. Python manages method lookup using MRO, which makes multiple inheritance safer and more predictable.