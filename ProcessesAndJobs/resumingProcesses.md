# Resuming Processes
### Key points
1. The suspended processes need to be resumed at some point of time, otherwise, why not just terminate them?
2. For resuming there is this `fg` command a builtin that takes the suspended process, resumes it, and puts it back in the foreground of the terminal.
3. Here, the run needs to be suspended then resumed.

## My solve
**Flag :** `pwn.college{0VV0l2u12MuG5UBxKw2wQBRtbS2.QX2QDO0wCOwIzNzEzW}`

I just simply launched /challenge/run, it said it needs to be suspended then resumed for it to give out the flag, following is an image of how I did it:

<img width="602" height="206" alt="Screenshot 2025-10-07 at 5 08 05 PM" src="https://github.com/user-attachments/assets/508a8ff7-9fed-4097-8129-3a1b1862b5d4" />

## What I Learned
- Learned about the new `fg` command, which resumes suspended processes.

### References
No exterenal references.
