# Shell commads
##### pwd
shows the current path in a hierarchical directory
##### cd
change directory
##### ls
list files and directories
##### arguments
[directory name]
/ root
. current directory
.. upper-level directory
~ home of current user
/[directory name]: absolute path
./[directory name]: relative path
../[directory name]: relative path
##### options
- l show detailed information (long format)
- lh same as above, but size in units

##### More on ls
it is commonly used Linux command. it can be used in a number of different ways. Here are some ls commands examples.
[command]
```
ls : List the files in the working directory
ls /bin : List the files in the /bin directory (or any other directory we care to specify)
ls -1 : List the files in the working directory in long format
ls -1: /etc /bin : List the files in the /bin directory and the /etc directory in long format
ls -la .. : List all files (even ones with names beginning with a period character, which are normally hidden) in the parent of the working directory in long format
```
---
### [Tip]
- 1\. Tap key  : Autocompletion
- 2\. up arrow key : Past commands

---
##### clear
Clear all commands and return to the first line.

---
### Manipulation
##### cp
copy files and directories.
[command]
```
cp files1 files2 : copies the contents of file1 into files2. if file2 does not exist, it is created. otherwise, file2 is silently overwritten with the contents of file1.
cp -i file1 file2 : -i option is specified, if file2 exists, the user is prompted before it is overwritten with the contents of file1.
cp file1 dir1 : copy the contents of file1 inside of directory dir1.
cp -R dir1 dir2 : copy the contents of the directory dir1. If directory dir2 does not exist, it is created. Otherwise, it creates a directory named dir1 within directory dir2.
```
##### mv
move files and directories or rename them.
[command]
```
mv file1 file2 : If file2 does not exist, then file1 is renamed file2. If file2 exists, its contents are silently replaced with the contents of file1.
mv -i file1 file2 : -i option is specified, if file2 exists, the user is prompted before it is overwritten with the contents of file1.
mv file1 file2 dir1 : The files file1 and file2 are moved to directory dir1. If dir1 does not exist, mv will exit with an error.
mv dir1 dir2 : If dir2 does not exist, the dir1 is renamed dir2. If dir2 exists, the directory dir1 is moved within directory dir2. 
```
##### rm
delete files and directories ***permantely and irreversevely!***
[command]
```
rm files1 files2 : delete file1 and file2.
rm -i file1 file2 : -i option is specified, the user is prompted before each file is deleted.
rm -r dir1 dir2 : directories dir1 and dir2 are deleted along with all of their contents.
```

##### mkdir
make a new directory.(make a sub-directory in current directory)
##### Wildcards
[paterns]
```
* : all filenames
g* : all filenames that begin with the character "g"
b* .txt : all filenames that begin with the character "b" and end with the characters ".txt"
Data??? : any filename that begins with the characters "Data" followed by exactly 3 more characters
```
[command]
```
cp *.txt text_files : copy all files in the current working directory with names ending with the characters ".txt" to an existing directory named text_files.
mv dir1 ../*.bak dir2 : move the subdirectory dir1 and all the files ending in ".bak" in the current working directory's parent directory to an existing directory named dir2.
rm *~ : delete all files in the current working directory that end with the character "~". Some applications create backup files using this naming scheme. Using this command will clean them out of a directory.
```

##### Caution
***Before using rm, use ls instead!!***

---
##### Help command
- help
- man

When the user types 'help' or 'man' and enter a command, a descrption of the command appears.
##### exit
it means 'exiting terminal'