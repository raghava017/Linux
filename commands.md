### Commands

Any command in Linux syntax is. Based on the command behaviour we can choose options and inputs.

```
[command-name] [options] [inputs]
```

When we login to Linux server by default we will land into
```
/home/[user-name]
```
In case of centos it is /home/centos.

To get sudo access.

```
sudo su -
```

to change the directory to any other folder.

```
cd [/path/to/folder]
```

#### listing the files.
 
* Just list files and folders.

```
ls
```
* List files and folders in long format
```
ls -l
```
* List files in reverse order.
```
ls -lr
```
* List files in latest time format.
```
ls -lt
```
* List files in reverse time format.
```
ls -ltr
```
* List hidden files. hidden files start with .
```
ls -la
```

#### Cat command

* Just to create empty file
```
touch [file-name]
```
* Create the file and open it to enter text. Enter the text and press ctrl+d to save.
```
cat > [file-name]
```
* Append the text to the file.
```
cat >> [file-name]
```
* Just open the file.
```
cat [file-name]
```

#### remove files
To remove any file.

```
rm [file-name]
```
To remove entire folder. -r means recursive.

```
rm -r [folder-name]
```

#### Copy and move

Copy the file.

```
cp [source] [destination]
```

Copy the folder into another folder, use recursive i.e -r
```
cp [source-folder] [dest-folder] -r
```

Move the file or folder.

```
mv [source-file-or-folder] [destination]
```

Rename the file also same command

```
mv [present-file-name] [new-file-name]
```

#### Others
find text in a file
```
grep [text-to-search] [file-name]
```

top 10 lines in a file.

```
head [file-name]
```

last 10 lines in a files

```
tail [file-name]
```

custom number of lines

```
head -n 5 [file-name]
```

#### File download

To download the file.

```
wget [download-URL]
```

To get the source and show the content in terminal.
```
curl [URL]
```



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

bg : List stopped or background jobs, resume a stopped jon in the background

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