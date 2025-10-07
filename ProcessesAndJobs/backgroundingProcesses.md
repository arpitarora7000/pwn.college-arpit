# Backgroundig Processes
### Key points
1. We've resumed processes in the foreground with the fg command. We can also resume processes in the background with the bg command! This will allow the process to keep running, while giving you your shell back to invoke more commands in the meantime.
2. In this challenge, invoking /challenge/run needs another copy of it already running in the background, _not suspended_ in the same terminal then it'll give the flag.
 
## My solve
**Flag :** `pwn.college{AEjAhKIJUmLvweW4ONRdaVCqJor.QX3QDO0wCOwIzNzEzW}`

I just ran `/challenge/run`, which said it'll give the flag only if there's a copy of it running in the background, and not suspended, following is an image of how I did it using the `bg` command.

<img width="598" height="574" alt="Screenshot 2025-10-08 at 1 08 30 AM" src="https://github.com/user-attachments/assets/424bf743-74cd-4583-9b9e-be42162d7d7b" />

## What I Learned
- Learned about the new `bg` command, which is useful to resume suspended processes in the background, giving the terminal back to give more commands.

### References
No xternal references used to solve.
