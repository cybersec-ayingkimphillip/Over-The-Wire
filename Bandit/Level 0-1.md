Objective: Locate the password to unlock level 1 host.

Given: Password for next level is found in a readme file located in the home directory.

Methodology:
```
    1. Execute command: _ssh bandit0@bandit.labs.overthewire.org -p 2220_
    2. Enter the password for the bandit0 user: _bandit0_
    3. Navigate to the home directory by executing the command: _cd ~/_
    4. Execute the command: _ls -l_ to show any directory and/or files inside the current directory.
    5. Execute the command: _cat readme_ to display the password for the next level.
```

Password: *ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If*