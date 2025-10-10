# Redirecting Script Output
### Key Points
1. We've used piping by `|`, but only for outputs of one command redirected to input of other command, but what if it is required to send output of multiple programs to one command.
2. We can use redirecting output from script, to a particular command, which solves the problem.
3. Example:
 
<img width="449" height="208" alt="Screenshot 2025-10-10 at 8 05 33 PM" src="https://github.com/user-attachments/assets/382f7cb1-dc92-4db2-8cfd-cfbec3938d6c" />

4. All of the various redirection methods work: > for stdout, 2> for stderr, < for stdin, >> and 2>> for append-mode redirection, >& for redirecting to other file descriptors, and | for piping to another command.
5. For this challenge --> `In this level, we will practice piping (|) from your script to another program. Like before, you need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command!`

## My solve
**Flag :** `pwn.college{ocZJ04j-DFmPNDkMN4l_ODGtp02.QX4ETO0wCOwIzNzEzW}`

This time I used `cat > script.sh`, and wrote to the file, both the commands, then piped ouput to `/challenge/solve`.

<img width="605" height="141" alt="Screenshot 2025-10-10 at 8 09 23 PM" src="https://github.com/user-attachments/assets/0871281b-2046-4f8a-8792-a42ea912edb9" />

## What I Learned
- Learned that if multiple oprogram outputs are to be redirected to one command, one can make use of shell scripts.
- Simply by making a shell script, can use bash to pipe to another command.

### References
None.
