
# FOBOS Design Documents

## Science Drivers

Document started 17 Apr 2018.  Linked to an Overleaf repo.

| Directory             | Overleaf |
| --------------------- | ------------- |
| science_drivers | https://www.overleaf.com/15611483cdhzxxhmcbps#/59306618/ |

### Add new science cases:

* Create a tex file in `science_drivers/src` called, e.g., `kinematic_weak_lensing.tex`
* The first line should be `\subsection{My Science Case Title}`
* Write the science case
* Include any bibtex references in `science_drivers/master.bib`
* Include the tex file in `science_drivers/ms.tex` using the input command within the Science Cases section.  E.g., `\input{kinematic_weak_lensing}`.

