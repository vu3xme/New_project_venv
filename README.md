# New_project_venv

Tutorials > How to create a Python virtual environment on Ubuntu 20.04
Search for a tutorial
Search
How to create a Python virtual environment on Ubuntu 20.04Published on: 05 March 2021 Development Django Python
Contents
How to create a Python virtual environment on Ubuntu 20.04
Introduction
Installing and configuring Python
Configuring a Python virtual environment
Creating a simple Python application
Conclusions
Introduction
Python is a high-level, object-oriented programming language that is very popular due to its ease of understanding and learning.

In this tutorial you will learn how to install or update the version of Python on your Ubuntu operating system and how to build a Python programming environment and test it with a sample application. The commands shown in this guide have been tested on Ubuntu 20.04, but can also work on different Debian distributions.

First, connect to your server via an SSH connection. If you haven't done so yet, following our guide is recommended to  connect securely with the SSH protocol. In case of a local server, go to the next step and open your server terminal.

Installing and configuring Python
The installation of the Python package has to be performed mainly through the terminal of the operating system.

Once inside, start giving the first commands to check if Python versions 2 and 3 are up to date. Ubuntu usually comes with both versions.

$ sudo apt-get update
$ sudo apt-get -y upgrade
By running these two commands, the packages installed on your system can be checked and, if everything is correctly updated to the latest version,a response flag in the form -y is returned.

Another direct can be performed on Python 3 version. To do so, use the command:

$ python3 -V
As output, the version of Python in use on your OS will be shown.

Please note that an important package manager, very useful for managing and updating programming packages for your projects is pip,.

So, if you want, install pip :

$ sudo apt-get install -y python3-pip
Once pip is installed, depending on your needs as a developer, any useful Python package can now be installed.

To do so, just enter the following command, replacing the package_name with the name of the one you wish to install:

$ pip3 install package_name
Finally, it is important to install a series of packages to make your programming environment more consistent. To do so, use the command:

$ sudo apt-get install build-essential libssl-dev libffi-dev python-dev
Configuring a Python virtual environment
In case of working with multiple projects, it is important to manage multiple virtual environments. Virtual environments (virtualenv) create isolated and self-consistent spaces on your system, dedicated to specific projects, in this case, of Python.

The differentiation of virtual spaces has the advantage of isolation: no environment interacts with another, each works as an independent unit and its destruction does not damage other projects.

To create these environments, install a module called venv, which is present in the Python library. Then, proceed  with the installation of  venv with the following command:

$ sudo apt-get install -y python3-venv
Now it’s time to create new virtual environments for your projects. To start, use the mkdir command to build a new directory to populate with your environments. Then, move into it with the cd command ,  as in the following example:

$ mkdir directory_env
$ cd directory_env
Once in the directory where to create the new environments, create the first one using the venv module . To do so, follow the command:

$ python -m venv 
environment1
N.B. Obviously, for both the directory and the environments to be created any name can be chosen.

Within the new directory, an additional directory will be created containing some objects, which can be viewed with the ls command .

$ ls 
environment1
Environment folder view
These objects will be able to make your environment work properly, isolating it from other folders on the machine and improving some efficiency features of the development and execution processes, such as compilation.

To make use of a new environment, activate it now by calling its activation script with the command:

$ source 
environment1
/bin/activate
Inside your terminal, the name of the environment you are in can now be viewed, as shown in the figure.

Environment name

The prefix you will read will provide the information about the activated environment (in the example:  environment1 ).

Creating a simple Python application
Now that you've set up your virtual environment, it's time to create your first Python application to test how it works.

As per tradition, the first program you will be explained how to build is the classic " Hello World!"

Start by building a new file named hello.py via a text editor, such as nano :

(
environment1
) driel@ARU-UBU20:~/directory_env$ nano hello.py
At this point, the file will open in the terminal and it can be typed in your program's instruction.

print("Hello, World!")
Now, use the combination CTRL + X and press y to confirm saving the file.

After exiting the file editing and returning to the shell, get your program running, through the command:

(
environment1
) driel@ARU-UBU20:~/directory_env$ python hello.py
The hello.py program just created will cause your terminal to print the message indicated in your print statement, as in the following example:

Script output
Finally, to exit the virtual environment, enter the deactivate command in the terminal .

Conclusions
At this point, you will have updated Python, set up a working environment and created a first simple application to test its correct functioning.

To learn how to build more complex applications with Python, consult the official manuals of the Python programming language to deepen the study and exploit it to its full potential.







