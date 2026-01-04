1. File Creation

Command: echo "Linking and Inode Lab Data" > ~/sample_data.txt

Explanation: I used the echo command to create a file named sample_data.txt in my home directory with some sample text to serve as our base file.
![alt text](<Screenshot 2026-01-04 133222.png>)

2. Hard Link Creation

Command: ln ~/sample_data.txt ~/sample_hard.txt

Explanation: I used the ln command to create a hard link. This creates a new filename pointing to the exact same physical data on the disk as the original file.
![alt text](<Screenshot 2026-01-04 133327.png>)

3. Symbolic Link Creation

Command: ln -s ~/sample_data.txt ~/sample_soft.txt

Explanation: I used the ln -s command to create a symbolic link (soft link). Unlike a hard link, this is a special file that acts as a shortcut pointing to the path of the original file.
![alt text](<Screenshot 2026-01-04 133422.png>)

4. Inode Verification

Command: ls -i ~/sample_data.txt ~/sample_hard.txt ~/sample_soft.txt

Explanation: I used the ls -i command to display the inode numbers (the unique index ID on the disk) for all three files.
![alt text](<Screenshot 2026-01-04 133515.png>)

5. Inode Analysis

Noticing that sample_data.txt and sample_hard.txt have the exact same inode number, while sample_soft.txt has a different one.

Explanation: The original file and the hard link share an inode because they both point to the same physical data. The symbolic link has a different inode because it is a separate file that merely stores the text of a file path.
![alt text](<Screenshot 2026-01-04 133515-1.png>)

6. File Metadata Inspection

Command: stat ~/sample_data.txt

Explanation: I used the stat command to view comprehensive metadata, including access/modify/change timestamps and the exact number of links pointing to the file.
![alt text](<Screenshot 2026-01-04 133846.png>)

7. Disk Usage Check

Command: du -sh ~

Explanation: I used du (disk usage) with the -s (summary) and -h (human-readable) flags to see the total size of my home directory in Megabytes or Gigabytes.
![alt text](<Screenshot 2026-01-04 133950.png>)

8. File Size Overview

Command: ls -lh ~

Explanation: I used ls -lh to list all files in the home directory. The -h flag converts the file sizes into a format that is easy to read (e.g., 2K, 4M).
![alt text](<Screenshot 2026-01-04 134047.png>)

9. Link Deletion Test

Command: rm ~/sample_soft.txt && cat ~/sample_data.txt

Explanation: I deleted the symbolic link using rm and then used cat to read the original file. This proves that deleting a soft link does not affect the source data.
![alt text](<Screenshot 2026-01-04 134207.png>)

10. Disk Utility Demonstration

Command: du -h --max-depth=1 ~ && df -h

Explanation: I used du -h --max-depth=1 to see the size of each folder in my home directory and df -h to see the total available space on the entire system's disk partitions.
![alt text](<Screenshot 2026-01-04 134412.png>)
