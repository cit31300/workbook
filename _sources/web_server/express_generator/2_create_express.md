# Create Express Application
Create a web application using the Express Generator app.

1. In the Terminal, navigate to your **local root folder** for this course.
  * *Do not create a top-level folder for this project! One will be created by the generator!*

2. At the command prompt, enter the following command to create the app scaffold. This will create a directory named `hello-express-generator` and will add all of the files to that directory.

```
express --view=ejs hello-express-generator
```

3. Move into the application's directory

```
cd hello-express-generator
```

4. Install all the packages required by your application with a single command:

```
npm install
```
This will install all packages listed in the `package.json` file (and the packages those are dependent upon as well).

5. Ensure you have the most recent version of all installed packages with one more command:

```
npm audit fix --force
```