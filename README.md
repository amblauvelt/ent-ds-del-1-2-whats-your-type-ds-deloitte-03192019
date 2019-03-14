
# What's Your Type?


## Introduction
Imagine that you've got a spreadsheet full of data, but it's pretty messy. The person and company names all have different capitalization, the dates are in all kinds of different formats, there are longer chunks of text that you need to extract information from. Some of the data is missing or has invalid values.

One of the things programming in Python will allow you to do is to import a file like that, loop over the data and automate the cleaning of it so in the future when you get similar data you can just run it through the same (or a similar) program to clean it up really quickly.

By the end of next week, you're going to be able to import a file, loop over all of the data, clean it up and then save it back to a file again. Over the next few lessons we'll be introducing the key concepts you'll need to be able to do that.

In this lesson, we'll introduce a couple of key concepts that the rest of your programming will depend upon - **variables** (for storing information) and **data types** (for working differently with different types of data).


## Objectives
You will be able to:
* Explain how variables are a key element of programming 
* List some common data types in Python
* Pick the appropriate Python data type for a given type of information

## Variables

A variable is a representation of some data that can be changed over time. 

Hit `shift-enter` to run the two cells below . . .


```python
name = "Sally"
name
```


```python
name = "Bill"
name
```

As you can see, we started by **assigning** the value of "Sally" to the variable called `name` 
We then changed the value of the variable called `name` to "Bill"

Variables are one of the most important building blocks in programming as they allow us to store information, change it and act based on it's values . . . Run the next few cells using `shift-enter` . . .


```python
first_name = "Jessie"
last_name = "Warden"
full_name = first_name + " " + last_name
full_name
```


```python
if last_name == "Warden":
    print("I think it's Jessie")
else:
    print("I don't think it's Jessie")
```


```python
last_name = "Something Else"
if last_name == "Warden":
    print("I think it's Jessie")
else:
    print("I don't think it's Jessie")
```

## Data Types

Every variable has a data type associated with it in Python. You can find the type using the following code:


```python
type(first_name)
```

As you can see if you run the cell above, the data type for the first_name variable is "str" which is short for "string".

The **string** data type is one of the most common and flexible data types. When you import data into Python, it'll often start off as a string. If something can be represented by a set of characters, it can have a data type of string. Pretty much the only thing you can't store in a string is a binary file - something like an image or a video.

Even though you *can* store almost anything in a string, you don't always want to.

For example, lets say you have sales figures for three stores in a region last month and want to know what the total sales were, storing the information as variables with a data type of string might not work the way you'd want it to:


```python
store_1_sales = "20000"
store_2_sales = "30000"
store_3_sales = "15000"
regional_sales = store_1_sales + store_2_sales + store_3_sales
regional_sales
```

If you run the code above you'll see *that* isn't what you want! So we've going to have to change the type of the three variables to a type that allows for math. One good data type for that is the **Integer** (for whole numbers - no fractions or decimals).


```python
store_1_sales = "20000"
store_2_sales = "30000"
store_3_sales = "15000"
regional_sales = int(store_1_sales) + int(store_2_sales) + int(store_3_sales)
regional_sales
```

## Common Data Types in Python
Some of the most common, simple data types in Python are:
* **String** - Pretty much any set of characters can be stored as a string. Strings are a good starting point for most of your data, but you'll have to convert data if you want to do math with it, use it easily to return "true" or "false", or want to operate on dates and/or times.
* **Integer** - Perfect for round numbers that you want to do math on. Number of students in a class, houses in a city or the number of pets that a particular family owns would all be great examples *(assuming there aren't any half demolished houses and that nobody owns a quarter of a pet goldfish!)*
* **Floating point** - Ideal for numbers that require more precision than integers. It could be a stock price in dollars, the average age of a group of people, or the exact height of a person in meters. Be careful though. Floating point math in computers is not absolute, so occasionally you'll do math and the computer will return an answer of 23.00000001 or 22.99999999999 when if you'd done the same math yourself you'd see that actually the real answer is exactly 23.0
* **Boolean** - Perfect for storing a value that is either **true** or **false**. `has_children` or `is_employed` would be examples of variable names that might want to have a boolean data type.
* **DateTime** - If you want to compare dates, calculate the length of an event in hours or figure out how long it is until a discount code expires, you probably want to use a DateTime data type. Very powerful, but be careful. It might seem easy to write code using date times, but make sure to think about issues like timezones and daylight saving time - otherwise you might get some unexpected results!

## Summary

In this lesson we introduced the concept of variables and data types. We also provided a summary of some of the more popular, simple Python data types *(we'll talk about more complex data types like arrays, sets, lists and collections later)*. We also looked at the use cases for those popular variables.

In the next lesson we're going to look at some common data cleaning tasks and how we can perform them on variables.


