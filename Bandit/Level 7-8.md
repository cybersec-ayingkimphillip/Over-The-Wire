Objective: Get the password that is beside the word "millionth".

Given: A file with filename data.txt that contains 2 columns. The left column contains common words and the right column contains passwords paired to the common words. The password for the next level is the password paired with the common word "millionth".

Methodology:

    1. Execute the command: sudo ssh bandit7@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit7: (From previous step). Once logged into bandit7, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find the data.txt file in the current directory.

    5. To get the password for the next level, user would need to execute the command: cat data.txt | grep 'millionth'

        cat data.txt:       Executing this command will display the content of file to the terminal screen
        |:                  Having this symbol at the end of the cat command will cause the terminal not to display the content of the file but rather pass the content to the command at the right of the | symbol.
        grep 'millionth':   Executing this command will cause the terminal to display only the line that contains the word 'millionth'. With this, the password for the next level is the password next to the word 'millionth'


Password: *dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc*