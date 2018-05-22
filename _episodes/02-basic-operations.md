---
title: "Basic Operations"
teaching: 10
exercises: 5
questions:
- "How can I read common nuclear physics data file formats?"
objectives:
- "Import a Python library to read ROOT data files."
- "Plot simple graphs from ROOT data files."
keypoints:
- "Use the `uproot` library to read ROOT data files in Python."
- "Use `arrays()` to access fields in ROOT data files as `numpy` arrays."
- "Use the `pyplot` library from `matplotlib` for creating simple visualizations."
---

## Reading ROOT files with python

The majority of nuclear, hadronic, and particle physics data files are in the
ROOT file format. At some point or other, reading a ROOT file is a requirement
in any analysis chain. In this episode we explore how to read ROOT files in
the Jupyter notebook using (only) python tools.

We will be using the package *uproot* to read ROOT files. Since uproot is a
quickly evolving package, we refer to the [documentations](http://uproot.readthedocs.io/en/latest/)
for the latest.

> ## PyROOT vs. uproot
>
> There is a python interface included in most ROOT installation: PyROOT. This
> package solves a different problem than what we are aiming for here. PyROOT
> provides bindings from python to the ROOT C++ functions. It allows therefore
> not only the reading of ROOT files but access to *any* ROOT function.
>
> uproot only aims to enable the reading of ROOT files in python, and assumes
> that there are sufficient tools available within the python ecosystem to do
> the rest of the analysis.
{: .callout}

Let's start by opening a new python 3 notebook and reading a ROOT file using
uproot. We will use the notebook "read-root-files.ipynb" that you uploaded in
the previous episode of this lesson.

> ## Load a ROOT file using uproot, convert into pandas and plot using matplotlib
>
> The notebook "read-root-files.ipynb" reads in a ROOT file located at
> ~~~
> /lustre/expphy/cache/hallc/qweak/rootfiles/pass5b/QwPass5b_18110.000.trees.root
> ~~~
> As you may surmise, this is one of the ROOT files of the Qweak experiments.
> It contains about 5 minutes of data (from a 2-year long experiment).
>
> On the Jupyter server we cannot use the convenient shortcut `/cache/` to
> access the MSS cache storage. Instead we use the full path `/lustre/expphy/cache/`.
>
> 1. Execute the entire notebook and observe the results
> 2. The same file contains another tree, `Mps_Tree`, with slightly differently
>    named branches. Modify the notebook to load this different tree in the same
>    input ROOT file.
> 3. Use uproot's function `get()` to list the names of the branches in this
>    different tree. Find the ones that are most likely equivalent, i.e. also
>    beam current monitor (BCM) outputs.
> 4. Recreate the correlation plots for the MPS quantities.
>
{: .challenge}
