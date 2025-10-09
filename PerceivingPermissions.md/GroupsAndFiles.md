# Groups and Files
### Key points
1. Sharing is caring, and sharing is built into Linux's design. Files have both an owning user and group. A group can have multiple users in it, and a user can be a member of multiple groups
2. One can check what groups you are part of with the id command:

> hacker@dojo:~$ id
> 
> uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
> 
> hacker@dojo:~$

3. Here, hacker user is only in the hacker group, the most common use-case for groups is to control access to different system resources.
4. If I'd done the same thing in practice mode it'd also show the group 27(sudo), other than 1000(hacker).
5. A typical main user of a typical Linux desktop has a lot of groups, the following is for `zardus`:

> zardus@yourcomputer:~$ id
> 
> uid=1000(zardus) gid=1000(zardus) groups=1000(zardus),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),100(users),106(netdev),114(bluetooth),117(lpadmin),120(scanner),995(docker)
> 
> zardus@yourcomputer:~$

All these groups give Zardus the ability to read CDs and floppy disks (who does that anymore?), administer the system, play music, draw to the video monitor, use bluetooth, and so on. Often, this access control happens via group ownership on the filesystem! For example, graphical output can be done via the special `/dev/fb0` file: 

> zardus@yourcomputer:~$ ls -l /dev/fb0
> 
> crw-rw---- 1 root video 29, 0 Jun 30 23:42 /dev/fb0
> 
> zardus@yourcomputer:~$

This file is a special device file (type c means it is a "character device"), and interacting with it results in changes to the display output (rather than changes to disk storage, as for a normal file!). Zardus' user account on his machine can interact with it because the file has a group ownership of video, and Zardus is a member of the video group.

6. Now, for the `/flag` file, if we try to cat it out, it says _permissions denied_, because the hacker user is neither the root, nor the part of root group, but there is a command called `chgrp`, which helps to change group ownership.
7. Unless you have write access to the file and membership in the new group, this typically requires root access, so let's check it out as root:

> root@dojo:~# mkdir pwn_directory
> 
> root@dojo:~# touch college_file
> 
> root@dojo:~# ls -l
> 
> total 4
> 
> -rw-r--r-- 1 root root    0 May 22 13:42 college_file
> 
> drwxr-xr-x 2 root root 4096 May 22 13:42 pwn_directory
> 
> root@dojo:~# chgrp hacker college_file
> 
> root@dojo:~# ls -l
> 
> total 4
> 
> -rw-r--r-- 1 root hacker    0 May 22 13:42 college_file
> 
> drwxr-xr-x 2 root root   4096 May 22 13:42 pwn_directory
> 
> root@dojo:~#

8. In this challenge, the `chgrp` command is usable by the hacker, and also, the flag is readable by whatever group owns it, I have to change the group read out the file,

## My solve
**Flag :** `pwn.college{sfAlA6B7DSQMy3U2GQjjYbC5Dzl.QXxcjM1wCOwIzNzEzW}`

I just ran `chgrp hacker /flag` then catted it out to get the flag.

<img width="575" height="256" alt="Screenshot 2025-10-10 at 12 37 07 AM" src="https://github.com/user-attachments/assets/20b26d07-4fc6-486c-a226-fdf676bf7671" />

## What I Learned
- Learned about the new command `chgrp`, typically usable by root, and helps change group ownership.

###  References
No external references used.
