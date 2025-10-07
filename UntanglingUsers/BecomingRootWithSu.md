# Becoming root with su
### Key points
1. It's not just hackers that need to become `root`. Oftentimes, you, as the **owner** of your computer, need to use root access to administer it. Becoming root is a fairly common action that Linux users take, and there are two utilities that exist for this purpose: `su` and `sudo`.
2. This challenge is about covering the older one `su` it's probably short for _the substitute user command_, this is not typically used to elevate to _root_ access anymore, but it's an elegant utility from a more civilised time.
3. `su` is a setuid binary:
 
> hacker@dojo:~$ ls -l /usr/bin/su
> 
> -rwsr-xr-x 1 root root 232416 Dec 1 11:45 /usr/bin/su
> 
> hacker@dojo:~$

Because it has the **SUID** bit set, su runs as root. Running as root, it can start a root shell! Of course, su is discerning: before allowing the user to elevate privileges to root, it checks to make sure that the user knows the root password: 

<img width="394" height="116" alt="Screenshot 2025-10-08 at 2 24 22 AM" src="https://github.com/user-attachments/assets/35a796b7-3285-4224-bd27-73cb7927cbc8" />

This check against the root password is what obsoletes su. Modern systems very rarely have root passwords, and different mechanisms (that we will learn later) are used to grant administrative access.

4. But, in this and only this challenge there is password set for root (root password) which is `hack-the-planet`, and one must provide it to `su` to become root.

## My solve
**Flag :**`pwn.college{4OY4M3X_ctE0Gr370MbAGljAYkx.QX1UDN1wCOwIzNzEzW}`

I firstly ran `ls -l` to check for files in `~` then ran `su`, then gave it the root password and became the root, catted out the flag file to get the flag.

<img width="556" height="305" alt="Screenshot 2025-10-08 at 2 27 52 AM" src="https://github.com/user-attachments/assets/ffd9eebe-e732-4b96-8a8a-53515dec9e58" />

## What I Learned
- Learned about, how a user can get administrative access using su, the command which is now obsoleted, due to the complication of _root password_, which is no longer existent in modern systems.
- Elevated to root for the first time, using `su`, and catted out my flag by looking at the existent files.

### References
No external references other than in-challenge hints.

