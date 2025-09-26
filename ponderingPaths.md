# The Root
### Problem Statement

Alright, so the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs, and, most importantly, flags. In this level, we've added a program right in /, called pwn, that will give you the flag. All you need to do for this level is to invoke this program!

You can invoke a program by providing its path on the command line. In this case, you'll be giving the exact path, starting from /, so the path would be /pwn. This style of path, one that starts with the root directory, is referred to as an "absolute path".

Start the challenge, launch a terminal, invoke the pwn program using its absolute path, and Capture that Flag! Good luck!
### Key points that I got out from the given statement
- The filesystem starts at **/** and then there are a lot of directories, programs, configuration files within it.
- In this challenge there is a program added, called *pwn* right in **/**.
- I was supposed to invoke this program through the _absolute path_ which is a path starting from the root directory i.e **/**.
## My solve 
**Flag:**'pwn.college{821l8GzeSK1R0M4ixBTljrqb4Tg.QX4cTO0wCOwIzNzEzW}'

I just had to simply use SSH and in the terminal, invoke the program by the absolute path '/pwn' and it gave me the flag, following is an image for it.

<img width="479" height="101" alt="Screenshot 2025-09-24 at 10 09 34 AM" src="https://github.com/user-attachments/assets/3a5c7ebb-4e3f-4d3f-be9b-d3903a61eefd" />

## What I Learned
- I learned what an absolute path is.
- I learned that **/** is the root directory.
### References
None.

# Program and absolute paths
### Problem Statement

Let's explore a slightly more complicated path! Except for in the previous level, challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

This challenge again requires you to execute it by invoking its absolute path. You'll want to execute the run file that is in the challenge directory that is, in turn, in the / directory. If you invoke the challenge correctly, it will give you the flag. Good luck!
### Key points
- There is a **challenge** directory right within the root directory.
- Name of the program is _run_ and it lives in the **challenge** directory.
- I was supposed to invoke this program by the absolute path which will be starting by the root directory.
## My Solve 
**Flag :** 'pwn.college{0DDCyGXuz9HU788aNOb2v4sBZ1U.QX1QTN0wCOwIzNzEzW}'

I just had to simply invoke the program 'run' through the absolute path, so first navigate to the 'challenge' directory and then run the program in it following is an image of it.

<img width="438" height="83" alt="Screenshot 2025-09-24 at 10 23 51 AM" src="https://github.com/user-attachments/assets/c5c7c4c0-41ad-418c-8843-a3c72e451f06" />

## What I learned
- How can programs lie in directories which themselves lie in the root directory.
- How can one still invoke the program by navigating to the directory that the program lies in like ***/challenge/run***.
### References 
No external references were used for this challenge.
# Position thy self 
## Problem Statement

The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:

hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!
### Key points
- One can navigate around all the files and directories in a filesystem by using the ***cd*** command.
- This affects the _current working directory_ of your process, in essence all your commands are now running in the directory that you've changed to.
- The ~ in the prompt means that **~** is the current path where the shell is located.
- I was supposed to change to a directory by the **cd** command and then invoke the program _run_ which lies in the **challenge** directory like in the previous challenge.
## My Solve
**Flag :** 'pwn.college{IM04K7yEjtf7yYXi6rHFpYXrQ3d.QX2QTN0wCOwIzNzEzW}'

I invoked the program when **~** was the current path and then the terminal told to me to change to the ***/usr/include*** directory, I changed to that by the cd command and then invoked the program and got the flag following is an image of it.

<img width="500" height="185" alt="Screenshot 2025-09-24 at 10 42 16 AM" src="https://github.com/user-attachments/assets/a47a2a0f-5af7-48b0-b9c2-e7ece1985171" />

## What I Learned 
- I learned about a very useful cd command.
- I learned what the ~ meant in the prompt, and what is my current path.
### References
Solved entirely with in - challenge hints and exploration.
# Position elsewhere
The context of this challenge is same as the previous one, only the directory to change to is different this time being ***/proc/132*** instead of /usr/include, the program to invoke is same.
## My solve
**Flag :** 'pwn.college{Unh5An7DQt_aUwx6irvwo8fSbeX.QX3QTN0wCOwIzNzEzW}'

Simply changed the directory and invoked the program which gave me the flag, following is an image of it.

<img width="537" height="183" alt="Screenshot 2025-09-24 at 10 53 39 AM" src="https://github.com/user-attachments/assets/51e3fa9c-2b9d-4d43-8758-47604616e8c1" />

### References 
None.

