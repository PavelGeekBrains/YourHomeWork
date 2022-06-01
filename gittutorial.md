## Базовые команды Git

+ Имя пользователя и адрес электронной почты

_git config --global user.name "Tara Routray"_

_git config --global user.email "dev@tararoutray.com"_

+ Инициализация репозитория

_git init_

+ Добавление файлов

_git add somefile.js_

+ Проверка статуса репозитория

_git status_

+ Фиксация текущей версии с комментарием

_git commit -m "Your short summary about the commit"_

+ Журнал изменений

_git log_

+ Переключение между коммитами

_git checkout_

## Материалы:

[Источник 1](https://texterra.ru/blog/ischerpyvayushchaya-shpargalka-po-sintaksisu-razmetki-markdown-na-zametku-avtoram-veb-razrabotchikam.html?)

[Источник 2](https://habr.com/ru/company/ruvds/blog/599929/)

![Котик](https://w7.pngwing.com/pngs/890/216/png-transparent-cat-kitten-chi-s-sweet-home-drawing-anime-cat.png)

## Работа с ветками в Git

+ Создание новой ветки

    _Создать новую ветку можно с помощью параметра branch, указав имя ветки._
    
    __*git branch new_branch_name*__

+ Переход на нужную ветку

    _Перейти на новую ветку можно с помощью параметра checkout, указав имя ветки._

    __*git checkout new_branch_name*__

+ Просмотр списка веток

    _Можно просматривать полный список веток, используя параметр branch. Команда отобразит все ветки, отметит текущую звёздочкой (*) и выделит её цветом._

    __*git branch*__

+ Слияние двух веток

    _Объединить две ветки можно параметром merge с указанием имени ветки. Команда объединит указанную ветку с основной._

    __*git merge existing_branch_name*__

    ![модель слияния](https://i.stack.imgur.com/2Oh83.png)

+ Удаление веткок

    _Удалить ветку можно параметром branch с добавлением флага -d и указанием имени ветки. Если вы завершили работу над веткой и объединили её с основной, можно её удалить без потери истории._

    __*git branch -d existing_branch_name*__

**В данной инструкции перечислены основные команды git.**

![финал](https://media.dayoftheshirt.com/images/shirts/ARseF/neatoshop_lil-sith-graffiti_1501445519.large.png)


