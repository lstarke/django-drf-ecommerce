# Commands

## Packaging

Create requirements.txt: ```pip freeze requirements.txt```<br>
Install requirements: ```pip install -r requirements.txt```

## VSCode

Preview markdown file: ```ctrl+shift+v```

## Environment variables

Install python-dotenv package: ```pip install python-dotenv```<br>
Create a ```.env``` file to place your variables.<br>
Using dotenv:

```
from dotenv import load_dotenv
import os

load_dotenv()

SECRET_KEY = os.environ.get("SECRET_KEY")
```

## Virtual Environment

Create a virtual environment: ```python -m venv .venv```<br>
Activate a virtual environment: ```.venv\Scripts\activate```<br>
Deactivate a virtual environment: ```.venv\Scripts\deactivate```

## Django

Create new project: ```django-admin startproject <project-name>```<br>
Run project: ```python manage.py runserver```<br>
Create secret key:<br>
1. Enter shell by typing ```python manage.py shell```<br>
2. Use ```get_random_secret_key()``` from ```django.core.management.utils``` 

```
from django.core.management.utils import get_random_secret_key

print(get_random_secret_key())
```
3. Copy and paste result in SECRET_KEY located in```<project-name>/settings.py```.

## Pytest

Installing Pytest: ```pip install pytest```.<br>
```pytest -h```: prints options and config file settings<br>

Installing Pytest-django: ```pip install pytest pytest-django```<br>
Create a file ```pytest.ini``` in the project root directory and add the content bellow:.<br>
```
[pytest]
DJANGO_SETTINGS_MODULE = drfecommerce.settings
python_files = test_*.py
```






