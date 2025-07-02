# **Install MkDocs**
 
-----

This page will show you how to get MkDocs set up and ready to use on your computer. 

## **Requirements**

To use MkDocs, you need two things:

  * **Python 3.x:** A programming language that MkDocs uses.
  * **pip:** A tool that helps install Python programs. It usually comes with Python.

## **Check if Python is Installed**

Open your computer's Terminal on Mac/Linux or Command Prompt on Windows.

Type this:

```bash
python3 --version
```

If you see a version number like `Python 3.9.x`, you're good.
 
You'll need to install Python otherwise. You can download and install python from the official [Python website](https://www.python.org/downloads/).

## **Install MkDocs**

Once Python is ready, use `pip` to install MkDocs. In your Terminal/Command Prompt, type:

```bash
pip install mkdocs
``` 

Confirm it has installed and works by checking the version with:   

```bash
mkdocs --version
```
This should show you the MkDocs version number.

## **Initialize a New MkDocs Project**

To create your first docs site, type this (you can change `My-New-Doc` to any name you like):
    
```bash
mkdocs new My-New-Doc
```

This command creates a new folder called `My-New-Doc`. 

Inside, you'll find a basic setup with a file named `mkdocs.yml` which is used for settings and a `docs` folder where your pages are created.


## **Preview Your Site Locally**

Navigate into your new project folder in your terminal:

```bash
cd my-new-docs
```

You can also open this project folder in your VS Code or preffered IDE by:

```bash
code .
```

Then, start the preview server:

```bash
mkdocs serve
```

You can then follow the link, `http://127.0.0.1:8000` to your web browser and you should see a simple webpage.

This server updates automatically as you make changes.

## **Recap**

You've just:

  * Checked for python.
  * Installed MkDocs.
  * Created a new docs project.
  * Seen your site running in your browser