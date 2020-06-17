# Unit 2 - Object Oriented Programming

## [**L7 Sandbox**][sandbox]

## Scope

Variables are extremely useful, but they have limits. These limits are characterized as [**global**](https://javaconceptoftheday.com/global-and-local-variables/) and [**local**](https://javaconceptoftheday.com/global-and-local-variables/) scope.

Scope is the block of code between two brackets. Consider the following: 

```java
public class Scope{

    private int number;
    private int total; 
    
    public Scope(){        
        number = 12;
    }
    
    public void addNumbers(){
        int numberB = 4;        
        total = numberB + number;
    }    

    public void displayTotal(){
        System.out.println("The total of " + number + " + " + numberB + " is " + total);
    } 
}
``` 
This class will cause an error if `displayTotal()` is called, so let's look at why. 

There are a lot of scopes in the program. The first set of brackets define the scope of the class. Variables can only be accessed the in scope they are defined. Any variable defined at the beginning of the class scope is available to any method in the class. These are called [**global**](https://javaconceptoftheday.com/global-and-local-variables/) because they can be used anywhere in the class.

Next, each method has its own scope. This is the [**local**](https://javaconceptoftheday.com/global-and-local-variables/) scope of the variable. Variables defined in a method's scope can only be accessed in the method's scope.

So where's the error?  The error lies in the `displayTotal()` method. It tries to access the variable `numberB` which is declared in the `addNumbers` method. So `numberB` doesn't exist in the scope of `displayTotal`. _**A variable can only be accessed within the scope it was declared.**_ 

Let's jump into the [**Sandbox**][sandbox] and see some more examples. 

[sandbox]: ../L7.java