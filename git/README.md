## Как работать с gitHub
##### 1. Инициализируем папку"

` git init `
##### 2. Создаем нужные файлы или добавляем существуеющие
Только один:

` git add name.py ` 

Добавить все файлы и папки для отслеживания github

`git add .`
##### 3. Проверка статуса
Если горит всё зеленым значит все файлы отслеживаются, а если горят красным, то игнорируются

` git status `
##### 4. .Gitignore
Создаём файл gitignore, можно создать с помощью PyCharm
` .gitignore `
После этого списком, по дному в строчку добавляем файлы которые не хотм отселживать, и заливать на github. Также можно писать название папок
##### 5. Создаём коментарий измений или инициализации
` git commit -m "Add README" `
##### 6. Создаём репозиторий, куда мы хотим сохранить проект 
После этого ищем информацию о добавление на удаленный репозиторий
сылка для залива проекта

` git remote add origin https://github.com/skaylife/FlaskAplication.git `
##### 7. Создаём репозиторий, куда мы хотим сохранить проект (GitHub) 
Заливаем проект на github

` git push -u origin master `

#### Вы можете сохранить изменения в рабочем кталоге перед мержем:
Заливаем проект на github

` git stash save `

` git merge origin/master `

` git stash pop `


## Пример до залива проекта 
Добавляем файлы в списке ` .gitignore `

` git rm --cached 'git ls-files -i --exclude-from=.gitignore' `

Убираем отслеживание файлов в ` .gitignore `

` git rm -rf --cached . `

Добавляем комит

` git commit -m "Commit" `

Проверяем отслеживание файлов

` git status  `

Добавляем все файлы кроме тех, которые находятся в списке файла ` .gitignore `

` git add . `

Устанавливаем нужный репозиторий 

` git remote set-url origin https://git@github.com/skaylife/FlaskAplication.git `

Создаем новую ветку branch

` git checkout -b Final_Version `

Заливаем проект в новую ветку branch

` git push origin Final_Version `

В Git v1.7.0, вы можете удалить удалённую ветку, используя

`git push origin --delete <branchName>`




 