# Position Yet elsewhere
Context of this challenge is also same as the previous 2 and the details are exactly as the 3rd challenge.

**Flag :** 'pwn.college{0CoMMoO-7FUbxYFEu3ibh5LiU7I.QX4QTN0wCOwIzNzEzW}'

Image:

<img width="536" height="223" alt="Screenshot 2025-09-24 at 10 57 51 AM" src="https://github.com/user-attachments/assets/3658639a-0673-423b-b0bf-4ea070c48b3d" />

### References
None.

# Implicit relative paths, from /
### Problem statement

Now you're familiar with the concept of referring to absolute paths and changing directories. If you put in absolute paths everywhere, then it really doesn't matter what directory you are in, as you likely found out in the previous three challenges.

However, the current working directory does matter for relative paths.

A relative path is any path that does not start at root (i.e., it does not start with /).
A relative path is interpreted relative to your current working directory (cwd).
Your cwd is the directory that your prompt is currently located at.
This means how you specify a particular file, depends on where the terminal prompt is located.

Imagine we want to access some file located at /tmp/a/b/my_file.

If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
If my cwd is /tmp, then a relative path to the file is a/b/my_file.
If my cwd is /tmp/a/b/c, then a relative path to the file is ../my_file. The .. refers to the parent directory.
Let's try it here! You'll need to run /challenge/run using a relative path while having a current working directory of /. For this level, I'll give you a hint. Your relative path starts with the letter c 😊


### Key points
- The current working directory _cwd_ matters for relative paths.
- Relative path is any path which doesn't start at the root i.e **/**, it is interpreted relative to the _cwd_, which is where your prompt is currently located at.
- I was supposed to run ***/challenge/run*** with a relative path while my cwd is **/**.
## My solve
**Flag :** 'pwn.college{I77ZnbWFMrPYnouWc318HLE0wmz.QX5QTN0wCOwIzNzEzW}'

I simply changed my directory using _cd_ command to the root directory **/**, and then ran ***challenge/run*** , it is a relative path to my cwd which is /, following is an image for it.

<img width="505" height="149" alt="Screenshot 2025-09-24 at 8 13 07 PM" src="https://github.com/user-attachments/assets/6cb37d2f-6d1b-440f-aab6-59a2ca0100eb" />

## What I Learned
- I learned what a relative path is, and how is it interpreted relative to the _cwd_.
- I ran a program with a relative path while my cwd was the root directory.
### References
No external references were used for this challenge.

# Explicit relative paths, from /
### Problem statement 
Previously, your relative path was "naked": it directly specified the directory to descend into from the current directory. In this level, we're going to explore more explicit relative paths.

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: . and ... The first, ., refers right to the same directory, so the following absolute paths are all identical to each other:

/challenge
/challenge/.
/challenge/./././././././././
/./././challenge/././
The following relative paths are also all identical to each other:

challenge
./challenge
./././challenge
challenge/.
Of course, if your current working directory is /, the above relative paths are equivalent to the above absolute paths.

This challenge will get you using . in your relative paths. Get ready!
### Key points
- Previously, our relative path was **naked** i.e it used to directly specify, which directory to descend to from the cwd.
- Every directory has two **implicit entries** '.' and '..'. '.' refers right to the same directory.
- I was supposed to use a relative path with a '.' in it while cwd being /.
## My solve
**Flag :** 'pwn.college{ooHBgfgJHDFahAEF3qgVjnYj9-k.QXwUTN0wCOwIzNzEzW}'

I simply changed to the root directory and ran ***./challenge/run*** which is a relative path with a '.' in it, following is an image for it.

<img width="516" height="123" alt="Screenshot 2025-09-24 at 8 27 00 PM" src="https://github.com/user-attachments/assets/b04cf76a-2460-4b96-90f3-9f85a00ad810" />

## What I Learned
- I learned about the implicit entries.
- I learned about naked relative paths.
- I used a relative path with an implicit entry.
### References
None.

# Implicit relative path
### Problem statement
In this level, we'll practice referring to paths using . a bit more. This challenge will need you to run it from the /challenge directory. Here, things get slightly tricky.

Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path. Consider the following:

<img width="469" height="65" alt="Screenshot 2025-09-24 at 10 32 21 PM" src="https://github.com/user-attachments/assets/cca212ff-91e3-46b5-a3fe-017cee4478e5" />


This will not invoke /challenge/run. This is actually a safety measure: if Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will yield the following error:

<img width="466" height="45" alt="Screenshot 2025-09-24 at 10 32 37 PM" src="https://github.com/user-attachments/assets/2c9fca11-732a-46ec-a5a2-49beebcc30a7" />


