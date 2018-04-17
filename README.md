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
% git clone https://github.com/Keck-FOBOS/docs.git
% cd docs
% git checkout -b mybranch
% cp /path/to/doc ./presentations/my_presentation.pdf
% git add presentations/my_presentation.pdf
% git commit -m 'adding my presentation'
% git push
```

### Connecting this repo to an Overleaf project

When preparing new documentation, you can connect this repo to the
Overleaf repo as follows.  (This is a summary of procedures I adopted
from [here](https://abyvinod.github.io/gitsubmodules.html).)

As an example, I started the 2018 Keck white paper on Overleaf.  The
share button in the Overleaf menu bar gives the repo location as:

https://git.overleaf.com/15600261fykfjpznsdpz

, please create a branch/fork of this repo,
write/edit the documentation and then perform a pull request to merge it
into master.



