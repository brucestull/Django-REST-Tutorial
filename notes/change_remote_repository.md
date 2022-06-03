# Change Remote Repository

## Resources:
* https://www.atlassian.com/git/tutorials/syncing

## Process:

1. Create remote repository:
    * Sample repository:
        * `https://github.com/brucestull/new-user-repo`

1. Open terminal in local repository:
    * Sample repository directory:
        * `C:\Users\Bruce\Programming\DjangoStarter`

1. Investigate current remote repository settings:
    ```
    git remote -v
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> git remote -v
        origin  https://github.com/brucestull/DjangoStarter.git (fetch)
        origin  https://github.com/brucestull/DjangoStarter.git (push)
        ```
1. Remove remote repository (https://github.com/brucestull/DjangoStarter.git) which has a 'name' of (origin) where repo was cloned from:
    ```
    git remote rm origin
    ```

1. Investigate current remote repository settings (There should be no remote repository listed since we removed the repository connection):
    ```
    git remote -v
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> git remote -v
        PS C:\Users\Bruce\Programming\DjangoStarter>
        ```

1. Add connection of our local repository to the remote repository (https://github.com/brucestull/new-user-repo) we created above. We are using the standard 'origin' name for remote repository:
    ```
    git remote add origin https://github.com/brucestull/new-user-repo
    ```

1. Verify proper remote repository connection:
    ```
    git remote -v
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> git remote -v
        origin  https://github.com/brucestull/new-user-repo (fetch)
        origin  https://github.com/brucestull/new-user-repo (push)
        ```

1. Push local repository contents to remote repository called 'origin':
    ```
    git push
    ```
    * Sample output (push didn't happen since we need to set the remote as upstream):
        ```
        PS C:\Users\Bruce\Programming\test-directory\DjangoStarter> git push
        fatal: The current branch main has no upstream branch.
        To push the current branch and set the remote as upstream, use

            git push --set-upstream origin main
        ```

1. Set the remote as upstream:
    ```
    git push --set-upstream origin main
    ```
    * Sample output:
        ```
        PS C:\Users\Bruce\Programming\DjangoStarter> git push --set-upstream origin main
        Enumerating objects: 89, done.
        Counting objects: 100% (89/89), done.
        Delta compression using up to 8 threads
        Compressing objects: 100% (52/52), done.
        Writing objects: 100% (89/89), 32.06 KiB | 32.06 MiB/s, done.
        Total 89 (delta 33), reused 89 (delta 33), pack-reused 0
        remote: Resolving deltas: 100% (33/33), done.
        To https://github.com/brucestull/new-user-repo
        * [new branch]      main -> main
        branch 'main' set up to track 'origin/main'.
        ```

1. Verify that our remote repository reflects the new code:
    * Sample remote repository link:
        * https://github.com/brucestull/new-user-repo

1. We now have the cloned repository connected to our own repository.

## Links
* [README.md](../README.md)