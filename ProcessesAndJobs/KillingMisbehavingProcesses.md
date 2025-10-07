# Killing Misbehaving Processes
### Key Points
1. Sometimes, misbehaving processes can interfere with work, so need to be killed.
2. In this challenge, there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge) /challenge/run wants to write my flag. I need to kill this process.
3. General workflow should be to check which processes are running, then find the decoy process, `/challenge/decoy`, then kill it and run /challenge/run to get the flag.
 
> NOTE: You might see a few decoy flags show up even after killing the decoy process. This happens because Linux pipes are buffered: conceptually, they have a sort of length through which data flows, and you might kill the decoy process while data is in the pipe. That data, having already entered the pipe, will proceed to the other end (your cat). If you wait a second, you'll see the decoys stop, and then you can /challenge/run and win!
 
## My solve
**Flag :** `pwn.college{oMiJMISJMi-9RCo4E1FteYuovBb.0FNzMDOxwCOwIzNzEzW}`

I ran `ps -efww` to see all the running processes, then killed the one with PID  142, which was the /challenge/decoy, then I ran /challenge/run it said _Sending the flag to /tmp/flag_fifo!_ it took some time , used the `^C` to stop it, and ran `cat /tmp/flag_fifo` which gave out over 50 flags, obviously all decoy except one, but as was mentioned they're the leftovers from the `/challenge/decoy` I used `^C` again to stop `cat /tmp/flag_fifo`, then I ran /challenge/run and it again said what It said earlier but didn't take time, then I catted out the fifo file again which gave out the real flag, following are some images:

<img width="624" height="602" alt="Screenshot 2025-10-07 at 4 45 08 PM" src="https://github.com/user-attachments/assets/8f433109-aa81-4831-ab43-e317b8f26e10" />

A lot more flags just like that, then:

<img width="537" height="59" alt="Screenshot 2025-10-07 at 4 47 39 PM" src="https://github.com/user-attachments/assets/21fde7eb-78ab-4926-b0f9-949ce534ead7" />


## What I Learned
- Learned about the new application of killing misbehaving processes.
- 

### References
No external references.
