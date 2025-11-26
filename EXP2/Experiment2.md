\# <h1 style="background-color: orange;">EXPERIMENT 2 - Linux File systems, Permissions \& Commands</h1>



-------------------------------------------------------------------------

Name: Vivek Chauhan   SAP id:590029184    Date:09/09/2025



--------------------------------------------------------------------------

\##  Aim

To understand the structure of the Linux file system, manage file permissions and ownership, and practice essential Linux commands.



---------------------------------------------------------------------------

\## Tools \& Software Used 

\- \*\*Operating System:\*\* Ubuntu running on Oracle VirtualBox  

\- \*\*Terminal Emulator:\*\* GNOME Terminal 

\- \*\*Shell:\*\* Bash (\*Bourne-Again Shell\*)



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">Linux File Systems </h1>

\- The Linux file system is a structured and hierarchical way of storing and organizing files and directories.

\- Linux treats everything as part of a single directory tree starting from the root directory `/`

\- To view all files and directories in the root `/` directory along with their details such as \*permissions\*, \*ownership\*, etc.

We can use the command

```

ls -l /

```

&nbsp;### Output:

&nbsp; !\[output](images/201.png) <br><br>



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">File Permissions and Ownership</h1>



\- Every file and directory in Linux has three types of permissions:

&nbsp; - `r` \*read\*

&nbsp; - `w` \*write\*

&nbsp; - `x` \*execute\*



\- Categories of Users:

&nbsp; - Owner

&nbsp; - Group 

&nbsp; - Others



\- Using the `ls -l` command to see the permission and ownership for a file `file1.txt`



&nbsp;### Output:

&nbsp;!\[output](images/202.png) <br><br>



---------------------------------------------------------------------------



\## <h1 style="background-color: pink;"> Modifying Permissions</h1>

&nbsp; ### Using the `chmod` command

\- To change the permission and make `myfile.txt` executable for the user, we can use the command

```

chmod u+x myfile.txt

```

&nbsp;### Output:

&nbsp;!\[Output](images/203.png)<br><br>

\- We can also change permissions using numeric mode 

```

chmod 744 myfile2.txt

chmod 754 myfile2.txt

```

&nbsp;### Output:

&nbsp;!\[Output](images/204.png)<br><br>



---------------------------------------------------------------------------



\## <h1 style="background-color: pink;">Basic Navigation Commands</h1>



\### 1. `ls` - List Directory content

\- `ls` - \*List files in current directory\*

\- `ls - l` - \*List with detailed information\*

\- `ls - a` - \*List all files using hidden ones\*

\- `ls - la` - \*Combined option for viewing detailed view with hidden files\*



&nbsp;### Output:

\- `ls`:

!\[Output](images/205.png) <br><br>



\- `ls -l`:

!\[Output](images/206.png) <br><br>



\- `ls -a`:

!\[Output](images/207.png) <br><br>



\- `ls -la`:

!\[Output](images/208.png) <br><br>



---------------------------------------------------------------------------

\### 2. `pwd` - Print working Directory

\- Shows your current location in the file.

&nbsp;### Output:

&nbsp;!\[Output](images/209.png) <br><br>



---------------------------------------------------------------------------

\### `cd` - Change Directory

\- `cd`- \*Go to home directory\*

\- `cd /home/vivekchauhan12/Downloads/lab2`- \*Go to a specific directory\*

\- `cd ..` - \*Go up one level\*

\- `cd -` - \*Go to previous directory\*

\- `cd /` - \*Go to root directory\*

&nbsp;#### Output:

&nbsp; !\[Output](images/210.png) <br><br>



---------------------------------------------------------------------------

\### 3. `mkdir` - Make a directory 

&nbsp;#### Syntax

&nbsp; ```

&nbsp; mkdir \[options] directory\_name

&nbsp; ```

\- \*\*Creating a single directory\*\*

&nbsp;  `mkdir directory\_name`<br><br>



\- \*\*Creating multiple directories at once\*\*

&nbsp;  `mkdir directory\_1 directory\_2 directory\_3`<br><br>



\- \*\*Creating nested directories\*\*

&nbsp;  `mkdir -p parent\_directory/child\_directory`<br><br>



\- \*\*Creating directory with special permissions\*\*

&nbsp;  `mkdir -m mode directory\_name`<br><br>



&nbsp;#### Output:

&nbsp;!\[Output](images/211.png) <br><br>



