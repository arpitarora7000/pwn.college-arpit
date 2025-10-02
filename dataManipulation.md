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

I ran /challenge/run, and got the case-swapped flag, then after trying a few times, not being able to figure out, what to do, I wrote `man tr`, which openend the manual for the **tr** command, I found out how one can create different sets of characters as arguments, like for all lower case alphabets, one could use [:lower:] and for all upper case, [:upper:], then I tried putting in some arguments to the, tr command, following are images:

This is what I found on the man page for tr.

<img width="482" height="214" alt="Screenshot 2025-10-02 at 7 54 52 PM" src="https://github.com/user-attachments/assets/7f7ea1e7-1d03-440c-b68b-1d9bb81d08eb" />

This and some more, that I tried to swap case.

<img width="572" height="173" alt="Screenshot 2025-10-02 at 7 56 21 PM" src="https://github.com/user-attachments/assets/a96c26a9-fe5b-4c95-a723-89d2dbb43b75" />

Then asking SENSAI about the problem, I found out that I could make one whole argument as the set of letters that I want to change by using quotations, like writing '[:lower:][:upper:]' this is the first argument, and the second one that this changes to is the exact reverse of this, something like:

<img width="584" height="71" alt="Screenshot 2025-10-02 at 8 00 20 PM" src="https://github.com/user-attachments/assets/065dadbf-70ce-4468-b69c-5bc4479cd670" />

This gave out the exact flag.

While going through the manpage, I found out some other methods to solve this too, like making sets of characters like 'a-zA-Z' changes to 'A-Za-z', here it is:

<img width="559" height="48" alt="Screenshot 2025-10-02 at 8 04 20 PM" src="https://github.com/user-attachments/assets/a94ca888-b95b-47dc-8403-1635e65e02cf" />

<img width="562" height="52" alt="Screenshot 2025-10-02 at 8 04 49 PM" src="https://github.com/user-attachments/assets/d2ffbb6c-04b1-4315-8a68-8ce41dc1f662" />

## What I Learned
- I learned about the new `tr` command, useful application of data manipulation.
- Went through the manpage of the command, learned about different arguments that one can use for it.

### References
Manpage of tr and SENSAI.

# Deleting Characters
### Key Points
1. Something I'd already noticed while doing the last challenge, is the `-d` flag for `tr` command, which helps deleting characters.
2. An example:
 
<img width="643" height="91" alt="Screenshot 2025-10-02 at 8 12 16 PM" src="https://github.com/user-attachments/assets/97023216-0e7a-4c7c-855e-092bb65a892f" />

3. Here some decoy characters (specifically: % and ^) are interspersed among thr flag, I gotta delete them.

## My solve
**Flag :** `pwn.college{8pQcc7Yv7afe2x-ZbdBw9qTikBL.0FNxEzNxwCOwIzNzEzW}`

Firstly I tried, to remove the characters one after the other, which obviously didn't work, then I tried making two different strings to remove, which didn't work too, learnt that using the `-d` flag, it takes only one complete string as an argument, then places both the characters together to be deleted, following is an image:

<img width="498" height="122" alt="Screenshot 2025-10-02 at 8 17 37 PM" src="https://github.com/user-attachments/assets/efecf97d-decd-4c62-9203-1a5d8a181962" />

## What I Learned
- Learned about the usage of **-d** flag for the `tr` command.

### References
No external references used.

# Deleting New Lines
### Key Points
1. A common class of characters to remove is a line separator. This happens when you have a stream of data that you want to turn into a single line for further processing. You can specify newlines almost like any other character, by _escaping_ them:

<img width="496" height="116" alt="Screenshot 2025-10-02 at 8 20 51 PM" src="https://github.com/user-attachments/assets/e58d0000-5e84-48f5-89fa-56634e46f8fe" />

Here, the backslash (\) signifies that the character that follows it is a standin for a character that's hard to input into the shell normally. The newline, of course, is hard to input because when you typically hit Enter, you'll run the command itself. \n is a standin for this newline, and it must be in quotes to prevent the shell interpreter itself from trying to interpret it and pass it to tr instead.

2. Now, the flag has a bunch of new lines in it, I have to delete them to get the complete real flag.
 
> Fun fact! Want to actually replace a backslash (\) character? Because \ is the escape character, you gotta escape it! \\ will be treated as a backslash by tr. This isn't relevant to this challenge, but is a fun fact nonetheless!
 
## My solve
**Flag :** `pwn.college{0iaz0O40rUE8spgyIw2UaWt-Ft6.0VNxEzNxwCOwIzNzEzW}`

I just simply wrote the following command, which gave out the flag

<img width="582" height="90" alt="Screenshot 2025-10-02 at 8 25 32 PM" src="https://github.com/user-attachments/assets/bb1ce931-4fa2-43cd-b4f2-c9e6007a50f4" />

## What I Learned
- Learned about the newline character, and also how to delet them using `tr -d`.

### Reerences
None.

# Extracting the first lines with head
### Key Points
1. The head command is used to display the first few lines of its input:
 
<img width="877" height="322" alt="Screenshot 2025-10-02 at 8 29 10 PM" src="https://github.com/user-attachments/assets/154c0d54-f745-40a3-a3e6-88ba0ec37b21" />

By default, it shows the first 10 lines, but you can control this with the -n option:

<img width="664" height="111" alt="Screenshot 2025-10-02 at 8 30 30 PM" src="https://github.com/user-attachments/assets/f5b3f043-610e-4c51-af2c-d88edb02694b" />

2. Here I have to use the `head`  command to get the first 7 lines of the output that `/challenge/pwn` gives, and then further pipe it to `/challenge/college`, then it'll give the flag.

## My solve
**Flag :** `pwn.college{M1GHSojfvcphnGDbB9p-JPWcoSM.0lNxEzNxwCOwIzNzEzW}`

I just simply wrote the following command:

<img width="597" height="94" alt="Screenshot 2025-10-02 at 8 35 07 PM" src="https://github.com/user-attachments/assets/da33e85e-c6d7-4f8a-a008-1ca087dda92f" />

## What I Learned
- Learned a new command called `head` and a flag for it `-n` which is used to particularly get the number of lines specified from a given output.
 
### References

No external references used.

# Extracting specific sections of text
### Key points
1. Sometimes, you want to grab specific columns of data, such as the first column, the third column, or the 42nd column. For this, there's the cut command.
2. For example, imagine that you have the following data file:

<img width="453" height="108" alt="Screenshot 2025-10-02 at 10 58 13 PM" src="https://github.com/user-attachments/assets/1a56e068-6243-434b-822e-1a2e53468483" />

3. 
