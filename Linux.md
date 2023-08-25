### Linux ###
Linux is an opensource Platform
Main components of Linux
  1. Kernal  also called OS
  2. shell
  3. Hardware
  4. Applications
Kernal is the heart of the OS, the kernel interacts with the hardware

shell takes the inputs from the user and passes them to the kernel

OS-> os is a bridge between the user and the hardware

UNIX: is not portable and costly need to buy both OS and hardware  so it's costly, and tightly coupled with hardware

Kernel + Linux = Linux, Inventor Linus Torvals

Linux is free and open-source software, it's portable and has no hardware locking 

96% of servers are running in the world on Linux, even supercomputers also.

why Linux is good than any OS :
  #. less cost & More performance and secured 
  #. consume less memory and more speed
  #. secured - originally from unix Principles
  #. More community support and & Very stable (Linux can run without restarting  and without doing any updates run  for years)
  #. Consume low Power

Linux OS or Kernel.?
Linux is a kernel and opensource code kernel with a shell
added more utilities such as Ubuntu, Centos, Fedora, Redhat and etc
Linux + Shell+ graphics = Android, Ubuntu, Desktop
Linux + Shell + some Utilities = Server

What are SSH keys .?
SSH keys are 2 types 
  1. Public key -> keep inside the server 
  2. Private key -> Who ever wants to access the server they have the private key 

How to generate SSH key 
command is 
ssh-keygen -f <filename>  -> it will generate the private key

### Commands ###


Any command in Linux syntax is. Based on the command behavior we can choose options and inputs.

[command-name] [options] [inputs]

When we login to the Linux server by default we will land into

/home/[user-name]

In the case of centos, it is /home/centos.

To get sudo access.

sudo su -

to change the directory to any other folder.

cd [/path/to/folder]

$ - normal User

 - Root user

pwd - present working Directory

uname -> command will show the OS information

man uname -> manual OS informtion 

uname -a ->  will give you complete information about OS 

ls ->  listing

ls -l ->  listing in a detailed way 

ls -lr ->  listing in reverse order (Reverse Lengthy format)

ls -lt ->  listing in time-based (Latest files)

ls -ltr ->  listing in time-based reverse order

ls -la -> It will show hidden files

ls -lar -> It will show hidden files in reverse order

cd ->  directly navigate to the home directory 

cd .. -> This command will navigate to 1 step back 

cp ->  for copying the content

mv -> move the files or directories syntax mv [source-file-or-folder] [destination]

Rename the file with also same command syntax mv [present-file-name] [new-file-name]

mkdir ->  making new a directory 

cat -> to view the content in  the file 

rm ->  for deleting the empty directory

rm -r -> delete file or directory (-r is recursive)

grep ->  find something in the file

syntax grep [text-to-search] [file-name]

head -> command will display 1st 10 lines of the file

head [file-name]

head -n 5 ->  command will display the first 5 lines of the file

head -n 5 [file-name]

tail ->  command will display the last 10 lines of the file

tail [file-name]

tail -n 5 ->  command will display the last 5 lines of the file

tail-n 5 [file-name]

To download the file.

wget [download-URL]

To get the source and show the content in the terminal.

curl [URL]


### Exit status ###


exit status is very important in Linux. We use this to know whether the result is success or failure. Linux store the result in a special variable
$?
echo $?

Success - 0

Failure - Other than 0 any number


### Permissions and Ownership   ###


We have 3 types of ownership.

User: He is the one who created the file/folder. Denotes by u

Group: a group of users the file belongs to. Denotes by g

Other: Anyone other than the user and group. Denotes by o

3 types of Permissions

Read: denotes by number 4

Write: Denotes by number 2

Execute: Denotes by number 1

-rw-rw-r-- 1 ec2-user ec2-user  1483 May 24 13:58 eks-client.sh

The above line has a total of 10 characters. The first character shows it is file(-)
The next 3 characters denote the permission of the user.
The next 3 characters denotes the permission of the group
The next 3 characters denote permission of other

So the user has read and write access.
Group has read and write access.
others have only write access.

If we want to add execute permission to everyone.

chmod ugo+x [file-name]

If we want to add write permission only to user and group.

chmod ug+w [file-name]

If we want to remove execute access to all.

chmod ugo-x [file-name]

We can use letters also. R+W = 4+2 =6 R+W+X = 4+2+1 = 7

