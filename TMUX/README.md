# Tmux Cheat Sheet

### Contents
1. [About tmux](#about-tmux)
2. [General](#general) 
3. [Sessions](#sessions)
4. [Windows](#windows)
5. [Panes](#panes)



---
## About tmux

tmux的主要元素分为三层：

- Session 一组窗口的集合，通常用来概括同一个任务。session可以有自己的名字便于任务之间的切换。
- Window 单个可见窗口。Windows有自己的编号，也可以认为和ITerm2中的Tab类似。
- Pane 窗格，被划分成小块的窗口，类似于Vim中 C-w +v 后的效果。

![Concept](images/concept.jpg)

**Tips:**  (Credit to https://github.com/gpakosz/.tmux)
  - `<prefix>` means you have to either hit <kbd>Ctrl</kbd> + <kbd>a</kbd> or <kbd>Ctrl</kbd> + <kbd>b</kbd>
  - `<prefix> c` means you have to hit <kbd>Ctrl</kbd> + <kbd>a</kbd> or <kbd>Ctrl</kbd> + <kbd>b</kbd> followed by <kbd>c</kbd>
  - `<prefix> C-c` means you have to hit <kbd>Ctrl</kbd> + <kbd>a</kbd> or <kbd>Ctrl</kbd> + <kbd>b</kbd> followed by <kbd>Ctrl</kbd> + <kbd>c</kbd>


## General

```tmux``` start new 

```tmux new -s myname``` start new with session name

```tmux a -t sessionName``` attach to session with name

```tmux ls``` list sessions

```tmux kill-session -t myname``` kill session

```tmux kill-server```  kill all tmux open sessions (and server)

```tmux kill-session -a``` If you are inside a tmux session you would like to keep, use it to close all other sessions

```tmux kill-session -t targetSession``` kill that specific session

```<prefix> e``` opens ~/.tmux.conf.local with vim

```<prefix> r``` reloads the configuration

```C-l``` clears both the screen and the tmux history

```<prefix> t``` bring up clock




## Sessions


```<prefix> C-c``` creates a new session

```<prefix> s``` switch session

```<prefix> d``` detached from session

```<prefix> $``` rename current session

## Windows

```<prefix> c``` create window

```<prefix> w```  list windows

```<prefix> C-h```  next window

```<prefix> C-l```  previous window

```<prefix> f```  find window

```<prefix> Tab``` brings you to the last active window

```<prefix> ,```  name window

```<prefix> &```  kill window

## Panes

```<prefix> -``` splits the current pane vertically

```<prefix> _``` splits the current pane horizontally

```<prefix> q```  show pane numbers

```<prefix> x```  kill pane

```<prefix> o```  swap panes

```<prefix> <``` and ```<prefix> >``` swap panes with arrows

```<prefix> h```,```<prefix> j```, ```<prefix> k``` and ```<prefix> l``` navigate panes using vim

```<prefix> H```, ```<prefix> J```, ```<prefix> K```, ```<prefix> L```  resize pane

```<prefix> +``` maximizes the current pane to a new window

```<prefix> q``` list id of  all the panes

```<prefix> “``` split a new pane horizontally

```<prefix> %``` split a new pane vertically

```<prefix> z``` Temporarily maximize the pane 

