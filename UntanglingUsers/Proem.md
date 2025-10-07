One would ponder if, they are the only user in the workspace, well that is far from the truth that there are MANY users on a typical Linux system, the full list of users is specified in the `/etc/passwd` file, named so for historical reasons, doesn't store passwords anymore. One could check out by catting out this file that what all users are there, except from us the _hacker_, an example is as follows:

<img width="501" height="237" alt="Screenshot 2025-10-08 at 1 56 07 AM" src="https://github.com/user-attachments/assets/06d3618d-80c4-4e50-afb8-475d636dd2bc" />

This is from the dojo container, there are many more not in the image shown, a lot of users here, and a lot of info! Each line contains, separated by :s (colons), the username, an x as a placeholder for where the password used to be, the numerical user ID, the numerical default group ID, long-form user details, the home directory, and the default shell, We can see the hacker user at the bottom. That's me! Most of the rest of these users are either there for historical reasons, are service accounts to support various installed software, or some are "utility" accounts (e.g., the nobody user is used to ensure that, e.g., some programs run without any special privileges).

One important user is `root`: the system administrator. The system administrator has obvious security implications: a _hacker_ user that can somehow, through various functionalities of Linux, become the root user would be able to wreak havoc on the system. A very frequent goal of hackers breaking into systems is to escalate to root, and thus root must be defended at all cost!

This module is about exploring various user shenanigans, learn the intended ways to switch users to administer the system, and have fun along the way!





