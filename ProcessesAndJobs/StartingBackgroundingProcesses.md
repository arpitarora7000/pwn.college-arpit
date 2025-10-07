# Starting Background Processes
### Key Points
1. Of course, you don't have to suspend processes to background them: you can start them backgrounded right off the bat! It's easy; all you have to do is append a & to the command, like so:

<img width="470" height="211" alt="Screenshot 2025-10-08 at 1 19 00 AM" src="https://github.com/user-attachments/assets/97d5a211-b645-408a-8066-e456d6301a13" />

Here, sleep is actively running in the background, _not suspended_.

2. Launch /challenge/run backgrounded for the flag!

## My solve
**Flag :** `pwn.college{wQw5uC4NV3yTOZ3QBzbf_f02RTe.QX5QDO0wCOwIzNzEzW}`

All I had to do was to append the `&` with the command for it to be backgrounded and actively running, without even suspending it once.

<img width="593" height="278" alt="Screenshot 2025-10-08 at 1 23 31 AM" src="https://github.com/user-attachments/assets/4c312120-d4ea-4ecd-aa84-22e6bdcfe5ce" />

## What I Learned
- I'd already learned about backgrounding processes, using the `bg` command, but that method was applicable only after once suspending the prcess using `ctrl-z`, here I learned about a new method to do it without suspending, which is by appending the `&` character to the command.

### References
None.
