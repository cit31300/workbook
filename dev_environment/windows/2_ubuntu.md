# Run and Configure Ubuntu Linux

Once your computer has restarted, you can find “Ubuntu” installed as an app in your Start menu. Launch Ubuntu and allow it to finish its installation.

(devenv:windows:ubuntu)=
## Create a Username & Password
You will be asked to create a username and password for the administrator of this operating system. These DO NOT need to be the same as the username/password for your Windows OS.

## Update Ubuntu
The first thing you should do is ask Ubuntu to install any updates. 

1. **From the Ubuntu command prompt**, type the following:

```
sudo apt update && sudo apt upgrade
```

2. You will be asked to input the password you just created.

*(This will probably take a while.)*

`````{admonition} Pro Tip!
:class: tip

*sudo* is Linux-speak for "super user do" – it basically means that this command should be run as an administrator (which is why you have to enter your password).

You're running two commands in one statement here: *apt* is a utility to manage Linux packages and you are asking it to both *update* and *upgrade* your installation. The "&&" symbol means to run two commands at once.
`````