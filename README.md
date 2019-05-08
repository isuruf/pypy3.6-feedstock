About pypy3.6
=============

Home: http://pypy.org/

Package license: MIT

Feedstock license: BSD 3-Clause

Summary: PyPy is a Python interpreter and just-in-time compiler. This is a Python3.6 compatible version, in beta quality.


How to use this package?
========================

Since PyPy is an alternative *interpreter*, using this package is different than other conda-forge packages.

Note that currently this package only works for macOS and Linux.

You want to create an **empty** Conda environment:

```
conda create -n pypyenv
conda activate pypyenv
```

(🔴️ you might still have `python` or `pip` binaries in your $PATH, but those are the system's and you MUST NOT use them!️)

Then, install this package:

```
conda install -c conda-forge pypy3.6
```

Now you can install `pip`:

```
pypy3 -m ensurepip
```

🎉 using this `pip` you can install any package you like! 
For example, to update `pip` itself (which you should do!):

```
pypy3 -m pip install -U pip
```

or

```
pip3 install ...
```

(You can verify that it's the correct `pip3`/`pip` using `which {pip3,pip}`. It should be something like `.../miniconda3/envs/pypyenv/bin/pip` )

🔴 You CANNOT use `conda install x` to install anything,
because Conda provides pre-built package for the regular CPython interpreter, which are incompatible with PyPy.



Current build status
====================


<table>
    
  <tr>
    <td>Azure</td>
    <td>
      <details>
        <summary>
          <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=6451&branchName=master">
            <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/pypy3.6-feedstock?branchName=master">
          </a>
        </summary>
        <table>
          <thead><tr><th>Variant</th><th>Status</th></tr></thead>
          <tbody><tr>
              <td>linux</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=6451&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/pypy3.6-feedstock?branchName=master&jobName=linux&configuration=linux_" alt="variant">
                </a>
              </td>
            </tr><tr>
              <td>osx</td>
              <td>
                <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=6451&branchName=master">
                  <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/pypy3.6-feedstock?branchName=master&jobName=osx&configuration=osx_" alt="variant">
                </a>
              </td>
            </tr>
          </tbody>
        </table>
      </details>
    </td>
  </tr>
  <tr>
    <td>Windows</td>
    <td>
      <img src="https://img.shields.io/badge/Windows-disabled-lightgrey.svg" alt="Windows disabled">
    </td>
  </tr>
![ppc64le disabled](https://img.shields.io/badge/ppc64le-disabled-lightgrey.svg)
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-pypy3.6-green.svg)](https://anaconda.org/conda-forge/pypy3.6) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/pypy3.6.svg)](https://anaconda.org/conda-forge/pypy3.6) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/pypy3.6.svg)](https://anaconda.org/conda-forge/pypy3.6) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/pypy3.6.svg)](https://anaconda.org/conda-forge/pypy3.6) |

Installing pypy3.6
==================

Installing `pypy3.6` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `pypy3.6` can be installed with:

```
conda install pypy3.6
```

It is possible to list all of the versions of `pypy3.6` available on your platform with:

```
conda search pypy3.6 --channel conda-forge
```


About conda-forge
=================

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating pypy3.6-feedstock
==========================

If you would like to improve the pypy3.6 recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/pypy3.6-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@ohadravid](https://github.com/ohadravid/)
* [@omerbenamram](https://github.com/omerbenamram/)

