# Ruby on Rails

As I have previously said, Ruby on Rails (or Rails for short) is a framework for developing web applications in Ruby. But what does a framework actually do? Every website with some programs on is more complex than just having a couple of HTML files. So it needs additional things: a place to keep your database information, a place to keep your CSS, a place to keep your images, error pages, tests for the programs, etc. They need to be organized and properly documented (meaning that there should be explanations what does what on the site). Moreover, there needs to be additional technical work connecting all parts together. A programmer can do all the folders and connections between the files and the databases by him/herself but that is a long task prone to mistakes. That is why, it is better to use a tool that generates an "empty" general purpose working site for us. Such a tool is Rails. 

In order to use it, you must first install it locally or select an Internet IDE that mimics what you see when you work locally. IDE stands for Integrated Development Environment and is a program that simulates your command line, your file structure and your text editor. If you are using Atom, it is like an Atom with a separate mini window for writing commands for the command-line. My advice for Ruby on Rails is to work locally because it gives you more practice. To be honest, installing Rails on your computer may be a headache but you should at least try it before choosing to work on an IDE. 

After you have installed Rails, you will make your first project using it. This will generate a folder with your project full of subfolders and files. One of the files will be your Gemfile. It contains all small programs and libraries that get your CSS, database and others to work well with Ruby files. These libraries are also called dependencies because the proper work of your Rails app depends on them. The tool desgned to easily manage them and installing them is called RubyGem. You communicate with the RubyGem and make all the installations in the Gemfile from the command-line. 


## Resources: 

