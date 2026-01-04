1. System Uptime Verification

Command: uptime -p

Explanation: I used the uptime command with the -p flag to display the system's "pretty" uptime. This tells me exactly how many hours and minutes have passed since the lab machine was last started.
![alt text](<Screenshot 2026-01-04 142008.png>)

2. User Process Listing

Command: ps -u $USER

Explanation: I executed ps with the -u flag followed by the $USER variable to list every active process currently owned by my account. This shows process IDs (PIDs) and the specific commands running.
![alt text](<Screenshot 2026-01-04 142119.png>)

3. CPU Usage Analysis

Command: ps -u $USER --sort=-%cpu | head -n 5

Explanation: I used the ps command sorted by CPU percentage in descending order. By piping this into head, I identified the top 5 processes consuming the most processing power under my user.
![alt text](<Screenshot 2026-01-04 142304.png>)

4. Background Process Execution

Command: sleep 500 & jobs

Explanation: I started a sleep command and added the & symbol to push it into the background. I then immediately ran jobs to verify that the process was indeed running in the background without blocking my terminal.
![alt text](<Screenshot 2026-01-04 142356.png>)

5. Process Priority Management

Command: renice +10 -u $USER

Explanation: I used the renice command to change the "niceness" value of my user's processes to +10. This lowers the priority of my tasks, allowing other system processes more CPU access if needed.
![alt text](<Screenshot 2026-01-04 144048.png>)

6. Memory Usage Monitoring

Command: free -h

Explanation: I ran the free command with the -h flag to display total, used, and available RAM in a human-readable format (Gigabytes). This helps in monitoring if the system is running low on memory.
![alt text](<Screenshot 2026-01-04 144139.png>)

7. Disk Space Inspection

Command: df -h .

Explanation: I used df -h on the current directory (.) to check the disk space of the specific partition where my home files are stored. It shows the total size, used space, and percentage used
![alt text](<Screenshot 2026-01-04 144237.png>)

8. Shell Identification

Command: echo $SHELL

Explanation: I used echo to print the value of the $SHELL environment variable. The output confirms that I am currently using the /bin/bash shell environment.
![alt text](<Screenshot 2026-01-04 144326.png>)

9. Output Redirection

Command: lscpu > system_report.txt

Explanation: I executed the lscpu command to gather CPU architecture details and used the > operator to save all that information into a file named system_report.txt.
![alt text](<Screenshot 2026-01-04 144415.png>)

10. Disk Usage Visualization

Command: ncdu ~

Explanation: I used ncdu to open an interactive disk usage analyzer for my home directory. It provides a visual, navigable list of folders and files, ranked by size, making it easy to see what is consuming the most disk space.
![alt text](<Screenshot 2026-01-04 144635.png>)
