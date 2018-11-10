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