Intro + a Couple of Terms: [Rails Tutorial.com: Chapter 1, From Zero to Deploy, sections up to 1.1 including](https://www.railstutorial.org/book/beginning): don't spend time clicking on all the additional links with resources. They are all payed and you will find enough practice throughout the tutorial and the additional resouces so you don't need to pay

Installing Rails and Setting Up a Database for Ubuntu [Go Rails](https://gorails.com/setup/ubuntu/16.04): alternatively, you can use an IDE that is recommended in the Rail's Tutorial. I guess so far everybody has switched to Ubuntu one way or another (by virtual box or on a USB key) but if you are using another operating system, google for instructions. 

Simple First Project: [Rails Tutorial.com: Chapter 1, From Zero to Deploy, sections up to 1.3 including]

<hr>

## Models, Controllers, Views Overview: 

A common way to structure your site and display information from your site to the user with Rails (actually, the default one) is by using the MVC model. The idea is to separate user data from the code that displays it and from the internal data of the application. I explain: 

We spoke about browsers and pigeons. Let's continue with the same analogy! We said that when a user enters an address in the address bar of a browser, the address gets packed in a letter and a small pigeon takes the address to a webserver, where the website lives. The server is like a hotel with many rooms where different sites live. At the reception there is a receptionist (a program which is again called web server). So when the pigeon arrives, the receptionist sees what's inside the letter and sends another small pigeon to go to the room where the website that the user wants lives. At the door of the room there is the website receptionist, called Ruby router. It takes the letter, reads the request in it and sends it to the corresponding controller. Controllers are where most of the logic of the website is. It contains all the actions that the site may take and it commands what to do at each page of the site. It may sond complicated but controllers are nothing more than a Ruby class. 

The controller desides what needs to be done next. Sometimes, it directly renders a template with Ruby code that gets converted to HTML. This template is called a view.

More commonly however: 

1. The controller takes the views and see whether there are pieces of information that are stored in the database. In most cases, there are. 
2. The controller needs to fetch information from the database to fill it in the views. To do that, it "sends" a Ruby object that represents an element of the site, for example, a user to go to the database and get the information needed. The object is called a model and to be precise, it is not sent anywhere but it is good for an analogy.
3. After the model fetches the information from the database, it gives it to the controller, which fills it into the template that gets converted into an HTML (i.e. the view) 

Let's give an example: 

Imagine a news website. It has articles that change every single day. You have to have the articles stored into your database to keep the history of all written. So you create the structure of your website like this: 
* Views: and HTML, mixed with Ruby, which represents the skeleton of your webpages with "empty holes" for the articles that are to be fetched from the database.
* Models: a Ruby object that approaches the database and gets the articles from the database. The website may have other objects as well, for example, with your username and email, if you can log into the website, for comments, etc. There can be many models that fill in a lot of "holes" with content from the database. The models are called, for example, index.html.erb, meaning that they have html and embedded Ruby inside the file.
* Controller: the boss who says: Let me see what's in the view, ok, there are empty holes. Model, give me the articles from the database. Views, here is the info that you need: fill in your holes. The way this is done: the model is a Ruby object. We call its methods and we should keep the values of the output of the methods in a variable that is in the controller. The variable is an instance variable, beginning with @, and is automatically available to use in the views.   

General sidenote: for every model you have a different controller which is a subclass of the application controller that you get by default when you generate your project. The router tells which controller is needed for the particular request, comming from the browser. 

## Resources: 
[Rails Tutorial, Chapter 1.3.3] (https://www.railstutorial.org/book/beginning#sec-mvc): the Wikipedia link is not very comprehensible, no stress if you do not get it. 

Now take a look at your hello_app folders. Open the folder with your app and click on the different folders. See where your default controller is and how it looks. Open the file with the text editor. 

Routing: (The Odin Project)[http://www.theodinproject.com/courses/ruby-on-rails/lessons/routing]

You can also try this more advanced reading and if something does not make sense, skip it or google it but be careful not to get bogged by googling too many unknown terms: [Ruby on Rails Guides] (http://guides.rubyonrails.org/action_controller_overview.html#what-does-a-controller-do-questionmark)

Then continue with [Rails Tutorial, Chapter 1.3.4] (https://www.railstutorial.org/book/beginning#sec-hello_world)

<hr>

## Getting Familiar with Git

What is Git? It is a software that allows us to track changes to our projects. This is good because from time to time we may delete some code we wanted or we may change our mind and want the site the way it was before we made changes. Git is formally called a version control system, meaning that it keeps all your previous versions of the project and you can easily compare them. 

Another great advantage of Git is that if you work in a team with more people, each one of you can submit changes to the project and you can easily track down or reverse the changes if need be. 

At the beginning, Git may sound a little bit counterintuitive. Remember that version control is like sophisticated saving of a Word document. You will see a couple of terms that may sound a bit confusing. 

First, git and GitHub are different. Git is the software that allows you to save changes in a sophisticated manner and be able to see the different versions of your file at different times. So git is a program that runs locally on your computer. The history of all changes that git software generates is called repository. GitHub is a website where you can upload your repository (the code and the history of the changes) so that other people can reach it. So in a way, it is similar to OneDrive, Google Drive, Dropbox and others because it is a place on the Internet, where you have a storage for your files. 

Let's take a look at the process of using git. We give git commands through the command line. First, we need to initialize a git repository. We use the git init command. It is as if you make a folder in which you will save all the versions of your files. The only difference is that it is not empty. It is the git database with lots of internal files and no database entries (it is an empty database). You may notice that the repository is called .git. The dot before the name of the directory means that it can't be seen in the file structure because it is hidden. 

Next step is to select the files you want to save to the repository. This is done by the git add command. It is as if you select with the mouse the files you want to move. This is called "the files are in the staging area" but it is simply choosing what files you want to include in the repository. 

The "final" step is to actually include them to the repository (in our analogy, similar to moving the files with a mouse). Once you commit, the files are included in the history log of the database of git.

All these things happen locally on your computer. In order to upload or download project files from GitHub, you use only two commands: git push and git pull. Here is the time to mention that there are also other git hosting companies, like GitHub. These are BitBucket, GitLab and others. The one you choose is up to you. 

All these steps explained one by one: [Rails Tutorial: until 1.4.4](https://www.railstutorial.org/book/beginning#sec-version_control)

Branches, Commit, Merge, Pull Request: [GitHub Tutorial](https://guides.github.com/activities/hello-world/): just for an overview to see how it is done with button clicking

Branches, Commits, Merges: [Rails Tutorial, Section 1.4.4](https://www.railstutorial.org/book/beginning#sec-git_commands)

<hr>

## Deploying with Heroku

To deploy is just another way to say to put your application to the Internet to be available to others to use and to be working. Sometimes it is also called to push in production. In order to publish your application on the Internet, you need to have a software to make sense of all your different files and how they are related and a place on a server or in a cloud. This is what Heroku does. 

Heroku is a hosting for web applications. It is not used for websites that have no programs in them. You use git in order to transport your code in Heroku and if your application is written by a well-known framework, like Rails, Heroku easily realises what is what in the application and puts it running on a server. Well, it is a cloud-based application, so it puts your site in a cloud. 

A reminder about dependencies: it is another word for libraries. The term comes from the idea that the website you are building and it's proper work depends on having the libraries. 

Deploying: [Rails Tutorial, Section 1.5 onwards](https://www.railstutorial.org/book/beginning#sec-deploying): the part where we run bundle install --without production may seem pointless but we still do it because bundle innstall will do two things: install the gems that are specified and update the Gemfile.lock with all the version of the listed libraries in the Gemfile. But what is the Gemfile.lock? It is a file that explicitly lists all the versions of the gems that are used. If you specify them in the Gemfile, it is not that important what there is in the Gemfile.lock. However, a lot of applications do not specify the version of the gems so the latest is installed and the application runs well with the latest version but after some time, when people install the application the Gemfile which does not specify the version may install a newer version of a gem and the app may break. So the Gemfile.lock says that the application works under the specified versions of the gems. 

Note that in the example, for testing, sqlite3 is used, whereas for production pg is used. It is not a good idea to use different databases for testing and for production but most probably the tutorial does so because installing and using PostreSQL on Windows is a bit troublesome. So for simplicity maybe the author chose such solution. 

Learning about Heroku: [Heroku Guides](https://devcenter.heroku.com/articles/how-heroku-works): until Running applications with dynos. A bit more challenging text because it also speaks about other languages and platforms. Concentrate on what you know and on Rails. 

<hr> 

## Second Project

Scaffolding and MVC practice, REST Basics: [Rails Tutorial](https://www.railstutorial.org/book/toy_app): Here you encounter a couple of terms and practicies for first time. Scaffolding is a way to create quickly and automatically the main pieces of an app. After we generate scaffolding, we "migrate" the database. Migrating the database means making changes. The generate scaffold command has generated a database migration and we need to update the database with the migration. Active Record is the Class that gives a lot of functionality to all the models relating the database. It is the parent class, from which all model objects inherit and therefore, they know how to communicate with the database. 

Another note: Maybe in Listings 2.14 and 2.15 you will wonder why microposts is in plural and user is in singular?

```
Listing 2.14: A user has many microposts. app/models/user.rb

class User < ApplicationRecord
  has_many :microposts
end
```

```
Listing 2.15: A micropost belongs to a user. app/models/micropost.rb

class Micropost < ApplicationRecord
  belongs_to :user
  validates :content, length: { maximum: 140 }
end
```
Good news! Rails understands plural and singular. So when we are speaking about many posts, we use plural, whereas when we speak about one user, we use singular. 

REST Overview: [A Brief Intro to REST](https://www.infoq.com/articles/rest-introduction)

Overview: [Rails Guides](http://guides.rubyonrails.org/v3.2.9/getting_started.html): too difficult for a beginner, if you don't know something, skip. Read it to see what you understand out of it. 

More Details: [Tutorial's Point: Rails](https://www.tutorialspoint.com/ruby-on-rails/index.htm): until the Example
