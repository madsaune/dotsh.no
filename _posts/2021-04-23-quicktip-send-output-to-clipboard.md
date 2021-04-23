---
layout: post
title: "Quicktip: Send output to clipboard"
tags: [Powershell]
---

Ever found yourself wanting to copy the output from a command to your clipboard without having to select it first? In this short article we're going to cover how to do that in Windows, MacOS and Linux with Powershell.

_NOTE: These commands are not Powershell spesific and will work in the same way from cmd, bash, zsh, etc._

## Windows

In Windows we have a command called `clip` that we can pipe some output to and it will copy it to our clipboard. Now let's say we want to fetch our public ip and copy it to clipboard we would do the following:

```powershell
irm ifconfig.co/ip | clip
```

If you `Ctrl+v` in your text editor of choice you should see the output of the command (in this example; your public ip).

## MacOS

MacOS also comes with it's own command for copying output to clipboard, which is `pbcopy`.

```powershell
irm ifconfig.co/ip | pbcopy
```

## Linux

Similar for Linux, we have the `xclip` command which will do the same thing.

### Installation

Unlike Windows and MacOS, `xclip` does not come pre-installed in most Linux distributions, but is available from all the major package managers.

**Ubuntu based systems**

```bash
sudo apt install xclip
```

**RHEL based systems**

```bash
sudo yum install xclip
```

**Arch based systems**

```bash
sudo pacman install xclip
```

### Copy to clipboard

```powershell
irm ifconfig.co/ip | xclip
```
