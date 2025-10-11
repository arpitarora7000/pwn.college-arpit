# Adding Commands
### Problem statement

Previously, the win command that /challenge/run executed was stored in /challenge/more_commands. This time, win does not exist! Recall the final level of Chaining Commands, and make a shell script called win, add its location to the PATH, and enable /challenge/run to find it!

> Hint: /challenge/run runs as root and will call win. Thus, win can simply cat the flag file. Again, the win command is the only thing that /challenge/run needs, so you can just overwrite PATH with that one directory. But remember, if you do that, your win command won't be able to find cat.

You have three options to avoid that:

1. Figure out where the cat program is on the filesystem. It must be in a directory that lives in the PATH variable, so you can print the variable out (refer to Shell Variables to remember how!), and go through the directories in it (recall that the different entries are separated by :), find which one has cat in it, and invoke cat by its absolute path.
2. Set a PATH that has the old directories plus a new entry for wherever you create win.
3. Use read (again, refer to Shell Variables) to read /flag. Since read is a builtin functionality of bash, it is unaffected by PATH shenanigans.

Here I went with the first option to avoid that problem.

## My solve
**Flag :** `pwn.college{snRrJYTu0vmIDALRCOKu41uy2du.QX2cjM1wCOwIzNzEzW}`

I used `which cat`, to find absolute path of cat and then use it in the shell script to cat out `/flag`, which would obviously avoid the problem of `PATH`, getting overwritten, and not being able to find cat.

<img width="444" height="95" alt="Screenshot 2025-10-11 at 3 24 36 PM" src="https://github.com/user-attachments/assets/fdafc217-df7d-40fc-b18d-7b4b4b88d09c" />

<img width="556" height="169" alt="Screenshot 2025-10-11 at 3 24 51 PM" src="https://github.com/user-attachments/assets/1e14f5e4-dc8c-47af-b386-5a7f12b01f0b" />

## What I Learned
- I combined knowledge of variables, shell scripts and playing with the path variable, understood about the overwriting PATH variable, learned about 3 different ways to avoid that, used the one with finding the absolute path of the command that we needed.

### References
SENSAI
