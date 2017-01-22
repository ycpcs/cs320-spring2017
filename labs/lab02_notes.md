---
layout: default
title: "Notes for Lab 2: Guessing Game Webapp"
---

Setting the JRE System Library
===============

These instructions are for Eclipse Mars (which is installed on the PCs in KEC 119 and KEC 123).  The isntructions will be similar for Luna and Neon - but might have some slight differences.

There is a conflict with the default JRE Library version (jre1.8.0\_111) that was installed with Eclipse on the lab PCs, and CS320\_Lab02.  You will probably need to change the default JRE Library version to an earlier version in order to get CS320\_Lab02 to work.

In KEC 119, there are two versions of the JRE Library, 1.8.0\_51 and 1.8.0\_111.  You will need to select 1.8.0\_51 in KEC 119 for CS320\_Lab02 to work properly.

First, create a folder on your home (H:) drive named "cs320-spring2017".
Set the default workspace for Eclipse to that location.
Download CS320\_Jetty.zip and CS320\_Lab02.zip.
Open Eclipse, switch the Workspace to H:/cs320-spring2017.
Import CS320\_Jetty.zip.
Import CS320\_Lab02.zip.
Expand the CS320_Lab02 project.
If it shows the JRE System Library as "jdk1.8.0\_51" or "jdk1.8.0\_60", then you have no further steps to take.

On the other hand, if the JRE System Library is "jre1.8.0\_111", you will need to switch to a compatible library.

Go to C:/Program Files/Java and look for a jdk folder that is for jdk1.8.0\_xx, where 'xx' is < 90.  Hopefully, you have one of those installed in the Java folder.  For the lab PCs, there are up to three: jdk1.8.0\_51, jdk1.8.0\_60, and jre1.8.0\_111.

Go into Eclipse, right-click on the CS320\_Lab02 project.
Got to the the bottom, select Properties.
Select Java Build Path on the left.
Select the Libraries tab.
Select the JRE System Library entry.
Select the Edit... button on the right
Select the Installed JREs... button on the right
That will pop up a list of installed JRE's.
If you see one for jdk1.8.0\_51 or jdk1.8.0\_60 (or any < 90), select that one, and hit Apply, followed by OK.
You should see that the Workspace defalt JRE has changed to the one you just selected.
Hit Finish, and then OK, and you are ready to roll.  The JRE System Library for CS320\_Lab02 should also have been updated.

If you do not see an acceptable jdk version, then  select search, and browse to the C:/Program File/Java folder under Computer, and hit OK.

Now, all of the jdks and jres that are included in that folder will show up, and you can select an appropriate one. (Apply, OK, Finish, OK).
You should now be able to run the lab.

If you do not find an acceptable jdk installed on your computer, you'll have to install one from this location:
http://www.oracle.com/technetwork/java/javase/downloads/java-archive-javase8-2177648.html

Create a free Oracle account and then download and install the appropriate version for your Eclipse/java installation - the 64-bit version will show up in C:/Program Files/Java, and then you can select it as described above.

You will want to select Java SE Development Kit 8u51 or 8u60.

Then select the appropriate file to download - you want the SDK.  For Windows 64-bit, that will be jdk-8u51-windows-x64.exe or jdk-8u60-windows-x64.exe.

Download the file - it is 180MB, it could take a while to download.

Then run the executable - it will bring up the installer.  By default, it will install to the C:/Program Files/Java folder.  It will install both the JDK and the JRE at that location.

After it is installed, you can then follow the above instructions to set the JRE System Library to the jdk you just installed.

There are some other issues that I've seen popping up with CS320\_Lab02.
1) For some unknown reason, the CS320\_Lab02.zip file might be protected, and Eclipse won't let you import it.  Let me know if this continues to happen - I think this is fixed with the latest ZIP file.
2) When you start Eclipse on the lab PCs, Windows will likely warn you about running a program that was downloaded from the Internet.  You can ignore this and move on.
3) When you go to run main() in the CS320\_Lab02 project, you may get a Windows Firewall warning.  You can hit Cancel and the lab will work.

You should see two new projects in your workspace, **CS320\_Jetty** and **CS320\_Lab02**.

See **AddNumbers.java**, **\_view/addNumbers.jsp**, and **AddNumbersServlet.java** to understand how the model, view, and servlet classes work for the AddNumbers example.

To run the AddNumbers webapp, run **Main.java** as a Java application and enter the following URL in your web browser:

> [http://localhost:8081/lab02/addNumbers](http://localhost:8081/lab02/addNumbers)


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


