# cat: not the pet but the command!

After thoroughly reading the statement attached to the problem I got out the following key points
### Key points
- cat is most often used for reading out files.
- cat can concatenate multiple files if given multiple arguments.
- if no arguments are given to cat, it'll read from the terminal
## My solve 
**Flag :** 'pwn.college{0Mxrr8yMySefW7flgj3opNV5NWA.QXxcTN0wCOwIzNzEzW}'

I simply had to give **flag**as an argument to the **cat** command and it gave out the flag.

Image:

<img width="495" height="75" alt="Screenshot 2025-09-25 at 12 56 14 AM" src="https://github.com/user-attachments/assets/fb040bfa-3d7f-4cd5-b79a-778ce1ea28a2" />

## What I Learned
- I learned about the cat command, how does it work, the way it takes up arguments.
### References 
None.
# catting absolute paths
## Key Points
- We can specify absolute paths as arguments to the **cat** command.
- I can read it with cat at its absolute path ***/flag***.
- **/flag** is where the flag always lives, but cant typically access that file directly.
## My solve
**Flag :** 'pwn.college{09M_OFmFPFPSyUtxedcelJ_Ix94.QX5ETO0wCOwIzNzEzW}'


I simply ran the cat command with the argument as the absolute path of flag, and it read out the flag. Following is an image.

<img width="442" height="85" alt="Screenshot 2025-09-26 at 12 21 49 AM" src="https://github.com/user-attachments/assets/9cb9f0a8-c733-4c69-b553-7f17abeb2dfd" />

## What I Learned
- I learned that absolute paths can be arguments for the **cat** command.
### References 
None.
# more catting practice
### Problem statement
You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with cd, so no cat flag for you. You must retrieve the flag by absolute path, wherever it is.
## Key points
- We cannot use cd to change directories, so will have to use absolute path for the file in which the flag is stored
- It is mentioned that flag is in some crazy directory, image from the terminal:

<img width="662" height="62" alt="Screenshot 2025-09-26 at 12 29 45 AM" src="https://github.com/user-attachments/assets/1fc0bc42-837b-40c0-9421-c21f72e8fe7f" />

So the flag is in the shown file 
- I was simply supposed to run cat with the absolute path given.
## My solve 
**Flag :** 'pwn.college{ImzXUEEVZvIihLJ5xFBzXq3jJEj.QXwITO0wCOwIzNzEzW}'
I simply ran the cat command for the file given as argument and it gave me the flag, Image:

<img width="603" height="61" alt="Screenshot 2025-09-26 at 12 31 36 AM" src="https://github.com/user-attachments/assets/c8ad91a4-e837-445a-a986-d2d709ee3bbf" />

## What I Learned
It was the same as the previous challenge just a different file in which the flag was stored, i had to run the cat command with it.
### References
None.


