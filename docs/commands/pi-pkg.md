
#  Pi Package

[Pionux](https://pionux.org/) is a fully customized and self-customizable Cambodia based open-source operating system software solution for up and coming engineers, inventors, organizers, developers and basically free thinkers in a modern-day post-Microsoft world.

## pi or pacman 

The **`pi`** which is the shortcut formation of **`pacman`** is one of the majority features of our System. It is a combination of simple binary package manager with easy-open-source-to-use build system.


> Note: Make sure you have `pi` installed and your `system is fully up to date` before installing. 

If you haven't done it yet.[Click here](https://github.com/koompi/users-guide/blob/master/commands/pi-installation.md)

Usage:
```
    $ pi
    $ pi <operation> [...]
    $ pi <package(s)>
```
> **Noted:** Packages often have optional dependencies which are packages that provide additional functionality to the application but not strictly required for running it. When installing a package, the list of package optionals dependencies will be pop up.

> **Warning:** When installing packages, avoid refreshing the packages list without updated the system. In practice for running command  do **not** run ```$ pi -Sy package_name``` instead of ``` $ pi -Syu package_name```, as it could lead to dependency issues.
Basic usage:
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
## Uninstall packages
```    
    $ pi -R <Package name>
```
> **Note:** All operation is required password.Then if you aren’t satisfied with the build tool and configuration choices, you can eject at any time. This command will remove the single build dependency from your operation.

Here Special usage to automate the install procedure (Recommend):
```
	$ yes | pi -S <Package name> or $ pi -S --noconfirm <Package name> => [Install packages with no confirm] |	
```