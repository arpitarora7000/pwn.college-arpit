This module is about Linux permissions, which is a very important part of the journey ahead, and mediates the access to files across different users.

In Linux, files have different permissions or file modes. You can check out the permissions of a file or directory using ls -l. Let's make some files and look at their permissions:

> hacker@dojo:~$ mkdir pwn_directory
> 
> hacker@dojo:~$ touch college_file
> 
> hacker@dojo:~$ ls -l
> 
>total 4
> 
> -rw-r--r-- 1 hacker hacker    0 May 22 13:42 college_file
> 
> drwxr-xr-x 2 hacker hacker 4096 May 22 13:42 pwn_directory
> 
> hacker@dojo:~$
 
Lots of information is there, let's look at it at a high level.

# The file type

The first character of each line represents the file type. In pwn_directory's case, the d indicates that it's a directory, and in college_file's case, the - represents that it's a normal file. There are other types as well, that we'll explore later.

# The Permissions

The next nine characters are the actual access permissions of the file or directory, split into 3 characters denoting the permissions that the user who owns the file (termed the "owner") has to the file, 3 characters denoting the permissions that the group that owns the file (termed the "group") has to the file, and 3 characters denoting the permissions that all other access (e.g., by other users and other groups) has to the file, more about these in later modules.

# Ownership Information

There are two columns showing the user that owns the file (in this case, user _hacker_) and then the group that owns the file (in this case, also group _hacker_). You'll mess around with that here!

This module is for practicing perceiving permissions.





