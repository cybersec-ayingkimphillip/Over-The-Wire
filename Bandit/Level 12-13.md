Objective: Get the password from a hexdump file that has been repeatedly compressed.

Given: A hexdump file located in the home directory.

Hint: Create a temporary directory within the /tmp directory.

Methodology:

    1. Execute the command: sudo ssh bandit12@bandit.labs.overthewire.org -p 2220

    2. Enter the password for bandit12: (From previous step). Once logged into bandit12, user is automatically in ~ directory.

    3. Execute the command: ls -l to check the files and/or directories inside the current directory.

    4. After executing the previous command, user will find the data.txt file in the current directory. This file is a hexdump file.

    5. Navigate into the /tmp directory using the command: cd /tmp and create a temporary directory using the command: mktemp -d. This will create a temporary directory with random characters.

    6. Navigate into this temporary directory (cd /tmp/*name of temporary directory*) and copy the data.txt file from the ~ directory to the current one using command: cp ~/data.txt /tmp/*name of temporary directory*

    7. Once data.txt file is copied into the current directory, it is advised for user to rename the file for better file representation. In this case, the data.txt file was renamed to hexdump_data by executing the command: mv data.txt hexdump_data

    8. Because a hexdump file cannot be decompressed, user would have to create another file where the content is the reversing of the hexdump process of the hexdump_data file. This is achieved by executing the command: xxd -r hexdump_data > compressed_data

    9. The compressed_data file can now be de-compressed using de-compression softwares.

    10. To know which de-compression software to use, user would need to identify some clues within the compressed_data file by executing the command: xxd compressed_data

        10a. If the first row of the output contains "1f8b 0808" in the second and third column, the de-compression software to use is gzip.

        10.b If the first row of the output contains "425a" in the second column and "BZ..." in the last column, the de-compression software to use is bzip2.

    11. After identifying the de-compression software to use, user would need to rename the compressed_data file by adding a file extension that would match the de-compression software. If the de-compression software to use is gzip, then the compressed_data file would have to be renamed to compressed_data.gz, and if the de-compression software to use is bzip2, then the compressed_data file would have to be renamed to compressed_data.bz2.

    12a. To de-compress using gzip, user would execute the command: gzip -d compressed_data.gz

    12b. To de-compress using bzip2, user would execute the command: bzip2 -d compressed_data.bz2

    13. Because it was compressed multiple times, the compressed_data would have to be de-compressed multiple times as well. To this end, steps 10-12 would need to be repeated a few more times.

    14. After multiple de-compressions, a file with a .bin extension is seen on the last column of the compressed_data file after executing the command: xxd compressed_data.

    15. This file would have to be extracted by adding a .tar extension to the compressed_data file. 
    
    16. Extraction is done by first executing the command: mv compressed_data compressed_data.tar to rename the file and secondly, execute the command: tar -xf compressed_data.tar to extract the file with the .bin extension.

    17. After extraction, the file with the .bin extension would have to be subjected to Steps 10-16 to extract other files with .bin extension.

    18. When running the command: xxd *name of file*.bin and the last column shows content that is human readable, user is advised to execute the command: cat *name of file*.bin to check and get the password.

Password: *FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn*