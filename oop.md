# Object-Oriented Programming Super Basics

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

<hr>
Some thoughts about the relationship between classes and objects: 

An object is the actual thing that consists the data. The class is just an empty definition of how the object will look like and behave. So the class is the blueprint of the objectq the template of what the object would be like. If you didn't have a predefined type integer, it would be like: you create a class Integer that should be able to take part in arithmetic operations. It is just an empty definition, a blueprint, that is true for all the object of this class. Then you use in your program the object 5 of class Integer and it has all the actions that all the other pbjects of the same class have by definition. 

In OOP tutorials you will ofthentimes hear: an object is an instance of the class. It is as if you say: "By creating this object, I give an instance (example) of an object of this class." So 5 is an instance of our hypothetical class Integer, Square(4) is an instance of our class Square, etc. 

It is just a fancy way to say a simple thing. 

## The Art of OOP

Since each program has a different purpose, each program will require different objects. Our squares and cirlces will be totally inappropriate for a program used to calculate the amount of energy you need to break atoms into particles in CERN. Sometimes the objects needed are pretty obvious as in our example with squares and triangles but sometimes there can be different objects, having different goals, achieving the same result (as in mathematics, when you have different ways to solve a problem but all methods give the same answer). Different programmers identify and define classes differently so they can give different solutions to the same program. Even though there are differences, here are the rules that you'd better follow when designing your classes: 

What is the point of OOP?

The main reason is that they are convenient and keep your code in order so that if you can make changes in future, you will know where to look and what to change. If you make a piece of software and it will never ever have to change, then you can write it whichever way you want and as long as it works, you are fine. But in real life there is no such a thing as neverchanging software. The more you have to make changes the better it is to have your code organised. OOP is one way to organize your code so that you make it easier to change in future. So OOP is a way of managing the complexity of your program.

There are four main tools that OOP uses to keep your code in order: 

1. Encapsulation: putting pieces of code into black boxes (building blocks) to hide some code in them so that we can use the whole box to achieve your goals

2. Abstraction: having the building blocks getting more and more complicated stepping on the building blocks below them. What is more: after a building block is constructed, most of the details of it can be ignored and a simpler description of it can be used for interaction

3. Inheritance: having subclasses that inherit the features of the parent classes (there are materials on inheritance below so it will become clear). Public methods can be created to open a defined way to access the logic inside an object. 

4. Polymorphism: well, in Ruby and Python there is no polymorphism such as in Java and C++ for example but there is duck typing. Polymorphism in Java refers to setting a rule called interface that defines what sort of methods and features your object should have so in our above example it is a rule, saying that all objects of the geometry figure classes should have a method that calculates area and if we miss to put a method calculating the area in one of them, the compiler will complain. In Ruby and Python the logic is that at runtime (when the program runs) if there is something missing to dirupt the proper working of the program, there will be an error message. 

## Software Architecture

<hr>
## Resources: 
Modules, Classes and Objects: [Learn Ruby the Hard Way] (https://learnrubythehardway.org/book/ex40.html)

Learning the terminology: [Learn Ruby the Hard Way] (https://learnrubythehardway.org/book/ex41.html)

Subclasses and Inheritance: [Learn Ruby the Hard Way] (https://learnrubythehardway.org/book/ex42.html), {The Bastard Book of Ruby] (http://ruby.bastardsbook.com/chapters/oops/): in reality in Ruby chances are that if you use inheritance, you will most probably mess it up and it may create more problems than it solves. In Java there are things called interfaces that keep OOP in order but in Ruby there are no such things. What is more: they is no compiler to protect us and to check if changes hold throughout the program if we make changes. 

Overview so far: [Tutorials Point] (https://www.tutorialspoint.com/ruby/ruby_object_oriented.htm) & [Codecademy, Section 9] (https://www.codecademy.com/learn/ruby)

Duck typing: 
