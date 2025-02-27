# Инструкция для работы с Git и удалёнными репозиториями

![Git-logo](git-logo.jpg)

# Что такое Git?

Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

# Подготовка репозитория

Для создание репозитория необходимо выполнить команду *git init* в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

# Создание коммитов

## Git add

Для добавления измений в коммит используется команда *git add.* Чтобы использовать команду *git add* напишите *git add <имя файла>*.

## Просмотр состояния репозитория

Для того, чтобы посмотреть состояние репозитория используется команда *git status.* Для этого необходимо в папке с репозиторием написать *git status,* и Вы увидите были ли измения в файлах, или их не было.

## Создание коммитов

Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit.* Выполняется она так: *git commit -m "<сообщение к коммиту>.* Все файлы для коммита должны быть *__ДОБАВЛЕНЫ__* и сообщение к коммиту писать *__ОБЯЗАТЕЛЬНО__.*

## Перемещение между сохранениями

Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>.*

> &#9888; **Warning!**  
 Во избежание ошибок, обязательно вернитесь на конец ветки **master** (**HEAD**) с помошью команды *git checkout master*.

# Выделение текста

## Выделение текста

Чтобы выделить текст курсивом необходимо обрамить его звездочками (*) или знаком нижнего подчеркивания. Например, *вот так* или или _вот так_.

Чтобы выделить текст полужирным, необходимо обрамить его двойными звездочками (**) или двойным знаком нижнего подчеркивания (__). Например, **вот так** или __вот так__.

Альтернативные способы выделения текста жирным или курсивом нужны для того, чтобы мы могли совмещать оба этих способа. Например, _текст может быть выделен курсивом и при этом быть **полужирным**_.

# Списки

Чтобы добавить ненумерованные списки, необходимо пункты выделить звездочкой (*) или знаком +. Например, вот так:
* Элемент 1
* Элемент 2
* Элемент 3
+ Элемент 4


Чтобы добавить нумерованные списки, необходимо пункты просто пронумеровать. Например, вот так:
1. Первый пункт
2. Второй пункт

# Работа с изображениями

Чтобы вставить изображение в текст, достаточно написать следующее:

![Текст](имя файла с *__обязательным__* указанием типа файла).

# Журнал изменений

Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log.* Для этого достаточно выполнить команду *git log* в папке с репозиторием

# Ветки в Git

## Создание ветки

Для того, чтобы создать ветку, используется команда *git branch.* 
Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*.

>&#128712; **Information!**
 Для вывода списка веток изпользуйте команду *git branch*. Ветка, на которой Вы сейчас находитесь будет отмечена звёздочкой (*).

## Слияние веток

Для того чтобы дабавить ветку в текущую ветку используется команда *git merge*. 
Например: *git merge <название ветки>.*

>&#9757; **Important!**
 Важно помнить, что слияние веток происходит в ту, из которой Вы вызываете команду - *git merge*.

Иногда, если в сливаемых ветках в одном и том же месте указаны разные данные, может возникнуть конфликт.  

## Удаление веток

Для удаления ветки ввести команду "git branch -d 'name branch'"

# Добавление ссылки

Для добавления ссылки в файл, необходимо прописать следующее: [Наименование ссылки](адрес ссылки).

Например: Более подробную информацию можно посмотреть на [оффициальном сайте](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%9E-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B5-%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8F-%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9)

# Краткая сводка по командам
---
|Команда|Действие|Примечание
|:-|:-:|-:
|git init|Создание репозитория|Создаётся скрытая папка .git
|git add|Добавление изменений в коммит|
|git status|Просмотр состояния репозитория|
|git commit|Создание коммита|Фиксация, сохранение, снимок изменений
|git log|Вывод всех изменений в файле|Выводится хэш коммита, автор, его e-mail, дата и время коммита
|git checkout|Перемещение между коммитами|И ветками
|git branch|Создание новой ветки|Вывод списка веток на экран
|git merge|Слияние веток|
|git clone|Клонирование внешнего репозитория|Загрузка на свой ПК
|git pull|Скачивание информации из текущего репозитория| В этом случае автоматически идет *merge*
|git push|Отправка нашей версии на внешний репозиторий|Требует авторизации на внешнем репозитории
---

# Работа с удаленными репозиториями

## Команда *__git clone__*

Эта команда позволяет склонировать внешний репозиторий на наш ПК.

Пример кода: *git clone <Адрес репозитория, который копируем на свой ПК>.*

## Команда *__git pull__*

Эта команда позволяет скачать все из текущего репозитория и автоматически сделать *__merge__* с нашей версией.

Пример кода: *git pull*

## Команда *__git push__*

Эта команда позволяет отправить нашу версию репозитория на внешний репозиторий. *__ТРЕБУЕТ АВТОРИЗАЦИИ__* на внешнем репозитории.

Пример кода: *git push*

## Команда *__pull request__*

Как сделать *pull request*: 

* Делаем *__fork__* репозитория
* Делаем *__clone__* __СВОЕЙ__ версии репозитория
* Создаем новую ветку и в __НЕЕ__ вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой __GitHub__
* На сайте __GitHub__ нажимаем кнопку *__pull request__*