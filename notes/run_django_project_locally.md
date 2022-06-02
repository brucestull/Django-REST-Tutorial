# Run Django Project Locally

## Prepare:

1. Verify `python` and `pipenv` installed:
    * `pip list`

## Process:

1. Create `pipenv` virtual environment:
    * `pipenv install`

1. Activate virtual environment:
    * `C:\Users\Bruce\.virtualenvs\DjangoHeroku-test-MdRWzatq\Scripts\activate.ps1`

1. Perform migrations:
    1. `python manage.py makemigrations users`
    1. `python manage.py migrate users`
    1. `python manage.py migrate`

1. Create `superuser`:
    * `python manage.py createsuperuser`

1. Test server:
    1. Run server:
        * `python manage.py runserver`
    1. Open browser to server address:
        * http://localhost:8000/
