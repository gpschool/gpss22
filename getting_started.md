---
layout: page
title: Getting Started
weight: 3
---


## Introduction 

The Gaussian Process Summer School will include some hands-on tutorials in which we will build some simple Gaussian process models. The tutorials will be in Python, featuring the open source GPy package that has been developed by the Machine Learning group at the University of Sheffield.

We'll hold the labs in the same room as the talks and lunch.

Prior Python programming skills are not required, however you should ensure that you have installed the appropriate version of Python and the packages/libraries we will be using:

- **Python 3.6+**
- `numpy`
- `scipy`
- `matplotlib`
- `GPy`
- `jupyter`

Additional requirements include
- `climin`
- `GPyOpt`
- `pyDeepGP`

All labs are in a format called "_notebooks_", which can be run using [Jupyter](http://jupyter.org/index.html). These are worksheets that can execute Python code in blocks in your web browser.

## Running Labs in Binder

This year, we are hosting the labs on Binder, a cloud-based environment that you can use to run labs in. You can run the labs in Binder from your browser, without the need to setup a python environment locally on your machine.

To access the labs on Binder, follow the appropriate links on the [Labs](./labs) page. Note that due to high numbers of participants and limits on concurrent users in Binder, you may have to use one of the mirror lab, if you are unable to load a lab. You can also run them locally on your computer if you have installed GPy.

It is really important to **remember to download your notebooks if you would like to save them, as changes made will not be saved across different sessions.**

## Running Labs on your Local Machine

You may wish to run the labs on your local machine. You can do this by setting up a Python environment using the following instructions. We highly recommend that you install an integrated Python environment, in particular [Anaconda](https://store.continuum.io/cshop/anaconda) which will allow for easy installation of packages. It also comes with the latest versions of `numpy` and `scipy`.

The following instructions will tell you how to install and setup the Python library for the tutorials, and some information on installing and running Jupyter.

To use the notebooks locally, you should download the respective lab sheet. In a terminal window, navigate to the file's path (using the `cd` command) and run the command `jupyter notebook`. This will open a browser window connecting to the (locally hosted) notebook server. The notebook should be visible in the file list.

Typically, Jupyter will launch the server at [http://localhost:8888/tree](http://localhost:8888/tree), and you can navigate to it this way, should you accidentally close the window.

## Installing Python with Anaconda

Anaconda is a distribution of the Python prorgamming language that comes integrated with a number of precompiled libraries, and its own package and environment manager, called `conda`. It freely allows use of installation of packages and libraries via `conda` or `pip`. We recommend using Anaconda to manage your Python language environment, _particularly if you are new to Python_, and the following instructions will assume you are using Anaconda. If you are using a different Python distribution, you may have to tailor to following instructions, but you should ensure that you are using Python 3.6+.

### Installing
The easiest way to get a working Python environment is to install Anaconda. It is fairly straightforward to install, but can take some time so you must make sure this is done before the lab.

1. Download and install the free version of Anaconda from its webpage: [https://www.anaconda.com/download](https://www.anaconda.com/download), selecting the *Python 3.9 version* (the latest at the time of writing) appropriate for your operating system
  - Windows: the installer will be a `.exe` executable, and you can follow the setup as instructed
  - macOS: the installer is a `.pkg` software package, and you can follow the setup as instructed
  - Linux: the installer is a `.sh` shell script, and you can run it in the terminal and follow the setup as instructed
    - Note you may have to enable execution of the file, by either
      - Right click the file and select Properties, and under `Permissions` check "Allow executing file as program"
      - `$ chmod +x /path/to/installationfile.sh`
1. Update Anaconda, `numpy`, `scipy`, and `matplotlib`: open a command prompt or terminal and execute the following commands
  1. `conda update -y anaconda`
  1. `conda update -y numpy scipy matplotlib`
1. Update `jupyter`
  1. `conda update -y jupyter`
  - If you are not using Anaconda, you can install `jupyter` by calling `$ python3 -m pip install juypter`

## Installing with Libraries with `pip`
If you have manually created your Conda environment, or would simply like to install these libraries in your base `python` environment, follow these instructions.
  
### GPy
We will install `GPy` using `pip`, by performing the following command in the terminal/command prompt:

```
$ pip install GPy
```

Installing `GPy` will also install its other dependencies, such as `paramz`, so you don't need to worry about these. You can test that the installation of `GPy` is working by running the following in a Python shell:
```
>>> import GPy
```
If you want to check your installation, you need to `$ pip install nose` and run `>>> GPy.tests()` in the Python shell. This will run through the testing sequence.

### GPyOpt

```
$ pip install gpyopt
```
Some of the options of GPyOpt depend on other external packages: `DIRECT`, `cma`, and `pyDOE`. Please be sure that these are installed if you want to use all the options. With everything installed, you are ready to start.

### pyDeepGP

This is the library used for creating deep Gaussian Processes with GPy.

```
$ pip install git+https://github.com/SheffieldML/pyDeepGP
```

### climin
This is the library used for stochastic optimisation, and is required for the final section of Lab 2.

```
$ pip install git+https://github.com/BRML/climin
```

**Do not install `climin` from PyPI -- ensure you use the GitHub version as instructed**
