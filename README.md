**Лабораторная работа №1**
В ходе работы было выполнено подключение к данному репозиторию с MacOS.
Выполнена синхронизация файлов greeting.py и hello.py.
SSH-ключ сгенерирован и успешно добавлен в аккаунт GitHub (проверка командой ssh прошла успешно).
Git сконфигурирован с указанием имени и email.
Локальный репозиторий проинициализирован.
Создан удаленный репозиторий на GitHub, и ветка main успешно отправлена в него (git push).
Создана и merged ветка feature/greeting (история коммитов и файлы на GitHub это
подтверждают).
В репозитории на GitHub присутствует файл greeting.py.
Код в файле greeting.py рабочий (можно проверить по предоставленному скриншоту
test_result.png).
Вся работа выполнена через командную строку Ubuntu (терминал), использование GUI VSCode
для операций Git сведено к минимуму или не использовалось.
SSH-ключ защищен паролем (passphrase).
log:
"""
Last login: Thu Sep  4 09:38:33 on console
whifff@MacBook-Air-Aleksandr-2 ~ % ssh-keygen -t ed25519 -C "aks1de1337@ya.ru"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/Users/whifff/.ssh/id_ed25519): 
Created directory '/Users/whifff/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/whifff/.ssh/id_ed25519
Your public key has been saved in /Users/whifff/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:n0d6f0OOZLhct8Oq09Tbv0EkDOUr0bJHy47BkzuOcxk aks1de1337@ya.ru
The key's randomart image is:
+--[ED25519 256]--+
|           ...   |
|            =    |
|           o * . |
|          . B =  |
|        S  Bo=.. |
|         . EO=.+ |
|          =+%.*.+|
|         .oO.+ B+|
|         .ooo.oo*|
+----[SHA256]-----+
whifff@MacBook-Air-Aleksandr-2 ~ % eval "$(ssh-agent -s)"
Agent pid 13759
whifff@MacBook-Air-Aleksandr-2 ~ % ssh-add ~/.ssh/id_ed25519
Enter passphrase for /Users/whifff/.ssh/id_ed25519: 
Identity added: /Users/whifff/.ssh/id_ed25519 (aks1de1337@ya.ru)
whifff@MacBook-Air-Aleksandr-2 ~ % cat ~/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAILQqvboaCprfBlptPLWfL9oTCEyO9iM2pXkW4pMjMmQ8 aks1de1337@ya.ru
whifff@MacBook-Air-Aleksandr-2 ~ % ssh -T git@github.com    
The authenticity of host 'github.com (140.82.121.4)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
Hi wh1fff! You've successfully authenticated, but GitHub does not provide shell access.
whifff@MacBook-Air-Aleksandr-2 ~ % ssh -T git@github.com
Hi wh1fff! You've successfully authenticated, but GitHub does not provide shell access.
whifff@MacBook-Air-Aleksandr-2 ~ % SHA256:n0d6f0OOZLhct8Oq09Tbv0EkDOUr0bJHy47BkzuOcxk
zsh: command not found: SHA256:n0d6f0OOZLhct8Oq09Tbv0EkDOUr0bJHy47BkzuOcxk
whifff@MacBook-Air-Aleksandr-2 ~ % cat ~/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAILQqvboaCprfBlptPLWfL9oTCEyO9iM2pXkW4pMjMmQ8 aks1de1337@ya.ru
whifff@MacBook-Air-Aleksandr-2 ~ % git
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
whifff@MacBook-Air-Aleksandr-2 ~ % git config --global user.name "александр"
whifff@MacBook-Air-Aleksandr-2 ~ % git config --global user.email "aks1de1337@yandex.ru"
whifff@MacBook-Air-Aleksandr-2 ~ % git config --global core.editor "code --wait"
whifff@MacBook-Air-Aleksandr-2 ~ % mkdir python-git-lab1
whifff@MacBook-Air-Aleksandr-2 ~ % cd python-git-lab1
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % code .
zsh: command not found: code
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git init
Initialized empty Git repository in /Users/whifff/python-git-lab1/.git/
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git add hello.py
fatal: pathspec 'hello.py' did not match any files
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git add hello.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git commit -m "Add initial hello.py script"
[main (root-commit) f355faa] Add initial hello.py script
 1 file changed, 1 insertion(+)
 create mode 100644 hello.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   hello.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store

no changes added to commit (use "git add" and/or "git commit -a")
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git add hello.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git commit -m "Add a new print statement to hello.py"
[main 33739c5] Add a new print statement to hello.py
 1 file changed, 2 insertions(+), 1 deletion(-)
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git log --oneline 
33739c5 (HEAD -> main) Add a new print statement to hello.py
f355faa Add initial hello.py script
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git checkout -b feature/greeting
Switched to a new branch 'feature/greeting'
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git create 
git: 'create' is not a git command. See 'git --help'.

The most similar command is
	reset
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git add greeting.py
fatal: pathspec 'greeting.py' did not match any files
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git add greeting.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git commit -m "Add a new greeting module with user input" 
[feature/greeting 600502f] Add a new greeting module with user input
 1 file changed, 1 insertion(+)
 create mode 100644 greeting.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git checkout main
Switched to branch 'main'
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % ls
hello.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git merge feature/greeting
Updating 33739c5..600502f
Fast-forward
 greeting.py | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 greeting.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % ls
greeting.py	hello.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git remote add origin git@github.com:wh1fff/python-git-lab1.git
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git push -u origin main
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (9/9), 855 bytes | 855.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0
giTo github.com:wh1fff/python-git-lab1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git push origin feature/greeting
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'feature/greeting' on GitHub by visiting:
remote:      https://github.com/wh1fff/python-git-lab1/pull/new/feature/greetin
remote: 
To github.com:wh1fff/python-git-lab1.git
 * [new branch]      feature/greeting -> feature/greeting
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % python3 greeting.py
как вас зовут? Wh1fff
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   greeting.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store

no changes added to commit (use "git add" and/or "git commit -a")
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git commit -m "Add a new greeting module with user input v2"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   greeting.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store

no changes added to commit (use "git add" and/or "git commit -a")
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git add greeting.py
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git commit "Add a new greeting module with user input v2" 
error: pathspec 'Add a new greeting module with user input v2' did not match any file(s) known to git
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git commit -a "Add a new greeting module with user input v2"
fatal: paths 'Add a new greeting module with user input v2 ...' with -a does not make sense
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   greeting.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store

whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git ignore .DS_Store
git: 'ignore' is not a git command. See 'git --help'.

The most similar command is
	diagnose
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   greeting.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store
	README.md

whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git add README.md
whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   README.md
	modified:   greeting.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store

whifff@MacBook-Air-Aleksandr-2 python-git-lab1 % 
"""