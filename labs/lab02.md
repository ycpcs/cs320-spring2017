---
layout: default
title: "Lab 2: Guessing Game Webapp"
---

Getting Started
===============

Import [CS320\_Jetty.zip](CS320_Jetty.zip) and [CS320\_Lab02.zip](CS320_Lab02.zip) into Eclipse (**Import &rarr; General &rarr; Existing Projects into Workspace &rarr; Archive File**).

You should see two new projects in your workspace, **CS320\_Jetty** and **CS320\_Lab02**.

Your Task
=========

Implement the **GuessingGameController** class so that it implements a guessing game where the user thinks of a number between 1 and 100 and the web application tries to guess it.

See **GuessingGame.java**, **\_view/guessingGame.jsp**, and **GuessingGameServlet.java** to understand how the model, view, and servlet classes work.

To run the webapp, run **Main.java** as a Java application and enter the following URL in your web browser:

> [http://localhost:8081/lab02/guessingGame](http://localhost:8081/lab02/guessingGame)

If you have time, implement JUnit tests to test the **GuessingGame** and **GuessingGameController** classes.
