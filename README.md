# docs

Created: 16 Apr 2018

This repo is meant to store relevant documentation for Keck-FOBOS
development; e.g., white papers, proposals, SPIE papers, etc. **Be aware
that this repo is currently public.**

## Adding a new document

For now, even when just including an already finalized document
(presentation, paper, whatever), clone the repo, branch it, add the
document to the branch, and then perform a pull request to merge your
branch back into master:

```
git clone https://github.com/Keck-FOBOS/docs.git
cd docs
git checkout -b mybranch
cp /path/to/doc ./presentations/my_presentation.pdf
git add presentations/my_presentation.pdf
git commit -m 'adding my presentation'
git push
```

The last step merges your changes to the remote repository.  Then use
the GitHub interface to perform a pull request.

### Connecting this repo to an Overleaf project

When preparing new documentation, you can connect this repo to an
Overleaf repo as follows.  (This is a summary of procedures I adopted
from [here](https://abyvinod.github.io/gitsubmodules.html).)

As an example, I started the 2018 Keck white paper on Overleaf.  The
share button in the Overleaf menu bar gives the repo location as:

https://git.overleaf.com/15600261fykfjpznsdpz

I can then add the Overleaf as a submodule to this repo as follows.

```
cd ~/Work/FOBOS/repos/docs
git submodule add https://git.overleaf.com/15600261fykfjpznsdpz proposals/KeckWP_2018
# Make the parent repository ignore any future commits (Disable git submodule's tracking capabilities)
git config submodule.proposals/KeckWP_2018.ignore all
# Set ignore=all in .gitmodules to propagate this to remote repository of Papers
vim .gitmodules # Make appropriate changes
# Shift to master branch from a detached head state
cd proposals/KeckWP_2018
git checkout master
```

, please create a branch/fork of this repo,
write/edit the documentation and then perform a pull request to merge it
into master.



