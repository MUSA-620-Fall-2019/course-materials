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
