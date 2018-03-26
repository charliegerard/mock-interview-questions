# Comparing and Equating (in JavaScript)

Back in my first programming course we were taught the difference between comparing two values and setting a variable equal to another. This is something very trivial, but essential to understanding the basics of Computer Science.

I’ve heard that a common question recruiters ask is the differences between ‘==’ and ‘===’ in JavaScript. I didn’t know the answer to this. until after I took a moment and looked at the [MDN.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript#Operators) So I decided to do a write up on it to reinforce my learning (and hopefully teach you something as well.)

## Equating
Setting a variable equal to another value is the most common case we see ‘=’ used in code. Located below is an example of some code that illustrates this point.

```var someThing = 123; //sets a variable named someThing equal to the integer 123```


## Comparing
We can also compare two (or more) variables or values. This will return us with a TRUE or FALSE evaluation of the comparison. This is done usually when trying to confirm a value before executing some other code else.
In this next example we will use ‘==’ to compare a variable with a value.

## Comparing with ‘==’

```
var name = "john"; //set a variable named name equal to the string "john"
name == "john" //when evaluated this returns the value true
if (name == "john") //because this is true it will execute the code in the brackets
{
console.log( "hello " + name); 
}
```

Now to help illustrate the difference we have to know a term called “Type Coercion”. It is simply converting one data type to another. Like converting a String to an Integer. ‘==’ does support Type Coercion, which will be shown off in this following example. The integer 123 will be compared to the string “123” and return true. This is because of Type Coercion converting the string to an integer.

### Comparing with ‘ ==’ and Type Coercion
```123 == "123" //This will be true```

Now we get to the main point of this post, what is so special about ‘===’?
Well let me tell you, it is way more strict. Like how your Mom wouldn’t let you do anything so you asked your Dad, and got away with it. Well ‘===’ is your Mom and **you’re grounded**. 

Comparing with ‘===’ does not support Type Coercion so it will look at what you stated explicitly and evaluate it. This will build off our previous example code but will give us the opposite result. 

### Comparing with ‘ ===’ and Type Coercion
``` 123 === "123" //This will be false ```


## Wrap up
Now we know the differences between ‘==’ and ‘===’ when doing comparisons! Now when you are in your job interview and they try to trick you with this question:
> what is the difference between using 2 and 3 equal signs when comparing in JavaScript?

Spit out the words “Type Coercion” and hopefully they are happy with that answer. **Hopefully**.