The below line denotes read access to the user and no access to the group and others.

chmod 400 [file-name]

# System Information #
date : shows the  current date and time

cal : shows this month's calender

uptime : Show Current Uptime

w : display who is On line

whoami : who you are logged in as 

finger user : Display information about user

uname -a : Shows kernal Information

cat /proc/cpuinfo  : CPU information

cat /proc/meminfo  : memory information

man command : shows the manual for command 

df : shows the disk usage 

du : shows the directory space usage

free : show the memory and swap usage 

whereis app : shows the possible locations of app

which app : shows which applications will be run by default

# Process management #
ps : To display the current working Process

top : Display the running process

kill PID : kill the process with given PID 

PID means Process ID

Killall proc : kill all the process named proc

pkill pattern : will kill all process matching the pattern

bg : List stopped or background jobs, resume a stopped jobs in the background

fg : Brings the most recent job to foreground

fg n : Brings job n to the foreground

# Searching Commands #

grep pattern files : search file pattern in file

grep -r pattern dir : search resursively for pattern in dir 

command | grep pattern : search pattern in the output of a command 

locate file : find all instances of file 

find . -name : filename 

search in the current directory (represented by a period) and below it, for files and directories with names starting with file pattern

pgrep pattern : searches for all the named process, that matches with the pattern and, by default, returns their ID

# File Permissions #
chmod octal file 

change the permission of file to octal,which can be found separately for user, group,world by adding 
. 4-read (r)
. 2-write (w)
. 1-execute (x)


# Network #

ping host : Ping host and output the result

whois domain : Get whois information for domains

dig domain : Get DNS information for domain

dig -x host : Reverse lookup host

wget file : Download the file 

wget -c file : continue a stopped download 

# Compression #
tar cf file.tar file : Create tar named file.tar containg file

tar xf file.tar : Extract the files from file.tar

tar czf file.tar.gz files : Creates a tar with Gzip compression

tar xzf file.tar.gz : Extract atar using Gzip

tar cjf file.tar.bz2 : Extract a tar using Bzip2

gzip file : Compress file and renames it to file.gz

gzip -d file.gz : Decompresses file.gz back to file


# Shortcuts #
ctrl+c  : Halts the current command

ctrl+z : stops the current command, resume with fg in the foreground or bg in the background

ctrl+d : logout the current session, similar to exit

ctrl+w : Erases the one word in the current line 

ctrl+u : erasses the whole line 

ctrl+r : Type to bring up a recent command 

!! : Repeats the last command 

exit : Logout the current session 

# User management#
useradd <username>  ----> to add new user 
ex: useradd ram
 
passwd <username>  ----> to setup password for the new user

ex: passwd ram 

id username   ----> command to read the user information

ex: id ram

id : command will give you  current user information , if it is root user id is always "0" 
normal user id is anything except "0"

when ever a user is created, by default a group on the same user name will be created 

every user have 2 groups
  1. primary group
  2. secondary group

vim /etc/passwd   ----> command for view the user info

ex: ram:x :1001:1001:: /home/ram: /bin/bash 

ram is username , 1001 - user ID , 1001 - group ID , /home/ram - default home directory, /bin/bash - default shell terminal 

getent passwd ----> it will display the passwd file 

##group info ##

groupadd <group-name> 

ex: groupadd devops   

getent group ----> command will give you the list of groups 

usermod -g <group-name> <user-name>  ----> primary group to add user to the group 

ex: usermod -g devops ram

usermod -a -G devops ram 

-a append 
-G group 

now user have one primary and one secondary group wich is devops

# How to remove user from Group #

gpasswd -d <username> <groupname>   

ex: gpasswd -d ram devops

-d : delete 

# how to delete groups #

groupdel usergroupname 

ex: groupdel devops

# how to remove user from group #
gpasswd -d <username> <groupname>

ex: gpasswd -d ram devops

if user exit oranization first remove from primary and secondary groups 

gpasswd -d <user-name> <group-name>

if above command not working add him to the default group and then delete from the group

usermod -g <username> <user-groupname>   (user will be deleted from all the groups)

userdel <username> 
ex: userdel ram

groupdel <groupname>

ex: groupdel devops






# Package Management #
yum ----> yellow dog utility manager  or Yellowdog Updater, Modified (yum Package)

apt ----> Advanced Package Tool
rpm ----> redhat package management

