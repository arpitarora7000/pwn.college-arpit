# The PATH variable
### Key points
1. It turns out that the answer to "How does the shell find ls?"(question from the proem) is fairly simple. There is a special shell variable, called PATH, that stores a bunch of directory paths in which the shell will search for programs corresponding to commands. If you blank out the variable, things go badly:

<img width="462" height="191" alt="Screenshot 2025-10-10 at 11 44 38 PM" src="https://github.com/user-attachments/assets/d9359405-f263-4b9b-b234-efb7cdfa7955" />

Without a PATH, bash cannot find the `ls` command. 

2. for this challenge --> `In this level, you will disrupt the operation of the /challenge/run program. This program will DELETE the flag file using the rm command. However, if it can't find the rm command, the flag will not be deleted, and the challenge will give it to you! Thus, you must make it so that /challenge/run also can't find the rm command!`

> Keep in mind: /challenge/run will be a child process of your shell, so you must apply the concepts you learned in Shell Variables to mess with its PATH variable! If you don't succeed, and the flag gets deleted, you will need to restart the challenge to try again!

## My solve
**Flag :** `pwn.college{MQdJDU4Mt1LeT2pJK6KZxaztl1M.QX2cDM1wCOwIzNzEzW}`

I just ran `PATH=""`, which removed contents of PATH, then `/challenge/run`, which wasn't able to find the `rm` command anymore, so couldn't delete flag.

<img width="473" height="133" alt="Screenshot 2025-10-10 at 11 48 56 PM" src="https://github.com/user-attachments/assets/a1e39e29-d13c-4c25-9888-ed491b2ec0c3" />

## What I Learned
- Learned about the shell variable called `PATH`, how if it's contents are removed basic commands are not usable.

### References
None.
