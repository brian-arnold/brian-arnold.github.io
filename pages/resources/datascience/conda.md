---
layout: article
key: page-resources-bioinfoTools
permalink: /resources/datascience/conda
---

Back to [Data Science](/resources/datascience/)

# Conda

Much research involves analyzing data using software developed by others. Conda is **extremely** useful for *installing* and *managing* this software. Most program I've wanted to use are installable via conda, and you can even manage R packages with conda.

## ***Why*** should you use conda?

### Software installation

Software engineers typically build upon previously-existing software to make a new program (or package). Thus, when you install their new program, you also need to install this previously-existing software they used, which are called *dependencies*. Conda takes care of all of this for you automatically!

### Software management

If you want to simultaneously use several software packages, you may run into conflicts in which several of them have conflicting dependencies; i.e. the software packages require different versions of the same dependency. If you run into this issue, you can get strange error messages that take a while to solve. When you install software via conda, it tries to install software in such a way that everything is compatible, saving you a lot of time and frustration.

## ***How*** do you use conda?

I will soon put some details here directly, but see [here](https://astrobiomike.github.io/unix/conda-intro#:~:text=command%2Dline%20environment%3A-,Getting%20and%20installing%20Conda,-Conda%20comes%20in) for a fabulous introduction on how to install and use conda.


