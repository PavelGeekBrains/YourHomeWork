 **This is my git Tutorial**
 ==
![GIT LOGO](https://host-base.ru/wp-content/uploads/1/7/c/17c86d4f862234bbc3a2f0a432a9f850.jpeg)

> *Git* - распределённая система управления версиями. Git поддерживает быстрое разделение и слияние версий, включает инструменты для визуализации и навигации по нелинейной истории разработки. 
[Википедия](https://ru.wikipedia.org/wiki/Git)
### **Terms:**
* ***Репозиторий (repository)*** - совокупность файлов, состояние которых отслеживается, и история их изменений. По факту, репозиторий — это проект, над которым ведется работа, и все изменения в этом проекте. Для отслеживания состояния файла его необходимо добавить в репозиторий.
* ***Коммит (commit)*** - сохраненное состояние (версия) файлов репозитория.
* ***Ветка (branch)*** - последовательность коммитов (история изменения состояния репозитория).
* ***Мастер (master, main)*** - основная ветка репозитория, создается автоматически при создании репозитория.
* ***Чекаут (checkout)*** - переход на другое (существующее) состояние репозитория (на другой коммит или ветку).

### **basic commands we learned from the first lesson:**
* ***git init*** - команда для создания репозитория
* ***git status*** - команда для проверки текущего состояния репозитория
* ***git add*** - команда для "сохранения" текущего состояния проекта в истории коммитов
* ***git commit*** - команда для записи индексированных изменений в репозиторий
* ***git log*** - команда для просмотра истории коммитов
* ***git checkout*** - команда для проверки старых коммитов 
* ***git diff*** - команда для вывода изменений в файлах по сравнению с последним коммитом
---
### ***Questions***
* Что будет если переименовать файл в репозитории?
     * Как изменить message в уже отправленном коммите?
        * Как сделать чек-лист в md. документе?


# Second Seminar

1. Creating of new branches and switching between them 

* To create new branch use command *git branch branch_name*
* Use command *git checkout branch_name* to switch between branches
* You can use command *git checkout -b branch_name* to switch to a new branch. This is shortland for two command mentioned above. 

2. Branch merging

* To merge branches use command *git merge branch_name*
* Before merging make sure that you checked out the branch you wish to merge into. 

3.  Merge conflicts and resolutions

*  Conflicts appers when git is unable to merge parts cleanly if there are different changes in the same parts of the same file in the two merging branches. 

4. Branch deleting 

* To delete branch use comand *git branch -d branch_name* 

5. Summary

* Now we know how to create branches, switch between them, merge and delete unnecessary branches. 

---
# Third Seminar

### Working with remotes 

1. Showing remotes

- Use command *git remote* to see which remotes servers you have configured

2. Adding remote depositories 

- *git remote add (shortname) (url)* Use this command to add a new remote Git repository. 
- command *git clone* will add the copy of remote repository to your local repository with the name *origin* as a default name 

3. Pulling from your Remotes

- If your current branch is set up to track a remote branch using *git pull* command will automatically fetch and then merge that remote branch into your current branch.

4. Pushing to Remotes

- *git push* command will send all changes from your local repository to remote one 

5. Renaming and removings Remotes 

- You can run *git remote rename (first_name) (desired_name)* to change a remote’s shortname.
- *git remote remove* or *git remote rm* will remove a remote