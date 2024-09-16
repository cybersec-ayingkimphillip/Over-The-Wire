Objective: Get the password from one of the files inside the *inhere* directory. The password is the only human readable content in one of the files.

Given: A directory with name *inhere* that contains several files. One of the files contain the only human readable content, which is the password for the next level.

Methodology:

    1. Execute the command: sudo ssh bandit4@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit4: (From previous step). Once logged into bandit4, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find a directory with name inhere. To enter the inhere directory, user would need to execute the command: cd inhere

    5. Once inside the inhere directory, user would need to execute the command: ls -la to show all files and/or directories within the current directory, including those files/directories that are hidden as well as their permissions level.

    6. After executing the previous command, user would find several files that contain dash in their filenames.

    7. To read the content inside the files, user would have to use the escape characters ./ in order for the - to be ignored as a command option. This is done by executing the command: cat ./-file00 and so on until the only human readable content is found in one of the files.


Password: *4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw*