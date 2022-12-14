# *Конспект по теме "Знакомство с контролем версий GIT"*

## СЕМИНАР 1

*Git* - это программа, позволяющая решать проблему, связанную с контролем версий. *Git* сохраняет в памяти не файлы целиком, а разницу между ними, что позволяет экономить память.

## *Список основных команд Git:*

1. git config --global user.name

2. git config --global user.email

3. git init

4. git add "название файла с расширением"

5. git commit -m "комментарий"

6. git log

7. git checkout

8. git checkout master

9. git status

## *Git config --global user.name и git config --global user.email*

Команда установки Вашего имени и электронной почты

## *Git init*

Команда инициализации (создания) репозитория. Репозиторий - это место где хранятся и поддерживаются какие-либо данные. При инициализации репозитория *Git* создает ветку с именем master по умолчанию. При инициализации создается скрытая папка, в которой содержатся все объекты и ссылки, которые *Git* использует и создает в истории работы над проектом. 

## *Git add*

Команда добавления файлов под контроль версий. При добавление одного файла после git add указываем название файла с расширением, также можно добавить сразу все файлы (команда git add --all).

## *Git commit -m*
Команда создания коммита. Коммит - точка сохранения проекта. У каждого  коммита есть hash (уникальный id) и комментарий. 

## *Git log*

Команда просмотра истории коммитов с изменениями. Список коммитов, созданных в данном репозитории, по умолчанию выводится в обратном хронологическом порядке, т.е. самые последние коммиты показываются первыми.

## *Git checkout*

Команда запуска какого-то предыдущего сохранения. Для запуска команды необходимо ввести git checkout и несколько первых цифр идентификатора коммита (идентификатор коммита можно увидеть при запуске команды git log).

## *Git checkout master*

Команда возвращения в актуальную версию.

## *Git status*

Просмотр статуса нужного репозитория (его действие распространяется на подготовленные, неподготоленные и неотслеживаемые файлы). 

## Другие команды

* git show и идентифакатор коммита - просмотр полного списка изменений, внесенного конкретным коммитом.

* git commit --amend -m "коммит" - внесение изменений в последний коммит (команда, чтобы отредактировать сообщение предыдущего коммита, если, напрмер, была допущена ошибка).


## СЕМИНАР 2

## *Ветки в Git и их использование на практике*

### *Основные команды:*

### 1. git branch

>Команда *git branch* выводит на экран список имеющихся веток. При выводе на экран веток звездочкой (*) отмечена текущая ветка.
   
>> Для создания новой ветки используют команду *git branch имя_новой_ветки*.
>> Для создания новой ветки и перехода сразу же в нее, используется команда <*git checkout -b <название_новой_ветки>*>.

>> Для удаления ненужной ветки используют команду *git branch -d имя_ненужной_ветки*

### 2. git checkout

> Для перехода с ветки на ветку используется команда <*git checkout название_ветки*>. <*Git checkout*> - команда запуска какого-то предыдущего коммита (сохранения). Сейчас вместо коммита указываем ветку, на которой хотим оказаться. 

### 3. git merge

> Команда <*git merge*> отвечает за слияние веток. 
>>Команда <*git merge*> вызывается из той ветки, в которую необходимо добавить ветку. Для перехода в необходимую ветку используем команду <*git checkout <название_ветки>*>. Командой <*git branch*> проверяем находимся ли мы в нужной ветке, а также проверяем все ли сохранено, вызвав команду <*git status*>.
>>>Если все в порядке, то далее используем команду <*git merge <название_ветки_которую_нужно_присоединить>*>.


## Другие команды:

* <git log --branches=* > - просмотр всех коммитов во всех ветках.

* <git log название_ветки> - просмотр всех коммитов в одной ветке.

* <git log --graph> - иное (графическое) отображение дерева коммитов.

* ![текст](имя файла,откуда изображение необходимо достать) - добавление изображения. Например:

> ![Привет, Тоторо!](totoro.jpg) 

> Добавим в папку картинку, теперь в папке помимо файла Lesson1.md есть еще и картинка. Сохраняем изменения в файле, но не сохраняем картинку. Добавляем новый файл <.gitignore>, в котором записываем название нашей картинки (не принято добавлять в Git какие-то фотографии или большие файлы. Их обычно игнорируют и работают только с текстовой составляющей. В файле <.gitignore> указываем имя файлов, которые необходимо игнорировать Git). Далее сохраняем внесенные изменения (git add и git commit).

![конец)](end.jpg)


##   Семинар 3

Репозиторий добавлен на GitHub
   
Эта информация добавлена из удаленного репозитория
