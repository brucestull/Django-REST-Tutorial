# Run Django Project Locally

## Prepare:

1. Verify `python` installed globally:
    ```
    python --version
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> python --version
        Python 3.10.4
        ```

1. Verify `pipenv` installed globally:
    ```
    pipenv --version
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> pipenv --version
        pipenv, version 2022.1.8
        ```

## Process:

1. Start in root of project repository:
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

1. Verify local repository contents:
    ```
    Get-ChildItem
    ```
    * Sample current directory contents:
        ```
        (DjangoStarter) PS C:\Users\Bruce\Programming\DjangoStarter> Get-ChildItem

            Directory: C:\Users\Bruce\Programming\DjangoStarter

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        d----          2022-06-02    10:05                my_current_project
        d----          2022-06-02    16:20                notes
        d----          2022-06-02    10:13                staticfiles
        d----          2022-06-02    09:44                templates
        d----          2022-06-02    09:44                users
        -a---          2022-05-25    13:41           1455 .gitignore
        -a---          2022-04-02    08:55          35823 LICENSE
        -a---          2022-05-15    15:50            708 manage.py
        -a---          2022-05-15    11:49            244 Pipfile
        -a---          2022-05-15    11:49           9066 Pipfile.lock
        -a---          2022-05-15    11:49            106 Procfile
        -a---          2022-06-02    16:20            308 README.md
        ```

1. Create `pipenv` virtual environment:
    ```
    pipenv install
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> pipenv install
        Creating a virtualenv for this project...
        Pipfile: C:\Users\Bruce\Programming\DjangoStarter\Pipfile
        Using C:/Users/Bruce/AppData/Local/Programs/Python/Python310/python.exe (3.10.4) to create virtualenv...
        [=   ] Creating virtual environment...created virtual environment CPython3.10.4.final.0-64 in 2817ms
        creator CPython3Windows(dest=C:\Users\Bruce\.virtualenvs\DjangoStarter-WkL7vbpe, clear=False, no_vcs_ignore=False, global=False)
        seeder FromAppData(download=False, pip=bundle, setuptools=bundle, wheel=bundle, via=copy, app_data_dir=C:\Users\Bruce\AppData\Local\pypa\virtualenv)
            added seed packages: pip==22.0.4, setuptools==62.1.0, wheel==0.37.1
        activators BashActivator,BatchActivator,FishActivator,NushellActivator,PowerShellActivator,PythonActivator

        Successfully created virtual environment!
        Virtualenv location: C:\Users\Bruce\.virtualenvs\DjangoStarter-WkL7vbpe
        Installing dependencies from Pipfile.lock (5c8b0c)...
        ================================ 11/11 - 00:00:09
        To activate this project's virtualenv, run pipenv shell.
        Alternatively, run a command inside the virtualenv with pipenv run.
        ```

1. Note directory path on line with `Virtualenv location: `. This shows the virtual environment location:
    * Sample output:
        * `C:\Users\Bruce\.virtualenvs\DjangoStarter-WkL7vbpe`

1. That location will determine the locations of activation scripts for various terminal programs. I'm using PowerShell (which is the `activate` script with `ps1` extension):
    * Sample location:
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
* [Run Django Project Locally (abridged)](run_django_project_locally_abridged.md)
* [README.md](../README.md)



