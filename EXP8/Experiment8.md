\# <h1 style="background-color: orange;"> EXPERIMENT 8 - Shell Programming</h1>

---------------------------------------------------------------------------

Name: Vivek Chauhan   SAP id:590029184    Date:29/09/2025



---------------------------------------------------------------------------

\## Aim

&nbsp;  \*\*To understand and demonstrate the concepts of process control and signals, process monitoring and resource usage, process communication and synchronization, background processes and job control, and system monitoring and logging in Linux\*\*



---------------------------------------------------------------------------

\## Tools \& Software Used 

\- \*\*Operating System:\*\* Ubuntu running on Oracle VirtualBox  

\- \*\*Terminal Emulator:\*\* GNOME Terminal 

\- \*\*Shell:\*\* Bash (\*Bourne-Again Shell\*)



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">Process Control \& signals</h1>

&nbsp;#### - `   kill   ` - used to terminate or send signals to processes

&nbsp;

&nbsp;#### Syntax:

&nbsp;````



&nbsp;  kill \[options] <PID>



&nbsp;````

&nbsp; #### Signals (used as options):

&nbsp;  1. `  2  ` - \*\*SIGINT\*\* (\*interrupt\*)

&nbsp;  2. `  15  ` - \*\*SIGTERM\*\* (\*termiante gracefully\*)

&nbsp;  3. `  9  ` - \*\*SIGKILL\*\* (\*force kill\*)

&nbsp;  4. `  19  ` - \*\*SIGSTOP\*\* (\*Stops a process\*)

&nbsp;  5. `  18  ` - \*\*SIGCONT\*\* (\*resumes the stopped process\*)



&nbsp;#### OUTPUT:



&nbsp;!\[output1](images/8011.png)



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">Process Monitoring and Resource Usage</h1>



&nbsp;#### Commands:

&nbsp;1. `   top    ` - \*\*live view of processes, CPU, memory\*\* <br><br>

&nbsp; #### OUTPUT:

&nbsp;!\[output2.1](images/8021.png)<br><br>



&nbsp;2. `   htop    ` - \*\*user friendly version of \*top\*\*\*

&nbsp; #### OUTPUT:

&nbsp; !\[putput2.2](images/8022.png)<br><br>



&nbsp;3. `   ps aux    ` - \*\*snapshot of all processes\*\*

&nbsp; #### OUTPUT:

&nbsp; !\[putput2.3](images/8023.png)<br><br>



&nbsp;4. `   free -h  ` - \*\*show memory usage\*\*

&nbsp;5. `   uptime    ` - \*\*system load averages\*\*

&nbsp; #### OUTPUT:

&nbsp; !\[putput2.4](images/802.4.png)<br><br>

&nbsp; 



&nbsp;---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">Process Communication</h1>

&nbsp;

\- \*\*Pipes `  |  ` - to pass output of one command to another\*\*



&nbsp;#### OUTPUT:

&nbsp;!\[output3](images/803.1.png)



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">Process Synchronization</h1>

&nbsp;#### To prevent conflicts, processes can be synchronized

&nbsp; - `   wait  ` - \*\*used to pause the execution of a script until all the background processes complete.\*\* <br><br>

&nbsp;  #### SCRIPT:

&nbsp;  !\[script1](images/8041.png)<br><br>

&nbsp;  #### OUTPUT:

&nbsp;  !\[output4.1](images/8042.png)<br><br>

