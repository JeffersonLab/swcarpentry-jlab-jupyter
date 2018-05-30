---
title: "Advanced Operations: TensorFlow on Jefferson Lab data"
teaching: 10
exercises: 10
questions:
- "How do I use Jupyter to go beyond what ROOT can do?"
objectives:
- "Import a Python library to perform machine learning."
- "Train a neural network using gradient descent to find correlations."
keypoints:
- "Use the `tensorflow` library for machine learning in Python."
---

## Installing your own python packages

Not all packages you need will be installed on the Jefferson Lab
Jupyter server. To install your own packages, log in to the
interactively farm nodes and make sure you have access to the correct
python environment (we will use python 3). To do this, add the python
path to your search path:
~~~
export PATH=/apps/python/3.4.3/bin:$PATH
~~~
or in tcsh
~~~
set path = (/apps/python/3.4.3/bin $path)
~~~
This will give you access to the `pip` python package manager. You can
get a listing of currently installed packages with
~~~
pip list
~~~

We first have to setup the proxy so we can access the internet from
the interactive farm node. We can do this by setting the following
environment variables:
~~~
export HTTP_PROXY=http://jprox.jlab.org:8080
export HTTPS_PROXY=https://jprox.jlab.org:8080
~~~
or in tcsh
~~~
set HTTP_PROXY http://jprox.jlab.org:8080
set HTTPS_PROXY https://jprox.jlab.org:8080
~~~

To install new packages we have to get around the Jefferson Lab proxy,
which modifies https traffic. Install (or upgrade if already installed)
the package `tensorflow` with
~~~
pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org --user --upgrade tensorflow
~~~

When you now restart you python 3 kernel and load tensorflow, you
should find the version you just installed.
