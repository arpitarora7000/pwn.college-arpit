# Learning from Documentation
### Key points
1. Correct usage of programs depends on proper specification of arguments to them, like it was the case for **ls** command to show hidden files using _-a_.
2. Program for this challenge is **/challenge/challenge**, we have to invoke it properly, in order for it to give out the flag.
3. Following is the given documentation:

<img width="493" height="141" alt="Screenshot 2025-09-26 at 8 59 27 PM" src="https://github.com/user-attachments/assets/dd7dd44b-fd97-4aee-8dc5-667839756d29" />

## My solve
**Flag :** 'pwn.college{0xfVPrio0aaHbhMCKhdpCapxEdj.QX0ITO0wCOwIzNzEzW}'

I simply ran /challenge/challenge with the argument  _--giveflag_ which gave out the flag, following is an image:

<img width="592" height="103" alt="Screenshot 2025-09-26 at 9 03 25 PM" src="https://github.com/user-attachments/assets/d1d22208-8827-4615-8a51-5cdb4052efc9" />

## What I Learned
- Learned the importance of correct usage of arguments while invoking a program.
### References
No external references were required for this challenge.
# Learning Complex usage
### Key points
1. Using most commands is straightforward but in commands like **sed** and **awk** the rguments can be entire programs in estoric programming languages
2. We,ve already encountered this while using the find commandl, while giving it -**name** argument which in itself takes another argument, specifying the name to search for, many other commands are analogous.
3. Given documentation, for /challenge/challenge:


 <img width="489" height="246" alt="Screenshot 2025-09-26 at 9 34 21 PM" src="https://github.com/user-attachments/assets/58a41492-4569-4f69-aaa9-31f0493919aa" />

## My solve
**Flag :** 'pwn.college{kRcNn3L5ojni1X-UkUfW_JHC7--.QX1ITO0wCOwIzNzEzW}'

I just simply ran **/challenge/challenge** with the _--printfile_ argument which takes an argument of itself and prints that file which is **/flag** following is an image for it:

<img width="629" height="103" alt="Screenshot 2025-09-26 at 9 36 52 PM" src="https://github.com/user-attachments/assets/25ed8da8-5c31-482c-9f79-005211510bfc" />

## What I Learned
- I learned the complex usage which required an arguemnt for a command which takes an argument itself.
### References
No references were used to solve this challenge.
# Reading Manuals
### Key points
1. The **man** command short for manual, if we have to see the manual, i.e learn about any command, we can pass it to the man command as an argument.
2. For the yes command if given as an argument to man command it'll give a manual page for yes, which shows **name**,**synopsis**,**description**,author,reporting bugs,copyright and a **see also section**, important ones are higlighted.
3. One can hit q to quit from the manual page, and use pgup and pgdn to move up and down.
4. Man pages are stored in centralized database, database lives in **/usr/share/man** directory.
5. One never needs to interact with it directly: you just query it using the man command. The arguments to the man command aren't file paths, but just the names of the entries themselves (e.g., you run man yes to look up the yes manpage, rather than man /usr/bin/yes, which would be the actual path to the yes program but would result in man displaying garbage).
6. There is a secret stored in the manpage of _challenge_ when used, will give the flag out.
## My solve
**Flag :** 'pwn.college{welqi7tryndCBU3oSS-pfvvgMvI.QX0EDO0wCOwIzNzEzW}'

I just ran the man command with the challenge argument which gave out the man page which has a secret stored in it, which said: **gives out flag if --welqit NUM used as argument and NUM is 730.**, i quit the manpage and ran challenge with that particular argument, it gave out the flag, image:

<img width="612" height="97" alt="Screenshot 2025-09-26 at 9 58 36 PM" src="https://github.com/user-attachments/assets/730ab96e-dbbf-4111-82ff-6e8fd896be2e" />

## What I Learned
- I learned about the new man command, how to access manual for any command and how to operate inside it, and what important contents are their in a manpage, where the database lives with all the manpages.
- Used the man command to check the manual for challenge and figure out the argument which would give out flag.
### References
Solution purely based on reasoning and in - challenge hints.
# Searching Manuals
### Key points
1. One can search using **/** inside a man page for a particular command.
2. Here, one has to search for an argument which would give out the flag using the /, also one can go back to the prev result by typing in _N_ and to the next result by _n_.
## My solve
**Flag :** 'pwn.college{YEUOOEwFeqKZxHm_6H0ZLcqSSxX.QX1EDO0wCOwIzNzEzW}'

I just opened the man page for challenge and searched by writing **/flag** which highlighted the word flag, which corresponded to the --yr argument written as:

<img width="456" height="202" alt="Screenshot 2025-09-26 at 10 18 29 PM" src="https://github.com/user-attachments/assets/84876acc-45ff-4cfe-a93d-5ed4e2959ced" />

Then i invoked /challenge/challenge with the given argument following is an image:

<img width="628" height="170" alt="Screenshot 2025-09-26 at 10 19 29 PM" src="https://github.com/user-attachments/assets/8f2cd75c-3036-42ec-97db-e97eb3fd508a" />

## What I Learned
- Learned about how to search in a man page.
- Searched a particular keyword in the man page which gave me the command to find my flag.

### References
No references used, just in - challenges hints.
# Searching For Manuals
### Key points
1. In this challenge, the man page for **challenge** is hidden by randomizing its name, Luckily, all of the manpages are gathered in a searchable database.
2. Now we'll have to use **man man** which'll teach advanced usage of man command, which'll be usable to figure out, how to search for the right man page that in turn will tell how to use **/challenge/challenge**
3. Though the manpage is randomly named, one still actually uses /challenge/challenge to get the flag!
## My solve
**Flag :** ''
  
