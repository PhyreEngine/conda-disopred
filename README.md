This repository contains a [conda][conda] recipe for building
[DISOPRED][disopred], a tool for predicting disordered regions of protein
structure from a sequence profile.

## Prerequisites

1. You will need an installation of [conda][miniconda].

2. Your root conda installation must have the `conda-build` installed.

## Building

You should be able to build this package by simply running `./build`.

## Patches

This recipe contains the following patches:

* `makefile.patch`

    Play nicely with `conda build` by allowing the `$(CC)` and `$(CXX)`
    environment variables to pass through. Also change the location of the data
    files to `$PREFIX/share/disopred/{data,dso_lib}`.

[conda]: https://conda.io
[miniconda]: https://conda.io/miniconda.html
[disopred]: http://bioinf.cs.ucl.ac.uk/psipred/?disopred=1
