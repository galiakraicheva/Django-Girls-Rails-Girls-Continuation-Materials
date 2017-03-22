# Ruby on Rails

As I have previously said, Ruby on Rails (or Rails for short) is a framework for developing web applications in Ruby. But what does a framework actually do? Every website with some programs on is more complex than just having a couple of HTML files. So it needs additional things: a place to keep your database information, a place to keep your CSS, a place to keep your images, error pages, tests for the programs, etc. They need to be organized and properly documented (meaning that there should be explanations what does what on the site). A programmer can do all the folders and connections between the files and the databases by him/herself but that is a long task prone to mistakes. That is why, it is better to use a tool that generates an "empty" general purpose working site for us. Such a tool is Rails. 

In order to use it, you must first install it locally or select an Internet IDE that mimics what you see when you work locally. IDE stands for Integrated Development Environment and is a program that simulates your command line, your file structure and your text editor. If you are using Atom, it is like an Atom with a separate mini window for writing commands for the command-line. My advice for Ruby on Rails is to work locally because it gives you more practice. To be honest, installing Rails on your computer may be a headache but you should at least try it before choosing to work on an IDE. 

text, text, explain what Ruby gem is: wikipedia says RubyGems is a package manager for the Ruby programming language that provides a standard format for distributing Ruby programs and libraries (in a self-contained format called a "gem"), a tool designed to easily manage the installation of gems, and a server for distributing them.

The interface for RubyGems is a command-line tool called gem which can install libraries and manage RubyGems.[1] RubyGems integrates with Ruby run-time loader to help find and load installed gems from standardized library folders.



## Resources: 

Intro + a Couple of Terms: [Rails Tutorial.com: Chapter 1, From Zero to Deploy, sections up to 1.1 including](https://www.railstutorial.org/book/beginning): don't spend time clicking on all the additional links with resources. They are all payed and you will find enough practice throughout the tutorial and the additional resouces so you don't need to pay

Installing Rails and Setting Up a Database for Ubuntu [Go Rails](https://gorails.com/setup/ubuntu/16.04): alternatively, you can use an IDE that is recommended in the Rail's Tutorial. I guess so far everybody has switched to Ubuntu one way or another (by virtual box or on a USB key) but if you are using another operating system, google for instructions. 

Simple First Project: [Rails Tutorial.com: Chapter 1, From Zero to Deploy, sections up to 1.3 including]

<hr>

## Models, Controllers, Views Overview: 

A common way to structure your site and display information form your site to the user with Rails (actually, the default one) is by using the MVC model. The idea is to separate user data from the code that displays it and from the internal data of the application. I explain: 

We spoke about browsers and pigeons. Let's continue with the same analogy! We said that when a user enters an address in the address bar of a browser, the address gets packed in a letter and a small pigeon takes the address to a webserver, where the website lives. The server is like a hotel with many rooms where different sites live. At the reception there is a receptionist (a program which is again called web server). So when the pigeon arrives, the receptionist sees what's inside the letter and sends another small pigeon to go to the room where the website the user wants lives. At the door of the room there is the website receptionist, called Ruby controller. It is nothing more than a Ruby class. 

The controller than desides what needs to be done next. Sometimes, it directly renders a template with Ruby code that gets converted to HTML. This template is called a view.

More commonly however: 

1. The controller interacts with a Ruby object that represents an element of the site, for example, a user. The object is called a model and it comminucates with the database and fetches all the information that is needed for the user-specific display of the website. 
2. After the model fetches the information from the database, it fills it into the template that gets converted into an HTML (i.e. the view) 

Let's give an example: 

Imagine an online shopping website for beauty products. You go to the website and you log in. Then you expect to see all your previous history of buying bundles on the website listed. You expect to see all the products you have marked as favorite, etc. So when the browser request gets to the website room at the server hotel, a controller sends the Ruby object, called a model, to  the database to get all the favorite products of the user and the previous shopping carts. When the model returns with all the needed information, it fills it in the views template, that gets converted into HTML. So the HTML is sent back to the browser and the beauty website is displayed.

## Resources: 
[Rails Tutorial, Chapter 1.3.3] (https://www.railstutorial.org/book/beginning#sec-mvc): the Wikipedia link is not very comprehensible, no stress if you do not get it. 

Now take a look at your hello_app folders. Open the folder with your app and click on the different folders. See where your default controller is and how it looks. Open the file with the text editor. 

You can also try this more advanced reading and if something does not make sense, skip it or google it but be careful not to get bogged by googling too many unknown terms: [Ruby on Rails Guides] (http://guides.rubyonrails.org/action_controller_overview.html#what-does-a-controller-do-questionmark)

Then continue with [Rails Tutorial, Chapter 1.3.4] (https://www.railstutorial.org/book/beginning#sec-hello_world)

<hr>

## Getting Familiar with Git

What is Git? It is a software that allows us to track changes to our projects. This is good because from time to time we may delete some code we wanted or we may change our mind and want the site the way it was before we made changes. Git is formally called a version control system, meaning that it keeps all your previous versions of the project and you can easily compare them. 

Another great advantage of Git is that if you work in a team with more people, each one of you can submit changes to the project and you can easily track down or reverse the changes if need be. 

So, how do we do it? Here is an overview of the steps, which are further explained in the links below: 

1. We need to install the git software on your local computer and create a user name and a password. 
2. You create a folder inside the project's folder called .git. It is local on your computer and is called the staging area. This is the place where you make changes locally and after you are ready with the changes, you put them online at GitHub (there are also other sites that provide version control with git but GitHub is more common. The tutorial we use so far uses BitBuket. It doen't matter what you use). 
3. When you are ready with the changes, you put them online to be approachable by the other people in the team.
