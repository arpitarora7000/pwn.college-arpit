# Launching Screen
### Key points
1. `screen` creates virtual terminals inside the terminal, it's somewhat like having multiple browser tabs, but for your command line!
2. Starting screen is super simple:

 <img width="257" height="32" alt="Screenshot 2025-10-10 at 10 52 07 PM" src="https://github.com/user-attachments/assets/d1470441-1e54-4788-9977-647d0449ce7c" />

Yes, that is all, now we're inside a screen session, it looks exactly like a terminal, but there are new capabilities there, waiting to be discovered.

3. Just launching screen will get the flag here.

> NOTE: When you're done with your command line, type exit or press Ctrl-D to leave the screen session. Then screen will terminate and return you to your original shell.

## My solve
**Flag :** `pwn.college{0y9P9PDQL8l-vPmO4cCj2inkLbn.0VN4IDOxwCOwIzNzEzW}`

I just launched a screen session to get the flag.

<img width="576" height="109" alt="Screenshot 2025-10-10 at 10 57 24 PM" src="https://github.com/user-attachments/assets/38b251e0-60c7-4f9d-a8ce-53caf0b725e9" />

## What I Learned
- Learned about how can we create a virtual terminal inside a terminal, and how can i terminate it.
- Learned about the new command `screen`,

### References
None.
