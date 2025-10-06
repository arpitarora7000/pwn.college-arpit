# Interrupting Processes
### Key Points
1. We've learned how to kill other processes with the kill command, but sometimes you just want to get rid of the process that's clogging up your terminal! Luckily, terminals have a hotkey for this: Ctrl-C (e.g., holding down the Ctrl key and pressing C) sends an "interrupt" to whatever application is waiting on input from the terminal and, typically, this causes the application to cleanly exit.
2. Here, I just have to interrupt /challenge/run to get the flag.

## My solve
**Flag :** `pwn.college{sUKAinNBKspmx4MlHshDlAiTbdw.QXzQDO0wCOwIzNzEzW}`

I just simply ran /challenge/ran, then it said the following:

<img width="571" height="55" alt="Screenshot 2025-10-07 at 1 11 48 AM" src="https://github.com/user-attachments/assets/c71a4c42-66e8-43d6-b192-10df971bbda7" />

Then I held the control key and pressed c which gave out the flag.

<img width="633" height="91" alt="Screenshot 2025-10-07 at 1 12 22 AM" src="https://github.com/user-attachments/assets/906e4aa0-bafe-491f-b5b0-290451c2ca7d" />

## What I Learned
- Learned about interrupting processes, using the `Ctrl-c`, this is useful when one just wants to get rid of the processes that are clogging up the terminal.

### References
No external references.
