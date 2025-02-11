
## Pre-requisites

- Following tool should be installed:
    
    - [SQLite Browser](https://linuxhint.com/install_sqlite_browser_ubuntu_1804/)
        
        ```
        $ sudo apt-get install sqlitebrowser
        ```
        

## Why

Mobile applications interact with local system in order to store persistent/temporary data, and SQLite is the most preferred format to store persistent data.

Unless an encrypted variant of SQLite is used, the data stored in simple SQLite file is not secure. An attacker having access to the SQLite file can view its contents using any SQLite client.

## What

During vulnerability assessment of a mobile application, the analyst should check if any sensitive data has been stored locally on the the device, in unencrypted SQLite databases. In order to do this check, the analyst can follow these steps:

Locate database files Read contents of database files using SQLite Browser

## How

1. Using adb, view files in `/data/data/<app-folder>/databases/`
    
    ```
     $ adb shell ls /data/data/<app-folder>/databases/
    ```
    
2. Copy the database files (e.g., `.db`, `.sqlite`) to your local system.
    
    ```
     $ adb pull /data/data/<app-folder>/databases/<filename>.db
    ```
    
3. Use SQLite Browser to read the contents of the database files.
    
    ![Sqlite Browser](https://null-android-pentesting.netlify.app/src/image/tools/3-sqlite-browser.png)