We'll explore the mechanisms behind this concept later, but in this challenge, we'll learn how to explicitly use relative paths to launch run in this scenario. The way to do this is to tell Linux that you explicitly want to execute a program in the current directory, using . like in the previous levels. Give it a try now!
### Key points
- We have to invoke the program directly from the ***/challenge*** directory.
- After going to the challenge directory we cannot simply write run to invoke the program because linux doesn't find programs like that in a given directory.
- I was supposed to launch run by using a relaive path including '.'.
## My solve
**Flag :** 'pwn.college{0H8SkrhTb0iB1TomJcnDIq_v5Xy.QXxUTN0wCOwIzNzEzW}'

I simply changed to the /challenge directory and ran the ***./run*** and it ivoked the program by an implicit relative path and gave me the flag, following is an image for it.

<img width="518" height="99" alt="Screenshot 2025-09-24 at 10 53 48 PM" src="https://github.com/user-attachments/assets/cdcde8e4-8c84-4ceb-b58e-dddb3e67d066" />

## What I Learned
- How to invoke program from within the directory.
- Ran the ./run to invoke program.
### References 
No references
# Home Sweet Home
### Problem Statement
Every user has a home directory, typically under /home in the filesystem. In the dojo, you are the hacker user, and your home directory is /home/hacker. The home directory is typically where users store most of their personal files. As you make your way through pwn.college, this is where you'll store most of your solutions.

Typically, your shell session will start with your home directory as your current working directory. Consider the initial prompt:
<img width="471" height="45" alt="Screenshot 2025-09-25 at 12 17 58 AM" src="https://github.com/user-attachments/assets/3a66a14f-6839-4723-9f84-76a04a5ef3e7" />

The ~ in this prompt is the current working directory, with ~ being shorthand for /home/hacker. Bash provides and uses this shorthand because, again, most of your time will be spent in your home directory. Thus, whenever bash sees ~ provided as the start of an argument in a way consistent with a path, it will expand it to your home directory. Consider:

<img width="447" height="236" alt="Screenshot 2025-09-25 at 12 18 33 AM" src="https://github.com/user-attachments/assets/f62075fa-181a-4197-bdfa-c3ad0ac70094" />


Note that the expansion of ~ is an absolute path, and only the leading ~ is expanded. This means, for example, that ~/~ will be expanded to /home/hacker/~ rather than /home/hacker/home/hacker.

Fun fact: cd will use your home directory as the default destination:

<img width="450" height="84" alt="Screenshot 2025-09-25 at 12 18 59 AM" src="https://github.com/user-attachments/assets/871c27f8-1c91-4d7c-8914-b4bab804a46f" />


Now it's your turn to play! In this challenge, /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:

1.Your argument must be an absolute path.
2.The path must be inside your home directory.
3.Before expansion, your argument must be three characters or less.
Again, you must specify your path as an argument to /challenge/run as so:

<img width="471" height="46" alt="Screenshot 2025-09-25 at 12 19 51 AM" src="https://github.com/user-attachments/assets/03993802-1b1b-4ab9-8c5c-2fe8802fdd70" />

### Key points
- Every user has a home directory under _/home_ in the filesystem, my home directory in the dojo is _/home/hacker_
- Home directory is typically where users store most of their personal files.
- Shell session starts with the home directory as cwd, ~ is shorthand for /home/hacker.
- Whenever bash sees ~ provided as the start of an argument in a way consistent with a path, it will expand it to your home directory, only leading ~ is expanded.
- cd uses ~ as default destination.
- I was supposed to run /challenge/run which'll write the copy of the flag to any file I specify as an argument.

## My solve
**Flag :** 'pwn.college{EcMO6OZXR7NvCmO3uILWHT_qFii.QXzMDO0wCOwIzNzEzW}'

I ran ***/challenge/run*** with the argument ***~/c*** which was aligned with the 3 given constriants --> **Argument is absolute path, Path is inside home directory, Argument before expansions is 3 characters or less.**

Image:

<img width="472" height="90" alt="Screenshot 2025-09-25 at 12 37 30 AM" src="https://github.com/user-attachments/assets/4578c14e-7048-42e1-b46e-8fe17854d0a6" />

## What I learned
- I learned about the home directory, what my home directory is and how is it represented in the first prompt, and how most users save thier personal files in it.
- Figured a out a way to give an argument following the constraints and getting a copy of the flag.
### References
Based purely on reasoning and standard tools.
                     







   


