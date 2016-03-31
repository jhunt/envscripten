envscripten
===========

I love my environment. I take it everywhere with me, and now you
can too!

Getting Started
---------------

First (and this only has to be done once), clone and rename/push
this repo back up to your Github organization:

    cd $HOME
    git clone https://github.com/jhunt/envscriptend env
    cd env
    git remote remove origin
    git remote add origin git@github.com/<YOU>/env
    git push origin master

(don't foget to make the `env` repo on your Github!)

Then, you can start customizing!

A few key things to note:

1. Any scripts you put in `bin/` will be copied to `~/bin` and
   properly chmodded.
2. Any files you put in `dot/` will be copied into `~`, with a dot
   in front of their file name.  For example, `dot/vimrc` will
   become `~/.vimrc`

Moving In
---------

To move into a brand new machine, do this:

    cd $HOME
    git clone https://github.com/<YOU>/env
    cd env
    ./install init

That will install any packages that you may want (probably
requires sudo), and install your environment configuration files
into your home directory.

If you don't have sudo rights, you can just drop the `init`
argument and run `./install` from the env directory.

If you've made some changes to your environment (and I hope you
do!), you're just a few commands away from being up-to-date on any
box you happen to be on:

    cd ~/env
    git pull
    ./install

Happy Hacking!
