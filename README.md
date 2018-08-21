
# What Are Libraries?

## Introduction

Buildings with lots of books are not the only type of library now that we are programmers. We have another type of library, which you'll likely be using much more of. Similar to a conventional library, programming libraries are collections of things. Except the things in this case are pieces of code. We'll introduce exactly what are libraries, what they are used for, and how to use them. 

![library_open_gif](https://i.gifer.com/EXxP.gif)

## Objectives
* What is a Library?
* Why use a Library?
* How to Use a Library

## What is a library?

A library, in it's most basic form, is a collection of reusable, organized code. It is intended to be a central place for a subset of common and or complex operations that we or other programmers can then access and use or reuse in a project. 

Let's say we are a graphic designer and we're frequently creating fliers for our company, whose logo is a very detailed bumble bee. We frequently need to create new fliers for different events. How would you like to re-create the complex bumble bee every time? Probably not a whole lot. So, instead, you create a file that has that bumble bee and you import the bumble bee into your new project and use it there. Now, you have the exact same bumble bee to use and reuse in every project. And now that the company's logo is so consistent, it's generating more business and hiring more designers. Instead of those designers creating their own bumble bees, they can also just use the one logo we created. If you take the bumble bee out of this example and replace it with functions and complex code, you have a pretty good image of a programming library.

Typically, the libraries we use in this course will be industry standard libraries that are widely used, heavily documented, and frequently updated. This means that the library we import in our program is actively being maintained and updated so that it is as easy to use and efficient as possible. That, ultimately, is the goal of a programming library. The end user (us) doesn't need to know how the library is structured or how the code is performing an operation. It just needs to offer an easier, more streamlined and efficient way of doing something when compared to creating the tool or library ourselves.

A great example of a widely used library in Python would be the **[Requests](http://docs.python-requests.org/en/master/)** library. Feel free to look at the documentation and get a sense for what a library looks like, but don't worry about understanding how it works just yet.

## Why do we use libraries?

As programmers, we have a lot of hard problems to solve everyday. Maybe we are a software engineer who needs to create a website that lists the tasks we need to do. This website would take in some text and add it to a running list of tasks we have. Like so:

```python
- 'BUY GROCERIES'
- 'PAY credit CARD BILLS'
- 'DO homeWork'
```

That list looks fine, but let's say we want our program to automatically format our list of tasks so that they are all relatively uniform and easy for our users to read. Well, that sounds like it might be a lot of extra code to figure that out. This doesn't seem like an ideal solution considering that the point of our application is to make it easy for our users to create a list of things they need to do. 

Thankfully, it doesnt have to come to that since there are libraries that have this type of functionality for us. For example many languages like Python have built-in libraries that perform string manipulation and formatting. So, say we would like to make it so each task is in title case. That is, each word begins with a capital letter and the rest is lower case. We do not need to write code that performs that operation. Instead, we can just call the functions from a library, like the built-in Python library that will perform this operation.

So, now what could have been a complex set of functions that took hundreds of lines of code can now just be one or two lines of code that are optimized to change a string into title case.

```python
"BUY GROCERIES".title() => "Buy Groceries"
```

## How do we use libraries?

Some libraries can be built into a language, like we've seen above. But most libraries will be thing we import into our code base. Commonly used libraries in Python include but are not limited to Pandas, Plotly, and Matplotlib. To use them, we simply import them into our code.

```python
import pandas
```

> **Note:** If using a library for the first time, it may be necessary to install it before importing. To do so, we simply use a tool like `pip` to install the library from our command line.

```
pip install pandas
```


And just like that, we now have access to the Pandas library in the project we are working on!

BUT it's actually a bit more complicated. When importing a library, there might be some more nuanced conventions to follow or we might want to make our code a bit cleaner by importing the library in a specific way. For example, the convention for importing the Pandas library is to alias it as `pd`. Which, in python, is done like the below:
```python
import pandas as pd
```

If we wanted to import only a certain function from a library we would then need to change our import to read differently as well. For example Pandas provides a function that reads data from an excel file, aptly named `read_excel`, so, currently we would need to write that as `pd.read_excel()`, but if we change our import we can be more declarative and potentially cut down on the amount of code we are writing like in the example below:

```python
from pandas import read_excel
```

Don't worry too much about these different ways to import libraries. The main thing to remember is that **to use a library we simply import it into our code** (and install it if necessary).

## Summary

In this lesson we talked about what a library is, why we would use them, and how they are used. Libraries are a tremendous tool for programmers and provide powerful ways to create concise, efficient code. 
