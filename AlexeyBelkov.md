# Git ReadMe

## Работа с ветками

Для просмотра всех существующих веток, необходимо применить следующую команду:
* git branch

*git status* - позволит отобразить текущее состояние проэкта и местонахождение в материале

### Добавление новой ветки

Для добавления ветки используется следующая команда:
* git branch ``branch_name``

### Переход между ветками

Для перехода между ветками применяется команда:
* git checkout ``branch_name``

### Слияние веток 

Для слияния двух веток, используем команду:
* git merge ``branch_name``

**Важные моменты при слиянии**

1. В момент слияния мы должны находиться в ветке, где будем изменять файлы путём слияния
2. "``branch_name``" - название ветки, присоединение, или слияние которой будет происходить

**Слияние может произойти чисто(без дополнительных действий и вмешательств в дифузию материала), или с конфликтом (если мы работаем с VS Code), при котором возникает ``3`` варианта развития событий:**

1. Оставить в основной ветке её версию данных.

2. Заменить данные основной ветки на данные вливаемой ветки.

3. Оставить оба варианта, для возможности вручную указать итоговые данные.

### Удаление ветки

Для удаления ветки, применяем команду:
* git branch -d ``brabch_name``

*Вниминие!* - перед удалением ветки, убедитесь в том, что она больше не потребуется

## Работа с удалёнными репозиториями

1. Для того, чтобы просмотреть список настроенных удаленных репозиториев, вы можете запустить команду *git remote*. Она выведет названия доступных удаленных репозиториев. Если вы клонировали репозиторий, то увидите как минимум origin - имя по умолчанию, которое Git дает серверу, с которого производилось клонирование:

* _$ git clone https://github.com/schacon/ticgit
Cloning into 'ticgit'...
remote: Reusing existing pack: 1857, done.
remote: Total 1857 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (1857/1857), 374.35 KiB | 268.00 KiB/s, done.
Resolving deltas: 100% (772/772), done.
Checking connectivity... done.
$ cd ticgit
$ git remote
origin_

* Вы можете также указать ключ -V, чтобы просмотреть адреса для чтения и записи, привязанных к репозиторию:

_$ git remote -v
origin	https://github.com/schacon/ticgit (fetch)
origin	https://github.com/schacon/ticgit (push)_ 

* Если у вас больше одного удаленного репозитория, команда выведет их все. Например, для репозитория снесколькими удалёнными репозиториями в случаау совместной работы несколькиз пользователей, вывод команды может выглядеть примерно так:

_$ cd grit
$ git remote -v
bakkdoor  https://github.com/bakkdoor/grit (fetch)
bakkdoor  https://github.com/bakkdoor/grit (push)
cho45     https://github.com/cho45/grit (fetch)
cho45     https://github.com/cho45/grit (push)
defunkt   https://github.com/defunkt/grit (fetch)
defunkt   https://github.com/defunkt/grit (push)
koke      git://github.com/koke/grit.git (fetch)
koke      git://github.com/koke/grit.git (push)
origin    git@github.com:mojombo/grit.git (fetch)
origin    git@github.com:mojombo/grit.git (push)_

* Это означает, что мы можем легко получить изменения от любого из этих пользователей. Возможно, что некоторые из репозиториев доступны для записи и в них можно отправлять свои изменения, хотя вывод команды не даёт никакой информации о правах доступа.

* Для того, чтобы добавить цдалённый репозиторий и присвоить ему имя (shortname), просто выполните команду git remote add <shortname> <url>:

 _$ git remote
origin
$ git remote add pb https://github.com/paulboone/ticgit
$ git remote -v
origin	https://github.com/schacon/ticgit (fetch)
origin	https://github.com/schacon/ticgit (push)
pb	https://github.com/paulboone/ticgit (fetch)
pb	https://github.com/paulboone/ticgit (push)_

* Теперь вместо указания полного пути вы можете использовать ``pb``. Например, если вы хотитеполусить изменения, которые есть у Антония, но нету у вас, вы можете выполнить команду git fetch pb:

$ git fetch pb
remote: Counting objects: 43, done.
remote: Compressing objects: 100% (36/36), done.
remote: Total 43 (delta 10), reused 31 (delta 5)
Unpacking objects: 100% (43/43), done.
From https:``ссылка Антония``
 * [new branch]      master     -> pb/master
 * [new branch]      ticgit     -> pb/ticgit

 * Ветка master из репозитория Антония сейчас доступна вам под именем pb/master. Вы можете слить её с одной из ваших веток, или переключить на неё локальную ветку, чтобы просмотреть содержимое ветки Антония. 

2. Получение изменений из удалённого репозитория - ``Fetch`` и ``Pull``

* Как вы только что узнали, для получения данных из удалённых проектов, следует выполнить:

``git fetch [remote-name]``

