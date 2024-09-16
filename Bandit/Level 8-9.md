Objective: Get the password from the file data.txt and it is the only unique password of the file.

Given: A file with filename data.txt contains a several passwords and all are repeating except a unique one.

Methodology:

    1. Execute the command: sudo ssh bandit8@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit8: (From previous step). Once logged into bandit8, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find the data.txt file in the current directory.

    5. To get the password for the next level, execute the following command: sort data.txt | uniq -u

        sort data.txt:      Executing this command will sort all the content of the file alphabetically and numerically.
        |:                  This symbol will send the output of the previous command to be the input of the following command.
        uniq -u:            Executing this command will display the only unique line.


Password: *4CKMh1JI91bUIZZPXDqGanal4xvAg0JM*