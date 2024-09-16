Objective: Get the password that is located somewhere within the host server.

Given: Only the conditions of the file are given for this Level.

Conditions are:

    1. Owned by user bandit7

    2. Owned by group bandit6

    3. 33 bytes in size

Methodology:

    1. Execute the command: sudo ssh bandit6@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit6: (From previous step). Once logged into bandit6, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the command, user would find that there is no file or directory within the ~ directory.

    5. User would have to execute the command: cd / to change directory to the root folder.

    6. Once in root folder, user would need to execute the find command to locate the file that contains the password for the next level. The command to be executed is: find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null

        -type f:            Explicitly instructs the find command to only look for files and not directories
        -user bandit7:      Explicitly instructs the find command to only look for files that is owned by user bandit7
        -group bandit6:     Explicitly instructs the find command to only look for files that is also owned by group bandit6 on top of being owned by user bandit 7
        -size 33c:          Explicitly instructs the find command to only look for files that has size 33c
        2>/dev/null         This option will drop the results that indicates "Permission denied"

    7. The result of executing the previous command will show the complete path of the file that contains the password for the next level (/var/lib/dpkg/info/bandit7.password)

    8. Execute the cat command to display the password for the next level: cat /var/lib/dpkg/info/bandit7.password


Password: *morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj*