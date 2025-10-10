# Setting PATH
### Key points
1. We can use PATH to store new program directories, PATH stores a list of directories to find commands in and, for commands in nonstandard places, we must typically execute them via their path:

> hacker@dojo:~$ ls /home/hacker/scripts
> 
> goodscript	badscript	okayscript
> 
> hacker@dojo:~$ goodscript
> 
> bash: goodscript: command not found
> 
> hacker@dojo:~$ /home/hacker/scripts/goodscript
> 
> YEAH! This is the best script!
> 
> hacker@dojo:~$

2. If you maintain useful scripts that you want to be able to launch by bare name, this is annoying. However, by adding directories to or replacing directories in this list, you can expose these programs to be launched using their bare name! For example:

<img width="431" height="107" alt="Screenshot 2025-10-10 at 11 54 22 PM" src="https://github.com/user-attachments/assets/0a7f2f40-92ec-40ba-8f9d-e2a6b2ccca01" />

3. For this challenge --> `Let's practice. This level's /challenge/run will run the win command via its bare name, but this command exists in the /challenge/more_commands/ directory, which is not initially in the PATH. The win command is the only thing that /challenge/run needs, so you can just overwrite PATH with that one directory.`

## My solve
**Flag :** `pwn.college{sqCLXB-OxwgzAslc9OW6XTNNhjl.QX1cjM1wCOwIzNzEzW}`

I just ran `PATH=/challenge/more_commands/`, which added this directory in the list that PATH stores to find commands, then ran `/challenge/run`, which gave out the flag.

<img width="485" height="146" alt="Screenshot 2025-10-10 at 11 57 47 PM" src="https://github.com/user-attachments/assets/4b2e4478-ea84-4da7-ad66-044c3a5b72f1" />

## What I Learned
- Learned about the list of directories that PATH stores, to find commands in, and how we can add our own directory in it, containing programs.

### References
No external references used.
