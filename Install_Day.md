# Web Dev Install Day

In order to get started with our journey into web development, you will need to install a few things on your computer. This guide will walk you through the process of installing the necessary software we need and walk you through a short project to make sure everything is working.

## Install Visual Studio Code
Visual Studio Code is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux. It comes with built-in support for HTML, CSS, JavaScript, TypeScript and Node.js and has a rich ecosystem of extensions for other languages (such as C++, C#, Python, PHP, Go) and runtimes (such as .NET and Unity).

1. Go to the [Visual Studio Code website](https://code.visualstudio.com/).
2. Download the installer for your operating system.
3. Install Visual Studio Code.

## Install Node.js
Node.js is a JavaScript runtime meaning it allows you to run JavaScript on your computer. We use it to run development servers, build tools, and more.

1. Go to the [Node.js website](https://nodejs.org/).
2. Download the installer for your operating system.
3. Install Node.js.

## Install Git
Git is a version control system that allows you to track changes in your code and collaborate with others.

1. Go to the [Git website](https://git-scm.com/).
2. Download the installer for your operating system.
3. Install Git.

Note: On Windows, you will need to use Git Bash to run Git commands. On macOS and Linux, you can use the terminal. Git Bash is essentially a terminal for Windows that allows you to run Unix commands. Unix is an operating system that macOS and Linux are based on and Git was originally built for Unix.

## Optional: Install GitHub Desktop
GitHub Desktop is a graphical user interface for using Git. It allows you to manage your repositories on GitHub without having to use the command line. While it is not necessary, it can be helpful for beginners who are not yet comfortable with the command line. You can download it from the [GitHub Desktop website](https://desktop.github.com/).

Our class will be using Visual Studio Code and the terminal to write and run code, so you will need to be comfortable with using the terminal. Use GitHub Desktop if you need to, but you will need to be comfortable with the terminal by the end of the class.


## Optional: Install Chrome (Brave) or Firefox 
While you can use any web browser to view your web pages, I recommend using Chrome or Firefox for development. Chrome has a lot of great developer tools that make it easier to debug your code. You can download Chrome from the [Chrome website](https://www.google.com/chrome/). If you are concerned about privacy, you can use Brave, which is based on Chrome but has more privacy features. You can download Brave from the [Brave website](https://brave.com/). Firefox is available from the [Firefox website](https://www.mozilla.org/en-US/firefox/new/). 

Make sure that whichever browser you choose is set as your default browser. This will make it easier to open your web pages in development.


## Install Postman
Postman is a tool for testing APIs. We will use it to test our APIs in class. You can download it from the [Postman website](https://www.postman.com/).


## Install Live Server Extension for Visual Studio Code
Live Server is a Visual Studio Code extension that allows you to launch a development server with live reload capability. This means that when you make changes to your code, the server will automatically reload the page so you can see your changes without having to manually refresh the page.

1. Open Visual Studio Code.
2. Click on the Extensions icon in the Activity Bar on the side of the window.
3. Search for "Live Server" in the Extensions view. Look for the one by Ritwick Dey.  
4. Click the Install button for the "Live Server" extension.


## Test Your Installation

Now that you have everything installed, let's test it out. We will create a simple web page and run it using the Live Server. 

Web pages are made up of HTML, CSS, and JavaScript. We will create a simple web page with HTML and chat about each part of the code as we go.

1. Open Visual Studio Code.
2. Create and open a new folder for your project. You can do this by clicking on the File menu and selecting Open Folder and using the New Folder button to add a folder to your Desktop or a folder of your choice. Then save the folder as `web-dev`.
3. Create a new file called `index.html`. You can do this by clicking the New File button in the Explorer view and typing `index.html` in the file name box. 
4. Add the following code to the `index.html` file:

```html
<!DOCTYPE html>
<html>
</html>
```

4. Save the file.

What you just wrote is the basic structure of an HTML file. The `<!DOCTYPE html>` line tells the browser that this is an HTML5 document. The `<html>` tag is the root of the HTML document. HTML is written in tags, which are enclosed in angle brackets. Tags usually come in pairs, an opening tag and a closing tag. The closing tag has a forward slash before the tag name.

5. Right-click anywhere in the `index.html` file and select "Open with Live Server". This will open a new tab in your web browser with the `index.html` file.

If you see a blank page in your web browser, congratulations! That is exactly what we expected. We haven't added any content to the page yet. If you see an error, make sure you followed the instructions correctly and try again. If you still have trouble, ask for help.

Let's add some content to the page and ensure we can see it update in the browser.

6. Add the following code to the `index.html` file:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Web Page</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
  </body>
</html>

```

7. Save the file.

The `<head>` tag contains meta-information about the HTML document, such as its title. The `<title>` tag sets the title of the page, which is displayed in the browser's title bar or tab. Meta-information is information about the data on the page, such as keywords, author, and character set. We'll learn more about the `<head>` tag later in the class.


 The `<body>` tag contains the content of the HTML document. The `<h1>` tag is a heading tag. There are six levels of headings in HTML, from `<h1>` to `<h6>`. The `<h1>` tag is the most important and the `<h6>` tag is the least important. The `<h1>` tag is often used for the main heading of the page.

8. Go back to your web browser and refresh the page. You should see the text "Hello, World!" displayed on the page.

If you see the text "Hello, World!" displayed on the page, congratulations! You have successfully created and run your first web page. If you see an error, make sure you followed the instructions correctly and try again. If you still have trouble, ask for help.


## Save Your Work

As you work through the class, you will be creating and modifying a lot of files. In order to keep track of your changes and to be able to share your work with others, you will need to use Git.

1. Open the terminal in Visual Studio Code. You can do this by clicking on the Terminal menu and selecting New Terminal.
2. Check that you are in the `web-dev` folder by typing `pwd` and pressing Enter. You should see the returned path end with `web-dev`. If you are not in the `web-dev` folder, try re-opening the folder in Visual Studio Code.
3. Type `git init` and press Enter. This will initialize a new Git repository in the `web-dev` folder.
4. Type `git status` and press Enter. You should see a message that says "nothing to commit, working tree clean". This means that Git is tracking the files in the folder but there are no changes to commit.
5. Type `git add .` and press Enter. This will stage all the files in the folder for commit.
6. Type `git commit -m "Initial commit"` and press Enter. This will commit the staged files with the message "Initial commit".
7. Type `git status` and press Enter. You should see a message that says "nothing to commit, working tree clean". This means that Git is tracking the files in the folder and there are no changes to commit.

You have now saved your work to a Git repository. You can continue to work on your project and save your changes to the repository as you go. We will learn more about Git and how to use it and Github in class.


## Next Steps
Take the next few minutes before we start our lecture, to continue playing around with your HTML file and add new HTML elements. You can see a great list of elements you can add to your HTML file [here](https://www.w3schools.com/tags/default.asp).

