README.md - описание репозитория для сторонних пользователей 

В Git ignore отправляются файлы  медиаформата (видео, картинки), системные и настроечные файлы (которые одинаковые у всех)

При командах git push и git pull эти файлы будут игнорироваться. 

Как создать новый локальный репозиторий?

Создаем папку, создаем файл в ней README.md (markdown)
git init
Добавляем название/ описание в файле
Сохраняем  command + s
git add README.md
git commit -m "Initial commit»

К локальному репозиторию может быть привязан только один репозиторий, а к удаленному - несколько локальных.

git push -u origin main = u означает  upstream - она будет отправляться

Как проверить, что репозитории синхронизированы?
git pull
Already up to date.
git push
Everything up-to-date

git remote
origin
irinagladkikh@MacBook-Pro-Irina WinterSeminar % git remote 
-v 
origin  https://github.com/rinagladkikh/WinterSeminar.git (fetch)
origin  https://github.com/rinagladkikh/WinterSeminar.git (push)


1. Создать локальный репозиторий.
2. "Подружить" ваш локальный и удаленный репозитории. Github при создании нового репозитория подскажет, как это можно сделать.
Добавить строки из Github:
…or push an existing repository from the command line
git remote add origin https://github.com/rinagladkikh/123.git
git branch -M main
git push -u origin main
3. Отправить (pull) ваш локальный репозиторий в удаленный (на Github), при этом вам, возможно, нужно будет авторизоваться на удаленном репозитории.
4. Провести изменения "с другого компьютера".
5. Вытянуть (pull) актуальное состояние из удаленного репозитория.

git pull - чтобы обратно добавить версию на компьютер
При дальнейшей работе с файлом его можно изменять локально (в VS Code). Версия на GitHub остается прежней.

Pull request - запрос на вливание изменений в репозиторий


Как мы добавляем изменения в чужой репозиторий? Как сделать pull request?

1. Делаем форк (fork) интересующего нас репозитория.
2. Мы делаем git clone для нашей версии этого репозитория.
3. Мы создаем ветку с предлагаемыми изменениями, производим все изменения только в этой ветке.
4. Отправляем эти изменения на свой аккаунт (push)
5. В окне на Github появляется возможность отправить pull request.