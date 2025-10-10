# Executable Shell Scripts
### Key points
1. It turns out that you can avoid the need to manually invoke `bash`.
2. If the file is executable, we can invoke it simply by it's  relative or absolute path.
3. For this challenge --> `Try that here! Make a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash!`

## My solve
**Flag :** `pwn.college{cEFBgSK3TElMhGdgAbqduif55Ot.QX0cjM1wCOwIzNzEzW}`

I just wrote to the script `script.sh`, the given command, then used `chmod u+x script.sh`, to make it executable, then executed the file without using `bash`.

<img width="574" height="88" alt="Screenshot 2025-10-10 at 8 22 56 PM" src="https://github.com/user-attachments/assets/8b9e6250-8abb-42c8-8305-e20aeb0ded61" />

<img width="472" height="72" alt="Screenshot 2025-10-10 at 8 23 03 PM" src="https://github.com/user-attachments/assets/52a61c29-08fa-43e3-816f-c15a6ea3fde6" />

## What I Learned
- Learned about how shell scripts can be executed without using bash.

### References
None.
