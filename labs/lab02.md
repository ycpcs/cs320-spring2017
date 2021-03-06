---
layout: default
title: "Lab 2: Web Applications I"
---

Getting Started
===============

Import [CS320\_Jetty.zip](CS320_Jetty.zip) and [CS320\_Lab02.zip](CS320_Lab02.zip) into Eclipse (**Import &rarr; General &rarr; Existing Projects into Workspace &rarr; Archive File**).

You should see two new projects in your workspace, **CS320\_Jetty** and **CS320\_Lab02**.

See **AddNumbers.java**, **\_view/addNumbers.jsp**, and **AddNumbersServlet.java** to understand how the model, view, and servlet classes work for the AddNumbers example.

To run the AddNumbers webapp, run **Main.java** as a Java application and enter the following URL in your web browser:

> [http://localhost:8081/lab02/addNumbers](http://localhost:8081/lab02/addNumbers)

**NOTE:** If you get a mass of Java JSP compiler errors returned from the local host, as well as a heaping pile of red text in the Eclipse console, go to the [Notes for Lab 2 Page](lab02_notes.html) for instructions on solving the problem.  There are also some additional notes at the bottom of that page for other problems that you might encounter.

Your Task
=========

Implement the **GuessingGameController** class so that it implements a guessing game where the user thinks of a number between 1 and 100 and the web application tries to guess it.

See **GuessingGame.java**, **\_view/guessingGame.jsp**, and **GuessingGameServlet.java** to understand how the model, view, and servlet classes work.

To run the webapp, run **Main.java** as a Java application and enter the following URL in your web browser:

> [http://localhost:8081/lab02/guessingGame](http://localhost:8081/lab02/guessingGame)

Lastly, implement JUnit tests to test the **GuessingGame** and **GuessingGameController** classes.

Submitting
==========

When you are done, submit the lab to the Marmoset server using the method below.


From a web browser
------------------

Save the project (**CS320\_Lab02**) to a zip file by right-clicking it and choosing

> **Export...&rarr;Archive File**


Upload the saved zip file to the Marmoset server as **lab02**. The server URL is

> [https://cs.ycp.edu/marmoset/](https://cs.ycp.edu/marmoset/)