Данная команда сязывается с указанным удалённым проектом и забирает все те данне проекта, которых у вас еще нет. После того как вы выполнили команду , у вас должны появиться ссылки на все ветки из этого удалённого проекта, которые вы можете просмотреть или слить в любой момент.

* Когда вы клонируете репозиторий, команда ``clone`` автоматически добавляет этот удалённый репозиторий под именем ``origin``. Таким образом, ``git fetch origin`` извлекает всу наработки, отправленные на этот сервер после того, как вы его елонировали (или получили измкнкния с помощью ``fetch``). Важно отметить, что команда ``git fetch`` забирает данные в ваш локальный репозиторий, но не сливает их с какими-либо вашими наработками и не модифицирует то, над чем вы работаете в данный момент. Вам необходимо вручную слить эти данные с вашими, когда вы будете готовы.

## Отправка изменений в удалённый репозиторий(Push)

* Когда вы хотите поделиться своими наработками, вам необзодимо отправить их в удалённый репозиторий. Команда для этого действия простая : ``git push <remote-name> <branch-name>``. Чтобы отправить вашу ветку master  на сервер ``origin``, можете выполнить слудующую команду для отправки ваших коммитов:

*git push origin master*

    Эта команда срабатывает толко в случае, ксли вы клонировали с сервера, на котором у вас есть права на запись, и если никто другой с тех пор не выполнял команду ``push``. Если вы и кто-то ещё одноовременно клонируктк, затем он выполняет команду ``push``, а после него выполнить команду ``push`` попытаетесь вы, то ваш ``push`` точно будет отклонён. Вам придётся сначала получить изменения и объединить их с вашими и толко после этого вам будет позволено выполнить ``push``.


## Просмотр удаленного репозитория

* Если хотите получить поболише информации об одном из удалённых репозиториув, вы можете использовать команду ``git remote show <remote>``. Выполнив эту команду с некоторым именем, например, ``origin``, вы получите следующий результат:

``$ git remote show origin``
*  _remote origin
  Fetch URL: https://github.com/schacon/ticgit
  Push  URL: https://github.com/schacon/ticgit
  HEAD branch: master
  Remote branches:
    master                               tracked
    dev-branch                           tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)_
    Она выдаёт ``URL`` удалённого репозитория, а также информацию об отслеживаемых ветках. Эта команда любезно сообщает вам, что если вы, находясь на ветке ``master``, выполните ``git pull``, ветка ``master`` с удалённого сервера будет автоматически влита в вашу сразу после получения всех необходимых данных. Она также выдаёт список всех полученных ею ссылок.


**Это был пример для простой ситуации и вы наверняка встречались с чем-то подобным. Однако, если вы используете Git более интенсивно, вы можете увидеть гораздо большее количество информации от ``git remote show``**:

    $ git remote show origin
* remote origin
  URL: https://github.com/my-org/complex-project
  Fetch URL: https://github.com/my-org/complex-project
  Push  URL: https://github.com/my-org/complex-project
  HEAD branch: master
  Remote branches:
    master                           tracked
    dev-branch                       tracked
    markdown-strip                   tracked
    issue-43                         new (next fetch will store in remotes/origin)
    issue-45                         new (next fetch will store in remotes/origin)
    refs/remotes/origin/issue-11     stale (use 'git remote prune' to remove)
  Local branches configured for 'git pull':
    dev-branch merges with remote dev-branch
    master     merges with remote master
  Local refs configured for 'git push':
    dev-branch                     pushes to dev-branch                     (up to date)
    markdown-strip                 pushes to markdown-strip                 (up to date)
    master                         pushes to master                         (up to date)

    __Данная команда показывает какая именно локальная ветка будет отправлена на удалённый сервер по умолчанию при выполнении ``git push``. Она также показывает, каких веток с удалённого сервера у вас ещё нет, какие ветки всё ещё есть у вас, но уже удалены на сервере, и для нескольких веток показано, какие удалённые ветки будут в них влиты при выполнении ``git pull``.


## Удаление и переименование удалённых репозиториев 

 *Для переименования удалённого репозитория можно выполнить ``git remote rename``. Например, если вы хотите переименовать ``pb`` в ``paul``, вы можете это сделать при помощи ``git remote rename``: 

    $ git remote rename pb paul
    $ git remote
    origin
    paul

* Стоит упомянуть, что это также изменит имена удалённыз веток в вашем репозитории. ТоЮ к чему вы обращались как ``pb/master``, теперь стало ``paul/master``.

* Если по какой-то причине вы хотите удалить удаленный репозиторий - вы сменили сервер, или больше не используете определённое зеркало, или кто-то перестал вносить изменения - вы можете использовать ``git remote rm``:
    
    *git remote remove paul*
   
     *git remote origin*


* При удалении ссылки на удалённый репозиторий все отслеживаемые ветки и настройки, связанные с этим репозиторием, так же будут удалены.

                                ***

            Файл изготовлен, при поддержке головы рукой.