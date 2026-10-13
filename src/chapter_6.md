# An Intro to XSS

## Fixing the website

There are 3 common ways of fixing XSS:
1. Escaping HTML for user inputted variables. This is general and can be applied to most different technologies.

2. In Flask (and most web app frameworks) you can use template render functions that have in built XSS prevention and are the standard way of making websites. [https://www.geeksforgeeks.org/python/flask-rendering-templates/](https://www.geeksforgeeks.org/python/flask-rendering-templates/)

3. Implementing a Content Security Policy which is a response header that allows website administrators to control resources the user agent is allowed to load for a given page. Allowing them to limit the ability of scripts from executing from particular sources. [https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)

For the purposes of this exercise we will keep it simple and just use the escape funtion:

### Step 10

Create a new line below your line:
```python
user = flask.request.args.get('user', default='Callum')
```
New line to add below:
```python
user = html.escape(user)
```
Also update the import line to:
```python
import flask, html
```


Now try your payload, you should see that it is rendered safely.
