1. Project Workspace Setup

Command: mkdir ~/documents

Explanation: I used the mkdir command to create a new directory named "documents" in my home folder (~) to serve as the initial workspace for project files.
![alt text](<Screenshot 2026-01-04 123146.png>)

2. File Creation

Command: cd ~/documents && touch plan.txt

Explanation: I navigated into the newly created directory using cd and used the touch command to generate an empty file named plan.txt.
![alt text](<Screenshot 2026-01-04 123359.png>)

3. Content Addition

Command: echo "Project Alpha: Complete system audit by Friday." > plan.txt

Explanation: I used the echo command with the redirection operator > to write a project reminder into plan.txt. This replaced the empty file with a file containing my sample text.
![alt text](<Screenshot 2026-01-04 123714.png>)

4. File Metadata Verification

Command: ls -l plan.txt

Explanation: I ran ls -l to view the long-format metadata of the file. The output confirms the file permissions, that my user "codespace" is the owner, and the file size.
![alt text](<Screenshot 2026-01-04 123819.png>)

5. File Duplication

Command: cp plan.txt plan_copy.txt

Explanation: I used the cp (copy) command to create an exact duplicate of plan.txt named plan_copy.txt within the same directory.
![alt text](<Screenshot 2026-01-04 123913.png>)

6. Directory Renaming

Command: cd .. && mv documents project_documents

Explanation: I moved up one level and used the mv (move/rename) command to change the directory name from "documents" to "project_documents" to better reflect the project's scope.
![alt text](<Screenshot 2026-01-04 124014.png>)

7. Archival Structure

Command: mkdir project_documents/archive

Explanation: I used mkdir to create a new subdirectory named "archive" inside the project_documents folder to organize older versions of files.
![alt text](<Screenshot 2026-01-04 124131.png>)

8. File Organization

Command: mv project_documents/plan_copy.txt project_documents/archive/

Explanation: I used the mv command to move plan_copy.txt from the main project folder into the specific "archive" subdirectory I just created.
![alt text](<Screenshot 2026-01-04 124619.png>)

9. Recursive Listing

Command: ls -R project_documents

Explanation: I executed ls with the -R (recursive) flag. This allows the terminal to display every file and subdirectory within project_documents, showing the full hierarchy at once.
![alt text](<Screenshot 2026-01-04 124710.png>)

10. Path Verification

Command: realpath project_documents/archive/plan_copy.txt

Explanation: I used the realpath command to resolve and display the full absolute path of the moved file, starting from the root directory.
![alt text](<Screenshot 2026-01-04 124758.png>)
