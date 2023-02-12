## Работа с удаленными репозиториями

### Создание нового репозитория и привязка его к удаленному репозиторию

* создание файла README.md
* git init
* git add README.md
* git commit -m "first commit"
* git branch -M master
* git remote add origin [remote_repository_url]
* git push -u origin master


### Отправка локального репозитория в удаленный
* git remote add origin [remote_repository_url]
* git branch -M master
* git push -u origin master


**git pull** — получение изменений из удаленного репозитория в локальный

Сценарий работы:

* Добавляем или изменяем файлы в локальном репозитории;
* git add ... / git commit -m ... в локальном репозитории;
* git push — для публикации изменений в удаленном репозитории.

### Использование Fork
1. Делаем fork репозитория;
2. Клонируем репозиторий и открываем в VSCode;
3. Создаем побочную ветку;
4. В побочной ветке создаем отдельный файл;
5. Делаем push ветки;
6. Оформляем pull request;
7. Profit!