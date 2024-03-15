[![logo](git_logo.png)](https://git-scm.com/) 
# GIT - инструкции и команды

[Документация по git](https://git-scm.com/doc)  

## Git - *это система контроля версий с локальными и удаленными репозиториями*

### Работа с локальным репозиторием

Создание репозитория с папкой .git 
```sh
git init 
```
 Добавить изменения в файле для отслеживания
```sh
git add Имя_файла
```
Сохранение файла, его фиксация
```sh
git commit -m "Комментарии к изменениям" 
```
Просмотр журнала, выводит списком все коммиты
```sh
git log 
```
 Укороченный вид журнала
```sh
git log --oneline 
```
Просмотр статуса/ изменений в репозитории
```sh
git status 
```
 Перемещение между коммитами, вводим первые символы нужного коммита
```sh
git checkout 
```
Показывает изменения между отредактированным файлом и последним закомиченным файлом
```sh
git diff 
```
Удаление незакомиченного файла
```sh
git restore имя_файла 
```

### Работа с ветками

*Ветка это не файл, а черновик*

 Выводит список веток в репозитории
```sh
git branch 
```
Создание новой ветки в репозитории
```sh
git branch new_branch 
```
Переходим на другую ветку
```sh 
git checkout new_branch 
```
Удаляем данную ветку, находясь в ветке master
```sh 
git branch -d new_branch 
```
Сливает данную ветку с веткой master
```sh 
git merge new_branch  
```
Показывает слияние двух веток в виде дерева
```sh 
git log --graph 
```
*- для дальнейшей работы с основной веткой, изменения в новой ветке необходимо добавить (add) и закоммитить (commit)*

*- после создания файла __gitignor__, его также необходимо добавить (add) и закоммитить (commit)*

### Конфликты

*Конфликт слияния в git возникает тогда, когда один и тот же блок текста/кода в разных ветках отличаются*
+ Accept Current Change - оставить текущую версию.
+ Accept Both Change - оставить оба варианта.
* Compare Change - сравнить изменения.
* Accept Incoming Change - принять версию от другой ветки.

### Работа с удаленным репозиторием

Для работы с удаленным репозиторием используем [сервис Github](https://github.com/)

Копировать внешний репозиторий на свой ПК
```sh 
git clone 
```
Отправляет изменения в удаленный репозиторий
```sh
git push
```
Подгружает изменения из удаленного репозитория и делает merge всех веток 
```sh 
git pull 
```

__Делаем pull request__

1. Делаем fork репозитория
2. Делаем clone своей версии репозитория
3. Создаем новую ветку и в НЕЕ вносим свои изменения 
4. Фиксируем изменения (делаем коммиты) 
5. Отправляем свою версию в свой GitHub 
6. На сайте GitHub нажимаем кнопку pull request

Выполнили домашнюю работу