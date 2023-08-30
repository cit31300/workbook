# Install Git on Both Windows and Ubuntu

Git is source control management software that allows you to manage, back up, and collaborate while you are doing development work. 

`````{admonition} Pro Tip!
:class: tip

Remember! Your Ubuntu instance is essentially a virtual machine that is separate from your Windows OS. For optimal performance, you should install Git on BOTH your Windows AND your Ubuntu operating systems.
`````

(devenv:windows:install_git_windows)=
## Install Git on Windows

You will install or update your version of Git for Windows. It's important to have the latest version so that you can share credentials between the Windows and Ubuntu operating systems.

1. [Download the latest version of Git for Windows here](https://gitforwindows.org/) and follow all of the instructions in the installer.

2. You may accept the default value for all of the options.

3. **Ensure you select the Git Credential Manager option during the installation** (This will be important later.)

(devenv:windows:install_git_ubuntu)=
## Install Git on Ubuntu

Git should be installed automatically with Ubuntu, but it's best to ensure it's completely up to date.

```{important}
Make sure you are running the following commands in your Ubuntu command prompt!
```

1. Open (or return to) the Ubuntu command prompt window.

2. To obtain the latest stable version of Git, enter the following command into your **Ubuntu command prompt**:

```
sudo apt-get install git
```

(devenv:windows:configure_git_ubuntu)=
## Configure Git on Ubuntu

Configure Git so it can automatically add your user details to the commits you will make to your repositories. 

1. Input the following commands on the Ubuntu command line, replacing the information as needed with your personal details.

```
git config --global user.name "Your Name"
```

You will *not* see any kind of feedback from the command prompt after you issue this command.

2. Use your school email address here (@iupui.edu or @iu.edu):

```
git config --global user.email "youremail@iu.edu"
```

Again, the command prompt will be empty after this command.

(devenv:windows:configure_git_gcm)=
## Configure Git Credential Manager

Now you will instruct your Ubuntu distribution to share your Git credentials with the Git installation on Windows. This will help you share logins between your two operating systems without the need to configure them individually.

1. Input the following command on the Ubuntu command line:

```
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager.exe"
```

```{note}
The location of git-credential-manager.exe may be different in your installation of Git for Windows. if the above command doesn't work, you must find the correct path for `git-credential-manager.exe` on your computer.
```