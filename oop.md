#Object-Oriented Programming Super Basics

**Note**: This gives examples of Ruby and Python that are not pure object-oriented languages. In Java for example, numbers and strings are not objects and the analogies won't hold. But this manual is for Ruby and Python. There is enough for Java, C++ and other languages.

So far you have seen how to define a class with methods in it and how to make objects of this class. So what is really a class? It is a description of the type of the object. I explain: 

If you have a variable, it has some type. For example, 5 is of type integer. "Hello" is of type string. [] is of type array, etc. How do they differ? They all mean some piece of data that the program uses to achieve some goal. But they differ in that you can do different things with them. For example, you can divide numbers and take them to some power, whereas you can't divide and take powers of strings. Similarly, you can can make a sting upper case, but you can't make a number upper case. Different objects just have different things that you can do with them because they make sense. An if you decide to do some action to an object of another type, it doesn't make sense. 

Well, now what if I tell you that you can define your own types of objects? This is just exactly what defining a class is. Let's have an example: 

You are supposed to write a program that calculates the area of a scatch, consisting of triangles, squares and circles that do not overlap. You may have many different shapes of the scatch with different number and sizes of the figures. So what we actually have is the AREA of the scatch = area of triangle 1 + area of triangle 2... + area of square 1 + area of square 2... + area of circle 1 + area of circle 2... What the actual equation will be depends on the original shape of the scatch that you give as an input to your program. 

Now, your can go along and start giving variables to the sides, start calculating each area or let's say the 100 circles in the scatch and then add, afterwards, do the same for the squares, etc. But that sounds repetative and unneeded. In reality,it is much better to have your triangles, squares and circles as variables. Moreover, it is good if these variables have some hidden actions that they can take, like calculate their area, just as strings have hidden actions to make themselves upper case or to reverse themselves. 

So we have to create a variable that is of type square that has a function in it, which calculates the area of the square in general. In order to do that, it should have a hidden variable inside, which is the side of the square to use for the method/function of the area a x a. Once we define such a variable, we will not need to know what is going on inside it. All we will know is the type of the variable and what actions it can perform. 

Then we do the same with the triangles and the circles. So here we have 3 new types in Ruby/Python. 

What is next: you start using them. How? By creating objects of these classes. Just as 5 is an object that is of type integer, so will Square(4) be a square with a side 4, that will be able to calculate its own area. 

Why do we need to bother to create classes when they are program specific and not as general purpose as the integers? 

The main reason is that they are convenient. It is super handy to be able to encapsulate some code into a black box and be able to reuse it without writing it over and over again. 

<hr>
Some thoughts about the relationship between classes and objects: 

An object is the actual thing that consists the data. The class is just an empty definition of how the object will look like and behave. So the class is the blueprint of the objectq the template of what the object would be like. If you didn't have a predefined type integer, it would be like: you create a class Integer that should be able to take part in arithmetic operations. It is just an empty definition, a blueprint, that is true for all the object of this class. Then you use in your program the object 5 of class Integer and it has all the actions that all the other pbjects of the same class have by definition. 

In OOP tutorials you will ofthentimes hear: an object is an instance of the class. It is as if you say: "By creating this object, I give an instance (example) of an object of this class." So 5 is an instance of our hypothetical class Integer, Square(4) is an instance of our class Square, etc. 

It is just a fancy way to say a simple thing. 

##The Art of OOP

Since each program has a different purpose, each program will require different objects. Our squares and cirlces will be totally inappropriate for a program used to calculate the amount of energy you need to break atoms into particles in CERN. Sometimes the objects needed are pretty obvious as in our example with squares and triangles but sometimes there can be different objects, having different goals, achieving the same result (as in mathematics, when you have different ways to solve a problem but all methods give the same answer). Different programmers identify and define classes differently so they can give different solutions to the same program. Even though there are differences, here are the rules that you'd better follow when designing your classes: 

##Managing the complexity of your program
Sometimes you have so many different classes in your program that you have to manage them somehow because otherwise you will get too lost in information. 

##Software Architecture

<hr>
##Additional Resources: 
Modules, Classes and Objects: [Learn Ruby the Hard Way] (https://learnrubythehardway.org/book/ex40.html)

Learning the terminology: [Learn Ruby the Hard Way] (https://learnrubythehardway.org/book/ex41.html)

Subclasses: [Learn Ruby the Hard Way] (https://learnrubythehardway.org/book/ex42.html)
