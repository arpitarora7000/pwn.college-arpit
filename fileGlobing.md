# Matching with *
### Key Points

1. The first glob is _*_, when shell encounters a _*_ in any argument, it'll treat it as a _wild card_
2. And then try to replace that argument with any files that match the pattern, just like:

<img width="466" height="184" alt="Screenshot 2025-09-27 at 1 08 12 PM" src="https://github.com/user-attachments/assets/aebf1605-292c-4121-8fbe-d26b049eee13" />

3. In this glob resulted in multiple arguments, it can also simply match only one, like:

<img width="636" height="142" alt="Screenshot 2025-09-27 at 1 09 34 PM" src="https://github.com/user-attachments/assets/725bc5f2-6334-46ab-9862-cb5da8ce339f" />

4.When zero files are matched, the shell leaves the glob unchanged, something like using nope_ _*_ instead of file_ _*_, like:

<img width="557" height="134" alt="Screenshot 2025-09-27 at 1 11 17 PM" src="https://github.com/user-attachments/assets/72d1911c-e532-4019-bca5-f4b44dbc1c65" />

5. The * matches any part of the filename except for / or a leading . character. For example:

<img width="536" height="158" alt="Screenshot 2025-09-27 at 1 13 02 PM" src="https://github.com/user-attachments/assets/626c1b80-9aa7-4c23-a411-fb99fa072315" />

6. In this i gotta use the glob to cd to /challenge and then run /challenge/run to get the flag.

## My solve
**Flag :** 'pwn.college{MKWqFu_RYG5zRqdYxbssIOzqrs3.QXxIDO0wCOwIzNzEzW}'

I just cd'd into the /challenge directory by using the glob and that too with an argument of length less than or equal to 4 charactes something like, and then ran /challenge/run, which gave out the flag.

<img width="533" height="88" alt="Screenshot 2025-09-27 at 1 21 46 PM" src="https://github.com/user-attachments/assets/ded50bcb-c79a-4d50-a20f-6b4f172dffe2" />

The **/challenge/run** could've also be run by using glob like:

<img width="531" height="43" alt="Screenshot 2025-09-27 at 1 36 43 PM" src="https://github.com/user-attachments/assets/353e4baa-f31e-47f9-b783-6330c47cd1bc" />


or:

<img width="540" height="62" alt="Screenshot 2025-09-27 at 1 36 56 PM" src="https://github.com/user-attachments/assets/364ac638-6fee-4cfc-a02e-f88787333dac" />


## What I Learned
- I learned about globbing, the first glob *, how to use it, differne ways and formats to use it.
- I used it to change directory and also for invoking program to get the flag
### References
This solution is entirely based on the problem statement.
# Matching with ?
### Key points
1. This glob is just like _*_ but only for a single character instead of being for n number of characters as is _*_.
2. When it encounters a ? character in any argument, the shell will treat it as a single-character wildcard, something like:

<img width="437" height="236" alt="Screenshot 2025-09-27 at 1 43 02 PM" src="https://github.com/user-attachments/assets/7747d2fe-5f59-470a-9536-3e9ce9fde4d3" />

3. In this challenge i gotta change the directory using the ? glob with some constarints and then run /program/run to get the flag.
## My solve
**Flag :** 'pwn.college{YYX9U3l4x3hP97RJ6a9zkhbldDJ.QXyIDO0wCOwIzNzEzW}'

I just cd'd into the /challenge directory using the glob and follwoing the constraints which were to use ? in place of c and l, and then invoked /challenge/run to get the flag, following is an image:

<img width="578" height="169" alt="Screenshot 2025-09-27 at 1 50 39 PM" src="https://github.com/user-attachments/assets/c036f4f7-8924-44ac-8653-218657ab1d5e" />

I could've also invoked the program by using the glob like in the last challenge.

## What I Learned
- I learned about the ? glob, how it is used for a single character only, other than works like _*_ only.
### References
None.
# Matching with []
### Key points
1. [] is a limited form of ?, instead of matching any characters it is a wildcard for some subest of potential characters, specified witin brackets.
2. For example, [pwn] will match the character p, w, or n. For example:


<img width="392" height="180" alt="Screenshot 2025-09-27 at 1 55 50 PM" src="https://github.com/user-attachments/assets/5ebe6362-abda-472f-8809-23331e5aa6e1" />

3. Hint given:

<img width="475" height="149" alt="Screenshot 2025-09-27 at 1 58 25 PM" src="https://github.com/user-attachments/assets/f392b28b-a085-4167-bbd7-b028f8244230" />

## My solve
**Flag :** 'pwn.college{c8OSQLjkUWFnxmK4U319CeKftyq.QXzIDO0wCOwIzNzEzW}'

I just changed my directory to the given one and then ran the program with the glob to search for any files, with the names as were given, then it gave out the flag

Image:

<img width="566" height="118" alt="Screenshot 2025-09-27 at 2 02 20 PM" src="https://github.com/user-attachments/assets/1b25feac-38df-44f3-81b5-fa5bf2ffd457" />

