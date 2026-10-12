# An Intro to XSS

## Fixing the website

There are 3 common ways of fixing XSS:
1. Escaping HTML for user inputed variables. This is general and can be applied to most different technologies.

2. In Flask (and most web app frameworks) you can use template render functions that have in built XSS prevention and are the standard way of making websites.

3. Implementing Content Security Policies (search engine what that is if you are interested).

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

Now try your payload, you should see that it is rendered safely.
