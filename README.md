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

- The official Emacs portal: https://www.gnu.org/software/emacs/manual/
- Official guide: https://www.gnu.org/software/emacs/manual/pdf/emacs.pdf 

Emacs is powered be a dialect of Lisp so it might help to learn about that language one day:

- Official reference to Emacs Lisp: https://www.gnu.org/software/emacs/manual/pdf/elisp.pdf
- Official guide to Emacs Lisp: https://www.gnu.org/software/emacs/manual/pdf/eintr.pdf

However the most immediate win is discovering spacemacs:
- https://github.com/syl20bnr/spacemacs
- https://twitter.com/spacemacs


#### Begin using ~~Emacs~~ Spacemacs

It turns out that `Spacemacs` is great. That is what I will be using.

There is a handy [tutorial](http://thume.ca/howto/2015/03/07/configuring-spacemacs-a-tutorial/) that will help kick things off assuming you want to being with configuration.

On the first boot of `Spacemacs` generate the automatic `~/.spacemacs` file by typing `<SPC> : dotspacemacs/install RET`. The look at it/edit it via `SPC f e d` which will open it for you.

The font is too small, try `18`.

#### Theme

The deafult available themes are not much to my liking. To get better ones follow these [instructions](https://github.com/syl20bnr/spacemacs/blob/master/doc/DOCUMENTATION.md#example-themes-megapack-example). I picked out these special ones:

```
django
fogus
birds-of-paradise-plus
tronesque
busybee
dakron
gruvbox
dorsey
```

#### Misc

Since I am not a novice I will want [strict smart parens on](https://github.com/syl20bnr/spacemacs/blob/2d28e5325118127eae6f7602dcd7d5bfe62ab22f/doc/DOCUMENTATION.md#smartparens-strict-mode).

Note to self: `dotspacemacs/config` is where most all config should live.

