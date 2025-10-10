# Scripting With Conditionals
### Key points
1. In bash, you can use if statements to make decisions:

<img width="326" height="108" alt="Screenshot 2025-10-10 at 8 54 15 PM" src="https://github.com/user-attachments/assets/4f9dbc7e-c47d-4545-bc08-1669b1894bac" />

The above, in English, is if the first argument is "ping", print out "pong". The syntax is somewhat unforgiving for a few reasons. First, you must have spaces after if (if you're used to a language like C, this is different), after [, and before ]. Second, if, then, and fi must all be on different lines (or separated by semicolons); you can't lump them into the same statement. It's also a bit weird: instead of endif or end or something like that, the terminator of the if statement is fi (if backwards). Just something you have to remember.

2. For this challenge --> For this challenge, write a script at /home/hacker/solve.sh that:

 - Takes one argument
 - If the argument is "pwn", output "college"
 - For any other input, output nothing

 Example:

> hacker@dojo:~$ bash /home/hacker/solve.sh pwn
> 
> college
> 
> hacker@dojo:~$ bash /home/hacker/solve.sh foo
> 
> hacker@dojo:~$

Once your script works correctly, run /challenge/run to get your flag!

## My solve
**Flag :** `pwn.college{wd9PYI7Yc7n8gXKl7R1-tyKsZpF.0lNzMDOxwCOwIzNzEzW}`

I wrote the following to the shell script solve.sh, to get the flag:

<img width="492" height="165" alt="Screenshot 2025-10-10 at 9 04 28 PM" src="https://github.com/user-attachments/assets/5b8b7828-6056-4040-ba03-f795561c4eae" />

## What I Learned
- Learned about using conditional statements in the shell scripts, and the exact syntax to be taken care of.

### References
None.
 
