# lab3_linux
1. Create a user account with the following attribute
   • username: “your first name”
   • Fullname/comment: “full name”
   • Password: islam
2. Create a user account with the following attribute
   • Username: baduser
   • Full name/comment: Bad User
   • Password: baduser
3. Create a supplementary (Secondary) group called pgroup with group ID of 30000
4. Create a supplementary group called badgroup
5. Add islam user to the pgroup group as a supplementary group
6. Modify the password of islam's account to password
7. Modify islam's account so the password expires after 30 days
8. Lock bad user account so he can't log in
9. Delete bad user account
10. Delete the supplementary group called badgroup
11. Create a folder called myteam in your home directory and change its permissions to read only for the owner.
12. Log out and log in by another user
13. Try to access (by cd command) the folder (myteam)
14. Using the command Line
    • Change the permissions of oldpasswd file to give owner read and write permissions and for group write and execute and execute only for the others (using chmod in 2 different ways)
    • Change your default permissions to be as above.
    • What is the maximum permission a file can have, by default when it is just created? And what is that for directory.
    • Change your default permissions to be no permission to everyone then create a directory and a file to verify.
15. Starting from your home directory, find all files that were modified in the last two day.
16. Starting from /etc, find files owned by root user.
17. Find all directories in your home directory.
18. Write a command to search for all files on the system that, its name is ".profile".
19. Identify the file types of the following: /etc/passwd, /dev/pts/0, /etc, /dev/sda
20. List the inode numbers of /, /etc, /etc/hosts.
21. Copy /etc/passwd to your home directory, use the commands diff and cmp, and Edit in the file you copied, and then use these commands again, and check the output.
22. Create a symbolic link of /etc/passwd in /boot.
23. Create a hard link of /etc/passwd in /boot. Could you? Why?
