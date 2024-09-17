Objective: Get the password that is preceeded with several '=' symbol.

Given: A file with filename 'data.txt' having content that contains both readable and non-readable to humans. The password for the next level is preceeded by multiple '=' symbol.

Methodology:

    1. Execute the command: sudo ssh bandit8@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit8: (From previous step). Once logged into bandit8, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find the data.txt file in the current directory.

    5. To display only the texts that are human readable, user would need to execute the command: strings data.txt

    6. After executing the previous command, the output of the terminal would only display the part of the content that are human readable.

    7. To narrow down the search for the password, user would have to use the output from the previous command as the input for the grep command with the search filter of several '=' symbol. To do this, user would have to execute the command: strings data.txt | grep '==========='

    8. The password for the next level would be the texts after the several '=' symbol. It is possible that the previous command would output a few lines, so user would have to determine which one of the lines is the password for the next level.


Password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*