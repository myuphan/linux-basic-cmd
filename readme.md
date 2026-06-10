# 🐧 Linux Fundamentals & Bash Notes

Nothing much. This repository contains my Linux learning notes and command-line practice using Bash on WSL Ubuntu.

The goal of this project is to build a strong foundation in:
- Linux filesystem navigation
- Bash commands
- File management
- Searching and documentation tools
- Linux command-line workflow

---


## The shell
In this project, we'll focus on the Bash - the default shell for most Linux distribution

## Command Line 

### echo - Print text to the terminal
echo "Hello world"


### pwd (print working directory): to find the 'current directory linux'

/
├── home
├── etc
├── var
├── usr
├── bin
├── dev
└── tmp

/: root directory
/root: root user's home folder

### cd : to change your current directory
cmd.exe /c echo %USERNAME% : find users name

cd /home/phanu: move to phanu

### ls : list the directories and files in your command

ls -a: view hidden files like .file
ls -l: provide detailed list of files in a long format

myu@icebox:~$ ls -l
total 80
drwxr-x--- 7 pete penguingroup   4096 Nov 20 16:37 Desktop
drwxr-x--- 2 pete penguingroup   4096 Oct 19 10:46  Documents
drwxr-x--- 4 pete penguingroup   4096 Nov 20 09:30 Downloads

ls -r: source in order

### touch: create an empty file

touch file.txt

linux touch -r:  allows you to set a file's timestamp to match that of another file (a reference file). This is useful for synchronizing timestamps across related files.

#### Set file2.txt's timestamp to match file1.txt's timestamp
touch -r file1.txt file2.txt

#### Set the timestamp to a specific date and time
touch -d "2023-01-01 12:30:00" mysuperduperfile

### rm: remove file
rm -f
rm -i
rm -r directory
rmdir empty_directory

### file: find the type of file

find banana.jpg 

Note: banana.jpg is not nessessary a .jpg format

### cat: viewing file contain

#### cat > newfile 
enable to write the newfile's contain. If newfile is an existing file, file will be overwritten 

ctrl +D to exit

What if you overwrite the file accidentally? 
cat > newfile then ctrl+D to rescue

### Less: to view super duper large file

g: move to the beginning of the file
G: jump to the end
h: help menu
/" search here"
quit: q

### cp: copy

cp + file + directories/new_name

cp mycoolfile /home/pete/Documents/mycoolfile_backup
cp *.jpg /home/pete/Pictures

cp will perform overwrite, to avoid it, use 
cp -i + file + directory to confirm file is exist

preserve original database
cp -p + file +directory
### mv: move

rename a file
mv oldfile newfile

redirectory (rename folder in window)
mv old directory name new_directory_name

move a file to another directory
mv file /home/phanu/documents

again, mv -i for confirmation for overwrting


mv -b
Move the file, but if something already exists, don’t delete it — just save a copy of the old one.

echo "oldfile" > folder/file.txt
echo "newfile" > file.txt
mv -b file.txt folder/

so we have two files:
file.txt
file.txt~

### mkdir: make new directory
create multiple directory


### find 
find [path] [expression]

find /home -name puppies.jpg

find /home -type d -name MyFolder

### help 
help echo: display summary function for echo

### man
 man ls: access manual

### what is 

whatis cat: shorter version to describe cat command

### alias
a quick command (temporary) for combination of command

alias ll ='ls -la'

make alias permanent

open the file in a text editor: nano ~/.bashrc
alias ll='ls -la'
alias update='sudo apt update && sudo apt upgrade'



change is made




