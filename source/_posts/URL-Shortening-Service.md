---
title: URL Shortening Service
date: 2017-09-06 21:25:23
excerpt: Lets try django and then fail...
tags: 
    - python 
    - web-development
---

## Dropping this project 

<em>Why?</em>

Learning API development is fun, challanging and rewarding, but I think with internet, it is just figuring out a way how a piece of technology works by googling, reading documentation and wiring things together. You might say that there is more to this, like Databases, Scalablity and User Interfaces, but for me it is boring. I know if required, I can get quickly learn but to squeeze learning time from a full time job for a less intriguing task is more like drinking poison for not setting foot on moon.

## <em>(2017-09-05)</em>
Starting out with basic Django toolchain setup.

Django Apps are independent modules doing a specific task.
To create: 
<code>python manage.py startapp MyApp</code>

Model are abstracted representation of data for database. To make one just create a class that inherits from models.model in models.py and register that class in admin.py, so that it can be visible in Django admin.

## <em>(2017-09-06)</em>
Need to create and run migrations after every change in a model. It create a new file everytime specifying operations that takes Database from one state to another. Creates a lot of files !

Before adding new fields to existing models, Django needs some value to populate in existing objects. We can pass null=True or default=”some value” to the field constructor.
For eg. someObj = models.CharField(max_length=64, null=True)
someObj = models.CharField(max_length=64, default=”some default value”)

## <em>(2017-09-07)</em>
Generating random short url from given url.

Check if URL is already shortened before. If yes return short URL.
If not, Generate random string, check if it is not assigned for an existing URL.
If yes, go to step 2
Else save string as short url for new URL
A naive approach (need further investigation)

Using model manager for returning only active url from the database. So, if an url is marked as
active = **False**, then it will not show up in any querysets that will be returned from overridden methods.

[Code](https://github.com/narveersingh/chotelinks-platform)
