Guide to install Python related software for the course.
# TKT4196
jorgemendozaesp (jorge.m.espinosa@ntnu.no)
NTNU - PhD student

## Python
Make sure you have python 3.7 installed. To verify that, type the following command on your terminal:
```
$ python -V
```
If you need to install Python 3.7 in your computer, here is a guide:
+ [For MacOS](https://opensource.com/article/19/5/python-3-default-mac)

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
To update Spyder:
```
$ conda update spyder
```

### Python packages
- Generate requirements file:
```
$ pip freeze > requirements.txt  
```
- Create a conda environment with course requirements
```
$ conda create --name tktpy python=3.7
$ pip install -r tktreq.txt 
```

## Jupyter
Jupyter notebooks are created for pedagogic purpose. To use widgets in Jupyter-lab follow these instructions:
* Install jupyter-lab (assuming that conda is installed): 
```
$ conda install jupyter
$ conda install jupyterlab
$ conda install nodejs
$ pip install ipywidgets
$ jupyter nbextension enable --py widgetsnbextension
$ jupyter labextension install @jupyter-widgets/jupyterlab-manager
$ jupyter labextension install @jupyterlab/git
$ pip install jupyterlab-git
$ jupyter serverextension enable --py jupyterlab_git
```