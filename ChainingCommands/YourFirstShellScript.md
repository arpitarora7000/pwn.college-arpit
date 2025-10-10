# Your first shell script
### Key points
1. If a lot of commands are required to be run in the commandline, they can be stored in a file, and run them by executing the file, the file is called _shell script_.
2. Consider the semicolon technique:

<img width="443" height="82" alt="Screenshot 2025-10-10 at 7 25 33 PM" src="https://github.com/user-attachments/assets/6c231a1f-e8af-4f5e-9d67-2b53e599e5a1" />

<img width="487" height="595" alt="Screenshot 2025-10-10 at 7 26 53 PM" src="https://github.com/user-attachments/assets/e421ca65-e2fb-4b94-a5f6-59040a5db952" />

3. For this challenge --> `Now, it's your turn! Same as last level, run /challenge/pwn and then /challenge/college, but this time in a shell script called x.sh, then run it with bash!`

> NOTE: We haven't yet talked about Linux's amazing array of competent command line file editors. For now, feel free to use the Text Editor application in Desktop mode (Applications->Accessories->Text Editor) or the default editor in the VSCode Workspace!

## My solve
**Flag :** `pwn.college{YjU1H-jdU-9OY1gQGyttqdrroU3.QXxcDO0wCOwIzNzEzW}`

I wasn't able to figure out, where to make the file and then how to execute it, I took help of AI, which made me learn about the `nano` command, and different options in it, which can help writing to a file, then I used it and then wrote both the given commands there, then used bash to get the flag.

<img width="592" height="134" alt="Screenshot 2025-10-10 at 7 57 30 PM" src="https://github.com/user-attachments/assets/648a7330-0dac-4d78-a95e-2f1d420fb7ed" />

## What I Learned
- Learned about shell scripts, how if a lot of commands are to be run, we can store them in a file then execute the file using the `bash` command to run all the commands within it.
- I learned about creating a file, with the extension `.sh`, by the `nano` command, with help of AI.
- Also using cat in the format `cat > filename.sh`, helps to write to the file, SENSAI, told me that. 

### References
SENSAI.
