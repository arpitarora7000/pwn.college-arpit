# Using Sudo 
### Key Points

Some History:


In the olden days, a typical Linux system had a root password that administrators would use to su to root (after logging into their account with their normal account password). But root passwords are a pain to maintain, they (or their hashes!) can leak, and they don't lend themselves well to larger environments (e.g., fleets of servers). To address this, in recent decades, the world has moved from administration via su to administration via sudo (Fun Fact: sudo originally stood for superuser do, but has changed to "su 'do'", and because su stands for "substitute user", the current meaning of sudo is "substitute user, do").

1. Unlike su, which defaults to launching a shell as a specified user, sudo defaults to running a command as root:

<img width="351" height="131" alt="Screenshot 2025-10-08 at 3 28 05 AM" src="https://github.com/user-attachments/assets/97e453cd-08c4-4edd-b20c-ab92161c24ae" />

Or, more relevant to getting flags:

> hacker@dojo:~$ grep hacker /etc/shadow
> 
> grep: /etc/shadow: Permission denied
> 
> hacker@dojo:~$ sudo grep hacker /etc/shadow
> 
> hacker:$6$Xro.e7qB3Q2Jl2sA$j6xffIgWn9xIxWUeFzvwPf.nOH2NTWNJCU5XVkPuONjIC7jL467SR4bXjpVJx4b/bkbl7kyhNquWtkNlulFoy.:19921:0:99999:7:::
> 
> hacker@dojo:~$

2. Unlike `su`, which relies on password authentication, `sudo` checks policies to determine whether the user is authorized to run commands as `root`. These policies are defined in `/etc/sudoers`, and though it's mostly out of scale for our purposes, there are plenty of resources for learning about this!

So, the world has moved to sudo and has (for the purposes of system administration) left su behind. In fact, even pwn.college's Practice Mode works by giving you sudo access to elevate privileges! 

3. In this challenge, `sudo` access is given, by using it we've to get the flag nice and easy.

> NOTE: After this level, we will enable Privileged Mode! When you launch a challenge in Privileged Mode (by clicking the **Privileged** button instead of the **Start** button), the resulting container will give you full `sudo` access to allow you to introspect and debug to your heart's content, but of course with a placeholder flag.

## My solve
**Flag :** `pwn.college{wBHwYuqs1u5Px1HvSn7nAuI9zEd.QX4UDN1wCOwIzNzEzW}`

I just first checked the files, then ran `sudo cat /flag` which gave out the flag, if I'd catted out the /flag file without sudoing it would've said permission denied, but sudoing gives full access.

<img width="458" height="84" alt="Screenshot 2025-10-08 at 3 35 47 AM" src="https://github.com/user-attachments/assets/2e2bde08-93f8-4535-820c-38d2da76626f" />

## What I Learned
- Learned alot about the `sudo` method to get administrative access, it's all history is mentioned above, learned that sudo gives access based on policies which determine whether or not the user is authorized to get access, and these policies are saved in /etc/sudoers.
- Learned about how sudo defualts to running a command as root, and doesn't default to launching a shell as a specified user as in su.
- Learned about the privileged mode.

### References
No external references used.
