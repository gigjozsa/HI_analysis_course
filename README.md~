# Template notebook

An ipython notebook-based book to teach or record studies in the scope of radio astronomy. These notebooks are thought to be a community effort with the aim to be constantly improving and adding to the content in an effort to make the topics as accessible as possible.  Please contribute, whether it is content, editing, or even suggestions.

The first book of this kind has been used to teach the NASSP 2016 [Fundamentals of Radio Interferometry](https://griffinfoster.github.io/fundamentals_of_interferometry/) Masters' Course. Most structural material is copied from that course.

## Data Files

Additional large files (> 1MB), mainly FITS images, which are needed for some of the sections, should be made available from a seperate place and be put into the data directories of each section. One possible way is to define a tarball that will extract the data files into the single directories.

```
cd template/chapter_01_somename/01_data
tar xvzf somename_fits.tar.gz
cd template/chapter_02_somename/02_data
tar xvzf somename_ms.tar.gz
```

## Style Guide

In order to keep the content consistent across sections we have written a style guide in the introduction. Additionally, we have an editing guide for those who wish to suggest changes and edits to the current content. See the preface of the ipython notebook.

## Setup contributor virtualenv

If you would like to contribute to notebooks it is useful to setup a python virtual environment to ensure your environment is consistent with other contributors. This section provides a guide for how to do this in an Ubuntu system (tested on 14.04), other systems should work with slight modifications.

Currently we are using pip to install packages, the most important package versions are:

* pip 7.1.2
* python 2.7.6
* numpy 1.10.1
* matplotlib 1.5.0
* scipy 0.16.1
* ipython 4.2.0
* astropy 1.1.1
* aplpy 1.0
* ipywidgets 4.1.1

This guide was developed from these references:

* <http://jeffskinnerbox.me/posts/2013/Oct/06/ipython-notebook-in-virtualenv/>
* <http://iamzed.com/2009/05/07/a-primer-on-virtualenv/>
* <http://jonathanchu.is/posts/virtualenv-and-pip-basics/>
* <https://warpedtimes.wordpress.com/2012/09/23/a-tutorial-on-virtualenv-to-isolate-python-installations/>

Before setting up a virtual environment there are a few system level libraries which need to be installed

```
sudo apt-get install libpng-dev libncurses5-dev
```

To setup a clean environment to run our ipython-notebook standard system, start by making sure virtualenv is installed on your system. Run:

```
$ which pip
```

If there is no output, then you need to install pip:

```
$ sudo easy_install pip
```

Next, run:

```
$ which virtualenv
```

If there is no output, then you need to install virtualenv:

```
$ sudo apt-get install python-virtualenv
$ sudo pip install virtualenvwrapper
```

Once you have all the basic packages installed you can create a vitrualenv, I tend to keep all my virtualenvs in one place, e.g. a .virtualenv directory in my home directory

```
$ [mkdir .virtualenv]
$ cd .virtualenv
$ virtualenv --no-site-packages nameofbook [replace nameofbook by the name of the book]
```

This creates a virtualenv called nameofbook in the .virtualenv directory which is completely independent of any system site-packages, to active the virtualenv run the activation script

```
$ cd nameofbook
$ source bin/activate
```

First, lets clone the repository from github, you should use your own forked version if you want to make changes

```
$ git clone https://github.com/[username]/template.git
```

If you just want to run the notebooks interactively you can just use this repository.

```
$ git clone https://github.com/gigjozsa/template.git
```

Now this is a completely clean environment, there are no python packages installed, we need to set those up. There are two ways to do this, first is by running the following pip install commands, the other is by installing from the requirements file included in the this repository. I recommend the requirements file as it contains current version information (but, this may fail due to the package ordering, then you will need to try the to install packages manually, described below). The file is in the main directory of the repository. This will take a bit of time to setup, I recommend a tea break.

```
$ pip install --upgrade pip
$ pip install -r [path to file]/requirements.txt
```

or

```
$ pip install --upgrade pip
$ pip install yolk
$ pip install numpy
$ pip install matplotlib
$ pip install scipy
$ pip install ipython[all]
$ pip install --no-deps astropy
$ pip install aplpy
$ pip install ipywidgets
```

We are now ready to start the ipython notebook server:

```
$ cd template
$ jupyter notebook
```

To kill the server, type ctrl-c at the terminal and input y. To deactivate the virtualenv and return to your normal environment run:

```
$ deactivate
```

In the future, when you wish to return to the virtualenv, change to the fundamentals directory and run:

```
$ source bin/activate
```

### Ubuntu 12.04 Issues

The system setuptools/distribute (0.6.24) is not new enough and needs to be updated with easy_install

```
easy_install -U distribute
```

### Ubuntu 14.04 Issues

Matplotlib and numpy have many system-level dependencies, you may be required to install package before the virtualenv setup will work.

#### freetype

If there is a freetype related error, try:

```
sudo apt-get install libfreetype6-dev
```

#### fortran

If there is a fortran related error, try:

```
sudo apt-get install gfortran
```

### Contributors

* Griffin Foster ([@gigjozsa](https://github.com/griffinfoster))
* Trienko Grobler
* Gyula (Josh) Jozsa ([@gigjozsa](https://github.com/gigjozsa))
* Oleg Smirnov ([@o-smirnov](https://github.com/o-smirnov))
* et al.