---
title: Introduction To Tmux
permalink: /introduction-to-tmux/
tags: Linux
categories: Tools
---

## What is Tmux
Tmux is an awesome terminal multiplexor.  It's a command line tool which will allow you to run multiple programs from within Tmux.  Let's cover some basic terminology real quick. At a high level Tmux has sessions, windows, and panes. A session is started when we run the Tmux command from our favorite terminal. A session contains the windows and panes. A window contains the panes, and a pane is where we will interact with the terminal. 

When we start a Tmux session we start off with a single window with a single pane. From here we have a few options. Keep in mind these are just a few samples. There's so much more that you can do with Tmux.

- We can immediately start using the terminal.
- We can split the pane as needed and have more than one active terminal.
- We can create more than one window.
- We can start a program and then detach from the session.

One of Tmux's greatest strengths is that it runs as a process. Tmux can detach and reattach sessions. Let's say you use ssh to connect to a server hosted with your favorite cloud provider.  Maybe you use this server to run port scans on your home network to check for open ports. If you are using Tmux and your ssh session dies, you can just reconnect to your server and attach to the Tmux session which has your port scan running. If you are not using Tmux, you will have to start the scan over after reconnecting to your server.

Let's get started on how to use Tmux.

## Installing Tmux
* MacOS (```brew install tmux```)
* Debian Linux (```apt install tmux```)
* Most Linux Distrobutions have a Tmux package
* Windows doesn't have a Tmux package but it can be used with WSL (Windows Subsystem for Linux).

## Using Tmux
Tmux can be used by simply typing ```tmux``` in the terminal.  Once, you're in a Tmux session you can use ```ctrl-b``` to activate in session commands.  The ctrl-b command sequence allows you to split panes, create new windows, detach active sessions etc.  


## Helpful Commands To Start 

| Key Command  | Description   |
|---|---|
| tmux | Start a session |
| tmux new -s Test | Start a new session called Test   |
| tmux ls | List any active sessions |
| tmux attach -t # | Connect to an active session (# = session number) |
| tmux rename-session -t # new_name | Rename a session (# = session number)  |

## Helpful Commands For Interacting With Active Sessions

| Key Command  | Description   |
|---|---|
| exit or ctrl-d | Exit an active session, window, or pane |
| ctrl-b then shift-5 | Create another pane |
| ctrl-b then arrow keys | Move between panes |
| ctrl-b then c | Create a new window |
| ctrl-b then n | Move to the next window |
| ctrl-b then p | Move to the previous window |
| ctrl-b then d | Detach current session |
| ctrl-b then D | Detach session of choice |

# Conclusion
There you have it! The very basics of installing and using Tmux to enhance your terminal experience. We only scratched the surface of what Tmux is capable of, so continue learning by visiting [https://github.com/tmux/tmux/wiki/Getting-Started](https://github.com/tmux/tmux/wiki/Getting-Started)!
