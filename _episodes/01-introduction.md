---
title: "Introduction"
teaching: 10
exercises: 5
questions:
- "Why would I want to use the Jefferson Lab Jupyter server?"
- "How can I access the Jefferson Lab Jupyter server?"
objectives:
- "Explain the benefits of using the centralized server."
- "Create a new Jupyter notebook with the Python 3 kernel."
keypoints:
- "Access Jefferson Lab's Jupyter server at [jupyter.jlab.org](https://jupyter.jlab.org)."
---

## The Jefferson Lab Jupyter server allows for centralized analysis

You may be familiar with the benefits of using python, IPython, or Jupyter
notebooks on your local computer, whether that is a laptop or a desktop computer
at your institutions. This may appear as a sufficient solution to you.

Why would you want to use a centralized Jupyter server for storing your
notebooks?

> ## What are the benefits and disadvantages of a centralized approach?
>
> Take a few minutes to list the benefits and disadvantages that you see at this
> point to using a centralized server. Consider both your own convenience
> as well as the point of view of others with whom you are collaborating.
>
> If you have the opportunity to talk to another Jupyter user about your list,
> compare and explain why you may have listed things that the other person has
> not listed.
>
> > ## Solution
> >
> > It is difficult to give an exhaustive overview of all benefits and
> > disadvantages. Here are a few:
> >
> > Benefits:
> > - large data files can be kept on the central server,
> > - no knowledge for starting Jupyter is required since that is handled centrally,
> > - all users of the central server will be using the same software version.
> >
> > Disadvantages:
> > - online access is required to be able to use the central server,
> > - updating packages to bleeding edge versions may not be possible,
> > - the security implications of using a central system are stricter than
> >   when accessing a service running on your local system only.
> {: .solution}
{: .challenge}

## Accessing the Jefferson Lab Jupyter server

You can access the Jefferson Lab Jupyter server at [jupyter.jlab.org](https://jupyter.jlab.org).
You will be asked to log in with your Jefferson Lab username and password.

As with a locally running instance of a Jupyter Notebook, you will at first
reach your Jupyter Notebook file tree. When you log in for the first time, this
file tree will be empty.

## Creating notebooks on the Jefferson Lab Jupyter server

We can create blank notebooks by using the "New" button on the top right of the
file tree window. There are several kernel options available:
- Python 2 Notebook
- Python 3 Notebook
- Text File
- Folder
- Terminal

> ## More kernel options listed?
>
> It is possible that in the future more kernels will be added to the Jupyter server
> to allow anything from interactive ROOT C++ notebooks to R notebooks. There are
> currently more than 50 different kernels supported by the Jupyter server.
{: .callout}

> ## Different interface?
>
> It is also possible that the server will be upgraded to the new Jupyter Lab
> interface which will appear familiar to users of IDEs or analysis studios
> (such as RStudio or even Matlab).
{: .callout}

Let's practice using the server to create a new python 3 notebook.

For this lesson we will exclusively use python 3. Most functionality on the
Jefferson Lab Jupyter server should be equivalent between python 2 and python 3.
The system administrators have been attempting to keep the same set of packages
installed for both python versions, to the extent possible

> ## Create your first notebook on the Jefferson Lab Jupyter server!
>
> Log in to the Jefferson Lab Jupyter server at [jupyter.jlab.org](https://jupyter.jlab.org)
> and perform the following actions:
>
> 1. Create a new directory called `tutorial`
> 2. Create a new Python 3 Notebook in the directory `tutorial`
> 3. Change the name of the Notebook to `python3-intro`
> 4. Add the following cells of code, and execute them with Shift-Enter:
>    ~~~
>    import sys
>    print(sys.version)
>    !pip list
>    ~~~
>
> > ## Solution
> >
> > You should obtain output that specifies the python version that you are using.
> > ~~~
> > 3.4.8 (default, Mar 23 2018, 10:04:27)
> > [GCC 4.8.5 20150623 (Red Hat 4.8.5-16)]
> > ~~~
> >
> > With the exclamation point (`!`) we can execute system commands. Even though
> > you can open a terminal on the Jupyter server, it is locked down for security
> > reasons. Using the exclamation point can be useful in a pinch, such as here
> > to verify which python packages are available.
> {: .solution}
{: .challenge}

## Uploading Jupyter Notebooks to the Jefferson Lab Jupyter server

To get started with the tutorial, we will be uploading Jupyter Notebooks from
a GitHub repository at [github.com/JeffersonLab/jupyter_tutorial](https://github.com/JeffersonLab/jupyter_tutorial/).

You can upload multiple files at once by selecting them in the upload dialog.
You will need to confirm the files individually before they will be uploaded.

> ## Upload sample notebooks on the Jefferson Lab Jupyter server!
>
> Log in to the Jefferson Lab Jupyter server at [jupyter.jlab.org](https://jupyter.jlab.org)
> and perform the following actions:
>
> 1. Download the sample Jupyter notebooks in the [jupyter_tutorial GitHub repository](https://github.com/JeffersonLab/jupyter_tutorial/archive/master.zip)
> 2. Upload the files in the `1_Basics` directory
{: .challenge}
