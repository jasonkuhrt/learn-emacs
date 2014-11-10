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

#### Getting started
Some resources matter more than others:

The official Emacs portal: https://www.gnu.org/software/emacs/manual/

Learn about Emacs:
- Official guide: https://www.gnu.org/software/emacs/manual/pdf/emacs.pdf
- Official reference card: https://www.gnu.org/software/emacs/refcards/pdf/refcard.pdf. I will be using evil which reduces the benefit of this, however, seeing the scope of actions at a glance is still useful. I learn which out-of-the-box features the authors thought mattered enough to highlight. There are some other reference cards for specific features like `dired` but I am not interested in this yet. I might came back to it later...

Learn about Emacs Lisp (the programming language powering Emacs):
- Official reference: https://www.gnu.org/software/emacs/manual/pdf/elisp.pdf
- Official guide: https://www.gnu.org/software/emacs/manual/pdf/eintr.pdf


#### Figuring out package management
Next I want to setup the basis for which all subsequent installation will be based upon. After reading too much seems like we're all best off using MELPA + Cask + Pallet.

- MELPA is a repository for Emacs packages
- Cask handles dependencies and build stuff... Ok
- Pallet intercepts the Emacs `:package-install` command such that it updates the Cask manifest for you and then runs `Cask install` for you, and probably something else(s) for you.

To me this is insane. In a normal world you just have `apm` `npm` `wahtever-pm` and call it a day. Oh, and there is no automatic and clean way to uninstall packages... Wow.

Melpa is here: http://melpa.org and it appears unlike a nice cli tool like `apm` for `atom` there is no cli-based search. There is in-emacs autocomplete when executing `:package-install <pkg>` but that is unacceptable as a discovery solution; we need more info! So, note the Melpa website at least for now.

#### Install Cask & Pallet
- Repo: https://github.com/cask/cask.
- Docs: http://cask.readthedocs.org/en/latest/

We have a bunch of things to do:
```sh
brew install cask
# Create a home for our Emacs userland files.
mkdir -p ./.emacs.d
# Then, we have to manually tell Cask about Pallet.
echo "(source melpa)\n\n(depends-on \"pallet\")" > ~/.emacs.d/Cask
# Then, we have to manually tell Cask to install Pallet
Cask install
# Then, we need to manually tell Emacs about Pallet and pallet.
# But first we need <path-to-cask>... That is in the root of where
# we installed Cask... We can use brew info to remember that root
brew info cask
# and then figure out to use: 
echo "(require 'cask \"/usr/local/Cellar/0.7.1/cask.el\")\n(cask-initialize)\n(require 'pallet)\n(pallet-mode t)" > ~/.emacs.d/init.el
# So we require Cask, then activate it, then require Pallet, then activate it. Ok.
```
