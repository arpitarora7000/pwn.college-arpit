# Foregrounding Processes
### Key points
1. This challenge is about _foregrounding_ the earlier backgrounded process, using the `fg` command that we've learnt about already.
2. So in this challenge suspend the `run` then resume it in the background, then foreground it to get the flag.

## My solve
**Flag :** `pwn.college{8zGXvrINPC2aGTfLvdkzU8qfWQC.QX4QDO0wCOwIzNzEzW}`

I just ran `/challenge/run` and it said that it needs to be suspended then backgrounded, after doing that it asked to be foregrounded using the `fg` command, without re-suspending it, which eventually gave out the flag.

<img width="606" height="409" alt="Screenshot 2025-10-08 at 1 15 19 AM" src="https://github.com/user-attachments/assets/7b0946db-9899-40e9-aded-7fcb7a1c97fc" />

## What I Learned
- Learned about foregrounding an already backgrounded process, using a familiar command `fg`.
- Suspended the process, resumed it in background, foregrounded it, did all three in one challenge.

### References
None.
