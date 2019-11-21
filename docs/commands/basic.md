# Basic Commands in Pionux

> Noted: To do all these basic commands below, you must be in the terminal:


To show the directory you are currently in:
```
    [koompi@koompi-pc ~]$ pwd
```
Output :
```
    /home/koompi
```
Use "ls" for showing all the files in your directory:
```
    [koompi@koompi-pc ~]$ ls
```
Output :
```
    Desktop         Save               dconf       mkrepo     
    Documents       Videos             Downloads   code    
    Musics          example.desktop
```
Use "ls -a" to list down even the hidden files:
```
    [koompi@koompi-pc ~]$ ls -a
```
Output :
```
    .               ..                 .mozilla        .viminfo
    .vscode-oss     Save               dconf           mkrepo   
    Desktop         Videos             Documents       Downloads           
    Musics          example.desktop    code
 ```
 " cd " ― Use this command for go into other directory.If you are in /home/koompi you want go into *Documents*:
 ```
    [koompi@koompi-pc ~]$ pwd
    /home/koompi
    [koompi@koompi-pc ~]$ cd Documents/
```
Output :
```
    [koompi@koompi-pc Documents]$
```
To create file " Touch ":
```
    $ touch <file name with extension >
```
For example :
```
    $ touch Name.txt
```
To create a directory, you must use:
``` 
    $ mkdir <name of directory you want to put>
```
For removing the directory, you can use:
```
    $ rmdir <name of directory you want to delete>
```
> Noted : This command only working when your directory is empty.
To delete directory or files, "rm" it is:
```
    $ rm <file's name or directory's name>
```
> Tips : Not Strongly Recommended.
>
> Warning : Not only empty directory or file, but also everything!!!
If you cant't delete, you can use command below to force remove:

```
    $ rm -rf <directory or files's name>
```
Need some help with commands, this would be useful:
```
    $ man cd or $ cd --help
```
(" cd ") is the command you want to know more info.
Output :
```
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value 
    HOME shell variable.
    
    The variable CDPATH defines the search path for the directory conta
    DIR.  Alternative directory names in CDPATH are separated by a colo
    A null directory name is the same as the current directory.  If DIR
    with a slash (/), then CDPATH is not used.
    
    If the directory is not found, and the shell option `cdable_vars' i
    the word is assumed to be  a variable name.  If that variable has a
    its value is used for DIR.
    
    Options:
      -L        force symbolic links to be followed: resolve symbolic
                links in DIR after processing instances of `..'
      -P        use the physical directory structure without following
                symbolic links: resolve symbolic links in DIR before
                processing instances of `..'
      -e        if the -P option is supplied, and the current working
                directory cannot be determined successfully, exit with
                a non-zero status
      -@        on systems that support it, present a file with extende
                attributes as a directory containing the file attribute
    
    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname com
    back to a slash or the beginning of DIR.
    
    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successful
    -P is used; non-zero otherwise.
```
You know, you can also copy file through command. It takes only two arguments: The first is the location of the file to be copied, the second is where to copy.
```
    [koompi@koompi-pc ~]$ ls
    Desktop         Save               dconf       mkrepo     
    Documents       Videos             Downloads   code    
    Musics          example.desktop    New.txt
    [koompi@koompi-pc ~]$ cp New.txt /Documents
```
Let's check in *Documents* directory:
```
    [koompi@koompi-pc ~]$ ls Documents/
    New.txt
```
"mv" ― You know, you can also move file through command. It takes only two arguments like `cp`:
```
    [koompi@koompi-pc ~]$ ls
    Desktop         Save               dconf       mkrepo     
    Documents       Videos             Downloads   code    
    Musics          example.desktop    New.txt
    [koompi@koompi-pc ~]$ mv New.txt /Documents
```
Here in *Documents* directory:
```
    [koompi@koompi-pc ~]$ ls Documents/
    New.txt
```
If you want to search for the locateion of the file, you can use **locate**:
```command
    $ locate <file_name>
```
## Intermediate Commands in Pionux

- The **echo** command helps us move some data, usually text into file.For example, if you want to create a new text file or add to an already made text file, you just need to type in, **“echo Hello, This is Pionux. >> new.txt”**.

- **cat** is the command for showing the contents in file. It is usually used to easily view programs. 
```
    [koompi@koompi-pc ~]$ echo Hello, This is Pionux. >> new.txt
    [koompi@koompi-pc ~]$ cat new.txt
```
Output :
```text
    Hello, This is Pionux.
```
- "**nano**" and "**vi**" are already installed in Pionux command line. The **nano** command is a good text editor that denotes keywords with color and can recognize most languages. And **vi** is simpler than nano.
- **sudo** — A widely used command in the Linux command line, sudo stands for "SuperUser Do". So, if you want any command to be done with administrative or root privileges, you can use the sudo command. 
you can change root password by using command below:
```
    [koompi@koompi-pc ~]$ sudo passwd
```
Output :
```
    New password: 
    Retype new password: 
    passwd: password updated successfully
```
> Tips : When you type the password it was hidden you can't see.

- **df** — We use **df**  command to see the available disk space in each of the partitions in your system. You can add more options like **-h** to see size in gigabyte.
```
    [koompi@koompi-pc ~]$ df -h
```
Output :
```
    ilesystem      Size  Used Avail Use% Mounted on
    dev             3.9G     0  3.9G   0% /dev
    run             3.9G   18M  3.9G   1% /run
    /dev/sdb6        58G   33G   23G  60% /
    tmpfs           3.9G   85M  3.8G   3% /dev/shm
    tmpfs           3.9G     0  3.9G   0% /sys/fs/cgroup
    tmpfs           3.9G   15M  3.9G   1% /tmp
    tmpfs           3.9G  1.5M  3.9G   1% /etc/pacman.d/gnupg
    tmpfs           786M   20K  786M   1% /run/user/1001
```
----



















   