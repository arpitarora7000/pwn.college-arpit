# Executable Files
### Key points
1. This challenge is not about making a file readble, to cat it out, but to make one executable, exploring execute permissions.
2. When /challenge/run is invoked, Linux will executed only if, I have execute-access, to the program file.
3. For this challenge --> `In this challenge, the /challenge/run program will give you the flag, but you must first make it executable! Remember your chmod, and get /challenge/run to tell you the flag!`
 
## My solve
**Flag :** `pwn.college{wOw-LABHCwYePMRfc6Xk67iOVrE.QXyEjN0wCOwIzNzEzW}`

Checked permissions for the program file `/challenge/run` then ran `hmod u+x /challenge/run`, checked permissions again, It'd added the execute permission for the user, then invoked the program to get the flag.

<img width="560" height="186" alt="Screenshot 2025-10-10 at 1 28 20 AM" src="https://github.com/user-attachments/assets/712b5a2c-7c07-4947-ac10-ab3715d8208f" />

## What I Learned
- Learned about how a program if invoked, executes only if, the user has execute-access.
- Added execute permssion for the user(hacker), to make it executable.

### References
No external references.
