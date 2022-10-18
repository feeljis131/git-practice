# Shell commads
---
### I/O Redirection: Standard Output
Standard output is screen.
1. ">" : it creates and saves the output in a file
2. ">>": it appends output to an existing file (if it already exists), or create and write to a new file if it doesn't exist.

Command "cat": it displays the content of a text file.  
### I/O Redirection: Standard Input
Standard input is from keyboard.
1. ">": it directs input from a file.
2. "<"and ">": they can mix together in a single line.
---

### Pipelines "|"
Pipeline feeds output of previous command to input of next command.
For example, **command1 | command2 | command3**
 -> The output of command 1 becomes the input of command 2, and the output of command 2 becomes the input of command 3.
(Pressing 'q' key can exit the screen.)
---
### Expansion
Special Characters expand its meaning when given to shell commands.
- echo: it prints text after 'echo'.
- echo *: it prints the file of the current directory.
- echo ~: it prints the current user's home directory.

### [Tip]: Backslash
Backslash can be used to ignore line change in command "enter", to enter a long command in multiple lines.

---
### Permission
- Linux is a multi-user system.
- Files and directories have a permisson assigned differently to owner/group/others.

Default: **-rwx rwx rwx**
-: File type, - indicates regular file, d indicates directory.
the first three digits: read,write,and execute permissions for the file owner.
the second three digits: read,write,and execute permissons for the group owner of the file.
the third three digits: read,write,and execute permissons for all other users.
### Changing Permissons
- "chmod" changes permissons.

rwx = 111 in binary = 7
rw- = 110 in binary = 6
r-x = 101 in binary = 5
r-- = 100 in binary = 4
[Value : Meaning]
```
777: (rwxrwxrwx) No restrictons on permissons. Anobody may do anything. Generally not a desirable setting.
755: (rwxr-xr-x) The file's owner may read, write, and execute the file. All others may read and execute the file. This setting is common for programs that are used by all users.
700: (rwx------) The file's owner may read, write, and execute the file. Nobody else has any rights. This setting is useful for programs that only the owner may use and must be kept private from others.
666: (rw-rw-rw-) All users may read and write the file.
644: (rw-r--r--) The owner may read and write a file, while all others may only read the file. A common setting for data files that everybody may read, but only the owner may change.
600: (rw-------) The owner may read and write a file. All others have no rights. A common setting for data files that the owner wants to keep private.
```
Change the permisson of a file "word.txt" that only the owner (you) can read and write, but all the others (including others in the group) can only read it. No execution is needed for all users.

---
### Superuser
it has all system administation authority.
Some commands need superuser's privilleges.
Put "sudo" before the command if you are a superuser.
(It is recommended not to use it normally, but only when necessary.)
Type "exit" to get out of a superuser session.
---
### Text Editors
In Linux, you can choose CLI-based or GUI-based text editors.
[Name : Description : Interface]
```
vi, vim: It is difficult for beginners to use. Most of them use keyboard shortcuts and are often used by experts.: command line
Emacs: It's not very important.: command line
nano: It's good for beginners to use.: command line
gedit: It's good for beginners to use. Especially, the interface is Gui, so it is good for beginners to use.: graphical
kwrite: It's good for beginners to use. Especially, the interface is Gui, so it is good for beginners to use.: graphical
```
---
### Shell Script
Write and run a shell script.
### [Tip]: History
Type "history" to see previous command history or save it to a text file.
