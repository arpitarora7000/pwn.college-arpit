# Killing Processes
### Key points
1. This challenge is about learning to terminate processes.
2. This is done using the agressively named `kill` command, `kill` will terminate a process in a way that gives it a chance to get its affairs in order before ceasing to exist.
3. Let's say you had a pesky sleep process (sleep is a program that simply hangs out for the number of seconds specified on the commandline, in this case, 1337 seconds) that you launched in another terminal, like so:

<img width="399" height="42" alt="Screenshot 2025-10-07 at 12 40 33 AM" src="https://github.com/user-attachments/assets/ec7a7132-7d56-4929-8da4-56b930d6f18f" />

4. How do we get rid of it? You use kill to terminate it by passing the process identifier (the PID from ps) as an argument, like so:

<img width="424" height="141" alt="Screenshot 2025-10-07 at 12 41 26 AM" src="https://github.com/user-attachments/assets/b943ad54-e7a2-4143-93c8-eece8e32c180" />

5. Now , here /challenge/dont_run is launched, we've to terminate it and then launch /challenge/run to get the flag.

## My solve
**Flag :** `pwn.college{gdhyuFa46KDUJxIHQUita2jc09a.QXyQDO0wCOwIzNzEzW}`

I ran `ps -ef` to check the PID for /challenge/dont_run, then used the kill command, to terminate the process, and then checked again if its deleted or not, it was, then ran /challenge/run to get the flag.

<img width="687" height="170" alt="Screenshot 2025-10-07 at 1 03 48 AM" src="https://github.com/user-attachments/assets/91f3b9ed-2071-4e2e-a0e1-f6f30f32fa98" />

<img width="661" height="160" alt="Screenshot 2025-10-07 at 1 04 32 AM" src="https://github.com/user-attachments/assets/fb09a2fc-5d23-45a4-8834-bdcf434187ff" />

## What I Learned
- Learned about the new `kill` command, which is very useful to terminate running processes, all it requires is the PID for the particular process, which one can get by using `ps -ef`.

### References
None.

