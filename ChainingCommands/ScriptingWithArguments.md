# Scripting with Arguments
### Key points
1. We've already learned about creating shell scripts, but they can do much more, which is to accept arguments, which make them much more powerful.
2. This might look like:

<img width="458" height="42" alt="Screenshot 2025-10-10 at 8 40 19 PM" src="https://github.com/user-attachments/assets/8953b54c-80dd-478a-a460-63121b229330" />

<img width="494" height="512" alt="Screenshot 2025-10-10 at 8 44 12 PM" src="https://github.com/user-attachments/assets/aa267f30-0fae-4e82-97f6-e0fba55c0bcd" />

3. For this challenge --> For this challenge, you need to write a script at /home/hacker/solve.sh that:

 1.Takes two arguments

 2.Outputs them in REVERSE order (second argument first, then the first argument)

 For example:

 > hacker@dojo:~$ bash /home/hacker/solve.sh pwn college
 > 
 > college pwn
 > 
 > hacker@dojo:~$

 Once your script works correctly, run /challenge/run to get your flag!


## My solve
**Flag :** `pwn.college{Uzm4vWfZo9Ik0aqEP5bJj0W-uW_.0VNzMDOxwCOwIzNzEzW}`

I wrote to the file `echo "$2 $1"`, then saved it then ran `/challenge/run`, to get the flag.

<img width="476" height="140" alt="Screenshot 2025-10-10 at 8 51 49 PM" src="https://github.com/user-attachments/assets/1e794a1b-1e59-441e-93d6-3628fda93e56" />

## What I Learned
- Learned about a fascinating concept, which is _shell scripts accepting arguments_.

### References
None.
