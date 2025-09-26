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
# Grepping for a needle in a haystack
## Key points
- The **grep** command searches for contents in a file one needs.
- Sometimes files that we cat out can be too big, grep is useful to find specified contents.
- It runs like: **hacker@dojo:~$ grep SEARCH_STRING /path/to/file**
- I was supposed to find my flag which was within a file with over 100 thousand lines of text, hint is given that all flags start from **pwn.college**
## My solve 
**Flag :** 'pwn.college{g0HZfqNx7Sv737N4GzP08d3rIT_.QX3EDO0wCOwIzNzEzW}'

I simply ran the _grep_ command with the argument **pwn.college /challenge/data.txt** because /challenge/data.txt is the file in which we have to search and the search string is _pwn.college_. Following is an image:

<img width="655" height="87" alt="Screenshot 2025-09-26 at 1 08 53 AM" src="https://github.com/user-attachments/assets/00eeed52-9c04-4c53-8523-abe014bf2f31" />

## What I Learned
- Learned about the new grep command and its use cases
- Learned about the format of the command in which it runs.]
### References
None.
# Comparing Files
## Key points 
- Eyeballing differneces between similar files can be tedious, and tricky, here is where the **diff** command becomes invaluable.
- The diff command points out the differnece between the two files that we give to it as arguments while running.
- Runs in the following format:

<img width="467" height="291" alt="Screenshot 2025-09-26 at 1 20 23 AM" src="https://github.com/user-attachments/assets/bf70d39b-b676-46e3-b174-64853bfe192c" />

- In the output it tells us in which line what has changed and if an extra line is added with some contents, something like:
 
<img width="467" height="209" alt="Screenshot 2025-09-26 at 1 23 27 AM" src="https://github.com/user-attachments/assets/1981f5c9-84d9-4a0d-b071-113214d145e1" />

- There are 2 files in **/challenge**, I have to use diff command to find the difference in them, in essence the flag.
- **/challenge/decoys_only.txt** contains 100 fake flags, **/challenge/decoys_and_real.txt** contains all 100 fake flags plus the one real flag.

## My Solve
**Flag :** 'pwn.college{4_5Rbp_9L-GBxPEBE4CE0AOam_0.01MwMDOxwCOwIzNzEzW}'

I simply used the ***diff*** command with two arguments the first and the second file belonging to /challenge and it gave me the flag, following is an image:

<img width="667" height="131" alt="Screenshot 2025-09-26 at 1 28 42 AM" src="https://github.com/user-attachments/assets/1af9f264-4bc4-4699-8167-b8c7de04c8d6" />

## What I Learned
- I learned about the new _diff_ command and its use case
- It quickly tells where and what is the differnce between 2 similar files.
- Ran the command to find my flag.
### References 
None.
# listing files
### Key points
- Their can be a lot of files in a single directory, and also other directories, to list them and to list their contents, a command called ***ls*** is used
- _ls_ will list all the files in all the directories we provide to it as arguments and from the current directory if no arguments are passed.
- It lists something like following:

<img width="467" height="238" alt="Screenshot 2025-09-26 at 1 35 45 AM" src="https://github.com/user-attachments/assets/3089118a-9c92-4350-a1d9-1a526d5b54da" />

## My solve
**Flag :** 'pwn.college{kLKlyI9SAX9USOY1FgI7MBO7bBV.QX4IDO0wCOwIzNzEzW}'

I just ran the ***ls*** command with /challenge as argument directory, then it listed all the files in that directory which were **22008-renamed-run-11057** and **DESCRIPTION.md**, the first one looked more like the _run_ file renamed, then I used the absolute path to invoke it by **/challenge/22008-renamed-run-11057**, then it gave me the flag, I could've also used cd to change to /challenge and then use ls which would've listed all files in the current directory, following is an image:

<img width="527" height="117" alt="Screenshot 2025-09-26 at 1 47 18 AM" src="https://github.com/user-attachments/assets/11e1cdd0-2073-428c-9e0f-68de12eb48c4" />

