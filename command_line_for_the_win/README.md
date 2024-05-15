# Command line for the win
* Using SFTP File Transfer .

***step 1: Open a Terminal***

Open a terminal window on your local machine. You can typically find the terminal application in your system's applications or utilities.

***step 2: Connect to the Remote Server***

Use the sftp command to connect to the remote server. Replace <username> with your actual username and <hostname> with the server's hostname or IP address:

bash
Copy code
sftp <username>@<hostname>
For example:

bash
Copy code
sftp john@example.com
If the server uses a non-standard port (not 22), you can specify it with the -P option:

bash
Copy code
sftp -P 2222 <username>@<hostname>

***step 3: Authenticate***

You will be prompted for your password. Enter your password to authenticate, or if you're using SSH key-based authentication, make sure your SSH key is correctly configured and added to the ~/.ssh/authorized_keys file on the remote server.

***step 4: Navigate to the Remote Directory***

You will be in the SFTP prompt, similar to a regular shell prompt. You can navigate to the directory on the remote server where you want to transfer files using standard Unix navigation commands such as cd, ls, and pwd. For example:

bash
Copy code
cd /path/to/remote/directory

***tep 5: Upload a File***

To upload a file from your local machine to the remote server, use the put command. Replace <local_file> with the full path to the local file and <remote_file> with the desired filename on the remote server:

bash
Copy code
put <local_file> <remote_file>
For example:

bash
Copy code
put localfile.txt remotefile.txt

***step 6: Download a File***

To download a file from the remote server to your local machine, use the get command. Replace <remote_file> with the full path to the file on the remote server and <local_file> with the desired filename on your local machine:

bash
Copy code
get <remote_file> <local_file>
For example:

bash
Copy code
get remotefile.txt localfile.txt
Step 7: Exit SFTP

When you're done transferring files, you can exit the SFTP session by typing exit or quit:

bash
Copy code
exit
