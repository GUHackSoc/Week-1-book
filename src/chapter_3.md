# An Intro to XSS

## Building the website

### Step 6

Create a file named basic.py and then code this:

```python
import flask

app = flask.Flask(__name__)

@app.route('/')
def hello_world():
    return 'hello world'

if __name__ == '__main__':
    app.run()

```
Run in your terminal:
```
./basic.py
```
Then click on the localhost address to see a new webpage.

### Step 7

Create a new Route and copy the your basic.html into the return f''' '''.

Here's the file without the basic.html entered:
```python
import flask

app = flask.Flask(__name__)

@app.route('/')
def hello_world():
    return 'hello world'

@app.route('/hello')
def hello_user():
    user = flask.request.args.get('user', default='Callum')
    return f'''
'''

if __name__ == '__main__':
    app.run()
```
Change default=Callum to your username.

Here is mine with my basic.html code between the f''' ''':
```python

import flask

app = flask.Flask(__name__)

@app.route('/')
def hello_world():
    return 'hello world'

@app.route('/hello')
def hello_user():
    user = flask.request.args.get('user', default='Callum')
    return f'''
<!DOCTYPE html>
<html>
    <head>
        <style>
            p {{
                color: aqua;
                font: bold;
                font-size: 14px;
            }}   body {{
                background-color: black;
            }}
        </style>
    </head>
    <body>
       <p><span>Hi there! {user}</p>
    </body>
</html>
'''
if __name__ == '__main__':
    app.run()
```
Note that I changed each "{" and "}" to "{{" and "}}" and added the {user} variable, you should do this with your code too.
I have also removed my alert script.

Now we can go to our localhost to view the webpage at:
```
http://127.0.0.1:5000/hello/
```