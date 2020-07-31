
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
##### tkinter - интерфейс Python к Tcl/Tk 
1 `https://pythoner.name/documentation/library/tkinter` ru
##### Курс по библиотеке Tkinter языка Python
2 `https://goo-gl.su/Xxnmrp` ru
##### Python GUI Examples (Tkinter Tutorial)
3 `https://likegeeks.com/python-gui-examples-tkinter-tutorial/` en
##### Примеры разметки в Tkinter [Урок №2]
4 `https://python-scripts.com/tkinter-layout-example` ru

## Установка SQLALCHEMY_DATABASE & SQlite3 
##### install flask-sqlalchemy
`pip install flask-sqlalchemy`
##### Создание и Вход в SQlite3 
`sqlite3 blog.db`
##### Созанание таблицы SQlite3 и выход из режима 
`.tables`
`.exit`
##### Конструкция использваония
`app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///C:\\pyt\\Flask\\Clean-Blog\\blog.db'` ИЛИ

`app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:////mnt/c/Users/antho/Documents/blog/blog.db'`

`app.config["SQLALCHEMY_TRACK_MODIFICATIONS"] = False` - отключение предупреждения в консоли

`db = SQLAlchemy(app)` 
##### Пример работы с SQlite3 
`
class BlogPost(db.Model):

    id = db.Column(db.Integer, primary_key=True)
    
    title = db.Column(db.String(50))
    
    subtitle = db.Column(db.String(50))
    
    author = db.Column(db.String(20))
    
    date_posted = db.Column(db.DateTime)
    
    content = db.Column(db.Text)
`
    
##### Создание роута в SQlite3 и прием данных посланных с addpost 
`
@app.route('/addpost', methods=['POST'])

def addpost():
    title = request.form['title']
    subtitle = request.form['subtitle']
    author = request.form['author']
    content = request.form['content']

    post = BlogPost(title=title, subtitle=subtitle, author=author, date_posted=datetime.now(), content=content)

    db.session.add(post)
    db.session.commit()

    return redirect(url_for('index'))`
    
##### Проверка на отсутвие созданной таблицы, и созданию 
`import os `

` 
if __name__ == "__main__":
    if not os.path.exists('db.sqlite'):
        db.create_all()
    app.run(debug=True)
`
