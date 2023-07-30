# django-project-01
django-project-01

## Future Tasks
- [x] Add auto formatting
- [ ] Connect to postgres database
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


## Reference
1. https://blog.logrocket.com/django-rest-framework-create-api/#what-is-rest-api - Starting reference for the project
