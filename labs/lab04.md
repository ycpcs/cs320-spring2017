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

Use **create table** commands to create **books** and **authors** tables. From the **SQL\>** prompt, enter the following commands.  Rather than typing them, you can actually copy each command from this page and paste it into the SQL prompt - then press "Enter" to execute the command.

    create table books (
        book_id int
            primary key generated always as identity (start with 1, increment by 1),
        author_id int,
        title varchar(70),
        isbn varchar(15),
        published int
    );

    create table authors (
        author_id int
            primary key generated always as identity (start with 1, increment by 1),
        lastname varchar(40),
        firstname varchar(40)
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

Compose and execute SQL queries that retrieve the following information.  For the later queries, you will have to do some research at [w3schools](http://www.w3schools.com/sql/default.asp) in order to learn the proper SQL commands to complete the query.

Each query should be terminated with a semicolon (**;**). For example, here is session showing a query to select all of the tuples in the **authors** table (user input in **bold**):

<pre>
SQL> <b>select * from authors;</b>
AUTHOR_ID    LASTNAME FIRSTNAME
--------- ----------- ---------
        1       Adams   Douglas
        2       Adams     Scott
        3    Breathed  Berkeley
        4     Chapman    Graham
        5      Cleese      John
        6     Gilliam     Terry
        7     Hawking   Stephen
        8        Idle      Eric
        9       Jones     Terry
       10    Kahneman    Daniel
       11    Mlodinow   Leonard
       12      Newton     Isaac
       13       Palin   Michael
       14   Watterson      Bill
OK (14 rows(s))
</pre>

Make sure to verify that the results of each query are correct by comparing against the  database tables themselves.

-   the title for each book written by Stephen Hawking
-   the title and year of publishing for each book written by Douglas Adams
-   the author's name (first and last), the ISBN, and the year published for the book with the title "Something Under the Bed is Drooling"
-   all of the authors for "The Complete Monty Python's Flying Circus; All the Words, Volume 1"
-	the title and author for each of Berkeley Breathed's and Bill Watterson's books, sorted in ascending order by title
-   the author(s) and title for each book with the word "Time" or "Universe" in the title, sorted in ascending order by lastname, and then ascending by title.
-   attempt to insert a new book into the **books** table, with an **author_id** that does not appear in the **authors** table (this attempt should fail, due to specifying an invalid **foreign key** for **author_id**)
-   insert yourself as a new author in the the **authors** table (do not specify an author_id, Derby will do that for you, since **author_id** is the auto-generated primary key for the **authors** table)
-   retrieve the **author_id** from the **authors** table for your entry and insert a new book into the **books** table, using your **author_id**
-   now retrieve all of the information for your book (title, ISBN, published, lastname, firstname)

# What to submit

Create a text file containing, for each query listed above:

* The exact query you came up with
* The exact output of the query

You can cut and paste these from the console window as shown in the example above.

Save your queries and outputs in a plain text file and upload the text file to Marmoset as **lab04**.
