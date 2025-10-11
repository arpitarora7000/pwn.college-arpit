# Hijacking Commands
### Key points
1. Similar to the first challenge, `/challenge/run`, deleted flag by the `rm` command, but if the PATH is set differently, it still won't print anything for us.
2. So, here by writing a shell script, we'll have to change contents of rm so that it prints out flag instead of deleting.

## My solve
**Flag :** `pwn.college{EQGoYMYKPEAaROaYZbXREcD-pPB.QX3cjM1wCOwIzNzEzW}`

I created a shell script called `rm`, then with a shebang, wrote in it the absolute path of cat, which I got by `which cat`, and then `/flag`, which printed out the flag, saved the script, and made it executable, then I set PATH variable so it has the new `rm`, command, then ran `/challenge/run`.


<img width="522" height="314" alt="Screenshot 2025-10-11 at 3 16 36 PM" src="https://github.com/user-attachments/assets/074482de-92b5-41fb-8828-261ad1a29cef" />

## What I Learned
- Compiled all the knowledge, from previous chellenge, where I created the `win`, script, and did similar things, used knowledge of variables also.

### References
SENSAI
