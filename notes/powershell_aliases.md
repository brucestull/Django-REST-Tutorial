# PowerShell Aliases

* Short list of some mappings of PowerShell commands to their linux-type commands.

## Linux-type to PowerShell command mappings:

* `cd`:
    ```
    Set-Location
    ```
    ```
    PS C:\Users\Bruce\Programming> Get-Alias cd

    CommandType     Name                                               Version    Source
    -----------     ----                                               -------    ------
    Alias           cd -> Set-Location
    ```

* `ls`:
    ```
    Get-ChildItem
    ```
    ```
    PS C:\Users\Bruce\Programming> Get-Alias ls

    CommandType     Name                                               Version    Source
    -----------     ----                                               -------    ------
    Alias           ls -> Get-ChildItem
    ```

* `pwd`:
    ```
    Get-Location
    ```
    ```
    PS C:\Users\Bruce\Programming> Get-Alias pwd

    CommandType     Name                                               Version    Source
    -----------     ----                                               -------    ------
    Alias           pwd -> Get-Location
    ```

## Links:
* [README.md](../README.md)