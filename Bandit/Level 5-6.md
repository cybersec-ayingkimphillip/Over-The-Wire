Objective: Get the password from one of the files inside the *inhere* directory.

Given: There are multiple directories inside the *inhere* directory and the password for the next level is inside one of the multiple directories.

Conditions of the file that contains the password are the following:

    1. Human readable

    2. 1033 bytes in size

    3. Not executable

Methodology:

    1. Execute the command: sudo ssh bandit5@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit5: (From previous step). Once logged into bandit5, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find a directory with name inhere. To enter the inhere directory, user would need to execute the command: cd inhere

    5. Once inside the inhere directory, user would need to execute the command: ls -lah to show all files and/or directories within the current directory, including those files/directories that are hidden, their permissions level and displays the file size in a more understandable format.

    6. After executing the previous command, user would find several directories inside the inhere directory, and each directory contain several files that could contain the password for the next level.

    7. User would have to inspect each directory using the command: ls -lah ./maybehere** and look for a file that matches that matches the conditions 1033 bytes in size and not executable.

    8. Once user finds a file that matches the last 2 conditions, user can check if content of the file is human readable by executing the command: cat ./maybehere**/*file**


Password: *HWasnPhtq9AVKe0dmk45nxy20cvUa6EG*