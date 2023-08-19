# Install nvm, Node.js, and npm

Node.js has many different versions available and developers working on multiple projects often need to change which version they are using so that they are working in the same environment as the application they've built. It's possible to install multiple versions of Node.js on a single machine, but it can be confusing to manage the different versions.

You will use `nvm` (the Node Version Manager) to install the `Node.js` JavaScript runtime and `npm` (the Node Package Manager).

`````{admonition} Pro Tip!
:class: tip

`nvm` helps you manage which version(s) of the Node.js runtime you have installed on your OS.

`npm` manages the additional packages that you will install to support your application development.

The names are similar but they provide very different functionality, so really think about what the acronyms mean!
`````

(devenv:mac:uninstall_outdated)=
## Uninstall Outdated Files
Node.js is sometimes automatically included with the Linux distribution in MacOS. Unfortunately, the version that is installed is outdated. Therefore, the first thing we have to do is uninstall the old version.

This is done in two steps: `purge`, which uninstalls Node.js, and `auto-remove` which removes any leftover files that no other software needs (now that Node.js has been uninstalled).

1. Run the following command in a MacOS Terminal window:

```
sudo apt-get purge --auto-remove nodejs
```

(devenv:mac:install_support)=
## Install Support Software
To install software from the internet, MacOS needs to be able to resolve web addresses (URLs). It can do that with a tool called `cURL`. 

1. Install `cURL` by typing this into the MacOS Terminal window:

```
sudo apt-get install curl
```

There are several different versions of Node.js, so they have developed software to help you obtain and switch between versions (which is helpful if you are working on multiple projects). That software is called `nvm` (Node.js Version Manager). 

2. Install `nvm`

*(Copy and paste this ENTIRE line - it is word-wrapping in the documentation, but it is a single command.)*

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash
```

```{important}
You must restart your **MacOS shell** (not your entire computer) after installing `nvm`! 
```

3. To restart the shell, enter the following at the MacOS Terminal window:

```
source ~/.zshrc
```

(You can also just quit and restart the Terminal.)

(devenv:mac:verify_installation)=
## Verify Installation

1. After restarting your MacOS shell, ensure that `nvm` was installed by entering the command:

```
nvm -v
```

This should return the message *"0.39.4"* or a higher number.

(devenv:mac:install_node)=
## Install Node.js

You will now use `nvm` to install the current stable LTS ("long term support") release of Node.js. 

1. Install Node.js with the following command:

```
nvm install --lts
```

(devenv:mac:verify_node)=
## Verify Node.js Version

Verify the version of Node.js that was installed. 

1. Run the following command:

```
node --version
```

You should receive a message that "v18.17.1" (or a higher number) is installed.