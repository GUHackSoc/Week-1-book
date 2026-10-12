# An Intro to XSS

## Breaking the website

### Step 9

What happens when we put in our own script in?

```
http://127.0.0.1:5000/hello?user=<script>alert('Hi I am an alert')</script>
```

Play around with scripts, try googling and see what the wildest thing you can do is.