## What I Learned
- Learned about the new glob, which is a wild card for some subset of potential characters, it is a limited version of ?.
### References
None.
# Matching paths with []
### Key points
1. Globbing happens on a path basis, so you can expand entire paths with your globbed arguments.
2. Like:
 
> hacker@dojo:~$ touch file_a

> hacker@dojo:~$ touch file_b

> hacker@dojo:~$ touch file_c

> hacker@dojo:~$ ls

> file_a	file_b	file_c

> hacker@dojo:~$ echo Look: /home/hacker/file_[ab]

> Look: /home/hacker/file_a /home/hacker/file_b

3. Hint given:
 
 <img width="472" height="184" alt="Screenshot 2025-09-27 at 3 06 14 PM" src="https://github.com/user-attachments/assets/ea19bb80-c73a-43e7-bea5-e8317f84be78" />

## My solve
**Flag :** 'pwn.college{IUcjl8-hdZljzbscxKYzQmtdIeg.QX0IDO0wCOwIzNzEzW}'

I just invoked /challenge/run with a single argument, that bracket globs into the absolute paths to the files file_b, file_a, file_s, and file_h.

Following is an image:

<img width="600" height="111" alt="Screenshot 2025-09-27 at 3 08 56 PM" src="https://github.com/user-attachments/assets/16de4af5-d281-4a62-9667-f4062a5f9abe" />

## What I Learned
- Learned about globbing onpaths basis, and how can i expand entire paths with globbed arguments.
### References
No external references used for this challenge.
#  Multiple Globs
### Key points
1. So far, weve specified one glob at a time, but you can do more, Bash supports the expansion of multiple globs in a single word. For example:

<img width="401" height="90" alt="Screenshot 2025-09-27 at 3 12 30 PM" src="https://github.com/user-attachments/assets/14298244-8bba-410d-b51e-0f416467e179" />

