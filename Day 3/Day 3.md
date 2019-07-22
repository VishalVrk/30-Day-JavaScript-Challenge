# Code Structure

The first thing to study is the building blocks of the code.

# Statements

Statements are synatx constructs and commands that perform actions.

We've already seen a statement

`alert('Hello', world!) ` , Which shows the message.

We can have as many statements in the code as we want. Another statement can be separated with a semicolon.

For example, here we split the message into two:

`alert('Hello'); alert('World');`

Usually each statement is written on a separate line - thus the code becomes more readable:

```
alert('Hello');
alert('World');
```

# Semicolons

A semicolon may be omitted in most cases when a line break exists.

This would also work:

```
alert('Hello');
alert('World');
```

Here JavaScript interprets the line break as an "implicit" semicolon that's also called an automatic semicolon insertion.

<b>In most cases a newline implies a semicolon. but "in most cases" does not mean the same "always"!</b>

There are cases when a newline does not mean a semicolon for example:
```
alert(3+
1
+2);
```
The code outputs 6, because JavaScript deos not insert semicolons here. it is intuitively obvious that if the line ends with a plus "+"
then it is an "incomplete expression", no semicolon required And in this case that works as intended

<b>But there are situations where JavaScript "fails" to assume a semicolon where it is really needed.</b>

Errors which occurs in such cases are quite hard to find and fix.

An example of an error

if you're curious to see a concrete example of such an error, check this code out:

`[1, 2].forEach(alert)`

No need to think about the meaning of the brackets [] and forEach yet.We'll study them later, for now it does not matter Let's just remember the result: it shows 1, then 2.

Now let's add an alert before the code and not finish it with a semicolon after alert:

``` 
alert("All fine now");
[1,2].forEach(alert)
```
Now we have "All fine now" message and then 1 and 2.

The error in the no-semicolon variant occurs because JavaScript does not imply a semicolon before brackets[...].

So, because the semicolon is not auto-inserted, the code in the first example is treated as a single statement.That's how the engine sees it:

```
alert("There will be an error")[1,2].forEach(alert)
```

But it should be two separate statements, not a single one. Such a merging in this case is just wrong, hence the error. There are other situations when such a thing happens.

It's recommended to put semicolon between statements even if they are seperated by newlines. this rule is widely adopted by the community. Let's note once again - it is possible to leave out semicolons most of the time. But it's safer - especially for a beginner - to use them.

# Comments

As time goes on , the program becomes more and more complex. it becomes necessary to add comments which describe what happens and why.

Comments can be put into any place of the script. they don't affect the execution, because the engine simply ignores them

<b>One-line comments start with two forward slash characters //.</b>

The rest of the line is a comment.It may occupy a full line of its own or follow a statement.

Like here:

```
//This comment occupies a line of its own
alert('Hello');
alert('World); //This comment follows the statement
```

<b>Multiline comment start with a forward slash an asterisk /* and end with an asterisk and a forward slash */</b>

Like this:

```html
/* An example with two messages.
This is a multiline comment.
*/
alert('Hello');
alert('World');
```

The content of comments is ignored, so if we put code insde /*....*/ it won't execute

Sometimes it comes in handy to temporarily disable a part of code:

/* Commenting out the code
alert('Hello');
*/
alert('World');

### <b>Use hotkeys!</b>

In most editors a line of code can be commented out by `Ctrl+/` hotkey for single-line comment and something like `Ctrl+Shift+/` - for multiline comments
(select a peice of code and press the hotkey). for Mac try `Cmd` instead of `Ctrl`.

Nested comments are not supported!
There may not be /*....*/ inside another /*...*/.

Such code will die with an error:
```
/*
    /* nested comment ?!?  */
/*

alert('World');
```

Please, don't hesitate to comment your code3.

Comments increase the overall code footprint, but that's not a problem at all. There are many tools which minify the code before publishing to the production server. They remove comments, so they don't appear in the working scripts. Therefore comments do not have any neagative effects on production at all.

Further in the tutorial, there will be chapter Coding style that also explains how to write better comments