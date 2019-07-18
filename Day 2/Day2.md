# JavaScript Fundamentals

Let' slearn the fundamentals of script building

1. Hello, World,
2. Code Structure
3. The modern mode, "use strict"
4. Variables
5. Data types
6. Type Conversions
7. Operators
8. Comparisions
9. Interaction: alert,prompt, confirm
10. Condtional operators: if, '?'
11. Logical operators
12. Loops: while and for
13. The "switch" statement
14. Functions
15. Functions expressions and arrows
16. JavaScript specials

# Hello, World!
The Github repository is like a online book, here in this 30 day challenge I'm looking forward to complete the core functionality of the JavaScript.

First let's set up an working environment for this we will be using WebStrom IDE although VS Code IDE is good open source tool we will be trying out the best in the market Jet Brains WebStorm IDE and to run our scripts we will be using browser.

So first let's see how to attach a script to a webpage.

# The " script" tag

JavaScript programs can be insertred in any part of html document with the help of the script tag.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    <p>Before the script tag.....</p>

    <script>
    alert('Hello, world!')
    </script>

    <p>After the script......</p>
</body>
</html>
```

You can run the example code by clicking on the "Play" button in its right top corner.

The script tag contains JavaScript code which is automatically executed when the browsers meet the tag.


# The modern markup

the script tag has a few attributes that are rarely used nowadays, but we can find them in old code

<b>The type Attribute:</b>  
```$xslt
<script type="">
```

The old standards HTML4 required a script to have a type. Usually it was <b>type="text/javascript"</b>.
It's not required any more. Also, the modern standard totally changed the meaning of this attribute. Now it can be used for
JavaScript modules. but that's an advanced topic, but we'll talk about modules later in another part of the tutorial.

<b>The language Attribute</b>

```html
<script language="">

</script>
```

The attribute was meant to show the language of the script. As of now, this attribute makes no sense, the language is 
JavaScript by default. No need to use it.

<b>Comments before and after scripts</b>

In really ancient books and guides, one may find comments inside script tag, like this,
```html
<script type="text/javascript">
<!--
...
-->
</script>

```

This trick isn't used in modern JavaScript. these comments were used to hide the JavaScript code from old browsers that
didnt know about a script tag. Since browsers born in the last 15 years don't have this issue, this kind of comment can
help you identify really old code.

# External scripts

if we have a lot of JavaScript code, we can put it into a separate file.

The script file is attached to HTML with the src attribute:
```html
<script src="/path/to/script.js">

</script>
```

Here /path/to/script.js is an absolute path to the file with the script (from the site root).

it is also possible to provide a path relative to this current page. For instance, `src="script.js"` would mean a file  `script.js` in the current folder.

We can give full URL as we, for instance:
`<script src="https://cdnjs.cloudfalre.com">`

<b>To attach several scripts, use multiple tags:</b>

```html
<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>
...
```

<b>Please note:</b>

As a rule , only the simplest scripts are put into HTML. More complex ones reside in separate files.

The benefit of a separate files is that the browsers will download it and then store it in its <a href="">cache</a>

After this, other pages that want the same script will take it from the cache instead of downloading it. So the file is actually downloaded only once

That saves traffic and makes the page load faster.

If src is set, the script content is ignored.

A single `<script>` tag can't have both src and attribute and code inside
```html
<script src="file.js">
alert(1); // the content here gets ignored, 
</script>
```

We must choose: either it's an external `<script src="..."` or a regular `<script>` with code.

The example above can be split into two scripts to work:
```html
<script> src="file.js"</script>
   
    <script>
        alert(1);
    </script>

```

# Summary 

- We can use a `<script>` tag to add JavaScript code to this page.
- The `type` and `language` attributes are not required.
- A script in an external file can be inserted with 
```html
<script src="path/to/script.js"></script>
```
There is much more to learn about browser scripts and their interaction with the web-page. but let's keep in the mind that this part
of tutorial is devoted to the JavaScript language, so we shouldn't distract ourselves from it. We'll be using browser as a way to 
run JavaScript, which is very convenient fro online reading, but yet one many.