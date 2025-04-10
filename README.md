# lab3_linux
1. Create a user account with the following attribute
   • username: “your first name”
   • Fullname/comment: “full name”
   • Password: islam

         sudo useradd Salma -c "salma sherif" -m -p islam

3. Create a user account with the following attribute
   • Username: baduser
   • Full name/comment: Bad User
   • Password: baduser

         sudo useradd baduser -c "Bad User" -m -p baduser

5. Create a supplementary (Secondary) group called pgroup with group ID of 30000

         sudo groupadd -g 30000 pgroup

7. Create a supplementary group called badgroup

         sudo groupadd badgroup

9. Add islam user to the pgroup group as a supplementary group

         sudo usermod -aG pgroup Salma

11. Modify the password of islam's account to password

          sudo passwd Salma

13. Modify islam's account so the password expires after 30 days

          sudo chage -M 30 Salma

15. Lock bad user account so he can't log in

         sudo passwd -l baduser

17. Delete bad user account
    
         sudo userdel -r baduser

19. Delete the supplementary group called badgroup

         sudo groupdel badgroup

21. Create a folder called myteam in your home directory and change its permissions to read only for the owner.

          mkdir ~/myteam
          chmod 400 ~/myteam

23. Log out and log in by another user
25. Try to access (by cd command) the folder (myteam)

          
27. Using the command Line
    • Change the permissions of oldpasswd file to give owner read and write permissions and for group write and execute and execute only for the others (using chmod in 2 different ways)
    • Change your default permissions to be as above.
    • What is the maximum permission a file can have, by default when it is just created? And what is that for directory.
             666 read write not excute. (file)
             777 read write and excute  (Dir)
    • Change your default permissions to be no permission to everyone then create a directory and a file to verify.

            chmod u=rw,g=wx,o=x oldpasswd
            umask 0022   # Or whichever mask gives that result
            umask 0777
            touch testfile
            mkdir testdir
            ls -l testfile
            ls -ld testdir
    
29. Starting from your home directory, find all files that were modified in the last two day.

            find ~ -type f -mtime -2

31. Starting from /etc, find files owned by root user.

             find /etc -user root

33. Find all directories in your home directory.

             find ~ -type d

35. Write a command to search for all files on the system that, its name is ".profile".

             sudo find / -name .profile

37. Identify the file types of the following: /etc/passwd, /dev/pts/0, /etc, /dev/sda

               file /etc/passwd
               file /dev/pts/0
               file /etc
               file /dev/sda

39. List the inode numbers of /, /etc, /etc/hosts.

                ls -i /
                ls -i /etc
                ls -i /etc/hosts

41. Copy /etc/passwd to your home directory, use the commands diff and cmp, and Edit in the file you copied, and then use these commands again, and check the output.
    
                cp /etc/passwd ~/newone
               diff /etc/passwd ~/newone
               cmp /etc/passwd ~/newone
               echo "hi" >> ~/newone
               diff /etc/passwd ~/newone
               cmp /etc/passwd ~/newone

43. Create a symbolic link of /etc/passwd in /boot.
    
             sudo ln -s /etc/passwd /boot/passwd_symlink
45. Create a hard link of /etc/passwd in /boot. Could you? Why?
    
             sudo ln /etc/passwd /boot/hardlink
No - hardlink for dir only
