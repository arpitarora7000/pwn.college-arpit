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
None.
# Position thy self 
## Problem Statement

The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:

hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!
### Key points
- One can navigate around all the files and directories in a filesystem by using the ***cd*** command.
- This affects the _current working directory_ of your process, in essence all your commands are now running in the directory that you,ve changed to.
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
None.
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




   


