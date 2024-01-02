---
aliases:
  - Heroku
  - platform-as-a-service (PaaS)
  - cloud app deployment platform
tags:
  - computer-science/programming
note-type:
  - general
description: 
file-created: 2023-12-29
file-modified: 2023-12-29
linter-yaml-title-alias: Heroku
---

# Heroku

#status/postponed

Related to [[Deploying an app]]

> [!tip] Deploying an existing Python app
> [Deploying Python and Django Apps on Heroku | Heroku Dev Center](https://devcenter.heroku.com/articles/deploying-python)
> For existing apps:  [Preparing a Codebase for Heroku Deployment | Heroku Dev Center](https://devcenter.heroku.com/articles/preparing-a-codebase-for-heroku-deployment)

For my [[Emotion wheel app project|emotional feelings wheel app project]], I want to deploy my Flask application using Heroku so I'm reading through this tutorial: [Getting Started on Heroku with Python | Heroku Dev Center](https://devcenter.heroku.com/articles/getting-started-with-python#create-and-deploy-the-app)
- Need a subscription plan for server resources
	- A dyno is a lightweight container that runs the command specific in the `ProcFile`
	- The Eco dynos plan provides 1000 dyno hours for $5 per month. This dyno hours pool is shared by all Eco dynos in your account.
	- Changing resource scaling on the deployment can be done through `heroku ps:scale web=0`
	- It's pretty fast at scaling up and down
- Requires install of heroku CLI
- Heroku uses a *Procfile* to tell the app what commands to execute on its bootup
- Heroku recognizes an app as a Python app by looking for key files. It checks the `requirements.txt` file in the root directory to recognize it. I should set up a virtual environment `venv` when I create the `requirements.txt`

## Deploying an existing codebase using Heroku

1. Track something in a version constrol system like Git/Github
2. Deploy new versions of apps by deploying to a Heroku-hosted git repo. It mirrors these code changes from the local repo.
	- [Deploying with Git | Heroku Dev Center](https://devcenter.heroku.com/articles/git#create-a-heroku-remote)
- Navigate to folder
- `git push heroku BRANCHNAME`
- It's good practice to specify which python version^[https://devcenter.heroku.com/articles/python-runtimes] to use in a `runtime.txt`
- Make sure to add `\venv\` to the `.gitignore` otherwise the heroku branch will try to deploy a huge ass folder

Overall steps:
1. Set up the code repo in github/VCS
2. Configure a `Procfile` Windows needs a port forward command so here's an example
	1. ![[Procfile]]
	2. ![[Procfile.windows]]
3. Create the app using `heroku create`
4. Deploy the code using `git push heroku git-branch-name`
	1. Testing the app locally using `heroku local --port 5001 -f Procfile.windows` or `heroku local --port 5001`

### Deploying a machine learning model in Heroku

> [!warning] Use CPU version of pytorch to overcome slug size
> Need to add the following lines into `requirements.txt`
>
>
>
> ```
> -f https://download.pytorch.org/whl/torch_stable.html`
> torch==2.1.2+cpu
> ```

There are limitations in terms of how Heroku works. It compresses files into something called a slug to be able to deploy it across resources easily, but it also means that there is a certain size limit in terms of how big the files are.

Right now I'm using the Transformers plugin and it's very large. So one of my solutions is to try and switch over to the CPU version of the Transformers library, and hopefully that's small enough. Otherwise, my other solution is to try it out with Docker, which does not have this size limit.

Guides
- [GitHub - imadtoubal/Pytorch-Flask-Starter: 🐍+🔥This project is aimed to help Pytorch machine learning developers to quickly build a Flask web app in a Docker container ready to be deployed.](https://github.com/imadtoubal/Pytorch-Flask-Starter)
- [Create & Deploy A Deep Learning App - PyTorch Model Deployment With Flask & Heroku - Python Engineer](https://www.python-engineer.com/posts/pytorch-model-deployment-with-flask/)

## Useful commands for Heroku

### Procfile

- The file is case-sensitive `Procfile` 
	- not ~~ProcFile~~ nor ~~Procfile.txt~~
- For gunicorn, `Procfile` should have the line `web: gunicorn flask_page:app`
	- Make sure it's in `requirements.txt`
	- **`web:`**: Specifies that this command is for the web process type, which handles HTTP requests.  
	- **`gunicorn`**: The command to start Gunicorn, a WSGI HTTP server for Python web applications.
	- **`flask_page:app`**: Specifies the Python module (or package) that contains your Flask application (`flask_page.py`), followed by the variable name of your Flask application instance (`app`).

### Administration for Heroku

Creates web app link
```term
heroku create 
```
Open URL of app directly
```term
heroku open
```

View logs
```term
heroku logs --tail
```

Deploys specific git branch to heroku

```term
git push heroku main
```

### Resource deployment and management with Heroku

- Check if app is deployed with instance. The parameters also controls to how many resources it's scaled.
- Scaling to 0 **pauses a specific process type**, while killing an app terminates all dynos and shuts it down completely.

```term
heroku ps:scale web=1
```

Check how many dynos are running
```term
heroku ps
```
Removing add-ons
```term
heroku addons:destroy heroku-postgresql
```
Removing application
```term
heroku apps:destroy
```
Confirming deletion
```term
heroku addons --all
$ heroku apps --all
```

#### One-off dynos

Used with `heroku run` command to spin-one up

The purpose of one-off dynos in Heroku is to run short-lived, ad-hoc tasks or commands outside of the normal web or worker dyno processes. One-off dynos are temporary dynos that are spun up to execute a specific command or script and then automatically shut down.

These dynos are useful for running tasks such as database migrations, running console commands, running scheduled jobs, or performing one-time administrative tasks. One-off dynos provide a separate environment where you can execute these tasks without impacting the normal operation of your application. Once the task is completed, the dyno is terminated, making them a convenient and isolated way to perform various tasks on your Heroku app.

#### Log management

Papertrail is a logging add-on for Heroku that provides real-time log management and analysis. It allows you to aggregate and view logs from your Heroku applications and other sources in a central location. With Papertrail, you can search and filter logs, set up alerts based on log events, and gain insights into your application's behavior and performance. It helps simplify troubleshooting and monitoring of your Heroku applications by providing a consolidated view of log data.

```term
heroku addons:create papertrail
heroku addons:open papertrail
```

#### Troubleshooting

- [Why am I seeing "Couldn't find that process type" when trying to scale dynos? - Heroku Help](https://help.
heroku.com/W23OAFGK/why-am-i-seeing-couldn-t-find-that-process-type-when-trying-to-scale-dynos)
- [python - H14 error in heroku - "no web processes running" - Stack Overflow](https://stackoverflow.com/questions/41804507/h14-error-in-heroku-no-web-processes-running)

