---
aliases:
  - python web backend
  - Flask web app framework
  - web app framework
  - Flask
tags: 
note-type:
  - general
description: 
file-created: 2023-12-14
file-modified: 2023-12-15
linter-yaml-title-alias: Flask website framework
---

# Flask website framework

#status/postponed

Related to [[Emotion wheel app project]]

---

- Flask is a minimalistic back-end framework for Python. An alternative is to use Django
- Using it for my [[Emotion wheel app project|feeling wheel project]]
- It can be used with Vercel which I am currently using to host my [[Publishing my digital garden|digital garden]]?

You can import a module and call it in.
- [python - Flask: Want to import file of helper functions - Stack Overflow](https://stackoverflow.com/questions/31361482/flask-want-to-import-file-of-helper-functions#:~:text=Simply%20have%20another%20python%20script,in%20helpers%20by%20adding%20helpers.)

## Function calling

```python
from flask import Flask

app = Flask(__name__)

def hello_world():
    return "<p>Hello, World!</p>"

# The hello_world function is triggered at endpoint '/'
app.add_url_rule('/', view_func=hello_world)

if __name__ == '__main__':
    app.run()
```

## Routing

[Quickstart#Routing — Flask Documentation (2.3.x)](https://flask.palletsprojects.com/en/2.3.x/quickstart/#routing)

We use a `route()` decorator to call specific/meaningful URLs to do things for us. It can also trigger functions?

## Using the HTML templates

- In the templating engine, we can set template variables which in turn can be passed by towards the functions
- You can also render Python script in the HTML by using the following syntax. It uses the Jinja template  syntax.

```html
<body>
{% for i in range(10)%} <!-- the enclosing % % allows us to write code  -->  
        <p>{{content}}</p>  
{% endfor %}  
</body>
```

### Bootstrap framework UI

[Get started with Bootstrap · Bootstrap v5.3](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

- I can text the functionality using the bootstrap framework to add to the Flask HTML templates
- You need to add the JS headers for it to render some of the stfuff

### Jinja template

- [Jinja cheatsheet](https://devhints.io/jinja)
- [Learn Flask: Jinja2 Templates and Forms Cheatsheet | Codecademy](https://www.codecademy.com/learn/learn-flask/modules/flask-templates-and-forms/cheatsheet)
- You can perform operations on the rendering variables using Jinja filters as seen here: [Template Designer Documentation — Jinja Documentation (3.1.x)](https://jinja.palletsprojects.com/en/3.1.x/templates/#jinja-filters.trim)

## HTTP requests and methods

> HTTP requests are the means by which clients communicate with servers to retrieve, send, or manipulate data, forming the basis of information exchange on the World Wide Web.

To communicate with servers, we use something called request-response protocol to transmit information between a client and a server. I'm trying to understand this in order to learn how to work with [[Flask web app framework|Flask]] in deploying my [[Emotion wheel app project|emotional feelings wheel app project]].

The two most common methods are the ones below:
- `POST` methods **sends** information to a server/resource
	- Sends data to a server, gets processed and the server returns a responses
	- Needs to point to a specific URL
- `GET` methods **retrieve** information from a server and retrieve data.
	- It also needs to specific a *specific URL* in order to retrieve the resource.

[What Is the Difference Between GET and POST Methods? | Baeldung on Computer Science](https://www.baeldung.com/cs/http-get-vs-post)

## Links

- [Deploying to Production — Flask Documentation (2.1.x)](https://flask.palletsprojects.com/en/2.1.x/deploying/)
- [Flask Hello World – Vercel](https://vercel.com/templates/python/flask-hello-world)
- [Flask Example Projects and Code - Full Stack Python](https://www.fullstackpython.com/flask-code-examples.html)
- [How To Create Your First Web Application Using Flask and Python 3 | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-create-your-first-web-application-using-flask-and-python-3) < - sems decent enough
- [Flask Tutorial #4 - HTTP Methods (GET/POST) & Retrieving Form Data - YouTube](https://www.youtube.com/watch?v=9MHYHgh4jYc) <- This guide has been usedl
