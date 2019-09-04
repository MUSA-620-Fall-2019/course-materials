# Creating your first Anaconda environment

To create your first Anaconda environment on your laptop, use the following steps:

## Step 1: Download the environment file

First, you'll need to download the enviroment.yml file, either from
the "week-1" or "assignment-1" repository.

See the [guide for downloading environment files](downloading-environment-files.md) for more details.

## Step 2: Change to the directory containing the environment file

It will be easiest to run the command in Step 4 from the same folder as
where the environment file is located. Let's imagine the environment file is located at:

/Users/YourUserName/Desktop/environment.yml (on a Mac),

or

C:\Users\YourUserName\Desktop\environment.yml (on Windows)

If you need help finding the folder name of the environment file, see [this guide](finding-file-path.md).

Your local environment can be updated to match this file by using the following steps:

**Step 1.** On Windows, open the Anaconda Prompt, or on Mac, open the Terminal.

**Step 2.** Navigate to the folder where the environment file is located. From the Prompt or Terminal run:

**Windows**

```
cd C:\Users\YourUserName\Desktop
```

**Mac**

```
cd /Users/YourUserName/Desktop/
```

Now, if you run the following command, you should see the "environment.yml" file
listed in the output of the command:

**Windows**

```
dir
```

**Mac**

```
ls
```

## Step 3: Create the environment

Now, run the following command from the Anaconda Prompt or Terminal:

```
conda env create --file environment.yml --name musa-620
```

To confirm that the command worked, you can run:

```
conda env list
```

You should see "musa-620" listed in the output.
