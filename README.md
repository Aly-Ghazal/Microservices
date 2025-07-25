# Version incompatibility issue solved

### The Issue

while running the app 1st time this was the output of its log

''' Traceback (most recent call last):
  File "/app/run.py", line 1, in <module>
    from app.main import app
  File "/app/app/__init__.py", line 2, in <module>
    from flask import Flask
  File "/usr/local/lib/python3.9/site-packages/flask/__init__.py", line 5, in <module>
    from .app import Flask as Flask
  File "/usr/local/lib/python3.9/site-packages/flask/app.py", line 30, in <module>
    from werkzeug.urls import url_quote
ImportError: cannot import name 'url_quote' from 'werkzeug.urls' (/usr/local/lib/python3.9/site-packages/werkzeug/urls.py) '''

### RootCause
this happened because of version incompatibility between Flask and Werkzeug.

### Solution

update your requirements.txt to include compatible versions
''' Flask==2.2.2
Werkzeug==2.2.2 '''
