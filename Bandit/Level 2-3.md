Objective: Get the password from a file with a filename that has spaces in it.

Given: A file with a filename that has spaces in it.

Methodology:
    
    1. Execute the command: sudo ssh bandit2@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit2: (From previous step). Once logged into bandit2, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After the previous command is executed, user will find a file with a filename 'spaces in this filename'. To read the content of this file, user would have to execute the command: cat 'spaces in this filename', which is also the password for the next level.


Password: *MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx*