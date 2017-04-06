---
layout: default
title: "Resources"
---

This page links to useful resources.

[Fetching and merging changes from within Eclipse](fetchMerge.html)

Violet UML: [violetumleditor-2.1.0.jar](violetumleditor-2.1.0.jar)

[UML: A Great Explanation of UML Relationships](http://usna86-techbits.blogspot.de/2012/11/uml-class-diagram-relationships.html)

[CS320\_Derby.zip](CS320_Derby.zip) &mdash; Eclipse project with jarfiles for Apache Derby (relational database)

[W3Schools: Great Tutorial site for HTML, CSS, Java Script, SQL, PHP](http://www.w3schools.com) - Go here first for HTML/CSS tutorials.

[Bootstrap: A visual editor for creating web front-ends](http://www.w3schools.com/bootstrap/default.asp)

[Brackets: A visual editor for working on HTML/CSS](http://brackets.io/)

[Great Tutorial Site for Creating HTML Forms](http://www.htmliseasy.com/form_tutor/lesson01.html)

[Great Tutorial site for JSP](http://www.tutorialspoint.com/jsp/index.htm) - note that this references Apache Tomcat, but much of it should apply to Eclipse Jetty.

[Working with JSTL](http://www.tutorialspoint.com/jsp/jsp_standard_tag_library.htm) - linked from above site.

[Creating and Using Session Information](http://www.tutorialspoint.com/jsp/jsp_session_tracking.htm) - linked from above site.

[An Java email validator class using regex (regular expressions)](https://www.mkyong.com/regular-expressions/how-to-validate-email-address-with-regular-expression/
)

[CS320\_Library\_Example\_2017.zip](CS320_Library_Example_2017.zip) &mdash; Eclipse project that ties the [Web Applications Lab](../labs/lab02.html) together with the [ORM Lab](../labs/lab06.html).  This application places a web front-end on the SQL transactions from Lab06, as well as provides examples for creating a Derby database from CSV files, how to use session information after login, and how to use JSTL to display a list of complex objects in a JSP.  It has been updated to incorporate a many-to-many relationship between **Books** and **Authors**, using a junction table (**booksAuthors**) that cross-references **book_id**'s with **author_id**'s.  It also contains some example JUnit Tests for testing the Derby database queries.

> <div class="callout"><b>NOTE: You are free to incorporate any of this code into your project(s) - as long as you cite the source.</b></div>

After you download the ZIP file, extract it into a new Java workspace separate from the others that you have used in the past.  This project is composed of 4 separate Java projects (**CS320_Jetty**, **CS320_Derby**, **CS320_Lab02**, and **CS320_Lab06**).

Before running the project, open up **DerbyDatabase.java** under **CS320_Lab06->src->edu.ycp.cs320.booksdb.persist** and edit the Derby database location in the **connect()** method so that it has the absolute path where your workspace is located.  Do the same thing in **SQLDemo.java** in the **main()** method.

Run **DerbyDatabase.java** as an application to create the Library database from the **authors.csv**, **books.csv**, and **bookAuthors.csv** files. It might take a few seconds for the application to create the DB - you will see it in the console.  Afterwards, **library.db** will show up as a folder under the **CS320_Lab06** folder.  If you have made the suggested changes to the location of your database, that is where your database files will be located.

Run **SQLDemo.java** as an application so that you can issue SQL queries to the Library DB.  If this step works - if you can issue queries and SQLDemo can locate the DB - then you have correctly updated the two files from above.

To run the web application, first stop **SQLDemo**, then run **CS320_Lab02->Main.java** as a Java application, followed by entering this URL in your web browser:

> [http://localhost:8081/lab02/login](http://localhost:8081/lab02/login)

There are currently two sets of login credentials hard-coded into the application: User name: **student** with PW: **ycp** and User name: **faculty** with PW: **E&CS**.  After you have successfully logged in, the user name will be passed around as part of the Session information, and each subsequent servlet checks for a valid Session (a non-null "user" attribute) before responding to the request.  Note that this is not a secure method for handling credentials, but is used as an example for passing around and checking Session information.

> <div class="callout"><b>When you implement the persistence layer using Derby for your team project</b>: when specifying the JDBC URL in the code where you connect to the database, you should use an absolute file name for the database name. For example, <code>jdbc:derby:H:/mydatabase.db;create=true</code> (this will create the database as <code>H:/mydatabase.db</code>).  If you use a relative file name, your web application will probably not find the database (because it runs in the <code>war</code> directory rather than the root directory of the project).</div>
