#How Does the Internet Work

We want to do websites and things like that. So let's say a couple of words about the Internet. 

##Internet is more than websites
We know that we need Internet to load a website (webpage) in your browser (a browser is a program that you have on your computer that reads HTML and displays the content of a website in a human-friendly beautiful website, such programs are Google Chrome, Mozilla Firefox, Internet Explorer, Opera, Safari, Edge, etc. Hopefully, they will be able to display the website in a similar way.) 

But what else do we have on the Internet? Just the websites? No. We also have other things that are not websites. Such are your mobile applications on your phone (an application is another word for a program), the Internet connected cameras, chats, e-mails and many others. In short the Internet is quite a general purpose thing and you can exchange any data on it. Obviously, you have different protocols to transfer data depending on whether it is a website, a mobile app or something else. For websites, we have http or https. 

##A couple of terms
**Website**: nothing more than a bunch of interrelated files that work together, written on HTML and other languages

**Server**: a place where you store and run your website. You can store and run your website files on your own computer. Nothing stops you from that. However, if you have a bigger site that more people will visit, with more content, it is a good idea not to store it on your local computer (local computer = your own computer). Why is that? Because you can have an electricity shortage during which people won't be able to open your site, your computer may crash and loose your site, your Internet connection may be down, etc. So you give your site to another computer, a much powerful one, in a datacenter (a place with a lot of powerful computers) and you usually pay the owner of the computer to guarantee that your site is alive 24/7. So the owner of the server addresses all sorts of problems that you may have at home. So a server is a powerful computer where people put their sites. 

**Protocol**: I already used the term, sorry for that. Now I explain. As we said, there is a lot of data that gets transferred by the Internet. Something should tell the servers what sort of data is to be sent in and out. We use protocols. HTTP protocol is used for websites, pdfs, and others and is the one that the browsers read. 

**Address bar**: the place on the browser where you type your address of the page you want to open (for example, github.com or www.amazon.com)

**URL**: the name of the site, the address of the site, this www.amazon.com thing that you write 

Now we are ready to see...

##How the Internet works
Every time a user (meaning you) type an address (meaning url) into the address bar, information goes from your computer to the server. Let's try with an example. It is as if, you give an address to a postal pigeon together with a letter and the pigeon will go to the server to get the site from there. The letter usually consists of information about who you are like cookies and others. The pigeon reaches the server that is like a big building and goes to the reception (called, port 80) where a program exists that builds together the pack of HTML files for the pigeon and the pigeon returns with a letter consisting of the website. It gives the letter to the browser and the browser reads it and displays the website to you. 

That's about it in the most simplifies words :) 

##Some other terms

When you read different sites on the topic, you will bump into the following terms as well: 

**Client**: this is you, the user, the computer who requested the files from the server

**Ports**: these are like the rooms in the building if we picture the server as a building. When you give your website to a server, it gets accommodated in a room (a port) and starts running constantly. So your program on the site runs 24/7 because if it stops, the user will get an error when approaching the site. When there is a website accommodated in a room (called a port), the door of the room is opened and the website can be approached. One server can have a lot of rooms where different sites live and when a pigeon comes to the reception, there is a receptionist (a program called HTTP server or webserver) and the receptionist checks the room (port) of the website needed and sends its own pigeon to bring the site to the reception. 

**Gateways:** Sometimes there are huge websites with lots and lots of users, like facebook.com. Such websites are not in one server. They have exactly the same copy of the website in hundreds and hundreds of servers. They are like a whole park of same buildings with the same website on their ports. At the entrance of this park, there are a couple of buildings (again servers), that tell the pigeon which building has a free receptionist to get the pigeon's letter and give back the website. These entrance buildings are called gateways. 

**Some interesting sidenotes:** 
So it turns out that protocols are like another language used for communication with servers. When a user requests information the pigeon goes to the server and depending on the protocol, the pigeon goes to the relative port with the relative receptionist. If the pigeon carries a letter with an HTTP protocol, it goes to port 80 where there is the receptionist program that understands HTTP. Pigeons carrying letters with FTP protocols go to port 20 or 21 (FTP is another protocol used for copying files from one machine to another), etc. 

And what about HTTP and HTTPS? They are similar except that the "s" in the end stands for "secured". As for now, the only thing you need to remember is not to give your passwords, credit card details, etc. to sites that are using the http protocol. Your data may be read by third-parties. 

 ***
Additional Resources: If you are interested in learning more terms, here is a quick guide from [Digital Ocean] (https://www.digitalocean.com/community/tutorials/an-introduction-to-networking-terminology-interfaces-and-protocols): read until Network Layers. However, as a beginning you won't need that much details so feel free to skip to the next section if you are not interested or you find the tutorial difficult to understand. 

The continuation of the topic, written by me :) Give link

Here is a another very descriptive tutorial, which goes into more details than the above description: [20 Things I Learned about Browsers and the Web] (http://www.20thingsilearned.com/en-US)
