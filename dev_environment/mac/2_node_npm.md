# Install nvm, Node.js, and npm

Node.js has many different versions available and developers working on multiple projects often need to change which version they are using so that they are working in the same environment as the application they've built. It's possible to install multiple versions of Node.js on a single machine, but it can be confusing to manage the different versions.

You will use `nvm` (the Node Version Manager) to install the `Node.js` JavaScript runtime and `npm` (the Node Package Manager).

`````{admonition} Pro Tip!
:class: tip

`nvm` helps you manage which version(s) of the Node.js runtime you have installed on your OS.

`npm` manages the additional packages that you will install to support your application development.

The names are similar but they provide very different functionality, so really think about what the acronyms mean!
`````

(devenv:mac:install_nvm)=
## Install nvm

There are several different versions of Node.js, so they have developed software to help you obtain and switch between versions (which is helpful if you are working on multiple projects). That software is called `nvm` (Node.js Version Manager). 

1. Install `nvm`

*(Copy and paste this ENTIRE line - it is word-wrapping in the documentation, but it is a single command.)*

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash
```

```{important}
You must restart your **MacOS shell** (not your entire computer) after installing `nvm`! 
```

2. To restart the shell, enter the following at the MacOS Terminal window:

```
source ~/.zshrc
```

```{note}
On some systems the file that holds your shell configuration is named `.zprofile` instead of `.zshrc`.

If the command above did not work, try `source ~/.zprofile`
```

(You can also just quit and restart the Terminal.)

(devenv:mac:verify_nvm_installation)=
## Verify nvm Installation

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