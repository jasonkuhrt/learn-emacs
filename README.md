# learn-emacs

My personal configuration journey through emacs


#### Installing stuff

```sh
# Install the version of emacs that works the best
# on OSX. I expect scrolling windows to have
# inertia to them, etc.
brew tap railwaycat/emacsmacport
# The default icon used is an aesthetic nightmare.
# Use `--icon-modern` to get something reasonable.
brew install emacs-mac --icon-modern
# Make the installed application available in my
# ~/Applications folder.
brew linkapps
# I will consider doing this when/if ever I hit the
# use-case.
consider: https://gist.github.com/railwaycat/4043945
# OSX comes with an older version of emcas that I
# do not want. Anyways, I want to manage emacs with
# brew.
sudo rm /usr/bin/emacs
sudo rm -rf /usr/share/emacs
```

#### Learning about Emacs
Some resources matter more than others:

The official Emacs portal: https://www.gnu.org/software/emacs/manual/

Learn about Emacs:
- Official guide: https://www.gnu.org/software/emacs/manual/pdf/emacs.pdf
- Official reference card: https://www.gnu.org/software/emacs/refcards/pdf/refcard.pdf. I will be using evil which reduces the benefit of this, however, seeing the scope of actions at a glance is still useful. I learn which out-of-the-box features the authors thought mattered enough to highlight. There are some other reference cards for specific features like `dired` but I am not interested in this yet. I might came back to it later...

Learn about Emacs Lisp (the programming language powering Emacs):
- Official reference: https://www.gnu.org/software/emacs/manual/pdf/elisp.pdf
- Official guide: https://www.gnu.org/software/emacs/manual/pdf/eintr.pdf

Discover spacemacs:
- https://github.com/syl20bnr/spacemacs
- https://twitter.com/spacemacs


#### Begin using Emacs

It turns out that `Spacemacs` is great. That is what I will be using.

