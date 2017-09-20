# What is CSS?
So far, you've learned about the fundamentals of HTML, including the basic structure required to set up HTML files, as well as the common HTML elements used to add content to a web page.
Unfortunately, the HTML elements that we've used to add content to a web page have resulted in fairly bland results in the browser. For example, it appears that all content seems to be the same color, have the same font, and offer no direct control over the size of the font (apart from the six different heading options). How can we make our HTML more visually appealing? 
CSS, or Cascading Style Sheets, is a language that web developers use to stylethe HTML content on a web page. If you're interested in modifying colors, font types, font sizes, shadows, images, element positioning, and more, CSS is the tool for the job!
In this unit, you'll first learn how to incorporate CSS so that you can style content. You'll also learn about CSS's basic structure and learn how to use its syntax. In later units, we'll explore in detail exactly how to change color, font options, and much more.
Let's begin!



# style
Although CSS is a different language than HTML, it's possible to write CSS code directly within an HTML file. This is possible because of the ``<style>`` element.
The ``<style>`` element allows you to write CSS code between its opening and closing tags. To use the ``<style>`` element, it must be placed inside of the head.


```HTML
<head> <style> </style> </head>
```



Once ``<style>`` is placed in the web page's head, we can begin writing CSS code.


```HTML
<head> <style> h2 { font-family: Arial; } </style> </head>
```
Don't worry about the CSS code in the example above just yet, you will learn more about the details of CSS code in later lessons.



# Structure vs Style
Although the ``<style>`` element allows you to write CSS code within HTML files, this mixture of HTML and CSS can result in code that is difficult to read and maintain.
It's common for developers to add substantial amounts of custom CSS styling to a web page. When all of that CSS code is placed within a ``<style>`` element in an HTML file, you risk the following two things:
1.	Creating a large HTML file that is difficult to read and maintain (by you and other developers). Overall, this can result in an inefficient workflow.
2.	Maintaining a clear distinction between web page structure (HTML) and web page styling (CSS).



# The .css file
Fortunately, the following solution will help you avoid creating large HTML files that mix in CSS code: a CSS file!
HTML files are meant to contain only HTML code. Similarly, CSS files are meant to contain only CSS code. You can create a CSS file by using the .css file name extension, like so: style.css
With a CSS file, you can write all the CSS code needed to style a page without having to sacrifice the readability and maintainability of your HTML file.



# Linking the CSS File
Perfect! We successfully separated structure (HTML) from styling (CSS), but why does the web page look continue to look so bland? The CSS code now lives in a separate CSS file called style.css — shouldn't that have worked without issue?
Not exactly. When HTML and CSS code are in separate files, the HTML file must know exactly where the CSS code is kept, otherwise, the styling can't be applied the web page. In order to apply the styling to the web page, we'll have to link the HTML file and the CSS file together.
You can use the ``<link>`` element to link the HTML and CSS files together. The ``<link>`` element must be placed within the head of the HTML file. It is a self-closing tag and requires the following three attributes:
1.	`href` - like the anchor element, the value of this attribute must be the address, or path, to the CSS file.
2.	`type` - this attribute describes the type of document that you are linking to (in this case, a CSS file). The value of this attribute should be set to `text/css`.
3.	`rel` - this attribute describes the relationship between the HTML file and the CSS file. Because you are linking to a stylesheet, the value should be set to `stylesheet`.

When linking an HTML file and a CSS file together, the ``<link>`` element will look like the following:


```HTML
<link href="https://www.codecademy.com/stylesheets/style.css" type="text/css" rel="stylesheet">
```



Note that in the example above the path to the stylesheet is a URL:


```HTML
https://www.codecademy.com/stylesheets/style.css
```



Specifying the path to the stylesheet using a URL is one way of linking a stylesheet. 
If the CSS file is stored in the same directoryas your HTML file, then you can specify a relative path instead of a URL, like so:


```HTML
<link href="/style.css" type="text/css" rel="stylesheet">
```


Using a relative path is very common way of linking a stylesheet.



# Review: CSS Setup
Great job! You learned how to link an HTML file and a CSS file together. 
Let's review what you've learned so far:
1. HTML and CSS are kept in separate files in order to keep code maintainable and readable, as well as keep structure separate from styling.
2. The ``<style>`` element allows you to write CSS code within an HTML file.
3. A CSS stylesheet can be linked to an HTML file using the ``<link>`` element, which requires three attributes:
•	`href` - set equal to the path of the CSS file.
•	`type` - set equal to `text/css`.
•	`rel` - set equal to `stylesheet`.
In this lesson, you learned about the two different places in which you can write CSS code, but you didn't write any CSS code at all. 
In the next lesson, you'll learn about the basic structure and syntax of CSS so that you can start using CSS on your own.
