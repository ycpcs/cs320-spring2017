---
layout: default
title: "Lab 5: JDBC"
---

Getting Started
===============

Download [CS320\_Lab05.zip](CS320_Lab05.zip). Import it into your Eclipse workspace (**File&rarr;Import...&rarr;General&rarr;Existing projects into workspace&rarr;Archive File**). You will see a project called **CS320\_Lab05** in the Package Explorer.  (You will also need to have the **CS320_Derby** project in your workspace, which should already be there from [Lab 4](lab04.html).)

The lab contains a database called **test.db** which is the books database described in [Lecture 9](../lectures/lecture09.html).

You may work individually or with your one of more members of your team.  If you choose to work as a **team**, you **MUST** truly work on the lab in a collaborative fashion.  You **MUST** also indicate with comments at the top of your submission which members of your team contributed to the solution, and the percentage contribution of each team member, including yourself.  Make sure that the percentage contributions you assign add up to 100%.  Each contributing team member must then submit the same solution to Marmoset, with the exception that each member individually assesses the relative effort of all contributing members.  Your individual grade on the lab will be based on the quality of your team's solution, multiplied by your relative effort.

**NOTE:** You will each be individually responsible for being able to construct SQL queries, to establish a connection between a Java program and a SQL database, and to write SQL queries embedded in Java code.  This **WILL** come up on the exam.

Task
====

In the lab skeleton you will find a program called **TitleQuery** which demonstrates basic JDBC tasks such as loading a driver, connecting to a database, creating and executing a prepared statement, and iterating through results returned from a query.

Using **TitleQuery** as a model, extende the program to do the following:

**(1)** Find all books written by an author whose last name is specified by the user. Return the books in the same form as the **TitleQuery** program, but sorted in ascending order by title.

**(2)** For an existing author, given the full (first and last) name of an author, a title, an ISBN, and the year that the book was published, insert the book into the database.  Your program must first retrieve the existing author's **author\_id** before inserting the new book entry into the **books** table.

**(3)** Modify the above to allow insertion of a new book for an author that is not already in the database.  In this case, the program must first add the new author to the **authors** table, and then retrieve the auto-generated **author\_id** for the new author, before inserting the new book into the **books** table.  Hint: This requires multiple steps: attempt to retrieve the **author\_id**.  If the result set is empty, add the new author to the **authors** table.  Then, retrieve the **author\_id** that was automatically assigned for the new author.  Now you can insert the new book into the **books** table.  Use the SQL **insert** statement to insert the new tuple(s).

Submitting
==========

When you are done, submit the lab to the Marmoset server using the method below.

From a web browser
------------------

Save your project (**CS320\_lab05\_username**) to a zip file by right-clicking it and choosing

> **Export...&rarr;Archive File**


Upload the saved zip file to the Marmoset server as **lab05**. The server URL is

> [https://cs.ycp.edu/marmoset/](https://cs.ycp.edu/marmoset/)
