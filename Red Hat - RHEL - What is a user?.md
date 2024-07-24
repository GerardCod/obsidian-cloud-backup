#Redhat #RHEL #Linux

A _user_ account provides security boundaries between people and programs that can run commands.

Users have _usernames_ to identify them to human users and for ease of working. Internally, the system distinguishes user accounts by the unique identification number, the user ID or _UID_, which is assigned to them. In most scenarios, if a human uses a user account, then the system assigns a secret _password_ for the user to prove that they are the authorized user to log in.

User accounts are fundamental to system security. Every process (running program) on the system runs as a particular user. Every file has a particular user as its owner. With file ownership, the system enforces access control for users of the files. The user that is associated with a running process determines the files and directories that are accessible to that process.

User accounts are of the following main types: the _superuser_, _system users_, and _regular users_.

- The _superuser_ account administers the system. The superuser name is `root` and the account has a UID of 0. The superuser has full system access.
    
- The _system user_ accounts are used by processes that provide supporting services. These processes, or _daemons_, usually do not need to run as the superuser. They are assigned non-privileged accounts to secure their files and other resources from each other and from regular users on the system. Users do not interactively log in with a system user account.
    
- Most users have _regular user_ accounts for their day-to-day work. Like system users, regular users have limited access to the system.