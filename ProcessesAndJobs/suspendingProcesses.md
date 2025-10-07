# Suspending Processes
### Key points
1. We've used the `ctrl-c` multiple times to interrupt processes, but there are less drastic measures, that one can use to get the terminal back.
2. One can suspend processes in the background by `ctrl-z`.
3. This challenge is about learning to suspend processes, and the next is about learning how to resume those suspended processes.
4. This level's run wants to see another copy of itself running and using the same terminal. How? Use the terminal to launch it, then suspend it, then launch another copy while the first is suspended!
## My solve
**Flag :** `pwn.college{UGXxjdWs_dF2bQMHgDQhsxN8qkO.QX1QDO0wCOwIzNzEzW}`

I just simply launched /challenge/run, it said that it needs to be suspended and run again to get the flag, did that and it gave out the flag, following is an image for it:

<img width="602" height="405" alt="Screenshot 2025-10-07 at 5 01 02 PM" src="https://github.com/user-attachments/assets/6a7c388e-b56d-4ab5-bed0-96d53861a2d1" />

## What I Learned
- Learned about the new `Ctrl-z` operation which is less drastic than `Ctrl-c` and does the work of suspending running processes, which can be later resumed.

### References
No external references used for this challenge.
