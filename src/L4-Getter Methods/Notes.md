# Unit 2 - Object Oriented Programming

## [**L4 Sandbox**][sandbox]

## Getter Methods

[**Setter**](https://dzone.com/articles/java-getter-and-setter-basics-common-mistakes-and) methods allow us to pass values into a method and set an objects attribute or characteristic. [**Getter**](https://dzone.com/articles/java-getter-and-setter-basics-common-mistakes-and) methods allow us to retrieve those values back to the `main` method.  

### Method Header

The **getter** method header looks similar to the **setter** but there are a few distinct differences. The method below gets the length attribute from the `Rect` class.

```java
public double getLength(){
    return length;
}
``` 

* `public` - this is the same as accessibility on attributes. We want methods set to `public` so we can access them from any class. 

* `double` - this is the data-type that is returned by the method. 

* `setLength` - this is the identifier for the method. Notice that a getter does not require a parameter. 

The major difference between Getters and Setters is what happens in the code block of the method itself. 

### Return Statements

If parameters are an introduction, a doorway from the `main` class to the object's class, then a `return` statement is the doorway from the object's class back to the `main` class.

The methods we've seen in both the `String` class and `Math` class are return methods. They send data back to the main class, which can be assigned to variables, output for display or even used for further calculations.

Return statements can return values or the result of a computation. 

### .getWidth() Method

Add the `getWidth` method to the `Rect` class, which returns the `width` attribute.

Let's look at some more implementation in the [**Sandbox**][sandbox].

[sandbox]: ../L4.java
[rect]: ../Rect.java