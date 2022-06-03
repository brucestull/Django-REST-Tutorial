# Clone DjangoStarter

## Process:
1. Start in directory where the repository directory will be located.
    * Sample location:
        * `C:\Users\Bruce\Programming`

1. Clone the repository:
    * Clone with default directory name for local repository directory:
        ```
        git clone https://github.com/brucestull/DjangoStarter
        ```
    * Clone with user-provided directory name for local repository directory:
        ```
        git clone https://github.com/brucestull/DjangoStarter user-provided-directory-name
        ```

1. Change directory into the newly created repository:
    ```
    Set-Location DjangoStarter
    ```

1. Verify repository contents:
    ```
    Get-ChildItem
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> Get-ChildItem

            Directory: C:\Users\Bruce\Programming\DjangoStarter

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        d----          2022-06-03    10:34                my_current_project
        d----          2022-06-03    10:34                notes
        d----          2022-06-03    10:34                templates
        d----          2022-06-03    10:34                users
        -a---          2022-06-03    10:34           1455 .gitignore
        -a---          2022-06-03    10:34          35823 LICENSE
        -a---          2022-06-03    10:34            708 manage.py
        -a---          2022-06-03    10:34            244 Pipfile
        -a---          2022-06-03    10:34           9066 Pipfile.lock
        -a---          2022-06-03    10:34            106 Procfile
        -a---          2022-06-03    10:34            643 README.md
        ```

1. The project can now be run locally:
    * [Run Django Project Locally](run_django_project_locally.md)
    * [Run Django Project Locally (abridged)](run_django_project_locally_abridged.md)

1. Proceed to change remote repository settings.
    * [Change Remote Repository](change_remote_repository.md)

## Links
* [README.md](../README.md)