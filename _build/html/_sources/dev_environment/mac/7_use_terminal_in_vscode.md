# Use MacOS Terminal in Visual Studio Code

Now that you have VS Code installed, you can use its user interface to create and edit files as well as interact with the MacOS Terminal.

(devenv:mac:vscode_panel)=
## Open a Terminal in Visual Studio Code

You can split the VS Code view to show both the file editor as well as the MacOS Terminal. To do this, you will open the bottom panel in VS Code and show the Terminal.

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

3. You should now see MacOS command prompt in the Terminal within VS Code. Your terminal prompt will be unique to you, but may be as simple as `~ %`. This is where you can issue Linux commands to your MacOS Terminal.

(devenv:mac:root_directory)=
## Create a Root Directory for this Course

Create a root directory on your computer that you will use as your "home base" for all of the files you work with in this course.

```{note}
You will hear me refer to this specific directory as your "root directory" or "local root directory" throughout this course!
```

By default, your Terminal prompt is at the user's home directory in MacOS. You can create a new directory at this location or you can create a directory somewhere else on your computer.

You can create your root directory in one of two ways: through the Terminal, or through the Graphical User Interface.

(devenv:mac:root_directory:terminal)=
### Option 1: Create a Root Directory Using the Terminal

1. From the Terminal prompt in VS Code, type `ls`. This will show you all of the directories and files stored within your currently active directory.

  * You likely will see common MacOS directories such as `Desktop` and `Documents` here.

Think about the location on your computer where it makes the most sense for you to store your files. Say, for example, that you want to create your root directory *inside* your Documents directory. We'll use that as our example.

2. From the command prompt, navigate into the `Documents` directory with the following command: `cd Documents`

3. Then enter the command `mkdir cit31300` at the command prompt.

4. Move into the newly-created directory with the command `cd cit31300`

5. You should see that your command prompt has changed and now includes the current directory. Your prompt will look something like `Documents/cit31300 %`

(devenv:mac:root_directory:gui)=
### Option 2: Create a Root Directory Using the Graphical User Interface

Think about the location on your computer where it makes the most sense for you to store your files. Say, for example, that you want to create your root directory *inside* your Documents directory. We'll use that as our example.

1. Using Finder on your MacOS, open your `Documents` folder.

2. Create a new folder named `cit31300` inside your `Documents` folder.

3. **Right-click** on your newly-created `cit31300` folder and choose "New Terminal at Folder"

This will launch a MacOS Terminal window and set the current working directory to your `cit31300` directory.

To open this directory in VS Code, do the following:

4. Type `code .` (make sure you include the `.`) at the command prompt.

This will open VS Code and set the active workspace to your `cit31300` directory. It *should* have also opened the VS Code panel and set the current working directory to your `cit31300` directory.

(devenv:mac:test_file)=
## Create a Test File

Regardless of the method you chose above, you should be ready to write and store code in VS Code. Create a test file to show the connection between the Terminal and your file editor in VS Code.

1. Ensure you are in your `cit31300` root directory.

When you installed VS Code, it added a special command that you can use to create and open a new file with a single command.

2. At the command prompt, type `code test.txt`.

You should see a file open in the file editor at the top of the VS Code window.

```{note}
If you are asked to trust the authors of any files, you should respond positively.
```

3. Enter any text you like in the file in the editor and choose Save.

4. To see that the file is now saved in your local root directory, type the following at the command prompt: `ls`

5. You should see the file `test.txt` appear. As you add more directories and files, they will be displayed when you "list" (`ls`) your files.