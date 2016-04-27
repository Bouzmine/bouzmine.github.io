---
layout: default
title: "My Terminal"
date: 2016-04-26
---

Ha, the terminal, that thing...

![The Terminal](http://i.imgur.com/71Ownzu.png)

I love mine, but I've come a long way before loving it. First, it *was* ugly and second, it was unfriendly. 

### Appearance

Let's start with the ugly aspect, on a fresh Mac, you are greated with 

![Default OS X Terminal](http://i.imgur.com/U8YZZLC.png)

It's *white*. That's it. First thing I did was to install [iTerm](http://iterm2.com). It's a Terminal.app replacement and I have to admit it's quite great (even if I haven't scratched the surface of what I'd be able to do with it). The real reason I did so (install it), was to be able to customize the appearance of that Terminal window. ![Blur settings](http://i.imgur.com/AIXZIhu.png) In iTerm, you can customize the behavior of the window (tab bar location, theme, etc.) and you can customize the appearance *a lot* : color scheme, font, constrast, cursor, transparency, blur, background image, etc. What I did, was to install *[Tomorrow Night Eighties](https://github.com/chriskempson/tomorrow-theme/blob/master/iTerm2/Tomorrow%20Night.itermcolors)* theme for iTerm so colors where a big more flat and stylish. I played with the transparency and blur to find a great balance between reading ease and *swag*. Next step, installing [ZSH](http://zsh.sourceforge.net) via [Pretzo](http://zsh.sourceforge.net), a lightweight configuration framework for ZSH, a shell (roughly a terminal manager) which is much more powerful than *bash*, OS X's default shell. ZSH's advantages are : **much** better path and command completion, different shell prompt, path expansion, spelling correction, interactive prompt (colors to tell if command exists), etc. 

Path and command completion : Hit `tab` and see the path or command being completed (Docu -> Documents/ or git stat -> git status)

Path expansion : Enter `/U/f/D` and type `tab` to see that snippet expanded in `/Users/francis/Documents`

Spelling correction : If you mistype a command, you'll be prompted with the right command which you will then have the choice to accept or decline.

Interactive prompt : The commands I type turn green if they exsit and red if they don't (quite useful), also, when I type in a correct filepath, it's underlined.

Different shell prompt : That's a big one for me, you can change your shell prompt to something that suites your needs better. [Here](http://mikebuss.com/2014/04/07/customizing-prezto/) is an article explaining how to customize your prompt. Personally, I chose `pure` and here's what it does : 

![Pure Shell Prompt](http://i.imgur.com/VvdDAOQ.png)

In blue : current file path

In grey : current branch

In yellow : last command execution time

The arrow is the prompt and `git add .` is the command I typed in at that moment

**To note** : I had to play with the constrast in iTerm's preferences as the current branch label would not show up correctly.

### Unfriendlyness

When playing in the Terminal, you might find some difficulties, or some things that are just not quite instinctive : 

Escaping of `man`: From time to time, I use `man` but I never remember how to get out of it. Every time, I try `escape`, `ctrl-c`, etc. But the right one is just `q`.

My favorite or more useful `git` commands or options :

- `git commit -am ""` to commit every file that is already tracked.
- `git commit -S […]` to sign a commit using a GPG key.
- `git reset —hard HEAD` to reset to the state saved with the last commit.
- `git checkout -b [new branch name]` to create a new branch and checkout to it.
- `git worktree add [path] [branch]` to map a branch to a folder to have two (or more) branches of the same repo available concurrently.

There are much more difficulties in the Terminal, than I listed, but those were the one I encountered or encounter. I will try to keep this list updated with my discoveries.