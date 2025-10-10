# Reading shell scripts
### Key points
1. The shell scripts come in very handy for doing simple "system-level" tasks, so are a common tool that _developers_ and _sysadmins_ reach for, in fact, a surprising fraction of the programs on a typical Linux machine are shell scripts.
2. For this challenge --> `In this level, we will learn to read shell scripts. /challenge/run is a shell script that requires you to put in a secret password, but that password is hardcoded into the script iself! Read the script (using, say, cat), figure out the password, and get the flag!`

> NOTE: Feel free to try to read the code of other challenges as well! Reading code is a critical strategy in learning new skills, because you can see how certain functionality was implemented and reuse those strategies in your own scripts. But watch out: some program files are machine code, and will not be readable to humans. You can use the file command to differentiate, but almost all the challenges in the Linux Luminarium are implemented as shell scripts and are safe to cat out.

## My solve
**Flag :** `pwn.college{88PpCiXbi7F8VtFukoe9S0eHhQu.0lMwgDOxwCOwIzNzEzW}`

I simply catted out the `/challenge/run`, file, figured out the flag invoked `/challenge/run`, gave the password to get the flag.

<img width="605" height="313" alt="Screenshot 2025-10-10 at 10 46 29 PM" src="https://github.com/user-attachments/assets/b23c356a-371a-44c9-a04a-67c4e516d760" />

I also checked out the code for the previous challenge's `/challenge/run`, which was aligned with the requirements of the previous challenge.

## What I Learned
- I learned that how shell scripts are a frequently used tool, and can be readble, here by putting in a password.
- Reading can make one understand the concept deeply.

### References
None.
  
