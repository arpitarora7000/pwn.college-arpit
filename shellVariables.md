> The Linux command line interface is actually a sophisticated programming language with which you can write actual programs! Because the command line interface is colloquially referred to as a "shell", programs written in this language are referred to as "shell scripts". When you're using the command line, you are basically writing a shell script line by line!

> Like most programming languages, the shell supports variables. This module will get you familiar with setting, printing, and using these variables!

# Printing Variables
### Key Points
1. The flag for this challenge has been put into the variable names FLAG.
2. Echo can be used to print out variables just by prepending it with a $ sign, for example the variable PWD always holds the cwd of the current shell,

<img width="383" height="58" alt="Screenshot 2025-10-01 at 4 31 43 PM" src="https://github.com/user-attachments/assets/02df80d7-ddb9-48e5-a10c-f5c9dfeab888" />

3. Here, this challenge requires us to print the variable FLAG to get the flag.
  
## My solve
**Flag :** 'pwn.college{47FOlN0qTiGgdBeC-aXNpm0j1WT.QX3UTN0wCOwIzNzEzW}'

I just simply used echo command with the argument _$FLAG_, which printed out the FLAG variable, following is an image for it:

<img width="577" height="123" alt="Screenshot 2025-10-01 at 4 34 21 PM" src="https://github.com/user-attachments/assets/edbf64c2-5b71-4dd1-a5fe-a6dc36fd3791" />

## What I Learned
- I learned about shell variables, and how they can be printed using the echo command just prepending with $.
### References
No external references used.

# Setting Variables
### Key Points
1. We can write values to variables.
2. This is done, as with many other languages, using =. To set variable VAR to value 1337, you would use:

<img width="422" height="51" alt="Screenshot 2025-10-01 at 4 36 34 PM" src="https://github.com/user-attachments/assets/1869387b-9492-4d6d-a70e-1e587c036df9" />

3. Note that there are no spaces around the =! If you put spaces (e.g., VAR = 1337), the shell won't recognize a variable assignment and will, instead, try to run the VAR command (which does not exist).
4. This used VAR and doesn't prepend with $, which is used only while accessing variables, this prepending of $ triggers what is called variable expansion, and is, surprisingly, the source of many potential vulnerabilities.
5. Here the challenge requires us to set the PWN variable with the value COLLEGE.

## My Solve
**Flag :** 'pwn.college{kJKCvJz4_k8YEIpEjZVJU6QmFHX.QX5UTN0wCOwIzNzEzW}'

I just simply set the variable with the given value using the assignment operator **=**, then it gave out the flag, following is an image for it:

<img width="583" height="91" alt="Screenshot 2025-10-01 at 4 41 18 PM" src="https://github.com/user-attachments/assets/116b9d4d-b6ab-4bf9-8eac-008d9393dd4a" />

## What I Learned 
- Learned about how you can write to variables and store values in them, simply like any other coding language.

### References
No external references used for this challenge.

# Multi-word variables
### Key points
1. This challenge is about learning the significance of _quotes_, spaces have special significance in the shell, and there are places where you can't use them spuriously.
2. Writing to variables, we simply use = to specify values, without space, but what if we want to assign a value which has a space within it, for example 1337 SAUCE, one would try the following:

<img width="391" height="46" alt="Screenshot 2025-10-01 at 4 45 17 PM" src="https://github.com/user-attachments/assets/181d97bd-5425-4a55-be6b-4e9a16cb5122" />

This won't work for the simple reason that shell interprets anything as a command if written after space.
3. Here we'll have to use double quotes around the value that we need to store in the variable, for it to interpret it as a value to be specified, something like:

<img width="375" height="39" alt="Screenshot 2025-10-01 at 4 47 57 PM" src="https://github.com/user-attachments/assets/5777fbd2-692d-40d9-99b2-3f7efd992ee1" />

Here, the shell reads 1337 SAUCE as a single token, and happily sets that value to VAR. 

4. In this challenge one needs to set the variable PWN to COLLEGE YEAH.

## My Solve
**Flag :** 'pwn.college{sGgsc7kFhorpE3XXUr8IkwhxSm2.QXwYTN0wCOwIzNzEzW}'

I just simply specified the given value to the VAR variable using double quotes, following is an image:

<img width="503" height="69" alt="Screenshot 2025-10-01 at 4 51 25 PM" src="https://github.com/user-attachments/assets/00c3d81a-d2b1-4c16-8244-5c2befa302c9" />

## What I Learned
- Learned more about writing to variables, what to do and what not to.

### References
None.
# Exporting Variables
### Key Points
1. By default, variables that you set in a shell session are local to that shell process. That is, other commands you run won't inherit them. You can experiment with this by simply invoking another shell process in your own shell, like so:

<img width="407" height="161" alt="Screenshot 2025-10-01 at 4 53 29 PM" src="https://github.com/user-attachments/assets/0b8789f6-1cda-49cf-8613-4026c679c78b" />

