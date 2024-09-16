Objective: Get the password from a file that is hidden within a directory.

Given: A directory with name *inhere*

Methodology:

    1. Execute the command: sudo ssh bandit3@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit3: (From previous step). Once logged into bandit3, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find a directory with name inhere. To enter the inhere directory, user would need to execute the command: cd inhere

    5. Once inside the inhere directory, user would need to execute the command: ls -la to show all files and/or directories within the current directory, including those files/directories that are hidden.

    6. After executing the previous command, the file with filename ...Hidden-From-You is shown in the list.

    7. Execute the command: cat ...Hidden-From-You to display the content of the file, which is also the password for the next level.


Password: *2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ*