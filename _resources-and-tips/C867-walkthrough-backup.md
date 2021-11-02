This post is a backup of a walkthrough I wrote out for reddit on the project for C867.

<hr />

Hello everyone,

I notice a lot in this subreddit that there are questions about the project for C867. Long ago it wasn't nearly as difficult because of the CI-made playlist that existed on Youtube. Unfortunately that playlist was removed, the backup was also removed, and while the instructors put a lot of effort into putting up new resources to help, there's still a lot of confusion about this class.

Like my post for D191, I wanted to see if perhaps I could create a "walkthrough" of the project that wouldn't get struck down from the school, but would alleviate some of the issues students often run into.

I'm going to preface everything first however by saying this; if you've run into a wall that nothing in this post seems to help with, put your project folder into a zipped file, upload it to the Google Drive attached to your student email, and send it to your assigned CI with questions. You don't even need to fight for an appointment in their schedules, just email them. It's the fastest way to get an answer and it'll likely save you a lot of time. I know when I took this class, which was NOT that long ago, trying to find a free appointment with a CI was difficult.

Now, onto the meat...

The project for this class requires you to take the string presented to you and create a command-line C++ application that parses this string into an array, then carries out some specified functions below. Those of you with a lot of C++ familiarity will likely find this to be a breeze, but if you're coming into this without C/C++ knowledge or being simply new to programming, you'll likely feel a bit shell-shocked.

<br />

**Understanding C++**

<br />

If you're new to C++ or programming in general, you'll want to start by getting an understanding of how C++ works and the fundamentals of working with C++. You'll also want to understand how the Data Structure, Arrays, work in C++ (although I have heard people use Vectors instead in the past, but the evaluators may fail you for it now). When you start the course, you'll gain access to a Zybook that's...alright, but definitely not the best. Personally, I think there are far better resources out there for learning C++, and I've listed a few below.

