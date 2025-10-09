# Fun with group names
### Problem statement

In the previous levels, you may have noticed that your hacker user is a member of the hacker group, and that zardus is a member of the zardus group. There is a convention in Linux that every user has their own group, but this does not have to be the case. For example, many computer labs will put all of their users into a single, shared users group.

The point is, you've used hacker for the group before, but in this level, that is not going to work. I'll still allow you to use chgrp, but I have randomized the name of the group that your user is in. You will need to use the id command to figure that name out, then chgrp to victory!

> Basically, now the group name that the hacker user is in is randomized, that can be checked by the `id` command and then use `chgrp` to change group ownership, and access flag through `/flag`.

## My solve
**Flag :** `pwn.college{Ub2PBUui5Qug5g_YmSy-lW0B6ca.QXycjM1wCOwIzNzEzW}`

I just simply ran the following commands to get the flag:

<img width="584" height="313" alt="Screenshot 2025-10-10 at 12 51 07 AM" src="https://github.com/user-attachments/assets/a23d0844-b256-459e-bb5d-af3ae480aef6" />

## What I Learned
- Ran the `id`, and `chgrp` simultaneously, to get the group name then change group ownership and get the flag.

### References
None.