## What I Learned
- I learned about the ***ls*** command and how it can list all the files in a directory or the current directory if no argument is given.
### References 
SENSAI
# touching files
### Key points
- We can create files,by several ways, But by a simple comand called ***touch*** we can create a blank file.
- By touching it with touch command as:
  
  <img width="469" height="166" alt="Screenshot 2025-09-26 at 1 56 12 AM" src="https://github.com/user-attachments/assets/e5e0cc62-39ce-45f9-b875-26ca8c5173ff" />

- I had to create 2 files namely **pwn** and **college** in the /tmp directory.
  
## My solve
**Flag :** 'pwn.college{I0uQY1B-FHRrYjPWt9bZR7ZVwnj.QXwMDO0wCOwIzNzEzW}'

I just changed my directory to /tmp and then by the touch command, made two blank files pwn and college and then ran **/challenge/run** which gave me the flag, following is an image:

<img width="436" height="106" alt="Screenshot 2025-09-26 at 2 00 37 AM" src="https://github.com/user-attachments/assets/459f7055-0961-413f-ac1e-203cb890df0c" />

## What I learned
- I learned about the new ***touch*** command which makes empty files just by giving it file names/paths as arguments.
### References
None.
# removing files
### Key points
- Files can be deleted by simply using the ***rm*** command.
- Something like:

 <img width="428" height="205" alt="Screenshot 2025-09-26 at 2 06 40 AM" src="https://github.com/user-attachments/assets/ee52a48a-537c-459b-b4bb-a149d2b0d0f0" />

- I was supposed to delete a file using the rm command, the file is created in the home directory, after deleting i had to run /challenge/check which gave me the flag.
## My solve
**Flag :** 'pwn.college{QgQvCpl2UwoQWF-TOoHY3GKZ7jZ.QX2kDM1wCOwIzNzEzW}'

I just used the rm command with the argument _delete_me_ which deleted that file and then i ran /challenge/check, following is an image:  

<img width="466" height="82" alt="Screenshot 2025-09-26 at 2 10 28 AM" src="https://github.com/user-attachments/assets/60eb0ca5-12a9-45ca-88c4-d5b892d55d01" />

## What I Learned
- Learned about the new rm command which deletes files given as arguments.
### References 
None.
# moving files
### Key points
- one can move around files with the ***mv*** command, it moves the contents of one file to the other.
- somehting like:

 <img width="479" height="256" alt="Screenshot 2025-09-26 at 2 12 47 AM" src="https://github.com/user-attachments/assets/cc9c1f40-ecb7-4c40-8da8-b0ade53943ac" />

## My solve
**Flag :** 'pwn.college{g-qOy1F7JlL0ENStUMfmXpjsgdH.0VOxEzNxwCOwIzNzEzW}'

I just used the mv command gave it arguments as the flag file and the given file to which i had to move the flag file to, then ran **/challenge/check** which gave me the flag, following is an image:

<img width="594" height="156" alt="Screenshot 2025-09-26 at 2 17 15 AM" src="https://github.com/user-attachments/assets/9b45b856-0e67-49fe-b11e-efca50d2afed" />

## What I learned
- I learned about the new mv command which moves the contents of one file to the another file quite simply.
### References
None.
# Hidden Files
### Key Points
- ls doesnt list all the files by default, files that start with a **.** are not listed by ls, and in a few other contexts.
- To view them one has to invoke ls with the **-a**, as shown:


<img width="461" height="189" alt="Screenshot 2025-09-26 at 2 29 21 AM" src="https://github.com/user-attachments/assets/61b97ec2-0a97-40b1-b5b8-b3e6c6a421bd" />

- I was supposed to find the **.-prepended** file to get the flag.
## My solve
**Flag :** 'pwn.college{I9MR4nCVN2y4EOdru8uvOvYNg-n.QXwUDO0wCOwIzNzEzW}'

I just ran ls with **-a** which gave me all files, even the hidden ones, then i used the cat command with the argument as that file which contains my flag, following is an image: 

<img width="599" height="149" alt="Screenshot 2025-09-26 at 2 33 17 AM" src="https://github.com/user-attachments/assets/e6116ce9-dfe7-4284-80b3-1d3cb6f6025e" />

