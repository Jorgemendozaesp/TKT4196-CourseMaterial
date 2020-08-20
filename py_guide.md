# Getting started with Python

## Guide to install Python related software for the course.

If you find mistakes/typos or links that do no longer function, please contact: 

Jorge Mendoza (jorge.m.espinosa@ntnu.no)  
NTNU - PhD student

### Install Python 3.7

First, make sure that you have python 3.7 installed. To verify that, type the following command on a terminal:
```
$ python -V
```
If you need to install Python 3.7 in your computer, here are some guides:
+ [NTNU guide](https://innsida.ntnu.no/wiki/-/wiki/English/Installing+Python#section-Installing+Python-Install+the+latest+version+of+Python)(for Windows, MacOS, and LINUX)
+ [For MacOS](https://opensource.com/article/19/5/python-3-default-mac) (in case you find it better/easier than the NTNU guide)

### Install Anaconda

#### MacOS

Make sure you are working on a zsh terminal. Type the following command:
```
$ chsh -s /bin/zsh
```
And restart your terminal. It should say -- ~ -- -zsh on top. 

Now install Anaconda.  You may follow [these instructions](https://towardsdatascience.com/how-to-successfully-install-anaconda-on-a-mac-and-actually-get-it-to-work-53ce18025f97)

Then run this command: 
```
$ conda init zsh
```

To check installed Spyder version:
```
$ conda list Spyder$
```
If Spyder is not installed:
```
$ conda install -y spyder
```
To update Spyder:
```
$ conda update spyder
```

### Python packages

Create a conda environment called, e.g. tktpy: 
```
$ conda create --name tktpy python=3.7
```

Once the process is finished, check that it has been successfully created:
```
$ conda info --envs
```

It should show at least an environment called base (with a * next to it) and another called tktpy. The * means that the current environment is base. We need to activate the environment we want to work at. For that, type the following:
```
$ conda activate tktpy
```

Next, you need to install the course requirements. These are the python packages that we will use during the course. They are stored in a file called 'tktreq.txt'. To download the file, type:
```
curl -OL https://raw.githubusercontent.com/Jorgemendozaesp/TKT4196-CourseMaterial/master/tktreq.txt
```

To install them, type the following command:
```
$ pip install -r tktreq.txt 
```

### Jupyter

Jupyter notebooks are created for pedagogic purpose. To use widgets in Jupyter-lab follow these instructions:
* Install jupyter-lab (assuming that conda is installed): 
```
$ conda install -y jupyter jupyterlab nodejs
$ pip install ipywidgets
$ jupyter nbextension enable --py widgetsnbextension
$ jupyter labextension install @jupyter-widgets/jupyterlab-manager
```
