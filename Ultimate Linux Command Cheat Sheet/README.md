# Linux Command Cheat Sheet

![linux cmd](linux-commands.png)

## Basic Linux commands


| CMD  | Description  |
|:---|:---|
| ls  | Lists all files and directories in the present working directory
| ls-R |	Lists files in sub-directories as well 
|ls-|	Lists hidden files as well
|ls-al|	Lists files and directories with detailed information like permissions,size, owner, etc.
|cd or cd ~|	Navigate to HOME directory
|cd ..|	Move one level up
|cd|	To change to a particular directory
|cd /|	Move to the root directory
|cat > filename|	Creates a new file
|cat filename|	Displays the file content
|cat file1 file2 > file3|	Joins two files (file1, file2) and stores the output in a new file (file3)
|mv file "new file path"|	Moves the files to the new location
|mv filename new_file_name|	Renames the file to a new filename
|sudo|	Allows regular users to run programs with the security privileges of the superuser or root
|rm filename|	Deletes a file
|man|	Gives help information on a command
|history|	Gives a list of all past commands typed in the current terminal session
|clear|	Clears the terminal
|mkdir directoryname|	Creates a new directory in the present working directory or a at the specified path
|rmdir|	Deletes a directory
|mv|	Renames a directory
|pr -x|	Divides the file into x columns
|pr -h|	Assigns a header to the file
|pr -n|	Denotes the file with Line Numbers
|lp -nc , lpr c|	Prints "c" copies of the File
|lp-d lp-P| 	Specifies name of the printer
|apt-get| 	Command used to install and update packages
|mail -s 'subject' -c 'cc-address'   -b 'bcc-address' 'to-address'| 	Command to send email
|mail -s "Subject" to-address < Filename| 	Command to send email with attachment|

<br />

## File Permission commands


