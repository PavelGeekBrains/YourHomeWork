## Работа с удалённым репозиторием.

### …or create a new repository on the command line

* echo "# TestRepo" >> README.md
* git init
* git add README.md
* git commit -m "first commit"
* git branch -M main (master)
* git remote add origin https://github.com/ BlockchainOff/TestRepo.git
* git push -u origin main (master)

### …or push an existing repository from the command line
* git remote add origin https://github.com/BlockchainOff/TestRepo.git
* git branch -M main
* git push -u origin main

git push - отправка комита на удалённый репозиторий.
git pull - вытягивания из удалённой ветки.