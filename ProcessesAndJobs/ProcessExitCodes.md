# Process Exit Codes
### Key points
1. Every shell command, including every program and every builtin, exits with an exit code when it finishes running and terminates. This can be used by the shell, or the user of the shell to check if the process succeeded in its functionality (this determination, of course, depends on what the process is supposed to do in the first place).
2. We can access the exit code of the most recently-terminated command using the special `?` variable (don't forget to prepend it with `$` to read its value!):

> hacker@dojo:~$ touch test-file
> 
> hacker@dojo:~$ echo $?
> 
> 0
> 
> hacker@dojo:~$ touch /test-file
> 
> touch: cannot touch '/test-file': Permission denied
> 
> hacker@dojo:~$ echo $?
> 
> 1
> 
> hacker@dojo:~$

3. As is there, commands that succeed typically return 0 and commands that fail typically return a non-zero value, most commonly 1 but sometimes an error code that identifies a specific failure code.

4. In this challenge, you must retrieve the exit code returned by `/challenge/get-code` and then run `/challenge/submit-code` with that error code as an argument.

## My solve
**Flag :** `pwn.college{goZmpr6tc-WkL4nM26g_7T9jn-p.QX5YDO1wCOwIzNzEzW}`

I just ran the given command and used `echo $?` to get it's exit code, then ran the other command with the exit code of the first command as an argument, which gave out the flag.

<img width="562" height="164" alt="Screenshot 2025-10-08 at 1 33 25 AM" src="https://github.com/user-attachments/assets/94dd2038-3151-4385-b234-9349c10763e3" />

## What I Learned
- Learned about the new and interesting concept of error codes, commands succeding generally giving out 0 and 1, if not and some error code for error. learned about how to get the exit code by using the echo command as `echo $?`.

### References
No external references for this challenge.
