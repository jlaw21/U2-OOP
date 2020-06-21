# Unit 2 - Object Oriented Programming

## Documentation

An important part of any program is documentation. This can take on many different forms, some of which we have already used.

### Single-line Comment

As you've seen multiple times `//` denotes a single-line comment. Comments allow the programming to explain parts of the code, but comments are not executed by Java. 

```java

//This is a single-line comment.

```

### Block Comment

A block comment begins with `/*` and ends with `*/`. This is also known as a multi-line comment.

```java
/*
    This is a multi-line comment.
*/
```
### Javadoc Comment

Javadoc comments are used to create the documentation we've seen when we've looked at [**String**](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html) class and [**Math**](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html) class. Typically, these comments are added after creating a class, where the two previous ones are used throughout.

A Javadoc comment begins with `/**` and ends with `*/`

```java
/**
    Returns the sum of two numbers.

    @param num1 the first number to add
    @param num2 the second number to add
    @return     the sum of the parameters.
*/

public int sum(int num1, int num2){
    return num1 + num2;
}
```

In this example, we create a Javadoc documentation based on the `sum` method. These comment follow a specific order and must be done in this order.

First line is a brief description of the method's function. The next few lines are the tags. These tags are the specifics of the block of code. Each tag is defined by the `@` symbol at the beginning. 

Here is a list of tags we will add and where they can be used:
* `@author` (classes and interfaces only, required)
* `@version` (classes and interfaces only, required. See footnote 1)
* `@param` (methods and constructors only)
* `@return` (methods only)

Notice that `@author` and `@version` can only be used at the class level while `@param` can only be used on methods and constructors and `@return` can only be used on methods.

The `@param` tag also includes the identifier of the parameter. 

Once you have all the Javadoc comment created, Java has a built in system which will create the documentation page. Although this won't be used very much in this course, in a larger setting, the documentation pages can be compiled online to help others understand the classes in your programs.

Let's jump over to our [**Rect**][rect] class and add some documentation and create the Javadoc page.  


[rect]: ../Rect.java