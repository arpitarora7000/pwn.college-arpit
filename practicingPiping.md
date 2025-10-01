> This is a proem based on the theory given in the module before challenges.

> The technology goes much deeper than, some commands putting out data ion the terminal, the mechanisms behind the handling of input and output on the commandline contribute to the commandline's power.

> This module is about _input_ and _output_ _redirection_. Every process in linux has three initial, standard channels of communication:
>
> Standard _Input_ is the channel through which the process takes input. For example, your shell uses Standard Input to read the commands that you input.
>
> Standard _Output_ is the channel through which processes output normal data, such as the flag when it is printed to you in previous challenges or the output of utilities such as ls.
>
>  Standard _Error_ is the channel through which processes output error details. For example, if you mistype a command, the shell will output, over standard error, that this command does not exist.

> Frequently used short forms: _stdin, stdout, stderr_

> This module will teach one how to redirect, chain, block, and otherwise mess with these channels.

# Redirecting output
### Key points
1. Use **>** to redirect std
out to files.
2. Illustration:

<img width="476" height="41" alt="Screenshot 2025-10-01 at 10 05 18 AM" src="https://github.com/user-attachments/assets/8302f7ad-a78e-4668-a256-f119f4db80fb" />

This will redircet the output of _echo hi_ to the file _asdf_.

<img width="483" height="77" alt="Screenshot 2025-10-01 at 10 06 53 AM" src="https://github.com/user-attachments/assets/46a91855-ff8b-4f7c-a8a0-57892523c98b" />

3. In this challenge, I am supposed to write **PWN**  to the file name **COLLEGE**, using output redirection.
## My solve
**Flag :** 'pwn.college{UshSXKcK00PmHFlmKYM2P1FyM6p-QX0YTN0wC0wIzNzEzW}'

I just ran the _echo_ command with the argument PWN, and redirected the output to the COLLEGE file, following is an image for it:

<img width="574" height="112" alt="Screenshot 2025-09-28 at 5 36 38 PM" src="https://github.com/user-attachments/assets/3fd25619-16ae-4d85-8a13-dfacadd65f39" />

## What I Learned
- Learned about the use of the new **>** character in the terminal, which is redirection of _stdout_ to files.
### References
No external references.
# Redirecting more Output
### Key points
1. One can redirect output of any command, here **/challenge/run** will give the flag, but only if it's output is redirected to the file _myflag_.
2. One could notice that /challenge/run prints to the terminal, despite redirecting stdout, that's because it communicates its instructions and feedback over standard error, and only prints the flag over standard output, and only the standard output is redirected.
## My Solve
**Flag :** 'pwn.college{QipQpvm-Yrqoxc0C6nTdd98EQZc…QX1YTN0wC0wIzNzEzW}'

I just redirected outout of /challenge/run to the myflag file, and catted it out which gave out the flag, following are images: 


<img width="587" height="223" alt="Screenshot 2025-09-28 at 5 39 57 PM" src="https://github.com/user-attachments/assets/b3be03f5-f37e-4ad6-9c2b-809496a7ef37" />

<img width="581" height="203" alt="Screenshot 2025-09-28 at 5 40 22 PM" src="https://github.com/user-attachments/assets/d8eff5e7-1ff7-4fc6-aac6-a08ac19d61c1" />


## What I Learned
- Redirected more output, learned how redirecting output of a command, doesn't affect if it prints or not in the terminal, because it communicates its feedback and instructions over _stderr_.
### References
None.
# Appending output
### Key Points
1. **>** will create a new output file every time, deleting the old contents, if we need to append the output in the same file over and over again, without letting the data getting lost, one needs to redirect some other way.
2. One can redirect input in append mode using >> instead of >, as so:

 
 <img width="445" height="158" alt="Screenshot 2025-10-01 at 10 28 55 AM" src="https://github.com/user-attachments/assets/4d8f3ff2-6763-4daa-92bb-4333a5e90229" />

3. Here I am supposed to  redirect the output of /challenge/run(this gives out the second half of the flag) to the ~/the-flag(this contains the first half of the flag), in append mode so that the first half doesn't get overwritten, if done in truncation mode with **>** it'll overwrite the first half.
## My Solve
**Flag :** 'pwn.college{ohKckBLhgpzitShDLahUKBp60nZ.QX3YTN0wC0wIzNzEzW}'

I just simply redirected output of **/challenge/run** to **~/the-flag** using **>>**, then ran cat command with the input ~/the-flag, which gave out the flag, both the halves.

<img width="587" height="217" alt="Screenshot 2025-09-28 at 5 55 21 PM" src="https://github.com/user-attachments/assets/355de471-9f8c-4d8f-b06f-ac1ee54192c5" />

