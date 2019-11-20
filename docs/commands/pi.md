## pi or pacman 

The **`pi`** which is the shortcut formation of **`pacman`** is one of the majority features of our System. It is a combination of simple binary package manager with easy-open-source-to-use build system.

### How to Install Pi


To install pi package on your system, follow these steps:
```
    1. Downloads pi.tar.gz in your Downloads folder

    2. Run tar -xvf pi.tar.gz

    3. In the terminal run cd pi-update

    4. In the terminal do sudo chmod +x run

    5. In the terminal do ./run

    6. Test if pi is installed do pi
```
### Update the System
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
### Install Packages
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
### Removing packages
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

Operations:

```text
    $ pi {-h --help}
    $ pi {-V --version}
    $ pi {-D --database}    # <options> <package(s)>
    $ pi {-F --files}        # [options] [package(s)]
    $ pi {-Q --query}       # [options] [package(s)]
    $ pi {-R --remove}      # [options] <package(s)>
    $ pi {-S --sync}        # [options] [package(s)]
    $ pi {-T --deptest}     # [options] [package(s)]
    $ pi {-U --upgrade}     # [options] <file(s)>
```

New operations:

```text
    $ pi {-Y --pi}          # [options] [package(s)]
    $ pi {-P --show}        # [options]
    $ pi {-G --getpkgbuild} # [package(s)]
```

New options:

```text
    --repo        # Assume targets are from the repositories
    -a --aur      # Assume targets are from the AUR
```

Permanent configuration options:

```text
    --save                Causes the following options to be saved back to the
                          config file when used

    --aururl      <url>    # Set an alternative AUR URL  
    --builddir    <dir>    # Directory used to download and run PKGBUILDS
    --editor      <file>    # Editor to use when editing PKGBUILDs
    --editorflags <flags>    # Pass arguments to editor
    --makepkg     <file>    # makepkg command to use  
    --mflags      <flags>    # Pass arguments to makepkg
    --pacman      <file>    # pacman command to use
    --tar         <file>    # bsdtar command to use
    --git         <file>    # Git command to use  
    --gitflags    <flags>    # Pass arguments to git
    --gpg         <file>    # gpg command to use  
    --gpgflags    <flags>    # Pass arguments to gpg
    --config      <file>     # pacman.conf file to use
    --makepkgconf <file>    # makepkg.conf file to use
    --nomakepkgconf        # Use the default makepkg.conf

    --requestsplitn <n>    # Max amount of packages to query per AUR request
    --completioninterval   # <n> Time in days to to refresh completion cache
    --sortby    <field>     # Sort AUR results by a specific field during search
    --answerclean   <a>    # Set a predetermined answer for the clean build menu
    --answerdiff    <a>     # Set a predetermined answer for the diff menu
    --answeredit    <a>    # Set a predetermined answer for the edit pkgbuild menu
    --answerupgrade <a>    # Set a predetermined answer for the upgrade menu
    --noanswerclean        # Unset the answer for the clean build menu
    --noanswerdiff          # Unset the answer for the edit diff menu
    --noansweredit         # Unset the answer for the edit pkgbuild menu
    --noanswerupgrade      # Unset the answer for the upgrade menu
    --cleanmenu            # Give the option to clean build PKGBUILDS
    --diffmenu              # Give the option to show diffs for build files
    --editmenu             # Give the option to edit/view PKGBUILDS
    --upgrademenu          # Show a detailed list of updates with the option to skip any
    --nocleanmenu          # Don't clean build PKGBUILDS
    --nodiffmenu            # Don't show diffs for build files
    --noeditmenu           # Don't edit/view PKGBUILDS
    --noupgrademenu        # Don't show the upgrade menu
    --askremovemake        # Ask to remove makedepends after install
    --removemake           # Remove makedepends after install
    --noremovemake         # Don't remove makedepends after install

    --cleanafter           # Remove package sources after successful install
    --nocleanafter         # Do not remove package sources after successful build
    --bottomup             # Shows AUR's packages first and then repository's
    --topdown              # Shows repository's packages first and then AUR's

    --devel                # Check development packages during sysupgrade
    --nodevel              # Do not check development packages
    --gitclone             # Use git clone for PKGBUILD retrieval
    --nogitclone           # Never use git clone for PKGBUILD retrieval
    --rebuild              # Always build target packages
    --rebuildall           # Always build all AUR packages
    --norebuild            # Skip package build if in cache and up to date
    --rebuildtree          # Always build all AUR packages even if installed
    --redownload           # Always download pkgbuilds of targets
    --noredownload         # Skip pkgbuild download if in cache and up to date
    --redownloadall        # Always download pkgbuilds of all AUR packages
    --provides             # Look for matching providers when searching for packages
    --noprovides           # Just look for packages by pkgname
    --pgpfetch             # Automatically resolve conflicts using pacman's ask flag
    --nouseask             # Confirm conflicts manually during the install
    --combinedupgrade      # Refresh then perform the repo and AUR upgrade together
    --nocombinedupgrade    # Perform the repo upgrade and AUR upgrade separately

    --sudoloop             # Loop sudo calls in the background to avoid timeout
    --nosudoloop           # Do not loop sudo calls in the background

    --timeupdate           # Check packages' AUR page for changes during sysupgrade
    --notimeupdate         # Do not check packages' AUR page for changes
```

Show specific options:

```text
    -c --complete         # Used for completions
    -d --defaultconfig     # Print default pi configuration
    -g --currentconfig     # Print current pi configuration
    -s --stats            # Display system package statistics
    -w --news             # Print arch news
```

Pi specific options:

```text
    -c --clean            # Remove unneeded dependencies
       --gendb            # Generates development package DB used for updating
```

getpkgbuild specific options:

```text
    -f --force            # Force download for existing tar packages
```

Developed by @LyhourChhen
