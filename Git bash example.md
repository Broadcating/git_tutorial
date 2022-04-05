```git
bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ eval $(ssh-agent -s)
Agent pid 512

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ ssh-add ~/.ssh/id_rsa
Identity added: /c/Users/bearr/.ssh/id_rsa (antti.kokko.kalmah@gmail.com)

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ cat ~/.gitconfig --global user.name
cat: unknown option -- global
Try 'cat --help' for more information.

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ git config --global user.name

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ cat ~/.gitconfig
[core]
        editor = \"C:\\Users\\bearr\\AppData\\Local\\Programs\\Microsoft VS Code\\bin\\code\" --wait

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ git config --global user.name "Bear"

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ git config --global user.email "antti.kokko.kalmah@gmail.com"

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ cat ~/.gitconfig
[core]
        editor = \"C:\\Users\\bearr\\AppData\\Local\\Programs\\Microsoft VS Code\\bin\\code\" --wait
[user]
        name = Bear
        email = antti.kokko.kalmah@gmail.com

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ mkdir git_workspace

bearr@LAPTOP-8JOOUUQO MINGW64 ~
$ cd git_workspace

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace
$ where git_workspace
INFO: Could not find files for the given pattern(s).

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace
$ mkdir git_tutorial

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace
$ cd git_tutorial

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial
$ git init
Initialized empty Git repository in C:/Users/bearr/git_workspace/git_tutorial/.git/

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ ll
total 0

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ touch README.md

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git add README.md

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md


bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git rm --cached README.md
rm 'README.md'

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git Add A
fatal: cannot handle Add as a builtin

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git add -A

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ ll -la
total 4
drwxr-xr-x 1 bearr 197609 0 Apr  4 00:44 ./
drwxr-xr-x 1 bearr 197609 0 Apr  4 00:43 ../
drwxr-xr-x 1 bearr 197609 0 Apr  4 00:48 .git/
-rw-r--r-- 1 bearr 197609 0 Apr  4 00:44 README.md

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ cd .git

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial/.git (GIT_DIR!)
$ ll
total 8
-rw-r--r-- 1 bearr 197609  23 Apr  4 00:44 HEAD
-rw-r--r-- 1 bearr 197609 130 Apr  4 00:44 config
-rw-r--r-- 1 bearr 197609  73 Apr  4 00:44 description
drwxr-xr-x 1 bearr 197609   0 Apr  4 00:44 hooks/
-rw-r--r-- 1 bearr 197609 104 Apr  4 00:48 index
drwxr-xr-x 1 bearr 197609   0 Apr  4 00:44 info/
drwxr-xr-x 1 bearr 197609   0 Apr  4 00:46 objects/
drwxr-xr-x 1 bearr 197609   0 Apr  4 00:44 refs/

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial/.git (GIT_DIR!)
$ cat index
DIRCbI▒dvxbI▒q_▒▒▒▒⛲▒▒CK▒)▒wZ▒▒▒S▒     README.m▒b▒▒bp▒▒▒ ▒▒▒o$H)
bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial/.git (GIT_DIR!)
$ ..
bash: ..: command not found

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial/.git (GIT_DIR!)
$ cd ..

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git commint -m "add README.md"
git: 'commint' is not a git command. See 'git --help'.

The most similar command is
        commit

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md


bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git remote add origin https://github.com/Broadcating/git_tutorial.git

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git remote -v
origin  https://github.com/Broadcating/git_tutorial.git (fetch)
origin  https://github.com/Broadcating/git_tutorial.git (push)

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git push origin master -u
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/Broadcating/git_tutorial.git'

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md


bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git commit -m "creat README.md"
[master (root-commit) d5d45e0] creat README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git status
On branch master
nothing to commit, working tree clean

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
$ git push -u origin master
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 220 bytes | 220.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Broadcating/git_tutorial.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

bearr@LAPTOP-8JOOUUQO MINGW64 ~/git_workspace/git_tutorial (master)
```