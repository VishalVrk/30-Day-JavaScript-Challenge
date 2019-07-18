# Day 1

## The JavaScript language

Here we learn JavaScript starting from scratch and go on to advanced concepts like OOP , We concentrate on the language itself here with minimum environment specific notes

## An Introduction to JavaScript

Lets see whats so special about JavaScript what we can achieve with it and which other technologies play well with it

## What is JavaScript?

JavaScript was initially created to "Make web pages alive".

- The Programs in this language are called scripts. they can be written right in the HTML and execute automatically as page loads
- Scripts are provided and executed as plain text. they dont need a special preparation or a compilation to run
- In this aspect JavaScript is very different from Java

## Why JavaScript ?

- When JavaScript was created, it initially had another name "LiveScript". But Java language was very popular at that time. so it was decided that 
positioning a new language as a "Younger Brother" of Java would help

- But as it evolved JavaScript became a fully independent language, with its own specification called ECMA Script and now it has no relation 
with Java at all

- At present, JavaScript can execute not only in the browser, but also on the server or actually on any device where there exists a special Program
called the JavaScript engine 

The browser has an embedded engine sometimes its also called a "JavaScript virtual Machine"

Different enginer have different "codenames" for example:

```
V8 - Chrome and Opera
SpiderMonkey - Firefox
```
There are other codenames like "Trident" "Chakra" for different versions "IE",

```
"ChakraCore" for Microsoft Edge
"Nitro" and "SquirrelFish" for Safari
```

The terms above are good to remember, because they are used in the developer articles on the internet. We will use them too. for instance,
If "A feature X is supported by V8" then it probably works for both Chrome and opera

## How does the engine work?

Engine are Complicated.But the basics are easy 

### 1. The engine(embedded if its a browser) reads ("parses") the scripts
### 2. Then it converts ("compiles") the script to the Machine language.
### 3. And then the Machine code runs pretty fast
The engine applies optimization on every stage of the process. it even watches the complied script as it runs, analyzes the data that flows through
it and applies optimization to the Machine code based on that knowledge. at the end scripts are quite fast


## What can in browser JavaScript do?

- The modern JavaScript is a "safe" Programming language. it does not provide low-level acess to memory or CPU, because it was initially created 
for browsers which do not require it

- The capabilities greatly depend on environment that runs JavaScript. 

- For instance Node.js supports functions that allow JavaScript to read/write arbitary files, perform network requests etc.

- In browser JavaScript can do everything related to webpage manipulation interaction with the user and the webserver.

#### For instance, in-browser JavaScript is able to:

- Add a new HTML to the page, change the existing content, modify styles.

- React to user actions, run on mouse clicks, pointer movements, key presses.

- Send requests over the network to remote servers download upload files (AJAX and COMET)

- Get and set cookies, ask questions to the visitors, show messages

- Remember the data on the client side ("local storage")

## What cant browser JavaScript cant do ?

JavaScript's abilities in the browser are limited for the sake of the user's safety. the aim is to prevent an evil webpage from 
accessing private information or harming the user's data

#### The examples of such restrictions are

- JavaScript on Webpage may not read/write arbitar files on the hard disk , copy them or directly execute programs. it has no direct accessing
to OS system functions

- Modern browsers allow it to work with files, but the access is limited and only provided if the user does certain actions like "dropping" a file 
into browser window or selecting it via an input tag

- There are ways to interact with camera/microphone and other devices, but they require a user's explicit permission. So a JavaScript-enabled
page may not sneakly enabled a web-camera, observe the surroundings and send the information to the NSA

- Different tabs/Windows genrally do not know about each other. sometimes they do, for example when one window uses JavaScript to open the other one.
but even in this case, JavaScript from one page may not access the other if they come from different sites(from a different domain, protocol or port)

- This is called the Same Origin Policy to work around that both pages must contain a special JavaScript code that handles data exchange.

- The limitation is again for user's safety A page from http://anysite.com which a user has opened must not be able to access another browser tab with the http://gmail.com and steal information from here.

JavaScript can easily communicate over the net to the server where the current page came from. but its ability to receive data from other sites/domains is crippled
though possible , it requires explicit agreement (expressed in HTTP headers) from remote side. once again, thats safety limitations such limits do not 
exist if JavaScript is used outside fo the browser,for example on a server, Modern browsers also allow installing plugin/extensions which may get extended
permissions

## What makes JavaScript unique?

There are atleast three great things about JavaScript

- Full intergration with HTML/CSS
- Simple things done simply.
- Supported by all major browsers and enabled by default 

Combined all the three things exists only in JavaScript and no other browser technology.That what makes JavaScript unique that's why its the most widespread tool to create browser interfaces.

While planning to learn a new technoloy its beneficial to check its perspectives. So let's Move on to the modern trends that include new
languages and browser abilities

## Languages over JavaScript

The syntax of JavaScript does not suit everyones need Different people want different features. That's to be expected because project and requirements are different for everyone.

So recently a plethora of new languages appeared which are transpiled(converted) to JavaScript before they run in the browser.

Modern tools make transpilation very fast and transparent, actually allowing developers to code in another language and autoconverting it
"Under the hood"
```
CoffeeScript is a "syntactic sugar" for JavaScript it introduces shorter syntax, allowing to write more precise and clear code. Usually
Ruby devs like it.

TypeScript is concentrated on adding "Strict data typing", to simplify development and support of complex systems.
it is developed by Microsoft.

Dart is a standalone language that has its own engine that runs in non-browser environments(like mobile apps). it was initially offered by google
as a replacement for JavaScript, But as of now browseres require it to be transpiled to JavaScript just like the ones above.
```

#### There are more of course even if we use one of theose languages we should also know JavaScript, to really understand what we're doing 

## Summary

- ### JavaScript was initially created as a browser-only language, but now it is used in many other environments as well but now it is used in many other environments as well 
- ### At this movement JavaScript has a unique position as the most widely-adopted browser-langauge with full intergration with HTML/CSS there are many languages that get transpiled to JavaScript and provide certain features. it is recommended to take a look at them at least briefly, after mastering JavaScript.