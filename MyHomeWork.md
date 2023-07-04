## Home Work 3

### Remote repository

### Push an existing repository from the command line

* *git remote add origin https://github.com/name_remote_repository.git* - команда связи между локальным репозиторием и удаленным, основным репозиторием хранения информации будет удаленный репозиторий;

* *git branch -M master* -команда для определения основной ветки;

* *git push -u origin master* - команда отправляющая текущее состояние локального репозитория;
* *-u* -команда резрешения для быстрой отправки/получения;
* *origin* - текущее состояние.

### Example of transferring information to a remote repository

* Change from local repository

* *git push* - - команда отправляющая текущее состояние локального репозитория, если связь уже установлена;

* ### Example of transferring information from a remote repository

*  Change from remote repository

*  ### Действия для сохранения текущего сотсояния через удаленный репозитарий на github

*  - нет необходимости сохранять изменений (ctrl+s)
   - первый шаг кнопка *commit changes..*
   - *сommit message* команда аналог команды *git commit -m "name_commit"*
   - Extended description -расширенное описание, не обязательн
   - *Commit directly to the master branch* - команда добавления в ветку master
   - *Create a new branch for this commit and start a pull request* - создание новой ветки с запросом на одобрение изменений
