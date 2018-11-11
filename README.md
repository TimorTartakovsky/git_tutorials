# GIT tutorial for a company needs


## Configuration 

[link to Git!](https://git-scm.com/)

Configure your credentials.

```
IN BASH

git config --global user.name "Your name"
git config --global user.email "Your email"
```


### Git core editor

Downnload Notepad++ editor as a commonly used.


```
IN BASH

alias npp="notepad++ -multiInst -nosession"
git config core.editor "notepad++ -multiInst -nosession"
```


### To look on the global config

```
IN BASH

git config --global -e
```

to leave the configuration press: 'shift' + ':' -> 'q' -> 'enter'<br />


### This tool is optional it allows you to work with merged files (pre-merge) and compare different commits

[to load it click here!](https://www.perforce.com/downloads/helix#clients)

find p4merge soft and download it.

```
IN BASH

git config --global diff.tool p4merge
git config --global difftool.p4merge.path "C:/Program Files/Perforce/p4merge.exe"
git config --global difftool.prompt false

git config --global merge.tool p4merge
git config --global mergetool.p4merge.path "C:/Program Files/Perforce/p4merge.exe"
git config --global mergetool.prompt false

```
<br />
Git state devided on three local sections and one remoted: 

"Working directory" - The files that were changed do the development process but untracked yet. <br />
"Staging directory" - The files that were accepted to a future commit 
"Tracked directory" - Comitted files

```
git status
``` 
this command shows  untracked files.
<br />

```
git add <file/s name>
git stage <file/s name>
```
this command prepare files to be tracked
<br />
```
git add .
```
allow to accept all the files
<br />

```
git commit -m "<T.Tartakovsky> #US_number 'Store the passed git tutorials' reviewer: Itamar"
```
This way we may do one commit and to commit all the added files run this
```
git commit
```
Then the multi commit window is opened and editable. To execute it press 'ctrl' + 's' -> 'ctrl' + 'w'
<br />

To see GIT inner folder:
```
cd .git
tree
```
It will show construction of a git tree.
<br />

```
rm -rf <folder name>
```
It will delete the file or folder
<br />

```
git log
git show
```
This too commands allows you to see details of the commits
<br />

```
git ls-files
```
Shows all the racked files.
<br />

```
git commit -am "Commit message"
```
It will track the files and then commit them.
<br />

```
git reset HEAD <file name>
```
It will unstage already staged file
<br />

```
git checkout <file name>
```
reset file on the state that was before it was modified.
<br />

```
git log --oneline --graph --decorate --all
```
Run this command to better see a tracking trace of commits.
<br />

```
git config --global alias.hist "log --oneline --graph --decorate --all"
```
It will help to shortcut this command :
```
git hist - short way to call it.
```
<br />

```
git config --global --list
```
This command will show you all the global configurations you have.
<br />

```
git hist -- <file name>
```
This showing the history of the particular file.
<br />

```
git mv <old file name> <new file name>
```
To change the file name, use this command.<br />
Then commit it.

```
git add -u
```
This command updates files before adding in to a stage.  (used in case some files changed the extension ....)
<br />

```
git add -A
```
adds all the modifications.


## Barnching and Merging

'HEAD' the last commit?

Answer. HEAD is a reference to the last commit in the currently check-out branch. You can think of the HEAD as the "current branch". <br />
When you switch branches with git checkout, the HEAD revision changes to point to the tip of the new branch. <br />
You can see what HEAD points to by doing: cat .git/HEAD. <br />

To manage a branches on your localhost just run the following commands: 
```
git branch
```
It will show you branch you working on  colored 'green' and other white in default configuration.
<br />

To create a new branch this command will help you. 
```
git checkout -b
```
<br />

To move from one branch to another: 
```
git checkout <branch name>
```
<br />

## Merging branches
