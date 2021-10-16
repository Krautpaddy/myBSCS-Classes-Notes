# D191 Walkthough Backup

This post is a backup of the walkthrough I posted on reddit after D191 was turned into a PA course.

----

For this project you have to do the following;

- Create a video of yourself going through a series of required queries in the virtual lab linked.
- Write a paper answering all of the questions brought up in Section A of the  paper. (For safe measures I would copy your entire series of queries from the presentation and paste them at the end of your paper).

Now to begin, skip directly to the PA page. Nothing in the course lessons is even remotely helpful.

Read the PA description over, we're going to walk through it one at a time using links to the Postgre tutorial. For now, you'll want to go to the [Sample Database](https://www.postgresqltutorial.com/postgresql-sample-database/) link and grab the ERD for the dvdrentals database. This is the database that is used in the virtual lab 1:1. It's a very handy reference. 

Next, open a blank txt file in Notepad (or whatever text editor you have). We're going to draft our queries here. 

<br />

## **UNDERSTANDING THE REQUIREMENTS:**

Before we create our "business question", we're going to want to figure out what we actually need for queries. Because it's left VERY open-ended in the PA description but apparently not to the evaluators, you must use the following, unless specified:


- [CREATE TABLE](https://www.postgresqltutorial.com/postgresql-create-table/)
- [CREATE FUNCTION](https://www.postgresqltutorial.com/postgresql-triggers/)
- [CREATE TRIGGER](https://www.postgresqltutorial.com/postgresql-triggers/)
- [CREATE PROCEDURE](https://www.postgresqltutorial.com/postgresql-create-procedure/)


You must also use have the following types of queries, but they don't seem to be as set in stone;


- [JOIN (since you must use data from at least 2 tables)](https://www.postgresqltutorial.com/postgresql-joins/)
- [Verify data in a table](https://www.postgresqltutorial.com/postgresql-select-into/)
- [Extract data](https://www.postgresqltutorial.com/postgresql-insert/)
- [An Aggregate function (like Count(**field**)) ](https://www.postgresqltutorial.com/postgresql-aggregate-functions/)
- A transformation function (like [CASE](https://www.postgresqltutorial.com/postgresql-case/))
- Clear data from a table (like [TRUNCATE](https://www.postgresqltutorial.com/postgresql-truncate-table/))


I've included links to Postgre's official(?) tutorial links for all of these functions. If you can figure out how to apply the examples to your business problem, you will pass. 

<br />

## **CREATING A BUSINESS PROBLEM:** 

This will likely be the hardest part of your project. You're tasked with creating a "business problem" that the database can solve. Luckily you should've downloaded the database ERD, so you have an idea of what options you have. Also keep in mind that you must use 2 tables (1 field at least per table), an aggregate function, and a transformation function. So I recommend using these three requirements to build your problem.

My best advice is to find a problem where using your aggregate function will solve your problem. Remember that the transformation function needs to be performed in your detailed table, so that field may not need to be in the summary table.

If you're struggling to understand what a Business Problem is, [Chapter 9 of the SQL for Data Analytics book](https://lrps.wgu.edu/provision/262398022) (also linked on the course page in Readings) actually has an example of going through solving one with Postgre (however, you won't be using the shell for the PA). **Think of something that, using the information in the database, you could run the numbers on to help the business.**

<br />

## **PUTTING YOUR QUERIES TOGETHER:**

REMEMBER: Write your drafted queries out on a text file and save them on your PC!

Now that you should have your business question (and an idea of what your answer will be determined by), we're going to start putting our queries together.

To start, we need to know what fields we'll need, from which tables. That will help us determine not only what our extract and JOIN should look like, but what the CREATE TABLEs for detailed and summary need in terms of fields and datatypes.

Once we determine the tables and fields (you may need to use an extra table for your joins but not for your extracted fields), we can create our extraction, JOINS, and CREATE TABLE queries. Now you can also determine your Aggregate and Transformation functions based on the fields you picked to include into your tables.

The verifying table, CREATE FUNCTION, CREATE TRIGGER, CREATE PROCEDURE, and clear table functions will be determined by what you refer to your detailed and summary tables as. The details aren't determined by what tables you pull from.

Now that you've got your queries drafted, make sure you have them in the correct order on your paper. Then, double check to make sure that there are no errors in the syntax, names of tables queried, etc. When you've given it a once-over, open up the Lab linked at the bottom of Assessments.

Once the lab opens, click on Pgadmin, find the dvdrentals database and right click and select "Query Tool". To prepare for the next part, you're going to practice running through your code to make sure it works. NOTE: It seems the demonstration does not require you to call your Function, Trigger, or Stored Procedure, so just make sure they can be created successfully and leave it at that. When you've made any adjustments necessary, move onto the next part. 

<br />

## **RUNNING YOUR DEMONSTRATION:**

Once you've ensured your code works, cancel out of the virtual lab and reload a new one. Get whatever you need to create your Panapoto recording ready and start recording. 

PLEASE NOTE, THERE IS NO "FOLDER XXX" TO SAVE YOUR PA VIDEO IN, SO SAVE IT IN ANYTHING THAT YOU CAN SHARE FROM.

For your recording, make sure the query window in the lab is visible and start running through your queries one by one (erase each after running). If you don't have a mic, use "-- (text)" to write line comments as you code. Take your time, there is no time limit since the 2hr timer will automatically give you more time in the lab. When you're finished, exit the lab and we'll move onto the last part.

<br />

## **WRITING YOUR PAPER:**

For this final section, you're going to need to answer everything from Section A, plus F1 for good measure, in a word doc. There doesn't seem to be any minimum word count or length. I just used a numbered list and wrote whatever I needed to answer each question. 

When you finish, I suggest saving all of your saved queries on the bottom of your doc. 

<br />

## **WRAPPING IT UP:**

Now that your paper is written and hopefully proofread and your video demonstration is uploaded, submit your paper and a link to the Panopto video in the Submissions page and you should be "g-to-g". 


Btw, here's links to a few more pages that may be helpful to you:

- [PostgreSQL's documentation](https://www.postgresql.org/docs/)
- [W3School's SQL tutorial](https://www.w3schools.com/SQL/default.asp) 
- [Goalkicker's SQL book](https://goalkicker.com/SQLBook/)
