# Linux
## These are some Linux commands that I learn for DevOps.
#### Intro & Background:
- In 1964, Bell labs tried to develop a multipurpose OS.
- In 1969, they withdrew.
- The project was a UNIX project (Uniplex Information & Computing Services), it was free for all.
- Linus Torvald was a student of Helsinki University who started project Linux in 1991. At that time, UNIX was being sold very expensive.
- Linux is free for all.
- Linux is actually a kernel, not an OS.
- Linux is open source.
- Linux is lightweight in comparison with other operating systems.
- Multi User OS.

# Linux Commands:

# 1: clear
Usage: clear command is used to clear the terminal screen.

&nbsp;
# 2: sudo su
Used to switch to superuser for more privileges.
Please note: in terminal, $ denotes common user, # denotes super user.

&nbsp;
# 3: cat
Is used to create, read, concatenate, and modify files.
It opens a new editor window when used. Ctrl+d is used to exit.
### Different uses of cat command:
- cat>file1.txt inserts contents into the file, creates a new
file ‘file1.txt’ if not already created. Replaces contents of
a file.
- cat>>file1.txt here double insertion operator means
appending new contents into the file.

&nbsp;
# 4: tac
tac inverse of cat, used to print lines of contents in
reverse order.

&nbsp;
# 5: touch
Is used to create files and change attributes of files.
### Different uses of touch command.
- touch file2.txt creates an empty file file2.txt.
- touch file1 file2 creates two files.
- touch -a filename is used to change access time of file.

&nbsp;
# 5: nano
A simple & easier text editor.

&nbsp;
# 6: vi
A standard text editor
### Some info about vi:
- Press i to insert initially. Esc to return.
- :wq to save & quit.
- :w to save the file.
- :q to quit the file.
- :q! to quit forcefully.


### sudo su
Used to switch to superuser for more privileges.

### Please note: in terminal, $ denotes common user, # denotes super user.

cat: used to create, read, concatenate, and modify files.
		   It opens a new editor window when used. Ctrd+d is used to exit.
### Different uses of cat command:
- cat>file1.txt inserts contents into the file, creates a new file ‘file1.txt’ if not already created. Replaces contents of a file.
- cat>>file1.txt here double insertion operator means appending new contents into the file.
- tac inverse of cat, used to print lines of contents in reverse order.

touch: used to create empty files, or change attributes.
### Different uses of touch command.
- touch file2.txt creates an empty file file2.txt.
- touch file1 file2 creates two files.
- touch -a filename is used to change access time of file.

nano: a simple & easier text editor.

vi: a standard text editor.
### Some info about vi:
- Press i to insert initially.
- Esc to return.
- :wq to save & quit.
- :w to save the file.
- :q to quit the file.
- :q! to quit forcefully.

cd change directory command is used to navigate between different directories.
cd .. goes one level up in directory hierarchy. 

### ls
Lists the contents of a directory.

### Different uses of  ls command:
- ls is simply used to list non-hidden files and subdirectories.
- ls -a lists all files (including hidden ones).
- ls -l is often known as longlist. Lists contents with details. Along with access rights.

### stat
Command is used to list down the timestamps attributes of a file. Touch command can be used to alter the timestamps.

- mkdir: used to create new directories.
- mkdir dira dirb creates two directories.
- mkdir -p: creates directory along with parent directories. Mkdir root/rashid/dir2/dir3.

- rm -rf dir1: removes dir1 directory.
- rm -rf * deletes all the visible contents.

- pwd or present working directory shows the current directory.

### Hidden files can be created by adding . in the start of their name i.e touch .file1.txt.
- cp file1 dira copies file1 to dira directory.
- mv file2 dirb moves (cut paste) file2 to dirb.
- mv file1 xyz renames file1 to xyz. Works for directories as well.

### sort
Alphabetically sorts the rows in the file.

### useradd Rashid
Creates a new user named Rashid.
### groupadd DevOps
Will create a new group called DevOps.

### cat /etc/gpasswd -a/m displays all the users.
### gpasswd -a username groupname 
This -a flag is used to add a single user into the group.
gpasswd -m user1, user2, user3 DevOps here -m allows us to add multiple users at a given time in a group.

### cat /etc/group
- Is the file containing group info.
- ln -s file1 softFile1  creates a shortcut of file1 named softFile1.
- ln without -s flag is used to create a hard link. Which is the exact same backup copy of the file.
- tar -cvf xyz.tar dir creates a .tar file named xyz.tar adding contents of the dir directory.
-gzip xyz.tar is used to compress xyz.tar and creates xyz.tar.gz file.
- gunzip xyz.tar is the reverse of gzip.

## Yum
### yum (install, remove, update, list)
- yum remove httpd: removes apache from the machine.

### service (start, stop, status)
### which
Shows where the particular package is located.

### whoami
Displays user id.

### hostname
Displays machine name, ip version, region.

### wget
Download files from url. 

### httpd
For installing Apache server.

## OS Release
- A detailed text file containing OS version, host, details.
- Located in ‘/etc/os-release’. Can be read by cat command.

### ifconfig
Used for network info (port, private ip, public ip, mask).

### Apache
A web server used by more than 80% systems requires manual start of service.

### yum install httpd -y
Installs Apache on the machine.

### yum update httpd
Updates Apache.

### service httpd status checks status (o/p= disabled).
### service httpd start
Starts Apache service.

### service httpd stop
Stops Apache service.

### Tree
Tree is a package which displays directory structure in tree-like hierarchy.

### Access Rights:
-rw-rw-rw-@ 1 rashidwassan  staff  1630 Feb 26 19:08 commands.md
- First character ‘-’ shows that this is a file. Succeeding 3 triads are of access rights. Users, group, others respectively.
- chown rashid file1 changes owner of file1 to rashid.
- chgrp changes group.
- chmod changes access rights.
- Two ways to change access rights
- Decimal/Numeric way: r=4, w=2, x=1 unit. Makes 7 total weight.
- chmod 764 file1 means 7 for user, rwx; 6 for group rw-; 4 for others r–.
- chmod 67 file1 means 6 for groups, 7 for others.
- dchmod 6764 file1 adds special access right.
- Symbolic/Alphabetical way: Three operators +, -, = are used along with representations i.e u for user (first block), g for group (second block), and o for others (third block).
- chmod u=rwx, g+x, o-w file1 adds or removes the access for a particular group. We can use this for modifying rights for one block only too.
