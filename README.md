# Инструкция по Git

![git logo](https://git-scm.com/images/logos/downloads/Git-Logo-White.png)

Развернутую инструкцию по работе с Git можно найти по [ссылке](https://gbcdn.mrgcdn.ru/uploads/asset/4245110/attachment/d4eb8c232f8f2bdf4e42ba7cb49e0c50.pdf).

## Что такое Git?

Git - это одна из реализаций распределенных систем контроля версий, имеющая как локальные, так и удаленные репозитории.

Git — самая популярная система контроля версий, но не единственная. Алгоритм работы подобных систем схож.

Программа Git берёт на себя контроль версий проекта и позволяет переключаться между ними. Обратите внимание: Git хранит не файлы целиком, а отличия между ними. Это позволяет экономить память. Автор программы — Линус Торвальдс, создатель ОС Linux. 

## Начало работы с Git

Все команды задаём при помощи написания кода в терминале.

Прежде чем создавать репозиторий и инициализировать Git, проверим текущую установленную версию пограммы. Для этого в терминале введём команду: _git --version_.

Если Git установлен на компьютер, вы увидите его текущую версию.

При первом использовании Git необходимо представиться. Для этого в терминале нужно ввести две команды: 
* _git config --global user.name_ "Ваше имя английскими буквами"
* _git config --global user.email_ ваша почта@example.com

## Основные команды Git

* _git init_ - инициализируем пустой репозиторий
* _git status_ - проверяем текущее состояние файлов
* _git add имя_файла.расширение_ - добавляем версионность файлу
* _git commit -m "Message"_ - команда для фиксации изменений файлов
* _git log_ - вывод истории коммитов в хронологическом порядке
* _git diff_ - вывод изменений на текущий момент по отношению к последнему коммиту
* _git checkout master / main / хэш-номер коммита_ - переход между изменениями либо возврат к текущему сохранению

## Подготовка репозитория

Для создания репозитория необходимо выполнить команду *git init* в папке  с репозиторием.

## Git add

Для добавления изменений в коммит используется команда *git add*. Чтобы использовать команду *git add*, напишите *git add "имя файла"*.

## Создание коммитов

Для того, чтобы создать коммит (сохранение), необходимо выполнить команду *git commit -m "Сообщение"*.

## Создание ветки

Ветки позволяют легко управлять черновиками и чистовиками в Git.

Для того, чтобы создать ветку, нужно использовать *git branch имя_ветки* или *git checkout -b имя_ветки*.

Если у нас несколько версий черновика, мы можем вывести на экран ветку, где находимся, командой git branch.

Если потребуется переключиться с одной ветки на другую, вызовем команду *git checkout <имя ветки>*.

## Объединение веток

Чтобы слить любую ветку с текущей, вызываем *git merge <имя ветки для слияния с текущей>*.

Чтобы объединение веток прошло корректно, необходимо перейи в ветку, в котоную необходимо добавить информацию из ветки-черновика.

## Удаление ветки

Для того, чтобы удалить ветку, нужно воспользоваться командой *git branch -d <название ветки>*.

## Конфликт изменений

При работе в двух ветках одновременно может возникнуть ситуация, когда в одной и другой ветке мы по-разному изменили блок текста. Если затем мы попробуем слить эти ветки, Git сообщит о конфликте и предложит выбрать, какие же изменения записать. 

Поэтому у проекта в репозитории должен быть один ответственный пользователь, наделённый правом проводить слияния и разрешать конфликты.

## Визуализация всех веток

Ключ -graf в связке с командой log позволяет отобразить коммиты в виде дерева - *git log --graph*

## Работа с удаленными репозиториями

GitHub - самый популярный сервис Git от компании Майкрософт для организации работы удаленных репозиториев.

## Git clone

Копировать внешний репозиторий на свой ПК можно командой git clone.

Команда git clone составная: она не только загружает все изменения, но и пытается слить все ветки на локальном компьютере и в удаленном репозитории.

## Git Push

Отправить свою версию репозитория во внешний репозиторий поможет команда git
push. При первом её использовании нужна авторизация.

## Git Pull

Эта команда позволяет скачать все из текущего репозитория и автоматически сделать merge с нашей версией.

## Как настроить совместную работу

1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. “Подружить” ваш локальный и удалённый репозитории. GitHub при создании нового репозитория подскажет, как это можно сделать
4. Отправить (push) ваш локальный репозиторий в удалённый (на GitHub), при этом, возможно, вам нужно будет авторизоваться на удалённом репозитории
5. Провести изменения “с другого компьютера”
6. Выкачать (pull) актуальное состояние из удалённого репозитория

## Pull request

Предлагать изменения на GitHub нужно в отдельной ветке. Сначала пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем
клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет изменения командой push в свой аккаунт на GitHub и даёт команду pull request.

## Как сделать pull request
* Делаем   (ответвление) репозитория fork
* Делаем git clone   версии репозитория СВОЕЙ
* Создаем новую ветку и в НЕЕ вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой GitHub
* На сайте GitHub нажимаем кнопку pull requestg