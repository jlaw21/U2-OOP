# Unit 2 - Object Oriented Programming

## [**L1 Sandbox**][sandbox]

## String Objects

The best way to get familiar with OOP is to look at an example. The `String` class is an example of OOP. Each `String` variable is actually a `String` object. Remember that objects execute methods from the class they are made from.  

Below is a simple method from the `String` class:

`.length()` - returns the number of characters as an `int`.

Let's see an example. Run it in the [**Sandbox**][sandbox] if you want.
```java
public class L1{
    public static void main(String[] args){
        String name = "Alexander";
       
        int stringSize = name.length();
        
        System.out.println(name + " has " + stringSize + " letters.");
    }
}
```

First, we set the value of name, then the magic happens. `name` is now a `String` object and can run methods from the `String` class. The dot operator (`.`) executes the method on the value contained in the object `name`.  Notice that the method `returns` new data which must be assigned to a variable. 

In short, `.length()` counts the letters in `name` and returns that to the variable `stringSize` as an `int`.

### Other String class methods

Methods are defined in a class. Only those methods defined are available to be executed by the object. A list of available methods is usually found in the class's documentation. Let's look at the [**String**](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html) class.

These are a few of the methods we will be focusing on in this unit:
* `.length()` - returns the number of characters as an `int`.
* `.charAt(index)` - returns the character at `index` in the string
* `.toLowerCase()` - returns a copy of the string all in lower-case
* `.toUpperCase()` - returns a copy of the string all in upper-case

The index in `.charAt(index)` refers to a position in the `String`. Computers start counting at 0, so an index of 2, is the third character in the string. Consider these examples:

* "Hello World"   .charAt(4) = "o"
* "Hello World"   .charAt(5) = " "  
* "Hello World"   .charAt(8) = "r"

The program shows the implementation of these methods. Run it in the [**Sandbox**][sandbox].
```java
public class L1{
    public static void main(String[] args){
        
        String message = "Good morning, Mr. Smith.";
        
        String lowerCaseMessage = message.toLowerCase();
        String upperCaseMessage = message.toUpperCase();
        int messageLength = message.length();  //notice this counts spaces!!
        char thirdLetter = message.charAt(2);
        
        System.out.println("Lowecase: " + lowerCaseMessage);
        System.out.println("Uppercase: " + upperCaseMessage);
        System.out.println("Number of characters: " + messageLength);
        System.out.println("The third letter is: " + thirdLetter);
    }

}
```

### Objects vs. Variables

The beautiful thing about objects is that values assigned to an object stays with that object and objects can hold numerous values, which we will see later in this unit. 

When an object is created, a chunk of space is allocated in the user's computer to store all the information regarding that object. Variables can only store 1 value.

For example, a `car` object could hold the make and model of the vehicle. Where a `car` variable could only hold 1 value, possibly the car's name.   

This example shows a `Car` object, `myCar` vs. a car variable, `hisCar`. Run it in the [**Sandbox**][sandbox].

```java
public class L1{

    public static void main(String[] args){
        Car myCar = new Car();  //create a car object
        myCar.setMake("Dodge"); //call a method to set the make
        myCar.setModel("Challenger"); //call a method to set the model
        
        //myCar now holds both the make and model strings
        
        //variable to hold the make and model with a String literal
        String hisCar = "Dodge Challenger";
        
        //call methods to display the make and model
        System.out.println(myCar.getMake() + " " + myCar.getModel());
    
        //display the variable value
        System.out.println(hisCar);        
    }
}
```
Even though the output is the same, you can see that `myCar` and `hisCar` are very different implementation.Through this chapter we will be getting deeper into classes, objects and methods.


[sandbox]: ../L1.java