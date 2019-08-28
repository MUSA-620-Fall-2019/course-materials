# Getting started with Anaconda

The first step with Anaconda is to set up the Python environment we will use in this class and install the Python packages we will need.

To do this, you will need to execute commands via the command line. The exact process will depend on your operating system.

## Windows

The `Anaconda Prompt` program is a command line utility for executing commands related to Anaconda. This is the recommended approach for managing and updating Python packages with Anaconda on Windows.

Note that windows users can also use the command-line emulator [cmder](http://cmder.net/). However, this is more advanced and requires setting the `PATH` environment properly so that cmder is aware of the installation location of `Anaconda`.

## MacOS

Mac users can use the built-in command-line app `Terminal`. Terminal replacements such as [iTerm](https://www.iterm2.com/) can also be used to execute commands.

#### Note

Anaconda also installs a program called `Anaconda Navigator` which provides a graphical interface for managing environments and installing packages. Unfortunately, it doesn't provide all of the functionality that we will need to use when installing packages.

However, it can still be used to launch Jupyter notebooks (see below).

# The `conda` command

Managing environments and installing packages will be done by executing the `conda` command in the command line. Below are some of the most common commands that we will use in this class.

**Important:** All of the examples below should be run in the `Terminal` app (MacOS) or `Anaconda Prompt` (Windows).

For further information on the `conda` command, see
the [conda user guide](https://conda.io/projects/conda/en/latest/user-guide/).

## Making sure you are running the latest conda version

The first thing you should do is make sure you are running the latest `conda` version: From the command line, run

```
conda update -n base -c defaults conda
```

## Listing the available environments

The default environment when first installing Anaconda is called `'base'`. You can list the currently installed Python environments using the following command:

```
conda env list
```

The currently active environment will have a `'*'` next to it. You should see the `'base'` environment as well as other environments you have created.

## Creating your initial environment

Throughout this course, we will install and update packages using an `environment.yml` file. To create the environment for this course, first download the [`environment.yml`](../environment.yml)
from this repository to your computer.

Using the full filename of the environment file on your computer, you can create a new environment by running:

```
conda env create --file /path/to/environment.yml --name musa-620
```

## Activating your environment

To activate the environment for this course, you can run:

```
conda activate musa-620
```

Now all of the packages in this environment will be available when we run Python.

## Activating the `'base'` environment

To activate the `'base'` default environment, simply run:

```
conda deactivate
```

Note that you should also use the `musa-620` environment (or whatever you named it) to do the analysis in this course. The `'base'` environment contains many more packages than we will need in this class, and those packages can potentially cause dependency conflicts and issues.

## Deleting an environment

Note that you cannot create a new environment with the same name as an existing environment. If your environment becomes corrupted or you run into issues, it is often easiest to delete the environment and start over. To do, you can run the following commands:

```
conda deactivate
```

```
conda env remove --name musa-620
```

## Updating an existing environment

The GitHub repository for each week's lecture will include an `environment.yml` specifying the packages needed for that week. You can update your local environment by downloading the environment file and then running:

```
conda deactivate
```

```
conda env update --name musa-620 --file /path/to/weekly/environment.yml
```

```
conda activate musa-620
```

## Installing specific packages

The weekly environment files will have all of the necessary packages listed, but for reference, you can also install specific packages into your environment using:

```
conda activate musa-620
```

```
conda install package_name
```

# Launching a Jupyter notebook

We will use the [Jupyter notebook](https://jupyter-notebook.readthedocs.io/en/stable/) to run our Python data analysis in this course.

You can launch a Jupyter notebook on your computer two ways, either via the command line or using `Anaconda Navigator`.

## Using the command line

The recommended approach for starting a notebook is to use the Anaconda Prompt on Windows or the Terminal app on MacOS. To do so, we simply need to activate our `'musa-620'` environment and then launch the notebook.

From the command line, run:

```
conda activate musa-620
```

```
jupyter notebook
```

This will create the local Jupyter server. If it does not open in a browser, copy the link that is output by the command into your favorite browser. Typically, the server will be running at http://localhost:8080.

Once the server is running, you can create a new notebook and get started!

#### Note

The notebook will execute code from the current working directory (the directory that the notebook was launched from). If using relative file paths to load the data, the path should be relative to this working directory. From within the Jupyter notebook, you can find out the current working directory by running the following command in a cell:

```
pwd
```

## Using Anaconda Navigator

You can create new notebooks from the home page of the Anaconda Navigator.

First, you must select the `'musa-620'` environment from the dropdown button next to the `Applications on` text. Once you have switched to the right environment, simply hit the "Launch" button underneath the Jupyter notebook logo.

For more help launching a Jupyter notebook, see [the Jupyter documentation](https://jupyter.readthedocs.io/en/latest/running.html#running).

#### Next: If you encounter environment or installation problems see the [common problems](common-issues.md) guide for potential solutions.
