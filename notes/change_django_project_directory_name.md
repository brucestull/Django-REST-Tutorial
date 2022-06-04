# Change Django Project Directory Name

## Process:

1. Start in root of project directory:
        ```
        Get-Location
        ```
    * Sample location output:
        ```
        PS C:\Users\Bruce\Programming\test-directory> Get-Location

        Path
        ----
        C:\Users\Bruce\Programming\test-directory
        ```

1. Note the Django project directory name:
    ```
    Get-ChildItem
    ```
    ```
    PS C:\Users\Bruce\Programming\DjangoStarter> Get-ChildItem

        Directory: C:\Users\Bruce\Programming\DjangoStarter

    Mode                 LastWriteTime         Length Name
    ----                 -------------         ------ ----
    ...
    d----          2022-06-03    12:02                my_current_project
    ...
    ```

1. Decide new django project directory name:
    * Example directory name:
        ```
        django_starter
        ```

1. Do global search for `my_current_project`:
    * INSERT-IMAGE-HERE

1. Replace the instances of `my_current_project` with your new project directory name `django_starter`:
    * INSERT-IMAGE-HERE

1. Rename django project directory:
    ```
    Rename-Item -Verbose -Path .\my_current_project\ -NewName django_starter
    ```
    * Sample output:
    ```
    PS C:\Users\Bruce\Programming\DjangoStarter> Rename-Item -Verbose -Path .\my_current_project\ -NewName django_starter
    VERBOSE: Performing the operation "Rename Directory" on target "Item: C:\Users\Bruce\Programming\DjangoStarter\my_current_project\ Destination: C:\Users\Bruce\Programming\DjangoStarter\django_starter".
    ```

1. Inspect current directory contents and note changed django project directory name:
    ```
    Get-ChildItem
    ```
    ```
    PS C:\Users\Bruce\Programming\DjangoStarter> Get-ChildItem

        Directory: C:\Users\Bruce\Programming\DjangoStarter

    Mode                 LastWriteTime         Length Name
    ----                 -------------         ------ ----
    ...
    d----          2022-06-03    22:15                django_starter
    ...
    ```

1. Test server:
    1. Run server:
        ```
        python manage.py runserver
        ```
    
    1. Open browser to server address:
        * http://localhost:8000/
    
    1. Maybe click the "Django Admin" link to check functionality.

1. User should now have a functioning Django project, ready for addition of specific project application needs.

1. Continue on and add your own functionality.

## Links
* [README.md](../README.md)