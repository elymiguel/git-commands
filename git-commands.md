# Git & GitHub - Commands

### Commands
- git init 
- git add . 
- git add index.html style.css 
- git commit -m "New Commit"
- git status

### Config
- git config --global --edit

- git config --global user.name "your_user"
- git config --global user.mail "your@mail.com"

- git config --global --unset user.name
- git config --global --unset user.mail

### Git to GitBub
- git remote -v
- git remote add origin https://github.com/elymiguel/git-commands.git
- git push origin master
- git pull origin master
- git clone https://github.com/elymiguel/git-commands.git

### Modificar Branch
- git checkout -b main

### Logs de Commits
- git log --online

### List Branch
- git branch --list
### Change Branch
- git branch -m master main