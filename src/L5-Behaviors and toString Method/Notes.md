# Unit 2 - Object Oriented Programming

## [**L5 Sandbox**][sandbox]

## Behaviors

Objects in the real-world have characteristics, which are called attributes in code. But, a ball bounces, cars accelerate and apples can make pie. These are called [**behaviors**](http://www.dmc.fmph.uniba.sk/public_html/doc/Java/ch2.htm#Behavior) which determines what an object does or what can be done to an object.

Let's a list some behaviors of Rectangles. What can be done to a Rectangle and what are some things you can do with a Rectangle?

* <your answer here>
* <your answer here>

Behaviors are just methods which perform some operation or task on the attributes. You could use `.shuffle()` to shuffle a deck of cards or `.increaseScore()` to increase the player's score.  Behaviors can have parameters, or a return statement, or both. You can even have behaviors that simply output the attributes of the object. 

### Area and Perimeter

Since area and perimeter are computations we can perform on a rectangle, and are dependent upon `length` and `width` we can add a method to calculate these. Let's add the following behavior to our [**Rect**][rect] class. 

```java
public double getArea(){
    return length*width;
}
```
This method returns the value of `length * width` based on the values of `length` and `width` stored in the object. 

Again, note that all data is stored in the object. The `main` method calls the methods from the `Rect` class.

Add another method to the [**Rect**][rect] class for calculating the perimeter of a rectangle, `(2 * length) + (2 * width)`

Next, let's call these two methods in the [**Sandbox**][sandbox] 

### Multiple Parameters

Methods are also capable of having more than one parameter. We could add a behavior to this class which accepts as parameters both `lengthInput` and `widthInput` and then assigns those to the value of the `length` and `width` attributes.

Let's add this to [**Rect**][rect]. 

```java
public void set(double lengthInput, double widthInput){
    length = lengthInput;
    width = widthInput;
}
```

Notice the parameters are separated by a comma and both have declared data-types. When you are first designing a class, you never know which methods you will need and which you won't, so its always a good idea to add as many of these helpful behavior methods as you can. It is also handy if someone else uses this class in a different way than you intended. 

### .toString() Method

Add this line of code to the [**Sandbox**][sandbox]. 

```java
    System.out.println(box);
```
This weird number is how the internals of Java recognizes the object. However, this is not what we intended. We were hoping to output some `String` representation. 

That's where the `.toString()` method comes into play. When `System.out.println()` is called it is looking for a `String` data-type or specifically the default `toString()` method. It is generally a good idea to include this method, or a similar output method, when creating any class.

Let's add a `.toString()` method to our [**Rect**][rect] class. 
```java
public String toString(){

    String message = "";
    
    message += "The length of the rectangle: " + length + "\n";
    message += "The width of the rectangle: " + width + "\n";
    message += "The area of the rectangle: " + getArea + "\n";
    message += "The perimeter of the rectangle: " + getPerimeter + "\n";
    
    return message;
}
```

Let's again look at this implementation in the [**Sandbox**][sandbox]

[sandbox]: ../L5.java
[rect]: ../Rect.java