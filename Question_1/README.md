1. User Identity Verification

Command: whoami && groups

Explanation: I executed whoami to confirm my current username and groups to see which security groups my account is assigned to. I observed my username and the list of groups (docker) in the output.
![alt text](<Screenshot 2026-01-04 112613-2.png>)

2. Workspace Validation

Command: pwd && ls -l

Explanation: I used pwd to print the absolute path of my current directory and ls -l to view the files in long format, which shows permissions, owners, and timestamps.
![alt text](<Screenshot 2026-01-04 113340.png>)

3. Environment Confirmation File

Command: echo "Linux user environment verified" > user_info.txt

Explanation: I used the echo command combined with the > redirection operator to create a new file named user_info.txt containing the specified verification string.

4. File Integrity Check

Command: wc -c user_info.txt

Explanation: I ran the wc (word count) command with the -c flag to calculate and display the total number of characters in the user_info.txt file.
![alt text](<Screenshot 2026-01-04 115006.png>)

5. Learning the Tools

Command: man mkdir (Press q to exit the manual)

Explanation: I accessed the manual for mkdir. One useful option I found is -p, which allows the creation of parent directories if they do not already exist, preventing errors when creating nested folders.
![alt text](<Screenshot 2026-01-04 115230-1.png>)

6. Home Directory Inspection

Command: ls ~

Explanation: I used the ls command followed by the tilde (~) shortcut to view the contents of my home directory. The output shows pre-installed configuration folders such as java and nvm, which are part of the default GitHub Codespace environment.
![alt text](<Screenshot 2026-01-04 115714.png>)

7. Log Investigation

Running touch log.txt first to create the file.

Command: grep "admin" log.txt

Explanation: I used the grep command to search for the specific string "admin" within log.txt. Only lines containing that word were displayed in the terminal.
![alt text](<Screenshot 2026-01-04 121348.png>)

8. System Information Check

Command: uname -r

Explanation: I executed uname with the -r flag to extract and display the specific Linux kernel release version currently running on the system.
![alt text](<Screenshot 2026-01-04 121728.png>)

9. Network Connectivity Test

Command: ping -c 4 www.google.com

Explanation: I used the ping command to test the connection to Google's server. I used -c 4 to limit the test to four packets, observing successful replies (ICMP packets) and zero packet loss.
![alt text](<Screenshot 2026-01-04 122207.png>)

10. System Health Awareness

Command: uptime

Explanation: I ran the uptime command. The output shows how long the system has been running, how many users are logged in, and the "load average," which indicates the system's CPU demand over the last 1, 5, and 15 minutes.
![alt text](<Screenshot 2026-01-04 122329.png>)
