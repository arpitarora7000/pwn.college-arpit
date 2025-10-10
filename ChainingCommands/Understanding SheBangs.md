# Understanding SheBangs
### Key points

Some theory:


> You're well on your way to your new life as a shell scripter! However, so far, your shellscripts can only be launched from the shell. Things worked great in the previous level (because you were invoking your script from the bash shell), but they won't work if your script was being invoked by, say, a program written in Python (or any other language).
>
> When a program is invoked in Linux, the Linux kernel first inspects the file to determine how it should be run. This does NOT use the extension (which is why you don't have to name your shell scripts with a .sh extension, or your Python scripts with a .py extension, or so on). Rather, Linux looks at the first few bytes of the file for this information.

1. There are a bunch of different types of programs, but if the program file starts with the characters #! (often termed a "shebang"), Linux treats the file as an interpreted program, and the contents of the rest of the line as the path to the interpreter. It then invokes the interpreter with the path to the program file as its only argument.
2. Consider this shell script:

<img width="290" height="102" alt="Screenshot 2025-10-10 at 8 32 58 PM" src="https://github.com/user-attachments/assets/d0cdbe7c-e25b-4d57-96eb-520996da0696" />

this can be executed as:

<img width="397" height="117" alt="Screenshot 2025-10-10 at 8 33 24 PM" src="https://github.com/user-attachments/assets/ef248817-18ab-4bdc-b70d-5af059f2c555" />

3. When ./script.sh was executed, Linux opened the file, read the first line, extracted /bin/bash as the interpreter, and executed /bin/bash ./script.sh to launch the script!

Note, the shebang line must be the VERY FIRST line of the file - no blank lines or spaces before it
4. For this challenge --> `For this challenge, create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet". Remember to make it executable, then run /challenge/run to verify your script works correctly!`

<img width="501" height="236" alt="Screenshot 2025-10-10 at 8 34 56 PM" src="https://github.com/user-attachments/assets/3002d98d-1d48-455f-b8b2-1497d73e044a" />

## My solve
**Flag :** `pwn.college{gSuA0hF2CByQTP97KcEjofrGu0_.0VOzMDOxwCOwIzNzEzW}`

Just simply wrote to the file solve.sh, `#!/bin/bash`, before the given command, then changed permissions to make it executable, then ran `/challenge/run`.

<img width="480" height="237" alt="Screenshot 2025-10-10 at 8 36 33 PM" src="https://github.com/user-attachments/assets/af43d003-f40a-48c3-808e-4f178964b67f" />

## What I Learned
- Learned about filetypes, their extensions, when are they important and when are they not and why not.
- Learned about shebangs, any file starting with `#!` is a shebang.

### References
No external references.
 
