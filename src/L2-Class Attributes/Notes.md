# Unit 2 - Object Oriented Programming

## [**L2 Sandbox**][sandbox]

## Class Attributes

A class defines an object. An object is a representation of something in the real world. To understand a class, let's  make a digital representation of a ball. 

First all, what are some characteristics of a ball?  Add your own below: 

* color


These characteristics, called [**attributes**](https://www.w3schools.com/java/java_class_attributes.asp), act as variables inside the class storing information about the object.  If we wanted to create a `Ball` class it might contain a variable, `color`. 

Let's build a simple class which represents a Rectangle. 

### Class Header

All classes start with a class header. The class header includes the name of the class, which is frequently the object you are representing. The naming convention is a single upper-case noun. **The name of the class MUST match the name of the file**. 

For a `Ball` class the header looks like:
```java
public class Ball{

}
```

To create a class in IntelliJ, right-click `src` folder in the project view. Hover over `new` and select `Java Class`. Since we are creating a Rectangle, lets name this class `Rect`. 

*The class Rectangle already exists in the `java.awt` package. We use `Rect` to avoid confusion.*

Notice that IntelliJ automatically creates the class header. Pretty nice, huh?

### Attributes

Once we have the class header, next we declare the class [**attributes**](https://www.w3schools.com/java/java_class_attributes.asp). Typically, a class's attributes aren't assigned a value, because the objects made from those classes can all have different values for these attributes. We declare attributes the same way we declare variables, with one small addition.

Add the following to [**Rect**][rect].

```java
public class Rect{
    
    private double length;
    private double width;

}
```

### `public` vs. `private`

You will notice we add the keyword `private` in front of the variable declaration. 

* `private` - a private variable or attribute means it can only be accessed within the class its declared. 
* `public` - a public variable or attribute means it can be accessed from any other class. 

Before we illustrate how `public` and `private` keywords work, we need to understand how to use classes in the main class. Our main class for the next lessons are the [**Sandbox**][sandbox]. Remember the main class contains the main method.

```java
public class L2{
    
    public static void main(String[] args){
        
        //creates a Rect object
        Rect box = new Rect();
        
    }

}
``` 

Let's look at how the `public` and `private` keywords work.


[sandbox]: ../L2.java
[rect]: ../Rect.java