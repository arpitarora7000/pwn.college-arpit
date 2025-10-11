# The SUID bit
### Key points

Statement:

As you explored in the previous module, there are many cases in which non-root users need elevated access to do certain system tasks. The system admin can't be there to give them the password every time a user wanted to do a task that only root/sudoers can do. Instead, the "Set User ID" (SUID) permissions bit allows the user to run a program as the owner of that program's file.

This is actually the exact mechanism used to let the challenge programs you run read the flag or, outside of pwn.college, to enable system administration tools such as su, sudo, and so on. The permissions of a file with SUID look like this:

> hacker@dojo:~$ ls -l /usr/bin/sudo
> 
> -rwsr-xr-x 1 root root 232416 Dec 1 11:45 /usr/bin/sudo
> 
> hacker@dojo:~$

The s part in place of the executable bit means that the program is executable with SUID. It means that, regardless of what user runs the program (as long as they have executable permissions), the program will execute as the owner user (in this case, the root user).

As the owner of a file, you can set a file's SUID bit by using chmod:

> chmod u+s [program]

But be careful! Giving the SUID bit to an executable owned by root can give attackers a possible attack vector to become root. You will learn more about this in the Program Misuse module.

Now, we are going to let you add the SUID bit to the /challenge/getroot program in order to spawn a root shell for you to cat the flag yourself!

## My solve
**Flag :**`pwn.college{UkOSLANyZQpjpeo71mCfGco4W_i.QXzEjN0wCOwIzNzEzW}`

I set the SUID bit for the /challenge/getroot, then ran it, it made me the root, then I catted out the flag.

<img width="626" height="134" alt="Screenshot 2025-10-11 at 3 39 14 PM" src="https://github.com/user-attachments/assets/8670880d-58d5-4916-860d-4101cb22331a" />

## What I Learned
- Learned abou the SUID-bit in the permissions, how it allows a program to run as root, and allows to execute.

### References 
None.
 