<img width="592" height="170" alt="Screenshot 2025-09-28 at 5 56 17 PM" src="https://github.com/user-attachments/assets/0ea00627-17f4-44b5-a2d7-33aba472aefe" />

<img width="559" height="182" alt="Screenshot 2025-10-01 at 10 37 27 AM" src="https://github.com/user-attachments/assets/69b6457f-9b33-41de-b621-32dd3d8f4cbb" />

## What I Learned

- Learned about the use of >> in the terminal, which is to redirect output in append mode.
 
### References

No references other the in - challenge hints.

# Redirecting Errors
### Key Points
1. Just like output, we can also redirect error channel of commands.
2. A File Descriptor (FD) is a number that describes a communication   channel in Linux, we've already been using these, FD 0: Standard Input,
FD 1: Standard Output, FD 2: Standard Error.
3. When one redirects process communication, does it by FD number, though some FD numbers are implicit. For example, a > without a number implies 1>, which redirects FD 1 (Standard Output). Thus, the following two commands are equivalent:


<img width="460" height="57" alt="Screenshot 2025-10-01 at 10 53 08 AM" src="https://github.com/user-attachments/assets/e5db82b4-2f96-4788-ae35-79fc96d6e181" />


4. If we have a command, that might produce data via standard error (such as /challenge/run), you can do:

<img width="479" height="39" alt="Screenshot 2025-10-01 at 10 56 04 AM" src="https://github.com/user-attachments/assets/1d873872-f05c-4105-a1dd-139caf67c906" />

That will redirect standard error (FD 2) to the errors.log file.
5. Furthermore, we can redirect multiple file descriptors at the same time! For example:

> hacker@dojo:~$ some_command 1> output.log 2> errors.log

That command will redirect output to output.log and errors to errors.log.
6. Here I am supposed to redirect output of /challenge/run to myflag and the _errors_ for us, instructions to the instructions file.
## My solve
**Flag :** 'pwn.college{ohKckBLhgpzitShDLahUKBp60nZ.QX3YTN0wC0wIzNzEzW}'
I just simply, redirected both stout and sterr at the same time using respective file descriptors, to the respective files, and then catted out the myflag file, to get the flag.

<img width="558" height="122" alt="Screenshot 2025-09-28 at 6 00 09 PM" src="https://github.com/user-attachments/assets/02754620-3dae-496c-85f6-5e9d71f97466" />

### What I Learned

- Learned about the file discriptor numbers, how they can be  useful for redirecting all the communication channels.
- Learned how redirection can be done to multiple files at once, using FD numbers.

### References
None.

# Redirecting Input

### Key Points
1. Redirecting input **to** programs requires the use of **<**

  
<img width="464" height="134" alt="Screenshot 2025-10-01 at 11 10 06 AM" src="https://github.com/user-attachments/assets/d1ba6deb-29c3-4bc5-9686-42f99289cac0" />

2. This challenge requires storing the value COLLEGE in the PWN file and redirect the file to /challenge/run.

## My solve
**Flag :** 'pwn_college{IxF0o47_pnsXYZoQ_SRа=rZMKSQ.QXwcTN0wC0wIzNzEzW}'

I just simply used output of echo with the argument COLLEGE and redirected that to PWN file and then redirected the PWN file to the /challenge/run command, which gave out the flag

<img width="544" height="146" alt="Screenshot 2025-09-28 at 6 02 24 PM" src="https://github.com/user-attachments/assets/6be9fb1b-b1a4-4f5d-8131-af03cea7bf3a" />

## What I Learned

- I learned about redirecting input to programs just like redirecting out from them.
- Learned about the usage of < in the terminal.
- Did both simultaneously, redirecting output from one command to a file and then redirecting that file to another command.

### References
No external references are used to solve this challenge.

# Grepping Stored Results
### Key points
1. This challenge is about putting together the redirections concepts and searching through, the resulting file using **grep** command.
2. This challenge requires, output of /challenge/run being redirected to /tmp/data.txt file, which'll result in  hundred thousand lines of text, with one of them being the flag, in /tmp/data.txt.
3. I have to grep for that flag.

## My solve
**Flag :** 'pwn.college{E0N7F0o4jzsJhqGwrsAX4yy5CDY_QX4ED00wC0wIzNzEzW}'

I just redirected output from /challenge/run to the given file and then grepped through it as **grep pwn.college /tmp/data.txt** which gave out the flag.

<img width="584" height="215" alt="Screenshot 2025-09-28 at 6 07 09 PM" src="https://github.com/user-attachments/assets/660102c1-b507-4f14-b7d8-28a6a43948fe" />