## What I Learned
- I learned about another way of using the ls command which is as ***ls -a*** which lists all the files even the **. prepeneded** ones, which are by default not listed by the ls command.
# References 
None.
# An Epic Filesystem Quest
### Key Points
- Here the flag is hidden, I had to use ls, cd, and cat commands wherever required to find the flag.
- Hint given:

 <img width="470" height="261" alt="Screenshot 2025-09-26 at 12 27 31 PM" src="https://github.com/user-attachments/assets/422ea192-ed93-47b8-a03b-124612bde5a1" />

## My solve
**Flag :**'It is: pwn.college{MrI69ylPcoF4fSIiLHDTEDQ4t3p.QX5IDO0wCOwIzNzEzW}'

 I started with the first hint cd'ing into the root directory then ls into it to check what files and directories are in it, then moved forward with the clues and cues provided, following are images for the same:
 
 <img width="612" height="232" alt="Screenshot 2025-09-26 at 12 31 29 PM" src="https://github.com/user-attachments/assets/1b2cec7f-45c3-443f-990c-496c916dd291" />

_In the second step itself where, we had to cat out a file which had a similar name to HINT or CLUE, it took me time to figure out what file to cat._

<img width="612" height="240" alt="Screenshot 2025-09-26 at 12 32 05 PM" src="https://github.com/user-attachments/assets/248fd3a3-fddf-420b-9308-c39c36302981" />

<img width="620" height="233" alt="Screenshot 2025-09-26 at 12 32 31 PM" src="https://github.com/user-attachments/assets/158cf847-5e7a-46a6-810f-a5f9068c2cdb" />

_It took some time to figure out for the trapped file that I have to cat it out from an absolute path through it's directory and not just cd into the given directory, after that also it wasn't really working, I restarted 3 times and then it got completed._

<img width="616" height="226" alt="Screenshot 2025-09-26 at 12 34 56 PM" src="https://github.com/user-attachments/assets/a46fddd4-da7d-41e2-bdc1-ac219fb92677" />

<img width="624" height="232" alt="Screenshot 2025-09-26 at 12 35 23 PM" src="https://github.com/user-attachments/assets/5d42dfd9-8fe3-4a44-a04e-dc3c493ae8bd" />

<img width="618" height="185" alt="Screenshot 2025-09-26 at 12 35 46 PM" src="https://github.com/user-attachments/assets/0abf718f-ef91-4224-9ef8-dfeb3cfb7a61" />


_Here i chose the wrong file to cat, which gave me something else, then catted the **TEASER** file, which gave me the next hint_

<img width="615" height="236" alt="Screenshot 2025-09-26 at 12 37 12 PM" src="https://github.com/user-attachments/assets/22eef49e-d902-4f14-999f-3e47a1cb27d5" />

<img width="618" height="231" alt="Screenshot 2025-09-26 at 12 37 46 PM" src="https://github.com/user-attachments/assets/2a3bf130-1336-4a5b-936f-1e100f612331" />

## What I Learned
- This really felt like some application of what I'd learned, paving my way through the files and directories to find the flag was an interesting task.
- I learned about _delayed_ and _trapped_ files.
### References 
SENSAI, pwn.college discord.

PS: Didn't really get any help from both of those sources, had to figure it out myself by trying over and over agin.
# Making directories
### Key points
- We learned about making files by the touch command, here have a command ***mkdir*** to make directories
- I had to make a **/tmp/pwn** directory and then a **college** file in it.
## My solve
**Flag :** 'pwn.college{oqXiEb0onr8muQ3KW8dOD03EcMN.QXxMDO0wCOwIzNzEzW}'

I cd'd into the /tmp directory adn then did mkdir pwn which made the pwn directory in it then cd'd into pwn then by touch  command made the college file, following is an image for it:

<img width="613" height="232" alt="Screenshot 2025-09-26 at 12 53 02 PM" src="https://github.com/user-attachments/assets/273d78bf-6d13-483b-aaf6-37cb71f45523" />

## What I Learned
- Learned about the new command ***mkdir*** which makes directories, if desired directory names are given as arguments.
- Used the mkdir and touch command simultaneously to make a directory and then a file in it.
###  References
None.

# Finding files
### Key Points
- 

