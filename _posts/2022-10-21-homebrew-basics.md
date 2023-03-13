---
title: Getting Started With Homebrew
permalink: /homebrew-basics/
tags: macOS
categories: macOS
---


## What Is Homebrew
Homebrew is an awesome package manager for macOS. If you're familiar with linux then you'll feel right at home using Homebrew. All the information you'll ever need to know about Homebrew can be found at https://brew.sh/.  By the end of this article you'll have a better understanding of how to use Homebrew.

Let's get started!

## Installing Homebrew
To begin installing Homebrew copy and paste the command sequence below into your favorite terminal.  Alternatively, you can copy & paste the exact same command sequence from https://brew.sh/.  

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" `  

Once this is completed you can verify all is good by running `brew --version` to print the Homebrew version in your terminal.

## Using Homebrew
Using Homebrew is pretty simple. You will use the `brew` command to interact with the Homebrew package manager.

## Searching For Packages
First we need to find a package to install. To search for a specific package run `brew search nmap` from the terminal. Alternatively you can use https://formulae.brew.sh/ to search as well.

## Installing Packages
Now that we have a package we wish to install we can proceed with the next step. To install a package we'll use the brew command followed up with `install` and the app name.  The web version of searching for packages includes the exact commands to run for installing a package
We'll start by install nmap which is a command line tool for port scanning.
`brew install nmap`
It's a pretty simple collection of commands.   While installing other packages you might notice `--cask` is used in the command sequence.  Cask is used for when a package includes a user interface (GUI) such as Firefox or the iTerm2 terminal.  

`brew install --cask iterm2`  
`brew install --cask firefox`

## Uninstalling Packages
To remove a package installed with Homebrew simply run `brew uninstall nmap`. 

## Updating Packages
To update all installed packages definitions (formulae) and Homebrew simply run `brew update`. You can also upgrade your installed packages run `brew upgrade`. Whenever you install a new package Homebrew will also update it's package definitions as well.

## Conclusion
There you have it! The very basics of installing and using Homebrew to enhance your macOS experience. Homebrew is always at the top of my list after a new macOS installation.

Continue learning by visiting [https://brew.sh](https://brew.sh)

## Helpful Links
[https://brew.sh](https://brew.sh)  
[https://docs.brew.sh/](https://docs.brew.sh/)  
[https://formulae.brew.sh/](https://formulae.brew.sh/)
