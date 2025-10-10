# Detaching and attaching
### Key points
1. If someone is working on something important over a remote connection, everything will be gone if the connection drops, with `screen`, the work keeps running and can be _reattached_ later.
2. One can also deatach on purpose, which this challenge is about.
3. Simply by pressing `ctrl-a`, followed by `d`, this leaves the session running in background while we've returned to the normal terminal.

 <img width="408" height="135" alt="Screenshot 2025-10-10 at 11 03 48 PM" src="https://github.com/user-attachments/assets/423d57f3-8d91-44ce-a7bf-ec41904636f2" />

4. To reattach, we can use the `-r` argument to screen:

 <img width="344" height="35" alt="Screenshot 2025-10-10 at 11 04 42 PM" src="https://github.com/user-attachments/assets/4cbc4157-5779-47b9-aeaf-7869217c4f3f" />

<img width="469" height="203" alt="Screenshot 2025-10-10 at 11 05 00 PM" src="https://github.com/user-attachments/assets/1c1c84d4-63fd-4b52-8cc1-29ff62b0741a" />

> FUN FACT: Ctrl-A is screen's activation key for all of its shortcuts in its default configuration. All screen functionality is activated by some command combination starting with Ctrl-A.

> HINT: Remember: Hold Ctrl and press A, then release both and press d.

> HINT: If you see [detached from...], you did it right!

## My solve
**Flag :**  `pwn.college{Q-36xeVThfg2cmrIS7BFyfE_tdL.0lN4IDOxwCOwIzNzEzW}`

I just followed the steps one after the other, and also the hints given on the terminal and problem statement, to get the flag.

<img width="624" height="263" alt="Screenshot 2025-10-10 at 11 09 21 PM" src="https://github.com/user-attachments/assets/2fe572ee-c71f-49c9-a92f-e3fd7ef19724" />


after reattaching:

<img width="622" height="117" alt="Screenshot 2025-10-10 at 11 08 22 PM" src="https://github.com/user-attachments/assets/565c1a11-f859-48aa-8e23-912109513df5" />

## What I Learned
- Learned about the commands to attach and detach, learned how helpful it is in connection loss, and also if voluntarily wanting to go back to terminal.

### References
No external resources used.