---------------------------------------------------------------------------

\### 4. `rmdir` - Remove Empty Directory

&nbsp;#### Syntax

&nbsp;```

&nbsp;rmdir \[options] directory\_name

&nbsp;```

\- \*\*Remove an empty directory\*\*

&nbsp;  `rmdir directory\_name`<br><br>



\- \*\*Remove multiple empty directories\*\*

&nbsp;  `rmdir directory\_1 directory\_2 directory\_3`<br><br>



\- \*\*Remove nested empty directories\*\*

&nbsp;  `rmdir -p parent\_directory/child\_directory`<br><br>



&nbsp;#### Output:

&nbsp; !\[output](images/212.png) <br><br>



---------------------------------------------------------------------------

\##  <h1 style="background-color: pink;">File Operations</h1>



&nbsp;### 1. `touch` - Creates files

&nbsp; -  The `touch` command is used to create empty files or to update timestamps of existing files. 

&nbsp; #### Syntax

&nbsp;  ```

&nbsp;   touch \[options] file\_name



&nbsp;  ```

&nbsp;  - \*\*Creating a single file\*\*

&nbsp;     `touch file\_name`<br><br>



&nbsp;  - \*\*Creating multiple files at once\*\*

&nbsp;     `touch file1\_name file2\_name file3\_name`<br><br>



&nbsp;  #### Output:

