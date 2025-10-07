# Cracking Passwords
### Key points
1. When you enter a password for su, it compares it against the stored password for that user. These passwords used to be stored in /etc/passwd, but because `/etc/passwd` is a _globally-readable file_, this is **not good** for passwords, these were moved to `/etc/shadow`.
2. Here is the example /etc/shadow from the previous level:

>     root:$6$s74oZg/4.RnUvwo2$hRmCHZ9rxX56BbjnXcxa0MdOsW2moiW8qcAl/Aoc7NEuXl2DmJXPi3gLp7hmyloQvRhjXJ.wjqJ7PprVKLDtg/:19921:0:99999:7:::daemon:*:19873:0:99999:7:::

<img width="429" height="574" alt="Screenshot 2025-10-08 at 3 04 02 AM" src="https://github.com/user-attachments/assets/431c9244-5484-45bf-9024-733051f7225e" />

a few more and

> zardus:$6$bEFkpM0w/6J0n979$47ksu/JE5QK6hSeB7mmuvJyY05wVypMhMMnEPTIddNUb5R9KXgNTYRTm75VOu1oRLGLbAql3ylkVa5ExuPov1.:19921:0:99999:7::: 

Separated by :s, the first field of each line is the username and the second is the password. A value of * or ! functionally means that password login for the account is disabled, a blank field means that there is no password (a not-uncommon misconfiguration that allows password-less su in some configurations), and the long string such as Zardus' $6$bEFkpM0w/6J0n979$47ksu/JE5QK6hSeB7mmuvJyY05wVypMhMMnEPTIddNUb5R9KXgNTYRTm75VOu1oRLGLbAql3ylkVa5ExuPov1. is the result of one-way-encrypting (hashing) Zardus' password from the last level (in this case, dont-hack-me).

3. When you input a password into su, it one-way-encrypts (hashes) it and compares the result against the stored value. If the result matches, su grants you access to the user!

But what if you don't know the password? If you have the hashed value of the password, you can crack it! Even though /etc/shadow is, by default, only readable by root, leaks can happen! For example, backups are often stored, unencrypted and insufficiently protected, on file servers, and this has led to countless data disclosures.

If a hacker gets their hands on a leaked /etc/shadow, they can start cracking passwords and wreaking havoc. The cracking can be done via the famous John the Ripper, as so:

<img width="950" height="232" alt="Screenshot 2025-10-08 at 3 07 07 AM" src="https://github.com/user-attachments/assets/a81424f2-5e66-4876-90ca-163ca578c406" />

Here, John the Ripper cracked Zardus' leaked password hash to find the real value of password1337. Poor Zardus!

4. This level simulates this story, giving you a leak of /etc/shadow (in /challenge/shadow-leak). Crack it (this could take a few minutes), su to zardus, and run /challenge/run to get the flag!

## My solve
**Flag :**`pwn.college{M74G4rrDljrdY35CnOrOik7jRnj.QX3UDN1wCOwIzNzEzW}`

I ran `john /challenge/shadow-leak` which gave out the password for 'zardus' , then I used `su` for user zardus, using the password and ran /challenge/run to get the flag.

<img width="603" height="185" alt="Screenshot 2025-10-08 at 3 10 04 AM" src="https://github.com/user-attachments/assets/84091fa9-9a81-43c9-9a7a-e343709703cb" />

## What I Learned
- Learned a lot in this challenge, beginning with the file /etc/shadow, which stores passwords, and how it is not good for passwords to be store in /etc/passwd, because it is a globally readable file.
- Saw an example of /etc/shadow file from the previous challenge, which stored passwords for all users, in the pattern, with username then ! or *, showing that password login for this particular account is disabled, and a blank field meaning that there is no password, and also the long string such as Zardus' which is the result of one-way encrypting(hashing) Zardus' password from the last level.
- When a password is input into `su` it _hashes_ and then compares the result with the stored value.
- One can crack the password, by knowing just the hashed value, which can be accesses if there is a leak in `/etc/shadow`.
- Learned about the new command `john` which gives passwords from the hashed values if the leaked file containing the hashed value is given to it as argument.

### References
No external references, just the problem statement and theory about cracking passwords, were used to solve this problem.

