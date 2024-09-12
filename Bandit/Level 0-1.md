Objective: Locate the password to unlock level 1 host.
Given: Password for next level is found in a readme file located in the home directory.

Methodology:
    1. Execute command: ssh bandit0@bandit.labs.overthewire.org -p 2220
    2. Enter the password for the bandit0 user: bandit0.
    3. Navigate to the home directory by executing the command: cd ~/
    4. Execute the command: ls -l to show any directory and/or files inside the current directory.
    5. Execute the command: cat readme to display the password for the next level.

Password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If