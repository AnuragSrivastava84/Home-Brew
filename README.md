# Homebrew

The purpose of this document is to give the overview about homebrew.


### Why do we use homebrew?

*“Homebrew is a free and open-source software package management system that simplifies the installation of software on macOS and Linux. It is similar to the other package manager like apt, yum etc. which are available for the Linux system”*

The purpose of a package management is to install the software by identify a legitimate source of the particular software and ensuring that any dependencies required by that software are installed and present as per the required version level. It is taking the cumbersome job of installation of the software from the users who are new to the MacOS and Linux system.

<br>

# Commands:
The list of which are required to install, uninstall and manage the pacakge or software are given below:

- **To install homebrew**
```mardown
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)
```

- **To list out the packages we can install with home brew**
```mardown
  brew search
```

- **To search any package**
```mardown
  brew search <package name>
```

-  **To install any package**
```mardown
   brew install <package name>
 ```     


### Note: 
_Homebrew installs the package into their own folder and then symlinks their files into /usr/local_
```markdown
The location of the homebrew package is 
/usr/local/Cellar/…
```

- **To get the information about package**
```mardown
  brew info <package name> 
```
    
If we use the same command to get the info of not installed package then the brew command will give all the details of the package and their respective dependencies, which is required to install.

-  **To uninstall the package**
```mardown
   brew uninstall <package name>
 ```   

- **To list out the package which is installed**
```mardown
  brew list
```    

- **To update the newest version of all of the packages of the brew**
```mardown
  brew update
```    

- **To list out the outdated packages which are installed**
```mardown
  brew outdated
```

- **To update all the outdated packages**
```mardown
  brew upgrade 
```    

- **To update the specific outdated package**
```mardown
  brew upgrade <package name>
```    

- **To stop something from being updated/upgrade**
```mardown
  brew pin <package name>
```    

- **To allow that formulae to update again** 
```mardown
  brew unpin <package name>
```    


### Note:
_By default homebrew uninstall the old version packages after 30 days._


- **To remove all the older version of the packages manually**
```mardown
  brew cleanup
```
- **To remove specific older version of the package manually**
```mardown
  brew cleanup <package name>
```    

- **To disable the homebrew automatic clean up**
```mardown
  export HOMEBREW_NO_INSTALL_CLEANUP=1
```    


### Note:
If you ever come up with any problem with homebrew then homebrew comes up with self diagnosis tool, which diagnose the issue.

- **To diagnose homebrew issue**
```mardown
  brew doctor
```

<br>

# Homebrew Cask
To install Mac OS native application homebrew uses cask to install Mac OS application into the system

- **To install Mac OS application**
```mardown
    brew cask <software/app name>
```    

- **To get the info about the installed or yet to install software or package**
```mardown
    brew cask info <software/app name>
```    

- **To navigate to home page of the software**
```mardown
    brew cask home <software/app name>
```    


So far home-brew installs the package which exists on the core home-brew repository. What if the package does not exist into the core home-brew repository. On that case we need to add/tap that repository into the home-brew core repository then install by using the same command mentioned above.

- **Tap the repository**
```mardown
    brew tap <repository name>
```    

If the user wants uninstall homebrew from the system

- **To uninstall the homebrew**
```mardown
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"
 ```   

### Note: 
_If we uninstall the brew then the package which we have installed through the brew will also get uninstalled except the software or application which is installed by using brew cask._
