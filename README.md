# docs

Created: 16 Apr 2018

This repo is meant to store relevant documentation for Keck-FOBOS
development; e.g., white papers, proposals, SPIE papers, etc. **Be aware
that this repo is currently public.**

## Cloning the full repo

This repo has submodules linked to Overleaf.  To pull across all the
submodule files as well as the main repo files, use the `--recursive`
option:

`git clone --recursive https://github.com/Keck-FOBOS/docs`

### Submodules

For reference, try to keep an up-to-date list of Overleaf links here:

| Directory             | Overleaf |
| --------------------- | ------------- |
| proposals/KeckWP_2018 | https://www.overleaf.com/15600261fykfjpznsdpz#/59256766/ |

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

Or you can send the document to me and I can put it directly on the
repo.

### Connecting this repo to an Overleaf project

When preparing new documentation, you can connect this repo to an
Overleaf repo as follows.  (Inspired by the description
[here](https://abyvinod.github.io/gitsubmodules.html).  Beware that
behavior may vary with different git versions.  I'm using version
2.17.0.)

As an example, I started the 2018 Keck white paper on Overleaf.  The
share button in the Overleaf menu bar gives the repo location as:

https://git.overleaf.com/15600261fykfjpznsdpz

I can then add the Overleaf document as a submodule to this repo as
follows.

```
cd ~/Work/FOBOS/repos/docs
git submodule add https://git.overleaf.com/15600261fykfjpznsdpz proposals/KeckWP_2018
cd proposals/KeckWP_2018
git checkout master
```

You can then treat the docs/proposals/KeckWP_2018 directory as you would
any other git repository.  **Be sure to pull/push often to make sure
that you're in sync with anyone making edits directly via the Overleaf
browser interface.**

The status of the main repository should also track changes in the
submodule.  I'll update this with details of any complications I run
into.

### Updating all submodules

You can update all the submodules to match their respective remote
repositories by running:

```
git submodule foreach git pull
```

### Removing the submodule

You can remove the submodule connection to the Overleaf project.  This
does **not** actually delete the project from Overleaf!  Using the
proposals/KeckWP_2018 as an example, you would do the following:

```
git submodule deinit proposals/KeckWP_2018
git rm proposals/KeckWP_2018    # This also removes the local copy!  Use --cached option to keep the local copy.
rm -fR .git/modules/proposals/KeckWP_2018
```