yum can understand the dependency and it will automatically install required dependent packages

command for view the list of installed packages

yum list installed  ----> show all the installed packages

yum list installed | wc -l      ----> will display the count of installed packages

yum list all  ----> it will show all the availabe packages through this repos 

yum list all | wc -l   ---->it will show all the availabe packages  count 

yum update -y ----> update all the packages 

yum list available   -----> all-installed 

yum list available | wc -l  ----> will show count of all-installed packages 

yum remove nginx  ----> will remove the nginx package 

----------------------------------------

## Service Management ##

how can you run a software inside the webserver ?

sudo yum install nginx -y

systemctl start nginx ----> This will start the service

systemctl status nginx ----> this can check the status of nginx 

ps -ef | grep nginx 

systemctl stop nginx  ----> comamnd will stop the nginx service 

systemctl restart nginx  ----> comamnd will restart the nginx service

systemctl enable nginx ----> it will restart automatically if the server is reboot

systemctl disable nginx ----> it will desable the package 

reboot ----> command will reboot the system

## Network Management ##

cat /etc/*release  ----> to check the Linux Distribution 

cat /proc/cpuinfo  ----> to check the CPU info

cat /proc/meminfo    ----->  to check the memory info

cat /etc/os-release  ----> to check the os Info 

free -m   (or) free   ----> to check the free memory 

df -kh  (or)  df -h  ----> to check the harddisk 

df -hT   ----> command will display the harddisk  type and storage related  info 

du -sh *      ----> (Disk Utilization) Summarize disk usage of the set of FILEs, recursively for directories.

===============================================================================

du --help
Usage: du [OPTION]... [FILE]...
  or:  du [OPTION]... --files0-from=F
Summarize disk usage of the set of FILEs, recursively for directories.

Mandatory arguments to long options are mandatory for short options too.
  -0, --null            end each output line with NUL, not newline
  -a, --all             write counts for all files, not just directories
      --apparent-size   print apparent sizes, rather than disk usage; although
                          the apparent size is usually smaller, it may be
                          larger due to holes in ('sparse') files, internal
                          fragmentation, indirect blocks, and the like
  -B, --block-size=SIZE  scale sizes by SIZE before printing them; e.g.,
                           '-BM' prints sizes in units of 1,048,576 bytes;
                           see SIZE format below
  -b, --bytes           equivalent to '--apparent-size --block-size=1'
  -c, --total           produce a grand total
  -D, --dereference-args  dereference only symlinks that are listed on the
                          command line
  -d, --max-depth=N     print the total for a directory (or file, with --all)
                          only if it is N or fewer levels below the command
                          line argument;  --max-depth=0 is the same as
                          --summarize
      --files0-from=F   summarize disk usage of the
                          NUL-terminated file names specified in file F;
                          if F is -, then read names from standard input
  -H                    equivalent to --dereference-args (-D)
  -h, --human-readable  print sizes in human readable format (e.g., 1K 234M 2G)
      --inodes          list inode usage information instead of block usage
  -k                    like --block-size=1K
  -L, --dereference     dereference all symbolic links
  -l, --count-links     count sizes many times if hard linked
  -m                    like --block-size=1M
  -P, --no-dereference  don't follow any symbolic links (this is the default)
  -S, --separate-dirs   for directories do not include size of subdirectories
      --si              like -h, but use powers of 1000 not 1024
  -s, --summarize       display only a total for each argument
  -t, --threshold=SIZE  exclude entries smaller than SIZE if positive,
                          or entries greater than SIZE if negative
      --time            show time of the last modification of any file in the
                          directory, or any of its subdirectories
      --time=WORD       show time as WORD instead of modification time:
                          atime, access, use, ctime or status
      --time-style=STYLE  show times using STYLE, which can be:
                            full-iso, long-iso, iso, or +FORMAT;
                            FORMAT is interpreted like in 'date'
  -X, --exclude-from=FILE  exclude files that match any pattern in FILE
      --exclude=PATTERN    exclude files that match PATTERN
  -x, --one-file-system    skip directories on different file systems
      --help     display this help and exit
      --version  output version information and exit

===============================================================================


find [where-to-search]   -name  "what-file-to-search"

ex: find / -name "passwd"

find / maxdepth 1 -name "passwd"    ----> find  something in folder indepth

ex: find / maxdepth 1 -name "passwd" 

1, 2,3 and etc 


 