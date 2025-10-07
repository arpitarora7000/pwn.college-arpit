# Other users with su
### Key points
1. With no arguments, su will start a root shell (after authenticating with root's password). However, you can also give a username as an argument to switch to that user instead of root. For example:

<img width="313" height="88" alt="Screenshot 2025-10-08 at 2 33 16 AM" src="https://github.com/user-attachments/assets/0287a308-d357-4707-a828-b28c1bce4141" />

2. In this challenge, I gotta switch to `zardus` user and then run /challenge/run to get the flag, password for it is `dont-hack-me`.

## My solve
**Flag :** `pwn.college{E2h9ZvcHO4mXvsfMNyMdU91-H6n.QX2UDN1wCOwIzNzEzW}`

Simply ran the `su` command with 'zardus' as argument, then it asked for password, after authenticating I became the user zardus and then ran /challenge/run to get the flag.

<img width="455" height="124" alt="Screenshot 2025-10-08 at 2 36 39 AM" src="https://github.com/user-attachments/assets/0f26c4b9-8c86-4a32-8bad-b738181f4e6a" />

## What I Learned
- Learned about another application of `su`, which is to switch to other users, not just root, just by putting that user name as argument and then giving password.

### References
None.
 


