# Mellow Project

This is a project in order to make a code revision app.

## Technologies used

1. Python 3.6 on Django
1. PostgreSQL
1. VS Code
1. GitKraken
1. Waffle.io

## Python Setup

### Linux Setup

Depending on your Linux version, either Python 2 or Python 3 will be installed.

To check if Python 3 is installed, please type `python3` on your terminal. If it's not, install it with:

```shell
$ sudo apt-get update
$ sudo apt-get install python3.6
```

Now, verify if pip is already installed with:

```shell
$ command -v pip3
```

If not, install it with:

```shell
pip install -U pip
```

Now, you'll have to install virtualenv and test your installation:

```shell
$ pip install virtualenv
$ virtualenv --version
```

To create a virtual environment for our project you'll run:

```shell
$ mkdir -p ~/Virtualenvs ~/Library/Application\ Support/pip
$ cd ~/Virtualenvs
$ virtualenv -p /usr/bin/python3.6 mellow_env
$ vim ~/Library/Application\ Support/pip/pip.conf
```

Inside the `pip.conf` file, type:

```shell
[install]
require-virtualenv = true

[uninstall]
require-virtualenv = true
```

Save and quit using `:wq`.

### Windows Setup

You can download Python 3.6 [here](https://www.python.org/downloads/).

Add the `C:\Python36\;C:\Python36\Scripts\` path to your system variables.

To install pip you can run:

```shell
$ python -m pip install -U pip
```

Now, you'll have to install virtualenv and test your installation:

```shell
$ pip install virtualenv
$ virtualenv --version
```

To create a virtual environment for our project you'll run:

```shell
$ mkdir -p C:\\Virtualenvs C:\\Users\\Your_User\\AppData\\Roaming\\pip
$ cd C:\\Virtualenvs
$ virtualenv mellow_env
```

Inside the folder `C:\\Users\\Your_User\\AppData\\Roaming\\pip` create a file named `pip.ini`.

Inside the `pip.ini` file, type:

```shell
[install]
require-virtualenv = true

[uninstall]
require-virtualenv = true
```

Save and quit.

## PostgreSQL Setup

We didn't setup Postgres yet.

## VS Code Setup

### Linux Setup

In Preferences > Settings, put at the end of your User Settings file the text:

```json
"python.venvPath": "~/Virtualenvs",
"python.pythonPath": "~/Virtualenvs/mellow_env/bin/python3",
"python.linting.pylintPath": "~/Virtualenvs/mellow_env/bin/pylint",
```

Also, do this on your Workspace Settings file too.

### Windows Setup

In Preferences > Settings, put at the end of your User Settings file the text:

```json
"python.venvPath": "C:\\Virtualenvs",
 "python.pythonPath": "C:\\Virtualenvs\\mellow_env\\Scripts\\python.exe",
 "python.linting.pylintPath": "C:\\Virtualenvs\\mellow_env\Scripts\\pylint.exe",
```

Also, do this on your Workspace Settings file too.

## GitKraken

You can download GitKraken [here](https://www.gitkraken.com/).

You should fork this repo and clone it to your machine.

## Waffle.io

Go to [Waffle.io](https://waffle.io/) and sign up with your GitHub account. Fortunately the project Scrum Board should load automatically.

## Django Setup

With the repository cloned, you should see a `requirements.txt` file on the main folder.

### Linux

Activate your virtual environment and run the `requirements.txt` file inside your virtual env with:

```shell
$ source ~/Virtualenvs/mellow_env/bin/activate
$ cd your_project_folder #cd to your project folder
$ pip install -r requirements.txt
```

### Windows

Activate your virtual environment and run the `requirements.txt` file inside your virtual env with:

```shell
$ cd C:\\Virtualenvs\\mellow_env\\Scripts
$ activate
$ cd your_project_folder #cd to your project folder
$ pip install -r requirements.txt
```

***

Now, the project will be cloned to your machine and the virtualenv will be activated with all requirements already installed. On the main folder for ___\<mellow/\>___, you'll have a `manage.py` file. Every time you need to run the server, it has to be executed from that folder.

To run it, type:

```shell
$ python manage.py runserver
```

The server will be initialized in [`http://localhost:8000`](http://localhost:8000)

## General Guidelines

* Note that pushes will be made/merged only to the `develop` branch.

* Every card (feature) will have a branch, that when finished, will be merged to the `develop` branch.

* When the `develop` branch is fully working, it will be merged into `master`.