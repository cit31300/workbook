# Use Ubuntu with Visual Studio Code

Now that you have VS Code connected to your Ubuntu instance, you can use its user interface to create and edit files as well as interact with the Ubuntu command line.

```{important}
Make sure VS Code is connected to Ubuntu before performing these steps!
```

(devenv:windows:vscode_panel)=
## Open a Terminal in Visual Studio Code

You can split the VS Code view to show both the file editor as well as the Ubuntu command line. To do this, you will open the bottom panel in VS Code and show the Terminal.

1. From the top right of the menu bar in VS Code, choose the `Toggle Panel` icon:

    ```{image} ../img/vscode_toggle_panel.png
    :alt: Visual Studio Code's toggle panel icon
    :align: center
    :width: 150px
    ```

  * Alternatively, you can press `Ctrl+J`

2. If it is not already selected, choose the "Terminal" tab at the top of the VS Code panel.

    ```{image} ../img/vscode_terminal.png
    :alt: Visual Studio Code's tab bar in the panel with the Terminal (4th tab) highlighted
    :align: center
    :width: 300px
    ```

You should now see an Ubuntu command prompt in the Terminal within VS Code. Your terminal prompt will be unique to you, but should end with a `$ `. This is where you can issue Linux commands to your Ubuntu instance.

(devenv:windows:root_directory)=
## Create a Root Directory for this Course

Create a root directory on your Ubuntu instance that you will use as your "home base" for all of the files you work with in this course.

By default, your Terminal prompt is at the user's home directory in Ubuntu. You can create a new directory at this location.

1. Type the Linux command `mkdir cit31300` at the command prompt in the VS Code Terminal.

2. Move into the directory with the command `cd cit31300`

You should see that your command prompt has changed and now includes the current directory. Your prompt will look something like `~/cit31300$ `

```{note}
You will hear me refer to this specific directory as your "root directory" or "local root directory" throughout this course!
```

(devenv:windows:test_file)=
## Create a Test File

Create a test file to show the connection between the Terminal and your file editor in VS Code.

1. Ensure you are in your `cit31300` root directory (your command prompt should end with `cit31300$ `)

When you installed VS Code, it added a special command that you can use to create and open a new file with a single command.

2. At the command prompt, type `code test.txt`.

You should see a file open in the file editor at the top of the VS Code window.

```{note}
If you are asked to trust the authors of any files, you should respond positively.
```

3. Enter any text you like in this file and choose Save.

4. To see that the file is now saved in your local root directory, type the following at the command prompt: `ls`

5. You should see the file `test.txt` appear. As you add more directories and files, they will be displayed when you "list" (`ls`) your files.