| CMD  | Description  |
|:---|:---|
|ls-l|	To show file type and access permission
|r|	Read permission
|w|	Write permission
|x|	Execute permission
|-=|	No permission
|Chown user|	For changing the ownership of a file/directory
|Chown user:group filename|	Change the user as well as group for a file or directory
|chown [user] [file_name]| The ownership of the file called file_name is assigned or changed to a new owner called user.
|chmod -c -R|	Assign a file the read, write, and execute permissions.
|touch -a -t|	Useful in creating or modifying a file timestamp.
|chown -c -R|	Useful in changing the ownership of an assigned or owned file.
|chmod 775 file_name|Change mode of file to 775 [More Details](https://technicalmasterblog.wordpress.com/2019/02/23/what-does-chmod-775-mean/)
|chmod 777 file_name|	Everyone access the file called file_name will have read, write, and execute permissions.
|chmod 755 file_name|	The owner of the file called file_name will have read, write, and execute permissions while other users will only have read and execute permissions.
|chmod 766 file_name|The owner of the file called file_name has complete access to it while group and other users can only read and execute.
|chmod -R 600 folder|Recurs­ively chmod folder to 600

<br />

## Environment Variables command


| CMD  | Description  |
|:---|:---|
|echo $VARIABLE| To display value of a variable
|env|	Displays all environment variables
|VARIABLE_NAME= variable_value|	Create a new variable
|Unset|	Remove a variable
|export Variable=value|	To set value of an environment variable|

<br />

## User management commands of linux


| CMD  | Description  |
|:---|:---|
|sudo adduser username|	To display value of a variable
|sudo passwd -l 'username'|	Displays all environment variables
|sudo userdel -r 'username'|	Create a new variable
|sudo usermod -a -G GROUPNAME USERNAME|	Remove a variable
|sudo deluser| USER GROUPNAME	To set value of an environment variable
|finger|	Gives information on all logged in user
|finger username|	Gives information of a particular user

<br />

## Networking command


| CMD  | Description  |
|:---|:---|
|SSH username@ip-address or hostname| Login into a remote Linux machine using SSH
|Ping hostname="" or =""|	To ping and Analyzing network and host connections
|dir| Display files in the current directory of a remote computer
|cd "dirname"|	Change directory to "dirname" on a remote computer
|put file|	Upload 'file' from local to remote computer
|get file|	Download 'file' from remote to local computer
|quit|	Logout


<br />


## Process command


| CMD  | Description  |
|:---|:---|
|bg| To send a process to the background
|fg|	To run a stopped process in the foreground
|top|	Details on all Active Processes
|ps|	Give the status of processes running for a user
|ps PID|	Gives the status of a particular process
|pidof|	Gives the Process ID (PID) of a process
|kill PID|	Kills a process
|nice|	Starts a process with a given priority
|renice|	Changes priority of an already running process
|df|	Gives free hard disk space on your system
|free|	Gives free RAM on your system


<br />

## VI Editing Commands


| CMD  | Description  |
|:---|:---|
|i|	Insert at cursor (goes into insert mode)
|a|	Write after cursor (goes into insert mode)
|A|	Write at the end of line (goes into insert mode)
|ESC|	Terminate insert mode
|u|	Undo last change
|U|	Undo all changes to the entire line
|o|	Open a new line (goes into insert mode)
|dd|	Delete line
|3dd|	Delete 3 lines
|D|	Delete contents of line after the cursor
|C|	Delete contents of a line after the cursor and insert new text. Press ESC key to end insertion.
|dw|	Delete word
|4dw|	Delete 4 words
|cw|	Change word
|x|	Delete character at the cursor
|r|	Replace character
|R|	Overwrite characters from cursor onward
|s|	Substitute one character under cursor continue to insert
|S|	Substitute entire line and begin to insert at the beginning of the line
|~|	Change case of individual character|

<br />

## Search Files

| CMD  | Description  |
|:---|:---|
|grep pattern files| Search for pattern in files
|grep -i| Case insens­itive search
|grep -r| Recursive search
|grep -v| Inverted search
|grep -o| Show matched part of file only
|find /dir/ -name name*| Find files starting with name in dir
|find /dir/ -user name| Find files owned by name in dir
|find /dir/ -mmin num| Find files modifed less than num minutes ago in dir
|whereis [options] filename...| Used to find the location of source/binary file of a command and manuals sections for a specified file in Linux system [More Details](https://www.geeksforgeeks.org/whereis-command-in-linux-with-examples/)
|Find file| (quick search of system index)|

<br />

## Archives and File Compression
Unlike windows you will never fail to come across file archives or files in a compressed state within the Linux operating system environment.

| CMD  | Description  |
|:---|:---|
|tar xvfz|	Used for creating or extracting files with .tar or .tgz extensions.
|gzip, gunzip, zcat filename|	Used in creating, extracting. or viewing files with .gz extension
|uuencode, uudecode|	Used in creating or extracting files with .Z extension.
|zip, unzip -v|	Used in creating or extracting files with .Zip extension.
|rpm|	Used in creating or extracting files with .rpm extension.
|bzip2, bunzip2|	Used in creating or extracting files with .bz2 extension.
|rar|	Used in creating or extracting files with .rar extension.
|tar cf [compressed_filename.tar] [file_name]|	This command creates an tar archive called compressed_filename for the file_name file.
|tar xf [compressed_filename.tar]|	This command extracts the tar archive called compressed_filename.
|tar czf [compressed_filename.tar.gz]|	This command compresses a tar file into a gzip archive.
|tar cf my_archive.tar directory|	This command creates a tar archive called my_archive with a directory in it.
|tar xzf my_archive.tar.gz|	This command extracts a compressed tar file inside a gzip archive
|tar cjf archive.tar.bz2 director|	This command compresses a tar file inside a bz2 archive.
|tar xjf archive.tar.bz2|	This command extracts a tar file compressed inside a bz2 archive.

<br />

## Installing Packages


| CMD  | Description  |
|:---|:---|
|**apt install package**|	Using the APT package manager to install a package software.
|yum search [keyword]|	Trace a package installation based on specific keywords.
|yum install package.rpm|	The use of a YUM package manager to install and configure a package.
|yum info package|	The use of the YUM package manager to find more information about a package before optionally proceeding with its installation.
|rpm -i package.rpm|	Using the RPM package manager to install a downloaded package.
|yum remove package|	Using the YUM package manager to uninstall or remove a package from your system.
|tar zxvf <br> sourcecode.tar.gz <br> cd sourcecode <br> ./configure <br> make <br> make install|	Command sequence to install a package software that comes as a source code.
|dnf install package.rpm|	Using the DNF package manager to install a package software.
|rpm -e package.rpm|	Using the RPM package manager to remove or uninstall an rpm package|

<br />

## Un-Installing Packages 
Source : [linuxconfig](https://linuxconfig.org/how-to-uninstall-package-on-ubuntu-linux)

### 1. Uninstall a package
Once you have the name of the package, use apt or one of the other commands to remove it.
```
$ sudo apt remove package-name
OR
$ sudo apt-get remove package-name
OR
$ sudo dpkg -r package-name
```
Any of the above commands will remove the specified package, but they will leave behind configuration files, and in some cases, other files that were associated with the package. To remove those as well, you need to "purge" the package. You can do this either after removing a package or instead of removing a package (purging automatically implies removing as well).
```
$ sudo apt purge package-name
OR
$ sudo apt-get purge package-name
OR
$ sudo dpkg -P package-name
```

### 2. Uninstall a Snap package
The Snap package manager is somewhat new but it's part of all newer versions of Ubuntu. It works independently of apt, so uninstalling software that was installed as a Snap package will require a separate command.

To see a list of installed Snap packages on your system, execute the following command in terminal.
```
$ snap list
```
After you've obtained the exact name of the package you wish to remove, use the following command to uninstall it.
```
$ sudo snap remove package-name
```

### 3. Uninstall unused packages
While installing some software, your package manager may download dependencies that are required to install a package properly. When it finishes installing a package, these dependencies will linger on your system but be unused. Therefore, it's recommended to run the following command occasionally to remove any unused packages from your system.
```
$ sudo apt autoremove
```

## Reference
1. [cheatography](https://cheatography.com/davechild/cheat-sheets/linux-command-line/)
2. [fosslinux](https://www.fosslinux.com/45587/linux-command-cheat-sheet.htm)
3. [phoenixnap](https://phoenixnap.com/kb/linux-commands-cheat-sheet)
4. [linuxconfig](https://linuxconfig.org/how-to-uninstall-package-on-ubuntu-linux)
5. [guru99](https://www.guru99.com/linux-commands-cheat-sheet.html)
