---
title: Installing Go on Kali
permalink: /installing-go-on-kali/
tags: Linux
---
In this post you will learn how to install the Go programming language on Kali Linux using the terminal. The commands in the code blocks can be copied and pasted directly into the terminal.

#### Downloading Go

You can either download GO by visiting [https://golang.org/](https://golang.org/) or you can use the curl command like so.

`curl -L -O https://golang.org/dl/go1.15.linux-amd64.tar.gz`

#### Installing Go

You need to untar Go.*.tar.gz to /usr/local. This can be done by running the tar command and specifying which directory to untar the contents to like so.

`sudo tar -xvf go1.15.linux-amd64.tar.gz -C /usr/local`

The last step involves adding paths for login shells and non-login shells. An example of a login shell would be remotely accessing Kali using SSH. An example of a non-login shell would be logging into Kali using a GUI. Each login method requires the slight modification of two files. I prefer to modify both files.

##### Login Shell

You will first make a few modifications to the profile file like so.

`nano ~/.profile`

At the very bottom of the file after the "fi" add these three lines.

`export GOPATH=$HOME/go`  
`export PATH=$PATH:$GOPATH/bin`  
`export PATH=$PATH:/usr/local/go/bin`

To save the changes press CTRL X keys together and when prompted to save press the Y key and then the ENTER key. Now you need to reload the profile file so the new changes will be process. To do this run the following command.

`source ~/.profile`

##### Non-login Shell

You will need to repeat the same steps but for the bashrc file like so.

`nano ~/.bashrc`

Just like before add these three lines at the very bottom of the file.

`export GOPATH=$HOME/go`  
`export PATH=$PATH:$GOPATH/bin`  
`export PATH=$PATH:/usr/local/go/bin`

Save your changes exactly like you did when editing the profile file. Don't forget to reload the new changes like so.

`source ~/.bashrc`

Now to test the installation by typing the command go in the terminal. You should receive something similar to "Go is a tool for managing Go source code." as a response to running the command.
