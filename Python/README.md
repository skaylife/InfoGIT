
## Как создать витруальное окружение для Python на Windows 10
##### Перейти к терминалу andconda Шаг 1

` pip3 install -U pip virtualenv `
##### Шаг 2

` virtualenv --system-site-packages -p python ./venv `
##### или же

` virtualenv --system-site-packages -p python3 ./venv `
##### Шаг 3

` .\venv\Scripts\activate `

## Как установить Dajngo 
##### install Django
`pip install Django`
##### Создание проекта на Django 
`django-admin startproject mysite`
##### Запуск сервера 
`python manage.py runserver`
##### Для linux 
`python -m pip install --user google-assistant-sdk[samples]`
##### Для linux если есть ошибки
`python3 -m pip install --user google-assistant-sdk[samples]`

## Установка PyQt5 и env 
##### install Env 
`virtualenv env`
##### activate Env 
`env\Scripts\activate` run
##### install PyQt5
`pip install pyqt5 pyqt5-tools` если не работает то `pip3 install pyqt5==5.12.0`
##### Установка PyQT5 Disenger  
`pip install pyqt5-tools`
`NAME PROJECT\env\Lib\site-packages\pyqt5_tools\Qt\bin`
##### Конвертируем UI в PY
`python -m PyQt5.uic.pyuic -x visual.ui -o visual.py`
## Tkinter Информация к изучению
##### install Env 
#####1 `https://pythoner.name/documentation/library/tkinter`
