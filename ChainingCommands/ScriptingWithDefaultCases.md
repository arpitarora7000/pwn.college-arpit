# Scripting with default cases
### Key points
1. This challenge is about `else`, else clause executes when the condition for `if` is false.

 <img width="452" height="164" alt="Screenshot 2025-10-10 at 10 16 10 PM" src="https://github.com/user-attachments/assets/902cc62c-3cae-4990-b7c4-692a8dd526f5" />

Note that the else doesn't have a condition --- it catches everything that didn't match previously. It also doesn't have a then statement. Finally, the fi goes after the else block to denote the end of the whole complex statement! It is also optional: you didn't have it in the previous level, and you only need it if the logic you're trying to achieve demands it.

2. Here's a practical example:

> if [ "$1" == "start" ]
> 
> then
> 
>    echo "Starting the service..."
> 
> else
> 
>   echo "Unknown command. Use 'start' to begin."
> 
> fi

3. For this challenge --> For this challenge, write a script at /home/hacker/solve.sh that:

 - Takes one argument
 - If the argument is "pwn", output "college"
 - For any other input, output "nope"

 Example:

> hacker@dojo:~$ bash /home/hacker/solve.sh pwn
> 
> college
> hacker@dojo:~$ bash /home/hacker/solve.sh hack
> 
> nope
> 
> hacker@dojo:~$ bash /home/hacker/solve.sh anything
> 
> nope
> 
> hacker@dojo:~$

Once your script works correctly, run /challenge/run to get your flag!


## My solve
**Flag :** `pwn.college{cubJOYEBvjMZYa0SN1okuu4PeeM.01NzMDOxwCOwIzNzEzW}`

I just wrote the following to get the flag:

<img width="583" height="221" alt="Screenshot 2025-10-10 at 10 25 51 PM" src="https://github.com/user-attachments/assets/d4dba365-42c3-440b-9526-562fabb68183" />

## What I Learned
- Learned about the `else` statment, corresponding to the given `if` statement.
- Learned deeply about its syntax.

### References
None.
 
