---
layout: page
title: Lab Info
permalink: /wiki/
---

## Workstation

You can use the lab workstation to train models or do any other compute-intensive tasks. The workstation user name is `labmember`. Once you've logged in, create your own personal folder inside the home directory (e.g., `~/jhennig`).

### Setting up SSH access

To ssh into the lab workstation, you will need to do a few things:

1. If you have not already done so before, create an ssh key on your personal computer, with `ssh-keygen -t rsa -b 4096`

2. Copy the ssh public key on your personal computer (`~/.ssh/id_rsa.pub`) to the workstation's `~/.ssh/authorized_keys` for the `labmember` user.

3. On your personal computer, create or append to the file `~/.ssh/config`:

```
Host henniglab
    HostName WORKSTATION_IP
    User labmember
    Port WORKSTATION_PORT
```

where `WORKSTATION_IP` and `WORKSTATION_PORT` are numbers I or another lab member can tell you.

You should now be able to log in from your personal computer with `ssh henniglab`.

### Using the workstation's GPU in a Jupyter notebook

TBD


### General guidelines

When installing python packages, only install to a conda environment (or any other python environment manager), not the default python installation. For example, the following will create a new conda environment:

```
conda create --name valuernn python=3.9 pytorch matplotlib numpy scipy scikit-learn
conda activate valuernn
```

Once you have activated your environment, you can always install additional packages with:
```
conda install thepackageiforgot
```
