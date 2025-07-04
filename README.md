# Day3

## TrainingISO file

In Linux, an ISO file is a single file containing a complete copy of the data from a CD, DVD, or other optical media, formatted as an ISO 9660 file system.

## Dual Boot

Dual booting allows a computer to run two different operating systems, enabling users to choose which one to boot into upon startup.

## VMware and Virtual box

VMware is a commercial product known for its enterprise-grade features, performance, and comprehensive support, while VirtualBox is an open-source, free alternative, generally favored for personal use, testing, and development.

## Bare metal installation

It refers to setting up an operating system directly on a physical server's hardware, without any intervening virtualization layer like a hypervisor.

## Partitioning schemes

^ Dividing a hard disk into separate sections.

^ Each section (partition) acts like an independent disk.

^ Helps organize data and install multiple OS.

### Types

#### MBR (Master Boot Record):

^ Max 4 primary partitions.

^ Supports up to 2 TB.

^ Older, used with BIOS.

^ less flexible

#### GPT (GUID Partition Table):

^ Supports 128+ partitions.

^ Works with disks >2 TB.

^ Newer, used with UEFI.

^ more flexible

## Permissions & Shell programming:
#### File and directory permissions:

chmod (Change mode): It is used to change the access permissions of files and directories For the owner, group,and others. syntax :

## chmod [permissions] [file_name]

For example: chmod + x filename.sh

chmod +x filename.sh

The command chmod +x filename.sh is used to add execute permission to a file (usually a script like .sh), so it can be run as a program.

 Syntax Breakdown

Component	Description
chmod	Stands for Change Mode – used to change file permissions
+x	Adds execute permission
filename.sh	The name of the shell script file
Purpose
This command makes a file executable by the user, group, and others (by default). You can then run the script directly using:

./filename.sh
Without execute permission, you'll see:

bash: ./filename.sh: Permission denied

To give execute permission only to the file owner, use:

chmod u+x filename.sh
This is a safer option when sharing code in teams or on public systems.

Octal Permission Codes:
Number	Symbol	Meaning
7	rwx	Read, Write, Execute
6	rw-	Read, Write
5	r-x	Read, Execute
4	r--	Read only
0	---	No permissions
example:
chmod +x test.sh: Gives permission to run the script.

chmod 444 test.sh: Changes file to read-only image
r-- r-- r--

result
image

chmod 644 test.sh: Changes file such that only owner can edit it. For others it remain read-only. image
rw- r-- r--

result
image

chown :
How to Use chown:

Check current ownership (optional).
Run the chown command. Use sudo if you're not the current owner. used for Changing owner only:
Changing group only:

Changing both group and owner permissions:

## Redirection:

In Linux, whenever an individual runs a command, it can take input, give output, or do both. Redirection helps us redirect these input and output functionalities to the files or folders we want, and we can use special commands or characters to do so.

###  Types of Redirection:

Overwrite Redirection (For stdout): Overwrite redirection is useful when you want to store/save the output of a command to a file and replace all the existing content of that file. for example, if you run a command that gives a report, and you want to save the report to the existing file of the previous report you can use overwrite redirection to do this.
">" standard output

#### Append Redirection (For stdout):

With the help of this Redirection, you can append the output to the file without compromising the existing data of the file. image image

#### Overwrite Redirection (For stdin):
Redirects the standard input of a command to a file. "<" standard input

sorting with help of Redirection:
image

Pipe '|':
A pipe is a form of redirection (transfer of standard output to some other destination) that is used in Linux and other Unix-like operating systems to send the output of one command/program/process to another command/program/process for further processing.You can make it do so by using the pipe character '|'. Pipe for filtration: image

for finding multiple files: to find number of files/directory consisting p image