&nbsp;  \[Click here to view the video of execution of this script](https://drive.google.com/file/d/1LOsI58G-r8eLXDoungNDWrgqMH2JQtpB/view?usp=sharing)<br><br>



&nbsp; - ` wait <PID> ` - \*\*waits for a particular job to finish\*\*<br><br>

&nbsp;  #### SCRIPT:

&nbsp;  !\[script2](images/8043.png)<br><br>



&nbsp;  #### OUTPUT:

&nbsp;  !\[output4.2](images/8044.png)<br><br>

&nbsp;  \[Click here to view the video of execution of this script](https://drive.google.com/file/d/16UXcwnN6zB618G496qq2eE8MwZdvArRB/view?usp=sharing)<br><br>



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">Background Process and Job control</h1>



&nbsp;1. `   \&   ` - \*\*used to run a process in background\*\*

&nbsp;2. `  jobs  ` - \*\*shows background jobs\*\*

&nbsp;3. `   fg %1   ` - \*\*brings job 1 to foreground\*\*

&nbsp;4. `   bg %1   ` - \*\*resume job 1 in background\*\*



&nbsp;#### OUTPUT:

&nbsp;!\[output5](images/805.1.png)



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">System Monitoring and logging</h1>



&nbsp;1. `  dmesg | less  ` - \*\*kernel/ system messages\*\*

&nbsp;  #### OUTPUT:

&nbsp;  !\[output6.1](images/8061.png)<br><br>

&nbsp;  !\[output6.2](images/8062.png)<br><br>





&nbsp;2. `  journalctl  ` - \*\*systemlogs\*\*

&nbsp;  #### OUTPUT:

&nbsp;  !\[output6.3](images/8063.png)<br><br>

&nbsp;

&nbsp;

&nbsp;3. `  last  ` - \*\*logged-in users\*\*

&nbsp;  #### OUTPUT:

&nbsp;  !\[output6.4](images/8064.png)<br><br>

&nbsp;

&nbsp;

&nbsp;4. `  who  `  or  `  w  ` - \*\*user currently logged-in\*\*

&nbsp; #### OUTPUT:

&nbsp; !\[output6.5](images/8065.png)





---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">LAB Exericeses</h1>

\### <h1 style="background-color: lightgreen;">TASK 1: Check File Permissions</h1>

\*\*Write a script that checks the file permissions of a given file and displays whether it is readable, writable, or executable by the current user.\*\*<br><br> 



&nbsp;  #### Script:

&nbsp;  !\[script3](images/807.png)<br><br>

&nbsp; 

&nbsp;  #### Output:

&nbsp;  !\[output7](images/808.png)<br><br>



\### <h1 style="background-color: lightgreen;">TASK 2: String Operations</h1>

\*\*Create a script that prompts the user to enter a string and then performs operations like string length, string concatenation, and string comparison.\*\*<br><br>

&nbsp;  #### Script:

&nbsp;  !\[script4](images/809.png)<br><br>

&nbsp; 

&nbsp;  #### Output:

&nbsp;  !\[output8](images/810.png)<br><br>



\### <h1 style="background-color: lightgreen;">TASK 3: Search for a Pattern in a file</h1>

\*\*Write a script that searches for a specific pattern in a given file and displays the matching lines.\*\*<br><br>

&nbsp;  #### Script:

&nbsp;  !\[script5](images/811.png)<br><br>

&nbsp; 

&nbsp;  #### Output:

&nbsp;  !\[output9](images/812.png)<br><br>



\### <h1 style="background-color: lightgreen;">TASK 4: Display System Information</h1>

\*\*Create a script that displays various system information like the current date and time, logged-in users, system uptime, etc.\*\*<br><br>

&nbsp;  #### Script:

&nbsp;  !\[script6](images/813.png)<br><br>

&nbsp; 

&nbsp;  #### Output:

&nbsp;  !\[output10](images/814.png)<br><br>



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">OBSERVATIONS</h1>



&nbsp;- `kill`, `wait` and job control commands (`\&`, `jobs`, `fg`, `bg`) worked as expected.



&nbsp;- `top`, `htop`, `ps aux`, and `free -h` provided real-time process and resource information.



&nbsp;- Pipes (`|`) enabled inter-process communication.



&nbsp;- System monitoring commands (`dmesg`, `journalctl`, `last`, `who`) displayed logs and user activity correctly.



&nbsp;- Lab exercises executed successfully with expected outputs.

&nbsp;

---------------------------------------------------------------------------

\## <h1 style="background-color: pink;"> CONCLUSION</h1> 



\- The experiment demonstrated process control, monitoring, communication, and synchronization in Linux.



\- Background job management and system monitoring help efficiently manage processes.



\- Shell scripting with process commands enables effective automation and resource tracking.



---------------------------------------------------------------------------

---------------------------------------------------------------------------