In the output above, the $ prompt is the prompt of sh, a minimal shell implementation that is invoked as a child of the main shell process. And it does not receive the VAR variable!
2. This makes sense, of course. Your shell variables might have sensitive or weird data, and you don't want it leaking to other programs you run unless it explicitly should. How do you mark that it should? You export your variables. When you export your variables, they are passed into the environment variables of child processes. You'll encounter the concept of environment variables in other challenges, but you'll observe their effects here. Here is an example:

<img width="434" height="146" alt="Screenshot 2025-10-01 at 4 55 20 PM" src="https://github.com/user-attachments/assets/808a2742-32d3-4555-b3d8-14d3803798a6" />

Here, the child shell received the value of VAR and was able to print it out! You can also combine those first two lines.

<img width="471" height="116" alt="Screenshot 2025-10-01 at 4 56 08 PM" src="https://github.com/user-attachments/assets/21123578-7529-4bd5-a5e2-a177c15cbb54" />

3. In this challenge, one must invoke /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported (e.g., not inherited by /challenge/run).

 ## My solve
**Flag :** 'pwn.college{wQRtcLJe58VUZZpSSKBdT28nsp.QXyYTN0wCOwIzNzEzW}'

I just exported the given variable with the given value and specified the other variable with the given value and then ran /challenge/run with the given variable.

<img width="553" height="211" alt="Screenshot 2025-10-01 at 5 02 21 PM" src="https://github.com/user-attachments/assets/144c11a7-f63a-46f3-a8c1-ca496a4c3b29" />

## What I Learned
- Learned about exporting variables, so they can be used in all children shells.
 
### References
No external references.

# Printing exported variables
### Key points
1. There are multiple ways to access variables in bash. echo was just one of them, and this challenge is about learning at least one more of them.
2. There is this _env_ command which prints out every exported variable set in your shell, here it'll do the same and we have to look for the FLAG variable.

## My solve
**Flag :** 'FLAG=pwn.college{ACIhxhfLO7nFaFbq8bNkL7GyzHb.QX4UTN0wCOwIzNzEzW}'

I just ran the env command and looked through it to find the flag, image:


<img width="578" height="232" alt="Screenshot 2025-10-01 at 5 09 45 PM" src="https://github.com/user-attachments/assets/c5121be9-5783-43f1-ba03-a85b3d9acd5b" />

## What I Learned
- Learned about the new env command, and another method to print out variables other than using echo.

### References
No extrernal references.

# Storing command output
### Key points
1. Using command substitution we can store outputs of commands to shell variables.
2. Example:

<img width="418" height="112" alt="Screenshot 2025-10-01 at 5 14 15 PM" src="https://github.com/user-attachments/assets/3446b0ab-3cad-459a-b858-8105782546f5" />

So using $(command) we can store the output of the command to a given given variable.
3. Here, I am supposed to store the output of the command /challenge/run into the PWN variable, and then print it out to get the flag.

<img width="474" height="243" alt="Screenshot 2025-10-01 at 5 17 50 PM" src="https://github.com/user-attachments/assets/4f426434-8ef9-42ec-bab5-b73f33fc3c96" />

## My solve
**Flag :** 'pwn.college{ctbW9ygW9gi_rLHdSDb7NNDmORE.QX1cDN1wCOwIzNzEzW}'

I just stored the output of /challenge/run to the PWN variable using the given format, and read it out, using echo, which gave out the flag, following is an image for it:

<img width="581" height="150" alt="Screenshot 2025-10-01 at 5 20 02 PM" src="https://github.com/user-attachments/assets/722b8ebd-18cf-461d-bfd6-bcdb541df5af" />

## What I Learned
- Learned about how command outputs can be stored in variables, and some trivia about it.
  
### References
None.

# Reading Input
### Key points
1. One can take input from user, using the `read` builtin.
2. Using -p argument with read, lets us specify the prompt, example:

> hacker@dojo:~$ read -p "INPUT: " MY_VARIABLE
> 
>INPUT: Hello!
> 
> hacker@dojo:~$ echo "You entered: $MY_VARIABLE"
>
>You entered: Hello!

this stores the input in the MY_VARIABLE variable.
3. In this challenge, we've to use read to set the PWN variable to the value COLLEGE.

## My solve
**Flag :** 'pwn.college{YvGcPYfW8D_gcQDFHeUwecfruOO.QX4cTN0wCOwIzNzEzW}'

I just used `read` for the variable PWN and entered COLLEGE as my input, which then gave out the flag, image:

<img width="519" height="117" alt="Screenshot 2025-10-01 at 5 35 15 PM" src="https://github.com/user-attachments/assets/53b6dd9c-85a3-4201-ba4a-58d93775f547" />

## What I Learned
- Learned about the very significant builtin `read` which lets the user give input, using the -p argument to specify prompt while taking input.

### References
None.

# Reading files
### Key points
1. 










