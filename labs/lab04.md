---
layout: default
title: "Lab 4: SQL, Queries, Joins"
---

Getting Started
===============

Download [CS320\_Derby.zip](../resources/CS320_Derby.zip) and [CS320\_Lab04.zip](CS320_Lab04.zip). Import them into your Eclipse workspace<br> (**File-\>Import...-\>General-\>Existing projects into workspace-\>Archive File**). You will see a projects called **CS320\_Derby** and **CS320\_Lab04** in the Package Explorer.  You will be running the **SQLDemo** class in the **CS320_Lab04** project.

Setting up the database
=======================

Execute the **SQLDemo** class as a Java application.

Use **create table** commands to create **books** and **authors** tables. From the **SQL\>** prompt, enter the following commands:

    create table books (
        book_id int
            primary key generated always as identity (start with 1, increment by 1),
        author_id int,
        title varchar(50),
        isbn varchar(20)
    );

    create table authors (
        author_id int
            primary key generated always as identity (start with 1, increment by 1),
        author_lastname varchar(40),
        author_firstname varchar(40)
    );

Next, use **import** commands to load data into these tables:

    import books books.csv;

    import authors authors.csv;

Your database is now populated with data.

Now, use the **alter table** command to establish **author_id** as a foreign key in the **books** table.  Enter the following command:

    alter table books
        add foreign key (author_id)
        references authors (author_id);
    
The schemas of the database tables are described in the notes for [Lecture 9](../lectures/lecture09.html).

Task
====

Try executing some queries to retrieve the following information:

-   the titles of all books written by F.G. Smallfinger
-   the titles of all books written by Callus Tacticus
-   the author name (first and last) and the ISBN number of the book with the title "First Flights in Witchcraft"
-   attempt to insert a new book into the **books** table, with an **author_id** that does not appear in the **authors** table (this attempt should fail, due to specifying an invalid **foreign key** for **author_id**)
-   insert yourself as a new author in the the **authors** table (do not specify an author_id, Derby will do that for you, since **author_id** is the auto-generated primary key for the **authors** table)
-   retrieve the **author_id** from the **authors** table for your entry
-   insert a new book into the **books** table, using your new **author_id**

Each query should be terminated with a semicolon (**;**). For example, here is session showing a query to select all of the tuples in the **authors** table (user input in **bold**):

<pre>
SQL> <b>select * from authors;</b>
AUTHOR_ID AUTHOR_LASTNAME AUTHOR_FIRSTNAME
--------- --------------- ----------------
        1     Smallfinger             F.G.
        2       Whittlbey           W.H.J.
        3          Earwig          Lettice
        4         Lightly             W.E.
        5        Tacticus           Callus
OK (5 rows(s))
</pre>

[Here is a great tutorial website for learning SQL](http://www.w3schools.com/sql/default.asp)

# What to submit

Create a text file containing, for each query listed above:

* The exact query you came up with
* The exact output of the query

You can cut and paste these from the console window as shown above.

Save your queries and outputs in a plain text file and upload the text file to Marmoset as **lab04**.