<img width="578" height="193" alt="Screenshot 2025-09-28 at 6 07 31 PM" src="https://github.com/user-attachments/assets/31cf5035-e1fc-47fd-b500-7d3e6c2fc2a7" />

## What I Learned
- I learned the usage of grep with the concept of redirection, how to grep through the resulting file after redirecting output.

### References
None.

# Grepping Live Output
## Key points
1. We can cut out the middleman, no need to store results into another file, like in the last level.
2. One can do this by using the | (pipe) operator. Standard output from the command to the left of the pipe will be connected to (piped into) the standard input of the command to the right of the pipe. For example:

<img width="453" height="170" alt="Screenshot 2025-10-01 at 11 42 19 AM" src="https://github.com/user-attachments/assets/3402100f-0b0d-46e7-9cb2-43c0037f0d09" />

3. This challenge requires us to  grep for the flag from hundred thousand lines of text that /challenge/run will output.

## My solve
**Flag :** 'pwn.college180f5jf3hrkCYM-Jym2x8Xb-n9PQ-QX5ED00wCOw1ZNzEzW}'

I just simply put **/challenge/run** on the left side of the pipe, and _grep pwn.college_ on the right side of the pipe, by this the standard output of **/challenge/run** gets piped into standard input of the command on the right side of the pipe which is _grep pwn.college_.

 <img width="597" height="210" alt="Screenshot 2025-09-28 at 6 40 01 PM" src="https://github.com/user-attachments/assets/dbf69059-a57d-4260-9d6d-53fe04d993de" />

<img width="580" height="153" alt="Screenshot 2025-09-28 at 6 40 14 PM" src="https://github.com/user-attachments/assets/55071517-5194-4f51-8c78-bb25461da02a" />

## What I Learned
- I learned about the new |(pipe operator) which eliminates the need of storing output to the file, but instead can help grepping live output.

### References
None.

# Grepping Errors
### Key points
1. We've learnt redriecting errors to a file and pipe output to another program such as grep, what if one wants to directly grep through errors, also there is no 2| for standard errors to get redirected and grepped through live, like | for stdout.
2. There is this **>&** operator, which redirects a file descriptor to another file descriptor, now we can have a 2 step process of grepping through errors, first, we redirect standard error to standard output (2>& 1) and then pipe the now-combined stderr and stdout as normal (|)!
3. This challenge requires grepping the flag after redirecting sterr to stdout for /challenge/run and then use | to grep.

## My solve
**Flag:** 'pwn.college{4ugp5ihJLcg7u-jy0fblTxvMOuD.QX1ATO0wCOwIzNzEzW}'

I just simply used 2>&1 to redirect stderr to stdout and then grepped for the keyword pwn.college, which gave out the flag.

<img width="588" height="206" alt="Screenshot 2025-10-01 at 12 16 39 PM" src="https://github.com/user-attachments/assets/ae940d59-2eb2-4159-981d-bb70a271fb8c" />

<img width="592" height="138" alt="Screenshot 2025-10-01 at 12 17 06 PM" src="https://github.com/user-attachments/assets/888519aa-3ffa-4e49-9114-ea0abb7aaf38" />

## What I Learned
- Learned about the new >& operator which helps redirecting file descriptors themselves, from one to other
- Used the pipe with the new operator to grep for the flag.
 
### References
None.

# Filtering with grep -v
### Key Points
1. Exact opposite of what the normal grep command does, using grep -v searches for lines that **do not** match the pattern specified, in essence, if I give argument as pwn.college, it'll give out all lines which do not have pwn.college keyword in them.
2. Illustration:

<img width="467" height="172" alt="Screenshot 2025-10-01 at 12 21 54 PM" src="https://github.com/user-attachments/assets/3b12d1ba-4262-4fff-bb5e-189ea5c80950" />

3. Sometimes, the only way to filter to just the data you want is to filter out the data you don't want.
4. In this challenge, /challenge/run will output the flag to stdout, but it will also output over 1000 decoy flags (containing the word DECOY somewhere in the flag) mixed in with the real flag, requires filtering out all decoy flags and get the real one.

## My solve
**Flag :** 'pwn.college{M46P1SVibKFq9rL44mNpwvQCme.0FOxEzNxwCOwIzNzEzW}'

I just piped stdout of /challenge/run to grep -v DECOY, it gave out the real flag.

<img width="511" height="41" alt="Screenshot 2025-10-01 at 12 29 13 PM" src="https://github.com/user-attachments/assets/c6a39e85-074d-4829-91be-39280b33a6f9" />

