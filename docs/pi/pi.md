## pi or pacman 

The **`pi`** which is the shortcut formation of **`pacman`** is one of the majority features of our System. It is a combination of simple binary package manager with easy-open-source-to-use build system.

Some very basic commands.

### To update the System
```
    $ pi -Syu
```
To update the Database:
```
    $ pi -Syy
```

### Pi Usage
``` 
    $ pi
    $ pi <operation> [...]
    $ pi <package(s)>
```
> Note: Make sure you have your `system is fully up to date` before installing. 

> **Noted:** Packages often have optional dependencies which are packages that provide additional functionality to the application but not strictly required for running it. When installing a package, the list of package optionals dependencies will be pop up.

> **Warning:** "When installing packages, avoid refreshing the packages list without updated the system. In practice for running command  do **not** run ```$ pi -Sy package_name``` instead of ``` $ pi -Syu package_name```, as it could lead to dependency issues.
Basic usage:
> Note: Make sure you have your `system is fully up to date` before installing. 
## Install Packages
To installing a signal package, including the dependencies, follow the following command:
```  
    $ pi -S <Package name> or pi -i <Package name>
```
To installing the list of packages:
```sh
    $ pi -S <Package name1 Package name2 ...>
```
### Installing Package Group
Some packages belong to a **group of packages** that call be installed at the same time. For example as down here:
```sh
    $ sudo pi -S <Package group name>
```
To see what inside the package group, run:
```sh
    $ pi -Sg <Package group name>
```
## Removing packages
If you want to only remove the package, the following command is sufficient:
```    
    $ pi -R <Package name>
```
To remove the package and those of its dependencies that aren’t needed by any other application, do
```
    $ pi -Rs <Package name>
```
To remove a package, its dependencies and all the packages that depend on the target package:
```
    $ pi -Rsc <Package name>
```
To remove a package, which is required by another package, without removing the dependent package:
```
    $ pi -Rdd <Package name>
```
> **Note:** All operation is required password.Then if you aren’t satisfied with the build tool and configuration choices, you can eject at any time. This command will remove the single build dependency from your operation.

Here Special usage to automate the install procedure (Recommend):
```
	$ yes | pi -S <Package name> or $ pi -S --noconfirm <Package name> => [Install packages with no confirm] |
```
