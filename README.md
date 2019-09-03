# docs

Created: 16 Apr 2018

Updated:  3 Sep 2019

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

Or you can send the document to me and I can put it directly on the
repo.

