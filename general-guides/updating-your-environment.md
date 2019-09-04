# Updating your local environment

If you followed the instructions for [downloading environment.yml files from Github](./downloading-environment-files.md), you should have an environment file saved somewhere on your computer. Let's imagine the file is located at:

/Users/YourUserName/Desktop/environment.yml (on a Mac),

or

C:\Users\YourUserName\Desktop\environment.yml

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

Be sure to use the true location of the file on your computer. This will set the current "working directory" of the Prompt/Terminal to the folder location. You can confirm the contents of your current working directory by running:

**Windows**

```
dir
```

**Mac**

```
ls
```

**Step 3.** Then we can update your local environment using:

```
conda env update --name musa-620 --file environment.yml
```

(Assuming the file is called "environment.yml")