## What I Learned
- Learned about the new option which does opposite of what grep does, which is usin -v with grep, gives out lines which don't match the pattern.

### References 
No external references.

# Duplicating piped data with tee
### Key points
1. When data is piped from one command to another, it doesn't show up on the screen, which not always desired.
2. One might want to see the data as it flows through between commands to debug unintended outcomes (e.g., "why did that second command not work???").
3. The _tee_ command named after "T-splitter" from _plumbing_ pipes, duplicates data flowing through your pipes to any number of files provided on the command line. For example:

<img width="437" height="185" alt="Screenshot 2025-10-01 at 1 08 39 PM" src="https://github.com/user-attachments/assets/635032d1-3113-40d3-b550-905fc6ae01de" />

by providing 2 files to tee, we ended up with 3 copies of the piped-in data: one to stdout, one to the pwn file, and one to the college file.
4. This can be used to debug things

> hacker@dojo:~$ command_1 | command_2
>
> Command 2 failed!
>
> hacker@dojo:~$ command_1 | tee cmd1_output | command_2
>
> Command 2 failed!
>
> hacker@dojo:~$ cat cmd1_output
>
> Command 1 failed: must pass --succeed!
>
> hacker@dojo:~$ command_1 --succeed | command_2
>
> Commands succeeded!

5. This challenge requires /challenge/pwn getting piped into /challenge/college, but it'll need for me to intercept data, to find what pwn needs.
## My solve
**Flag :** 'pwn.college{gHvflb2n1HxzhrVB4SwrsH19IYO.QXxITO0wCOwIzNzEzW}'

I ran /challenge/pwn | /challenge.college, which gave out some information, then i catted the pwn file which gave out the secret argument, then again ran the piping command which finally gave the flag.

<img width="599" height="232" alt="Screenshot 2025-10-01 at 1 27 55 PM" src="https://github.com/user-attachments/assets/6418a93b-bbf1-4abc-bac6-48359a8f025a" />

## What I Learned
- Learned about the new _tee_ command and how it can be useful to debug and show the flowing data when piped.

### References
None.

# Process substitution for input
### Key Points
1. Sometimes we require to compare output of commands, one way can be to assign those outputs to 2 files and use _diff_ command for comparison, but there is a more elegant way to do it.
2. Instead of doing
 
<img width="394" height="80" alt="Screenshot 2025-10-01 at 3 11 16 PM" src="https://github.com/user-attachments/assets/33fa206c-7f31-4013-8231-e6682a99f3e3" />

we can play on the philosophy that linux follows _everything is a file_ That is, the system strives to provide file-like access to most resources, including the input and output of running programs! The shell follows this philosophy, allowing you to, for example, use any utility that takes file arguments on the command line and hook it up to the output of programs, as you learned in the previous few levels.
3. Interestingly, we can go further, and hook input and output of programs to arguments of commands. This is done using _Process Substitution_.
4. <(command) will run the command and create a temporary file with the output of the command, this isn't a real file, this is what is called a named pipe.
5. example:

<img width="452" height="97" alt="Screenshot 2025-10-01 at 4 10 06 PM" src="https://github.com/user-attachments/assets/f88a7363-4087-4f83-91dc-3aa8f21e510f" />

<(echo hi) creates a temporary file with the output of _echo hi_ in it which is _hi_, then running echo command  with argument of that particular file as shown in the image gives the file name.
6. If we use it with cat, it'll print hi in the terminal.
7. We can also specify multiple times, like:


<img width="472" height="163" alt="Screenshot 2025-10-01 at 4 13 47 PM" src="https://github.com/user-attachments/assets/dfb50fc5-9ff3-4884-b198-999857ff8520" />

8. Now, I am supposed to differentiate between outputs of two different commands, one of which gives decoy flags and the other gives all the decoy flags with the real flag, using the _diff_ command.

## My solve
**Flag :**'pwn.college{8uE0XTPklUGrh7CBCb3RB76lNzR.0lNwMDOxwCOwIzNzEzW}'
I simply used the diff command with arguments as <(command1) <(command2) which gave out the flag.

<img width="586" height="94" alt="Screenshot 2025-10-01 at 4 16 33 PM" src="https://github.com/user-attachments/assets/c067eb61-e747-4445-b8a7-fbce57b1df03" />

## What I Learned
- I learned about a very useful thing, where comparing between outputs of two commands is made very easy, instead of assigning the outputs to files and then comparing we can simply use **<(command)** which makes a temporary file consisting of the output of that particular command.

### References
None.

# Writing to multiple programs
### Key points
1. One can also use process substitution for writing to commands, can duplicate data to two files with tee.
2. 
 

