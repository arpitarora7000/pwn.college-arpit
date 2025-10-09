# Changing File Ownership
### Key points
1. Every file in Linux is owned by a user on the system, and most often the user is the user we logi as everyday.
2. On a shared system (such as in a computer lab), there might be many people with different user accounts, all with their own files in their own home directories. But even on a non-shared system (such as personal PC), Linux still has many "service" user accounts for different tasks.
3. The two most important user accounts are:
 - My user account! On pwn.college, this is the _hacker_ user, regardless of what my username is.
 - root. This is the administrative account and, in most security situations, the ultimate prize. If we take over the root user, we've almost certainly achieved the hacking objective!
4. So, the /flag file containing the flag is only accessible by the `root` user, to access it either we have to become root, or can change the owner of the file.
5. Interestingly, we can change the ownership of files! This is done via the `chown` (change owner) command:

   <img width="305" height="43" alt="Screenshot 2025-10-10 at 12 14 27 AM" src="https://github.com/user-attachments/assets/30738b54-fa6a-4cb6-a0ac-59676b56bdf2" />

6. Typically, `chown` also can be only used by the root.
7. If the owner is changed from root to hacker, then we can do everything that the root had been able to do all along.
8. Here, I have to change the owner of `/flag` file, using `chown` which is typically only usable by `root`, but in this challenge is usable by us.

## My solve
**Flag :** `pwn.college{otJd5QM6Qm75BioDFTKrbTTCMxX.QXxEjN0wCOwIzNzEzW}`

I just simply ran `chown hacker /flag`, which did it's work as was required, following is an image:

<img width="521" height="319" alt="Screenshot 2025-10-10 at 12 18 41 AM" src="https://github.com/user-attachments/assets/73b2dfa1-67a7-47d8-8d29-f76f9d5e2afd" />

## What I Learned
- Learned about file ownership, and how it can be changed using a new command `chown`, which is typically only usable by root.

### References
None.

 
