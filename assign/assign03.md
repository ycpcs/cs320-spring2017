---
layout: default
title: "Assignment 3: Team Project Milestones"
---

In the [Schedule](../schedule.html) you will notice days designated as team project milestones.  These are opportunities for your group to demonstrate progress on your team project.

This document describes the expectations for each milestone.

> Date | Milestone
> ---- | ---------
> Monday, March 20    | Milestone 1: Minimal Working System
> Monday, April 3     | Milestone 2: Progress on Features
> Friday, April 21    | Milestone 3: "75%" Working System (persistence using SQL database)
> Monday, May 1       | Milestone 4: "95%" Working System (presentation & demo "dry run")

## Expectations

**Milestone 1: Minimal Working System**. Your team should demonstrate

* Model classes, controllers, and unit tests associated with a small number of "essential" requirements
* A persistence interface and a "fake" in-memory implementation of the persistence interface (e.g., using array lists to store model objects rather than database tables)
* A minimal web-based user interface (e.g., JSPs and servlets) that implements a small number of essential features in some minimal form

The idea of a minimal working system is to create a working foundation early in the project's development.  Subsequent iterations of the development process will build upon this foundation to implement additional features.

**NOTE: In order to hit the first milestone, and place your team in a good position to achieve success, you should consider putting in a good deal of initial development work on your web front-end over Winter Break.**

**Milestone 2: Progress on features**.  In this milestone, your team should demonstrate some progress on features, such that at least some use cases are fully or partially implemented.  It is fine if your system is using the "fake" database at this point.

**Milestone 3: "75%" Working System, Persistence using SQL database**. Your team should demonstrate a working system that implements most of the major system requirements.  Also, Your team should demonstrate that there is a working implementation of the persistence interface that uses an SQL database to store and retrieve data (e.g., using Derby).  Note that it is not expected that the system has a high degree of "polish": the UI doesn't have to be beautiful, for example.  However, the features that are implemented should be functional and free of bugs.

**Milestone 4: "95%" Working System**. Your team should demonstrate a working system that is nearly complete.  Nearly all of the required features should be implemented.  The system should have a reasonable degree of "polish".  Your team should be prepared to discuss what remains in order to reach a point where the system is complete.  Your presentation should be a condensed "dry run" of your final presentation, with a degree of structure and polish that is closer to the formal presentation that your team will give for its final demonstration.  The presentation for MS4 should include the following:

* A slide on your SQL database schema, which should include your tables, the attributes in each table, and any relationships between the tables.  You can use the format shown in [Lecture 9](../lectures/lecture09.html).
* A slide that lists the names of your SQL database queries.  Note that this should not include the SQL code, but rather method names, such as "getAllBooksByAuthor", along with a short description of each query.
* A slide summarizing the current progress on your project, i.e., a list of features that have been implemented.
* A slide summarizing the major technical challenges that your team faced, and how you overcame them.
* A slide summarizing what you plan to accomplish before your final presentation and demo.

## Evaluation

For each of these milestones, I will give your team one of the following grades: *below expectations*, *meets expectations*, or *exceeds expectations*. Below expectations means that I am concerned that your team is not making sufficient progress.  At all 4 milestones, I expect that there will be sufficient effort put towards automated unit test case development.

<div class="callout">
<b>DO NOT LEAVE TEST CASES AS AN AFTER-THOUGHT.  YOUR TEAM WILL RECEIVE "BELOW EXPECTATIONS" IF YOU DO NOT HAVE SUFFICIENT TEST CASES DEVELOPED FOR EACH MILESTONE.</b>
</div>

<!-- vim:set wrap: ­-->
<!-- vim:set linebreak: -->
<!-- vim:set nolist: -->
