The following is my write-up of how best to prepare for C191 Operating Systems for Programmers. 

<sub>**NOTE** : If you're using Visual Studio as your IDE for C you'll likely run into an error at compile time when trying to use the function `scanf()`. To fix this, you'll need to add `_CRT_SECURE_NO_WARNINGS` to the preprocessor definitions (In Project > Properties > C/C++), [this video](https://www.youtube.com/watch?v=lHfLLy1Ya5U) will show you how. </sub>

--------

Hey everyone,

I notice a lot in this sub that students have difficulties with C191 Operating Systems for Programmers. And more so, I find most students seem to find it really boring and dry, which is a shame. I think part of the reason for this is because the program doesn't particularly prepare you for the topic or the text, Operating Systems Concepts (aka the Dinosaur Book). So to help combat this, I wanted to share some advice and a mini-study plan to help new and current students who haven't taken C191 prepare to enjoy this course. 

But before my plan, I'd like to recommend some courses to take before C191 and what to focus on from them to make the transition smoother;

- **C949 Data Structures and Algorithms I:** You'll want to make sure you get a firm understanding of basic types of data structures like stacks, heaps, arrays, linked lists, etc., the concept of algorithms and how to use BigO Notation. Also, although the OA is language agnostic, the course textbook is in Python, which I recommend using to learn the language for C950 anyway.

- **C836 Fundamentals of Information Security:** Try to get a good understanding of concepts such as policies and mechanisms as well as threats such as Buffer Overflow. A good portion of C191's OA deals with Security and Protection, so this will give you a nice head start.

- **C867 Scripting and Programming Applications:** For the PA of this project you'll be using C++. More importantly, try to get a good grasp on why the array of pointers you'll be using works as it does. Memory is a large part of C191, and this will give you your first taste of it.

**NOTE:** Most people recommend taking C952 Computer Architecture (and the current Standard Path has it first) before C191. Personally I took C191 and C952 together, completing C191 first. I recommend when you schedule them to take them as close to, if not together, as possible because C952's OA has a significant overlap with C191 (lots of OS questions).

---------------------------

Here's the breakdown of what we'll need for our study plan;

These two are the main books we'll be using for this study guide. 
- [Think OS by Allen Downey](https://greenteapress.com/wp/think-os/)
- [The Little Book of Semaphores by Allen Downey](https://greenteapress.com/wp/semaphores/)

And at least one of these:
- [Head First C by David and Dawn Griffiths](https://www.amazon.com/dp/1449399916) *Recommended in Think OS*
- [The C Programming Language, 2nd Ed by Brian W. Kernighan and Dennis M. Ritchie](https://www.amazon.com/Programming-Language-2nd-Brian-Kernighan/dp/0131103628/ref=pd_sbs_1/130-8059446-9822104?pd_rd_w=X1mdd&pf_rd_p=690958f6-2825-419e-9c16-73ffd4055b65&pf_rd_r=N023QQ24D478E02RSVQ0&pd_rd_r=e3f3bab8-fc86-4c75-965a-77f9db4c8712&pd_rd_wg=NEJRn&pd_rd_i=0131103628&psc=1) (also consider [The C Answer Book](https://www.amazon.com/exec/obidos/ASIN/0131096532/knking) for exercises)
- [Learn-C.org](https://www.learn-c.org/) (you'll want to complete all tutorials, especially those on pointers and dynamic allocation) 
- [Exercism's C language path.](https://exercism.org/tracks/c/exercises) *I recommend using this with one of the books above*

I know what you're thinking already-"Wait, are you telling me I need to learn C?!"

Yes! That is exactly what I'm suggesting. But there's good reason for it. By learning C you'll gain valuable experience working with memory and be able to follow along with Operating Systems Concepts since it very often uses C code to explain OS implementations. More importantly, it's something you can proudly put on your resume in the future! But I think the beginning of Allen Downey's book Think OS puts it best;

"In many computer science programs, Operating Systems is an advanced topic. By the time students take it, they usually know how to program in C, and they have probably taken a class in Computer Architecture. Usually the goal of the class is to expose students to the design and implementation of operating systems, with the implied assumption that some of them will do research in this area, or write part of an OS." (Downey, 2015) 

Downey specifically wrote his book, Think OS, for students who've learned Python as a way to both teach them both C and the basics of Operating Systems. In the book he specifically recommends using "Head First C" and his companion book "The Little Book of Semaphores." The preface recommends HFC chapters 1-3, 6, and 12, and TLBoS chapters 1-4.

Both of Professor Downey's texts are free to read online and have companion Github repos to use for any exercises. They're also short, less than Operating Systems Concepts combined (Think OS is 99pgs), so it should take you no time at all to work your way through them. While you're working through Think OS, read along with your C language book of choice (although Head First C may be the most approachable for beginners) and try out the exercises on [Exercism's C language path.](https://exercism.org/tracks/c/exercises)

By the time you do take C191 Operating Systems for Programmers, you will already have learned the core concepts and be ready to take on the Dinosaur book.

I hope you find this helpful!