- [The Cherno's C++ Playlist](https://www.youtube.com/playlist?list=PLlrATfBNZ98dudnM48yfGUldqGD0S4FFb) - The Cherno is a former game engine dev, and the C++ tutorial series he made has a bit of a game dev angle. He does things a little differently than other C++ tutorials in that he explains the nitty-gritty early and tends to gloss over simpler things (with the intention that you'll research them yourself), so completely new programmers may be a bit confused at times, but if you really want to understand the WHYs and HOWs, watch his series. If you need help installing Visual Studio, his tutorial covers it on all three systems.
- [Bucky's C++ Programming Tutorial](https://www.youtube.com/watch?v=tvC1WCdV1XU&list=PLAE85DE8440AA6B83) - Bucky's C++ tutorial is very beginner-friendly. If you're new to programming in general, I suggest starting here. Or if you don't understand something from The Cherno's playlist, try looking at the Bucky tutorial on the same topic.
- [Programming -- Principles and Practice Using C++ by Bjarne Stroustrup](https://www.stroustrup.com/programming.html) - If you're more into reading than watching videos, there's the creator of C++'s book on programming. It's not just a tutorial of C++, but a beginner's programming book and it's REALLY good. If you're looking to get your hands on it, maybe try a *lib*rary or some other *gen*eral bookst*or*e, but *pdf* copies exist. If you have the *drive* to read it, I recommend reading Chapters 9 (pg 336), 17 (pg 616), and 18 (pg 660) which cover the more challenging aspects of this project.
- [Cplusplus.com's Reference](https://www.cplusplus.com/reference/) - I kept this on-hand the entire time during this project. Although it isn't the most up-to-date resource in some areas, it's relevant enough for our purposes here.

Just keep in mind that you don't need to be a C++ master to pass this class, so to keep from getting lost in the weeds, I recommend focusing on concepts related to the project (at least until you've finished it) and learning new ones based on where you're struggling with it. Below are some of the most important concepts you'll want to learn, the ones that you'll need to complete your project.

- Outputing data to the screen (cout)
- Creating Classes and Objects
- Using for loops and if statements
- Accessing an Object's method
- Deleting Objects
- Creating functions, calling them, and returning data using them
- Creating Class Methods like Construtors, Destructors, Accessors/Getters, Mutators/Setters, and Print.
- Overloading a Class Constructor
- Creating Arrays in C++, specifically arrays of pointers
- Adding data to an Array and deleting data from it
- Parsing a string with delimiters
- Creating and using Enums
- Using C++ libraries (#include <libraryname>)
- Using the "this" keyword
- Using the "->" operator

<br />

**What You're Being Asked For**

The project requires you to deliver 6 C++ files, three .h or Header files and three .cpp or Source Code files. These are;

- Main.cpp
- Roster.cpp
- Roster.h
- Student.cpp
- Student.h
- Degree.h

Now the names may differ, but the contents and requirements for each file are generally the same. In this next leg of the post, I'm going to summarize what each file should include and what topics these might be covered under if not already stated. 

<br />

**Main.cpp**

This file you can think of as the base of operations for your project. It will include your main() function and all of the function calls you'll require for this project will be included in this source file. You'll also want to make sure to add the correct includes (such as the .h files you made) at the top.

These are the tasks the Main.cpp file should be performing;

- You should have your string of data to be parsed included here (make sure your information is included in A5).
- You should have code that outputs your personal information (Course Title, Language Used, Student ID, and Name)
- You should call your roster class's constructor to create a new roster object called "classRoster".
- You should a method that seperates the elements from the string array from the top and sends them a parse function. (I believe you can either include the parse function here OR you can call a parse function in one of your classes.)
- You should call a function that outputs the contents of your new Roster object (so you know all the Students were added correctly).
- You should call a function that outputs all Students that have invalid emails.
- You should loop through your classRoster and call a function that outputs the integer array for "average days in course" for each student ID.
- You should call a function that outputs students that match a certain degree program state.
- You should call a function that deletes a certain Student by its ID.
- You should call a function that outputs all Students again.
- You should call a function that deletes a certain Students by its ID again and comes up with an error.
- You should then delete your classRoster to free its memory.

For this file you're mostly going to want to focus on understandin how to call function methods, parse a string (or call a function in the class that does), use if and loop statements, output data to the screen, and release memory.

<br />

**Degree.h**

This is the only header file you'll be including into your program that will not require a matching .cpp. The reason for this is because the Degree.h file is used only to create your Enum class a certain variable.

I'm going to quickly explain something about enums that might help; think of an enum class as a traffic light. A traffic light might have 3 states, here's how that might look in C++;

enum class TrafficLight {
	RED,
	YELLOW,
	GREEN,
};

Don't be fooled by the text however, if you called an enum, you'd actually get back a number. That's because the states, which are what the RED, YELLOW, and GREEN, stand for in the enum class, actually refer to integers.

So for example, RED = 0, YELLOW = 1, GREEN = 2. Think about this as you set enums in your code for the other files. You can set strings to match your enum states by creating a static const string array that contained each state, but I believe that's above and beyond what's asked for this project.

<br />

**Roster.cpp and Roster.h**

I've bundled these two files together because you're going to be handling very similar code in these two. The first file you'll work on, the Roster.h file, is where you're going to define everything related to your Roster class. (Make sure you add the correct ".h" files to you includes so their code will work in this class.) That means you'll need to...

- Create a class constructor
- Create a class destructor
- IF YOU CHOOSE NOT TO PARSE IN MAIN.CPP, Create a function that parses a string with delimiters
- Create a function that adds a student object to a roster object
- Create a function that removes a student by their ID
- Create a function that outputs all the objects in this object
- Create a function that outputs the integer array of average days by student ID
- Create a function that outputs invalid email addresses
- Create a function that outputs all students with a certain degree program.
- And create an array that holds objects from an abstract class...

For the Roster.h file you only need to type out what functions/methods and variables this class will contain. In the Roster.cpp class, you'll take the above functions and actually define them (as in, you'll write the code that makes them work. Make sure you to add "roster.h" as an include for your Roster.cpp file.

<br />

**Student.cpp and Student.h**

Last, but surely not least, is the Student class. You may be a bit confused about this class at first because it's what you might call an "abstract class" meaning it's a class that's only called by another class to create objects. Like the Roster.cpp and Roster.h files, you'll be writing out what you need in your header files first, which is;

- A set of private variables for each of the information you want to parse from your string (including an array for three specific integers)
- Create a class constructor
- Create an overloaded class constructor
- Create a destructor
- Create "Accessor/Getter" functions for all your variables
- Create "Mutator/Setter" functions for all of your varaibles
- Create a function that prints all of those variables when called

As you define the functions in your Student.cpp file, you may want to keep your all of your getter and all of your setter functions grouped together so you can find them easily in case of errors. This is the part of the project where understanding how "this" and the "->" operator work will REALLY come in handy. Aside from that, the functions in this .cpp file are far less complicated than Roster.cpp's.

<br />

**Debugging and Help**

I thought I'd add this last part because this project can be a bit overwhelming for new programmers. It's so easy to forget one ";" after a function or forget the "*" in a variable call. Depending upon the IDE that you use, and likely that will be Visual Studio, you'll want to keep an eye on the errors list as you're working. It might not point directly to some of the more complicated errors, but 9/10 it will give you a head start on where to look. Even better, in the case where you run into an error you just can't understand, you can look up the error code or copy the message into an email to your CI for assistance.

If I can give one last piece of advice, it would be to work through this iteratively. If you implement a function and you aren't sure if it's working correcty, test it. Use "//" to comment out functions in your Main.cpp and write a piece of code to directly call that function and output it to make sure it works correctly. It's far better than trying to finish it all in one piece and get frustrated when it won't compile or the formatting is off because of an error in parsing.

Also, of course, there's plenty of places online you can look for general programming help like this sub, the other programming subs, and [stackoverflow](https://stackoverflow.com/). But HOPEFULLY, this will give everyone a nice headstart.
