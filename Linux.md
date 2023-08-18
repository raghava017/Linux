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

 # Root user

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

