# Listing Processes
### Key points
1. This challenge is about learning, listing the running processes.
2. Using the `ps` command. Depending on whom you ask, ps either stands for "process snapshot" or "process status", and it lists processes. By default, ps just lists the processes running in your terminal, which honestly isn't very useful:

<img width="396" height="140" alt="Screenshot 2025-10-07 at 12 08 22 AM" src="https://github.com/user-attachments/assets/b88ea06b-f194-4eca-9cd4-50be7c259ff1" />

In the above example, we have the shell (bash) and the ps process itself, and that's all that's running on that specific terminal.

We also see that each process has a numerical identifier (the Process ID, or PID), which is a number that uniquely identifies every running process in a Linux environment. We also see the terminal on which the commands are running (in this case, the designation pts/0), and the total amount of cpu time that the process has eaten up so far (since these processes are very undemanding, they have yet to eat up even 1 second!).

In the majority of cases, this is all that you'll see with a default ps. To make it useful, we need to pass a few arguments.

3. As ps is a very old utility, its usage is a bit of a mess. There are two ways to specify arguments, `"Standard" Syntax:` in this syntax, you can use -e to list "every" process and -f for a "full format" output, including arguments. These can be combined into a single argument -ef,`"BSD" Syntax:` in this syntax, you can use a to list processes for all users, x to list processes that aren't running in a terminal, and u for a "user-readable" output. These can be combined into a single argument aux.

4. These two methods, ps `-ef` and ps `aux` , result in slightly different, but cross-recognizable output, trying both in the terminal gave similar output, there are many commonalities between ps `-ef` and ps `aux`: both display the user (**USER column**), the **PID**, the **TTY**, the start time of the process (**STIME/START**), the total utilized CPU time (**TIME**), and the command (**CMD/COMMAND**). **ps -ef** additionally outputs the Parent Process ID (**PPID**), which is the **PID of the process that launched the one in question**, while ps aux **outputs the percentage of total system CPU and Memory that the process is utilizing**. Plus, there's a bunch of other stuff we won't get into right now.

5. Here, /challenge/run is renamed to some random filename, also can't `ls ` the /challenge directory, but it is launched so, one can find it in the running processes list, I am supposed to figure out the filename and relaunch it to get the flag.

> NOTE: Both `ps -ef` and `ps aux` truncate the command listing to the width of your terminal (which is why the examples above line up so nicely on the right side of the screen. If you can't read the whole path to the process, you might need to enlarge your terminal (or redirect the output somewhere to avoid this truncating behavior)! Alternatively, you can pass the w option twice (e.g., ps -efww or ps auxww) to disable the truncation. 

## My solve
**Flag :** `pwn.college{gK3pzNBNa3IH_EwbkY5D6oFBQxc.QX4MDO0wCOwIzNzEzW}`

I just ran `ps -ef`, which gave out all the running processes, one of them resembled /challenge/run, i relaunched that which gave out the flag, following is an image:

<img width="671" height="225" alt="Screenshot 2025-10-07 at 12 27 57 AM" src="https://github.com/user-attachments/assets/3667d505-e281-4204-a64d-8e7caa0ecc1e" />

It also says some interesting thing at the last.

## What I Learned
- Learned a lot about processes, commands to list processes, their internal arguments and various ways to use.
- Majorly about the ps command and its two arguments which join 2-3 arguments together, -ef and aux.

### References
No external references used for this solution.

