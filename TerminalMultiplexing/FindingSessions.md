# Finding Sessions
### Key points
1. If we end up with multiple sessions running, it is a task to find which one to reattach to.
2. Well, we can list them to figure out:

 <img width="443" height="165" alt="Screenshot 2025-10-10 at 11 13 02 PM" src="https://github.com/user-attachments/assets/9e14d787-5bda-4d59-835d-e0da3d2e7ad0" />

3. The identifiers of the sessions are the PID of each respective screen process, a dot, and the name of the screen session. To attach to a specific one, you use its **name or its PID** by giving it as an argument to `screen -r`.
4. This challenge has 3 screens, two have decoy flags, one has real, finding the real flag is the task.

## My solve
**Flag :** `pwn.college{UVCdoh8gwGl0W0lyvRoPA6ediK6.01N4IDOxwCOwIzNzEzW}`

Used the `screen -ls` command to see the screens, and `screen -r PID`, to reatach to particular screen, then tried, and found the flag in the second one.

<img width="636" height="169" alt="Screenshot 2025-10-10 at 11 17 00 PM" src="https://github.com/user-attachments/assets/8eec9d5f-e041-4f1c-99b4-33eeba306f24" />

<img width="467" height="190" alt="Screenshot 2025-10-10 at 11 17 12 PM" src="https://github.com/user-attachments/assets/17453af2-3b9b-44d7-a7ea-66be069b9610" />

## What I Learned
- Learned how `-ls`, can be used as `screen -ls`, to look at screens, and `screen -r` used with PID or name tto reatach.

### References
None.
