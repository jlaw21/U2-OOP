# Unit 2 - Object Oriented Programming

## [**L3 Sandbox**][sandbox]

## Setter Methods

The attributes of a class describe an object's characteristics. We use variables to represent these characteristics. We also saw how we could assign a value, if the attributes were `public` accessibility. 

_But how do we **SET** the values of the attributes if they are `private`?_

We use methods known as [**Getters and Setters**](https://dzone.com/articles/java-getter-and-setter-basics-common-mistakes-and) to **SET** the value of the attributes and **GET** those values to display. 

### Method Header

A method has multiple parts and might look a little confusing at first. Let's add the setter method for length in our [**Rect**][rect] class.

```java
public void setLength(double lengthInput){
    length = lengthInput;
}
```
Let's look at each part of the method header: 

* `public` - this is the same as accessibility on attributes. We want methods set to `public` so we can access them from any class. 
* `void` - this method's return type. We will go into more detail with return types in the next section, **Getters**. For now, `void` simply means there is no data to return.
* `setLength` - this is the identifier for the method.
* `(double lengthInput)` - this specifies the parameters for our method. 

The statement `length = lengthInput` is _inside_ the method's code block and takes the value from the parameter and assigns it to the length attribute.

### Parameters and Arguments

Think of a [**parameter**](https://www.w3schools.com/java/java_methods_param.asp) as passage into a ceremony or event. First, the person has to be announced, then they can enter the ceremony and interact with the other guests. To illustrate, let's watch, [this clip](https://www.youtube.com/watch?v=GccrayoVmzk).

First, the data type has to be declared, like the titles in the clip, then its given a unique identifier. Unique means different from all the other identifiers. 

So in this example, we want the data for the length attribute to come from OUTSIDE the class, so we create a parameter, (double lengthInput) to introduce the length data into the method. 

Once introduced, we can use it to execute statements inside the code block of the method. To better understand how this works, let's look at what happens in the `main` method.

_*note: we change the accessibility of length from `private` to `public` for demonstration_

Try this out in the [**Sandbox**][sandbox]
```java
public class L3 {

    public static void main(String[] args){
        Rect box = new Rect();
        
        box.setLength(5);
        
        System.out.println("The length is: " + box.length);
    }
}
``` 
First, we create a `Rect` object called `box`. `box` then calls the `setLength` method which requires a parameter. The value we give the parameter, called the [**argument**](https://www.w3schools.com/java/java_methods_param.asp), passes from the main class into the Rect class. `5`, from the `main` class, passes to `lengthInput` in the parameter definition, which passes to `length` in the `Rect` class. 

5 -> lengthInput -> length

### Benefits of Objects

_This seems overly complicated for something so simple. Why do it this way?_

Keep in mind that when you create an object, space is allocated for ALL the data for that object. The **object** is holding the data not the class. The `.setLength()` method is assigning data to the `box` object. Any other way, we could be assigning values directly to the class and therefore **ALL** objects would have the same data. We will look at more examples of this later.

The other reason is that in larger programs, this is actually simpler. Would you rather create 100 length variables for 100 boxes, or 1 `setLength` method and call it 100 times?

Lastly, and most important, keep in mind that the `main` method is the only method actually executed by Java. Parameters and arguments allow us to pass data from the `main` method to the objects, essentially. Without this, our programs would become 10x as long, 10x as complicated, and most the data would end up being hard-coded instead of interactive.

### Add the setWidth() method

Now, take what you've learned from creating the `setLength()` method and add a `setWidth()` method to [**Rect**][rect] which accepts a `double widthInput` as a parameter. 

Let's look at some more examples in the [**Sandbox**][sandbox].


[sandbox]: ../L3.java
[rect]: ../Rect.java