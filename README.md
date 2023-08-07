# django-project-01
django-project-01

## Future Tasks
- [x] Add auto formatting
- [x] Connect to postgres database
- [ ] Host it on a server
  - [ ] Find a service to host django application for free
  - [ ] Host the application on the server
- [ ] Add additional features to the API
  - [ ] Add date and time at which the task needs to be done
  - [ ] Add notification
- [ ] Connect the django application to a react frontend

## Commands

### Django
After making changes to the `models.py` file run the following commands

```bat
python manage.py makemigrations
```

```bat
python manage.py migrate
```

To run the APIs run the following command

```bat
python manage.py runserver
```

### Pre-commit
To auto-update the hooks
```
pre-commit autoupdate
```

To install pre-commit
```
pre-commit install
```

to run pre-commit on all files
```
pre-commit run --all-files
```

To skip a line add `# nosec` at the end of the line

## Log

### How to conect to Postgres DB

1. Download postgres from the [link](https://www.postgresql.org/download)
2. Go through the installation steps
3. Create a role `backend` with appropriate rights and assign it a password
4. Open file `settings.py` in the `todo` folder and update the following snippet of code from
    ```python
	DATABASES = {
		'default': {
			'ENGINE': 'django.db.backends.sqlite3',
			'NAME': BASE_DIR / 'db.sqlite3',
		}
	}
	```
	to
	```python
	DATABASES = {
		"default": {
			"ENGINE": "django.db.backends.postgresql",
			'NAME': 'postgres',
			'USER': 'backend',
			'PASSWORD': '<your password>',
			'HOST': 'localhost',
			'PORT': '5432'
		}
	}
	```
5. Then run the following command
	```shell
	python manage.py makemigrations
	```
	and
	```shell
	python manage.py migrate
	```
6. Once the migration is done run the django server
	```shell
	python manage.py runserver
	```

## Reference
1. https://blog.logrocket.com/django-rest-framework-create-api/#what-is-rest-api - Starting reference for the project
2. Precommit
    1. https://pre-commit.com/#intro - Precommit document
    2. https://gist.github.com/andyreagan/a3294561f3beff8a3622cfeee245b094 - Pre-commit configuration example
    3. https://ljvmiranda921.github.io/notebook/2018/06/21/precommits-using-black-and-flake8/ - Pre-commit configuration example
    4. https://pre-commit.com/hooks.html - Pre-commit hooks list
3. Database
	1. https://www.guru99.com/download-install-postgresql.html - Download Postgres
	2. https://www.w3schools.com/django/django_db_connect.php - Update Django settings