2. What happens above is that the shell looks for all files in **/** that start with anything, which can also be blank space i.e nothing, then have an _f_ and an _l_, and end in anything (including _ag_, which makes _flag_).
3. Hint given:
 
<img width="480" height="187" alt="Screenshot 2025-09-27 at 3 15 21 PM" src="https://github.com/user-attachments/assets/6bcc4cff-fbe2-4c80-9b98-f493e279c30f" />

## My solve
**Flag :** 'pwn.college{oy3x37IIwirXGG1YM6qhfxGAc_W.0lM3kjNxwCOwIzNzEzW}'

I just cd'd into the /challenge/files directory and thought of an argument to give to /challenge/run, which is 3 characters or less and will cover all words containing the letter p, which was easy to figure out: _*p*_, starts with anything, ends with anything, has the letter p, following is an image.

<img width="498" height="112" alt="Screenshot 2025-09-27 at 3 22 09 PM" src="https://github.com/user-attachments/assets/22650c14-f842-401b-b8a5-4a3ab9435de9" />

## What I Learned
- I learned about using multiple globs in a single argument.
### References
Took a little time to figure out the argument but no references other than the problem statement.
# Mixing globs
### Key points
1. Again a few happy but diversely named files are put in /challenge/files directory.
2. I gotta cd to that directory, and using the globbing that i've learned write a glob 6 characters or shorter that will match the files "challenging", "educational", and "pwning", when passed as an argument to /challenge/run.
##  My solve
**Flag :**'pwn.college{s5kO02GPoJGYWKyYGt-knIjFHFh.QX1IDO0wCOwIzNzEzW}'

This time it took significant time to figure out, what glob to pass as argument, the  realized I'll have to use [] and * both the globs, then, first good enough attempt was:

<img width="607" height="71" alt="Screenshot 2025-09-27 at 7 55 58 PM" src="https://github.com/user-attachments/assets/e101941f-c990-408a-a51b-71a9dd7acd2a" />

Then I thought of adding an "n":

<img width="625" height="85" alt="Screenshot 2025-09-27 at 7 57 08 PM" src="https://github.com/user-attachments/assets/f7c6dab2-dc3d-421a-86fa-b0b8ec11896b" />

after these 2 attempts, and another failed one, I used SENSAI, prompted it with help and it suggested to go for the beginnings of names of each of the 3 files instead of endings if that is somewhat unique, then I tried:

<img width="487" height="52" alt="Screenshot 2025-09-27 at 8 03 59 PM" src="https://github.com/user-attachments/assets/1caa9772-968f-469f-adf8-854905279e0f" />


This got me the flag.
## What I Learned
- I learned the correct usage of mixing globs.
- After multiple attempts, it led me to the flag, which made me learn what to do and what not to, keeping in mind the exact file names, which was very crucial in regard to this particular challenge.
### References
SENSAI's suggestion was used as an external resource to solve this challenge.
# Exclusionary Globbing
### Key points
1. Specifically for **[]** glob there is a character defined **!** which if typed in as the first character in the brackets with more characters, will list out files which doesn't have those characters, for newer versions of bash it is **^**.
2. It's just like the _!=_ used in coding languages as _not equal to_, following is an example:

 <img width="440" height="292" alt="Screenshot 2025-09-27 at 8 11 59 PM" src="https://github.com/user-attachments/assets/7d1a391f-df55-42f5-86a7-556d86a22d2a" />

3. Now, I gotta cd into /challenge/files and then invoke the program /challenge/run with all files that dont start with the letters _p,w or n_.
> NOTE: The ! character has a different special meaning in bash when it's not the first character of a [] glob, so keep that in mind if things stop making sense! ^ does not have this problem, but is also not compatible with older shells.
## My Solve
**Flag :** 'pwn.college{glpgmP621_nJvj8ETP0DnV3cJK5.QX2IDO0wCOwIzNzEzW}'

I just cd'd into the directory and ran /challenge/run with the glob [pwn]* which gave out the flag, following is an image:

<img width="581" height="125" alt="Screenshot 2025-09-27 at 8 18 12 PM" src="https://github.com/user-attachments/assets/11a73d8d-e154-4882-afc6-4039816eb0e1" />

## What I Learned
- Applied mixed gobbling again, with a special character usage, and learned the details about it.
### References
No external references.
# Tab Completion
### Key Points
1. Using * to shorten whatever is typed on the commandline is tempting but it might lead to errors and expand to unintended files, and it'll be too late when the rm command will already be running, no one is safe from this style of error.
2. A safer alternative when you are trying to specify a specific target is tab completion.
3. If one hits tab in the shell, it'll try to figure out what you're going to type and automatically complete it. Auto-completion is super useful.

4. Hint given:

 <img width="484" height="156" alt="Screenshot 2025-09-27 at 8 30 12 PM" src="https://github.com/user-attachments/assets/5a094d3b-3bc7-4916-b335-d7eae8afb29d" />

> hacker@dojo:~$ ls /challenge
 
> DESCRIPTION.md  pwncollege

> hacker@dojo:~$ cat /challenge/pwncollege
 
> cat: /challenge/pwncollege: No such file or directory

> hacker@dojo:~$ cat /challenge/pwn<TAB>

> pwn.college{HECK YEAH}

> hacker@dojo:~$

## My solve
**Flag :** 'pwn.college{MWmcuOkdbftLYwXevfmjGKgy3Fb.0FN0EzNxwCOwIzNzEzW}'

I just catted the /challenge/pwncollege, but as was mentioned I couldn't type in the name of the file exactly so used the tab key just after writing pwn which completed the name and gave out the flag.

<img width="454" height="88" alt="Screenshot 2025-09-27 at 8 34 00 PM" src="https://github.com/user-attachments/assets/0d2a8436-84d6-4a16-abe8-fa0a25914d52" />

## What I Learned
- I learned about the tab completion and how it is helpful and also saves times and errors when one tries to use globbing, might make errors, tab completion is a way better alternative.
### References
None.
# Multiple options for tab completion
### Key points
1. A confusing situation:

<img width="328" height="79" alt="Screenshot 2025-09-27 at 8 37 43 PM" src="https://github.com/user-attachments/assets/0061ecc3-0bbf-4224-8312-38ca40050d63" />

2.What happens varies based on the specific shell and its options. By default bash will auto-expand until the first point when there are multiple options (in this case, fl). When you hit tab a second time, it'll print out those options. Other shells and configurations, instead, will cycle through the options.
3. HINT: 

<img width="470" height="119" alt="Screenshot 2025-09-27 at 8 41 34 PM" src="https://github.com/user-attachments/assets/02a2269d-9822-4d20-ad4c-6db1518a80a6" />

## My solve
**Flag :** 'pwn.college{83zHq0Hf_Obsfd87yKNYZr-8r1a.0lN0EzNxwCOwIzNzEzW}'

I just catted out /challenge/files/pwn pressed tab once and then again and it listed out the files, then used cat again with that particular file which had flag, image:

<img width="609" height="156" alt="Screenshot 2025-09-27 at 8 43 16 PM" src="https://github.com/user-attachments/assets/247f33b5-2ca4-4c4e-a845-cf84fa5572e8" />


## What I Learned
- Learned about different ways to use tab completionm, how it can be useful when same begining characters are their for files.
### References
None.
# Tab completion on commands
### Key points
1. Tab completion can not only be used for files but also for commands.
2. Here a command starting from pwncollege needs tab completion to be used for it run
 
> NOTE: You can auto-complete any command, but be careful: callous auto-completes without double-checking the result can wreak havoc in your shell if you accidentally run the wrong commands!
## My solve
**Flag:** 'pwn.college{ovub67jv53JAbSLc91DANxqQ54q.0VN0EzNxwCOwIzNzEzW}'

I just typed in pwncollege and pressed tab and enter it gave out the flag autocompleting the command.

Image:

<img width="575" height="105" alt="Screenshot 2025-09-27 at 8 47 45 PM" src="https://github.com/user-attachments/assets/d3923147-483d-4a8b-89ed-bec895861a9e" />

## What I Learned
- learned about tab competion for commands and used it.
- learned how callous auto-completes without double-checking can wreak havoc in the shell if wrng commands run.
### References
None.
