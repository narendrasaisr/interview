### 1.What is command for created multiple files at a time?
Touch FILE1 FILE2
# 2. What is INODE and How to Identify?
Its unique identification code for files and directories, it is generated automatically while
create new file and directories
Command to get inode number of a file and directory
ls -i filename
ls -ldi directoryname
Command to get inode usage
df -i
# 3. List of Permissions and Users
Read(r), Write(w) and Execute(x) - Permissions
Owner(u), Group Owners(g) and Others(o) – Users
Every file has permissions defined for Owner(3 letters), Group ( 3 letters) and Others(3
letters)
If you run a ls -ltr in terminal you’ll get below
drwxr--r-- 2 tom staff 64 Jun 21 2021 samplefiles
lrwxr-xr-x 1 tom staff 1 Jul 6 2021 x
• chmod u+rwx filename -- to add permissions.
• chmod u-rwx directoryname -- to remove permissions.
• chmod u+x filename -- to allow executable permissions.
• chmod u-wx filename -- to take out write and executable permissions.
Permission numbers are:
• 0 = ---
• 1 = --x
• 2 = -w-
• 3 = -wx
• 4 = r-
• 5 = r-x
• 6 = rw-
• 7 = rwx
For example:
• chmod 777 foldername --will give read, write, and execute permissions for everyone.
• chmod 700 foldername -- will give read, write, and execute permissions for the user
only.
• chmod 327 foldername -- will give write and execute (3) permission for the user, w (2)
fo the group, and read, write, and execute for the users.
#4. What is use of “top” command and how to sort Memory and User wise?
Its used to real time monitor hardware utilization of linux machine.
Press M to sort Memory wise result
Press U to sort User wise result
#5. What is command for to force close one particular process
kill -9 Processid
#6. What is File Path of DNS Configuration ?
/etc/reolv.conf
#7. How to edit and save file using editors?
The following commands are used to exit from vi editors.Hit Esc
:wq saves the current work and exits the VI.
:q! exits the VI without saving current work.
#8. What is file path of Alias name set by Permanent?
/etc/bashrc
#9. What types of Installation Tools in REDHAT?
RPM = Redhat Package Manager
YUM = Yellow Dog Updated Modifier
10. Tell me Linux Boot Sequence Flow?
BIOS → MBR → Boot Loader → Kernal → Runlevel
BIOS Basic Input output system, executes MBR
MBR Master boot record executes GRUB
GRUB Grand unified boot loader
Kernel Executes /sbin/init
init Executes run level programs
Runlevel executes from /etc/rc.d/rc*.d/
11. Types of Zone in DNS?
Forward lookup zone Reverse lookup zone
12. What is LDAP
The Lightweight Directory Access Protocol (LDAP) is a set of open protocols used to access
centrally stored information over a network.
13. What is command package install using YUM without ask Prompt?
yum install packagename -y
14. What is command Uninstall package?
yum remove packagename
15. What is command package re-install using YUM without ask Prompt?
yum reinstall packagename -y
16. Location of Cron file in linux?
/var/spool/cron
17. What is command for to see Particular user Job Schedule ?
crontab -lu username
18. What is command for restart cron service?
service crond restart
19. What is Kernel un Unix Operating system?
Kernel is the heart of operating system. It interacts with shell and executes the machine level
language.
20. How to create a file in Unix?
There are multiple way to create files in unix, but the simple way to create a file is using “cat”
and “Touch”
command Syntax:
cat > File name touch file name
21. How can I check which processes are running in my machine?
To check process which are running in my machine I can use two commands. (a) TOP and
(b) PS
22. What is the difference between TOP and PS command?
Top command gives the dynamic view of the processes are running in the server and
generally the dynamic change happens in every 3 second. Whereas PS commands gives
the static view of the processes.
23. You used TOP command and without aborting the TOP process I need to kill one
process. Is it possible to kill ?
Yes TOP command it self has a command prompt. Type K then it will ask you for the PID of
the process to kill. Hit the PID and enter, it will kill the process.
24. What is the difference between creating a file in cat and in touch command?
cat command creates a file and we can save some data inside the file but touch command
by default will create a blank file.
25. How can I create multiple directories at a time? Say I want to create a directory D1
and inside that D2 and inside that D3. Is it possible? If yes how ?
Yes creating multiple directories is possible. In this scenario the below command works.
Mkdir –p D1/D2/D3
26. I want to create D1, under that D2 and D3. Inside D2 I want D4 and inside D3 I want
D5 to be created. How is it possible?
The below command will work for it. mkdir –p D1/D2/D4 D1/D3/D5
27. How can I check in which directory I am in ?
Use PWD command to check which directory you are in.
28. We are using so many commands and getting output. Have you ever wondered how
the commands are executing and getting you the output?
Yes every command in Unix is a C program in the backend. When we type a command and
hit enter the program runs in the backend and gives you the output.
We can view the C program as well as below.
type <Command Name> ->hit enter, it will give you a path where the program the command
is located. You can view the program by doing cat and the path name. it will open a C
program file in decrypted mode.
29. How can I list the directories and the files ?
Using ls command. I can view the directories and files of the system.
30. How can I view hidden files in a system ?
Using ls –a command I can view the hidden files of the sytem
31. In real time environment many people use “ll” command instead of ls. So is there any
command called “ll” exits?
No there is no such command called “ll”. It’s just the alias of ls command. We can check it by
typing alias
command.
32. What is a shell ?
Description of shell is huge, but yes commonly we explain it as the interpreter between the
user and the machine.
33. Describe the usage of rm –r* command in unix and shall we use it in real time
environment?
rm –r* will remove all the file entries in the current directory. It is not advisable to use this
command in real time environment. Specifically in production. Because we have huge files
which are necessary to be accessed by other users.
34. What is symbolic link ?
The second name of a file is called a link, it’s assigned to create another link to the current
file.
35. What is absolute path and relative path in unix ?
Absolute path refers to the path starting from the root directory and the path continues with a
sequence starting from Root. Whereas relative path is the current path.
36. How can I check the system IP ?
type hostname command or else you can use ifconfig as well.
37. How can I check if a server is up and running or not ?
you can use ping –t command for this. Ping –t <hostname> or <IP address>
38. How can I append some lines in an existing file ?
cat >> file name and hit enter. You can append lines below the existing lines of the file. And
do a ctrl D to save and exit.
39. What is FIFO and LIFO in unix ?
FIFO is first in first out and LIFO is last in last out.
40. What is PATH variable ?
PATH is an environmental variable which contains the path of the command files and we can
change the paths inside the PATH variable.
41. How can I kill a process in unix?
first use PS –ef command and get the PID of the process you want to kill. Then use kill -9
<PID_Number> command to kill the process.
42. How can I check the memory size of a linux/unix machine ?
Use Free –m or free –G command to check the memory size of a linux machine.
43. How to check disk utilization of a linux server?
Use du command to check the disk utilization.
44. How to check the disk free of all the mount points in unix ?
use df –h command, it will show the disk free of linux machine.
45. How can I check who are the users logged in my system?
use users command. It will how the details of the users logged in to the system.
46. I have a file Mantu.txt which contains multiple lines and few of the lines has a
particular
pattern as “India”. I want to print only those lines. How can I ?
I will use grep command here. And the syntax will be as below. Grep -i “India” Mantu.txt
Grep command is used for pattern searching.
47. What do you mean by a super user ?
A admin while giving permission to the users usually give normal access permission but few
of the user having special permission then normal user, they are called super user.
48. What is the syntax to move to a super user?
sudo su – <user name>
49. What is a process group in unix ?
collection of more than one process is called as a process group in unix.the function getpgrp
returns the process group id.
50. How many numbers are used with kill while killing a process ?
there are 64 numbers which can be used with kill command but generaly we use kill -9
51. What are different types of files available in unix?
There are multiple type of files available in unix, few of among them are :
• Regular file
• Image file
• Binary file
• Linked file
52. What are cmp and different command in unix?
cmp command compares the two files byte by byte and gives the output what is not common
in between them. Diff command through the output which is not matching between the two
file immediately rather comparing bit by bit.
53. What is pipe command ? why it is used for ?
Pipe symbol interlinks two commands. It stores the output of the first command and give it to
the second command as input.
Cat emp.lst | mantu.txt
54. How can I number the lines of a file in VI editor?
Open the file using vi <filename>
Then go to command prompt and type set number. The numbers will be set before every line
of the file.
55. What is the command to check all the options and detail information of a command in
unix ?
We can use man <command name>. it will show you all the possible way to use the
command.
56. What is head command used for ?
head command is used to view the top portions of the file. Say if I want to view top 5 lines of
a file then I can use the below command.
Cat <filename> | head -5
57. What is tail command used for ?
tail command is used to view the bottom of the lines of a file. Say if I want to view bottom 5
lines of a file then I can use the below command.
Cat <filename> | tail -5
58. What are the other commands used for pattern searching ?
Grep and sed are the main command used for pattern searching.
59. How can I search a pattern in vi editor ?
Open the file with vi. Use /pattern name , then hit enter, it will show you the matching
patterns in VI.
60. How can I delete one line in Vi editor ?
Use dd in command mode to delete one line of a file in vi.
61. What is the command used for copying a file?
Use cp command while copying a file in unix.
cp <sourcepath of the file> <destination path of the file>
62. What is SCP in unix ?
Scp stands for secure copy in unix. The files which get copied by using scp command are
decrypted so we need not be worry of hacking of the file system.
63. What is mv command in unix?
We can move a file or rename a file using this command. General purpose of using mv
command is to use it for reaming purpose.
64. What does a touch command do apart from creating a blank file?
Touch command is used to change the access and modification time of the file.
65. Explain the advantages of executing a process in background
We use “&” symbol to execute a job in back ground. When we execute a job or process in
unix it starts executing in the prompt itself and we can’t do other stuffs in the command
prompt at that time. So until unless the process gets executed we have to seat idle. So for
continuous interaction with the command prompt we prefer executing the jobs or processes
in back ground.
66. How do you protect file deletion in ext4?
you change any attributes of the file to read only. The command is:
chattr +i filename And to disable it: chattr -i filename
67. Special Permissions in linux
Sticky bit – Only created user and root can able to delete the file
$ chmod o+t tecadmin.txt$ chmod +t tecadmin.txt# chmod 1777 tecadmin.txt# ls -ld
tecadmin.txtdrwxrwxrwt 2 himanshu himanshu 4096 Oct 24 16:19 tecadmin.txt
SUID – Ging permission for all users like root
chmod u+s /bin/ls – ls can be used for all users as like root # chmod 4555 [path_to_file] #ls -l
/bin/ls
-rwsr-xr-x-x 1 root user 16384 Jan 12 2014 /bin/ls
SGID – SGUID :- chmod g+s /dir –> all subdirectories and files created inside will get same
group
ownership as the main directory, it doesn’t matter who is creating.
chmod 2555 [dir] # ls -l /usr/bin/write
-r-xr-sr-x 1 root tty 11484 Jan 15 17:55 /usr/bin/write
68. What files are created/modified when adding a user (useradd) in linux?
/etc/passwd and /etc/shadow
files from /etc/skel are typically copied into the new user’s home directory
69. How to see and get info about RAM in your system
free
cat /proc/meminfo
70. How will you suspend a running process and put it in the background?
Ctrl+z
71. Name the Daemon responsible for tracking System Event on your Linux box?
Syslogd
72. To see tar file without extracting?
tar -tvf
73. How to check dependencies of RPM Package on before Installing ?
# rpm -qpR BitTorrent-5.2.2-1-Python2.4.noarch.rpm
/usr/bin/python2.4 python >= 2.3
python(abi) = 2.4
python-crypto >= 2.0 python-psyco
python-twisted >= 2.0 python-zopeinterface
rpmlib(CompressedFileNames) = 2.6 q : Query a package
p : List capabilities this package provides.
R: List capabilities on which this package depends.
74. How Many Run Levels present in Linux?
There are seven run levels, with each having its own properties.
• Halt the system
• Single-user mode
• Multiuser mode without networking(NFS)
• Multi-user mode with text login
• Not used
• Multi-user mode with graphical login
• Reboot
75. How do i check which NFS version ?
rpcinfo -p localhost | grep -i nfs rpm -qa | grep nfs
rpm -qi nfs nfs-utils
76. Use find command to delete file by inode?
Find and remove file using find command follows:
$ find . -inum 782263 -exec rm -i {} \;
77. Explained BOOT LOADER?
The boot loader is then responsible for loading the kernel
A boot loader finds the kernel image on the disk, loads it into memory, starts it. Stage 1 boot
loader
First stage the primary boot loader is to find and load the secondary boot loader
It will find by looking through the partition table for an active partition
This is verified methos to the active partition’s boot record is read from the device into RAM
and
executed.
Stage 2 boot loader
The second-stage, boot loader called the kernel loader.
The first- and second-stage boot loaders combined are calledGRand Unified Bootloader.
With stage 2 loaded, GRUB can display a list of available kernels You can select a kernel
parameters.
78. So how do I find out zombie process?
# ps aux | awk ‘{ print $8 ” ” $2 }’ | grep -w Z Output:
Z 4104
Z 5320
Z 2945
79. How do I kill zombie process?
ps axo ppid,stat | grep Z | awk ‘{print $1}’ | xargs kill -HUP kill -HUP $(ps -A -ostat,ppid | grep
-e ‘[zZ]’| awk ‘{ print $2 }’) kill -9 $(ps -A -ostat,ppid | grep -e ‘[zZ]’| awk ‘{ print $2 }’)
To set a password to the boot loader # grub
grub> md5crypt Password: ************
Encrypted: $1$3yQFp$MEDEglsxOvuTWzWaztRly. grub> quit
Next, add this to your grub.conf file like so:
default=1 timeout=10
splashimage=(hd0,0)/grub/splash.xpm.gz
password –md5 $1$3yQFp$MEDEglsxOvuTWzWaztRly.
80. Determining Filesystem Usage
To determine how much disk space is being used for a given partition, logical volume, or
NFS mount, use the df command.To display the output in “human readable” format, use the
-h argument to df.
The du command displays the disk usage totals for each subdirectory and finally the total
usage for the current directory.Values are in kilobytes.
du -hs /etc
du -h /vol1/group1/examplefile
81. Reporting Disk Performance
For example, if the access time for a drive suddenly drops, an administrator
must quickly start troubleshooting the problem to determine if it is a software or hardware
issue or simply due to lack of free space on the disk.
82. Displaying Memory Usage with free
# free -m
The free command tells you about current memory usage.
Two types of system memory exist: physical and virtual. To display the amount of free and
used memory, both physical and virtual (swap), use the free command
83. Monitoring and Tuning the Kernel
Using the /proc Directory
Instead of executing utilities such as free and top to determine the status of system
resources or fdisk to view disk partitions, an administrator can gather system information
directly from the kernel through the
/proc filesystem.
When you view the contents of files in /proc, you are really asking the kernel what the
current state is for that particular device or subsystem. To view the contents of a special file
in /proc, use the cat, less,or more file viewing utilities.
84. Yum Server in linux
$ cat /etc/yum.conf
[main] cachedir=/var/cache/yum keepcache=0
debuglevel=2 logfile=/var/log/yum.log pkgpolicy=newest distroverpkg=redhat-release
tolerant=1
exactarch=1 obsoletes=1 gpgcheck=1 plugins=1 metadata_expire=1800
ErrorDocument
The ErrorDocuments directive lets you specify what happens when a client asks for a
nonexistent document.
Specifies a file that the server
sends when an error of a specific type occurs. You can also provide a text message for an
error. Here are some examples:
ErrorDocument 403 “Sorry, you cannot access this directory”
ErrorDocument 403 /error/noindex.html
ErrorDocument 404 /cgi-bin/bad_link.pl
ErrorDocument 401 /new_subscriber.htm
• 400: Bad Request
• 401: Unauthorized
• 402: Payment Required
• 403: Forbidden
• 404: Not Found
• 405: Method Not Allowed
• 406: Not Acceptable
• 407: Proxy Authentication Required
• 408: Request Timeout
• 409: Conflict
• 410: Gone
• 411: Length Required
• 412: Precondition Failed
• 413: Request Entity Too Large
• 414: Request-URI Too Long
• 415: Unsupported Media Type
• 416: Requested Range Not Satisfiable
• 417: Expectation Failed
• 500: Internal Server Error
• 501: Not Implemented
• 502: Bad Gateway
• 503: Service Unavailable
• 504: Gateway Timeout
• 505: HTTP Version Not Supported
85. Find Files Using Name in Current Directory?
# find . -name tecmint.txt
86. Find Files Under Home Directory?
# find /home -name tecmint.txt
87. Find Files Without 777 Permissions?
# find / -type f ! -perm 777
88. Find SGID Files with 644 Permissions?
# find / -perm 2644
89. Find Sticky Bit Files with 551 Permissions?
# find / -perm 1551
90. Find SUID Files?
# find / -perm /u=s
91. Find SGID Files?
# find / -perm /g=s
92. Find Read Only Files?
# find / -perm /u=r
93. Find Executable Files?
# find / -perm /a=x
94. Find all Empty Files?
# find /tmp -type f -empty
95. Find all Empty Directories?
# find /tmp -type d -empty
96. File all Hidden Files?
# find /tmp -type f -name “.*”
97. Find Single File Based on User?
# find / -user root -name tecmint.txt
98. Find all Files Based on User?
# find /home -user tecmint
99. Find all Files Based on Group?
# find /home -group developer
100.Find Last 50 Days Modified Files?
# find / -mtime -50
101.Find Last 50 Days Accessed Files?
# find / -atime -50
102.Find Last 50-100 Days Modified Files?
# find / -mtime +50 –mtime -100
103.Find Changed Files in Last 1 Hour?
# find / -cmin -60
104.Find Modified Files in Last 1 Hour?
# find / -mmin -60
105.Find Accessed Files in Last 1 Hour?
# find / -amin -60
106.Find 50MB Files?
# find / -size 50M
107.Find using inode number?
find . -inum 27492358 -exec rm -i {} \;
108.Main configuration file of Apache server ?
/etc/httpd/conf/httpd.conf
109.Main configuration file of Apache server ?
/etc/httpd/conf/httpd.conf
110.What is the use of SCP command in Linux?
SCP command stands for secure copy. It is used to copy/download data from one machine
to another machine.
111.What is telnet and what does it do?
the telnet command is used to check the connectivity to other servers. It helps you to check
whether you are able to talk to another server or now. Ex: telnet 192.0.0.1 22 where 22 is the
port number.
112.What is a bastion host?
A bastion host is also known as a jump server. It is used to connect from one machine to
another machine securely. Bastion hosts are used to connecting to private servers securely.
113.What is the command to find the IP address of the host machine in linux?
You can use ifconfig/ ipaddr show command to find the IP address of the host machine.
114.Name some of the text editors that are available in Linux?
Some of the common text editors that are available in Linux are vi/vim, nano, subl, gedit,
atom, emacs. Vi is the default editor that you have in Linux machines.
115.What are the different zip files formats that are available in linux?
The different zip formats in Linux are zip, gzip and bzip.
116.What is the difference between cp and mv command?
cp command stands for copy and is used to copy data from one location to another. mv
stands for the move and is used to move data from one location to another.
117.How can you run a process in the background in Linux?
You can run a process in the background by pressing ctrl+z command.
118.What is the use of ‘chown’ command ?
chown stands for ‘change ownership’ and is used to change the ownership of a file or
directory. Eg: chown username.username <filename>.
119.What is the use of ‘chmod’ command?
chmod stands for ‘change mode’ and is used to change the permissions on files or
directories. Eg: chmod
a+w <filename>
120.What is the command to create a zip file in linux?
To create a zip file you can use tar command with -cvzf arguments. Eg: tar -cvzf test.tar.gz
<file names to be included in the zip>
121.What is the command to unzip the file in linux?
To unzip a file you can tar command with -xvzf arguments. Eg: tar -xvzf test.tar.gz
122.What is the command to show the contents of a zip file ?
To see the contents of the zip file you can use tar -tvzf arguments. Eg: tar -tvzf test.tar.gz
123.What is a soft link in Linux?
A soft link is used to create a shortcut in Linux. This is similar to creating a shortcut in
windows systems.
124.What is the command used to create a soft link?
To create a soft link you can use ln command with -s arguments. Eg: ln -s /var/www/html
html, where
/var/www/html is the source file and HTML is the destination of the shortcut.
125.What is the command to remove the soft link in Linux?
To remove the soft link in Linux you can use unlink command. Eg: unlink <filename>
126. What is the use of whereis command in linux?
Whereis command is used to find the binaries and libraries files of an application in linux.
127. What is the use of man pages?
Man pages stand for manual pages. It is the documentation about and helps you to
understand the commands and how to use the commands. Eg: man wget.
128. what does “2>” indicate in redirection?
This means that output will be shown on the screen and the errors will be written to a file that
you specify. Eg: ls /etc/test 2> error.txt
129. What are the different type of users that you have in Linux?
You have 2 types of users in linux. They are
• root user
• standard users.
Linux System Administration Interview Questions and Answers
130. How To check Memory stats and CPU stats ?
free & vmstat commands.
131. What is the purpose of runlevels ?
Useful for debugging purpose. Basic idea is each runlevel has some services operational
and depending on need can enable different runlevels to test which services are running
132. You are able to ping with a numeric IP address, but not by name. How will you debug
?
First check /etc/resolv.conf file for DNS Server Entry
133. Generally setting up services in Linux require ————— and ————–
Update the associated configuration file and ensure the appropriate daemon is started
134. What is the purpose of iptables command ?
Basically allows rule creation to filter packets according to established criteria. Network
Address Translation function is also done
135. How can you findout the current runlevel the system is in ?
who -r
136. Linux system has crashed and keeps getting to the # Debug Prompt. How do you
bring it to normal login prompt
Likely due to file system inconsistency, run fsck to check and accept inode repairs.
137. Name 3 Environment variables
SHELL,HOME,PATH
138. Where is my vmlinuz executable loaded from ?
/boot
138. As System Admin, log files are monitored as they grow. How is this achieved ?
tail -f
139. Automatic mounting of new file system at boot-time can be done by
Adding an entry in /etc/fstab file
140. You recently ran an install, the command for which you need to recall. How do you
get this?
history command
141. In writing a Bash Shell script, special character’ meaning has to be altered. How is it
done?
Escape sequence. Precede the special character with a ‘\’
142. Linux associates devices with File Descriptors. List them
0 – Standard Input. 1- Standard Output 2-Standard Error
143. How do you set a mask to stop certain permissions from being granted by default on
file creation?
umask command
144. You want to try out a Distribution before installation. Which image would suit?
LiveCD
145. System Administrators monitor load averages on System for analysis. How is this
done?
top command
146. What is the behaviour of the following very useful grep command ?
grep [abc] file1 : Looks for matches in file1 containing either an a or b or c character.
147. You need to make a file with only read permissions for yourself, group and all. How
can you ?
chmod 444 file1
148. What does su – do ? Give an example of when you would use this.
Gets the switch to root account. Need to be done before Software installation.
149. Pipe is a very important concept in process communication. Give an example
cat file1 |grep xyz : Pattern matching by grep happens on the displayed file1
150. In Shell scripting command return codes are checked prior to proceeding. Explain
These are Exit status codes. Linux follows 0 for success and nonzero codes for failures
151. What is load average and how to find it ?
The load average is the average system load on a Linux server for a defined period of time.
it is the CPU demand of a server that includes the sum of the running and the waiting
threads.
uptime -- command to see load average
152. What is difference between hard link and soft link?
A symbolic or soft link is an actual link to the original file, whereas a hard link is a mirror copy
of the original file. If you delete the original file, the soft link has no value, because it points to
a non-existent file.
has different inode number and file permissions than original file
ln -s file link
hard link: Even if you delete the original file, the hard link will still has the data of the original
file. Because the hard link acts as a mirror copy of the original file.
has the same inode number and permissions of original file
ln file link
153. Grep Usage
The grep command is a very useful tool, that when you master will help you tremendously in
your day to day.
You can use grep to search in files, or combine it with pipes to filter the output of another
command.
For example here's how we can find the occurences of the document.getEtementById line in
the index.md file:
grep document.getElementById index.md
Using the –n option it will show the line numbers:
grep -n document.getElementById index.md
One very useful thing is to tell grep to print 2 lines before, and 2 lines after the matched line,
to give us more context. That's done using the –C option, which accepts a number of lines:
grep -nC 2 document.getElementById index.md
Search is case sensitive by default. Use the –i flag to make it insensitive.
grep -i filter abc.txt
The search string can be a regular expression, and this makes grep very powerful.
Another thing you might find very useful is to invert the result, excluding the lines that match
a particular string, using the –v option:
grep -v filter abc.txt
To find all occurrences of the word `patricia' in a file:
$ grep 'patricia' myfile
To find all occurrences of the pattern `.Pp' at the beginning of a line:
$ grep '^\.Pp' myfile
The apostrophes ensure the entire expression is evaluated by grep instead of by the
user's shell. The caret `^' matches the null string at the beginning of a line, and the `\'
escapes the `.', which would otherwise match any character.
To find all lines in a file which do not contain the words `foo' or `bar':
$ grep -v -e 'foo' -e 'bar' myfile
A simple example of an extended regular expression:
$ egrep '19|20|25' calendar
Peruses the file `calendar' looking for either 19, 20, or 25.
