---
layout: default
title: pip Install
nav_order: 3
parent: Install
---


# Install GrimoireLab using pip

Use `pip` for installing GrimoireLab if you want to:

* have full control over the environment GrimoireLab runs in
* use only components of GrimoireLab
* learn the inner makings of GrimoireLab


## Prerequisites

**Software**

[Python 3](https://www.python.org/downloads/) is required. Currently, GrimoireLab is developed using Python 3.5 and 3.6, thus
any of these versions should be safe to grant GrimoireLab to run smoothly.

Some of GrimoireLab dependencies need non-Python packages as pre-requisites to be installed. In Debian-derived systems (such as Ubuntu), that can be done by installing the python3-dev package:

```console
$ sudo apt-get install python3-dev
$ sudo apt-get install build-essential
```

In order to run GrimoireLab, you need to have Elasticsearch, Kibiter and MySQL running in your machine. For the
sake of simplicity, we assume that they run in localhost with no authentication needed.

**Hardware**: Resources requirements depend on the number of projects and their size:
- Plan for a minimum of 100GB of storage, 2 CPUs, and 8 GB of RAM for analyzing a small/medium size project.


## Use a Python virtual environment

This step is optional but highly recommended.

Use Python 3 to create a Python virtual environment using the [Python3 venv module](https://docs.python.org/3/library/venv.html).

> _Note:_ Instead of driving the `venv` module directly, you can also use [the pipenv module](http://docs.python-guide.org/en/latest/dev/virtualenvs/#installing-pipenv).

First, create a new environment. The following instructions places the Python virtual environments under the `venvs` subdirectory in your home directory, and will call it `gl`:

```console
$ python3 -m venv ~/venvs/gl
```

Once the virtual environment is created, activate it:

```console
$ source ~/venvs/gl/bin/activate
(gl) $
```

Now, any Python module you install in that shell will be installed under ~/venvs/grimoirelab, and it will be used by Python only in shells with this virtual environment activated. Since the virtual environment is under your home directory, you won't need to sudo to install: everything will be installed in your name, with your permissions.

When you are done with a virtual environment, you can deactivate it until you need to activate it again. Deactivating is easy:

```console
(gl) $ deactivate
$
```

### Install Python tools in the virtual environment

This step will increase the chances that you have no troubles later.

Depending on what you have installed in your system, it may be convenient to install some Python tools in it, and to upgrade some others. We recommend that you type, in your activated virtual environment:

```console
(gl) $ pip install --upgrade pip
(gl) $ pip install --upgrade setuptools
(gl) $ pip install --upgrade wheel
```

### Install all GrimoireLab tools at once

Use `pip` to install the `grimoirelab` package, that pulls all the other GrimoireLab tools as dependencies:

```console
(gl) $ pip install grimoirelab
```

Once installed, check that everything is as it should be:

```console
(gl) $ grimoirelab -v
```


### Run GrimoireLab

GrimoireLab can be launched with the following command:
```console
(gl) $ sirmordred -c <path to setup.cfg>
```

The GrimoireLab repository contains a set of default settings that can be used to execute GrimoireLab. You
can follow the steps below to get them:

1. Clone the github.com/chaoss/grimoirelab project repository
```console
$ git clone https://github.com/chaoss/grimoirelab
```

2. Go to the settings folder
```console
$ cd grimoirelab/default-grimoirelab-settings
```

3. Run the following command
```console
$ sirmordred -c setup-pip.cfg
```

### Configure GrimoireLab

Configuration is done through two files:

* projects.json
* setup.cfg

They are described in the [Sirmordred repository](https://github.com/chaoss/grimoirelab-sirmordred/blob/master/README.md)
