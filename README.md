Exercise 1 : Hello World
========================

This exercise does not require that you use the machines at the real-time lab. However, for the last part of the exercise (and for exercise 2) you will need some way to run code written in C and Go.

 - C:
   - Windows: Use [TDM-GCC](https://jmeubank.github.io/tdm-gcc/download/), then use `gcc` from the command line or powershell.
   - OSX: You will need to download the [Apple Developer Tools](https://developer.apple.com/xcode/), then either use xcode, or `gcc` or `cc` from the command line.
 - Go:
   - [Download from golang.org](https://golang.org/)

Go has an [interactive tour](http://tour.golang.org/list) you can take. Go's syntax is a bit different, so it may be worth skimming through, or at least using as a quick reference.

1: Thinking about elevators
---------------------------

Not for handing in, just for thinking about. Talk to other groups, assistants, or even people who have taken the course in previous years.

Brainstorm some techniques you could use to prevent a user from being hopelessly stranded, waiting for an elevator that will never arrive. Think about the [worst-case](http://xkcd.com/748/) behavior of the system.
 - What if the software controlling one of the elevators suddenly crashes?
 - What if it doesn't crash, but hangs?
 - What if a message between machines is lost?
 - What if the network cable is suddenly disconnected? Then re-connected?
 - What if a user of the system is being a troll?
 - What if the elevator car never arrives at its destination?

2: Version control
------------------

If you can read this text you have already taken your first steps in starting to use a version control system.

A version control system is a tool helps a group of people work on the same files in a systematic and safe manner, allowing multiple users to make changes to the same file and merge the changes later. It is also possible to create diverging branches so that multiple independent areas of development can happen in parallel, then have these merged together safely at a later time. Version control systems also keep track of all previous versions of files, so that you can revert any or all changes made since a given date.

In this course we will be using Github Classroom, where you will find the assignment texts, project description, and all the code related to the project. You will be given private repositories on the TTK4145 organization, which means that teachers and student assistants will have access to your code by default. You can create issues that reference specific assignment tasks or part of your project code, while tagging the student assistants to get their attention.

You will not be able to complete this exercise without a very basic practical understanding of git. Unless you're already familiar with git, it's highly recommended to have a look at the following resources before moving on to Part 3 and 4. Don't let the feeling that you have to google everything discourage you, this is perfectly fine, even expected. And don't forget that the student assistants are there to help you.

- Do the [interactive tutorial](https://try.github.io/)
- [Feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)

Some prefer the command line while some prefer something graphical, both are fine. An overview of graphical git clients can be found [here](https://git-scm.com/downloads/guis/).

3: Reasons for concurrency and parallelism
------------------------------------------

To complete this exercise you will have to use git. Edit in your answers to [the theory questions in this file](/theory.md), then create one (or several) commits, and push it to GitHub to complete the task. 

When answering the questions, remember to use all the resources at your disposal (including the internet)

4: Finally some code
--------------------

Implement this in C and Go:


    global shared int i = 0

    main:
        spawn thread_1
        spawn thread_2
        join all threads (or wait for them to finish)
        print i

    thread_1:
        do 1_000_000 times:
            i++
    thread_2:
        do 1_000_000 times:
            i--
            
            
In this exercise you should take advantage of the starter code found in the subdirectories corresponding to the different programming languages. Fill out the missing code and make sure your program is working before committing and pushing the changes to your repository.

Finally, create a new file called `result.md` inside this directory explaining what happens, and why. Remember to add, commit, and push the new file.



