# Pionux Commands - CLI
[//]: # (TODO: format)

Usage:
	pi
    pi <operation> [...]
	pi <package(s)>
	----------------------------------------------------------
	| Welcome to pi - the official package manager for KOOMPI  |
	----------------------------------------------------------
	V0.0.1
	
Basic usage
	-------------------------------------------------
	| Install packages use                           |
	| pi -S <package name> or pi -i <Package name> 	 |	
	| Uninstall packages           	                 |
	| pi -R <Package name>			         |
	-------------------------------------------------		

Special usage to automate the install procedure (Recommend)

	---------------------------------------------------------------------
	| yes | pi -S <Package name>  => [Install packages with no confirm] |	
	---------------------------------------------------------------------


operations:
    pi {-h --help}
    pi {-V --version}
    pi {-D --database}    <options> <package(s)>
    pi {-F --files}       [options] [package(s)]
    pi {-Q --query}       [options] [package(s)]
    pi {-R --remove}      [options] <package(s)>
    pi {-S --sync}        [options] [package(s)]
    pi {-T --deptest}     [options] [package(s)]
    pi {-U --upgrade}     [options] <file(s)>

New operations:
    pi {-Y --pi}         [options] [package(s)]
    pi {-P --show}        [options]
    pi {-G --getpkgbuild} [package(s)]

New options:
       --repo             Assume targets are from the repositories
    -a --aur              Assume targets are from the AUR

Permanent configuration options:
    --save                Causes the following options to be saved back to the
                          config file when used

    --aururl      <url>   Set an alternative AUR URL
    --builddir    <dir>   Directory used to download and run PKGBUILDS
    --editor      <file>  Editor to use when editing PKGBUILDs
    --editorflags <flags> Pass arguments to editor
    --makepkg     <file>  makepkg command to use
    --mflags      <flags> Pass arguments to makepkg
    --pacman      <file>  pacman command to use
    --tar         <file>  bsdtar command to use
    --git         <file>  git command to use
    --gitflags    <flags> Pass arguments to git
    --gpg         <file>  gpg command to use
    --gpgflags    <flags> Pass arguments to gpg
    --config      <file>  pacman.conf file to use
    --makepkgconf <file>  makepkg.conf file to use
    --nomakepkgconf       Use the default makepkg.conf

    --requestsplitn <n>   Max amount of packages to query per AUR request
    --completioninterval  <n> Time in days to to refresh completion cache
    --sortby    <field>   Sort AUR results by a specific field during search
    --answerclean   <a>   Set a predetermined answer for the clean build menu
    --answerdiff    <a>   Set a predetermined answer for the diff menu
    --answeredit    <a>   Set a predetermined answer for the edit pkgbuild menu
    --answerupgrade <a>   Set a predetermined answer for the upgrade menu
    --noanswerclean       Unset the answer for the clean build menu
    --noanswerdiff        Unset the answer for the edit diff menu
    --noansweredit        Unset the answer for the edit pkgbuild menu
    --noanswerupgrade     Unset the answer for the upgrade menu
    --cleanmenu           Give the option to clean build PKGBUILDS
    --diffmenu            Give the option to show diffs for build files
    --editmenu            Give the option to edit/view PKGBUILDS
    --upgrademenu         Show a detailed list of updates with the option to skip any
    --nocleanmenu         Don't clean build PKGBUILDS
    --nodiffmenu          Don't show diffs for build files
    --noeditmenu          Don't edit/view PKGBUILDS
    --noupgrademenu       Don't show the upgrade menu
    --askremovemake       Ask to remove makedepends after install
    --removemake          Remove makedepends after install
    --noremovemake        Don't remove makedepends after install

    --cleanafter          Remove package sources after successful install
    --nocleanafter        Do not remove package sources after successful build
    --bottomup            Shows AUR's packages first and then repository's
    --topdown             Shows repository's packages first and then AUR's

    --devel               Check development packages during sysupgrade
    --nodevel             Do not check development packages
    --gitclone            Use git clone for PKGBUILD retrieval
    --nogitclone          Never use git clone for PKGBUILD retrieval
    --rebuild             Always build target packages
    --rebuildall          Always build all AUR packages
    --norebuild           Skip package build if in cache and up to date
    --rebuildtree         Always build all AUR packages even if installed
    --redownload          Always download pkgbuilds of targets
    --noredownload        Skip pkgbuild download if in cache and up to date
    --redownloadall       Always download pkgbuilds of all AUR packages
    --provides            Look for matching providers when searching for packages
    --noprovides          Just look for packages by pkgname
    --pgpfetch            Prompt to import PGP keys from PKGBUILDs
    --nopgpfetch          Don't prompt to import PGP keys
    --useask              Automatically resolve conflicts using pacman's ask flag
    --nouseask            Confirm conflicts manually during the install
    --combinedupgrade     Refresh then perform the repo and AUR upgrade together
    --nocombinedupgrade   Perform the repo upgrade and AUR upgrade separately

    --sudoloop            Loop sudo calls in the background to avoid timeout
    --nosudoloop          Do not loop sudo calls in the background

    --timeupdate          Check packages' AUR page for changes during sysupgrade
    --notimeupdate        Do not check packages' AUR page for changes

show specific options:
    -c --complete         Used for completions
    -d --defaultconfig    Print default pi configuration
    -g --currentconfig    Print current pi configuration
    -s --stats            Display system package statistics
    -w --news             Print arch news

pi specific options:
    -c --clean            Remove unneeded dependencies
       --gendb            Generates development package DB used for updating

getpkgbuild specific options:
    -f --force            Force download for existing tar packages

If no arguments are provided 'pi -Syu' will be performed
If no operation is provided -Y will be assumed

Ask more support, please go to https://t.me/kramaos
Developed by @LyhourChhen
