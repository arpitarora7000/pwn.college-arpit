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
