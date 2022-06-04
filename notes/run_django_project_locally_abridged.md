# Run Django Project Locally (abridged)

## Process:

1. Start in root of project repository.
    ```
    Get-Location
    ```
    * Sample location:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> Get-Location

        Path
        ----
        C:\Users\Bruce\Programming\DjangoStarter
        ```


1. Create `pipenv` virtual environment:
    ```
    pipenv install
    ```

1. Note directory path, in output above, on line with `Virtualenv location: `. This shows the virtual environment location:
    * Sample output:
        * `Virtualenv location: C:\Users\Bruce\.virtualenvs\DjangoStarter-WkL7vbpe`

1. That virtual environment location will determine the locations of activation scripts for various terminal programs. I'm using PowerShell (which uses the `activate` script with `ps1` extension):
    * Sample virtual environment activation script location:
        * `C:\Users\Bruce\.virtualenvs\DjangoStarter-WkL7vbpe\Scripts\activate.ps1`

1. Activate virtual environment:
    ```
    C:\Users\Bruce\.virtualenvs\[user's virtual environment directory]\Scripts\activate.ps1
    ```

1. Perform migrations:
    ```
    python manage.py makemigrations users
    ```
    ```
    python manage.py migrate users
    ```
    ```
    python manage.py migrate
    ```

1. Create `superuser`:
    ```
    python manage.py createsuperuser
    ```

1. Test server:
    1. Run server:
        ```
        python manage.py runserver
        ```
    1. Open browser to server address:
        * http://localhost:8000/

1. It may be necessary to run the activation script each time a new terminal is opened in order to have access to the features of the virtual environment.
    * LINK-TO-SET-UP-VSCODE-WORKSPACE-VIRTUAL-ENVIRONMENT

1. Proceed to change django project directory name:
    * [Change Django Project Directory Name](change_django_project_directory_name.md)

## Links
* [Run Django Project Locally](run_django_project_locally.md)
* [README.md](../README.md)
