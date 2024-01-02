---
aliases:
  - Google Colab 
tags:
  - 
note-type:
  - general
description: 
file-created: 2023-12-22
file-modified: 2023-12-22
linter-yaml-title-alias: Google Colab 
---

# Google Colab 

#status/postponed

Related to [[Emotion wheel app project]]

---

## Google Colab 

### Deploying Flask applications using Google Colab 

Runs the google Colab notebook through `pyngrok` and exposes a URL
[Integration Examples — pyngrok 7.0.3 documentation#using Google colab](https://pyngrok.readthedocs.io/en/latest/integrations.html#google-colaboratory)

You need to use these 3 blocks:
```
!pip install pyngrok
```

```
import getpass

from pyngrok import ngrok, conf

print("Enter your authtoken, which can be copied from https://dashboard.ngrok.com/auth")
conf.get_default().auth_token = getpass.getpass()

# Open a TCP ngrok tunnel to the SSH server
connection_string = ngrok.connect("22", "tcp").public_url

ssh_url, port = connection_string.strip("tcp://").split(":")
print(f" * ngrok tunnel available, access with `ssh root@{ssh_url} -p{port}`")
```

```
import os
import threading

from flask import Flask
from pyngrok import ngrok

app = Flask(__name__)
port = "5000"

# Open a ngrok tunnel to the HTTP server
public_url = ngrok.connect(port).public_url
print(" * ngrok tunnel \"{}\" -> \"http://127.0.0.1:{}\"".format(public_url, port))

# Update any base URLs to use the public ngrok URL
app.config["BASE_URL"] = public_url

# ... Update inbound traffic via APIs to use the public-facing ngrok URL

# Define Flask routes
@app.route("/")
def index():
    return "Hello from Colab!"

# Start the Flask server in a new thread
threading.Thread(target=app.run, kwargs={"use_reloader": False}).start()
```

### Importing new modules into Google colab

```python
from google.colab import drive
drive.mount('/content/drive', force_remount=True)

# Insert the directory
import sys
sys.path.insert(0,'/content/drive/My Drive/Colab Notebooks')
```
