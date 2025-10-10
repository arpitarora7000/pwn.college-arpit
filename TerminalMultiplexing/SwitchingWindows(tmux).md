# Switching Windows (tmux)
### Key points
1. Just like screen, tmux has windows. The key combos are different, but the concept is the same:
   
<img width="483" height="183" alt="Screenshot 2025-10-10 at 11 34 15 PM" src="https://github.com/user-attachments/assets/90e9424b-7071-46c4-8576-3b4270efda4d" />

Tmux shows your windows at the bottom in a status bar that looks like:

<img width="231" height="37" alt="Screenshot 2025-10-10 at 11 34 38 PM" src="https://github.com/user-attachments/assets/9ee4f8db-9a3e-4497-9606-06d17b38f22b" />

2. The * shows your current window, and each entry also shows the process that the window was created to run.

3. Here, there is a tmux session with two windows, window 0 has the flag.

## My solve
**Flag :** `pwn.college{wbW3p6JHzk21MKJ_XSSa1l0D3uS.0FM5IDOxwCOwIzNzEzW}`

I just wrote `tmux a`, got to the first window then changed to 0th using `ctrl-b 0`, and got the flag.

<img width="589" height="392" alt="Screenshot 2025-10-10 at 11 38 10 PM" src="https://github.com/user-attachments/assets/7da5eaf3-464a-4b9c-8a9c-a7530bb9fbd2" />

<img width="588" height="152" alt="Screenshot 2025-10-10 at 11 38 48 PM" src="https://github.com/user-attachments/assets/db8e3626-4a05-42f4-856a-70f9bf27a087" />

## What I Learned
- Learned about how there are windows in `tmux` exactly like screen, can be changed just by changing the command prefix, following the same commands.
- Learned where is the window shown which is the status bar at the bottom.
- _*_ shows the current window.
 
### References
None.
 
