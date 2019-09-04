# Changing the Jupyter Notebook Start-up Folder

By default, the Jupyter notebook launches from your home directory. It is best
to open notebooks from the specific assignment/week folder that you
are working on.

It will be easiest to change the directory before launching the Jupyter notebook:

## Step 1: Change to the desired directory

Let's imagine we want to change to a folder named:

/Users/YourUserName/MUSA_620 (on a Mac),

or

C:\Users\YourUserName\MUSA_620 (on Windows)

If you need help finding the folder name's path, see [this guide](finding-file-path.md).

Next, use the following steps:

**Step 1.** On Windows, open the Anaconda Prompt, or on Mac, open the Terminal.

**Step 2.** Navigate to the folder where the environment file is located. From the Prompt or Terminal run:

**Windows**

```
cd C:\Users\YourUserName\MUSA_620
```

**Mac**

```
cd /Users/YourUserName/MUSA_620/
```

## Step 2: Launch the Jupyter notebook

Now, type the following command, either in Anaconda Prompt or the Terminal:

```
jupyter notebook
```

And the launched notebook will start from your desired folder!

**Note:** It is also possible to launch the notebook in the default directory
using the Navigator, and then navigate to the desired folder within the Jupyter
notebook interface.
