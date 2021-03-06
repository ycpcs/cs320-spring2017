---
layout: default
title: "Lab 2A: Web Applications II"
---

Your Task
===============

This lab builds upon the **AddNumbers** and **GuessingGame** examples from [CS320\_Lab02](lab02.html).  It will "force" you to investigate, explore, and learn the structure of a WebApp, from the server (**main()**), through **Web.xml**, the servlets, the controllers, the model, and the JSPs, as well as how to refactor an entire project space.  You will need to have this kind of familiarity with the WebApp architecture in order to get started on your team project, as well as to be able to make significant technical contributions to any and all aspects of your team project.  

**NOTE: This lab will require a significant effort, and you should start on it as soon as possible.**

You have six tasks:

* First, make a copy of the **CS320_Lab02** project, and then refactor the copy so that it no longer refers to **Lab02**, but instead, refers to your YCP user name.  Your project name will be **CS320\_username**.  After you refactor the project name, you will also need to refactor the package names, change the locations specified in **Web.xml** and the JSP's, as well as the context folder specified in **main()**. Verify that both of the **AddNumbers** and **GuessingGame** WebApps still work - you will no longer be able to use the URL links included on the **CS320\_Lab02** page, you will need modify those URLs to replace **lab02** with your username.  You should save those new URLs as bookmarks in your browser.

* Add a third number to the **AddNumbers** example, such that a third number field shows up on the **AddNumbers** web page, and the returned result is the sum of all three numbers.  Your code should check for the same errors as the existing **AddNumbers** example does.  This problem will require changes to the **AddNumbers** servlet, controller, and JSP.

* Create a new WebApp based on the **AddNumbers** example, called **MultiplyNumbers**.  This WebApp should accept two numbers from the user and return the product of those numbers.  It should check for all of the same errors that the existing **AddNumbers** example does.  This problem will require changes to **Web.xml**, and the controller (modify the existing **AddNumbersController** and rename it **NumbersController**, rather than creating a new controller).  You will also need to create a new **MultiplyNumbers** servlet and new **MultiplyNumbers** JSP file, both of which can be based off the **AddNumbers** versions of those files.

* After you have modified **AddNumbers** and created **MultiplyNumbers** and have them both completely working, modify the existing **Index** JSP file so that you can access all three of the servlets (**AddNumbers**, **MultiplyNumbers**, and **GuessingGame**) from the **Index** page.  Implement this is a collection of three "submit" buttons, each labelled with one of the three functions.  Each button will result in **IndexServlet** issuing a **doGet** to the appropriate JSP.

* After all of the above are working, create a common model class (**Numbers.java**) for **AddNumbers** and **MultiplyNumbers**, such that the numbers submitted through the HTTP request are stored in the model, along with the result.  You will need **get** and **set** accessor methods for all model fields, along with a constructor for the model class.  Look at the model for the **GuessingGame** WebApp as a template - and how that model is instantiated, initialized, and accessed.  The corresponding JSP's should pull the data directly from the **Numbers** model, rather than from the HTTP request.  Again you can look at the **GuessingGame** implementation to see how this is done.

* As part of this exercise, you should also implement a complete set of test cases for the controller and model classes.  You should be implementing those test cases as you develop each of the above tasks.  A significant portion of the effort on your team project will be creating an extensive and comprehensive set of JUnit test cases - **WHILE YOU ARE DEVELOPING YOUR TEAM PROJECT**.

* **NOTE: I HIGHLY recommend that you save your work after each step.  Archive the project at each stage, and submit it to Marmoset.  That will provide a back-up in case you lose your work, or if you need to revert to a previous version of your work. In a few weeks, we will cover version control, and you will set up your own "Git" accounts and repositories.  For the time being, Marmoset can serve as your version archive.**


Submitting
==========

When you are done, submit the lab to the Marmoset server using the method below.

From a web browser
------------------

Save your project (**CS320\_username**) to a zip file by right-clicking it and choosing

> **Export...&rarr;Archive File**


Upload the saved zip file to the Marmoset server as **lab02a**. The server URL is

> [https://cs.ycp.edu/marmoset/](https://cs.ycp.edu/marmoset/)


