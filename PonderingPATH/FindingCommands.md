# Finding Commands
### Problem statement


When you type the name of a command, something inside one of the many directories listed in your `$PATH` variable is what actually gets executed (of course, unless the command is a builtin!). But which file, precisely? You can find out with the aptly-named `which` command:

<img width="371" height="136" alt="Screenshot 2025-10-11 at 12 02 41 AM" src="https://github.com/user-attachments/assets/cfdeff2f-fcef-4db1-adab-307a5b710bd4" />

Mirroring what the shell does when searching for commands, `which` looks at each directory in `$PATH` in order and prints the first file it finds whose name matches the argument you passed.

In this challenge, we added a `win` command somewhere in your `$PATH`, but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find `win` (with the `which` command), and cat the flag out of that directory!

## My solve
**Flag :** `pwn.college{4tmACxVFONkA0bIFEK9SAnvzNKm.01NzEzNxwCOwIzNzEzW}`

I wrote `which win`, which gave out the file for win, then I cd'd into that particular directory and ran `cat flag`, to get the flag.

<img width="586" height="208" alt="Screenshot 2025-10-11 at 12 09 31 AM" src="https://github.com/user-attachments/assets/219ba93f-8bb0-4ea5-9884-5696abc9f461" />

## What I Learned
- Learned about the new `which` command which gives the file for the particular command that we give to it as argument.

### References
None.
