# Switching windows 
### Key points
1. Inside a single screen session, you can have multiple windows, like your browser has multiple tabs. This can be super handy for organizing different tasks!
2. These windows are handled with different keyboard shortcuts, all starting with Ctrl-A:

 <img width="458" height="202" alt="Screenshot 2025-10-10 at 11 20 34 PM" src="https://github.com/user-attachments/assets/6e956912-38db-4ece-96d4-d186523425df" />

3. Here, a screen session is set up with 2 windows, attach to the session with `screen -r`, then use one of the key combinations above to switch to Window 1.

## My solve
**Flag :** `pwn.college{4O0M2PI-CY-nJ3bPrKVDwM18XXn.0FO4IDOxwCOwIzNzEzW}`

Just reattached, and then window 1 opened, then switched to window 0 to get the flag.

<img width="599" height="160" alt="Screenshot 2025-10-10 at 11 24 05 PM" src="https://github.com/user-attachments/assets/a59c5b04-ca1b-4fb7-a643-73e90b2c9f9d" />

<img width="464" height="296" alt="Screenshot 2025-10-10 at 11 24 27 PM" src="https://github.com/user-attachments/assets/b2fcb9cb-058f-446e-906d-adf3c87650b3" />

<img width="490" height="79" alt="Screenshot 2025-10-10 at 11 24 40 PM" src="https://github.com/user-attachments/assets/6939f138-f413-4bc1-9748-1be9d5146331" />

## What I Learned
- Learned that a screen can be more than just a virtual terminal, it can have multiple windows inside it.
- Learned about commands to siwtch between windows, create new window, and other things.

### References
No external references used for the solutions.
