---
layout: default
title: "Resources"
---

This page links to useful resources.

[Fetching and merging changes from within Eclipse](fetchMerge.html)

Violet UML: [violetumleditor-2.1.0.jar](violetumleditor-2.1.0.jar)

[Great Tutorial site for HTML, CSS, Java Script, SQL, PHP](http://www.w3schools.com)

[Great Tutorial Site for Creating HTML Forms](http://www.htmliseasy.com/form_tutor/lesson01.html)

[Great Tutorial site for JSP](http://www.tutorialspoint.com/jsp/index.htm)

[Creating and Using Session Information](http://www.tutorialspoint.com/jsp/jsp_session_tracking.htm)

[Working with JSTL](http://www.tutorialspoint.com/jsp/jsp_standard_tag_library.htm)

[CS320\_Derby.zip](CS320_Derby.zip) &mdash; Eclipse project with jarfiles for Apache Derby (relational database)

<!-- Commented out Library Example unitl after ORM Lab is complete
[CS320\_Library\_Example\_With\_M2M.zip](CS320_Library_Example_With_M2M.zip) &mdash; Eclipse project that ties the [Web Applications Lab](../labs/lab03.html) together with the [ORM Lab](../labs/lab06.html).  This application places a web front-end on the SQL transactions from Lab06, as well as provides examples for creating a Derby database from CSV files, how to use session information after login, and how to use JSTL to display a list of complex objects in a JSP.  It has been updated to incorporate a many-to-many relationship between Books and Authors.  It also contains some example JUnit Tests for testing the Derby database queries.

> <div class="callout"><b>NOTE: You are free to incorporate any of this code into your project(s) - as long as you cite the source.</b></div>

After you download the ZIP file, extract it into a new Java workspace separate from others that you have used in the past.  This project is composed of 4 separate Java projects (**CS320_Jetty**, **CS320_Derby**, **CS320_Lab03**, and **CS320_Lab06**).

Before running the project, open up **DerbyDatabase.java** under **CS320_Lab06->src->edu.ycp.cs320.booksdb.persist** and edit the Derby database location in the **connect()** method so that it has the absolute path where your workspace is located.  Do the same thing in **SQLDemo.java** in the **main()** method.

Run **DerbyDatabase.java** as an application to create the Library database from the **authors.csv** and **books.csv** files. It might take a few seconds for the application to create the DB - you will see it in the console.  Afterwards, **library.db** will show up as a folder under the **CS320_Lab06** folder.  That is where your database files are located.

Run **SQLDemo.java** as an application so that you can issue SQL queries to the Library DB.  If this step works - if you can issue queries and SQLDemo can locate the DB - then you have correctly updated the two files from above.

To run the web application, first stop **SQLDemo**, then run **CS320_Lab03->Main.java** as a Java application, followed by entering this URL in your web browser:

> [http://localhost:8081/lab03/login](http://localhost:8081/lab03/login)

There are currently two sets of login credentials hard-coded into the application: User name: **student** with PW: **ycp** and User name: **faculty** with PW: **E&CS**.  After you have successfully logged in, the user name will be passed around as part of the Session information, and each subsequent servlet checks for a valid Session (a non-null "user" attribute) before responding to the request.

--->

> <div class="callout"><b>When you implement your persistence layer using Derby</b>: when specifying the JDBC URL in the code where you connect to the database, you should use an absolute file name for the database name. For example, <code>jdbc:derby:H:/mydatabase.db;create=true</code> (this will create the database as <code>H:/mydatabase.db</code>).  If you use a relative file name, your web application will probably not find the database (because it runs in the <code>war</code> directory rather than the root directory of the project).</div>
