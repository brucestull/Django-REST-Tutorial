# Django REST Tutorial

## Resources:
* Tutorial being followed:
    * [Django REST Framework](https://www.django-rest-framework.org/tutorial/quickstart/)
* Production deployment:
    * 
* Project repository:
    * https://github.com/brucestull/Django-REST-Tutorial
* Project management board:
    * https://github.com/brucestull/Django-REST-Tutorial/projects/1
* Some terminal commands as PowerShell aliases:
    * [PowerShell Aliases](notes/powershell_aliases.md)

## Notes:
* The author is using PowerShell for terminal operations. Use appropriate terminal commands as necessary when using a different terminal application.
* When perfoming Django database migrations, it is important to do `makemigrations` and `migrate` for `users` app and then do for the rest of the app. This flow is take care of in Production by the `Procfile`.
* This guide is starting off with this author's Django Starter:
    * https://github.com/brucestull/DjangoStarter
    * The Django Starter includes the following:
        * Premade Django Project (my_current_project).
        * A premade CustomeUser model, with signup/login/logout, in a (users) app.
        * Django settings config files have been spread across development and production files, all in a `settings` directory (common.py, development.py, production.py).
        * Project is ready to deploy to Heroku with Heroku-specific imports and usage in settings config, and included `Procfile`.
  
## Guides:
1. [Clone DjangoStarter](notes/clone_repository.md)
1. [Change the remote repository to our own repository](notes/change_remote_repository.md)
1. Run Django Project Locally
    * [Run Django Project Locally](notes/run_django_project_locally.md)
    * [Run Django Project Locally (abridged)](notes/run_django_project_locally_abridged.md)
1. [Change the Django project directory name](notes/change_django_project_directory_name.md)
1. Add your own apps and functionality.
