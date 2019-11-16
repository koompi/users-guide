# Pionux Guideline
[Pionux](https://pionux.org) is a fully customized and self-customizable Cambodia based open-source operating system software solution for up and coming engineers, inventors, organizers, developers and basically free thinkers in a modern-day post-Microsoft world.
## pacman or pi
The **`pi`** which is the shortcut formation of **`pacman`** is one of the majority features of our fully customized System. It is a combination of simple binary package format with easy-open-source-to-use build system.

`Pi or Pacman` keeps the system up to date by synchronizing package lists with the master server. This server model also allows the user to download/install the packages with a simple command, with complete dependencies required. [Click here]() for commands.

## Installing git
In order to do this, We need to have the git installed and make sure your system is fully up to date before installing anything:

```sh
$ sudo pi -Syu 
```
Next:
```sh
$ sudo pi -S git
```
**Tips** If a package in the list is already installed on the system,it will be reinstalled even if it is already up to date. This behavior can be overridden with the --needed option.
**Note:** You will be asking for a password.Then if you aren’t satisfied with the build tool and configuration choices, you can eject at any time. This command will remove the single build dependency from your operation.

## Installing Packages


> **Noted:** Packages often have optional dependencies which are packages that provide additional functionality to the application but not strictly required for running it. When installing a package, the list of package optionals dependencies will be pop up.

> **Warning:** When installing packages, avoid refreshing the packages list without updated the system. In practice for running command  do **not** run ```$ sudo pi -Sy package_name``` instead of ``` $ sudo pi -Syu package_name```, as it could lead to dependency issues.

### Installing Specific Packages
To installing a signal package, including the dependencies, follow the following command:
```sh
$ sudo pi -S package_name
```
To installing the list of packages, including the dependencies:
```sh
$ sudo pi -S package_name1 package_name2 ...
```
Sometimes there are multiple versions of package in different repositories. To install it from *extra* reposiory you need to defined it in front of package name like in the example below:
```sh
$ sudo pi extra/package_name
```
To install a number of packages sharing similar patterns in their names one can use curly brace expansion. For example:
```sh
$ sudo pi -S plasma-{desktop,mediacenter,nm}
```
This can be expanded to however many levels needed:
```sh
$ pacman -S plasma-{workspace{,-wallpapers},pa}
```
### Installing Package Group
Some packages belong to a **group of packages** that call be installed at the same time. For example as down here:
```sh
$ sudo pi -S gnome
```
```Noted:```After entered the command, there will be a bunch of packages from ***gnome*** for you wish to install.
> Tips: Sometime a package group will contain a large amount of packages, Instead of having all number packages to installed except the ones you do not want , it is sometimes more convienient to `select` or `exclude`packages with the followin syntax:
```sh
Enter a selection(default=all): 1-10 15
```
`Explaination:`*1-10* and *15* are the index of packages in packages group(gnome).
```sh
Enter a selection (default=all): ^6-9 ^2
```
`Explaination:`which will select all packages except 5 through 8 and 2 for installation.
To see what inside the package group, run:
```sh
$ sudo pi -Sg package_group_name
```




