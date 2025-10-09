# Building on Success
### Key points
1. The && operator allows you to run a second command only if the first command succeeds (in Linux convention, this means it exited with code 0). This is called the "AND" operator because both conditions must be true: the first command must succeed AND then the second command will run. That's super useful for complex commandline workflows where certain actions depend on the success of other actions.

Here's the syntax:

<img width="459" height="39" alt="Screenshot 2025-10-10 at 2 39 43 AM" src="https://github.com/user-attachments/assets/bb4ae85e-7aa7-483a-8679-81ded1152ecc" />

This means: "Run command1, and IF it succeeds, then run command2."

2. This challenge --> `In this challenge, you need to chain the programs /challenge/first-success and /challenge/second using the && operator. Try running each command separately first to see what happens (which is that you will not get the flag). But if you chain them with &&, the flag will appear!`

## My solve
**Flag :** `pwn.college{sTSG5o119-VQN6Rja711INhtD9m.0lM0MDOxwCOwIzNzEzW}`

Ran the given commands individually, didn't get the flag and then ran them together by chaining with `&&`, to get the flag.

<img width="622" height="175" alt="Screenshot 2025-10-10 at 2 46 04 AM" src="https://github.com/user-attachments/assets/53d41032-adea-45cd-9ff9-1b6cbda14710" />

## What I Learned
- Learned about the `&&` operator which is similar to `AND` in coding languages, when the first command succeeds then then only the second one does.

### References
No external references.
