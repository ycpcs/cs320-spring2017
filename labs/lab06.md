---
layout: default
title: "Lab 6: ORM"
---

# Getting Started

Download [CS320\_Lab06.zip](CS320_Lab06.zip). Import it into your Eclipse workspace (**File&rarr;Import...&rarr;General&rarr;Existing projects into workspace&rarr;Archive File**). You will see a project called **CS320\_Lab06** in the Package Explorer.   (You will also need to have the **CS320_Derby** project in your workspace, which should already be there from [Lab 4](lab04.html).)

Start by creating **test.db**, which is the [books database](../lectures/lecture09.html).  Execute the **DerbyDatabase** class as a Java application: you should see the following output:

    Creating tables...
    Loading initial data...
    Success!

If you refresh your **CS320_Lab06** project, you should see the **test.db** directory.

You may work individually or with a small group.

# Task

In the lab skeleton you will find a program called **TitleQuery** which demonstrates using an ORM interface to find all books that have the title entered by the user (along with the author information).

Your task is very similar to [Lab 5](lab05.html), except that rather than directly executing database queries/statements, you will add methods to the **IDatabase** interface and implement them in **FakeDatabase** and **DerbyDatabase**.

Tasks:

Using **TitleQuery** as a model, write your own programs to do the following:

1. Find all books written by the author whose last name is specified. Return the books in the same form as the **TitleQuery** program.
2. Given the full (first and last) name of an author, a title, and an ISBN, insert the book into the database. The program should add a new tuple to the authors table if the author doesn't already exist. If the author does exist already, the program should use that author's **author\_id**.  Use the SQL **insert** statement to insert the new tuple(s).

## Hints

For the first task, add the following method to **IDatabase**:

    public List<Pair<Author, Book>> findAuthorAndBookByAuthorLastName(String lastname);

Implement it in **FakeDatabase** and **DerbyDatabase**.  Start by implementing the method in **FakeDatabase** (just have the method in **DerbyDatabase** throw an **UnsupportedOperationExecption**.)

For the second task, do a query to see if the author exists.  If it doesn't, insert it.  (Note: you will want to allow the database to automatically assign an author id).  Then, use the author id to insert a new tuple into the books relation (again, the database will automatically assign a book id).  Note that the entire operation should be executed as part of a single transaction.

<!-- vim:set wrap: ­-->
<!-- vim:set linebreak: -->
<!-- vim:set nolist: -->
