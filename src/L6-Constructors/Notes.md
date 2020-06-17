# Unit 2 - Object Oriented Programming

## [**L6 Sandbox**][sandbox]

## Constructors

The final piece of the classes puzzle are [**constructors**](https://www.tutorialspoint.com/java/java_constructors.htm). Constructors create objects and are called using the keyword `new`. 

Every class has a constructor, whether you create one or not. Constructors must have the same identifier as the class itself. A default constructors passes no arguments and sets no values, it simply creates an empty object. 

This is an example of the default constructor for the [**Rect**][rect] class:
```java
public Rect(){
}
```
Notice there are no parameters and no values assigned to the attributes of the object. It simply just creates the object, creates space on the user's computer to hold the object's data.

A constructor is a way to set standard default values for the attributes of an object. For example, if we wanted to simulate a dice, we may set the default value to a 1, since a dice cannot have [**null**](https://www.programcreek.com/2013/12/what-exactly-is-null-in-java/) value. `null` means empty or non-existent. No matter what side of the dice you look at, it has a value.

Same applies to a rectangle. A rectangle cannot have a length or width that doesn't exist. Constructors can either assign literal values to the attributes, or use parameters to pass values in, or both.

Add the following to [**Rect**][rect]:
```java
public Rect(){
    length = 1;
    width = 1;
}

public Rect(double lengthInput, double widthInput){
    length = lengthInput;
    width = widthInput;
}
```

Notice how both constructors have the same name as the class. The first constructor has no parameters but assigned the value of 1 to each of the attributes. The second constructor uses parameters to assign values to each of the attributes. 

Let's jump over to the [**Sandbox**][sandbox] and see how to implement these constructors.


[sandbox]: ../L6.java
[rect]: ../Rect.java