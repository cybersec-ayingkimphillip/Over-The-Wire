Objective: Get the password from a file with a dash as a filename.

Given: A file with a dash filename.

Methodology:

    1. Execute the command: sudo ssh bandit1@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit1: (From previous step). Once logged into bandit1, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After the previous command is executed, user will find out that the current directory contains a file with a dash filename. To read the contet of this file, the user will execute the command: cat ./- , which is also the password for the next level.

    5. The characters ./ before the - when executing the command: cat ./- are escape characters in order for - to be ignored as a command option.


Password: *263JGJPfgU6LtdEvgfWU1XP5yac29mFx*