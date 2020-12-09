
[![Build Status](https://github.com/mhewedy/vermin/workflows/Go/badge.svg)](https://github.com/mhewedy/vermin/actions?query=workflow%3AGo)
[![Go Report Card](https://goreportcard.com/badge/github.com/mhewedy/vermin)](https://goreportcard.com/report/github.com/mhewedy/vermin)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

<img src="https://raw.githubusercontent.com/mhewedy/vermin/master/etc/logo.png"  alt="logo" width="20%"/>

## The smart virtual machines manager (Put ★ for the project if you find it useful)

Table of Contents:

- [What is Vermin](#what-is-vermin)
- [Install Vermin](#install-vermin)
- [Usage](#Usage)
- [Contributors](#Contributors)
- [Why not Vagrant](#Why-not-Vagrant)
- [TODO](#TODO)

----

# What is Vermin
Vermin is a smart, simple and powerful command line tool for Linux, Windows and macOS. It's designed for developers/testers and others working in IT who want a fresh VM environment with a single command. It uses VirtualBox to run the VM. Vermin will fetch images on your behalf.

You can look to Vermin as a modern CLI for Vagrant Boxes.

Vermin can be used when you need an easy way to obtain a Linux environment up and running in minutes.

# Install Vermin

Vermin uses [VirtualBox v6.0 or later](https://www.virtualbox.org/wiki/Downloads) as the underlying hypervisor to create and run Virtual Machines. So you need to download and install it first.

To install/update on **macOS** and **Linux** run:

```shell script
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/mhewedy/vermin/master/install.sh)"
```

To install/update on **Windows** (PowerShell) run:

```
# Should run as Administrator
iex ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/mhewedy/vermin/master/install.ps1'))
```

# Usage:

```text
Create, control and connect to VirtualBox VM instances

Usage:
  vermin [command]

Examples:

You can use vermin by creating a VM from an image.

To list all images available:
$ vermin images

Then you can create a vm using:
$ vermin create <image>


Available Commands:
  commit      Commit a VM into a new Image
  completion  Generates shell completion scripts
  cp          Copy files/folders between a VM and the local filesystem or between two VMs
  create      Create a new VM
  exec        Run a command in a running VM
  gui         open the GUI for the VM
  help        Help about any command
  hypervisor  print the name of the detected hypervisor
  images      List remote and cached images
  ip          Show IP address for a running VM
  mount       Mount local filesystem inside the VM
  port        Forward port(s) from a VM to host
  ps          List VMs
  restart     Restart one or more VMs
  rm          Remove one or more VM
  rmi         Remove one or more Image
  ssh         ssh into a running VM
  start       Start one or more stopped VMs
  stop        Stop one or more running VMs
  tag         Add or remove tag to a VM
  update      Update configuration of a VM

Flags:
  -h, --help      help for vermin
  -v, --version   version for vermin

Use "vermin [command] --help" for more information about a command.
```

You can start using Vermin after installation using:

```shell script
$ vermin create <vagrant image here>

# example using vagrant image
$ vermin create hashicorp/bionic64

# also you can use rhel8 using:
$ vermin create generic/rhel8
```
You can use all [vagrant images](https://app.vagrantup.com/boxes/search) besides some images native to vermin. use `vermin images` to see list of vermin images and where to find vagrant images.

Vermin collects very simple usage data anonymously.

### For more info on the usage options see [Vermin documentations website](https://mhewedy.github.io/vermin/).

# Why not Vagrant:
* **Vagrant** uses a `Vagrantfile` which I think is most suited to be source-controlled inside `git`, and for some use case it is an overhead to create and maintain such file. In such cases **Vermin** come to the rescue.
* In **Vagrant**, any change you need to make to the VM you need to reload the VM (stop/start). In **Vermin** most of the changes on the VM is done while the VM is Running.
* **Vermin** is a single binary file that can be easily installed and upgraded.
* It is important to note that, starting from version `v0.94.0` **Vermin** can smoothly uses Vagrant Cloud images.
* Myself, I look (and try to achieve) to **Vermin** as a modern CLI (like Docker/Podman) for Vagrant Boxes.

# Contributors
Special thanks to [Ahmed Samir](https://github.com/aseldesouky) for contributing the logo.

### Stars Overtime
[![Stargazers over time](https://starchart.cc/mhewedy/vermin.svg)](https://starchart.cc/mhewedy/vermin)

# TODO
See [TODO.md](https://github.com/mhewedy/vermin/blob/master/TODO.md)
