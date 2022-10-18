# Git commads
---

### Git config: First-time setup
Git configurations are stored in three levels: 
(1) System level: --system option. Affects all uses and repositories on the system. (administrative)
**file:/etc/gitconfig**
(2) Global (user) level: --global option. Affects all repositories of a current user
**file:~/.config/git/config**
(3) Local level: --local option. Specific to the current repository
**file: .git/gitconfig**

**Each level overrides values in the previous level: system->global->local**

---
### Initializing a Repository in an Existing Directory
**$ git init**
Command $git init creates a sub-directory '.git' in an open source directory.
---
### Checking Repository Status
**$ git status**
It is used to determine what state the repository is in and where it is located in what file or directory.
---
### Adding a new file to be staged(tracked)
**$ git add [file_name]**
After writing the command and the file name, It can upload a specific file to the staging area.
(Caution: After putting the content on the staging area, when additional contents are needed, '*$ nano words.txt*' command changes the contents)
---
### Adding all files to be staged(tracked)
**$ git add .**
It posts all files and directories in the current directory together in the staging area.
---
### Unstaging a file
**$ git rm --cached[file_name]**
It can unstaging files that users don't want to commit.
---
### Ignoring a file
**$ nano .gitignore**
' .gitignore' is not command.
---
### Commit
**$ git commit -m "commit message"**
It is to record a specific version of the files, directories that are posted on the staging.
"commit message" is not an essential element.