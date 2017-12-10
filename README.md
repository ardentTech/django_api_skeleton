# Django API Skeleton

A Python3.x RESTful API skeleton based on [Django Rest Framework](http://www.django-rest-framework.org).

## Setup

1. `cd ~/ && mkdir .venv && cd .venv`
2. `python3.5 -m venv <project_name>`
3. `source ./<project_name>/bin/activate`
4. `cd ~/ && mkdir -p projects/<project_name> && cd projects/<project_name>`
5. `git clone git@github.com:ardentTech/django_api_skeleton.git .`
6. `pip install wheel`
7. `pip install -r requirements.txt`

## Environment Variables and Secrets
Create `api/env.py` contain all environment variables (database, smtp, etc.) and secrets (database password, django secret key, etc.):

```
ENV = {
    "@todo_SECRET_KEY": "",
    "@todo_DB_NAME": "",
    "@todo_DB_PASSWORD": "",
    "@todo_DB_USER": "",
}
```

This file is ignored by Git, and is the first check for the `from_env` function in `api/api/settings/base.py` before falling back to `ENV`.

## Todo

* Script to generate the Django secret key [@see](https://github.com/django/django/blob/master/django/utils/crypto.py)
* Logging (use console logger for dev)
* SMTP (use console for dev)
