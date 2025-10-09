# Changing Permissions
### Key Points
1. Learned already about permissions a little in the proem, that how after doing `ls -l` the first character is the file type.
2. Each character of the three represent permission for a different type:

> r - user/group/other can read the file (or list the directory)
> 
> w - user/group/other can modify the files (or create/delete files in the directory)
> 
> x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
> 
> _-_ _-_ nothing

3. For college_file above, the rw-r--r-- permissions entry decodes to:

r: the user that owns the file (user hacker) can read it

w: the user that owns the file (user hacker) can write to it

-: the user that owns the file (user hacker) cannot execute it

r: users in the group that owns the file (group hacker) can read it

-: users in the group that owns the file (group hacker) cannot write to it

-: users in the group that owns the file (group hacker) cannot execute it

r: all other users can read it

-: all other users cannot write to it

-: all other users cannot execute it

4. Now, let's look at the default permissions of /flag:

> hacker@dojo:~$ ls -l /flag
> 
> -r-------- 1 root root 53 Jul  4 04:47 /flag
> 
> hacker@dojo:~$

Here, there is only one bit set: the read permission for the owning user (in this case, root). Members of the owning group (the root group) and all other users have no access to the file.

One might wonder how the `chgrp` levels worked, if there is no group access to the file, well for those levels the permissions were set differently:

> hacker@dojo:~$ ls -l /flag
> 
> -r--r----- 1 root root 53 Jul  4 04:47 /flag
> 
> hacker@dojo:~$

The group had access! That is why chgrping the file enabled you to read the file.

5. Just like ownershipt, permissions can also be changed, using the command `chmod`, the basic usage is:

<img width="445" height="37" alt="Screenshot 2025-10-10 at 1 03 21 AM" src="https://github.com/user-attachments/assets/169fc9be-3360-4dd6-8b1c-fded4bb79ba1" />

One can specify the MODE in two ways: as a modification of the existing permissions mode, or as a completely new mode to overwrite the old one.

6. This level is about covering the former, modifying an existing mode.
7. `chmod` allows to tweak permissions in the mode format of `WHO+/-WHAT`  where WHO is user/group/other and WHAT is read/write/execute. For example, to add read access for the owning user, we would specify a mode of `u+r`.
8.  `w`rite and e`x`ecute access for the `g`roup and the `o`ther (or `a`ll the modes) are specified the same way. More examples:

<img width="464" height="210" alt="Screenshot 2025-10-10 at 1 08 08 AM" src="https://github.com/user-attachments/assets/ff285ce0-13d1-46c2-99e2-34db20b21f42" />

9. For this challenge --> `In this challenge, you must change the permissions of the /flag file to read it! Typically, you need to have write access to the file in order to change its permissions, but I have made the chmod command all-powerful for this level, and you can chmod anything you want even though you are the hacker user. This is an ultimate power. The /flag file is owned by root, and you can't change that, but you can make it readable. Go and solve this!`

## My solve
**Flag :** `pwn.college{8_gTsds23SitD_q9njiCayR9Wbx.QXzcjM1wCOwIzNzEzW}`

I ran `ls -l /flag` to check for the user(owner) of /flag, which was root obviously, then I ran `chmod o+r /flag`, which gave `other` users(which is the set that I lie in) permission to read the concerned file, then simply catted it out.

<img width="528" height="119" alt="Screenshot 2025-10-10 at 1 19 08 AM" src="https://github.com/user-attachments/assets/17accede-2b43-4177-a3e8-1a091ed571f9" />

## What I Learned
- Learned a lot about permissions here, how can they be changed for the user, or a group or other users and groups.
- A very helpful command `chmod`, helps change permissions for reading, writing and execution.

### References
None.