&nbsp;  !\[output](images/213.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### 2. `cp` - Copying files and directories

&nbsp; 

&nbsp; - The `cp` command is used to copy files from one location to another.  

&nbsp; #### Syntax 

&nbsp; ```

&nbsp; cp \[options] source destination

&nbsp; ```

&nbsp; - \*\*Copy a single file\*\* - Copies the content of the source file to the destination file.

&nbsp;   `cp source\_file destination\_file`<br><br>

&nbsp; 

&nbsp; - \*\*Copy multiple files to a directory\*\* - Copies all the files to the given destination directory at once.

&nbsp;   `cp source\_files destination\_directory\_path`<br><br>



&nbsp; - \*\*Copy a directory recursively\*\* - Copy all the files and subdirectories of the source directory to the destination directory.

&nbsp;   `cp -r \[source] \[destination]`<br><br>

&nbsp; 

&nbsp; - \*\*Copy and show details\*\* - Display each file being copied.

&nbsp;   `cp -v \[source] \[destination]`<br><br>



&nbsp; - \*\*Copy with confirmation\*\* - prompts for confirmation before overwriting a file.

&nbsp;   ` cp -i \[source] \[destination]`<br><br>



&nbsp; #### Output:

&nbsp; !\[Output](images/214.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### 3. `mv` - Move and rename

&nbsp; - `mv` command is used to move files and directories from one place to another.

&nbsp; 

&nbsp; #### Syntax 

&nbsp; ```

&nbsp;  mv \[options] source destination

&nbsp; ```

&nbsp; - \*\*Move file to different directory\*\*

&nbsp;   `mv source\_file destination\_directory`<br><br>

&nbsp; 

&nbsp; - \*\*Move multiple files\*\*

&nbsp;   ` mv source\_files destination\_directory`<br><br>



&nbsp; - \*\*Rename a file\*\*

&nbsp;   ` mv old\_name new\_name`<br><br>

&nbsp; 

&nbsp; - \*\*Rename a directory\*\*

&nbsp;   ` mv old\_name new\_name`<br><br>



&nbsp; #### Output:

&nbsp; !\[output](images/215.png) <br><br>



---------------------------------------------------------------------------

&nbsp;### 4. `rm` - Remove files and directories

&nbsp; - `rm` command is used to remove files permanently.

&nbsp;

&nbsp; #### Syntax

&nbsp; ```

&nbsp; rm \[options] file\_name

&nbsp; ```

&nbsp; - \*\*Remove a file\*\*

&nbsp;   `rm file\_name` <br><br>



&nbsp; - \*\*Remove multiple files\*\*

&nbsp;   ` rm file\_names` <br><br>

&nbsp;

&nbsp; - \*\*Remove directory and its content\*\*

&nbsp;   ` rm -r directory\_name` <br><br>



&nbsp; - \*\*Forced removal without confirmation\*\*

&nbsp;   ` rm -f file\_name` <br><br>



&nbsp; - \*\*Confirmable removal\*\*

&nbsp;  ` rm -i file\_name` <br><br>



&nbsp; #### Output:

&nbsp; !\[output](images/216.png) <br><br>



---------------------------------------------------------------------------

\##  <h1 style="background-color: pink;">File viewing and Editing</h1>



&nbsp;### 1. `cat` - Used for viewing, creating and merging files

&nbsp; - The `cat` command is used to display the content of files, create new files or combine multiple files.

&nbsp; 

&nbsp; #### Syntax

&nbsp; ```

&nbsp; cat \[options] file\_name

&nbsp; ```



&nbsp; - \*\*To display the content of files\*\*

&nbsp;   `cat file\_name` <br><br>

&nbsp; 

&nbsp; - \*\*To display multiple files together\*\*

&nbsp;   ` cat file\_names` <br><br>

&nbsp; 

&nbsp; - \*\*To create a new file\*\*

&nbsp;   ` cat > file\_name` <br><br>



&nbsp; - \*\*Merging files into a new file\*\*

&nbsp;   ` cat file1 file2 > file\_name` <br><br>

&nbsp; 

&nbsp; - \*\*To display all output lines with numbers\*\*

&nbsp;   ` cat -n file\_name` <br><br>



&nbsp;  - \*\*To display all non-empty output lines with numbers\*\*

&nbsp;   ` cat -b file\_name` <br><br>



&nbsp; #### Output:

&nbsp; !\[output](images/217.png)<br><br>

&nbsp; !\[output](images/218.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### 2. `head` - Viewing the beginning of files

&nbsp; - The `head` command is used to view the first few lines of a file.



&nbsp; #### Syntax 

&nbsp; ```

&nbsp; head \[options] file\_name

&nbsp; ```



&nbsp; - \*\*To display the first 10 lines of a file (\*default\*)\*\*

&nbsp;   ` head file\_name`<br><br>

&nbsp; 

&nbsp; - \*\*To display the first 5 lines\*\*

&nbsp;   `head -n 5 file\_name`<br><br>

&nbsp; 

&nbsp; - \*\*To display the first 20 bytes of a file\*\*

&nbsp;   ` head -c 20 file\_name`<br><br>



&nbsp; #### Output:

&nbsp; !\[Output](images/219.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### 3. `tail` - Viewing the end of files

&nbsp; - The `tail` command is used to view the last few lines of a file.



&nbsp; #### Syntax

&nbsp; ```

&nbsp; tail \[options] file\_name

&nbsp; ```

&nbsp; - \*\*To display the last 10 lines of a file (\*default\*)\*\*

&nbsp;   ` tail file\_name`<br><br>

&nbsp; 

&nbsp; - \*\*To display the last 5 lines of a file (\*default\*)\*\*

&nbsp;   ` tail -n 5 file\_name`<br><br>



&nbsp; - \*\*To display the last 20 bytes of a file\*\*

&nbsp;   ` tail -c 20 file\_name`<br><br>

&nbsp; 

&nbsp; - \*\*To monitor a file in real time\*\*

&nbsp;   ` tail -f file\_name` <br><br>



&nbsp; #### Output:

&nbsp; !\[output](images/220.png)<br><br>

&nbsp; !\[output](images/221.png)<br><br>



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;"> Text editors</h1>

&nbsp;### 1. Nano

&nbsp; - NANO is a text editor that works directly from the terminal, useful for creating and editing files.

&nbsp; 

&nbsp; #### Output:

&nbsp;  !\[output](images/222.png)<br><br>

&nbsp;  !\[output](images/223.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### 2. Vim

&nbsp; - VIM is an advanced text editor with features like syntax highlighting, efficient navigation and powerful editing commands.



&nbsp; #### OUTPUT:

&nbsp;  !\[output](images/224.png)<br><br>

&nbsp;  !\[output](images/225.png)<br><br>



---------------------------------------------------------------------------



\## <h1 style="background-color: pink;"> User Management</h1>

&nbsp;### 1. `whoami` - Display the current username 



&nbsp;### 2. `who` - Display all users currently logged into the system



&nbsp;### 3. `passwd` - To change user password



&nbsp;### 4. `sudo ` - To run commands with administrative privileges

&nbsp; -For tasks like updating and installing packages or editing system files, the `sudo` command is used

&nbsp; - `sudo` grants root privileges to the user to run commands.

&nbsp; #### Syntax

&nbsp;  ```

&nbsp;   sudo command

&nbsp;  ```

&nbsp; 

&nbsp;### OUTPUT:

&nbsp; !\[output](images/226.png)

&nbsp; !\[output](images/227.png)<br><br>



---------------------------------------------------------------------------

&nbsp; 

&nbsp;## <h1 style="background-color: pink;"> System Information</h1>

&nbsp; ### 1.`uname` - To display details about Linux system



&nbsp;  #### Syntax

&nbsp;  ```

&nbsp;   uname \[options]

&nbsp;  ```

&nbsp;  - \*\*To display basic system info\*\*

&nbsp;    `uname`<br><br>

&nbsp;   

&nbsp;  - \*\*To display all system info\*\*

&nbsp;    `uname -a`<br><br>



&nbsp;  - \*\*To display kernel version\*\*

&nbsp;    `uname -r`<br><br>



&nbsp;  - \*\*To display machine hardware info\*\*

&nbsp;    `uname -m`<br><br>



&nbsp;  - \*\*To display OS info\*\*

&nbsp;    `uname -o`<br><br>



&nbsp;  #### OUTPUT:

&nbsp;  !\[output](images/228.png)<br><br>



---------------------------------------------------------------------------

&nbsp; ### 2.`df` - To display the information about disk space usage

&nbsp;  

&nbsp;  #### Syntax

&nbsp;  ```

&nbsp;  df \[options] \[file\_systems]

&nbsp;  ```

&nbsp;  - \*\*To display basic disk usage\*\*

&nbsp;   `df`<br><br>



&nbsp;  - \*\*To display disk usage in human human-readable format\*\*

&nbsp;   `df -h`<br><br>



&nbsp;  - \*\*To display file system type\*\*

&nbsp;   `df -T`<br><br>

&nbsp; 

&nbsp;  #### OUTPUT:

&nbsp;  !\[output](images/229.png)<br><br>



---------------------------------------------------------------------------



&nbsp; ### 3.`top` - shows real-time information 

&nbsp;  - `top` shows real-time info about processes, CPU usage, memory usage and other system resources



&nbsp; ### OUTPUT:

&nbsp;  !\[output](images/230.png)<br><br>



---------------------------------------------------------------------------

&nbsp; ### 4. `history` - shows a list of commands that have been executed in the terminal



&nbsp;  #### Syntax 

&nbsp;  ```

&nbsp;  history

&nbsp;  ```

&nbsp;  - \*\*To display command history\*\*

&nbsp;    `history`<br><br>



&nbsp;  - \*\*To display last n commands\*\*

&nbsp;    `history n`<br><br>



&nbsp;  - \*\*To search history\*\*

&nbsp;    `history | grep "search\_term"` <br><br>

&nbsp;  

&nbsp;  - \*\*Execute previous command\*\*

&nbsp;    `!!<br><br>



&nbsp;  #### OUTPUT:

&nbsp;  !\[output](images/231.png)<br><br>



---------------------------------------------------------------------------

\## <h1 style="background-color: pink;">EXERCISES</h1>

&nbsp;### Exercise 1 - File system navigation<br><br>

&nbsp; !\[output](images/232.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### Exercise 2 - File operations and permissions<br><br>

&nbsp; !\[output](images/233.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### Exercise 3 - Text Editing and viewing<br><br>

&nbsp; !\[output](images/234.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### Exercise 4 - System exploration<br><br>

&nbsp; !\[output](images/235.png)<br><br>



---------------------------------------------------------------------------

&nbsp;### Exercise 5 - Cleanup <br><br>

&nbsp;!\[output](images/236.png)<br><br>



---------------------------------------------------------------------------

\##  <h1 style="background-color: orange;"> OBERVATIONS</h1>

&nbsp;

&nbsp;- The Linux file system structure was explored using commands.



&nbsp;- File permissions and ownership were checked and modified.



&nbsp;- Directories were navigated, and file operations were performed.



&nbsp;- File contents were viewed and edited with text editors.



&nbsp;- User management tasks were carried out using appropriate commands.



&nbsp;- System information and resource usage were monitored during the experiment.



-----------------------------------------------------------------------------



\##  <h1 style="background-color: orange;"> CONCLUSION</h1>

&nbsp;The experiment provided practical experience in using various Linux commands related to file systems, permissions, navigation, file operations, editing, user management, and system monitoring.



------------------------------------------------------------------------------

