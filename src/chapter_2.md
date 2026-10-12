# An Intro to XSS

## Building the website

### Step 3

Create a file named basic.html and then code this:

```html
<!DOCTYPE html>
<html>
    <head>

    </head>
    <body>
       <p>Hi there!</p>
    </body>
</html>
```
Right click on it on the right to open in file explorer.
Double click on it to view in the browser.
You should now see your coded webpage.

### Step 4

Adding style:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p {
                color: aqua;
                font: bold;
                font-size: 14px;
            }   body {
                background-color: black;
            }
        </style>
    </head>
    <body>
       <p>Hi there!</p>
    </body>
</html>
```

Feel free to play with the style, check out https://www.w3schools.com/html/html_styles.asp for more info.

Remember to test it:
Right click on it on the right to open in file explorer.
Double click on it to view in the browser.
You should now see your coded webpage.


### Step 5

Adding a script into the header.

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p {
                color: aqua;
                font: bold;
                font-size: 14px;
            }   body {
                background-color: black;
            }
        </style>
        <script>
            alert('hello I am an alert script')
        </script>
    </head>
    <body>
       <p>Hi there!</p>
    </body>
</html>
```

Test what this looks like:
Right click on it on the right to open in file explorer.
Double click on it to view in the browser.
You should now see your coded webpage.
