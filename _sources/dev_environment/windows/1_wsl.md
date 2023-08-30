# Install Windows Subsystem for Linux

Linux is the most common operating system for hosting and delivering web applications. You can develop your applications using any operating system, but it's best to use Linux for previews and testing. 

This will also let the entire class work with the same set of instructions regardless of what type of computer they have.

Windows has a new(ish) mechanism for running Linux side-by-side with your Windows OS, and allows you work with Linux without having to build a separate virtual machine. This is called the **Windows Subsystem for Linux (WSL)**.

(devenv:windows:wsl)=
## Install WSL
You will install WSL on your Windows computer.

```{important}
You MUST have adminstrator rights on your computer to follow these instructions!
```
1. Open a Command Prompt *as an adminstrator* on your computer
2. Use the following command to install WSL:

```
wsl --install
```

This command will enable your computer to run WSL and install the **Ubuntu** distribution of Linux. Ubuntu is used by default, and is the correct Linux flavor for use in this course.

If the above command *does not* start the WSL installation, you can use a more specific command to ensure you correctly install the subsystem and Linux distribution. 

3. ONLY do this if the prior command did not work:

```
wsl --install -d Ubuntu
```

You should receive a message that WSL was installed.

```{important}
Restart your computer after installing WSL!
```