# Translating Characters
### Key Points
1. One purpose of piping data is to _modify_ it, a command is `tr` which translates characters it receives over standard input and prints them to standard output.
2. In its most basic usage, tr translates the character provided in its first argument to the character provided in its second argument:

<img width="435" height="84" alt="Screenshot 2025-10-02 at 7 36 46 PM" src="https://github.com/user-attachments/assets/569e988f-6fae-4765-8b52-e48ec5e87efb" />

3. It can also handle multiple characters, with the characters in different positions of the first argument replaced with associated characters in the second argument.

<img width="425" height="79" alt="Screenshot 2025-10-02 at 7 42 20 PM" src="https://github.com/user-attachments/assets/1c9eac6d-3099-458d-a940-7d0853a31043" />

4. Here on invoking `/challenge/run`, I'll get a flag with all lower case characters turned to upper case and vice versa, I have to use the `tr` command to get the real flag.
## My Solve
**Flag :** `pwn.college{U8SW5gXj3okdc_RM1LwZaOwuKs6.01MxEzNxwCOwIzNzEzW}`

I ran /challenge/run, and got the case-swapped flag, then after trying a few times, not being able to figure out, what to do, I wrote `man tr`, which openend the manual for the **tr** command, I found out how one can create different sets of characters as arguments, like for [] 
