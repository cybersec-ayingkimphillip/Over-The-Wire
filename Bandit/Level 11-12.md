Objective: Solve the Caesar Cipher puzzle to get the password.

Given: A file that contains data that has been rotated 13 times from their original positions.

Methodology:

    1. Execute the command: sudo ssh bandit11@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit11: (From previous step). Once logged into bandit11, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find the data.txt file in the current directory.

    5. Since it is known that the letters are rotated 13 times from their original position, user would have to execute the tr command and put the letters back in their original place.

    6. To do #5, user would have to execute the cat command to display the data that were rotated and use this output as an input for the tr command.
    Command: cat data.txt | tr '[N-ZA-Mn-za-m]' '[A-Za-z]'

    7. The first set of brackets after the tr command informs the system that the letter schema after the letters are rotated 13 times, while the second set of brackets instructs the system to set the letters back to its original place.


Password: *7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4*