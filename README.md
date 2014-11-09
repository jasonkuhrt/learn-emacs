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

